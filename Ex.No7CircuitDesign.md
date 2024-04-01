# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:
```
and(0,0,0).
and(0,1,0).
and(1,1,1).
and(1,0,0).
xor(1,1,0).
xor(0,1,1).
xor(0,0,0).
halfadder(A,B,Sum,Carry):-
    xor(A,B,Sum),
    and(A,B,Carry).
```











### Output:
![WhatsApp Image 2024-04-01 at 15 24 28_4598d0d0](https://github.com/kannanAnanth/AI_Lab_2023-24/assets/160721190/1b38894e-5143-4f92-b12b-4b27b70215fb)




### Result:
Thus the truth table of circuit verified sucessfully.
