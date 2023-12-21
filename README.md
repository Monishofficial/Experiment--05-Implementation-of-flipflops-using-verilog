# NAME : MONISH N
# REG NO: 212223240097
# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:   PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
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



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
1)Create a New Project:

Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
2)Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.
3)Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic.
4)Compile the Project:

To compile the project, click on "Processing" > "Start Compilation" in the menu.
Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
5)Analyze and Fix Errors:

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary.
View the RTL diagram.
6)Verification:

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
Give the Input Combinations according to the Truth Table and then simulate the Output Waveform.

### PROGRAM 
/*
Developed by: MONISH N
RegisterNumber:212223240097
SR Flipflop
module sr(S,R,clk,Q,Qbar);

input S,R,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=S|((~R)&Q);

Qbar=R|((~S)&(Qbar));

end

endmodule

JK Flipflop
module jk(J,K,clk,Q,Qbar);

input J,K,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=(J&(~Q))|((~K)&Q);

Qbar=((~J)&(Qbar))|K&(~Qbar);

end

endmodule

D Flipflop
module d(d,clk,q,qbar);

input d,clk;

output q,qbar;

reg q,qbar;

always @(posedge clk)

begin

q=d;

qbar=~q;

end

endmodule

T Flipflop
module t(clk,T,q,qbar);

input clk,T;

output q,qbar;

reg q,qbar;

always @(posedge clk)

begin

q=(T&~q)|(~T&q);

qbar=~q;

end

endmodule

*/

### RTL LOGIC FOR FLIPFLOPS 
## SR Flipflop
![SR FLIPFLOP IMAGE](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/70ddcd22-4259-4648-95f4-13fdec53f35d)

## JK Flipflop
![JK FLIPFLOP IMAGE](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/96ce88d0-e563-43fe-b27d-de4aa736118d)

### D Flipflop
![DFLIPFLOP IMAGE](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/10b4ddd7-acb0-450e-9ce8-e08c0d54029e)

## T Flipflop
![T FLIPFLOP IMAGE](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/4f15154f-8d4c-4a7b-85e2-b24f5aaeee67)


# Truth Table
## SR Flipflop
![SRFLIPFLOPTRUTH](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/9038ac9c-c504-4b3c-95f0-358ded5745b7)


## JK Flipflop
![JKFLIPFLOPTRUTH](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/82483c40-bb51-408b-820d-40943f055fc6)


## D Flipflop
![DFLIPFLOPTRUTH](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/a0645067-3ef6-4cb0-aa2f-6d731444fc9d)


## T Flipflop
![TFLIPFLOPTRUTH](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/3eb15b51-f6b4-48a2-8713-0e2403727b9f)

### TIMING DIGRAMS FOR FLIP FLOPS

## SR Flipflop
![SRFLIPFLOPTIMING](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/578b4a52-7272-4e16-a64f-721936a3f45c)


## JK Flipflop
![JKFLIPFLOPTIMING](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/61452d69-aa18-4468-b35d-fd7d5afc841d)


## D Flipflop
![DFLIPFLOPTIMING](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/6f3b0a7f-b569-4cdf-b9cc-40e37e470604)


## T Flipflop
![TFLIPFLOPTIMING](https://github.com/Monishofficial/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149455421/f3caa3c7-fb68-4492-bb3d-e8a8afb83957) 


# RESULTS 
### Thus, the implementation of SR,JK,D and T flipflops using nand gates are done sucessfully.
