 KagaxOS-beta (Transitioning to 64-bit)
KagaxOS is an open-source mini operating system project written in C and Assembly. This project is currently in its most critical development phase: transitioning from 32-bit (Protected Mode) to 64-bit (Long Mode).
 
 STOP: DO NOT DOWNLOAD OR RUN YET
The project is currently in a non-bootable and broken state.

Please do not download the binaries to run them, as they will not work.

This repository is currently for code review and development purposes only.

If you are an OS developer, I invite you to examine the source code to help identify the 64-bit transition bug.

 Current Status
Bootloader: GRUB (Multiboot2) loads successfully.

The Issue: The system hangs or triggers a triple fault during the transition from 32-bit to 64-bit Long Mode.

Suspected Cause: Likely an issue within the Paging tables (PML4/PDPT) setup or the GDT (Global Descriptor Table) configuration during the architecture switch.

 Technical Specifications
Target Architecture: x86_64

Toolchain: GCC (x86_64-elf-gcc), NASM, GNU ld

Boot Protocol: Multiboot2 / GRUB

 How to Help
Since the 64-bit transition logic is currently broken, I am looking for contributors who enjoy debugging CPU states and memory mapping. If you can spot the error in the Assembly or C initialization code, please reach out!

 mehmetkagankoc001@gmail.com
