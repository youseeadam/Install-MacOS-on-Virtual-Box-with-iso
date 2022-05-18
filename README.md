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
16. Choose APFS give it a name and then erase: 
17. Click Done and then exit the disk utility
18. You can now continue to install the OS
<ul>
<li>MacOS Monterey 12 (<a href="http://swcdn.apple.com/content/downloads/39/60/002-23774-A_KNETE2LDIN/4ll6ahj3st7jhqfzzjt1bjp1nhwl4p4zx7/InstallAssistant.pkg" target="_blank" rel="noopener">Direct link to InstallAssistant.pkg</a>, <a href="https://apps.apple.com/us/app/macos-monterey/id1576738294" target="_blank" rel="nofollow noopener">App Store link</a>)</li>
<li><a target="_blank" rel="nofollow noopener noreferrer" href="https://support.apple.com/en-us/HT201475">macOS Big Sur 11</a> (<a target="_blank" rel="nofollow noopener noreferrer" href="https://apps.apple.com/us/app/macos-big-sur/id1526878132?mt=12">App Store link</a>)</li>
<li><a target="_blank" rel="nofollow noopener noreferrer" href="https://support.apple.com/kb/HT201475">macOS Catalina 10.15</a> (<a target="_blank" rel="nofollow noopener noreferrer" href="https://itunes.apple.com/us/app/macos-catalina/id1466841314?ls=1&amp;mt=12">App Store link</a>)</li>
<li><a target="_blank" rel="nofollow noopener noreferrer" href="https://support.apple.com/kb/HT210190">macOS Mojave 10.14</a> (<a target="_blank" rel="nofollow noopener noreferrer" href="https://itunes.apple.com/us/app/macos-mojave/id1398502828?ls=1&amp;mt=12">App Store link</a>)</li>
<li><a target="_blank" rel="nofollow noopener noreferrer" href="https://support.apple.com/kb/HT208969">macOS High Sierra 10.13</a> (<a target="_blank" rel="nofollow noopener noreferrer" href="https://itunes.apple.com/us/app/macos-high-sierra/id1246284741?ls=1&amp;mt=12">App Store link</a>)</li>
<li><a target="_blank" rel="nofollow noopener noreferrer" href="https://support.apple.com/kb/HT208202">macOS Sierra 10.12</a> (<a target="_blank" rel="nofollow noopener noreferrer" href="http://updates-http.cdn-apple.com/2019/cert/061-39476-20191023-48f365f4-0015-4c41-9f44-39d3d2aca067/InstallOS.dmg">Direct DMG download link</a>)</li>
<li><a target="_blank" rel="nofollow noopener noreferrer" href="https://support.apple.com/kb/HT206886">OS X El Capitan 10.11</a> (<a target="_blank" rel="nofollow noopener noreferrer" href="http://updates-http.cdn-apple.com/2019/cert/061-41424-20191024-218af9ec-cf50-4516-9011-228c78eda3d2/InstallMacOSX.dmg">Direct dmg download link</a>)</li>
<li><a target="_blank" rel="nofollow noopener noreferrer" href="https://support.apple.com/kb/HT210717">OS X Yosemite 10.10</a> (<a target="_blank" rel="nofollow noopener noreferrer" href="http://updates-http.cdn-apple.com/2019/cert/061-41343-20191023-02465f92-3ab5-4c92-bfe2-b725447a070d/InstallMacOSX.dmg">Direct download link</a>)</li>
<li><a href="https://support.apple.com/kb/DL2076?locale=en_US" target="_blank" rel="Nofollow noopener">Mac OS X Mountain Lion 10.8</a></li>
<li><a href="https://support.apple.com/kb/DL2077?locale=en_US" target="_blank" rel="nofollow noopener">Mac OS X Lion 10.7</a></li>
</ul>
