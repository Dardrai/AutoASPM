# AutoASPM (forke of https://github.com/notthebee/AutoASPM)

A Python script that automatically activates ASPM for all supported devices on Linux.

It parses the `lspci -vv` output to determine which ASPM level is supported by
a device (e.g. L0s, L0sL1 or L1).

## Dependencies

- `pciutils`
- `python3`
- `which`

## Usage in Proxmox

1. Clone this repository
2. Run `chmod +x ./autoaspm.py`
3. Run `./autoaspm.py`
4. Add `crontab -e` and `@reboot /root/AutoASPM/autoaspm.py > /dev/null 2>&1`

## Credits

- Luis R. Rodriguez for writing the original enable_aspm script:
  <https://www.uwsg.indiana.edu/hypermail/linux/kernel/1006.2/02177.html>
- z8 for his Python rewrite of the enable_aspm script: <https://github.com/0x666690/ASPM>
