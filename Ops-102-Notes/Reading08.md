# Reading 08
---
## What is an ISO File?
- An ISO file is a type of archive file that is treated as though it were a disk by the pc, it typically contains all the parts necessary to install and run a program on your PC. They can be extracted via decompression software like 7 zip. Unlike other archive files, like .zip and .rar, ISO files are typically meant to be used for installing software and are capable of being booted into, making them ideal for quick installation of Operating Systems and other crucial applications.
## How do you write an ISO file to a CD, DVD, or removable media (like a thumb drive)?
- You have several options when it comes to burning an ISO onto removable media, depending on the OS you are attempting to do so from. Windows presents you with the greatest number of options. Burning can be done through third party software, such as Rufus, which is designed to both format the USB drive in preparation to be burned, and then properly burns the file onto the device. Windows also has native software that will allow you to burn ISO files simply by double clicking the file and following the wizard that appears, or by copying and pasting the file onto the formatted drive.
## How do you create an ISO file?
- you would need to use a third-party tool and follow the process given by the application you choose. Some examples are WinCDEmu or the Windows media creation tool. Both seem to involve a process consisting of inserting the media you intend to create a copy of, copying the files on that media into a new directory, and using the application's process to convert the entire directory into an iso.
## How do you mount an ISO file?
- You would find the file in the file explorer, right click it, and on the drop-down menu that appears select "mount". This would allow you to view the file's contents in its new location. Alternatively, I learned this can be done in the command line on windows by entering Mount-DiskImage -ImagePath "PATH\TO\ISOFILE" and replacing "PATH\TO\ISOFILE" with the intended path and filename.
- difference between mounting and burning: "When you burn an ISO file to a DVD, it will create a DVD that is an exact duplicate of the file, including all the necessary code to allow the DVD to be bootable. If you mount the ISO file and then burn the files you see in there you will end up with a data DVD that is not bootable." - https://www.lifewire.com/mount-burn-iso-windows-8-10-3506971#:~:text=ISO%20Burning%20vs.-,Mounting,just%20the%20files%20on%20it.
--- 
## Things I want to know more about
- Why doesn't windows have native software for creating ISOs
- in what situation is an ISO more useful than an ova?
- when do you want to burn, and when do you want to mount?