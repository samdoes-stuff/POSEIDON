# This project needs a manual review


# 23/03/2026

After working for sometimes, I realized I need to journal everything or else I will forget. 

Massive change for now. Fully switched to RADXA CM4 for more options and feature around the same price. 
As I saw Jeff Geerling's youtube video previously, he mentioned that the Software support is bad. 

Also, I don't have a lot of experience in software. I mean no experience with embedded software. 

After inspecting through the schematic, I found a lot of good things. 

1. The connectors and even the connections of two parts of the CM4 are as same as Raspberry pi CM4. So 
I don't have to change the connections of those two. 
That means my Sensors and Connectors are going to be totally fine. 

2.  I was looking for active cooling. But I realized that I cannot afford pin in RP CM4. But RADXA solves this issue. 

3. Also, RADXA has amazing storage options. Onboard emmc, ssd, sata, sd card and even UFS. If you are wondering
what UFS are? Please check UFS out. I also got to know about UFS yesterday while navigationg RADXA. 

UFS are faster than emmc and can pack a lot of storage in small price. Hard thing is to source them. 

4. Also off mood, I will use this as my travel partner using my main ssd so It also provides the option. 

Danger:  It is too good true be true. I am doubting that Radxa CM4 can do lot of things at once. I have to do some research and update the journal. 

Time to fix my SSD portion and check the 40 pin gpio

decision changed again rooting for CM5. Better at eveything.


# 28/03/2026 

Plan changed again. I found out that Radxa is copy catting a chinese company and selling their module in a higher price. 
I found some more great option than RADXA CM5 which is SOM RK3399V2 from "Friendly Elec"  

It is much cheaper (87$) and meets most of my needs. I will use this hopefully I don't bring in any big change. 


Ahh may be I won't because I need the 40 pin gpio support for my carrier. eDP is supported in Radxa Cm5 but not used. I will definitely use the eDP let's see. 

what should I do? When I am focusing more on expandibility, I am losing some functions. Main purpose is to make a carrier board but when I am making something why don't I make this for my cyberdeck. Same thing but needs more time from me.  

Should I move on or I restart everything. Ohh boy!!!!

# 29/03/2026 

Pin config for my understanding 

First What is already equipped 

## PCIE-E key  
1. GPIO4_A1
2. GPIO4_A0
3. GPIO4_A2
4. GPIO3_A6
5. GPIO1_A3
6. GPIO1_A2
7. GPIO4_C3
8. GPIO1_A0
9. GPIO1_A1
10. GPIO2_C3
11. GPIO2_C0
12. GPIO0_C5
13. GPIO2_B7
14. GPIO0_C4
15. GPIO2_A6
16. GPIO2_A7
17. GPIO2_B0
18. GPIO2_B1
19. GPIO2_B2
20. GPIO0_B2
21. GPIO2_B3

## Type-C 
1. I2C6_SDA_M0
2. I2C6_SCL_M0
3. GPIO0_D3
4. GPIO1_D2

## Type-C 2
1. GPIO3_B4
2. GPIO0_D5
3. I2C7_SDA_M0
4. I2C7_SCL_M0

## PCIE3.0 M key 
1. GPIO4_B4
2. GPIO4_B5
3. GPIO4_B6

## eDP
1. GPIO3_A7
2. GPIO3_B7

## SD Card 
1. GPIO0_A4

## Ext_USB2.0 
1. GPIO1_B0

## Audio (Probably Need to change(I2S) the interface but GPIO remains)
1. GPIO1_A7
2. GPIO1_C4
3. I2C6_SDA_M0
4. I2C6_SCL_M0

## For navigator I need 4 pairs of RX & TX signal. 
1. TX1_RPI - GPIO1_B6 
2. RX1_RPI - GPIO1_B7
3. TX3_RPI - GPIO3_B5 
4. RX3_RPI - GPIO3_B6 
5. TX4_RPI - GPIO1_B3
6. RX4_RPI - GPIO1_B2
7. TX5_RPI - GPIO1_B5
8. RX5_RPI - GPIO1_B4

## I need 4 pairs of SDA & SCL
1. SDA0
2. SCL0
3. SCL1
4. SDA1
5. SDA4
6. SCL4
7. SCL6
8. SDA6

## I need 5 SPI
1. SPI_CS1 - 
2. SPI_CS2 - 
3. SPI1_SCLK -  
4. SPI1_MISO -  
5. SPI1_MOSI - 



# Exported Journal 

# DiveOut — Journal Export

- Exported at: 2026-06-24T10:57:21Z
- Project ID: 40
- Entries: 48

## Entry 1
- ID: 64
- Author: Shades
- Created At: 2026-03-14T16:30:46Z

### Content

Named the project. Though About what should I made. It was a basically a test recording to see if lapse work or not 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTczLCJwdXIiOiJibG9iX2lkIn19--1212fae5a056af1b5be21bd65dd9671dd03578b0/image.png)


### Recording Links



## Entry 2
- ID: 74
- Author: Shades
- Created At: 2026-03-15T04:02:37Z

### Content

Added the CM4 female connector to the schematics. It was sort and was part of  the lapse testing. ty

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg0LCJwdXIiOiJibG9iX2lkIn19--3691c1a5528cbc84d37dab1ab2e9eeb3524cc960/image.png)


### Recording Links



## Entry 3
- ID: 75
- Author: Shades
- Created At: 2026-03-15T04:04:36Z

### Content

Main goal was to make  a ROV so looked up some existing rov controller to make my design. Completed the UART section in the CM4. Took help from BLUE ROBOTICS NAVIGATOR design.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTg1LCJwdXIiOiJibG9iX2lkIn19--047dbe2c1aa03d4e98c86c010d7d45d2284b5e85/image.png)


### Recording Links



## Entry 4
- ID: 97
- Author: Shades
- Created At: 2026-03-16T03:55:42Z

### Content

Just finished the GPIO routing in  CM4. Basically using Blue Robotics Navigator Flight controller as a reference. Deciding which CM4 to select and using SD card or not. Probably will have space for both SD Card and SSD.

![Screenshot 2026-03-15 100433.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjM3LCJwdXIiOiJibG9iX2lkIn19--3894b7fe28180c8995eb35882c498feb4cfb4940/Screenshot 2026-03-15 100433.png)



### Recording Links


## Entry 5
- ID: 160
- Author: Shades
- Created At: 2026-03-18T09:32:53Z

### Content

Completely blundered the Schematics. I thought that kicad pin assignment refers to the exact pin of the connector. So I had to rechange everything. Had a bit of problem with lapse. I switched to Kicad to look up the CM4 PCB to ensure but lapse didn't capture it so If you see black screen, I swear I didn't tried to inflate hours. 

