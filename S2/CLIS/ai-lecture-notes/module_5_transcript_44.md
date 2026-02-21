# smartmontools & smartctl — Disk Health Monitoring (Linux) Cheat Sheet

Keywords: #smartmontools #smartctl #SMART #disk #hdd #ssd #selftest #health #monitoring #linux #apt #smartattributes #selftestlog #temperature #disktemp

---

## Key Definitions
- #SMART — Self-Monitoring, Analysis, and Reporting Technology built into most modern drives.  
- #smartmontools — Package providing smartctl CLI to access SMART data.  
- #smartctl — Command-line tool to query and control SMART on drives.  
- #DevicePath — Block device path (e.g., /dev/sda) passed to smartctl.  
- #ShortSelfTest — Quick built-in SMART test (few minutes).  
- #LongSelfTest — Thorough SMART test (can take hours).  
- #SelfTestLog — Log of past SMART self-tests and results.  
- #SMARTAttribute — Individual health metric reported by SMART (e.g., temperature, reallocated sectors).

---

## Formulas / Command Syntax (quick)
- smartctl [options] <device>  
- Install (Debian/Ubuntu): `sudo apt-get install smartmontools`  #linux #apt  
- Basic info: `smartctl -i <device>`  #smartctl #info  
- Full SMART report: `smartctl -a <device>`  #smartctl #report  
- SMART attributes: `smartctl -A <device>`  #smartattributes  
- Run short test: `smartctl -t short <device>`  #shortselftest  
- Run long test: `smartctl -t long <device>`  #longselftest  
- Show self-test log: `smartctl -l selftest <device>`  #selftestlog  
- Check temperature (example): `smartctl -A <device> | grep -i temperature`  #temperature

---

## Key Concepts / Operations
- Install package: use distro package manager (e.g., apt).  #smartmontools  
- Query device info: `-i` returns model, serial, firmware.  #smartctl  
- Dump SMART data: `-a` shows attributes, error logs, self-test results.  #SMART  
- List attributes: `-A` gives per-attribute raw and normalized values.  #smartattributes  
- Run self-tests: `-t short` (quick) or `-t long` (thorough).  #selftest  
- Inspect self-test results: `-l selftest` displays history and outcomes.  #selftestlog  
- Extract temperature: use `-A` and text filtering (grep).  #disktemp  
- Interpretation rule: non-zero or rising attribute values may indicate problems.  #health #monitoring

---

## Important Properties / Invariants
- SMART is built into most HDDs/SSDs but may vary by vendor.  #SMART  
- Many SMART attributes are counters; increases or non-zero critical fields can signal failure.  #smartattributes  
- Short tests are fast but less thorough; long tests are comprehensive and slower.  #shortselftest #longselftest  
- smartctl usually requires root privileges (use sudo).  #linux  
- Device path is required and must be the correct block device (e.g., /dev/sda).  #DevicePath  
- Regular monitoring helps detect issues early and reduce data-loss risk.  #monitoring

---

## Quick Reference (scannable)
- Install: `sudo apt-get install smartmontools`  #apt  
- Info: `smartctl -i /dev/sdX`  — model, serial, firmware  #smartctl  
- Full dump: `smartctl -a /dev/sdX`  — attributes, logs, tests  #SMART  
- Attributes only: `smartctl -A /dev/sdX`  #smartattributes  
- Start short test: `smartctl -t short /dev/sdX`  — check later with selftest log  #shortselftest  
- Start long test: `smartctl -t long /dev/sdX`  #longselftest  
- View self-test log: `smartctl -l selftest /dev/sdX`  #selftestlog  
- Temperature: `smartctl -A /dev/sdX | grep -i temperature`  #temperature  
- Interpret: watch for increasing counters (e.g., reallocated sectors) and non-zero critical attributes.  #health

---

Tags for quick search: #smartmontools #smartctl #SMART #disk #hdd #ssd #selftest #health #monitoring #linux #apt #smartattributes #selftestlog #temperature

(End of cheatsheet)