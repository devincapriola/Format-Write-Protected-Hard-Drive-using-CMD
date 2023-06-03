# Format Write-Protected Hard Drive using CMD

## Introduction
This guide will walk you through the process of removing the write protection attribute from a hard drive using Command Prompt (CMD). By following these steps, you will be able to clear the write protection and format the hard drive for further use.

Please note that performing these actions will erase all data on the selected hard drive. Ensure that you have backed up any important files before proceeding.

## Instructions

1. **Launch Command Prompt**: Click on the "Start" menu and type "cmd.exe" into the search field. Double-click on "Command Prompt" to open the program.

2. **Access Diskpart**: In the Command Prompt window, type the following command and press "Enter":
```
$ diskpart
```
3. **List Disks**: To view the list of available disks on your system, enter the following command and press "Enter":
```
$ list disk
```

Identify the disk number of the write-protected hard drive from the displayed list.

4. **Select the Disk**: Use the following command to select the write-protected disk, replacing `#` with the appropriate disk number (e.g., Disk 1), and then press "Enter":
```
$ select disk #
```

5. **Clear Write Protection**: To remove the write protection attribute from the selected disk, enter the following command and press "Enter":
```
$ attributes disk clear readonly
```

At this point, the write protection attribute will be removed from the disk.

6. **Format the Disk**: To proceed with formatting the disk, enter the following commands one by one, pressing "Enter" after each command:
```
$ clean
$ create partition primary
$ format fs=ntfs
$ exit
```

The above commands will clean the disk, create a primary partition, and format it with the NTFS file system.

7. **Completion**: After executing the formatting command, the hard drive will be successfully formatted and can be used without write protection.

## Conclusion
By following the steps outlined in this guide, you have successfully removed the write protection attribute from a hard drive using CMD and formatted it for further use. Remember to exercise caution while executing these commands, as they can result in data loss. Always ensure that you have backed up any important files before proceeding with disk formatting.
