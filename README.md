# SliTazCustomBuilds 

For more information on the SliTaz OS, please visit and consider supporting their work: [SliTaz Official Webiste](https://slitaz.org)

SliTazCustomBuilds are not ISO install custom builds but, rather dd copy of either bootable usb drive image (ie: /dev/sdb) or just the partition image (/dev/sda1) which can be written to a Hard Drive partion or one of my GoDistro built USB drives. Only the drive image contains the bootrecorder and GRUB2 bootloader. Both types of dd image files are configured to function with GRUB2 bootloader. They are dd images of complete builds of various SliTaz flavor "partition" which can be written to a ext3 hard drive partiion. They use GRUB2 bootloader files and once the file is written to your parition you can run update-grub from another partition add the copied SliTazCustomBuild should be added to your GRUB booloader menu. It will show up as unkown linux.

**Basic procedure for installing SliTazCustomBuilds
Install partition version to Hard Drive partition:**

1. Using Gparted create a parition of at least 1GB (Recommend: 5GB+) and format it to ext3
2. Terminal: write dd image file to ext3 prepared partition: ```sudo dd if=/path-to-file/filename.img of=/dev/sdaX bs=1MB status=progress && sync```
3. open Gparted: A. Select correct partition; B. Unmount if its mouted, Right click: Unmount; C. Click Partition / Check / Checkmark to expand partition to full size.
4. Terminal: ```update-grub```
5. Reboot | Select your correct /dev/sdaX unknown linux from the GRUB2 bootloader menu list.
6. Login using username: linux | Password: linux123  (Note: you can also log in to root account (Not Recommended unless necessary: username: root | Password: root)
7. Click Applications --> System Tools --> Sakura Terminal --> blkid --> (Locate the correct partition identifier for your new SliTaz Custom Install, ie, /dev/sda2. Record UUID Number
8. Click Applications --> System Tools --> SliTaz Panel --> Green Person Icon to top righ --> username: root | Password: root --> Boot --> Summary --> **rcS.conf** --> VIEW (Verify UUID matches Terminal blkid UUID)
9. If UUID in Boot Settings **rcS.conf** does NOT match blkid: Click -> Edit --> replace UUID with correct number --> Save
10. Recommend Changing your account passwords: user account passord can be changed from the SliTaz Panel but, the root password has be changed using Terminal. 

Install USB Drive version with bootrecorder and GRUB bootloader installed (bootalbe) to a USB Thumb Drive:
1. Its always best to use Gparted and format the USB Drive to ext3 filesystem:
     Terminal --> sudo gparted --> Click on correct partition --> Partition --> Format to --> ext3 --> Click Checkmark (or return icon) on top menu --> Click Apply --> Close
   
Below are complete specifics about these builds. Each build will use the same usernames and passwords which can be change using the SliTaz Panel. They all built on ext3 filesystem.

Accout information:
username: linux  / password: linux123 | root username: root / root password: root

Architecture / OS configuration: 64bit / GTK2 / yad 0.40.0 with html widget

OS Specific: LX Panel LXDE | OpenBox | SliTaz Web Server - httpd - url: localhost or 127.0.0.1 | configure with php

Partition Preparation format: ext3 | Size: at least 1GB but, 5GB+ is recommended.

Recommend writting dd img file from a local hard drive parition only and not from a USB stick, cd-rom or netowrk drive. Note: your partition identifier such as /dev/sdaX will vary. 

**WARNING: USING THE WRONG DRIVE AND/OR PARITION IDENTIFIER WILL DESTROY YOUR DATA !! ** Verify 3 times your terminal command is correct.
  Writing dd image to hard drive partition:  In bash / sh termial: cd to directory containing the SliTazCustomBuild img file | ```sudo dd if=./filename.img of=/dev/sdX bs=1MB status=progress && sync```
  
**Installed Programs: (packages) / Preferences & Tools:** (This list will vary somewhat from build to build. Note: Its easy to install available packages using SliTaz Panel)

**Accessories:**
  1. Burn CD/DVD
  2. Galcutor
  3. Grab Screenshot
  4. Leafpad
  5. Nano Text Editor
  6. Remote Terminal
  7. Spreadsheet
  8. Time.is
  9. VNC Viewer
  10. Wiki Documents

**Development**
  1. Beaver Code Editor
  2. BitBucket Repositories
  3. CGI Shell Environment
  4. Dialog Example
  5. Icon Browser
  6. SliTaz bug report
  7. Vi Text Editor

**Documentation**
  1. Cookutils Documentation
  2. GNU Genral Public License
  3. System Documentation
  4. Tazinst manaul
  5. Tazlito manual
  6. TazPkg manual
  7. Tazusb manual

**Games**
  1. 2048 | Alien Invasion | Anyone | Arkanoid | Boulder Dash | Checkers | Chinese Checkers | Connect Four | Digger | Lode Runner
  2. Mahjong | Mine sweeper | NanoChess | Pacman | Racer | Same | Sokoban | Space Invaders | Sudoku | Tetris

**Graphics**
  1. Gcolor2 Color Selector
  2. GNU Image Manipulation Program GIMP
  3. Image Viewer
  4. mtPaint Image Editor
  5. Shutterbug screenshot

**Internet**
  1. Gemini project
  2. Local Web Server (localhost | 127.0.0.1)
  3. Midori
  4. Midori Private Browsing
  5. SCP Secure Copy
  6. TazIRC IRC client
  7. Twitter Micro-bloggin
  8. VPN/SSH

**Multimedia**
  1. Alsamixer Volume mixer
  2. Alsaplayer Audio Player
  3. Asunder CD Ripper
  4. Audio Editor mhWaveEditor
  5. Jamendo Music
  6. Video Player
  7. Video Player (fullscreeen)
  8. Web Radio

**Office**
  1. Encrypted paste tool
  2. ePDFView PDF Viewer
  3. Network printer
  4. SQLite SQL Engine
  5. Wikipedia Encyclopedia

**Preferences**
  1. Account Password
  2. Appearance GTK+
  3. Defualt Applications
  4. Desktop Preferences
  5. Desktop Session Settings
  6. File Manager
  7. Keyboard and Mouse
  8. Keyboard mapping
  9. Manage local packages
  10. Monitor Settings
  11. Openbox Configuration Manager
  12. Package Manager
  13. Popup Notifications
  14. Perferred Applications
  15. Set screensaver timeout
  16. Shell profile
  17. System language
  18. Time Zone configuration
  19. Wi-Fi configuration
  20. x defaults behavior

**System Tools**
  1. Boot Log Viewer
  2. Bulk Rename
  3. Create a LiveCD
  4. Create a LiveUSB
  5. File Manager PCManFM
  6. Gparted Partition Manager
  7. LXSession Log Out
  8. Sakura Terminal
  9. SliTaz Config Dialogs
  10. SliTaz Installer (Install to Hard Drive)
  11. SliTaz Panel
  12. Task Manager
  13. Thunar File Manager
  14. XTerm Terminal

**RUN** (Type in name of applicate in RUN BOX to launch it)

**busybox intergration**(Terminal) (for more information on all the busybox commands, [CLICK HERE](https://busybox.net)

Desktop 1 | Desktop 2 | add a new Desktop

**SliTaz Live** (Right Click Desktop)
  1. TazLiTo Livde CD Tool
  2. TazUSB LiveUSB Tool
  3. TazUSB Writefs (qzip)
  4. TazUSB Writefs (lzma)
  5. TazUSB Writefs (none)

