# intercommunication protocol ideas
## options
### usb
#### pros
- naturally, a usb-c connector could be used
- sections could be used and connected to a host device independently, which is a neat feature
#### cons
- to respect the spec (which should be done), only 5v could be passed, requiring each section to regulate its own power instead of simply the host section
- thick protocol layer that is kinda useless in this scenario, could add latency
### i3c
#### pros (especially over i2c)
- hot-join support!
- dynamic addresses (important!)
#### cons
- veeeeery few mcu support it, so it's a no go
### uart
#### pros
- very simple
- could just fifo into the previous section, until the host section
- a very basic mcu could be used
#### cons
- janky i guess?
## choice
- i really like the appeal of each half working on its own, so usb is a natural first choice
  - more extensive testing is needed. if usb does the trick, i'll probably go forward with it