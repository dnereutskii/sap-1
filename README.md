# Simple as posible 1 computer (SAP-1) on logisim

## Brief

## Architecture

## Macroinstruction

Every instruction devides on operation code (high nibble) and address field (low nibble).


No | Mnemonic | OpCode
:---:|:---------------:|:-------------:
 1   | LDA          | 0b0000 
 2   | ADD            | 0b0001
 3   | SUB           | 0b0010
 4   | OUT           | 0b1110
 5   | HLT            | 0b1111


## Fetch microinstruction

## Programs

### Program 1

### Program 2

Assemler language  

```{asm}
LDA 9H
SUB AH
ADD BH
SUB CH
ADD DH
SUB EH
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

Machine language

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

### Program 3

### Program 4


## Sources

1. Digital computer electrionics A.P. Malvino