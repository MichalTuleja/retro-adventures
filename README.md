# Retro Adventures

## DOS 6.22

## Virtualization/Emulation

Running DOS on the modern hardware is fairly easy. There are multiple solutions for the x86 architecture.

- VirtualBox supports DOS out of the box. It emulates generic VESA graphics card, SoundBlaster 16, PS/2 mouse.
- QEMU allows using Cirrus Graphics card 
- For the ARM-based MacOS consider UTM. It is QEMU-based with a nice UI.
- VMware supports DOS out of the box
- PCem offers better compatibility but requires a good hardware.
- DOSBox is a great and efficient way to emulate DOS. You can choose it if your plan on running only DOS.

## Real Hardware

Finding a good hardware for DOS can be a headache, despite being the main system for a PC for over a decade. Finding parts is becoming a real challenge and prices of working hardware are rising.

On the other hand it is not difficult to run DOS on a much newer hardware which due to backwards compatibility of the whole PC platform. Virtually any combination up to XP-Era worked for me. There are several caveats however.

- AGP graphics cards usually do not support SVGA modes. These chips support SVGA on DOS:
    - Trident
    - Cirrus Logic
	- S3 Trio/Virge
	- Mach32/Mach64
- Lack of ISA slots makes it difficult to find a SB16-compatible sound card. The problem with sound under DOS originates from the hardware limitation that requires being at the certain hardware address, IRQ and DMA combination. DOS does not support any drivers, programs were shipped with certain drivers. 
Hardware manufactures were required to deliver a product that would offer certain compatibility. 
Comparing to nowadays standards imagine NVidia being limited to deliver cards that work with AMD or Intel drivers. Not that PCI cards, even those coming from Creative and being labeled as SoundBlaster rarely offer great compatibility when it comes to DOS. I have reached partial success with some C-Media cards with a TSR driver.
- Limited USB keyboard support. Older BIOSes have it but it has to be enabled using a PS/2 keyboard first.
- Mouse support - PS/2 was a standard and it is really beneficial to have one. USB mouse is considered to work with the CuteMouse driver.


See the Hardware Compatibility List for more details.


## Setting it up

To install DOS you will need three floppies. If you plan on using a CD-ROM drive consider adding the installer and drivers as the original DOS does not have them. A decent driver can be extracted from the Windows 98 bootdisk.

I strongly suggest preparing a boot CD in advance if your motherboard and BIOS support it. Otherwise a dedicated boot floppy would not hurt. I recently realised a slimmed down set of DOS tools, CD driver and Norton Commander is able to fit into 1.44 MB floppy.

If you plan on doing multiple installations, you can save a lot of time by preparing a root filesystem image before. There is a great change to test it with VirtualBox or QEMU before you go on a real hardware.

Here is the list of useful programs for Windows:
- CDBurnerXP allows creating bootable CDs.
- 7-zip allows browsing disk images from VirtualBox, VMware and raw floppies.

Linux offers equivalents apps:

> TODO: add mkisofs and find a tool for browsing images (mount)

### Preparing MS-DOS rescue disk

## Windows 3.11

### Emulation

When it comes to running Windows 3.11 usually everything what guarantees DOS 6.22 to work will also be true for Windows. A rather tempting solution 

- VMware Windows 3.11 supports VGA mode 640x480 with 4 colours. Additional patch enables 1024x768 with 256 colours.
- VirtualBox works with the same VESA mode patch that allows VMware to run on 1024x768.
- QEMU allows using Cirrus Graphics card that works with minor glitches.
- PCem works best of all but requires even better hardware that plain DOS.
- DOSBox runs Windows 3.11 with a lot of limitations. The most important is networking, which makes it difficult to run some specific application such as MS Office 4.3.

### Real Hardware

Firstly, it is important to mention that setting up Windows 3.11 on a real hardware might be a challenge. Microsoft dominance of the market started with Windows 95 which means most PC from that time focused on DOS compatibility. Some PCs around that time were shipped with Windows 3.x but for most users that was a purely optional product.

That situation significantly limits hardware options in this case. Usually most DOS-Era hardware should work, however there are more things to consider.

- SVGA support under DOS apps is a rarity, most games stick to VGA due to market share. Most PC were VGA only and Windows works perfectly with them offering decent 640x480 with 16 colours. To discover the full potential of Windows 3.x apps I would suggest to find a card that supports 800x600 pixels with 256 colour mode.
- Audio capabilities are usually limited to Sound Blaster compatible devices, the good thing is Windows 3.11 has build-in drivers for them.
- Mouse support limits you to PS/2.

See the Hardware Compatibility List for more details.
