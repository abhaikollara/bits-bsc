# SSH & SCP Cheatsheet — Secure Remote Access and File Transfer
#keywords: #SSH #SCP #SecureShell #encryption #publickey #privatekey #hostkey #known_hosts #DiffieHellman #/etc/ssh #ssh_config #sshd_config #port #identityfile #recursive

## Key Definitions
- SSH: Secure Shell protocol for encrypted remote login, command execution, and tunneling. #SSH
- SCP: Secure copy utility using SSH to transfer files/directories. #SCP
- Private key: Secret key file used for public-key authentication. #privatekey #publickey
- Public key: Key distributed to servers for verifying a client. #publickey
- Host key: Server’s key pair used by clients to verify server identity. #hostkey
- known_hosts: Client-side file storing host public keys to prevent MITM. #known_hosts
- /etc/ssh: System directory with SSH client/server configuration and keys. #/etc/ssh
- Moduli: File(s) containing primes for Diffie–Hellman key exchange. #DiffieHellman

## Formulas / Syntax Templates
- SSH connect: ssh [options] [user@]hostname [command]
- SCP copy: scp [options] source destination
- Remote path format: [user@]host:/absolute/or/relative/path
- Default SSH port: 22

## Common Options (quick)
- -p (ssh): specify port (e.g., -p 2000)  #port
- -i (ssh|scp): specify private key file (identity file)  #identityfile
- -r (scp): recursive copy for directories  #recursive
- -P (scp): specify port for scp (note: scp uses capital -P) — see note below

Note: SSH uses -p (lowercase) for port; scp historically uses -P (uppercase). Also scp’s -p (lowercase) preserves file times/modes.

## Key Algorithms / Concepts
- Authentication modes: password-based, public-key (key pair + optional passphrase). #publickey
- Host verification: client checks host key vs ~/.ssh/known_hosts to detect changes. #known_hosts
- Diffie–Hellman: key exchange method using primes from /etc/ssh/moduli to derive session keys. #DiffieHellman
- SSH daemon vs client: sshd (server) reads /etc/ssh/sshd_config; client reads /etc/ssh/ssh_config. #sshd_config #ssh_config

## /etc/ssh — Important Files (one-liners)
- ssh_config — global SSH client defaults. #ssh_config
- sshd_config — SSH server configuration (port, auth methods, allow/deny). #sshd_config
- moduli — primes for Diffie–Hellman key exchange. #moduli
- ssh_host_* (e.g., ssh_host_rsa_key, ssh_host_rsa_key.pub) — server private/public host keys. #hostkey
- known_hosts (client-side usually ~/.ssh/known_hosts) — stored remote host public keys. #known_hosts
- sshrc — optional script executed at login (server/client specific). #sshrc
- ssh_config.d / sshd_config.d — directories for included config fragments. #ssh_config.d #sshd_config.d

## Important Properties / Invariants
- Private key must be kept secret; set permissions (chmod 600) to avoid rejection. #privatekey
- Host key changes indicate possible MITM; verify out-of-band. #hostkey
- Key-based auth preferred over passwords; protect keys with passphrases. #publickey
- SSH defaults to port 22; changing port is obscurity, not security. #port
- scp follows source→destination order: swapping changes transfer direction. #SCP

## Quick Reference — Commands & Examples
- Connect (password auth): ssh user@example.com
- Connect (key + custom port): ssh -p 2000 -i ./key/key.txt user@BITSPilani
- Run remote command: ssh user@host 'ls -la /var/www'
- Copy local → remote: scp ./file.txt user@host:/remote/path
- Copy remote → local: scp user@host:/remote/file.txt ./localdir
- Copy directory recursively: scp -r ./dir user@host:/remote/dir
- SCP with port (correct): scp -P 2000 -r ./dir user@host:/remote/dir
  - Note: transcript used -p for scp port; correct OpenSSH scp flag is -P (uppercase). Lowercase -p preserves times/modes.
- Use identity file with scp: scp -i ./key/key.txt user@host:/file ./local
- View manuals: man ssh_config ; man sshd_config

## Security Best-Practices (short)
- Use key-based auth + passphrase-protected private keys. #publickey
- Keep SSH software/config up-to-date. #SSH
- Restrict RootLogin in sshd_config (e.g., PermitRootLogin no). #sshd_config
- Use strong ciphers; review /etc/ssh/ssh_config and /etc/ssh/sshd_config. #encryption
- Backup server host keys on reinstall to avoid host key mismatches. #hostkey

## Troubleshooting Tips (one-liners)
- Permission denied → check key permissions and correct user. #privatekey
- Host key mismatch → verify server identity; remove outdated entry in ~/.ssh/known_hosts to reconnect (but verify first). #known_hosts
- scp fails on port → try -P (uppercase) or verify server sshd port. #port

Keep this sheet handy for quick command syntax, config file names, and security checks during an open-book exam.