Also I was wondering what should I use. A sd card or a ssd. I didn't decided yet so I left it for later did some research though

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzgyLCJwdXIiOiJibG9iX2lkIn19--8df74ab5c32a1a20edb15d7c0b79066396ddd9d6/image.png)


### Recording Links



## Entry 6
- ID: 161
- Author: Shades
- Created At: 2026-03-18T09:59:24Z

### Content

Done the power indicating LED and GPIO pullup resistor. Kind of Just made the framework how the power and storage would look like.  Also changed the 3.3V power source to external. Thinking to provide external sources but how it will work I am not sure. Have to do a lot of research then.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzgzLCJwdXIiOiJibG9iX2lkIn19--5496214dfb0dda7678684d3f5491da1f14fee0c1/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6Mzg0LCJwdXIiOiJibG9iX2lkIn19--f658ceb0df70f203b08f1c134c5fe957b758f812/image.png)


### Recording Links



## Entry 7
- ID: 163
- Author: Shades
- Created At: 2026-03-18T10:06:56Z

### Content

Worked and researched on Sensors and decided what to put. Also worked on 5V power management to do the powers. Later I removed the 5V power section I thought I would use usb power also and some power modules. Later that I realized that high end rov controller has power sense module. I don't have a proper idea what this is. Will probably do some more research on that.

Also I worked with Leak Sensor, eeprom, Cm4 running indicator led  and called it a day. 

I am thinking how can I work with the power. That is the main issue now

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6Mzg3LCJwdXIiOiJibG9iX2lkIn19--a8bde3e1f6834c7e16b7c76c3791d3b2d813bcad/image.png)


### Recording Links



## Entry 8
- ID: 483
- Author: Shades
- Created At: 2026-03-26T10:29:02Z

### Content

Routed the Second CM4 connector.

 Added a HDMI support for using it as a device later. 
I may add a eDP display instead of HDMI or a USB-C display to avoid power problems. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTEzNywicHVyIjoiYmxvYl9pZCJ9fQ==--8b6c00d3ccd28498714d888934f79c9cb0992b0f/image.png)

Added leak sensor for working as a RC under water

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTEzNSwicHVyIjoiYmxvYl9pZCJ9fQ==--7b81e6133e1f9aebfa24a72b1ab0d1360c228c6e/image.png)

also for testing this controller with my joystick, I added analog input options 



![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTEzOCwicHVyIjoiYmxvYl9pZCJ9fQ==--93512a219f38502ce6c606ed8850a76b6b5d2031/image.png)


### Recording Links



## Entry 9
- ID: 485
- Author: Shades
- Created At: 2026-03-26T10:37:56Z

### Content

Made an expected PCB border and placed the board. 

I think I can fit all in pretty easily. 

Added the PWM channel as same as the Navigator one. It will be used to have ESC's signal and control some servos. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE0NCwicHVyIjoiYmxvYl9pZCJ9fQ==--bbfa89dc9cdaa3bfc71fa1dc6cf8bc4ff9d69a9b/image.png)


![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE0MywicHVyIjoiYmxvYl9pZCJ9fQ==--7639e10dffddc6e09a174527b38f5ddda6c7092b/image.png)


For the first time, I knew about array resistors. It is a package where multiple resistors are together to reduce the price. 

Also added SBUS to controll RC Signal if I think to fly it as a drone. It will be pretty cool. But I don't know how the Sbus system works in navigator. I will find out later.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE0NSwicHVyIjoiYmxvYl9pZCJ9fQ==--5503f96e43a91e02fdaa8ceaca9a7ed1f10d6b31/image.png)


### Recording Links



## Entry 10
- ID: 487
- Author: Shades
- Created At: 2026-03-26T10:45:36Z

### Content

Worked on Logic converter to expose some rx, tx and sda_scl output

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE0NiwicHVyIjoiYmxvYl9pZCJ9fQ==--f81e8fd3ce67731b491d5882c14ee49d5c95cd32/image.png)

Also worked on general Connectors which are pretty common for a RC controller. It is as just as navigator output.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE0OCwicHVyIjoiYmxvYl9pZCJ9fQ==--3ded783ee57e55c5c06d585336e988d4e45eb798/image.png)


### Recording Links



## Entry 11
- ID: 488
- Author: Shades
- Created At: 2026-03-26T11:28:35Z

### Content

Added some esd protections on HDMI. 
I want to add fast storage in this device. So I was thinking of two options one is SSD so that I can plug out my main one and use it. 
Another one is emmc or sd card. lemme think letter. 

Followed some M.key routing guide online. You can add so much feature to a M.2 connector. But checking my pins I realised I don't have enough CM4 outputs to make the best version it self. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE1MCwicHVyIjoiYmxvYl9pZCJ9fQ==--c3303209eaac5c8de7199a8185067800fcc04af7/image.png)

Also CM4 and CM5 both needs to attach an oscillator to the connector. 

And for clear 3V, we won't use normal one but step down the main 5V to 3V3. There is also a pin which is available in CM5 to control the power consumption of ssd which is not available in CM4. 


Also done the ethernet routing for network. I thought I would make the network switch with it  but that will be for later. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE0OSwicHVyIjoiYmxvYl9pZCJ9fQ==--91ed7a1c422c3fdcd4c84f99a83ec343852c79c6/image.png)



### Recording Links


## Entry 12
- ID: 489
- Author: Shades
- Created At: 2026-03-26T11:41:03Z

### Content

Did some research about M.2 footprint and found new atrocious storage option "UFS". It is a game changer. Faster than emmc and ssd and cheaper. But Radxa has module for it. 

Either I will make it onboard or I will do nothing. I tried to figured out what they are using as chips.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE1MSwicHVyIjoiYmxvYl9pZCJ9fQ==--585da544e4b2ae97f11ebb91ecc6d95ea0fcce34/image.png)


### Recording Links



## Entry 13
- ID: 493
- Author: Shades
- Created At: 2026-03-26T12:16:20Z

### Content

For sure CM4 is going to heat extremely. But I am out of pins to add a Active cooler fan. 

Even  I cannot add pwren to control the power of ssd. 

I was thinking about sacrificing some general connectors but I don't think it will work.  And also I will be using navigator ardupilot so ..... 

Also I have to add a camera for navigation. But I have to settle on some camera and lanes. I decided 4 lanes and found some long cable online at adafruit. 

I was researching some good connectors too but after sawing some schematic, I need more scl pins in 4 lane camera that CM4 doesnot have.  Imma crashout

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE1NiwicHVyIjoiYmxvYl9pZCJ9fQ==--f8c6182ad53fcef4802e188324dc5a87b30f7840/image.png)


### Recording Links



## Entry 14
- ID: 496
- Author: Shades
- Created At: 2026-03-26T12:43:58Z

### Content

Choosing RADXA CM4 instead of PI CM4. More pins more options but less software support. 

