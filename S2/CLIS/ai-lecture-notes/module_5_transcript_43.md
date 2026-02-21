# Disk Tools Cheatsheet — cfdisk, sfdisk, smartctl
#hashtags: #cfdisk #sfdisk #smartctl #partitioning #SMART #disks #linux #storage #console #scriptable #io-redirect #sudo #root

---

## Key Definitions
- cfdisk: Interactive, console-based disk partitioning utility.
- sfdisk: Scriptable partitioning utility for programmatic partition table edits.
- smartctl: SMART (Self-Monitoring, Analysis and Reporting Technology) control/monitoring tool for storage devices.
- Partition table: Metadata describing disk partitions (MBR/GPT).
- IO redirection: Shell operators `<` (input) and `>` (output) used to feed or capture command I/O.

---

## Syntax / Commands (Formulas & Examples)
- Run cfdisk (interactive):  
  sudo cfdisk /dev/sdb
- sfdisk from script (create partitions):  
  sudo sfdisk /dev/sdb < partition_script.txt
- sfdisk dump partition table to file:  
  sudo sfdisk -d /dev/sdb > partition_table.txt
- smartctl show all info:  
  sudo smartctl -a /dev/sda
- smartctl device info / SMART support:  
  sudo smartctl -i /dev/sda
- smartctl run short test:  
  sudo smartctl -t short /dev/sda
- smartctl view self-test results:  
  sudo smartctl -l selftest /dev/sda

(Note: most operations require root — use sudo.)

---

## Key Algorithms / Concepts
- #cfdisk: Menu-driven steps — New, Delete, [Type], Write, Quit — good for ad-hoc interactive partitioning.
- #sfdisk: Text-based, repeatable partitioning via scripts; ideal for automation and imaging.
- #smartctl: Query device SMART attributes, run self-tests, review logs to assess drive health.
- #IO-redirection: Use `<` to feed scripts into sfdisk; use `>` to capture sfdisk dumps or smartctl output.

---

## Important Properties / Invariants
- cfdisk changes are not persisted until you select Write and confirm (e.g., "yes").
- sfdisk modifies partition table based on input script — non-interactive and destructive if script is wrong.
- smartctl commands depend on device SMART support — use `smartctl -i` to verify.
- Always operate on device nodes (e.g., /dev/sda, /dev/sdb), not mounted filesystem paths.
- Partitioning operations can cause data loss — always backup before modifying.
- SMART tests take time (short/long); check results with `-l selftest`.

---

## Quick Reference (scannable)
- Interactive partitioning:
  - Command: sudo cfdisk /dev/<disk>
  - UI actions: New → size/type, Delete → select, Write → confirm, Quit
- Scripted partitioning:
  - Create: sudo sfdisk /dev/<disk> < partition_script.txt
  - Dump: sudo sfdisk -d /dev/<disk> > partition_table.txt
- SMART monitoring:
  - Info/support: sudo smartctl -i /dev/<disk>  #check SMART capability
  - Full attributes: sudo smartctl -a /dev/<disk>
  - Start short test: sudo smartctl -t short /dev/<disk>
  - Show self-test log: sudo smartctl -l selftest /dev/<disk>
- Common device names: /dev/sda, /dev/sdb, /dev/nvme0n1 (NVMe devices may require different device paths/options)
- Safety checklist before partitioning:
  - Backup important data
  - Unmount partitions on target disk
  - Confirm target device name (avoid /dev/sda mix-ups)
  - Use scripts with dry-run / verification where possible

---

## Quick Command Table
| Tool | Purpose | Key flags / usage |
|---|---:|---|
| cfdisk | Interactive partition editor | sudo cfdisk /dev/sdX — use menu: New/Delete/Write |
| sfdisk | Scriptable partitioning | sudo sfdisk /dev/sdX < script.txt ; sudo sfdisk -d /dev/sdX > table.txt |
| smartctl | SMART monitoring & tests | sudo smartctl -i/-a/-t short/-l selftest /dev/sdX |

---

Keep this sheet open during the exam for fast lookup of command syntax, flags, and safety reminders.