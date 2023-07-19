### About
NeohertzFC4 is my version of of a STM32F405 based flight controller, meant to operate quadcopters.
I developed this because I was curious what really went into the development of a flight controller; they seemed like relatively simple 
devices to cost so much. My goal was to develop something relatively simple and low-cost, and so that's why I opted to use the STM32F4 rather than an F7. Other 
open source designs (there aren't many!) aren't easy to interact with or order: they aren't in KiCAD and aren't on GitHub/Gitlab. So another one of my goals was to
provide a sort of template that would not only make my own development easier, but make it easier for other people as well. 

#### Features
- STM32F405RGTx main computing chip
- BMP280 barometer
- MMA8452QR1 accelerometer
- LIS3MDL magnometer
- AT7456 analog OSD chip
Bonus: LIS3DH accelerometer included as well, since I wanted to add support for it in betaflight

### Updates
- July 19th, 2023: I ordered the parts for the first 5 prototypes after working on the design for about a week. All the parts should be here in about two weeks.

### Potential issues
- There aren't many (if any at all) alternative parts for certain ICs. If one were to go out of stock, a small redesign would have to be done to use a different solution.
As of right now, the hardware is completely untested.

### Future plans
As of the first revision, there is only one onboard BEC. This means there is only a 5V rail and no 9v (or 10v/12v) rails for a digital 
video system. I am planning on adding a second BEC for that purpose, but it didn't fit with my initial goal of having all the core components on
the top of the PCB. 

I'm also interested in creating a version of this with an AT32 chip instead of an STM32. As far as I can tell they are cheaper, but not necessarily more
available. I'm inclined to making a board that can have either an AT32 or an STM32 chip, that way you could just select whichever one is best at the time. 
Of course, this hinges on betaflight actually having decent support for AT32 chips, since I don't personally have time to add support. 


#### License
GNU General Public License v3.0