I changed again I will use CM5 now but the CM5 schematic 
is very bad for following and don't have the UFS support that I want and I will combine those two schematics and make some changes again 

checking out the GPIO pins are compatible with me schematics or not

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE2MCwicHVyIjoiYmxvYl9pZCJ9fQ==--8048c03aeb4270d91384a172f22f8093650fc7b2/image.png)


### Recording Links



## Entry 15
- ID: 497
- Author: Shades
- Created At: 2026-03-26T12:54:25Z

### Content

Researching about CM4 and RADXA CM5. Finding out which is better and suit my plane. Also Doing prize comparison. 

Procasinating about my plans. And started finishing my SSD and Started my Fan connector

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTE2MSwicHVyIjoiYmxvYl9pZCJ9fQ==--3e980a9aac82155daf279145979be3bdba026f18/image.png)


### Recording Links



## Entry 16
- ID: 538
- Author: Shades
- Created At: 2026-03-27T17:03:09Z

### Content

Routed the Connector 3 of RADXA CM5. Was actually doing some research about compute modules. I found orange pi also. But the orange pi is not in great stock. 
Also was looking for UFS and EMMC connector. Finally decided that I won't use no emmc and UFS. 

The onboard emmc is enough and my pcie will be transformed into wifi and bluetooth module for better connection. 

And the sd card would included to work as bootloader for my blueOs.  

Also finished the RTC connection. deciding which type of display to use. Probably won't use HDMI in a portable machine. Good news is RK3588s supports eDp but problem is sourcing display panel. 

Many of the display panel don't have a public datasheet and I don't want to take risk. 

For now, I will have HDMI, Type-C Display and a touch screen lcd for later. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTI1NCwicHVyIjoiYmxvYl9pZCJ9fQ==--090b764dd33df77dd969a022cbcccc95032340c5/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTI1NSwicHVyIjoiYmxvYl9pZCJ9fQ==--d4b69beb53b22b29e00167995e2e179fb654bb44/image.png)


### Recording Links



## Entry 17
- ID: 590
- Author: Shades
- Created At: 2026-03-28T14:41:38Z

### Content

Just doing the USB-C display option but my current went off sadly. I am still thinking about display options

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTM2MSwicHVyIjoiYmxvYl9pZCJ9fQ==--cad2771195411788b86425147535e3e86ed029fd/image.png)
 

### Recording Links



## Entry 18
- ID: 660
- Author: Shades
- Created At: 2026-03-29T17:39:35Z

### Content

Eventually rk3588 as lot of caabilities but for me options are limited at radxa CM5.  I found friendly elec rk3588 which is lot cheaper and very much expandable. Also saw a DIMM module which serves all of purposes but lacks gpios. 

I was thinking about smart choice like when I will use it as a computer, I won't use the gpio. Same thing vice versa. Use gpio don't us computer. This way I can save pins more easily. I will research on that later.

My main concern is now that. Can the friendly elec module successfully run while taking those load at once. I don't believe it. But if it can great for me.

I don't have any good picture for this season. This is the module's pic.

![Screenshot_20260329-233900.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTUwMSwicHVyIjoiYmxvYl9pZCJ9fQ==--c9fe9bc64259670fd97e334af7c6095c346b2008/Screenshot_20260329-233900.png)


### Recording Links



## Entry 19
- ID: 7728
- Author: Shades
- Created At: 2026-05-18T03:14:46Z

### Content

Working with the friendly Elec CM3588 Pinout. 
Matching the pinout with What I need and What is already equipped by my device. 
Most of the cases, I need a 3.3V gpio pin where there are also some 1.8V Gpio Pins. So we have to select carefully. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTY4ODYsInB1ciI6ImJsb2JfaWQifX0=--7eb2ae238b140ea05eafee7b0affbd8bbb441bc8/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTY4ODcsInB1ciI6ImJsb2JfaWQifX0=--a6cbdb5085cdc78265c99c85ece7a0c74c85e18b/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MTY4ODgsInB1ciI6ImJsb2JfaWQifX0=--8dd5ce32ea99c6009507660d326173c604006a20/image.png)


### Recording Links



## Entry 20
- ID: 9038
- Author: Shades
- Created At: 2026-05-25T04:46:18Z

### Content

Decided to move to RP CM4 again. Cause switching to rk3588 just adds cost and for ROV carrier solely I don't need so much functionality. 

So back to connector routing again. 

Quick thing about the GPIO voltage. Got to learn things about 1.8V & 3.3V internal power. So after reading rpi forums, the conclusion is I don't need 1.8V. It is only used in low power SD card connection but I will do the job with 3.3V.

Because I revisited the project after a long time, I have to revision the schematic and see where I am. That's why I am going through the sensors and addons which were referred by Bluerobotics Navigator Schematics. 

Going through the revision, I have a better power management in my mind. Separate 5V & 3V3 power for CM4. And another 3v3 power rail which comes from the 5V or input voltage.

Got a good idea about Global en and run PG. That is basically hardware reset switch one of which cuts off the power and the other cuts off the connection not necessarily the power. So, I may need them. 

Also, analyzing the pinouts, I learnt that A set of sda0 and scl0 is reserved for Camera or Display. And I need a camera  so I need that.

So cleared up some basic confusion with claude about the power management. As I am using external power, I  don't need to use any power from CM4 itself. Though I need the 3V3 output for activate the GPIO line through Gpio - Vref. Also there are certain things which are to be connected by the CM4 output according to Claude but  I rechecked and those are the 22 pin camera connector that's it.  So the power system is sorted for now. 

Also, I am not gonna use SD card. So, skipping the SD card portion for now. 

Putting the GPIO pins right now. Leaving the SYNC_IN and SYNC_OUT portion. Reasons? 
1. I don't have 1.8V enabled
2. I also don't have multiple CM4 to make use of this pin cause these are what those pins are really for (to syncronize their connection in a cluster and Camera)


![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAwMDAsInB1ciI6ImJsb2JfaWQifX0=--9e4ce77b50782586f662c9c16aa90331f707eff6/image.png)


### Recording Links



## Entry 21
- ID: 9115
- Author: Shades
- Created At: 2026-05-25T14:11:43Z

### Content

Researching on the eeprom nwp of the CM4. As for now what I got is, I don't need to bring this out as a jumper cause It is my personal product not a business product and with jumper it prevents emmc to be flashed with third pirty OS. 

Claude suggested me to pull it up,. But I went through documentation of the official CM4

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAwMzgsInB1ciI6ImJsb2JfaWQifX0=--3f9142ba0860d7224d4a05bac6af7c6a7065fd6f/image.png)

So, I came to conclusion that I don't need it to be pulled down permanently cause I need access to fan settings, HDMI and network  Boot.   

