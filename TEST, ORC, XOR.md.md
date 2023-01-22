## Test Instruction
- In the x86 assembly language, the TEST instruction performs a bitwise AND on two operands. The flags SF, ZF, PF are modified while the result of the AND is discarded. The OF and CF flags are set to 0, while AF flag is undefined. There are 9 different opcodes for the TEST instruction depending on the type and size of the operands. It can compare 8-bit, 16-bit, 32-bit or 64-bit values. It can also compare registers, immediate values and register indirect values.
```asm
; Conditional Jump
test cl,cl   ; set ZF to 1 if cl == 0
jz 0x804f430  ; jump if ZF == 1

; Conditional Jump with NOT
test cl, cl   ; set ZF to 1 if cl == 0
jnz 0x804f430  ; jump if ZF == 0

; or
test eax, eax  ; set SF to 1 if eax < 0 (negative)
js error ; jump if SF == 1

;regular application
test al, $0F      ; set ZF if "al AND $0f = 0" (here: address-align test for 16b)
jnz @destination  ; jump if eax IS NOT "MODULO 16=0"
```


## Orc instruction
- Logically ORs the contents of a general-purpose register with the complement of the contents of another general-purpose register and stores the result in a third general-purpose register.
- The **orc** instruction logically ORs the contents of general-purpose register (GPR) _RS_ with the complement of the contents of GPR _RB_ and stores the result in GPR _RA_.

- The **orc** instruction has two syntax forms. Each syntax form has a different effect on Condition Register Field 0.

- The two syntax forms of the **orc** instruction never affect the Fixed-Point Exception Register. If the syntax form sets the Record (Rc) bit to 1, the instruction affects the Less Than (LT) zero, Greater Than (GT) zero, Equal To (EQ) zero, and Summary Overflow (SO) bits in Condition Register Field 0.


## Xor instruction

- xor = exclusive or, bitwise comparison operator
    - XOR is reversable meaning 0x8C ^ 0x2C = 0xA0 and 0x8C ^ 0xA0 = 0x2C
    - xor is a cheap way to encrypt data with a password
    - if the two arguments are the same the output is 0
    - if the two arguments are different the output is 1
    - more on xoring: https://ctf101.org/cryptography/what-is-xor
    - examples:
      ````
        bit1  bit2  equals
         0      0     0
         1      1     0
         1      0     1
         0      1     1
      ````
        - ![alt text](https://i.imgur.com/zHA07QB.png)
        - ![alt text](https://i.imgur.com/B3kGS7E.png)
          xor EAX, EAX  ; EAX now equals 0
