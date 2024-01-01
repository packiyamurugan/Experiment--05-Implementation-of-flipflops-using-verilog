### Name:Packiya Murugan R

### Register Number:212223050034

# Experiment--05-Implementation-of-flipflops-using-verilog

## AIM: 
To implement all the flipflops using verilog and validating their functionality using their functional tables
## HARDWARE REQUIRED: 
PC, Cyclone II , USB flasher
## SOFTWARE REQUIRED:
Quartus prime
## THEORY:
#### SR Flip-Flop:

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


### D Flip-Flop:
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop:

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



### T Flip-Flop:

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

## Procedure:
1.Using nand gates and wires construct SR flip flop.

2.Repeat same steps to construct JK,D,T flipflops.

3.Find RTL logic and timing diagram for all flipflops.

## PROGRAM:

Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by:Packiya murugan R
RegisterNumber:23014137

### SR Flipflop:
module srflipflops(S,R,clk,Q,Qbar);

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

### JK Flipflop:
module JK(J,K,clk,Q,Qbar);

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

### D Flipflop:
module D_flipflop(D,clk,Q,Qbar);

input D,clk;

output reg Q;

output Qbar;

always @(posedge clk)

begin

Q=D;

end

assign Qbar=~Q;

endmodule

### T Flipflop:
module T_flipflop(clk,T,Q,Qbar);

input clk,T;

output Q,Qbar;

reg Q,Qbar;

always @(posedge clk)

begin

Q=(T&~Q)|(~T&Q);

Qbar=~Q;

end

endmodule

## TRUTH TABLE FOR FLIP FLOPS:

### SR Flipflop:
![292232629-f884340b-31ce-4dc0-a544-56f79cc13bb3](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/a4eb7c93-e057-4556-a6fd-31574ed4277c)


### JK Filpflop:
![292232698-9a352452-5644-448d-8f48-ee9c4f6844b3](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/1a1b3711-0c41-47af-aa5f-484dbc24fb3c)



### D Filpflop:
![292244227-3513409e-3963-4bc6-ba58-804a78ff8898](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/17154782-02d6-43ca-86a0-1fb24104e40e)


### T Filpflop:

![292244351-e07830ce-c60e-42d6-b391-0eb14cafdee4](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/3259708f-3779-459e-99ae-4ef5b3cfa420)



## RTL LOGIC FOR FLIPFLOPS:
### SR Filpflop:
![292230396-ccc7e04e-47c0-4403-92ba-e9ab076a9867](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/a4295b3f-21c0-4403-b558-8e4c3661ffc6)


### JK Filpflop:
![292230564-b2c976f2-5287-4d7e-9563-4b4b4c9e79aa](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/fe6f7529-9870-45bf-9191-7f273ccd43a2)


### D Flipflop:
![292230704-c1a924ce-2598-46cd-9dae-ad09285151dc](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/fb407268-1db9-4fe6-a7a1-3d6b9c0a31ce)


### T Filpflop:
![292230817-a223e282-ed05-4607-b970-e9093598504f](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/bda580f7-bbd9-44ea-9cf6-3e3928a46823)




## TIMING DIGRAMS FOR FLIP FLOPS:
### SR Filpflop:
![292231018-69b4ea8b-c9f8-4818-ab61-23df8e63eb65](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/8a275235-c927-45ed-8c38-75affbcdeab3)


### JK Filpflop:
![292231172-aedc04dc-8ea1-4cfb-9521-458dfa8b0742](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/1bcdd917-8ffc-4f4a-bb46-287934123232)


### D Filp flop:
![292231297-af20b3a8-7b7e-4572-8915-b36a9a7aa16c](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/679d4b1f-6358-49e1-90a5-4c5ec7b2c118)


### T Filpflop:
![292231510-451647be-37c9-4274-bc3e-1a242802ecd2](https://github.com/packiyamurugan/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152168087/4ebf8d40-30b8-4918-b104-10cd04493a12)




## RESULTS:
Thus, the implementation of SR,JK,D and T flipflops using nand gates are done sucessfully.
