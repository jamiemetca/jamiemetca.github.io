31/10/2025

# SREG
Is an 8 bit status register, which has two purposes.
- Status flags for the ALU (Arithmetic logic unit)
- Control/Storage bits (I,T)

## General control (I)
Controls whenether the CPU can respond to any external or peripheral interrupts.
Set to 1 for interrupts to be active.

```c
/* Status Register */
#ifndef SREG
#  if __AVR_ARCH__ >= 100
#    define SREG _SFR_MEM8(0x3F)
#  else
#    define SREG _SFR_IO8(0x3F)
#  endif
#endif

/* My Arduino Uno R3 microcontroller has the __AVR_ARCH__ value of 5*/

/*
    hex = 0x3F
    binary = 00111111
*/

/*
    __SFR_OFFSET = 0x20;
    hex = 0x20
    binary = 00100000
*/

#define _SFR_IO8(io_addr) _MMIO_BYTE((io_addr) + __SFR_OFFSET)

#define _MMIO_BYTE(mem_addr) (*(volatile uint8_t *)(mem_addr))

/*
    io_addr =       0x3F =   00111111
    __SFR_OFFSET =  0x20 =   00100000
    mem_addr = io_addr + __SFR_OFFSET
    mem_addr = 00111111 + 00100000 = 01011111
    mem_addr = 01011111
    SREG = 01011111
*/
```
If the value of SREG is correct, this means the global interrupt is disabled.


### \__AVR_ARCH__
Is a built in msvto frginrf by the avr-gcc compiler to indeicate the specific instruction set architecture (ISA) verion of "core" of the target AVR microcontroller.

### \_SFR_IO8(0x3F)
Used as the \__AVR_ARCH__ value is less than 100 for my microcontroller SREG

Defined as;
```c
```














The SREG bits are set using the below code.
Haven't investigated this code.
```c
/* SREG bit definitions */
#ifndef SREG_C
#  define SREG_C  (0)
#endif
#ifndef SREG_Z
#  define SREG_Z  (1)
#endif
#ifndef SREG_N
#  define SREG_N  (2)
#endif
#ifndef SREG_V
#  define SREG_V  (3)
#endif
#ifndef SREG_S
#  define SREG_S  (4)
#endif
#ifndef SREG_H
#  define SREG_H  (5)
#endif
#ifndef SREG_T
#  define SREG_T  (6)
#endif
#ifndef SREG_I
#  define SREG_I  (7)
#endif
```
