# STM32F767ZI GPIO Output Driver — BSRR

Bare-metal GPIO output driver for the NUCLEO-F767ZI. 
Controls the onboard green LED (PB0) by developing 
an output driver using direct register manipulation 
(RCC, MODER, BSRR) without HAL libraries.

## Hardware
- Board   : NUCLEO-F767ZI (STM32F767ZI)
- LED     : LD1 Green → PB0
- Core    : ARM Cortex-M7

## What It Does
- Enables clock access to GPIOB via RCC_AHB1ENR
- Configures PB0 as output pin via GPIOx_MODER
- Blinks LED using GPIOx_BSRR register

## Registers Used
| Register       | Purpose                  |
|----------------|--------------------------|
| RCC->AHB1ENR   | Enable GPIOB clock       |
| GPIOB->MODER   | Configure PB0 as output  |
| GPIOB->BSRR    | Set and reset LED pin    |

## Reference Documents
- RM0410 — STM32F76xxx Reference Manual
- UM1974 — NUCLEO-144 User Manual
- STM32F767ZI Datasheet
