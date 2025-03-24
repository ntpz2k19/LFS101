## Linux Boot process

Berikut gambaran proses booting operasi sistem linux pada komputer x86:

Power on -> BIOS -> MBR/EFI -> Bootloader (e.g grub) -> Kernel -> Initial RAfM disk (Initramfs) -> /sbin/init (parrent process) -> Shell

### BIOS

Saat komputer di hidupkan, Bios terinisialisasi, termasuk layar, keyboard, dan memory test.

### MBR/EFI

Setelah dari BIOS, proses dialihkan ke Bootloader, entah itu dari boot sector (MBR/Legacy) atau partisi EFI (Unified Extensible Firmware Interface), di proses ini mesin belum mengakses penyimpanan apapun, lalu informasi seperti tanggal, waktu, dan komponen penting lainya di dimuat dari CMOS.

### Bootloader

Untuk system MBR, bootloader disimpan di 512 byte pertama di dalam disk, bootloader ini memproses partition table dan mencari bootable partition, setelah menemukan bootable partition, bootloader memasuki fase kedua bootloader, semisal GRUB, dan memuatnya ke RAM.

Untuk system UEFI, UEFI firmware akan membaca boot manager data untuk menentukan aplikasi UEFI mana yang akan dijalankan. lalu firmware akan menjalankan aplikasi UEFI semisal GRUB.

### Initramfs & kernel

Initramfs adalah file system binary yang menjalankan mount filesystem, menjalankan fungsionalitas kernel, driver. program ini terletak di /sbin/init .

dalam sistem init ini daemon akan di jalankan, di linux umumnya digunakan sysvinit dan systemd.

### tty

singkatan dari TeleTYpewriter, merupakan Login interface menggunakan text. 
