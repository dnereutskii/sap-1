# Simple as posible 1 computer (SAP-1) on logisim

## Brief

Simple as possible 1 (SAP-1) computer designed for educational purposes by A.P. Malvino. 
SAP-1 has an instruction set that is a subset of the 8080/8085 microprocessor instructions.

## Architecture

### Block list

1. Program counter (PC)
2. Memory address register (MAR)
3. Random access memory (RAM 16x8)
4. Instruction register (IR)
5. Controller/Sequencer (C/S)
6. Register A -- Accumulator (A)
7. Adder/Subractor (ADD/SUB)
8. Register B (B)
9. Output register (OUT)

## Macroinstructions

Every instruction devides on operation code (high nibble) and address field (low nibble).


 No  | Mnemonic  | OpCode
:---:|:---------:|:-------------:
 1   | LDA       | 0b0000 
 2   | ADD       | 0b0001
 3   | SUB       | 0b0010
 4   | OUT       | 0b1110
 5   | HLT       | 0b1111

## Fetch microinstructions

Macro | State |  CON  |   Active
------|-------|-------|------------
 LDA  | T4    | 1A3H  | Lm_N, Ei_N
      | T5    | 2C3H  | CE_N, La_N
      | T6    | 3E3H  | NOP

## Execute microintsructions



## Program examples

### Program 1

#### Assemler language  

```{asm}
LDA 9H
ADD AH
ADD BH
SUB CH
OUT
HLT
XXH
XXH
XXH
10H
14H
18H
20H
XXH
XXH
XXH
```

#### Machine language

```{}
09H
1AH
1BH
2CH
E0H
F0H
XXH
XXH
XXH
10H
14H
18H
20H
XXH
XXH
XXH
```
#### Output register value 

1CH

### Program 2

#### Assemler language  

```{asm}
LDA 9H
SUB AH
ADD BH
SUB CH
ADD DH
SUB EH
ADD FH
OUT
HLT
46H
1EH
0FH
07H
08H
04H
6AH
```

#### Machine language

```{}
09H
2AH
1BH
2CH
1DH
2EH
1FH
E0H
F0H
46H
1EH
0FH
07H
08H
04H
6AH
```
#### Output register value 

9EH

### Program 3

#### Assemler language  

```{asm}
LDA 9H
SUB AH
ADD BH
SUB CH
ADD DH
SUB EH
ADD FH
OUT
HLT
D5H
64H
05H
62H
15H
44H
06H
```

#### Machine language

```{}
09H
2AH
1BH
2CH
1DH
2EH
1FH
E0H
F0H
D5H
64H
05H
62H
15H
44H
06H
```
#### Output register value 

EBH


### Program 4

#### Assemler language  

```{asm}
LDA 9H
ADD AH
ADD BH
ADD CH
SUB DH
SUB EH
SUB FH
OUT
HLT
37H
1BH
2BH
24H
0FH
17H
9FH
```

#### Machine language

```{}
09H
1AH
1BH
1CH
2DH
2EH
2FH
E0H
F0H
37H
1BH
2BH
24H
0FH
17H
9FH
```
#### Output register value 

5CH

## Sources

1. Digital computer electrionics A.P. Malvino, J.A. Brown.