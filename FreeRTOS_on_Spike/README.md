# FreeRTOS
FreeRTOS for RISC-V(32 and 64-bit)

FreeRTOS is tested on Spike with several builds including single-task, multi-task and typical demo test which includes queues, semaphores, mutexes and about a dozen concurrent tasks running concurrently.

### Tools used

Spike commit on 20th October, 2017 "3b1e9ab7522b3b20cde6bd8d9f2b28222463cf1b"

riscv64-unknown-elf-gcc (GCC) version 7.1.1 20170509


Install [riscv-tools](https://github.com/riscv/riscv-tools) and Set the RISC-V tools install path to export

        $ export PATH=$PATH:/{INSTALL_LOCATION}/bin

### Getting the sources

        $ git clone https://github.com/RISCV-on-Microsemi-FPGA/FreeRTOS


Edit CCPATH to RISC-V tools install directory in `Makefile.inc`  i.e available in FreeRTOS/Demo/riscv-spike/Makefile.inc
    `CCPATH	= /{INSTALL_LOCATION}`

### Build Steps

Run demo application on Spike

        $ cd FreeRTOS/Demo/riscv-spike
        $ make
        $ spike riscv-spike.elf

        output : PASS! 
                 Task - 1
                 Task - 2
             
Run demo application on Spike with debug mode, Follow riscv-isa-sim [README.md](https://github.com/riscv/riscv-isa-sim) to know more about debug instruction.

        $ spike -d riscv-spike.elf

To capture debug log use below command

        $ spike -d riscv-spike.elf 2>&1 | tee text.txt
