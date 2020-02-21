# READ ME

This is an ongoing home project.
I would not <ins>yet</ins> recommend you to use it for your specific hardware.

### BIOS Settings

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
