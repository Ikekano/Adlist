# Pi-Hole AdList
Adlist and setup of Pi-hole in case it corrupts itself again

# Installation
## 1. Install Raspberry Pi OS Lite (64-bit)
Use Raspberry Pi Imager to install **Raspberry Pi OS Lite (64-bit)** on an SD Card

1. Select The Raspberry Pi Device being used
2. Select **Raspberry Pi OS Lite (64-bit)**
3. Select the SD card device for storage (Typically the SD Card Reader) -> Verify that the reported size matches that of the SD Card (32GB, 64GB, etc...)
4. Click **[Next]**
5. When prompted to **Use OS Customization** click **[EDIT SETTINGS]**
      - Set Username and Password to desired values (e.g. Username: pi-hole , Password: piholepasswd1)
      - Configure WLAN with SSID and Password of WiFi
      - Verify the **time zone** is correct
6. Click **[Save]**
7. Click **[YES]** to Apply OS Customisation Settings
8. Verify that data will be erased on the correct device
9. Click **[YES]** to begin writing to the SD Card  


## 2. Setting Up Pi-Hole

1. Plug Keyboard into Pi and insert finished SD Card
2. Boot the Pi with a monitor and use the login that was made using the Pi Imager in step 5 when prompted for a login
3. Use the following command to begin the setup script:

```
curl -sSL https://install.pi-hole.net | bash
```

4. Once the installer is loaded (Blue Screen) follow the prompts
      - In regards to the **Static IP**, if the DHCP is handled by the router and the Pi-hole is **NOT** the one responsible for DHCP assignments, then continue without assigning a static IP.
5. Select **eth0** for ethernet or **wlan0** for wifi interface (Ethernet is Preferred)
6. Select one of the upstream DNS servers (Google or Cloudflare are fine)
7. Continue through the prompts until the installation is complete

