## Linux Boot process

Here's what linux boot process in short looks like:

        |       |       |                       |           |                           |                               |
Power on | BIOS | MBR/EFI | Bootloader (e.g grub) | Kernel | Initial RAM disk (Initramfs) | /sbin/init (parrent process) | Shell
