# Linux Group Management — Cheatsheet
#hashtags: #Linux #groups #groupmanagement #/etc/group #GID #groupadd #groupdel #gpasswd #usermod #getent #id #groups #permissions

---

## Key Definitions
- Group: collection of users used to manage permissions collectively. #groups
- /etc/group: default config file that stores group records. #/etc/group
- GID: Group ID, numeric identifier for a group. #GID
- Group member list: comma-separated usernames in field 4 of /etc/group. #groupmembership
- Orphan files: files whose group no longer exists after a group is deleted. #orphan

---

## /etc/group — Record format
Each line:  
group_name:password:GID:user_list  
- Example: wheel:x:10:root,alice,bob  
- Field 1 = name, Field 2 = (encrypted) password, Field 3 = GID, Field 4 = comma-separated members. #/etc/group

---

## GID ranges / notes
- System GIDs (reserved): historically 0–499; many modern distros use 0–999 (check distro). #GID  
- Use a GID ≥ 500 (or ≥1000 depending on distro) for normal groups. #GID

---

## Common commands (quick reference)
| Action | Command (synopsis) | Notes |
|---|---:|---|
| Create group | groupadd [-g GID] groupname | -g sets GID (lowercase). #groupadd |
| Delete group | groupdel groupname | Removing group may orphan files. #groupdel |
| Change group name/GID | groupmod [-n newname] [-g newGID] groupname | #groupmod |
| Add user to group (append) | usermod -aG group username | -a (append) + -G (supplementary groups). #usermod |
| Add/remove member (group-managed) | gpasswd -a username group / gpasswd -d username group | Useful for managing /etc/group membership. #gpasswd |
| Show group entry | getent group groupname || grep '^groupname:' /etc/group | Portable lookup. #getent |
| Show user's groups | id username  OR  groups username | id shows uid/gid and supplementary groups. #id #groups |

(Use root or sudo for administration commands.)

---

## Key Concepts / Short Tips
- Primary vs supplementary groups:
  - A user's primary group is stored in /etc/passwd (not /etc/group) — supplementary groups appear in /etc/group. #groups
- When deleting a group, files with that GID remain but the group name is gone (become orphans); system may reassign or require manual fix. #orphan
- Prefer gpasswd or usermod -aG to add users — avoid usermod -G without -a (it replaces supplementary groups). #usermod #gpasswd
- Verify GID assignment after group creation via getent group or /etc/group. #groupadd #getent

---

## Important Properties / Invariants
- /etc/group is authoritative for supplementary group membership.
- Membership list is comma-separated; empty list = no supplementary members.
- GIDs must be unique for distinct groups (OS enforces uniqueness). #GID
- System account GIDs should not be reused for regular user groups. #GID

---

## Quick Reference (one-liners)
- Create group with specific GID: sudo groupadd -g 1500 AWS1  #groupadd
- Add existing user to group (append): sudo usermod -aG AWS1 BITS1  #usermod
- Add user to group (alternate): sudo gpasswd -a BITS1 AWS1  #gpasswd
- Remove user from group: sudo gpasswd -d BITS1 AWS1  #gpasswd
- Delete group: sudo groupdel AWS1  #groupdel
- View group record: getent group AWS1  OR  grep '^AWS1:' /etc/group  #getent
- Show user groups: id BITS1  OR  groups BITS1  #id #groups

---

Keep this sheet for quick lookup of formats, flags, and common pitfalls when managing Linux groups.