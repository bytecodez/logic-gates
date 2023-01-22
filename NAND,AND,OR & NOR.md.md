

### NAND

![alt text](https://i.imgur.com/chDyuSA.png)
- output of NAND is determined by A * B as a Complement

- Logically complements the result of ANDing the contents of two general-purpose registers and stores the result in another general-purpose register.

- The **nand** instruction logically ANDs the contents of `general-purpose register `(GPR) _RS_ with the contents of GPR _RB_ and stores the complement of the result in the target GPR _RA_.

- The **nand** instruction has two syntax forms. Each syntax form has a different effect on Condition Register Field 0.

---

### AND 
![alt text](https://i.imgur.com/mosb8QD.png)
- output of AND is determined by A * B 
- Logically ANDs the contents of two general-purpose registers and places the result in a general-purpose register.


The **and** instruction logically ANDs the contents of general-purpose register (GPR) _RS_ with the contents of GPR _RB_ and places the result into the target GPR _RA_.

The **and** instruction has two syntax forms. Each syntax form has a different effect on Condition Register Field 0.

- The two syntax forms of the **and** instruction never affect the Fixed-Point Exception Register. If the syntax form sets the Record (Rc) bit to 1, the instruction affects the Less Than (LT) zero, Greater Than (GT) zero, Equal To (EQ) zero, and Summary Overflow (SO) bits in Condition Register Field 0.

---

### OR
![alt text](https://imgur.com/urIXRSo.png)
- output of OR determined by A + B
- Logically ORs the contents of two general-purpose registers and stores the result in another general-purpose register.

- The **or** instruction logically ORs the contents of general-purpose register (GPR) _RS_ with the contents of GPR _RB_ and stores the result in GPR _RA_.
- The **or** instruction has two syntax forms. Each syntax form has a different effect on Condition Register Field 0.

- The two syntax forms of the **or** instruction never affect the Fixed-Point Exception Register. If the syntax form sets the Record (Rc) bit to 1, the instruction affects the Less Than (LT) zero, Greater Than (GT) zero, Equal To (EQ) zero, and Summary Overflow (SO) bits in Condition Register Field 0.

---

### NOR

![alt text](https://i.imgur.com/cozrO89.png)
- output of NOR is determined by A + B as a complement 
- Logically complements the result of ORing the contents of two general-purpose registers and stores the result in another general-purpose register.

- The **nor** instruction logically ORs the contents of general-purpose register (GPR) _RS_ with the contents of GPR _RB_ and stores the complemented result in GPR _RA_.

- The **nor** instruction has two syntax forms. Each syntax form has a different effect on Condition Register Field 0.

- The two syntax forms of the **nor** instruction `never affect the Fixed-Point Exception Register`. If the syntax form sets the Record (Rc) bit to 1, the instruction affects the Less Than (LT) zero, Greater Than (GT) zero, Equal To (EQ) zero, and Summary Overflow (SO) bits in Condition Register Field 0.