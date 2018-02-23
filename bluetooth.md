# Usage
## Make the first bluetooth device discoverable

1. Make the device discoverable

   ```bash
   sudo su -c "echo 1 > /sys/devices/platform/thinkpad_acpi/bluetooth_enable"
   sudo hciconfig hci0 up
   sudo hciconfig hci0 piscan
   ```
2. Check the status of the device

   ```bash
   echo show | bluetoothctl 2> /dev/null
   ```

   https://fixmynix.com/bluetooth-in-linux-with-bluez-and-hcitool/
   http://superuser.com/questions/940947/trying-to-enable-bluetooth-on-startup-debian

## Change the alias/name of a bluetooth device

1. Temporarily

   ```bash
   sudo hciconfig hci0 name <Device Name>
   ```

2. Permanently

   1. Change the name of the device in /var/lib/bluetooth/{device name}/config
   2. Change the alias of the device in /var/lib/bluetooth/{device name}/settings
   3. ```bash
      sudo service bluetooth restart
      ```
