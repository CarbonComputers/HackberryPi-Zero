### [How to increase the swapfile in RPi OS](https://pimylifeup.com/raspberry-pi-swap-file/)
For HackberryPi, I would recommend increasing the swap size to 2048MB(2GB)  

# Raspberry Pi Swap File Adjustment

This guide explains how to increase or decrease the swap file size on your Raspberry Pi. Adjusting the swap file can help your Pi handle more memory-intensive tasks.

## Instructions

1. **Disable the Current Swap**:
   ```bash
   sudo dphys-swapfile swapoff
   ```

2. **Modify Swap Configuration**:
   ```bash
   sudo nano /etc/dphys-swapfile
   ```
   Change `CONF_SWAPSIZE=2048` to your desired value in MB.

3. **Apply Changes**:
   ```bash
   sudo dphys-swapfile setup
   sudo dphys-swapfile swapon
   ```

For full instructions, visit [Pi My Life Up](https://pimylifeup.com/raspberry-pi-swap-file/).