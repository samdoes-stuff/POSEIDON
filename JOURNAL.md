
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

<img width="1596" height="812" alt="image" src="https://github.com/user-attachments/assets/76d2a7a8-eb4f-40a5-8ca4-3a84246cd516" />



### Recording Links
- https://public.lapse-hackclub.link/timelapses/FkCdQ_rLYuiU/timelapse-FkCdQ_rLYuiU.mp4


## Entry 2
- ID: 74
- Author: Shades
- Created At: 2026-03-15T04:02:37Z

### Content

Added the CM4 female connector to the schematics. It was sort and was part of  the lapse testing. ty

<img width="665" height="637" alt="image" src="https://github.com/user-attachments/assets/c11c6c58-f323-4b08-ade2-677beb171054" />



### Recording Links
- https://public.lapse-hackclub.link/timelapses/iTI5UaLuOtzo/timelapse-iTI5UaLuOtzo.mp4


## Entry 3
- ID: 75
- Author: Shades
- Created At: 2026-03-15T04:04:36Z

### Content

Main goal was to make  a ROV so looked up some existing rov controller to make my design. Completed the UART section in the CM4. Took help from BLUE ROBOTICS NAVIGATOR design.

<img width="770" height="619" alt="image" src="https://github.com/user-attachments/assets/ee76a77b-2834-4d33-9440-aac3d0a7f111" />



### Recording Links
- https://public.lapse-hackclub.link/timelapses/X69BuqMKmmVY/timelapse-X69BuqMKmmVY.mp4


## Entry 4
- ID: 97
- Author: Shades
- Created At: 2026-03-16T03:55:42Z

### Content

Just finished the GPIO routing in  CM4. Basically using Blue Robotics Navigator Flight controller as a reference. Deciding which CM4 to select and using SD card or not. Probably will have space for both SD Card and SSD.

<img width="770" height="619" alt="image" src="https://github.com/user-attachments/assets/4e5356ef-cc85-41db-b6cb-04e76e9e8c34" />




### Recording Links
- https://public.lapse-hackclub.link/timelapses/mEafCGJjIkwj/timelapse-mEafCGJjIkwj.mp4

## Entry 5
- ID: 160
- Author: Shades
- Created At: 2026-03-18T09:32:53Z

### Content

Completely blundered the Schematics. I thought that kicad pin assignment refers to the exact pin of the connector. So I had to rechange everything. Had a bit of problem with lapse. I switched to Kicad to look up the CM4 PCB to ensure but lapse didn't capture it so If you see black screen, I swear I didn't tried to inflate hours. 

Also I was wondering what should I use. A sd card or a ssd. I didn't decided yet so I left it for later did some research though

<img width="885" height="378" alt="image" src="https://github.com/user-attachments/assets/7d41ae2f-0831-42f2-9643-0633285521da" />



### Recording Links
- https://public.lapse-hackclub.link/timelapses/y2wBJvhOXfS3/timelapse-y2wBJvhOXfS3.mp4


## Entry 6
- ID: 161
- Author: Shades
- Created At: 2026-03-18T09:59:24Z

### Content

Done the power indicating LED and GPIO pullup resistor. Kind of Just made the framework how the power and storage would look like.  Also changed the 3.3V power source to external. Thinking to provide external sources but how it will work I am not sure. Have to do a lot of research then.

<img width="931" height="420" alt="image" src="https://github.com/user-attachments/assets/e8a8e4bd-0b9b-49e9-882f-f2784b2617ab" />

<img width="689" height="244" alt="image" src="https://github.com/user-attachments/assets/4d097136-5b03-4afa-b039-e74e5612654a" />


### Recording Links
- https://public.lapse-hackclub.link/timelapses/_kZoFr48UUBP/timelapse-_kZoFr48UUBP.mp4


## Entry 7
- ID: 163
- Author: Shades
- Created At: 2026-03-18T10:06:56Z

### Content

Worked and researched on Sensors and decided what to put. Also worked on 5V power management to do the powers. Later I removed the 5V power section I thought I would use usb power also and some power modules. Later that I realized that high end rov controller has power sense module. I don't have a proper idea what this is. Will probably do some more research on that.

Also I worked with Leak Sensor, eeprom, Cm4 running indicator led  and called it a day. 

I am thinking how can I work with the power. That is the main issue now

<img width="879" height="623" alt="image" src="https://github.com/user-attachments/assets/ce38f265-a34b-498b-8159-2c2bba468274" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/fIk_nT01mz3X/timelapse-fIk_nT01mz3X.mp4
- https://public.lapse-hackclub.link/timelapses/c4J8hU7nD0kO/timelapse-c4J8hU7nD0kO.mp4


## Entry 8
- ID: 483
- Author: Shades
- Created At: 2026-03-26T10:29:02Z

### Content

Routed the Second CM4 connector.

 Added a HDMI support for using it as a device later. 
I may add a eDP display instead of HDMI or a USB-C display to avoid power problems. 

<img width="914" height="491" alt="image" src="https://github.com/user-attachments/assets/320bd427-f2a1-4997-b35c-f7c92fccfc0c" />


Added leak sensor for working as a RC under water

<img width="550" height="431" alt="image" src="https://github.com/user-attachments/assets/dcadfbdd-9b3d-496d-8c3f-23579f37e6c3" />


also for testing this controller with my joystick, I added analog input options 



<img width="671" height="500" alt="image" src="https://github.com/user-attachments/assets/9b13d923-1f64-4a51-ad8b-045837a697a5" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/yoDpeuFibS_q/timelapse-yoDpeuFibS_q.mp4


## Entry 9
- ID: 485
- Author: Shades
- Created At: 2026-03-26T10:37:56Z

### Content

Made an expected PCB border and placed the board. 

I think I can fit all in pretty easily. 

Added the PWM channel as same as the Navigator one. It will be used to have ESC's signal and control some servos. 

<img width="601" height="434" alt="image" src="https://github.com/user-attachments/assets/7bbfdda5-1be4-4b37-b725-eca7d3e0c743" />


<img width="987" height="469" alt="image" src="https://github.com/user-attachments/assets/35566b53-1aa5-4b42-a7be-bc222cf19846" />


For the first time, I knew about array resistors. It is a package where multiple resistors are together to reduce the price. 

Also added SBUS to controll RC Signal if I think to fly it as a drone. It will be pretty cool. But I don't know how the Sbus system works in navigator. I will find out later.

<img width="900" height="567" alt="image" src="https://github.com/user-attachments/assets/6fb2cb25-0b5e-4a9c-85ca-f032e7ef94ec" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/mewFnlOkb6Dr/timelapse-mewFnlOkb6Dr.mp4
- https://public.lapse-hackclub.link/timelapses/pX_6vvWSdZ9X/timelapse-pX_6vvWSdZ9X.mp4


