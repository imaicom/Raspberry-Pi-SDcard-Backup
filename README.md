# Raspberry-Pi-SDcard-Backup for Mac

1. Put a copy the original SD card
2. Start the Terminal application
3. type "diskutil list"
4. Check the device of the SD card ( maybe /dev/disk3 )
5. type "diskutil unmountDisk /dev/disk3"
6. type "sudo dd if=/dev/disk3 of=~/Desktop/raspi.dmg bs=1m"
7. type "control-T"
8. Confirmation of remaining 
9. 32GB , Calculated as follows: ? byte / (32*10^9)
10. type "diskutil unmountDisk /dev/disk3"
11. end of backup
12. Put the copy destination SD card
13. type "diskutil unmountDisk /dev/disk3"
14. type "sudo newfs_msdos -F 16 /dev/disk3"
15. type "sudo dd if=~/Desktop/raspi.dmg of=/dev/rdisk3 bs=1m"
16. type "control-T"
17. 32GB , Calculated as follows: ? byte / (32*10^9)
18. type "diskutil unmountDisk /dev/disk3"
19. end of restore
