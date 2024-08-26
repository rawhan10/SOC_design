# SOC_design
# DAY 1
Introducation to QFN-48 and also Introduction to Openlane and familiarization with it <br />
  The microcontroller usually consists of the core alongwith storage elements, IPs, PLLs, DAC and ADC and other peripherals. An SOC is an integrated chip with all components and peripherals on the same die. It also needs an OS. The OS is responsible for allocating memorty and to handle I/O operations. This acts as an interface between software to hardware. The compiler converts the high-level language to lower level assembly language. This code is then converted to computer binary format(1/0s) by the assembler. Based on the computer instrusction set, the compiler converts to assembly language. And here, RISCV is an open source instruction set architecture and its specialilty is, it is open-source. Meaning it is open to customization. Later, Hardware descriptive lnaguages like Verilog is used to draw the logic onto the hardware. The RTL defines the flow of data between registers and the logical operations performed. Finally, the netlist genenarated from synthesis are placed and routed onto the silicon die.

  Openlane is an open source tool for ASIC design with open RTL designs, open EDA tools and open PDKs. It is benefical for users like us who are into experiments during education or worksshops. This tool allows for complete RTL2GDS flow. ![flow](https://github.com/user-attachments/assets/de27f487-f6b4-42c2-abb6-c674c7fa69ae)
  RTL Synthesis
  Floorplanning & Placement 
  CTS & Routing:
  Static Timing Analysis (STA)
  Physical Verification
  DFT(Design for Test)
  Static Timing analysis(STA)violations is there
  Physical Verification(DRC and LVS)

Design Preparation
  Running commands:
  docker
  ![openlane1](https://github.com/user-attachments/assets/9a4b4f7e-d5a7-4282-9466-ebd4519bdecb)

  ./flow.tcl -interactive
  ![1_2](https://github.com/user-attachments/assets/6fbcc601-b427-4409-b03d-4e03d844db2e)

  
  package require openlane 0.9
  prep -design picorv32a
  ![1_3](https://github.com/user-attachments/assets/811db84b-12dd-45f4-9765-efee54ffcefd)

  run_synthesis
  ![1_4](https://github.com/user-attachments/assets/6e84b304-eacd-4a02-b014-03b4f9d3e247)

  Flop ratio = no of ff / no of cells
             = 1613/14876 = 0.108 = 10.8%

# DAY2
  ![2_1](https://github.com/user-attachments/assets/9fed6a5d-596f-4335-9fb0-486c076487c0)
  ![2_2](https://github.com/user-attachments/assets/a1849b41-e94f-4768-aa36-7d46cee3dbbc)
  
  Open the layout after placement type the command magic -T home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read     
  picorv32a.placement.def & 
  ![2_3](https://github.com/user-attachments/assets/70ff5afd-727d-411d-8d02-400bffe22099)
  ![2_4](https://github.com/user-attachments/assets/1217ab05-8748-4e94-9433-aaffcc2d48e8)
  ![2_5](https://github.com/user-attachments/assets/22969c18-aded-43be-b58e-b12553488787)
  After Placement
  ![2_6](https://github.com/user-attachments/assets/407f4461-a6e4-4c91-ab72-4f0299deccea)

# DAY3
  Design library cells using magic layout and ngspice characterization 
![3_1](https://github.com/user-attachments/assets/b3d8e93e-2999-4502-bd69-ac4ac122566c)

![3_2](https://github.com/user-attachments/assets/d72fb2e8-d1a5-41bc-82da-8f4214441873)

![3_3](https://github.com/user-attachments/assets/dda75e8d-e52c-4c81-b1e6-88c63e2df4a4)

![3_4](https://github.com/user-attachments/assets/0207ca02-ce4d-4d27-8ead-3c276d24186d)


![3_5](https://github.com/user-attachments/assets/817b6068-c69f-41ee-8daa-3040ae05adeb)

![3_6](https://github.com/user-attachments/assets/17abef5e-3800-49d8-9469-560574e135b0)

![3_7](https://github.com/user-attachments/assets/01020896-6e62-4d56-9bbf-4e6c01ca12e4)

![3_8](https://github.com/user-attachments/assets/43c504c0-1e4d-44e7-ad24-c74e0535fe82)



![3_9](https://github.com/user-attachments/assets/ac27c09a-da81-4aaa-907c-28dbdd326a46)


![10 1](https://github.com/user-attachments/assets/4f4b7b7e-a094-43b9-a72c-08fbd47b6f4e)
![13](https://github.com/user-attachments/assets/6c402b77-715c-4077-834f-3fb6b199e53b)
![10 3](https://github.com/user-attachments/assets/b4a6a74d-e167-4e77-997d-025f9553814c)
![3_11](https://github.com/user-attachments/assets/195bce1b-9861-46a4-bb0d-47503e8199d5)

![10 4](https://github.com/user-attachments/assets/86f7fdd6-056c-4573-a850-2ea8469f749d)
![10 5](https://github.com/user-attachments/assets/d28256a1-94d5-4080-81cd-0e21c5b24a92)
![10 6](https://github.com/user-attachments/assets/eb1eb122-73fa-4ae6-9581-5d5d0f60e83e)
![10 7](https://github.com/user-attachments/assets/f86ae377-33e7-41df-a184-e90703c89ef5)

![3_10](https://github.com/user-attachments/assets/4ebb3b2b-0da9-4a3d-9712-a9b5617575d0)

![12](https://github.com/user-attachments/assets/3a12f776-7d19-4dba-a310-df784bdf67aa)

![11](https://github.com/user-attachments/assets/28406e20-4dd3-4c0d-b6b2-171c60655f4a)



# DAY 4

Pre-Layout timing analysis and Clock Tree synthesis

![4_1](https://github.com/user-attachments/assets/31d049b7-231f-4de5-92db-c8fd13c38288)

![4_2](https://github.com/user-attachments/assets/a1c3a97b-8456-4113-bf71-68eb301f764f)

![4_3](https://github.com/user-attachments/assets/205da6f5-4248-4bdb-bd38-1effb2ae8669)

![4_4](https://github.com/user-attachments/assets/cba09c11-4b81-4e6a-b42d-64320fa4a593)



![4_5](https://github.com/user-attachments/assets/9aa555a6-a733-4fd8-82c1-afe297b35abf)


![4_6](https://github.com/user-attachments/assets/19260eb9-1b6f-4509-a525-1b9b13384171)

![3_12](https://github.com/user-attachments/assets/31d92868-7767-4ab6-bc8d-8956c7b46344)

![4_7](https://github.com/user-attachments/assets/5b2038f4-52dc-4e5b-b742-191fd2ee282c)

![WhatsApp Image 2024-08-20 at 12 32 03 AM](https://github.com/user-attachments/assets/29d7b994-df8a-446d-ac86-9701ee039056)

![WhatsApp Image 2024-08-20 at 12 34 10 AM](https://github.com/user-attachments/assets/9811446b-6308-4903-aa52-5ae3b3d41e21)

![4_8](https://github.com/user-attachments/assets/fdce1bc2-fdf9-4cf4-a58a-dc88d4c72503)


![4_9](https://github.com/user-attachments/assets/5757207d-ebfc-4958-b61d-30ccaaafa251)

![1](https://github.com/user-attachments/assets/f7d7a602-5a17-48f5-ba31-6675b4c2942f)

![2](https://github.com/user-attachments/assets/7edb9abe-bf9a-4b1a-be20-4fc98dbd7c6d)

# DAY 5
TritonRoute

![3](https://github.com/user-attachments/assets/7ddc375c-3696-46ed-a472-d17dc9e0a832)

![4](https://github.com/user-attachments/assets/677b3fbb-3ee1-41b1-a094-166fdb20bd43)

![5_1](https://github.com/user-attachments/assets/1003925c-91ac-4ac4-91d5-98e27c46c445)

![5](https://github.com/user-attachments/assets/04467fb3-e63d-4d84-a975-2050615ec6a3)

![6](https://github.com/user-attachments/assets/89ee799c-5437-4f5c-8e4f-4629e937ef22)

![7](https://github.com/user-attachments/assets/b9f2245e-76a2-4452-819f-27534c3ae351)

![8](https://github.com/user-attachments/assets/7b3892d0-bc9c-4742-b75c-50cd3012bc9f)

![5](https://github.com/user-attachments/assets/86965003-933f-45ca-af65-e2fa61726425)




Acknowledgements:
Kunal Ghosh, Co founder (VSD Corp. Pvt. Ltd)
Nickson P Jose, Teaching Assistant (VSD Corp. Pvt. Ltd.)