## Entry 10
- ID: 487
- Author: Shades
- Created At: 2026-03-26T10:45:36Z

### Content

Worked on Logic converter to expose some rx, tx and sda_scl output

<img width="795" height="431" alt="image" src="https://github.com/user-attachments/assets/7ff169a9-cc7d-4bc7-a28a-9b8af0b27fa8" />


Also worked on general Connectors which are pretty common for a RC controller. It is as just as navigator output.

<img width="452" height="595" alt="image" src="https://github.com/user-attachments/assets/bfdea315-9127-4c6d-b3ed-12485e3106c8" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/mcBYZct6bPip/timelapse-mcBYZct6bPip.mp4
- https://public.lapse-hackclub.link/timelapses/8xp4VZ9ti-tL/timelapse-8xp4VZ9ti-tL.mp4


## Entry 11
- ID: 488
- Author: Shades
- Created At: 2026-03-26T11:28:35Z

### Content

Added some esd protections on HDMI. 
I want to add fast storage in this device. So I was thinking of two options one is SSD so that I can plug out my main one and use it. 
Another one is emmc or sd card. lemme think letter. 

Followed some M.key routing guide online. You can add so much feature to a M.2 connector. But checking my pins I realised I don't have enough CM4 outputs to make the best version it self. 

<img width="717" height="168" alt="image" src="https://github.com/user-attachments/assets/6b71b57a-71e9-4ddf-bc13-e198b8770423" />


Also CM4 and CM5 both needs to attach an oscillator to the connector. 

And for clear 3V, we won't use normal one but step down the main 5V to 3V3. There is also a pin which is available in CM5 to control the power consumption of ssd which is not available in CM4. 


Also done the ethernet routing for network. I thought I would make the network switch with it  but that will be for later. 

<img width="741" height="504" alt="image" src="https://github.com/user-attachments/assets/a255d996-b166-4254-b3f5-49716780d3a1" />




### Recording Links

- https://public.lapse-hackclub.link/timelapses/hqIDkxEc2Te9/timelapse-hqIDkxEc2Te9.mp4

## Entry 12
- ID: 489
- Author: Shades
- Created At: 2026-03-26T11:41:03Z

### Content

Did some research about M.2 footprint and found new atrocious storage option "UFS". It is a game changer. Faster than emmc and ssd and cheaper. But Radxa has module for it. 

Either I will make it onboard or I will do nothing. I tried to figured out what they are using as chips.

<img width="428" height="340" alt="image" src="https://github.com/user-attachments/assets/a5f0feef-ab0e-4403-b656-5882d928d270" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/gnpi_oq3L_N5/timelapse-gnpi_oq3L_N5.mp4


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

<img width="377" height="472" alt="image" src="https://github.com/user-attachments/assets/6ad703ce-7ebf-4db2-81d2-19f9c18ce7b2" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/jSBw6U57ijFM/timelapse-jSBw6U57ijFM.mp4


## Entry 14
- ID: 496
- Author: Shades
- Created At: 2026-03-26T12:43:58Z

### Content

Choosing RADXA CM4 instead of PI CM4. More pins more options but less software support. 

I changed again I will use CM5 now but the CM5 schematic 
is very bad for following and don't have the UFS support that I want and I will combine those two schematics and make some changes again 

checking out the GPIO pins are compatible with me schematics or not

<img width="829" height="525" alt="image" src="https://github.com/user-attachments/assets/771cf05f-0ebf-42e9-a730-fd7aa1417f38" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/qHMCX-IUguBo/timelapse-qHMCX-IUguBo.mp4


## Entry 15
- ID: 497
- Author: Shades
- Created At: 2026-03-26T12:54:25Z

### Content

Researching about CM4 and RADXA CM5. Finding out which is better and suit my plane. Also Doing prize comparison. 

Procasinating about my plans. And started finishing my SSD and Started my Fan connector

<img width="1036" height="294" alt="image" src="https://github.com/user-attachments/assets/b4f2e77d-9fc7-48ea-9215-221e74096a79" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/XKrGPVGXKPXA/timelapse-XKrGPVGXKPXA.mp4

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

<img width="490" height="619" alt="image" src="https://github.com/user-attachments/assets/bbbf3a43-69ec-4778-9cce-3a74ae1199bd" />

<img width="689" height="328" alt="image" src="https://github.com/user-attachments/assets/6137cc26-ea2c-4469-9c65-4f1458b47b61" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/Eg3N5_EF-WU_/timelapse-Eg3N5_EF-WU_.mp4
- https://public.lapse-hackclub.link/timelapses/7FGFwqUnIvln/timelapse-7FGFwqUnIvln.mp4


## Entry 17
- ID: 590
- Author: Shades
- Created At: 2026-03-28T14:41:38Z

### Content

Just doing the USB-C display option but my current went off sadly. I am still thinking about display options

<img width="955" height="518" alt="image" src="https://github.com/user-attachments/assets/e54b746d-48c2-4525-832a-456144576b87" />

 
### Recording Links

- https://public.lapse-hackclub.link/timelapses/sf-BrG9_NJRp/timelapse-sf-BrG9_NJRp.mp4
- https://public.lapse-hackclub.link/timelapses/IUoDDzcpERWQ/timelapse-IUoDDzcpERWQ.mp4

## Entry 18
- ID: 660
- Author: Shades
- Created At: 2026-03-29T17:39:35Z

### Content

Eventually rk3588 as lot of caabilities but for me options are limited at radxa CM5.  I found friendly elec rk3588 which is lot cheaper and very much expandable. Also saw a DIMM module which serves all of purposes but lacks gpios. 

I was thinking about smart choice like when I will use it as a computer, I won't use the gpio. Same thing vice versa. Use gpio don't us computer. This way I can save pins more easily. I will research on that later.

My main concern is now that. Can the friendly elec module successfully run while taking those load at once. I don't believe it. But if it can great for me.

I don't have any good picture for this season. This is the module's pic.

<img width="720" height="822" alt="image" src="https://github.com/user-attachments/assets/3d243d48-440d-4a75-9bf7-13cb9249cf7b" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/KVwawVGVoWle/timelapse-KVwawVGVoWle.mp4

## Entry 19
- ID: 7728
- Author: Shades
- Created At: 2026-05-18T03:14:46Z

### Content

Working with the friendly Elec CM3588 Pinout. 
Matching the pinout with What I need and What is already equipped by my device. 
Most of the cases, I need a 3.3V gpio pin where there are also some 1.8V Gpio Pins. So we have to select carefully. 