A jumper works just fine. 

Also, did some research about Ethernet and PHY signals and Exposed PHY signal with lan transformer. 

That is because many carrier does not use ethernet port. That make a inbuilt ethernet switch to connect to multiple devices. Especially, high end ROV carrier use sonar & dvl. With that on the way, PHY connections can give high speed Telemetry Data other than anything.  


After going through Blue Robotics website, It comes to my understanding that it is to paired with the very famous. Fathom x tether board which is able to give long range high speed ethernet. 

But after so much calculation I think I don't need all of that or any related hassle to deal with it. I have a sketch for what I can do is may be convert it to a switch rather than ethernet port or add a coaxial cable antenna for long range signal. 

Another slightly important thing I learnt. That is the ethernet jacks led should be powered by the CM4's 3V3 output. Not from my power source. 

Because in the official CM4 datasheet it is written that 

On Ethernet LED pins — pins 15, 17, and 19 are described as active-low Ethernet indicators explicitly labeled as CM4_3.3V signal with IOL = 8mA @ VOL < 0.4V. 

So another great thing I learnt.

New problem! 
Following the navigator schematics. It is clear that the power comes from a power module or a bec. Which normal for any ROV or drone. 

But my problem is what if I want to use it without power module or bec. At least, I have to connect it to a computer and upload the firmware or debug on it. Easiest solution is to use USB power. Which will only be used by the CM4 and anything related to boot it up. Not the sensors, motors or servos. 

I have make a another separate section of USB power.

Looks like CM4 is both capable of both Wifi and bluetooth. Then why you need to disable it. More research have to be done. 

For now, one connector is full completed. (Again with proper knowledge)

  
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAwNTMsInB1ciI6ImJsb2JfaWQifX0=--4cef0b4c0946723833b9993a46df3ede825d926a/image.png)


### Recording Links



## Entry 22
- ID: 9154
- Author: Shades
- Created At: 2026-05-25T17:19:13Z

### Content

Working with PCIE for my ssd. The reference I used for my ssd was from CM5. Now matching the pins I found out that two pins are not available in CM4 

1. PCIE_NWAKE &
2. PCIE_PWREN 

Both of them are absolutely necessary for good storage connection and to prevent short circuit damaging my ssd. 

After reviewing storage hat from this [project by will127534 ](https://github.com/will127534/CM4-Nvme-NAS/blob/main/RaspberryPiNVMeNAS.kicad_sch), I understood that I don't need the wake option but I certainly need the pwren pin. 

From his case, he used a micro-controller to provide that pin and set logic. I am also thinking of adding an micro-controller.  There is an another good reason to add a  mcu which is related to my previous journal. 

CM4 has both wifi and bluetooth. But only one is accessible through the onboard chip. So may be using wifi is a good choice. 

By using wifi, I can directly connect to the carrier and code the carrier without plugging the usb and disassembling  everything which is very helpful.

So, one reason for adding MCU is pcie pwren pin and another might be the the power source switching function more on that later. 

The camera 1 is chosen for my carrier camera cause it has 4 lanes and its design was done previously. 

The HDMI0 is used for the display. Cause it is the best output from CM4 and the audio signaling automatics routes to HDMI0. Also the port schematics was done previously.

The connector portion is finished. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAyMjksInB1ciI6ImJsb2JfaWQifX0=--808a64313fe8979f44fc3db15151975e84f10a8b/image.png)


Going in the accessories side of my board, I found that IIC connection is very important. But I know too little about it.  So, I have to learn the software side of it. 

I first thought of using a fan but I find it very high power 12V to be specific. Ans also using fan will create a negative pressure in the carrier. That's why I am skipping fan. Going to use only heatsink. 

Also, I spread misinformation about ethernet led power. I am very sorry for that. Since CM4's 3v3 is 180 mA is too little for providing power to anything almost. I think claude was tweaking. 

Working one the RTC. Suddenly got stuck with the crystal used in the RTC chip. Thankfully to some reddit post, I found specification for the crystal.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAyNTAsInB1ciI6ImJsb2JfaWQifX0=--22bf70fe499c39907d1a340cf58ce5c48770d163/image.png)

Learnt about the watchdog feature. which is actually lit !!!

There are many things that can be done but in simple terms if anything crashes or anything wrong with the network, it forces the Global En to do hard reset. 

So, it has a pulse system where it takes a break to restart and goes back to previous state. 

I can easily use this in carrier. If anything goes wrong rather than hardware, I don't have to do nothing. I may use the windows startup lookalike feature for my program. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjAyNjksInB1ciI6ImJsb2JfaWQifX0=--6ab0d62f5d4abccf4b49aabd71731df1b22a6723/image.png)


Now to the power, first of all I will refer to the Blue robotics Navigator power section. 


### Recording Links



## Entry 23
- ID: 9281
- Author: Shades
- Created At: 2026-05-26T04:10:37Z

### Content

Worked on the USB portion on the carrier. Plan is to figure out how many usb will I need.  All of the connection is USB 2.0 . So not many speed will be acquired. 

Also need a usb for my MCU programming. So keyboard and mouse will be connected for accessing the carrier so two port is need. One is OTG port which makes it a USB device and that is needed for firmware or software related stuff. 

Although, I do have a DC power brick but I want a USB power thing somehow. Because it is standard and works well in different country.   

So, total 5 USB is need for the board. Which is little excessive but workable. But I am thinking to use a Xiao rp2040 for it compactness. And the IO that is provides is more than enough for my job.  So 4 usb is final.

The USB hub chip is lil bit weird in official  CM4 io board schematics but none the less I am gonna use that. New problem acquired with the crystals specification used in the chip. I found some info for the chip's datasheet. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA1NzcsInB1ciI6ImJsb2JfaWQifX0=--a2b13649adf89bace4824ee91879aeb74511c2e1/image.png)


I told Ai to calculate its specification with 27 pf capacitor used in the official schematics. I found this one which will do the job. But according to calculation it is too over powered. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA1NzgsInB1ciI6ImJsb2JfaWQifX0=--0c10a97a04318c42458bdde98cdf98d984a9b69d/image.png)


But the crystal isn't correct cause it's four pin and I need 2 pin one. Atleast I found that.  

The decoupling of the 3v3 is just copy paste.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA1ODIsInB1ciI6ImJsb2JfaWQifX0=--cd8a41b67eb8515fece3edcaf0944ad2725654f1/image.png)


### Recording Links



## Entry 24
- ID: 9349
- Author: Shades
- Created At: 2026-05-26T12:36:15Z

### Content

USBhub is completed. I used USB-C for OTG. and two USB 2.0 Female Type-A for accessories to connect.  May use the other two ports for audio signal or some.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA3NTgsInB1ciI6ImJsb2JfaWQifX0=--b79555c28e5cef2282e32343ea06bdcdb40f3d92/image.png)


