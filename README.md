# expressvpn-gui
A fairly decent Linux GUI to interface with the official ExpressVPN app for Linux

Brandon Bourret - phatwares@cpan.org

I got tired of having to open up the console every time I wanted to interact with ExpressVPN for Linux (console-based is the only version they provide right now). So I wrote a dandy little GUI to interface with it instead.

Feature Overview:

Dashboard Panel - This area shows your current ExpressVPN connection status

   Current server location
   Button to open full list of all server locations
   Button to open advanced settings

VPN Server List - This area shows all available ExpressVPN servers

   Listed by country
   "Recommended" servers are starred in the list

Advanced Settings Panel - This area shows additional settings and information

   Set parameters including: auto-connect, preferred protocol, desktop notifications, etc.
   Option to reset the kernel WiFi module (a bug in the ExpressVPN app sometimes causes the kernel to stop recognizing the current WiFi device -
   this app will try to automagically detect your WiFi kernel driver and, with root permission, try to reset it)

System Tray Icon/Indicator - The app can be toggled to the system tray

   NOTE: You must have "libappindicator1" installed on your system (e.g. sudo apt-get install libappindicator1), and your system must support
   tray icons/notifiers (a few don't).
   Toggle the main GUI window
   Toggle the connection state
   Exit the main app and the tray icon/indicator

This app (and all others I publish so far) are PORTABLE APPS. That means there is no need for installation because all the program assets (images, fonts, .dll, and .so files) are packaged into the executable. Simply double-click and GO! Having said this, let me explain that some users may get a false positive warning about this app being a "Trojan". Why? Because when you execute the app, it unpacks all the aforementioned program assets into a temporary folder on your computer. Therefore, some anti-virus apps falsely identify this as malicious "Trojan Horse" activity. Please rest assured that this app is completely harmless - I would not put my real name on a malicious app.

I develop using ActivePerl (don't laugh, it's rapid development!) and "compile" with ActiveState's Perl Dev Kit (PDK).

Linux 64-bit: https://www.dropbox.com/s/yg5opf1g4ot6ifk/ExpressVPN-GUI?dl=0