<img width="783" height="669" alt="image" src="https://github.com/user-attachments/assets/e4fa7687-514f-44f9-84f9-9f4e9ae0587a" />

<img width="760" height="581" alt="image" src="https://github.com/user-attachments/assets/d6b21674-aab0-45fa-bf0a-3e9a2833c466" />

<img width="728" height="535" alt="image" src="https://github.com/user-attachments/assets/e517686c-6bf5-4ce5-b156-38498d9a08c4" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/kYiL7G6vFwHN/timelapse-kYiL7G6vFwHN.mp4

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


<img width="1068" height="651" alt="image" src="https://github.com/user-attachments/assets/269d9f5f-1943-4225-a9d8-0484a3cbcd56" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/-puKiixUWG1-/timelapse--puKiixUWG1-.mp4
- https://public.lapse-hackclub.link/timelapses/zB0LRgHoPVH5/timelapse-zB0LRgHoPVH5.mp4

## Entry 21
- ID: 9115
- Author: Shades
- Created At: 2026-05-25T14:11:43Z

### Content

Researching on the eeprom nwp of the CM4. As for now what I got is, I don't need to bring this out as a jumper cause It is my personal product not a business product and with jumper it prevents emmc to be flashed with third pirty OS. 

Claude suggested me to pull it up,. But I went through documentation of the official CM4

<img width="1585" height="808" alt="image" src="https://github.com/user-attachments/assets/8769d82e-3400-438a-9cdc-76103c51316b" />

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

  
<img width="542" height="620" alt="image" src="https://github.com/user-attachments/assets/81358b4b-ccc5-457e-83fb-97bf76c9e1d5" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/JHlyv3IIrujt/timelapse-JHlyv3IIrujt.mp4

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

<img width="591" height="598" alt="image" src="https://github.com/user-attachments/assets/eb07cb29-a25d-48fc-a4b4-d2aa010eca4a" />


Going in the accessories side of my board, I found that IIC connection is very important. But I know too little about it.  So, I have to learn the software side of it. 

I first thought of using a fan but I find it very high power 12V to be specific. Ans also using fan will create a negative pressure in the carrier. That's why I am skipping fan. Going to use only heatsink. 

Also, I spread misinformation about ethernet led power. I am very sorry for that. Since CM4's 3v3 is 180 mA is too little for providing power to anything almost. I think claude was tweaking. 

Working one the RTC. Suddenly got stuck with the crystal used in the RTC chip. Thankfully to some reddit post, I found specification for the crystal.

<img width="1599" height="812" alt="image" src="https://github.com/user-attachments/assets/4198d6c5-651f-4149-8a71-1040e2411225" />

Learnt about the watchdog feature. which is actually lit !!!

There are many things that can be done but in simple terms if anything crashes or anything wrong with the network, it forces the Global En to do hard reset. 

So, it has a pulse system where it takes a break to restart and goes back to previous state. 

I can easily use this in carrier. If anything goes wrong rather than hardware, I don't have to do nothing. I may use the windows startup lookalike feature for my program. 

<img width="983" height="252" alt="image" src="https://github.com/user-attachments/assets/783041fd-2e2b-4ebd-a5b6-7198993ad9fd" />


Now to the power, first of all I will refer to the Blue robotics Navigator power section. 


### Recording Links

- https://public.lapse-hackclub.link/timelapses/gwW8TM38hw0-/timelapse-gwW8TM38hw0-.mp4


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

<img width="1599" height="805" alt="image" src="https://github.com/user-attachments/assets/07d1ec73-3f14-41ab-bf4f-314566ce2b64" />


I told Ai to calculate its specification with 27 pf capacitor used in the official schematics. I found this one which will do the job. But according to calculation it is too over powered. 

<img width="1592" height="784" alt="image" src="https://github.com/user-attachments/assets/86470d86-4ef7-4c15-a88a-9596f40bf71d" />


But the crystal isn't correct cause it's four pin and I need 2 pin one. Atleast I found that.  

The decoupling of the 3v3 is just copy paste.

<img width="854" height="500" alt="image" src="https://github.com/user-attachments/assets/505cf9f5-398d-4e8b-91cc-08bc4ff4b57c" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/86eovrX3gII0/timelapse-86eovrX3gII0.mp4


## Entry 24
- ID: 9349
- Author: Shades
- Created At: 2026-05-26T12:36:15Z

### Content

USBhub is completed. I used USB-C for OTG. and two USB 2.0 Female Type-A for accessories to connect.  May use the other two ports for audio signal or some.

<img width="886" height="636" alt="image" src="https://github.com/user-attachments/assets/060eeda4-4258-4f41-ab1d-5009185bdc3f" />


### Recording Link

- https://public.lapse-hackclub.link/timelapses/3ci54Dbhon6r/timelapse-3ci54Dbhon6r.mp4
- https://public.lapse-hackclub.link/timelapses/YPs54McjTR9r/timelapse-YPs54McjTR9r.mp4

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
 
<img width="920" height="430" alt="image" src="https://github.com/user-attachments/assets/ad6c971f-880c-4ae5-8c64-c463055cc2a9" />

From my knowledge, I have to isolate the power section of the board cause it can heatup. GND stiching would be great for thermal.

Good thing is bluerobotics has the schematics for their power sense module which I can actually use. Implementing this right now.

So, actually I understood power sense module wrong. It is actually a observer between my power and my carrier and it gives out the information about voltage and current right through ardupilot. I did research because I don't want to implement something that I don't know about.


### Recording Links

- https://public.lapse-hackclub.link/timelapses/ZLkN0-Zi2Ta3/timelapse-ZLkN0-Zi2Ta3.mp4

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

<img width="850" height="435" alt="image" src="https://github.com/user-attachments/assets/b6117c10-f3ce-484a-9a38-e33c6d1c51c6" />

Now, I have to work on auxiliary power when I am not using battery and also and step down module like bluerobotics which can give 5V 6A. Let just hope I can get something like that even for USB type-C that works.

Got to know what is pull low and pull high is. Image is given here  for your advantage 

<img width="473" height="326" alt="image" src="https://github.com/user-attachments/assets/ed2d161f-280d-44a8-9fd1-832de3694fe3" />


I think making a step down converter is risky. I found one but cannot focus right now. After reviewing the actual rp 4 model b. It also use 5V power from the usb. So, I will consider this tomorrow.

### Recording Links

- https://public.lapse-hackclub.link/timelapses/S5h7vm4D6m8I/timelapse-S5h7vm4D6m8I.mp4

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