### Recording Link

## Entry 25
- ID: 9398
- Author: Shades
- Created At: 2026-05-26T16:12:21Z

### Content

Going to the power section, I am bit confused about the design. Cause I am referencing the Navigator Power section. And it looks like the navigator has two separate power input. One is in g eneral and the other one is for PWM channels. 

This what I think I did. I already recognized it and might did some work but I cannot find connections between those. May be I generalized all power as a whole and didn't keep two sections.

But I followed the toe to toe guidance as Navigator again. Cause I think that those power should be different cause they are analog power. But I don't know what bec is or I forgot what bec is. But I will try to include the whole bec in my board cause I don't want unnecessary modules. May be it is a important one who knows. 

 I was trying to read the BlueRobotics guide for how they connect their power to the board. I found their power supply which gives 5V 6A. which is great for on work. 

But when I will use hdmi or something I have find another way.

Looks like they don't have the schematics for that cause it is a of the shelf product.

Now, I am kinda lost about the power. The power thing is so complex. I may need to find out my own path.

I kinda figured out the power sense module. It is needed for watching the voltage and current of the battery going to the carrier. It is needed so Imma keep it up on my board.

Finished up the component sourcing + routing of the navigator power section. It was quite filled with resistor and capacitor.
 
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA4NTIsInB1ciI6ImJsb2JfaWQifX0=--bd89c671ad552ed04f36dd25915e2faffa3b5c92/image.png)

From my knowledge, I have to isolate the power section of the board cause it can heatup. GND stiching would be great for thermal.

Good thing is bluerobotics has the schematics for their power sense module which I can actually use. Implementing this right now.

So, actually I understood power sense module wrong. It is actually a observer between my power and my carrier and it gives out the information about voltage and current right through ardupilot. I did research because I don't want to implement something that I don't know about.


### Recording Links



## Entry 26
- ID: 9445
- Author: Shades
- Created At: 2026-05-26T18:58:41Z

### Content

Working on the power sense module refering to the BlueRobotics Power sense module schematic. 

Got to know that we have use as low tolerance as possible for accurate info. Cause Power is a very sensitive thing. 

For my tolerance, I kept it between 0.01%-0.1% and 50V operating voltage main power pass through.

For other design, I can easily get through the resistor and capacitor but power is sucker for mistake.

Power sense unit is complete 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA5NjgsInB1ciI6ImJsb2JfaWQifX0=--3e4b44fa99531e83da472821a4b666c5c4872b65/image.png)
 
Now, I have to work on auxiliary power when I am not using battery and also and step down module like bluerobotics which can give 5V 6A. Let just hope I can get something like that even for USB type-C that works.

Got to know what is pull low and pull high is. Image is given here  for your advantage 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjA5NzMsInB1ciI6ImJsb2JfaWQifX0=--3db5120a37395918b70ee4b0067d2f49a6b25bdf/image.png)

I think making a step down converter is risky. I found one but cannot focus right now. After reviewing the actual rp 4 model b. It also use 5V power from the usb. So, I will consider this tomorrow.

### Recording Links



## Entry 27
- ID: 9704
- Author: Shades
- Created At: 2026-05-27T17:35:47Z

### Content

Working on the dual power interfering. If my usb power comes then the raw power will stop.

Rather making a switch, I can make an another system which is I can change the CM4 intake system which can take both raw power and USB power but only takes whichever one is available.

From my previous session, I forgot to complete the power section. I didn't make the 3V3 regulator yet.  So, finishing that.

After couple of research, I come to a understanding that the navigators 3v3 isn't enough for my whole carrier. 

The reason navigator uses that 3v3 cause the pi model 4 has its own internal 3v3 power. I will refer to that. First, lemme finish navigator portion.

I may have to change the sensors 3v3 input name.
Changed the names.

New insight about the CM4 official IO board. I don't think It  will run on usb. Genuinely it needs a psu. Cause the 3v3 is close to 3A and the 5V is also close to 4/5A. 
So, there is no reason for not choosing the power module for BlueRobotics or using a PSU as per the RP instruction. 

Although the navigator portion will be as it is. Cause the hardware design suggest the 3V3 to move like that. 

So, yeah after watching the IO board video, I am officially confirmed that it needs the PSU. I actually feel dumb for not researching the actual Cm4 IO board in the first place. 

I am thinking not to include PSU on board. There would be a different module or board for that. But Finally I got the idea. 

Now, I have to crossmatch the navigator PSU to actually make one my self.

Honestly, unlike any other project, I read a lot less schematics. Cause the project is so big I don't want to mess up anything for my mistake. 

After researching a bit about 5V 6A, I found this board in blue robotics forum. I genuinely hope this can help me. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjE1MDksInB1ciI6ImJsb2JfaWQifX0=--99cd1275a07bdd5b91450df44f752ed04e770bde/image.png)

can this happen when input voltage in high but Amps is low and step down generates high Amps. 

Yes this is possible. I don't know the core about it yet but it was knowledgeful. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjE1MzcsInB1ciI6ImJsb2JfaWQifX0=--ea2be6709674396aa315d4db8246859b35c743e6/image.png)

Lots of research today but only less schematics.

### Recording Links



## Entry 28
- ID: 9720
- Author: Shades
- Created At: 2026-05-27T18:15:07Z

### Content

I finally figured out. I don't want to be stressed about power. The power will be 12V DC as mentioned in official IO board. In stead of building a power circuit, I rather change the input voltage or tweak the battery pack. 

I am still very confused about the power. Should I make the board for my own purpose or generalize it? Also making separate module aka pcb makes the carrier more safe. I mean what is the gurantee it will work 100%.  

I am still in a process of thoughts and don't know what to go ahead. Losing the motivation to work on by the way Half of the PSu in finished.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjE1NzAsInB1ciI6ImJsb2JfaWQifX0=--09d369046c1a7cdb16c5c0b9a7bd86265715ce09/image.png)

Also, I lot of research 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjE1NzEsInB1ciI6ImJsb2JfaWQifX0=--30a3862e99a8a5b106097387a8e6ffbbb74088d1/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjE1NzMsInB1ciI6ImJsb2JfaWQifX0=--42731082140aa7bac2ad3db00bd9de1d1555ae34/image.png)


### Recording Links



## Entry 29
- ID: 9922
- Author: Shades
- Created At: 2026-05-28T15:04:51Z

### Content

The end of power shit. I am tired. 

I have to make a power board. That is the solution. I don't want to mess thing up anymore.  

Middle of the power, I remembered to put ESD protection on my USB signals.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjE5OTQsInB1ciI6ImJsb2JfaWQifX0=--53f5c29089dc30e87b4f5a11c7250621bb4727b0/image.png)

