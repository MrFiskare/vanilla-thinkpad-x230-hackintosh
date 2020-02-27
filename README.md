# READ ME

This is an ongoing home project.
I would not <ins>yet</ins> recommend you to use it for your specific hardware.

![work-is-in-progress](https://pngimg.com/uploads/under_construction/under_construction_PNG18.png)

## BIOS Settings

These generic settings are just collected in order to prevent any compatibility issues. They shoud be kept in mind with [any laptop](https://fewtarius.gitbook.io/laptopguide/before-you-start/bios-configuration) that you're trying to install macOS on.

For further BIOS settings check: [Bizzaro's git](https://github.com/Bizzaro/x230-osx)

| Item | Setting |
| ------ | ------ |
| Secure Boot | Disabled |
| TPM * | Disabled |
| VT-D | Disabled |
| DVMT-Prealloc | 64MB *(if possible)* |
| SATA/AHCI/RAID | AHCI |
| Legacy USB support | Enabled |
| EHCI/XHCI Hand-off | Enabled |
| Fast Boot | Disabled |
| Wake on Lan | Disabled |
| Fingerprint Scanner | Disabled *(if present)* |
| SD Card Reader ** | Disabled *(if present)* |

*Trusted Platform Module - According to [this page](https://wiki.archlinux.org/index.php/Lenovo_ThinkPad_X230#Trusted_Platform_Module) it should be located in *Security > Security Chip > Security Chip*

**Security Tab, and then I/O Port Access option

[source 1](https://fewtarius.gitbook.io/laptopguide/before-you-start/bios-configuration) – [source 2](https://github.com/Bizzaro/x230-osx) – [source 3](https://wiki.archlinux.org/index.php/Lenovo_ThinkPad_X230#Trusted_Platform_Module)

## Which macOS to use?

At the pre-alpha version I am using macOS Catalina 10.15.3.
Hopefully this repo is going to end up a rock solid, update-proof collection kexts, and fixes.

TO DO: clover updater script

## Getting started with Clover

My repo aims to use the newest Clover Bootloader release available at [CDB](https://cloverdb.com).
The current newest version is [v2.5 r5103](https://github.com/Dids/clover-builder/releases/tag/v2.5k_r5103). My pre-alpha is based on the files inside the *CloverISO-5103.tar.lzma*.

##### Extracting .tar.lzma archives

###### On Linux *(mounting to /tmp/iso)*:

```sh
$ sudo apt install lzma
$ unlzma ~/Downloads/Clover*.tar.lzma
$ tar -xvf ~/Downloads/Clover*.tar
$ sudo mkdir /tmp/iso
$ sudo mount ~/Downloads/Clover*.iso /tmp/iso/ -o loop
```

###### On Mac:
Use [The Unarchiver](https://theunarchiver.com). After that, you'll be able to double click and open the ISO file.

##### Creating Clover structure

Once you're done with extracting the files you should create a barbone Clover structure using [this guide](https://fewtarius.gitbook.io/laptopguide/prepare-install-macos/preparing-the-usb-media#create-the-clover-structure)



[Source 1](https://cloverdb.com/) – [Source 2](https://github.com/Dids/clover-builder/releases/tag/v2.5k_r5103) – [Source 3](http://www.e7z.org/open-lzma-tlz.htm) – [Source 4](https://fewtarius.gitbook.io/laptopguide/prepare-install-macos/preparing-the-usb-media#create-the-clover-structure)

## macOS Memory Allocation

I used *OCQuirks* to fix memory allocation issues. Keep in mind that it depends on the *FwRuntimeServices.efi* driver. Copy these files to your *EFI/CLOVER/drivers/UEFI* folder.