<img width="1599" height="811" alt="image" src="https://github.com/user-attachments/assets/d4295176-ee4a-4301-9437-3ac1f6e82ca9" />

can this happen when input voltage in high but Amps is low and step down generates high Amps. 

Yes this is possible. I don't know the core about it yet but it was knowledgeful. 

<img width="651" height="248" alt="image" src="https://github.com/user-attachments/assets/623cea04-9cb2-4cf8-a937-b22135221d05" />

Lots of research today but only less schematics.

### Recording Links

- https://public.lapse-hackclub.link/timelapses/luTjL0mK1oGT/timelapse-luTjL0mK1oGT.mp4

## Entry 28
- ID: 9720
- Author: Shades
- Created At: 2026-05-27T18:15:07Z

### Content

I finally figured out. I don't want to be stressed about power. The power will be 12V DC as mentioned in official IO board. In stead of building a power circuit, I rather change the input voltage or tweak the battery pack. 

I am still very confused about the power. Should I make the board for my own purpose or generalize it? Also making separate module aka pcb makes the carrier more safe. I mean what is the gurantee it will work 100%.  

I am still in a process of thoughts and don't know what to go ahead. Losing the motivation to work on by the way Half of the PSu in finished.

<img width="738" height="433" alt="image" src="https://github.com/user-attachments/assets/398932b9-2d62-4606-b4d5-aa1f28ce57a0" />

Also, I lot of research 

<img width="945" height="567" alt="image" src="https://github.com/user-attachments/assets/73cff5b6-5d1b-4378-bac9-31d9487e5381" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/uShCDxBMUJd3/timelapse-uShCDxBMUJd3.mp4

## Entry 29
- ID: 9922
- Author: Shades
- Created At: 2026-05-28T15:04:51Z

### Content

The end of power shit. I am tired. 

I have to make a power board. That is the solution. I don't want to mess thing up anymore.  

Middle of the power, I remembered to put ESD protection on my USB signals.

<img width="1008" height="592" alt="image" src="https://github.com/user-attachments/assets/6ae394e1-780e-4458-9a77-dfc19b5b40f8" />

Got stuck on the OTG section of the USB again which I actively skipped. The problem is caused  by the CC pins. 

Just got to know USB-C doesn't support OTG. Get fcked

<img width="522" height="265" alt="image" src="https://github.com/user-attachments/assets/bccf5653-7370-4f80-bc1a-f1c8157c26fb" />

I hate to say but I have to do micro-USB. Also I made a mistake by using a two stack usb just like the IO board. But I don't need it rather it just increases the height of my carrier.

Yeah decision final. Separate Power Board. 

3V3 section is complete. 

<img width="857" height="339" alt="image" src="https://github.com/user-attachments/assets/3f7d1d61-a243-4a1f-b96a-3f52c991e52b" />

FInally moved to PCB. 

Just before moving to PCB, another realization hit me. I didn't check my power connectors Amp ratings or voltage ratings. So, There was a good chance that my connector would burn. I have rechanged those to good shit.

<img width="1530" height="102" alt="image" src="https://github.com/user-attachments/assets/de48af8b-cd87-4054-82c7-b238672f0e93" />

Now another problem. If I stack those selected pins, those won't be together to put my wires. It has so gaps. And roaming around I couldn't decide on a high amps connector cause everything is just weird. 

I decided to use the connectors used by the BlueRobotics Navigator. Oh man! I can't just get out from the schematics. 

### Recording Links

- https://public.lapse-hackclub.link/timelapses/2S3p1Lo2aYm0/timelapse-2S3p1Lo2aYm0.mp4

## Entry 30
- ID: 10090
- Author: Shades
- Created At: 2026-05-29T09:04:18Z

### Content

I have to change and go through revision to make sure all the connector are capable of the power and current. 

Probably all set but there is a high chance I will see another problem after starting my schematics. 


<img width="409" height="601" alt="image" src="https://github.com/user-attachments/assets/9624465e-05b1-4a7a-9bba-2f399f3e6ac5" />




### Recording Links

- https://public.lapse-hackclub.link/timelapses/MH_f8xRSa6LP/timelapse-MH_f8xRSa6LP.mp4

## Entry 31
- ID: 10103
- Author: Shades
- Created At: 2026-05-29T10:32:58Z

### Content

I am such a dumb for not using the RP CM4 official schematics. But the replacement was short timed.

<img width="822" height="389" alt="image" src="https://github.com/user-attachments/assets/23375905-8636-4127-8299-6fe7ff53eab7" />

Instead of using jumper, I am thinking of using test pad and solder bridge some connections if needed.

Also, adding lots of test point in the power section. So that if anything goes wrong, I can figure that out.

Working on the PCB!!

### Recording Links

- https://public.lapse-hackclub.link/timelapses/7ZStb5mw45wI/timelapse-7ZStb5mw45wI.mp4

## Entry 32
- ID: 10157
- Author: Shades
- Created At: 2026-05-29T15:35:32Z

### Content

Starting with the power section. But first I had to manually make front silk screen small for components. 

working on the power section.

<img width="421" height="588" alt="image" src="https://github.com/user-attachments/assets/fb0fdf44-e52b-4e27-b3a7-748c1e782d77" />

Just finished the power section with CMOS. But the space feels lil tight.

<img width="504" height="409" alt="image" src="https://github.com/user-attachments/assets/f5f33339-fc8b-4cd4-b966-ea650f5e87d3" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/7jdIsT6niurT/timelapse-7jdIsT6niurT.mp4
- https://public.lapse-hackclub.link/timelapses/rzooiJ6K5jkU/timelapse-rzooiJ6K5jkU.mp4

## Entry 33
- ID: 10205
- Author: Shades
- Created At: 2026-05-29T18:09:06Z

### Content

Placing the components out in the board.  It takes so much time.

<img width="627" height="476" alt="image" src="https://github.com/user-attachments/assets/e5e35a12-158d-4fe2-97d6-989e50e06f86" />

Space is so tight but have to fit all of the connectors. I am highly thinking about changing all to male connector

### Recording Links

- https://public.lapse-hackclub.link/timelapses/TPvH-USjY2j5/timelapse-TPvH-USjY2j5.mp4

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

<img width="871" height="574" alt="image" src="https://github.com/user-attachments/assets/abed2a6f-7d5c-4547-88a6-2396cc539639" />


<img width="325" height="444" alt="image" src="https://github.com/user-attachments/assets/a2dd4a79-d89d-4354-ac34-3b5c7b3be7a8" />


Next stop is to put the power sense module.

### Recording Links

