# Hackintosh-Dell-Inspiron-5570

Overview:

Hello everyone! Floricello have created an updated EFI file for Dell Inspiron 5570. There are two parts of EFI files because I can't upload the entire EFI folder as one ZIP file. After downloading, simply merge them together!

My Dell Inspiron 5570 Speficications:
1. Intel Core i5-8250U
2. Intel UHD Graphics 620, 15.6”, Full HD (1920 x 1080),
3. 1000GB HDD
4. 32GB DDR4, 2400 MHz
5. Fenvi BCM94360NG WiFi+Bluetooth Module

Updates: for v.1.1.0 (November 2023)
1. Still OpenCore Version 0.9.5., but now works perfectly with macOS Sonoma! (Please make sure to generate or use your own Serial Number and UUID)
2. Patched to make BCM94360NG working again on macOS Sonoma.
3. Source for work-around for the BCM94360NG: https://github.com/5T33Z0/OC-Little-Translated/blob/main/14_OCLP_Wintel/WIiFi_Sonoma.md
4. The work-around for the BCM94360NG has been already done!

However, after adopting my new EFI into your own Dell Inspiron 5570 doesn't automatically makes your own BCM94360NG work in an instant! Follow the next step for the things you still need to do:
1. Open Terminal App and enter the command: sudo spctl --master-disable
2. Download the latest copy of OpenCore Legacy Patcher and run the app!
3. Click Post-Install Root Patch
4. Let the installation go on its own.
5. Reboot and clear the NVRAM upon reboot! (Steady press the ALT key upon reboot then select Clear NVRAM, then restart your laptop again).
6. Let it boot on its own.
7. Enjoy!

However, there will be a time that when a new macOS updates comes and after installing it, the BCM94360NG will not work again. Just follow these steps:
1. Open Terminal App and enter the command: sudo spctl --master-disable
2. Reboot and clear the NVRAM upon reboot! (Steady press the ALT key upon reboot then select Clear NVRAM, then restart your laptop again).
3. Let it boot on its own.
4. Enjoy!




========================================== Older Updates ==========================================

Updates: for v1.0.0 (September 2023)
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
   The following must be directly edited on the BIOS: (I assume you have some expertise with Hackintoshing and BIOS editing, so I will not explain further
   about this!)
   
	1.1. DVMV PRE-ALLOCATED set to 64MB: setup_var 0x795 0x2
   
	1.2. DVMT TOTAL GFX MEM set to MAX: setup_var 0x796 0x3
   
	1.3. CFG Lock set to Disabled: setup_var 0x4ED 0x0
   
	1.4. I2CO INTERUPT MODE set to GPIO Interrupt: setup_var 0x272 0x0
   
3. Serial Number and UUID must be generated for your own personal use!
4. When using this EFI as a EFI for installing macOS Ventura using bootable USB Installer:
    2.1. Always enable "Show Picker".
    2.2. Always set Scan Policy to zero.

Credits to the following:
- AJ (https://www.youtube.com/watch?v=q8esNA6uu0M)
- crystall1nedev (https://github.com/crystall1nedev)
- Mateo1234454545 (https://github.com/Mateo1234454545)
