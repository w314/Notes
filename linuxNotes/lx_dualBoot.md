linux, windows, dualboot

# How to create windows ubuntu dual boot machine

## Sources

- [best for createing dual boot - freecodecamp](https://www.freecodecamp.org/news/how-to-dual-boot-windows-10-and-ubuntu-linux-dual-booting-tutorial/)
- [how to create windows-ubuntu shared storage drive](https://helpdeskgeek.com/how-to/how-to-create-a-shared-storage-drive-for-dual-boot-systems/)
- [askubuntu: dual boot](https://askubuntu.com/questions/1445518/guide-to-dual-boot-windows-11-ubuntu-with-shared-storage)
- [linuxtechi: dual boot](https://www.linuxtechi.com/dual-boot-ubuntu-22-04-and-windows-11/)
- [linuxsimply: dual boot](https://linuxsimply.com/linux-basics/os-installation/dual-boot/windows-11-and-ubuntu/)

## Steps to follow

Used [freecodecamp guide](https://www.freecodecamp.org/news/how-to-dual-boot-windows-10-and-ubuntu-linux-dual-booting-tutorial/)

### 1. Check if BIOS is in UEFI mode
For the two operating system to see each other you `BIOS` has to be in `UEFI` mode.

To check the mode of your BIOS search for `system information` and `BIOS mode`.

### 2. Create Ubuntu Bootable USB Drive

Download `Ubuntu` in `ISO image`format from Ubuntu distro website.

Create Ubuntu Bootable USB Drive:

- download [Rufus](https://rufus.ie/en/) bootalbe USB drive creator
- run `Rufus` as administrator when creating the image, otherwise you'll get a:<br>
`error: file /casper/val inuz not found.`

### 3. Create Partitions

#### 3.1 create partition for linux

#### 3.2 create partition for shared storage drive

### 4. install ubuntu


After installing Ubuntu and trying to open windows again, first it wanted a Bitlocker recovery key. It could be found on the my microsoft account as the instructions on the screen said.

