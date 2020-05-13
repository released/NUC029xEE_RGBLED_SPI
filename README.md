# NUC029xEE_RGBLED_SPI
 NUC029xEE_RGBLED_SPI


update @ 2020/05/13

1. Use SPI MOSI (PC3) , to send WS2812 data 

	- T1H 1 HIGH 580ns~1μs		target : 0.750 us

	- T1L 1 LOW 220ns~420ns		target : 0.375 us

	1111 1100 (0xFC)	==> if SPI = 7M

	- T0H 0 HIGH 220ns~380ns		target : 0.375 us

	- T0L 0 LOW 580ns~1μs			target : 0.750 us

	1100 0000 (0xC0)	==> if SPI = 7M	

	- RES : more than 280μs

2. upload picture (bit 1 , bit 0) for reference

	- bit 1 : ideal high level 0.375x2 us , low level 0.375x1 us

	- bit 0 : ideal high level 0.375x1 us , low level 0.375x2 us

##Scenario : 

1. Default LED pattern will show index state_AllColors in StateMachine function

2. DemoState auto increase , to demo each LED pattern
