# RISCV/QEMU Emulator with Software-managed TLBs

This fork of the [QEMU](https://github.com/qemu/qemu) project modifies the RISC-V emulator to shift conventional Virtual Memory responsibilities of the hardware (such as page table walking and TLB filling) to the software. This is done by raising an exception whenever the TLB misses instead of walking the page table to find the mapping, and by providing new CSRs to allow for TLB writing from the software side.

The changes introduced here are explained in the accompanying [bachelors' thesis](https://github.com/Meidimax99/bachelors_thesis). [This](https://github.com/Meidimax99/xv6-riscv-softtlb) fork of the xv6 operating system implements a software-managed virtual memory system based on this project.
