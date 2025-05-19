# OPAMP

Two stage  Operational Amplifier Design for high speed application
This repository contains the complete design, simulation, and analysis files for a two-stage CMOS Operational Amplifier implemented in Cadence Virtuoso using the 90nm technology node.

### Abstract
This project presents the design and simulation of a high-speed CMOS operational amplifier using a 90nm technology node. 

The amplifier architecture is optimized for high-speed performance while maintaining stability and reasonable power efficiency. Key design specifications include a phase margin (PM) of ≥ 60°, a gain of 3000 V/V (or 70 dB), and a gain bandwidth product (GBW) of 100 MHz. The op-amp achieves a slew rate (SR) of 100 V/µs, allowing it to handle fast input transitions effectively. The design operates with a dual power supply of ±1.3 V, and supports a common-mode input range from −0.5 V to +1.0 V.

The design flow follows the principles described in CMOS Analog Circuit Design by Phillip E. Allen and Douglas R. Holberg. Hand calculations were used to size the transistors based on gain, bandwidth, and slew rate requirements. The design is validated through simulations in Cadence Virtuoso using the Spectre simulator.

This project demonstrates a successful implementation of a high-performance analog building block that balances speed, gain, and power dissipation, making it suitable for integration in high-speed analog and mixed-signal systems.

## Design Methodology

The amplifier was designed using textbook design flow from **Allen & Holberg**:
- Sizing based on slew rate, gain, and compensation needs
- Two-stage topology with Miller compensation
- Biasing and gain optimization using hand calculations
- Verification via Spectre simulation (AC, transient, stability)


## Overview

The design targets high gain and stability with high slew rate, optimized for analog signal processing applications. 


### Key Design Specifications
![image](https://github.com/user-attachments/assets/28eed64a-b9a2-4108-9077-8d5ebcf29c27)


### Design Relationships
![opamp_relationship ](https://github.com/user-attachments/assets/d930a3ac-0fb8-456b-a9d8-b2db3414aa9c)

### Designing  of W/L value to meet  Key Specifications
![image](https://github.com/user-attachments/assets/180280ea-d734-4af5-ac9c-8fc31ebf1fce)
![image](https://github.com/user-attachments/assets/73f64201-680a-4c8e-bb58-7c97781250a3)
![image](https://github.com/user-attachments/assets/c2db6ac8-1692-4f5e-8926-308deaaff9e8)
![image](https://github.com/user-attachments/assets/8e01e361-2eae-4003-9c7f-49ee30b0cd4f)
### proposed design
![image](https://github.com/user-attachments/assets/9e1352ba-eaae-421c-ab30-721ed51f6fab)
![image](https://github.com/user-attachments/assets/f72b6dc0-c6cc-4419-a123-17838f01cd88)
![image](https://github.com/user-attachments/assets/bd00e43d-05c3-4c75-94c0-b953379f0d55)
![image](https://github.com/user-attachments/assets/3d4a3183-5ef0-4749-b9d9-4600059fa453)

### on Design W/L values
![image](https://github.com/user-attachments/assets/ab131f1e-fcbf-41ef-a2fe-f8fd307ab73f)

### Circuit simulation using cadence virtuoso (90nm)
![image](https://github.com/user-attachments/assets/1b73b3fa-bf98-46ab-9e8a-7b468011d516)

### Testing Circuit for transient simulation
![tran_testing](https://github.com/user-attachments/assets/5ec532bc-c88a-43b2-a136-6b9d6e59745b)

## output of transient simulation
![transient](https://github.com/user-attachments/assets/9ab2e038-8fd5-4cd6-bf9c-f3c5b2ae2805)

## Testing Circuit for AC Analysis
![Ac_test](https://github.com/user-attachments/assets/17f41932-51c7-438f-97d5-da5a8e7b60b3)

## AC Analysis Result
![ac](https://github.com/user-attachments/assets/26e6cc2d-b9aa-4bf5-a882-d77efc79e93f)
in above picture you can see that 
Gain = 70 dB
Bandwidth = 55.6k Hz
Unit Gain Bandwidth = 100.14 Hz
phase Margin = 


## Testing Circuit for  Slew_rate Calculation
![slewRate_test](https://github.com/user-attachments/assets/9bb842cc-d52b-42c3-a38d-2499c442ced9)

## slew_rate value
![slewrate](https://github.com/user-attachments/assets/ee36561f-96c3-4ec4-9a5e-cbbb3c68acb7)


















