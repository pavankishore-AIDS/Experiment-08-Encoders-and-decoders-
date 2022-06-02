# Experiment-08- Encoders-and-decoders 
### AIM: To implement 8 to 3 Encoder and  3to8 Decoder using verilog and validate its outputs
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## Encoders
Binary code of N digits can be used to store 2N distinct elements of coded information. This is what encoders and decoders are used for. Encoders convert 2N lines of input into a code of N bits and Decoders decode the N bits into 2N lines.

1. Encoders –
An encoder is a combinational circuit that converts binary information in the form of a 2N input lines into N output lines, which represent N bit code for the input. For simple encoders, it is assumed that only one input line is active at a time.

As an example, let’s consider Octal to Binary encoder. As shown in the following figure, an octal-to-binary encoder takes 8 input lines and generates 3 output lines.

![image](https://user-images.githubusercontent.com/36288975/171543588-bc0746df-a173-4b35-989e-5fb7d385fe8a.png)
## Figure -01 3 to 8 Encoder 


Implementation –

X = D4 + D5 + D6 + D7
Y = D2 +D3 + D6 + D7
Z = D1 + D3 + D5 + D7 
Hence, the encoder can be realised with OR gates as follows:


![image](https://user-images.githubusercontent.com/36288975/171543740-68403b82-aa93-4c98-9343-f32b14885a2e.png)
## Figure -02 3 to 8 Encoder implenentation 

 ### Decoders 
A decoder does the opposite job of an encoder. It is a combinational circuit that converts n lines of input into 2n lines of output.

Let’s take an example of 3-to-8 line decoder.
Implementation –
D0 is high when X = 0, Y = 0 and Z = 0. Hence,

D0 = X’ Y’ Z’ 
Similarly,

D1 = X’ Y’ Z
D2 = X’ Y Z’
D3 = X’ Y Z
D4 = X Y’ Z’
D5 = X Y’ Z
D6 = X Y Z’
D7 = X Y Z 


![image](https://user-images.githubusercontent.com/36288975/171543978-ee2d0671-2846-40a1-8705-507fd6287a49.png)
## Figure -03 8 to 3 Decoder 



![image](https://user-images.githubusercontent.com/36288975/171543866-5a6eace6-8683-49d7-9c4f-a7cb30ec3035.png)
## Figure -04 8 to 3 Decoder implementation 

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for Endocers and Decoders  and verify its truth table in quartus using Verilog programming.
Developed by: M.PAVAN KISHORE
RegisterNumber:  212221230076

module enc(d0,d1,d2,d3,d4,d5,d6,d7,a,b,c);
input d0,d1,d2,d3,d4,d5,d6,d7;
output a,b,c;
or(a,d4,d5,d6,d7);
or(b,d2,d3,d6,d7);
or(c,d1,d3,d5,d7);
endmodule
*/






### RTL LOGIC  

![171544996-5cfa93e7-86fc-42d8-9e5d-687b3146ff65](https://user-images.githubusercontent.com/94154941/171629283-1217b90b-6f37-44e5-9869-56462ea3afc4.png)







### TIMING DIGRAMS  

![171545012-01846b5b-2c52-4f99-9347-f1a583c71d13](https://user-images.githubusercontent.com/94154941/171629291-06a1e109-b511-4aba-91c7-dc4819a4bc43.jpeg)




### TRUTH TABLE 

![171545485-081f0497-5689-49ba-9e62-f1e1ead2c234](https://user-images.githubusercontent.com/94154941/171629299-c95d5d71-54b0-4e76-aa0a-dc1bef8399c6.png)


## PROGRAM(DECODER):
/*
Program for Endocers and Decoders  and verify its truth table in quartus using Verilog programming.
Developed by: M.PAVAN KISHORE
RegisterNumber:  212221230076


module enc(a,b,c,d0,d1,d2,d3,d4,d5,d6,d7);
input a,b,c;
output d0,d1,d2,d3,d4,d5,d6,d7;
assign d0 = (~a&~b&~c);
assign d1 = (~a&~b&c);
assign d2 = (~a&b&~c);
assign d3 = (~a&b&c);
assign d4 = (a&~b&~c);
assign d5 = (a&~b&c);
assign d6 = (a&b&~c);
assign d7 = (a&b&c);
endmodule
*/
## RTL LOGIC:
![171545203-cc7c2118-d4ae-4364-a095-9c418ef0a5d7](https://user-images.githubusercontent.com/94154941/171629735-9d083518-95df-4b9b-9c64-ad6fd1bda5f5.png)


## TIMING DIAGRAM:
![171545245-b8c00f4e-8474-4533-8fad-755bb2704671](https://user-images.githubusercontent.com/94154941/171629738-90d7ebdc-569c-4b82-8579-d2aa7a16e103.png)


## TRUTH TABLE:
![171546126-a5486670-9948-4b5d-aba6-dcad149b283b](https://user-images.githubusercontent.com/94154941/171629745-ceb58cd7-708b-4661-8b72-153d6d6102dd.png)


## RESULTS
Thus the program to desing encoder and decoder is done.
