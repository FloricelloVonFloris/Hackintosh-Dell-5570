# Hackintosh-Dell-5570

Overview:

Hello everyone! Floricello have created an updated EFI file for Dell Inspiron 5570. There are two parts of EFI files because I can't upload the entire EFI folder as one ZIP file. After downloading, simply merge them together!

Updates:
1. OpenCore Version updated to 0.9.5 and works perfectly with macOS Ventura!
2. Drivers and Tools are updated to the latest version!
3. HDMI Output fixed! (Thanks to AJ!)
4. ACPIs updated:
	4.1. SSDT-ALS0.aml
	4.2. SSDT-EC-USBX-LAPTOP.aml
	4.3. SSDT-PLUG-DRTNIA-aml
	4.4. SSDT-PNLF.aml
	4.5. SSDT-XOSI-aml
5. Kexts updated! The following kexts are not updated:
	5.1. AirportItlwm-Ventura.kext
	5.2. CtlnaAHCIPort.kext
	5.3. RealtekRTL8100.kext
	5.4. VerbStub.kext
	5.5. UTBMap.kext
	5.6. AppleBacklightSmoother.kext
	5.7. ApplePS2SmartTouchPad.kext

Important Information:
1. Be sure to perform BIOS Editing first on your Dell Inspiron 5570 (WARNING! EXTREMELY DANGEROUS! I'll not be held responsible, do this on your own risk!)
2. Serial Number and UUID must be generated for your own personal use!
3. When using this EFI as a EFI for installing macOS Ventura using bootable USB Installer:
    2.1. Always enable "Show Picker".
    2.2. Always set Scan Policy to zero.

Credits to the following:
- AJ (https://www.youtube.com/watch?v=q8esNA6uu0M)
- crystall1nedev (https://github.com/crystall1nedev)
