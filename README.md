# Install-MacOS-on-Virtual-Box-with-iso
This will show you how to install Mac OS on Virtual Box via an iso image that you create from Apple Store

1. Open the apple store and search for the version you want.  In this example it will be monterey 
2. Click on View and Get and then Download
3. After the download completes, quit the installer
4. Open a terminal and run this command, remember to change the name: hdiutil create -o /tmp/Monterey -size 14000m -volname Monterey -layout SPUD -fs HFS+J
5. Mount the created DMG: hdiutil attach /tmp/Monterey.dmg -noverify -mountpoint /Volumes/Monterey
6. Create the Install Media (This will take some time): sudo /Applications/Install\ macOS\ Monterey.app/Contents/Resources/createinstallmedia --volume /Volumes/Monterey --nointeraction
7. Once that step is completed, unmount the volume: hdiutil detach /volumes/Install\macOS\Monterey
8. Convert the DMG to ISO: hdiutil convert /tmp/Monterey.dmg -format UDTO -o ~/Desktop/Monterey.cdr
9. Rename the CDR to ISO: mv ~/Desktop/Monterey.cdr ~/Desktop/Monterey.iso
10. Create the virtual disk
11. Attach the ISO to the virtualbox
12. Now just select that ISO to boot from
13. Go through the setup.  When you get to the install screen, you need to create a new partition to install onto 
14. Select the harddisk to install to 
15. Choose Erase: 
16. Choose ADMS give it a name and then erase: 
17. Click Done and then exit the disk utility
18. You can now continue to install the OS
19. Go through the setup.  When you get to the install screen, you need to create a new partition to install onto
20. Select the harddisk to install to
21. Choose Erase
22. Choose ADFS give it a name and then erase
23. Click Done and then exit the disk utility
24. You can now continue to install the OS
