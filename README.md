# remote-start
Remote power management tool for Linux machines via WoL and SSH.
Tested on Ubuntu Server 24.04 LTS
---
### System Requirements
##### Source Machine
- Netcat
- Wakeonlan package
- Outgoing SSH
##### Target Machine
- Wake On LAN enabled in BIOS
- Incoming SSH
### Config File
- The config file must be populated by information of the target device
- If the config file is renamed, alter the env_file variable in the wol file
Default:
```bash
env_file="config"  # Replace config with the name of the environment file (.env, device.conf, etc.)
```
### Usage
- Once fully configured, the wol file can control power to the target machine
```bash
wol up    # Sends magic packet to specified broadcast & MAC addresses
wol down  # Injects 'sudo poweroff' into the target machine via SSH
```
### Future Development
- Compatibility for WoL on multiple simultaneous devices is in development
