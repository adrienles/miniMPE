# mcu choice
## picks
### stm32f407
#### pros
- powerful
- 2 usb phys
- st, so good software support/docs
#### cons
- expensive
  - ~$2.70/u
- power consumption
  - ~87 mA at max freq + peripherals
    - too much for final product if daisy chaining a bunch (say 5 sections + 1 host for 61 keys, 6*87 = 522 mA, which might be pushing it for bus/battery power)
### ch32v203
#### pros
- decent power
- 2 usb phys
- cheap*
  - c8 @ ~$0.84/u
    - this variant only has 10 adc channels, which would require an extra analog mux
  - rb @ ~$1.69/u
    - this variant has 16 adc channels, which is just enough. however, the cost difference is large enough where the extra mux might be worth it
- low power
  - ~11.8 mA at max freq + peripherals
#### cons
- far from the best support/docs...
- cheap variant has few adc pins