- https://public.lapse-hackclub.link/timelapses/HUCBWtYFix9t/timelapse-HUCBWtYFix9t.mp4
- https://public.lapse-hackclub.link/timelapses/OiwJzCBsVQbn/timelapse-OiwJzCBsVQbn.mp4

## Entry 35
- ID: 10601
- Author: Shades
- Created At: 2026-05-31T06:39:12Z

### Content

Power Module is complete with the power sense module. The output  is a 5V and 3V3 pad. And the input is DC power Jack. 

Also there is 8 pin Power sense connection directly to the board.

<img width="829" height="389" alt="image" src="https://github.com/user-attachments/assets/451ddf95-e7c9-45f7-a194-237f4da8b8dd" />

<img width="634" height="291" alt="image" src="https://github.com/user-attachments/assets/d5fa02ba-e22a-4cc5-acce-61d6577134a1" />

<img width="549" height="308" alt="image" src="https://github.com/user-attachments/assets/f8a30930-ad61-499b-8b56-b389a7d3c2bf" />

<img width="563" height="283" alt="image" src="https://github.com/user-attachments/assets/296a4816-3640-43f2-b14a-37251d7c009e" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/oN4TFWEil7sv/timelapse-oN4TFWEil7sv.mp4
- https://public.lapse-hackclub.link/timelapses/ZXu4JLrsx12G/timelapse-ZXu4JLrsx12G.mp4

## Entry 36
- ID: 10840
- Author: Shades
- Created At: 2026-06-01T06:24:48Z

### Content

Following up with the design guide for my Power supply board.

Working on the silkscreen of the PCB.

<img width="577" height="293" alt="image" src="https://github.com/user-attachments/assets/407a7b95-1352-4a1b-972b-c9dab4fcde46" />

<img width="836" height="602" alt="image" src="https://github.com/user-attachments/assets/6c514e2d-1d86-4ec4-b741-143e986015d0" />

<img width="728" height="472" alt="image" src="https://github.com/user-attachments/assets/da15a3f0-a6ac-4be1-b527-058f310891db" />


Finished for the power board for just now. I may change the design for better thermal efficiency.

Starting the high speed portion of my board.

<img width="458" height="606" alt="image" src="https://github.com/user-attachments/assets/4560f7f2-5be3-425e-a6cd-8bb9cc08edb8" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/KmI98mMz72Eu/timelapse-KmI98mMz72Eu.mp4

## Entry 37
- ID: 10926
- Author: Shades
- Created At: 2026-06-01T16:38:18Z

### Content

Working with high speed connections. Keeping them aside and make something out of the tight space to route my usb 

<img width="468" height="616" alt="image" src="https://github.com/user-attachments/assets/77987091-6fd7-4539-b190-2cb837ef645b" />

Removing ESD protection from HDMI. Camera and HDMI routing is complete. I am satisfied. 

Changing the ethernet connector cause it is upside down.

### Recording Links

- https://public.lapse-hackclub.link/timelapses/xFHyVZhXi8h0/timelapse-xFHyVZhXi8h0.mp4
- https://public.lapse-hackclub.link/timelapses/JNYpOZaWj2EU/timelapse-JNYpOZaWj2EU.mp4

## Entry 38
- ID: 11111
- Author: Shades
- Created At: 2026-06-02T11:30:15Z

### Content

USB routing

The usb routing was a real pain. Couldn't find a single way to match their length finally did it.

<img width="563" height="350" alt="image" src="https://github.com/user-attachments/assets/9d553fb0-ac12-4e64-80b8-21a840c1f068" />

Full usb section is complete 

<img width="528" height="441" alt="image" src="https://github.com/user-attachments/assets/708cd2dc-c385-479d-a0ec-501988bc7e68" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/KI-MojoC4JWq/timelapse-KI-MojoC4JWq.mp4

## Entry 39
- ID: 11154
- Author: Shades
- Created At: 2026-06-02T16:07:00Z

### Content

I was actually in progress with making changes with my ethernet but somehow I forgot. Today, when I was going to peer review the PDF then I noticed. Finished the unrouted esd protection on ethernet. 

Moving on to the ssd. I couldn't find the necessary outline for my ssd. I could only find the connector. Then I found a kicad file in my old folders.

Had to choose some smaller footprints for my board. 

Heading to the PCIe routing of my board. The power section is under the ssd. Hopefully it fits.

<img width="507" height="559" alt="image" src="https://github.com/user-attachments/assets/625f7521-e035-4098-8b31-0c67d019a77c" />

<img width="720" height="486" alt="image" src="https://github.com/user-attachments/assets/ff4d1cdb-abf8-4d79-be3b-c37e835144d3" />

<img width="224" height="426" alt="image" src="https://github.com/user-attachments/assets/56cd82c2-55e9-4142-a05e-c52d9b4106e9" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/hcZoLPGq7ifM/timelapse-hcZoLPGq7ifM.mp4

## Entry 40
- ID: 11326
- Author: Shades
- Created At: 2026-06-03T06:06:48Z

### Content

I am really crashing out. Cause the space is short and more connectors are here and there. I am passing a very hard time placing the components. and possibly figuring out their connections. I will take a rest and think about it.

Going to change the CM4 placement. 

<img width="665" height="500" alt="image" src="https://github.com/user-attachments/assets/24c563d0-3d14-43fa-b275-b9a48ecedefe" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/NE4n58Z3aAmA/timelapse-NE4n58Z3aAmA.mp4

## Entry 41
- ID: 11353
- Author: Shades
- Created At: 2026-06-03T10:01:06Z

### Content

High speed routing is a no joke. I am glad that I can get this result. Hope gully to soon finish my high speed routing. Then I have to move to ADC routing and section that.

<img width="788" height="507" alt="image" src="https://github.com/user-attachments/assets/c84d2569-b429-4924-9c51-55d7cded83b1" />

<img width="588" height="609" alt="image" src="https://github.com/user-attachments/assets/27953709-fd4d-4c30-a9fa-003964e7a68a" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/UuiyAvbRAL_y/timelapse-UuiyAvbRAL_y.mp4

## Entry 42
- ID: 11562
- Author: Shades
- Created At: 2026-06-04T08:20:08Z

### Content

Not much progress done. Finished off the High speed connectors IO port. Things are so messy, I can't get my mind on organizing it. 

<img width="444" height="508" alt="image" src="https://github.com/user-attachments/assets/de125310-0b3d-4c08-aff8-9a385fdcb1ff" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/oDL25D9EjMVE/timelapse-oDL25D9EjMVE.mp4
- https://public.lapse-hackclub.link/timelapses/yPMtM23YNdvk/timelapse-yPMtM23YNdvk.mp4

