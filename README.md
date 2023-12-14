   # Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![WhatsApp Image 2023-12-14 at 20 39 47_d5871c5a](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/8b835cc7-829c-4d57-b9ee-a81fec086558)
 

This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.

![WhatsApp Image 2023-12-14 at 20 39 23_931adb33](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/d4f52026-4a8c-4225-b14e-cef049bf0697)
 

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State

 ![WhatsApp Image 2023-12-14 at 20 37 04_b9df3c00](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/65667af2-3809-4c9f-943e-c7e4a50b8ade)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![th](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/e576092b-464c-4aaa-bc45-b376148636b6)
 
 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.

![WhatsApp Image 2023-12-14 at 20 38 25_aa141868](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/f9bcbc28-ad48-45d2-9879-0190e2835419)

![th](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/1209a257-ec41-4694-a2ef-ec8e264ced6b)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
 
 ![WhatsApp Image 2023-12-14 at 20 37 41_58735a7a](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/3bb90a12-0cd8-4451-b932-4e65c27959a3)

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.

![WhatsApp Image 2023-12-14 at 20 38 59_7ced7857](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/56efa8a6-7af2-4b62-b62a-3d49a54ff0ac)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

 ![WhatsApp Image 2023-12-14 at 20 37 15_2fbaf2d0](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/d3d09fa8-57e2-4a72-bbbf-cd0c3fffd724)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 

![download](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/cf1d9d30-2ba9-4701-83d3-4f8206752174)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)


 
### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

 ![WhatsApp Image 2023-12-14 at 20 38 11_25bfcd0a](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/c8c65c22-eabf-4312-8d22-12e75e928c3e)

![WhatsApp Image 2023-12-14 at 20 38 44_e5a7ed0d](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/86127d35-c9b4-4fd7-a2c3-cd4b4ef39528)


This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.

![WhatsApp Image 2023-12-14 at 20 37 14_f985d10a](https://github.com/PRAJAN-23013995/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/ab6d73b6-0cc7-4474-a9aa-4c6f40092390)

![download](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/7fc0705f-1bd6-4609-880b-e43f98c3824e)



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


 
From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: PRAJAN-P
RegisterNumber: 23013995
*/






### RTL LOGIC FOR FLIPFLOPS 









### TIMING DIGRAMS FOR FLIP FLOPS 








### RESULTS 
