### **SKILL ASSIGNMENT-1**
### **AIM:**

To write and execute an Assembly Language Program (ALP) for the 8051 microcontroller to find the largest number from a given set of N numbers stored in memory, and to display the result in the Accumulator (A register).

### **PROGRAM:**
Write an assembly language program in 8051 to find the largest number from a given set of N numbers stored in memory. Display the result in AL register.

### **APPARATUS REQUIRED:**

Laptop with Keil Software

### **PROGRAM:**
```
ORG 0000H
MOV R0, #30H
MOV R1, #05H
MOV A, @R0
INC R0
DEC R1
LOOP: MOV B, @R0
      CJNE A, B, CHECK
      SJMP NEXT
CHECK: JNC NEXT     
       MOV A, B     
NEXT: INC R0
      DJNZ R1, LOOP
MOV P1, A           
HERE: SJMP HERE
END
```
### **OUTPUT:**
<img width="1661" height="1015" alt="Screenshot 2025-11-05 143924" src="https://github.com/user-attachments/assets/b69631a7-98ea-4009-af90-8f61d56eb99e" />

### **RESULT:**

Thus the assembly language program in 8051 to find the largest number from a given set of N numbers stored in memory is executed and displayed the largest in AL register.
