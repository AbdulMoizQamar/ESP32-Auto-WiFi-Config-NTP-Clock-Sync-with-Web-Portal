# ESP32-Auto-WiFi-Config-NTP-Clock-Sync-with-Web-Portal
This project enables an ESP32 to automatically connect to a previously saved WiFi network using EEPROM-stored credentials. If the connection fails, it launches a WiFi Access Point and hosts a captive web portal to collect new credentials. It also synchronizes time with an NTP server (pool.ntp.org) and prints current time over Serial.

📝 Description:
This project enables an ESP32 to automatically connect to a previously saved WiFi network using EEPROM-stored credentials. If the connection fails, it launches a WiFi Access Point and hosts a captive web portal to collect new credentials. It also synchronizes time with an NTP server (pool.ntp.org) and prints current time over Serial.

✅ Features:
🔌 Automatically connects to saved WiFi credentials from EEPROM
📶 If unavailable, sets up a WiFi Access Point and serves a web portal for credential input
📝 Stores new credentials in EEPROM and reboots
🌐 Uses NTP (pool.ntp.org) to fetch real-time clock info
⏰ Displays Hour, Minute, and Seconds on Serial Monitor
📡 EEPROM read/write logic for persistent network config
🖥️ Simple HTTP server via WebServer.h on port 80

⚙️ Libraries Used:
WiFi.h – ESP32 WiFi control
WebServer.h – Lightweight web server
HTTPClient.h – For future expansions (HTTP requests)
EEPROM.h – EEPROM read/write for WiFi credentials
time.h – NTP-based time synchronization

📋 How It Works:
Tries to read SSID & password from EEPROM
Connects to saved WiFi, if successful → shows time using printLocalTime()
If connection fails → sets up AP named "ElectronicsInnovation"
User can scan available networks and submit SSID/password
Credentials are stored in EEPROM and ESP restarts with new settings
Time is fetched from NTP server and shown in 12-hour format