Got stuck on the OTG section of the USB again which I actively skipped. The problem is caused  by the CC pins. 

Just got to know USB-C doesn't support OTG. Get fcked

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjIwMTEsInB1ciI6ImJsb2JfaWQifX0=--05fb32ba6c56dd323d1dcb7d941f09fb784726a5/image.png)

I hate to say but I have to do micro-USB. Also I made a mistake by using a two stack usb just like the IO board. But I don't need it rather it just increases the height of my carrier.

Yeah decision final. Separate Power Board. 

3V3 section is complete. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjIwNzMsInB1ciI6ImJsb2JfaWQifX0=--50741f72bfffef8dbc907846ccf5f4f68f1aa93e/image.png)

FInally moved to PCB. 

Just before moving to PCB, another realization hit me. I didn't check my power connectors Amp ratings or voltage ratings. So, There was a good chance that my connector would burn. I have rechanged those to good shit.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjIwNzYsInB1ciI6ImJsb2JfaWQifX0=--c8fc8e9ded8564b22ee1996bb1c640e030d24f3e/image.png)

Now another problem. If I stack those selected pins, those won't be together to put my wires. It has so gaps. And roaming around I couldn't decide on a high amps connector cause everything is just weird. 

I decided to use the connectors used by the BlueRobotics Navigator. Oh man! I can't just get out from the schematics. 

### Recording Links



## Entry 30
- ID: 10090
- Author: Shades
- Created At: 2026-05-29T09:04:18Z

### Content

I have to change and go through revision to make sure all the connector are capable of the power and current. 

Probably all set but there is a high chance I will see another problem after starting my schematics. 


![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjIyNzIsInB1ciI6ImJsb2JfaWQifX0=--f6731da977ab6081bb0fc086398c3c5104f60d4a/image.png)




### Recording Links



## Entry 31
- ID: 10103
- Author: Shades
- Created At: 2026-05-29T10:32:58Z

### Content

I am such a dumb for not using the RP CM4 official schematics. But the replacement was short timed.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjI3ODIsInB1ciI6ImJsb2JfaWQifX0=--8adb4fee1cdc747fc03c5edcf831dd5f3af29f07/image.png)

Instead of using jumper, I am thinking of using test pad and solder bridge some connections if needed.

Also, adding lots of test point in the power section. So that if anything goes wrong, I can figure that out.

Working on the PCB!!

### Recording Links



## Entry 32
- ID: 10157
- Author: Shades
- Created At: 2026-05-29T15:35:32Z

### Content

Starting with the power section. But first I had to manually make front silk screen small for components. 

working on the power section.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjI5MTAsInB1ciI6ImJsb2JfaWQifX0=--1e109d9db49d9115e00d69fe9d65889c13e05f21/image.png)

Just finished the power section with CMOS. But the space feels lil tight.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjI5MzUsInB1ciI6ImJsb2JfaWQifX0=--8bf71995824fe4b001839b14f2d65b90f5b1f35f/image.png)


### Recording Links



## Entry 33
- ID: 10205
- Author: Shades
- Created At: 2026-05-29T18:09:06Z

### Content

Placing the components out in the board.  It takes so much time.
![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjMxMjQsInB1ciI6ImJsb2JfaWQifX0=--fbc40a6845827c174379f37401b0561eee664259/image.png)

Space is so tight but have to fit all of the connectors. I am highly thinking about changing all to male connector

### Recording Links

Private

## Entry 34
- ID: 10473
- Author: Shades
- Created At: 2026-05-30T18:25:44Z

### Content

Wasting so much time on my power board. Couldn't find a suitable power connector for my board. 

Moving everything related to power to a separate power board. 

New knowledge!! I was wondering what  PSM712  do? 
It is like a loghtening rod for electro static power. Imma keep that.

Also, forgot to separate analog and digital gnd.

FInished the power board schematics. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjM4NjIsInB1ciI6ImJsb2JfaWQifX0=--18aeeb66bb29e2ae3070dbcdc63558218947d74c/image.png)


![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjM4NjQsInB1ciI6ImJsb2JfaWQifX0=--f84e47abbb759be9c60136801b4f687bac4c42c6/image.png)


Next stop is to put the power sense module.

### Recording Links

Private

## Entry 35
- ID: 10601
- Author: Shades
- Created At: 2026-05-31T06:39:12Z

### Content

Power Module is complete with the power sense module. The output  is a 5V and 3V3 pad. And the input is DC power Jack. 

Also there is 8 pin Power sense connection directly to the board.

![Screenshot 2026-05-31 123614.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQxNzUsInB1ciI6ImJsb2JfaWQifX0=--4bf0fe4dc6013d2c4dc13b3be7d46c19e894cf40/Screenshot 2026-05-31 123614.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQxNzYsInB1ciI6ImJsb2JfaWQifX0=--b395029e3550bdc853d7078c1e9efc4e5af8b0ad/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQxNzcsInB1ciI6ImJsb2JfaWQifX0=--7cb25168b7b27147e0314680795aed41aadc17c5/image.png)

![Screenshot 2026-05-31 123712.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQxNzgsInB1ciI6ImJsb2JfaWQifX0=--38e350f88629716069c9befc3b19506dedc50f32/Screenshot 2026-05-31 123712.png)


### Recording Links

Private

## Entry 36
- ID: 10840
- Author: Shades
- Created At: 2026-06-01T06:24:48Z

### Content

Following up with the design guide for my Power supply board.

Working on the silkscreen of the PCB.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQ3MjEsInB1ciI6ImJsb2JfaWQifX0=--c559f4fb60251e94413c0b1549da1a7e6faa90fb/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQ3MjIsInB1ciI6ImJsb2JfaWQifX0=--1238ca0b00b299a1bdd5bedfa570997131ac7efd/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQ3MjMsInB1ciI6ImJsb2JfaWQifX0=--730876b1d0a45161ae148f9db059e698f74eb035/image.png)


Finished for the power board for just now. I may change the design for better thermal efficiency.

Starting the high speed portion of my board.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQ3MzYsInB1ciI6ImJsb2JfaWQifX0=--2f96f287b200e58a97d8657c2d9390469430a5c1/image.png)


### Recording Links

Private

## Entry 37
- ID: 10926
- Author: Shades
- Created At: 2026-06-01T16:38:18Z

### Content

Working with high speed connections. Keeping them aside and make something out of the tight space to route my usb 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjQ4OTcsInB1ciI6ImJsb2JfaWQifX0=--670f53986cf2cf5e7f81ca92e416ab0e039b594a/image.png)

Removing ESD protection from HDMI. Camera and HDMI routing is complete. I am satisfied. 

Changing the ethernet connector cause it is upside down.

### Recording Links

Private

## Entry 38
- ID: 11111
- Author: Shades
- Created At: 2026-06-02T11:30:15Z

