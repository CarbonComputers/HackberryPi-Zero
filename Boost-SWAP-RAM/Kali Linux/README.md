This is a important step to increase ram, otherwise the zero 2w often gets frozen while sudo apt update  & upgrades
### [How to increase the swapfile in Kali Linux](https://miloserdov.org/?p=2667)
For HackberryPi, I would recommend increasing the swap size to 2048MB(2GB) or more, check your distro for requirements

## How to add Swap file in Kali Linux
This guide provides steps to create or enlarge a swap file in Kali Linux, which can help manage system memory more efficiently, especially if RAM is limited.

## Instructions

1. **Check Current Swap**:  
   ```bash
   swapon --show
   ```

2. **Create a Swap File**:  
   ```bash
   sudo fallocate -l 10G /swapfile
   sudo chmod 600 /swapfile
   sudo mkswap /swapfile
   sudo swapon /swapfile
   ```

3. **Make Swap Permanent**:  
   Add to `/etc/fstab`:  
   ```plaintext
   /swapfile none swap defaults 0 0
   ```

4. **Adjust Swap Priority** (optional):  
   ```bash
   sudo swapon --priority 100 /swapfile
   ```

For detailed instructions, check the original guide [here](https://miloserdov.org/?p=2667).