# OPAMP
Two stage  Operational Amplifier Design for high speed application
This repository contains the complete design, simulation, and analysis files for a two-stage CMOS Operational Amplifier implemented in Cadence Virtuoso using the 90nm technology node.


## Table of contents
-1. [Abstract and overview](#Abstractandoverview)
-2. [Design Methodology](#DesignMethodology)
-3. [Key Design Specifications](#KeyDesignSpecifications)
-4. [Design Relationships](#DesignRelationships)
-5. [ Designing  of W/L value to meet  Key Specifications](#DesigningofW/LvaluetomeetKeySpecifications)
-6. [proposed design](#proposeddesign)
-7. [On Design W/L values](#OnDesignW/Lvalues)
-8. [Pre Layout simulation using cadence virtuoso (90nm)](#PreLayoutsimulationusingcadencevirtuoso(90nm))
-  [### Test Circuit for transient simulation](#TestCircuitfortransientsimulation)
-  [### Output of transient simulation](#Outputoftransientsimulation)

## Abstract and overview 
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


## Key Design Specifications
![image](https://github.com/user-attachments/assets/28eed64a-b9a2-4108-9077-8d5ebcf29c27)


## Design Relationships
![opamp_relationship ](https://github.com/user-attachments/assets/d930a3ac-0fb8-456b-a9d8-b2db3414aa9c)

## Designing  of W/L value to meet  Key Specifications
![image](https://github.com/user-attachments/assets/180280ea-d734-4af5-ac9c-8fc31ebf1fce)
![image](https://github.com/user-attachments/assets/73f64201-680a-4c8e-bb58-7c97781250a3)
![image](https://github.com/user-attachments/assets/c2db6ac8-1692-4f5e-8926-308deaaff9e8)
![image](https://github.com/user-attachments/assets/8e01e361-2eae-4003-9c7f-49ee30b0cd4f)
## proposed design
![image](https://github.com/user-attachments/assets/9e1352ba-eaae-421c-ab30-721ed51f6fab)
![image](https://github.com/user-attachments/assets/f72b6dc0-c6cc-4419-a123-17838f01cd88)
![image](https://github.com/user-attachments/assets/bd00e43d-05c3-4c75-94c0-b953379f0d55)
![image](https://github.com/user-attachments/assets/3d4a3183-5ef0-4749-b9d9-4600059fa453)

## On Design W/L values
![image](https://github.com/user-attachments/assets/ab131f1e-fcbf-41ef-a2fe-f8fd307ab73f)
- You can see that ther is some mismatch in above W/L value when compared to design valve
- This mismatch arises due to non linearity of tarnsistor
- W/L value of M8 is same as M5 and W/L value of M9 is 0.615

## Pre Layout simulation using cadence virtuoso (90nm)
![image](https://github.com/user-attachments/assets/1b73b3fa-bf98-46ab-9e8a-7b468011d516)
- In the circuit vin1 is positive terminal
- Similarly vin2 is negative terminal
- The reason for above two statement is
- total gain = (gain of 1st stage)*(gain of 2nd stage) => generalized gain equation 
- In my design the gain of 2nd stage is always negative
- In 1st stage the gain may be (positive or negative) depending on the terminal slection , so to get negative gain I choose vin as positive terminal => gain of 1st stage becomes negative
- Now gain of both 1st and 2nd stage in negative
- total gain = (-gain of 1st stage)*(-gain of 2nd stage) => it becomes postive

## Test Circuit for transient simulation
![tran_testing](https://github.com/user-attachments/assets/5ec532bc-c88a-43b2-a136-6b9d6e59745b)

## Output of transient simulation
![transient](https://github.com/user-attachments/assets/9ab2e038-8fd5-4cd6-bf9c-f3c5b2ae2805)

## Test Circuit for AC Analysis
![Ac_test](https://github.com/user-attachments/assets/17f41932-51c7-438f-97d5-da5a8e7b60b3)

### AC Analysis Result
![ac](https://github.com/user-attachments/assets/26e6cc2d-b9aa-4bf5-a882-d77efc79e93f)
In above picture you can see that 
- Gain = 70 dB
- Bandwidth = 55.6k Hz
- Unit Gain Bandwidth = 100.14 Hz
- phase Margin = 60.14 (180-119.86)

### Phase Margin
![pm](https://github.com/user-attachments/assets/7300b731-9ddf-4618-a203-3f2ac1e40183)

## Test Circuit for  Slew_rate Calculation
![slewRate_test](https://github.com/user-attachments/assets/9bb842cc-d52b-42c3-a38d-2499c442ced9)

### Slew_rate value
![slewrate](https://github.com/user-attachments/assets/ee36561f-96c3-4ec4-9a5e-cbbb3c68acb7)

## Test circuit for ICMR calculations
![icmr_test](https://github.com/user-attachments/assets/2fa961ab-0d79-4448-8114-15d3dbdd0bb8)

### ICMR value 
![icmr_valu](https://github.com/user-attachments/assets/70d55ed2-feb2-456b-8600-25e835b94f46)
in above picture you can see that 
- ICMR- = -0.5V
- ICMR+ = 1V






