### Content

USB routing

The usb routing was a real pain. Couldn't find a single way to match their length finally did it. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjU0NzMsInB1ciI6ImJsb2JfaWQifX0=--6f0e169f456956cef07a8d2843f2312bfcde5b26/image.png)

Full usb section is complete 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjU0NzQsInB1ciI6ImJsb2JfaWQifX0=--819e52a3569d834cff14092e8b743027408f2f87/image.png)


### Recording Links

Private

## Entry 39
- ID: 11154
- Author: Shades
- Created At: 2026-06-02T16:07:00Z

### Content

I was actually in progress with making changes with my ethernet but somehow I forgot. Today, when I was going to peer review the PDF then I noticed. Finished the unrouted esd protection on ethernet. 

Moving on to the ssd. I couldn't find the necessary outline for my ssd. I could only find the connector. Then I found a kicad file in my old folders.

Had to choose some smaller footprints for my board. 

Heading to the PCIe routing of my board. The power section is under the ssd. Hopefully it fits.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjU2MjAsInB1ciI6ImJsb2JfaWQifX0=--d0f84a5452fd56f793090ba4e2db848c6ce0677b/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjU2MjEsInB1ciI6ImJsb2JfaWQifX0=--f49e0fcbcc9b3f866a9573228e542774f7db3467/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjU2MjIsInB1ciI6ImJsb2JfaWQifX0=--5586964fd5db7949c84e09b06265167d45f68a7f/image.png)


### Recording Links

Private

## Entry 40
- ID: 11326
- Author: Shades
- Created At: 2026-06-03T06:06:48Z

### Content

I am really crashing out. Cause the space is short and more connectors are here and there. I am passing a very hard time placing the components. and possibly figuring out their connections. I will take a rest and think about it.

Going to change the CM4 placement. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjYxMjAsInB1ciI6ImJsb2JfaWQifX0=--fd65f7ef053cfd70e41b960016dbc0ed3dada444/image.png)


### Recording Links

Private

## Entry 41
- ID: 11353
- Author: Shades
- Created At: 2026-06-03T10:01:06Z

### Content

High speed routing is a no joke. I am glad that I can get this result. Hope gully to soon finish my high speed routing. Then I have to move to ADC routing and section that.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjYyODUsInB1ciI6ImJsb2JfaWQifX0=--369ba91e4422e690b113dae132e1c4ecf8abe627/image.png)

![Screenshot 2026-06-03 155750.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjYyODYsInB1ciI6ImJsb2JfaWQifX0=--ae42cf2bc2bcef2a537b413a68ba3668e3a904ac/Screenshot 2026-06-03 155750.png)


### Recording Links

Private

## Entry 42
- ID: 11562
- Author: Shades
- Created At: 2026-06-04T08:20:08Z

### Content

Not much progress done. Finished off the High speed connectors IO port. Things are so messy, I can't get my mind on organizing it. 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MjY4ODMsInB1ciI6ImJsb2JfaWQifX0=--1fa7518e1297e8a2445b500184f34dd56aedbce9/image.png)


### Recording Links

Private

## Entry 43
- ID: 12944
- Author: Shades
- Created At: 2026-06-10T05:37:24Z

### Content

Just doing the IO routing and planning out the component placement. There is not much to explain rather than following up with routing process 

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzA0MjIsInB1ciI6ImJsb2JfaWQifX0=--2a2fd18c3bdee612319339ea008b22e23d0609c8/image.png)


### Recording Links

Private

## Entry 44
- ID: 12983
- Author: Shades
- Created At: 2026-06-10T10:06:33Z

### Content

A big turn from me. I am removing nvme ssd from my carrier. Cause a thought suddenly striked me that is 

Is using nvme in a AUV carrier a good practice? I don't think so. Cause the power is so disruptive and a short circuit can brick the nvme

And that is why I don't see many even professional carriers to use ssd. 

It is quite sad and exciting at the same time. 

Sad cause I was so determined and lost so much effort. 

exciting cause I can fit everything in one side.

The thing is I can make use of the PCIE. 
One of the good uses in usb 3.0 but the 1.05V is another pain. Cause it needs separate power section. 

So I am figuring out what I can do.

Thinking about utilizing with Google Coral. Which will give me a npu support for ai through usb

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzA1NTksInB1ciI6ImJsb2JfaWQifX0=--51f888e95ef3518f1b5e78d98f2b5dab24fabec0/image.png)


## Entry 45
- ID: 12992
- Author: Shades
- Created At: 2026-06-10T11:20:16Z

### Content

Removed the SSD and related power converters and working on the USB 3.0. U can actually get two usb 3.0 but current I don't need one. I am quite happy with one. Challenge is I have to tight fit it in the PCB.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzA1OTEsInB1ciI6ImJsb2JfaWQifX0=--41d580ad5c0a1b30c34f6dd4042e0c7d27385474/image.png)


### Recording Links


## Entry 46
- ID: 15521
- Author: Shades
- Created At: 2026-06-20T08:47:35Z

### Content

Doing the routings of my PCB. 

Made a separate +1.05v copper section for my usb 3.0. 

Finally started routing on the GPIO. I choose a separate layer for GPIO signals as will as using the bottom layer for it. 

Lots of back and forth of design and almost finished the routing. 

For analog signal made a separate copper plane and agnd is connected to star gnd with a 0 ohm resistor

  
![Screenshot 2026-06-20 141635.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzcwMjIsInB1ciI6ImJsb2JfaWQifX0=--2b10274e9dce85f8b9c9cacba8e531d04a5aeb2f/Screenshot 2026-06-20 141635.png)


### Recording Links

Private

## Entry 47
- ID: 16027
- Author: Shades
- Created At: 2026-06-22T05:46:39Z

### Content

Making a revision out of my board. 

I am now using two copper gnd plane. 
Removed the ADC Channel controller. 

Removed the CMOS battery 

Re doing the power option cause it is very critcial. 

Reading docks about power. Now that I think about it, efuse is need if any sort required. 

Have to upgrade to better sensors cause Navigator uses some old ass sensors. 

My smd ethernet takes so much space and I don't like it so I am switching that to Through hole cause there is no line under it and it looks beautiful. 

Realized that the CM4 csi camera is of no use cause it has a very short range. I will convert it to ethernet so that I can use good camera and get a long range

Back to sensor I upgraded my barometer with more better sensor. Now I have to upgrade my IMU but the BMI088 needs two CS pin for Full flex SPI connection where I have only one. I need to figure it out later. 

Back to the ethernet

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6Mzg0MzgsInB1ciI6ImJsb2JfaWQifX0=--49d1a3dc25e2e88e08d11c841d02354f5f67e11a/image.png)


### Recording Links

Private

