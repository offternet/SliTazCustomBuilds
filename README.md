# SliTazCustomBuilds 

(For more information on the SliTaz OS, please visit and consider supporting their work: [SliTaz](htts://slitaz.org)

SliTazCustomBuilds are not ISO install custom builds but, rather dd copy of either bootable usb drive image (ie: /dev/sdb) or just the partition image (/dev/sda1) which can be written to a Hard Drive partion or one of my GoDistro built USB drives. Only the drive image contains the bootrecorder and GRUB2 bootloader. Both types of dd image files are configured to function with GRUB2 bootloader. They are dd images of complete builds of various SliTaz flavor "partition" which can be written to a ext3 hard drive partiion. They use GRUB2 bootloader files and once the file is written to your parition you can run update-grub from another partition add the copied SliTazCustomBuild should be added to your GRUB booloader menu. It will show up as unkown linux.

Basic Shema for installing SliTazCustomBuilds:
1. Using Gparted create a parition of at least 1GB (Recommend: 5GB+) and format it to ext3
2. Terminal: write dd image file to ext3 prepared partition: ```sudo dd if=/path-to-file/filename.img of=/dev/sdaX bs=1MB status=progress && sync```
3. open Gparted: A. Select correct partition; B. Unmount if its mouted, Right click: Unmount; C. Click Partition / Check / Checkmark to expand partition to full size.
4. Terminal: ```update-grub```
5. Reboot | Select your correct /dev/sdaX unknown linux from the GRUB2 bootloader menu list.
6. Login using username: linux | Password: linux123  (Note: you can also log in to root account (Not Recommended unless necessary: username: root | Password: root)
7. Click Applications --> System Tools --> Sakura Terminal --> blkid --> (Locate the correct partition identifier for your new SliTaz Custom Install, ie, /dev/sda2. Record UUID Number
8. Click Applications --> System Tools --> SliTaz Panel --> Green Person Icon to top righ --> username: root | Password: root --> Boot --> Summary --> **rcS.conf** --> VIEW --> Verify UUID matches Terminal blkid UUID.
9. If UUID in Boot Settings rcS.conf is not correct: --> Edit --> replace UUID with correct number --> Save
10. Recommend Changing your account passwords: user account passord can be changed from the SliTaz Panel but, the root password has be changed using Terminal. 

Below are complete specifics about these builds. Each build will use the same usernames and passwords which can be change using the SliTaz Panel. They all built on ext3 filesystem.

Accout information:
username: linux  / password: linux123 | root username: root / root password: root

Architecture / OS configuration: 64bit / GTK2 / yad 0.40.0 with html widget

Partition Preparation format: ext3 | Size: at least 1GB but, 5GB+ is recommended.

Recommend writting dd img file from a local hard drive parition only and not from a USB stick, cd-rom or netowrk drive. Note: your partition identifier such as /dev/sdaX will vary. 

**WARNING: USING THE WRONG DRIVE AND/OR PARITION IDENTIFIER WILL DESTROY YOUR DATA !! ** Verify 3 times your terminal command is correct.
  Writing dd image to hard drive partition:  In bash / sh termial: cd to directory containing the SliTazCustomBuild img file | ```sudo dd if=./filename.img of=/dev/sdX bs=1MB status=progress && sync```
  
Installed Programs:
Accessories:
  1. Burn CD/DVD
  2. Galcutor
  3. Grab Screenshot
  4. Leafpad
  5. Nano Text Editor
  6. Remote Terminal
  7. Spreadsheet
  8. Time.is
  9. VNC Viewer
  10. 