## Entry 43
- ID: 12944
- Author: Shades
- Created At: 2026-06-10T05:37:24Z

### Content

Just doing the IO routing and planning out the component placement. There is not much to explain rather than following up with routing process 

<img width="427" height="521" alt="image" src="https://github.com/user-attachments/assets/eeded49c-b44f-423f-bd6b-467b57a0601d" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/E4Y8ywEs9I4C/timelapse-E4Y8ywEs9I4C.mp4
- https://public.lapse-hackclub.link/timelapses/r4t2UuJQr76t/timelapse-r4t2UuJQr76t.mp4
- https://public.lapse-hackclub.link/timelapses/7H4ZOTzHdCOu/timelapse-7H4ZOTzHdCOu.mp4

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

<img width="525" height="556" alt="image" src="https://github.com/user-attachments/assets/88f5a4ad-a06e-4217-b285-f0bbfd0bbb5e" />


## Entry 45
- ID: 12992
- Author: Shades
- Created At: 2026-06-10T11:20:16Z

### Content

Removed the SSD and related power converters and working on the USB 3.0. U can actually get two usb 3.0 but current I don't need one. I am quite happy with one. Challenge is I have to tight fit it in the PCB.

<img width="486" height="504" alt="image" src="https://github.com/user-attachments/assets/af2182ce-ea0f-47ac-b15d-ff38c651f9da" />


### Recording Links

- https://lookout.hackclub.com/api/media/2c1a91ac-6a7a-4bf0-a090-aabfe188b551/video.mp4

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

  
<img width="611" height="633" alt="image" src="https://github.com/user-attachments/assets/76d4959d-f1ef-4638-b795-7d265c16bc8d" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/vSmwTnL_YXma/timelapse-vSmwTnL_YXma.mp4
- https://public.lapse-hackclub.link/timelapses/S8tbRpwZK-Cn/timelapse-S8tbRpwZK-Cn.mp4
- https://public.lapse-hackclub.link/timelapses/GuwFw5TXZ-ar/timelapse-GuwFw5TXZ-ar.mp4
- https://public.lapse-hackclub.link/timelapses/CGL0jWhBYsFE/timelapse-CGL0jWhBYsFE.mp4
- https://public.lapse-hackclub.link/timelapses/x00t-o2Sn_z3/timelapse-x00t-o2Sn_z3.mp4
- https://public.lapse-hackclub.link/timelapses/LqbKJ7__wGMF/timelapse-LqbKJ7__wGMF.mp4
- https://public.lapse-hackclub.link/timelapses/xeDYPC0AHXOI/timelapse-xeDYPC0AHXOI.mp4
- https://public.lapse-hackclub.link/timelapses/St1CwfxtTgNG/timelapse-St1CwfxtTgNG.mp4
- https://public.lapse-hackclub.link/timelapses/3tVIc7URmjrK/timelapse-3tVIc7URmjrK.mp4
- https://public.lapse-hackclub.link/timelapses/5xQssbtwQ4RQ/timelapse-5xQssbtwQ4RQ.mp4
- https://public.lapse-hackclub.link/timelapses/LDHQCrifa2-R/timelapse-LDHQCrifa2-R.mp4
- https://public.lapse-hackclub.link/timelapses/3CtyMrdTanRs/timelapse-3CtyMrdTanRs.mp4
- https://public.lapse-hackclub.link/timelapses/e8dkkCTp07Fd/timelapse-e8dkkCTp07Fd.mp4
- https://public.lapse-hackclub.link/timelapses/fQOuqm7ZlzR8/timelapse-fQOuqm7ZlzR8.mp4
- https://public.lapse-hackclub.link/timelapses/zIYhuz_87PA-/timelapse-zIYhuz_87PA-.mp4
- https://public.lapse-hackclub.link/timelapses/PDXCKILAGlf9/timelapse-PDXCKILAGlf9.mp4
- https://public.lapse-hackclub.link/timelapses/McYnFkFyqyul/timelapse-McYnFkFyqyul.mp4
- https://public.lapse-hackclub.link/timelapses/8b67HE7RBuXo/timelapse-8b67HE7RBuXo.mp4
- https://public.lapse-hackclub.link/timelapses/QwaJrjT8a9aK/timelapse-QwaJrjT8a9aK.mp4
- https://public.lapse-hackclub.link/timelapses/lBoWhs_5wVic/timelapse-lBoWhs_5wVic.mp4
- https://public.lapse-hackclub.link/timelapses/SDH7BYEjrn6f/timelapse-SDH7BYEjrn6f.mp4
- https://public.lapse-hackclub.link/timelapses/_-a0Pqh6-J0l/timelapse-_-a0Pqh6-J0l.mp4
- https://public.lapse-hackclub.link/timelapses/iJWLLDgzCElu/timelapse-iJWLLDgzCElu.mp4
- https://public.lapse-hackclub.link/timelapses/U5Ys-5A3Rxf2/timelapse-U5Ys-5A3Rxf2.mp4
- https://public.lapse-hackclub.link/timelapses/SFGooDfMDDP2/timelapse-SFGooDfMDDP2.mp4
- https://public.lapse-hackclub.link/timelapses/CIi1-UWWxcHr/timelapse-CIi1-UWWxcHr.mp4
- https://public.lapse-hackclub.link/timelapses/5w5d8yv57MfK/timelapse-5w5d8yv57MfK.mp4
- https://public.lapse-hackclub.link/timelapses/Ic2JTFEJTBZt/timelapse-Ic2JTFEJTBZt.mp4
- https://public.lapse-hackclub.link/timelapses/2CnwNKSWQaTL/timelapse-2CnwNKSWQaTL.mp4
- https://lookout.hackclub.com/api/media/fe1f186e-2a19-4837-9cff-e76c0c27f299/video.mp4
- https://lookout.hackclub.com/api/media/56543d2a-21f5-4683-b311-056076d6c296/video.mp4

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

<img width="443" height="550" alt="image" src="https://github.com/user-attachments/assets/1bdf230b-8840-44c0-b83d-a36474d7eeb0" />


### Recording Links

- https://public.lapse-hackclub.link/timelapses/_HKmpHNiDtY7/timelapse-_HKmpHNiDtY7.mp4
- https://public.lapse-hackclub.link/timelapses/lASp2E_Zi5JA/timelapse-lASp2E_Zi5JA.mp4
- https://public.lapse-hackclub.link/timelapses/NwuMD-jS2X-m/timelapse-NwuMD-jS2X-m.mp4
- https://public.lapse-hackclub.link/timelapses/KwSBTq0YiLcj/timelapse-KwSBTq0YiLcj.mp4

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



