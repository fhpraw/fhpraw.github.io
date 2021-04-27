---
layout: post
title:  "Minimal Arch Linux Installation"
date:   2021-04-23 22:37:00 +0700
categories: guide
---

## Prepare Partition

Using `cfdisk`, create partition plan based on table below:

| Partition | Size                          | Type                    | Mount |
| --------- | ----------------------------- | ----------------------- | ----- |
| /dev/sda1 | 260M                          | EFI System              | /efi  |
| /dev/sda2 | 20G (based on my RAM system)  | Linux Swap              | swap  |
| /dev/sda3 | rest of disk space            | Linux filesystem (root) | /     |

## Formating Partition

Format `sda1` EFI System partition to FAT32, `sda2` as swap, `sda3` as ext4

```shell
mkfs.fat -F32 /dev/sda1
mkswap /dev/sda2
mkfs.ext4 /dev/sda3
```

## Mount The File Systems and set swap

```shell
mount /dev/sda3 /mnt
mkdir /mnt/efi
mount /dev/sda1 /mnt/efi
swapon /dev/sda2
```

## Install minimum packages

```shell
pacstrap /mnt base base-devel linux linux-firmware vi
```

## Generate fstab

Generate fstab file

```shell
genfstab -U /mnt >> /mnt/etc/fstab
```

## Change root into the new system

```shell
arch-chroot /mnt
```

## Set Time Zone

```shell
ln -sf /usr/share/zoneinfo/[Region]/[City] /etc/localtime
hwclock --systohc
```

## Install some necessary packages

```shell
pacman -S networkmanager grub efibootmgr
```

## Set Localization

Edit `/etc/locale.gen` and uncomment `en_US.UTF-8 UTF-8` and generate

```shell
vi /etc/locale.gen
locale-gen
```

Edit `/etc/locale.conf`, set `LANG=en_US.UTF-8`

```shell
echo 'LANG=en_US.UTF-8' > /etc/locale.conf
```

## Set Network

Enable Network Manager at startup

```shell
systemctl enable NetworkManager
```

Edit `/etc/hostname`

```shell
echo 'yourhostname' > /etc/hostname
```

Edit `/etc/hosts`

```text
127.0.0.1     localhost
::1           localhost
127.0.1.1     yourhostname.localdomain yourhostname
```

## Set root password

```shell
passwd
```

## Set Boot Manager

Using GRUB

```shell
grub-install --target=x86_64-efi --efi-directory=/efi --bootloader-id=GRUB
grub-mkconfig -o /boot/grub/grub.cfg
```

## add user and configure sudo

add new user set to wheel group

```shell
useradd -m -g wheel youruser
passwd youruser
```

edit `/etc/sudoers` and uncomment this to allow wheel group execute as root:

```text
%wheel ALL=(ALL) ALL
```

## Reboot
