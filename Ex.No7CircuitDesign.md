# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE:  25/03/2024                                                                        
### REGISTER NUMBER : 212221060283
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
![WhatsApp Image 2024-04-01 at 15 32 04_dba3702c](https://github.com/Thirugnanaselvan/AI_Lab_2023-24/assets/160720772/81756ff6-9dff-4878-9761-b9bddebcb1e4)
### Result:
Thus the truth table of circuit verified sucessfully.
