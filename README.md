# MX-9916 Night Vision Platform

Teardown and Documentation on MX-9916/MX-9648 image intensifier tube used in PVS-5 night vision systems and space shuttle experiments camera.

Have you ever wondered how night vision goggles work? Did you know that if you've ever used night vision devices, you were probably exposing your eyes to 15,000 volts? In this walkthrough of the MX-9916/MX-9648 image intensifier tube made by Galileo Electro-Optics, Inc., I will show you the uses of this type of image intensifier tube and how it converts photons into electricity and then back into light.

![](https://github.com/ComputerFish/MX-9916/assets/52689119/c2b6c8c6-1255-47ab-9fef-63892523c5e0)
![](https://github.com/ComputerFish/MX-9916/assets/52689119/a1bc5a5e-af69-4193-9b55-6be7498fab28)
###### *AN/PVS-5B (Army/Navy Portable Visual Search - 5B)*

# So, how does night vision work?

There are three primary forms of night vision:
1. Image intensification
2. Active illumination
3. Thermal imaging
  
The most common type available to consumers is active illumination, which is commonly referred to as digital night vision. Digital night vision uses a digital camera with no infrared light filter across the sensor. This means that an area can be illuminated with infrared LEDs, and only the camera will be able to see this. This approach is how most security cameras and even Apple's Face ID works (sort of)!

The second most common type of night vision is image intensification (most common in military and scientific applications). This is sometimes referred to as "true" night vision and is characterized by the classic green-eyed devices seen in movies. This type is considerably more complex but offers advantages such as extended view distance, power savings, and enhanced reliability. Image intensification devices are extensively used in military applications and scientific instruments that require imaging capabilities in low-light conditions. For the purpose of this discussion, we will focus solely on this type.

There is also thermal imaging, which operates based on the detection of infrared radiation emitted by objects and living beings. Unlike image intensification or active illumination, thermal imaging does not rely on visible light. Instead, it captures the heat signatures emitted by objects and converts them into a visible image.

PVS-5C cross section displaying internals |  Electron Multiplication 
:-------------------------:|:-------------------------:
![](https://github.com/ComputerFish/MX-9916/assets/52689119/1664f68c-7bd2-4bcb-87c8-a1f0a7860ce1)  |  ![](https://github.com/ComputerFish/MX-9916/assets/52689119/d2b7d9bb-88fa-4f91-a0da-a19299386c5c)

Night vision devices based on image intensification technology, like the MX-9916/MX-9648 tube, work by amplifying available light to enhance visibility in low-light conditions. The tube consists of several key components, including a photocathode, microchannel plate (MCP), and phosphor screen.

The photocathode is the first component that receives incoming light. It absorbs photons and emits electrons as a result of the photoelectric effect. These electrons are then accelerated towards the MCP, which is a thin plate with millions of microscopic channels. Each channel acts as an electron multiplier, amplifying the electron signal as it passes through.

Once the electrons have passed through the MCP, they strike a phosphor screen at the end of the intensifier tube. The phosphor screen converts the amplified electron signal back into visible light, creating a brightened and intensified image that can be observed through an eyepiece or displayed on a screen.

By utilizing this process of converting photons into electricity and then back into light, night vision devices allow users to see in conditions where natural light is limited or absent.


# Surely, this uses a lot of power?

Well, surprisingly, even night vision units from the 1970s could operate on 3 volts! That's only two AA batteries (although they used non-standard-shaped batteries).

This power configuration (one of many) could last a few days of intermittent use. The MX-9916/MX-9648 image intensifier tube is considered GEN 2 technology. This means it is quite old now, and modern GEN 4 technology surpasses it in many ways this does not mean it is useless!

However, due to its age, many units have dead power supplies, and finding replacements for the MX-9916 is not possible. So, I decided to disassemble mine and examine the inner workings.

# What is the MX-9916 made by Galileo Electro-Optics, Inc.?
![](https://i.imgur.com/jNUwAyu.jpg)
This particular image intensifier tube is made by a company caleld Galileo Electro-Optics, Inc. This *type* of tube was primarily used in night vision goggles as explained above but those were all produced by ITT Industries and Littion Industries for the PVS-5 (and others). The tube I have was made to the MX-9916 spec but instead by Galileo for NASA during the space shuttle program in the 1970s.

NASA's Final Report|  Nikon F 35mm with Galileo tube fitted
:-------------------------:|:-------------------------:
![](https://github.com/ComputerFish/MX-9916/assets/52689119/756742d9-5366-44de-941a-e6ef86771331)  |  ![](https://github.com/ComputerFish/MX-9916/assets/52689119/57497614-a740-4d1f-9569-87f1c2b8b699)

My tube came with a broken power supply that when powered from a 3 volt source just had a tiny amount of arcing visable. so I had to take on the task of de-potting, this device internally uses a few thousand volts to power the different components and when voltage is that high the electricity has a tendency to want to jump the gap and find the nearest path to ground(which could be me if I am holding it, don't ask me how I know it hurts). Due to the nature of such high voltage the whole tube is encased in a thick dielectric silicone known as potting and coveres anything from being visable, I had to pick this all off very carefully with a pair of tweezers if I wanted to inspec the voltage multiplier.

Note: Such high voltage is dangerous but at only 0.035 milliamperes this not deadly, it still hurts and high voltge arcs emit X-Rays so caution was needed.

So how does 3 volts get turned into 15,000 volts? it all happens inside the PSU specifically the section that contains the capacitor array, this portion is so high voltage the silicone won't cut it so its encased in resin to prevent arcing and this all has to melted/picked away to show any components. 