<img width="619" height="517" alt="image" src="https://github.com/user-attachments/assets/656fce4f-f079-4a0c-bc31-531fdacd9c31" />

<img width="310" height="594" alt="image" src="https://github.com/user-attachments/assets/4509de2c-b44c-4ea6-9227-634d44a2fced" />



### Recording Links

- https://public.lapse-hackclub.link/timelapses/PqPItKbqLqq0/timelapse-PqPItKbqLqq0.mp4
- https://public.lapse-hackclub.link/timelapses/LxCBi2WoIM6P/timelapse-LxCBi2WoIM6P.mp4
- https://public.lapse-hackclub.link/timelapses/-dvHzAuRnAqH/timelapse--dvHzAuRnAqH.mp4
- https://public.lapse-hackclub.link/timelapses/My3rDsXS32y6/timelapse-My3rDsXS32y6.mp4
- https://public.lapse-hackclub.link/timelapses/DS9mbE6mK-QV/timelapse-DS9mbE6mK-QV.mp4
- https://public.lapse-hackclub.link/timelapses/p3LbimLtYvdT/timelapse-p3LbimLtYvdT.mp4
- https://public.lapse-hackclub.link/timelapses/r0l7DCXZQjhu/timelapse-r0l7DCXZQjhu.mp4
- https://public.lapse-hackclub.link/timelapses/ORh_R7Ul0bTR/timelapse-ORh_R7Ul0bTR.mp4
- https://public.lapse-hackclub.link/timelapses/rjyTsBQeRHGB/timelapse-rjyTsBQeRHGB.mp4
- https://public.lapse-hackclub.link/timelapses/HQn67IJpK4ai/timelapse-HQn67IJpK4ai.mp4
- https://public.lapse-hackclub.link/timelapses/aLCTMyf2e9O7/timelapse-aLCTMyf2e9O7.mp4
- https://public.lapse-hackclub.link/timelapses/mOOJ1YLa_nUb/timelapse-mOOJ1YLa_nUb.mp4


## Entry 49
- ID: 16214
- Author: Shades
- Created At: 2026-06-25T16:07:08Z

### Content

Moving all the GPIO and leds to one side. 

But shit How I removed all the GND Vias. I need to redo everything. I hate me .

<img width="720" height="696" alt="image" src="https://github.com/user-attachments/assets/fcbdd8af-8c88-4ad2-b043-e69e46b3e924" />


### Recording Links

- https://lookout.hackclub.com/api/media/ec513996-57b3-438f-be47-2b7e5f6c63c1/video.mp4
- https://lookout.hackclub.com/api/media/9d133300-d06e-4b1e-96fb-93e7ab270f24/video.mp4
- https://lookout.hackclub.com/api/media/1e66f787-22ad-4cd1-9a3d-71047f4a0720/video.mp4
- https://lookout.hackclub.com/api/media/8e13eab7-2cca-4941-a744-7779871e3edc/video.mp4
- https://lookout.hackclub.com/api/media/77eb1f32-a2b6-43c5-b46b-b7ebf807830c/video.mp4
- https://lookout.hackclub.com/api/media/eed234d3-5ca6-4eed-a69d-716427dc02f0/video.mp4
- https://lookout.hackclub.com/api/media/e3046363-fbc6-4c14-bd42-a93c004db32b/video.mp4
- https://lookout.hackclub.com/api/media/b049b273-ffd1-42e1-9c82-ab7a1c9ccc62/video.mp4
- https://public.lapse-hackclub.link/timelapses/c98tMR373Jar/timelapse-c98tMR373Jar.mp4
- https://public.lapse-hackclub.link/timelapses/_0YDM4YhgTvH/timelapse-_0YDM4YhgTvH.mp4
- https://public.lapse-hackclub.link/timelapses/cnXgSQfi-q-F/timelapse-cnXgSQfi-q-F.mp4

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

<img width="545" height="462" alt="image" src="https://github.com/user-attachments/assets/d47724d4-d1ab-4dc2-8dae-822b21d21c6a" />

<img width="331" height="478" alt="image" src="https://github.com/user-attachments/assets/6296db4f-ecea-4c92-9bd5-0e80428a5339" />


### Recording Links

- https://lookout.hackclub.com/api/media/919b24c2-1310-4ce9-9f7f-a03a00ceb50a/video.mp4
- https://lookout.hackclub.com/api/media/0f8cf35e-fd64-482c-a812-100707313888/video.mp4
- https://lookout.hackclub.com/api/media/ffa32473-c254-43bb-8d67-2b350449d706/video.mp4
- https://lookout.hackclub.com/api/media/72316c91-048b-4979-8507-9f8ee7449f44/video.mp4
- https://lookout.hackclub.com/api/media/970f241f-6b59-44b2-9371-fba0e0170114/video.mp4
- https://lookout.hackclub.com/api/media/006cb4ff-b1d5-4fc2-bc91-360ae99db945/video.mp4
- https://lookout.hackclub.com/api/media/97a3382a-ffed-4182-b29e-38c852ffc8c8/video.mp4
- https://lookout.hackclub.com/api/media/c30c4aa5-18e1-4c1e-b72a-fbc0730019f8/video.mp4
- https://lookout.hackclub.com/api/media/124d0300-1e26-49fc-9871-4528e30fdfd9/video.mp4
- https://lookout.hackclub.com/api/media/dfc76c7a-68dd-4240-acd4-817483653b6d/video.mp4
- https://lookout.hackclub.com/api/media/f3392da6-7e42-48c7-ab44-5e22363e57a2/video.mp4
- https://lookout.hackclub.com/api/media/573b6577-cdac-47a8-a411-7133731cb946/video.mp4
- https://lookout.hackclub.com/api/media/3308dbbb-31b3-4ddb-b380-9fcc91ab5b66/video.mp4
- https://public.lapse-hackclub.link/timelapses/0r_-icWn1W-z/timelapse-0r_-icWn1W-z.mp4
- https://lookout.hackclub.com/api/media/e65090e3-cf84-4d83-a8d1-8c2c5a8aea7d/video.mp4
- https://lookout.hackclub.com/api/media/26cb331e-67f0-4337-a569-6a668db1acb4/video.mp4

## Entry 51
- ID: 16461
- Author: Shades
- Created At: 2026-07-05T18:30:05Z

### Content

Finished up routing the Sensors and cleaning my routes. 

Cleared a whole backlog of DRC error. 

And working on the Silkscreen of my PCB and exposing testpads in the back

<img width="694" height="709" alt="image" src="https://github.com/user-attachments/assets/7fb48b19-874d-42f5-8eb1-3020cb71f536" />


