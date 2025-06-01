# ESP32-Auto-WiFi-Config-NTP-Clock-Sync-with-Web-Portal
This project enables an ESP32 to automatically connect to a previously saved WiFi network using EEPROM-stored credentials. If the connection fails, it launches a WiFi Access Point and hosts a captive web portal to collect new credentials. It also synchronizes time with an NTP server (pool.ntp.org) and prints current time over Serial.
