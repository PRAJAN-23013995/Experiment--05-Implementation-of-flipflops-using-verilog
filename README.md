# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.


 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.




Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 ![download](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/d2b871c2-61d8-4234-aeaa-dd315cead4a8)
![WhatsApp Image 2023-12-14 at 20 37 19_9ba6c291](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/973264e8-d7cf-43b0-85db-62caafacdc6f)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D


![WhatsApp Image 2023-12-14 at 20 38 25_fc02d75a](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/4cf6fd38-41fd-4aa6-9731-4421f9df9519)

![WhatsApp Image 2023-12-14 at 20 37 17_38a112e6](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/854b958e-a78b-4f27-9aa8-9d41bec2172a)
![download](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/f1bd4087-aa2c-4374-af69-79d7651056ff)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

 ![WhatsApp Image 2023-12-14 at 20 37 58_508e3e8e](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/cb4bbb9c-aed1-4e1b-8d4d-c712414513e6)

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.

![WhatsApp Image 2023-12-14 at 20 38 59_e9252a26](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/e7001403-b5f8-4354-9d7e-ede8c5600eda)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)
![WhatsApp Image 2023-12-14 at 20 37 15_ea6765f7](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/8465e64b-a642-491d-8309-b77f0862a1cd)
![download](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/60cfb353-2521-453d-8b66-7d034e6ba6f5)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.


![WhatsApp Image 2023-12-14 at 20 38 11_876f8719](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/2d6c6271-f7cc-46ce-bbf7-31e795abdb7b)
![WhatsApp Image 2023-12-14 at 20 38 44_6a2014e0](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/106f8537-36b7-4e8a-b594-262f8b76352f)

![WhatsApp Image 2023-12-14 at 20 37 15_f920072d](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/85c27b56-0a12-4fe2-9da1-a33236065a38)
![th](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150313345/4c7a25a9-731f-4d4b-a281-44693a5d5928)

This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



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
Developed by: 
RegisterNumber:  
*/






### RTL LOGIC FOR FLIPFLOPS 









### TIMING DIGRAMS FOR FLIP FLOPS 








### RESULTS 
