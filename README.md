# FreeRTOS port on Mi-V Soft Processors

This repository contains the FreeRTOS example projects

## FreeRTOS_on_Spike
   This folder contains the details of FreeRTOS running on Spike Simulator.
   
### Spike
   Spike is the official RISC-V Instruction Set Simulator. Spike supports RV32GC and RV64GC, and has Debug and GDB support.
   
   Find more details on Spike [here](https://github.com/riscv/riscv-isa-sim/)
   
## FreeRTOS_on_Mi-V_Processor
   This folder contains FreeRTOS example projects running on a Mi-V Soft Processor. It includes launchers for hardware deployment and for Renode emulation (which is bundled with SoftConsole 5.3 or higher). Group launcher "miv-rv32im-freertos-port-test Start-Renode-emulator-and-attach" will launch Renode, attach a GDB connection and then load the FreeRTOS binary to the emulation. After a successful launch, SoftConsole should break at main() and should behave similarly to real hardware. For details on how to use Renode from within SoftConsole see SoftConsole's Release Notes.