## Entry 48
- ID: 16139
- Author: Shades
- Created At: 2026-06-24T08:28:59Z

### Content

Finished working on the Lan transformer and  Jst twisted pair connection. 

These IC's require 2KV 1nF caps. And also most of them are stock out from the market. Have to find a way to source them. 

looking at the ICs open source project, I realized that they didn't route any differential pair under the IC. They used a lot of gnd vias . But I did route under it and now thinking of switching it. 

Have to do more research on it.



Also, Moved all the indicator led's to the side so that it looks clean and organized>



![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzkwMDYsInB1ciI6ImJsb2JfaWQifX0=--91bc3a78395bd134b84e64463447749bc0b57200/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6MzkwMDcsInB1ciI6ImJsb2JfaWQifX0=--96b3a6ff7272495e3e155f639adc15cef12de4d3/image.png)



### Recording Links

Private


## Entry 49
- ID: 16214
- Author: Shades
- Created At: 2026-06-25T16:07:08Z

### Content

Moving all the GPIO and leds to one side. 

But shit How I removed all the GND Vias. I need to redo everything. I hate me .

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6Mzk1NTQsInB1ciI6ImJsb2JfaWQifX0=--b145754c932bfa2b1cf20a195952f6e2242d9121/image.png)


### Recording Links



## Entry 50
- ID: 16427
- Author: Shades
- Created At: 2026-07-02T16:40:51Z

### Content

Pretty a progress. 

The Leds were sorted out and they turned out pretty good and I am very happy with results. It obviously took some routing revisions before it was done. 

I moved to the Connector section. Had to calculate space and best orientation to put the connectors. Also, it turned out pretty clean although there is some tight connections, I think it should be fine. 

I have to do research how to measure this signals integrity and how to identify good and bad signals. Recently, I saw a video where "Why Analog channel buffer is important" was discussed. 

My first Idea of removing E-Fuse from the board has been changed dramatically . Cause I now want really a good 5V and 3v3 protections. I am putting so much effort so making it polish adds no cost but my sanity. 

The protection IC TPS259474LRPWR fits so perfect in so tight space or I may found the perfect orientation. I guess my routing skills improved day by day. 

After scouting some MATE ROVs, I found that analog signal is important. So, I have to find a way to add it. But no dedicated Analog chip cause it takes so much detailing than I want to take.  For my case, I am not expert and also I am not finding any reference to do that. 

So, the most sensible option is to add a Secondary MCU which can fit in tight spaces. 

Also, there are three user configurable LEDs which I can use but I only need 2 may be and I will use on of the GPIOs to my IMU to achieve SPI connection which is faster than I2C.  

My user configure LEDs would be to status my co processor and to status my Sensor establishment.

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA2NTUsInB1ciI6ImJsb2JfaWQifX0=--7df8c40962f4f2af0ca0d4ed69e0d699da5ef2e0/image.png)

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA2NTYsInB1ciI6ImJsb2JfaWQifX0=--78550e5b1be71a3983f2945bb0ee135edf299395/image.png)


### Recording Links



## Entry 51
- ID: 16461
- Author: Shades
- Created At: 2026-07-05T18:30:05Z

### Content

Finished up routing the Sensors and cleaning my routes. 

Cleared a whole backlog of DRC error. 

And working on the Silkscreen of my PCB and exposing testpads in the back

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA3NjcsInB1ciI6ImJsb2JfaWQifX0=--cfb7475ebf9c2d99e1f8cf8ee08ce8e9dd5b04e3/image.png)



![Screenshot 2026-07-06 002935.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA3NjgsInB1ciI6ImJsb2JfaWQifX0=--c0ec0f1a038d6d401f986ad0c1110408057a59ae/Screenshot 2026-07-06 002935.png)


### Recording Links

## Entry 52
- ID: 16477
- Author: Shades
- Created At: 2026-07-07T03:34:36Z

### Content

Pretty Much Finished the Silkscreen of the PCB. Now it is the time for Power Sensing and Stuff. 

I quite a while ago removed the ADC IC from my carrier which was used in Navigator. But I realise I need that again cause I got 2 ILM pins from my E-Fuse.  ILM is current monitor output.  Which is ADC channel now I have to convert it to I2C so that I can put that in same I2C bus as Compass and Pressure Sensor

Also, I have to make place for my 12V powers sensing tooo. 

 Also, I did not realise that I have to length match the SPI connection in 50 ohms. So that was a cool trade off.


![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA4MTksInB1ciI6ImJsb2JfaWQifX0=--72f2f5c6b7fff3f390ba685ed29661b3df0f4ed3/image.png)

![Screenshot 2026-07-07 093409.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA4MjAsInB1ciI6ImJsb2JfaWQifX0=--eba4e8dd1c51e7f7a169ac8709e8231e51fdc25b/Screenshot 2026-07-07 093409.png)


### Recording Links


## Entry 53
- ID: 16512
- Author: Shades
- Created At: 2026-07-08T17:42:31Z

### Content

Finally finished the PCB. 

Made the test points 1mm diameter. Added silkscreen. 
Worked on making BOM and component sourcing. 

Also, finished the ADS chip routing. 

Here are some cool photos 

![Screenshot 2026-07-08 131203.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA5MjUsInB1ciI6ImJsb2JfaWQifX0=--1f4c3d5fccd5f4001465023937f73cd94a9df303/Screenshot 2026-07-08 131203.png)

![Screenshot 2026-07-08 150344.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA5MjYsInB1ciI6ImJsb2JfaWQifX0=--811d899bc6b6beba8e3cced40d3cef604d129893/Screenshot 2026-07-08 150344.png)

![Screenshot 2026-07-08 150350.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA5MjcsInB1ciI6ImJsb2JfaWQifX0=--f59a982020b809b0616f681f694d47477083193f/Screenshot 2026-07-08 150350.png)

![Screenshot 2026-07-08 150404.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA5MjgsInB1ciI6ImJsb2JfaWQifX0=--ad80014922cdd94d93cbd83c35ddbd495d84fc7e/Screenshot 2026-07-08 150404.png)


![Screenshot 2026-07-08 150414.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA5MjksInB1ciI6ImJsb2JfaWQifX0=--989916719eea2826f88fb5766055683a03c6f8e5/Screenshot 2026-07-08 150414.png)

![Screenshot 2026-07-08 162304.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA5MzAsInB1ciI6ImJsb2JfaWQifX0=--7b080dfdbfe3c0be6972532921d6d3c5b0cd386e/Screenshot 2026-07-08 162304.png)

![Screenshot 2026-07-08 162314.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDA5MzEsInB1ciI6ImJsb2JfaWQifX0=--f558c3219cee954af9214cb73d67e244fbc4c21c/Screenshot 2026-07-08 162314.png)


### Recording Links


Total hours - 136