<img width="482" height="508" alt="image" src="https://github.com/user-attachments/assets/3a6b2b1d-e708-4dba-a566-a535ee44c9a5" />



### Recording Links

- https://lookout.hackclub.com/api/media/135929fd-61d1-4400-8da8-5f9e30b15752/video.mp4
- https://lookout.hackclub.com/api/media/e80d6c00-f698-4f11-b1a8-265fbc6a25ff/video.mp4
- https://lookout.hackclub.com/api/media/a0cd3284-d6b0-4352-819b-1fe6abf4a1e2/video.mp4
- https://lookout.hackclub.com/api/media/4e4fa132-074b-4fff-9f16-e0c12fde303e/video.mp4
- https://lookout.hackclub.com/api/media/e3d602a2-6856-4d39-99ab-0197a0526803/video.mp4
- https://lookout.hackclub.com/api/media/c36edae7-6334-4a3c-bef3-547eb3b060da/video.mp4
- https://lookout.hackclub.com/api/media/3e7842ac-f375-4205-ba9a-43b27eeccf95/video.mp4
- https://lookout.hackclub.com/api/media/9b987326-e8c0-41ed-b52b-13afd7282191/video.mp4

## Entry 52
- ID: 16477
- Author: Shades
- Created At: 2026-07-07T03:34:36Z

### Content

Pretty Much Finished the Silkscreen of the PCB. Now it is the time for Power Sensing and Stuff. 

I quite a while ago removed the ADC IC from my carrier which was used in Navigator. But I realise I need that again cause I got 2 ILM pins from my E-Fuse.  ILM is current monitor output.  Which is ADC channel now I have to convert it to I2C so that I can put that in same I2C bus as Compass and Pressure Sensor

Also, I have to make place for my 12V powers sensing tooo. 

 Also, I did not realise that I have to length match the SPI connection in 50 ohms. So that was a cool trade off.


<img width="654" height="714" alt="image" src="https://github.com/user-attachments/assets/d2318e4e-55ea-415e-92b0-6359d9772263" />

<img width="703" height="650" alt="image" src="https://github.com/user-attachments/assets/d1589c79-5a71-4987-814a-2027cd819ff3" />


### Recording Links

- https://lookout.hackclub.com/api/media/a09e24bc-9a2b-4f71-bcf6-c9cbdc0bed70/video.mp4
- https://lookout.hackclub.com/api/media/a7bd70e8-b17b-4610-91c7-ecbf806630ed/video.mp4
- https://lookout.hackclub.com/api/media/3053cd3e-2ff8-467f-9ff7-66909c5620b2/video.mp4
- https://lookout.hackclub.com/api/media/da761f67-9e4c-44d0-9e35-43ba4ee9ddc7/video.mp4
- https://lookout.hackclub.com/api/media/166f364e-96e1-4b53-9737-ba12d337da92/video.mp4
- https://lookout.hackclub.com/api/media/e0369f84-d4a9-45d9-be72-e8661e6b4636/video.mp4

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

<img width="633" height="433" alt="image" src="https://github.com/user-attachments/assets/ea238dc3-adb5-43d8-ab36-a20794a4f459" />

<img width="643" height="622" alt="image" src="https://github.com/user-attachments/assets/81367800-10bc-4675-afc4-5c311881d172" />

<img width="601" height="605" alt="image" src="https://github.com/user-attachments/assets/853ddfe8-befc-4ed0-b607-2c5b291d44f3" />

<img width="1004" height="786" alt="image" src="https://github.com/user-attachments/assets/36c22f95-fe29-4cc8-9784-40698ccb6420" />

<img width="1056" height="787" alt="image" src="https://github.com/user-attachments/assets/fc05626e-42a8-4b52-9339-dddff7bedc91" />

<img width="672" height="556" alt="image" src="https://github.com/user-attachments/assets/494a6f75-2054-461f-9ce7-e4346bdb25d5" />

<img width="675" height="548" alt="image" src="https://github.com/user-attachments/assets/6440f8da-7b7f-4d67-b714-8a2da5402628" />



### Recording Links

- https://lookout.hackclub.com/api/media/aba2d06b-ec74-4040-8b1e-6d30a04420eb/video.mp4
- https://lookout.hackclub.com/api/media/cb4dee71-96c1-47e8-916f-ae4a861b3833/video.mp4
- https://lookout.hackclub.com/api/media/9a8e5d79-dfdd-4887-80e8-a0ff6f400296/video.mp4
- https://lookout.hackclub.com/api/media/52cff286-0f9b-4282-bfc2-5720e4c7e003/video.mp4
- https://lookout.hackclub.com/api/media/8bb4ecc5-a284-4476-8ed9-d853513e55b1/video.mp4
- https://lookout.hackclub.com/api/media/0b723606-5750-4f8a-986e-4b6bc04f3552/video.mp4
- https://lookout.hackclub.com/api/media/57f0ecae-70a4-4b41-8e13-25307f6b6b5a/video.mp4

## Entry 54
- ID: 16566
- Author: Shades
- Created At: 2026-07-12T05:12:03Z

### Content

After finishing the project, Uploaded everything in Github and now organizing everything to make it more presentable.

Fixing the image directory. Formatting the Journal.md with proper images and lapse link

![image.png](/user-attachments/blobs/redirect/eyJfcmFpbHMiOnsiZGF0YSI6NDExMTUsInB1ciI6ImJsb2JfaWQifX0=--af2e51faa9176e1354459b3b4ece149290356598/image.png)


### Recording Links

- https://lookout.hackclub.com/api/media/9e709473-7581-4ba7-9bbc-07ddc67b2434/video.mp4
- https://lookout.hackclub.com/api/media/638c31c7-f127-4a77-8180-7d546b28ab05/video.mp4
- https://lookout.hackclub.com/api/media/7694657e-4166-4c85-b47d-d3f8e2ad0104/video.mp4
- https://lookout.hackclub.com/api/media/f5c6f721-2499-4ecb-a8c7-bc3afb4e7759/video.mp4




# Note for the Reviewers - (Should be deleted after approval)

I used Lapse for all of my recordings. But in the middle when lapse was unstable, I used lookout. I will be very happy if that session also counts toward the project. Even though now lapse uses lookout.

Entry 45 and 46 
- [45](https://lookout.hackclub.com/api/media/2c1a91ac-6a7a-4bf0-a090-aabfe188b551/video.mp4)  - 1 hours and 9 minute 
- [46](https://lookout.hackclub.com/api/media/56543d2a-21f5-4683-b311-056076d6c296/video.mp4) - 16 minutes

