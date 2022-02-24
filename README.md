# Two-Stage-CMOS-Op-Amp-with-Miller-Compensation
This repository presents the design and analysis of Fully Differential Two-Stage CMOS Op-Amp with Miller Compensation using Synopsis Custom Compiler on 28ηm CMOS Technology as a part of Cloud Based Analog IC Design Hackathon.
# Table of Contents
1. [Introduction](#Introduction)
2. [Miller compensation technique](#Miller compensation technique)
3. [Design of two stage Opamp using Miller Compensation Technique](#Design of two stage Opamp using Miller Compensation Technique)
4. [Schematics](#Schematics)
6. [Simulation results](#Simulation results)
7. [Netist](#Netlist)
8. [Observation](#Observation)
9. [Tools Used](#Tools Used)
11. [Author](#Author)
12. [Acknowledgements](#Acknowledgements)
13. [References](#References)
# Introduction:
The fundamental, versatile and integral building block in analog and mixed signal circuit designs is an Operational amplifier. Opamps find a wide Varity of applications in comparators, differentiator’s bias applications etc. The scaling down of CMOS technology has created issues in design of Opamps and other circuits. With reduction of supply voltage it’s difficult to cascade transistors. The draw backs of single stage Opamps are overcome by implementing multistage amplifiers. These are used to achieve higher gain despite limitation of supply voltage. Due to high gain and high output swing two stage Opamp is most in use. The two pole transfer function of uncompensated Opamp lie below Unity Gain Frequency, hence to obtain stability frequency compensation circuit is required.
# Miller Compensation Technique:
![labelname :: This is the label text.](path/to/image.png)
![Fig. 1: Frequency Response of an uncompensated operational amplifier](https://user-images.githubusercontent.com/79392063/155585493-206ef16c-90da-4962-8132-2fee2844068c.png)
The {#Fig. 1: Frequency Response of an uncompensated operational amplifier} shows the phase shift is below 450 when the gain of two stage Opamp is unity gain frequency. Hence, to achieve stability, compensation technique is required in a two-stage operational amplifier. This can be achieved by pole splitting using Miller effect as shown in figure 2.
![image](https://user-images.githubusercontent.com/79392063/155585632-d5dfee42-7e3d-4680-b701-b216648440f1.png)
 This is known as the Miller compensation technique. In this technique one pole is made more dominant by moving it down the frequency and the other less dominant by moving it up the frequency.
 ![image](https://user-images.githubusercontent.com/79392063/155585699-75039b81-523b-4b94-8454-8e2891091a2d.png)
 A compensation capacitor is placed between the output of the first stage (differential amplifier) and the output of the operational amplifier as shown in figure 2.
 # Design of two stage Opamp using Miller Compensation Technique:
The first stage of the design is  NMOS differential amplifier with active load and in second stage is  a PMOS common source amplifier. Between the output of first stage and second stage a compensation capacitor Cc is connected. The compensation capacitor splits the poles to achieve the stability as shown in figure 4. The differential stage of opamp is formed using transistor M1, M2, M3 and M4 form the differential stage of the op-amp. The two nMOS transistors M1 and M2 form the differential inputs of the amplifier. The resistance of the input transistors and active load transistors which are M3 and M4 are the main resistances that contribute to the output. The transistors M6 and M7 forms a current sink load inverter.
![image](https://user-images.githubusercontent.com/79392063/155585752-5d6e4872-4db7-4885-b8b7-f2ea90a98907.png)

# Tools Used:
 **Synopsys Custom Compiler:**
The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level. <br />
 **Synopsys Primewave:**
PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.<br />
**Synopsys 28nm PDK:**
The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit. 
# Simulation Results
# Netlist of the Circuit:
Refer to the netlist of the circuits here: [Netlist](https://github.com/AdityaKalyani14/Two-Stage-CMOS-Op-Amp-with-Miller-Compensation-/blob/main/Netlist)
# Observations:
 The design is to be implemented using 28ηm synopsis PDK. Op-amp designed here exhibits DC gain of >50 dB, 30MHz unity gain bandwidth, phase margin of >450, and slew rate >10 V/µS for typical 1 pF differential capacitive load. The power dissipation should be <500µW.
# Author:
Aditya Kalyani, Indian Institute of Technology, Dharwad, Karnataka
# Acknowledgements:
• Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.<br />
• [Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)<br />
• [Synopsys India](https:www.https://www.synopsys.com/)<br />
• VLSI System Design (VSD) Corp. Pvt. Ltd India<br />
• Chinmay panda, IIT Hyderabad
• Sameer Durgoji, NIT Karnatak
# References:
1.	K. T. Tan, N. Ahmad, M. Mohamad Isa, and F. A. S. Musa , "Design and analysis of two stage CMOS operational amplifier using 0.13 µm technology", AIP Conference Proceedings  (2020.)    https://doi.org/10.1063/1.5142132.
2.	Razavi, B. (2001). Design of Analog CMOS Integrated Circuit. McGraw-Hill
3.	M. I. Idris, N. Yusop, S. A. M. Chachuli, M. M. Ismail, F. Arith, and A. M. Darsono, “Low power operational amplifier in 0.13um technology,” Mod. Appl. Sci., vol. 9, no. 1, pp. 34–44, 2015.
