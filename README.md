# SOC_design
# DAY 1
Introducation to QFN-48 and also Introduction to Openlane and familiarization with it
  The microcontroller usually consists of the core alongwith storage elements, IPs, PLLs, DAC and ADC and other peripherals. An SOC is an integrated chip with all components and peripherals on the same die. It also needs an OS. The OS is responsible for allocating memorty and to handle I/O operations. This acts as an interface between software to hardware. The compiler converts the high-level language to lower level assembly language. This code is then converted to computer binary format(1/0s) by the assembler. Based on the computer instrusction set, the compiler converts to assembly language. And here, RISCV is an open source instruction set architecture and its specialilty is, it is open-source. Meaning it is open to customization. Later, Hardware descriptive lnaguages like Verilog is used to draw the logic onto the hardware. The RTL the flow of data between registers and the logical operations performed. Finally, the netlist genenarated from synthesis are placed and routed onto the silicon die.

  Openlane is an open source tool for ASIC design with open RTL designs, open EDA tools and open PDKs. It is benefical for users like us who are into experiments during education or worksshops. This tool allows for complete RTL2GDS flow. ![flow](https://github.com/user-attachments/assets/de27f487-f6b4-42c2-abb6-c674c7fa69ae)
  RTL Synthesis
  Floorplanning & Placement 
  CTS & Routing:
  Static Timing Analysis (STA)
  Physical Verification
  DFT(Design for Test)
  Static Timing analysis(STA)violations is there
  Physical Verification(DRC and LVS)
