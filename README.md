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
This particular image intensifier tube, known as the MX-9916, was manufactured by Galileo Electro-Optics, Inc. This specific type of tube was primarily used in night vision goggles, as explained above, but those were predominantly produced by ITT Industries and Litton Industries for the PVS-5 and other models. However, the tube I have is a special version made to the MX-9916 specifications by Galileo for NASA during the space shuttle program in the 1970s.


NASA's Final Report|  Nikon F 35mm with Galileo tube fitted
:-------------------------:|:-------------------------:
![](https://github.com/ComputerFish/MX-9916/assets/52689119/756742d9-5366-44de-941a-e6ef86771331)  |  ![](https://github.com/ComputerFish/MX-9916/assets/52689119/57497614-a740-4d1f-9569-87f1c2b8b699)

My tube came with a broken power supply. When powered from a 3-volt source, there was a small amount of visible arcing. Therefore, I had to undertake the task of de-potting the device. Internally, this device utilizes a few thousand volts to power its different components. When the voltage is that high, electricity tends to seek the path of least resistance, potentially leading to a ground connection (which, if I am holding it, can be quite painful—I'd rather not explain how I know).

Due to the high voltage involved, the entire tube is encased in a thick layer of dielectric silicone known as potting. This potting material covers everything, making it impossible to see the internal components. To inspect the voltage multiplier, I had to very carefully remove the potting material using a pair of tweezers.

Note: While such high voltage can be dangerous, at only 0.035 milliamperes, it is not deadly. However, it can still cause discomfort, and it's important to be cautious. Additionally, high-voltage arcs emit X-rays, further emphasizing the need for caution in handling the device.

So, how does 3 volts get transformed into 15,000 volts? This transformation occurs inside the power supply unit (PSU), specifically within the section that houses the capacitor array. This part operates at such a high voltage that silicone insulation alone won't cut it. Therefore, it is encased in resin to prevent arcing. To reveal the underlying components, the resin had to be melted and carefully removed.

In the capacitor array, each capacitor's output is connected to the input of the next one, resulting in a cascading effect. Through this cascading arrangement, the voltage gradually increases until it reaches approximately 15,000 volts!
DC-To-AC Transformers (white ceramic squares)|  Capacitor Arrays In Series(black bars)
:-------------------------:|:-------------------------:
![](https://github.com/ComputerFish/MX-9916-Night-Vision/assets/52689119/dddd5784-b9ad-4527-9234-9cd9eec1914c)  |  ![](https://github.com/ComputerFish/MX-9916-Night-Vision/assets/52689119/35ae8f9f-cc5d-4f7e-9cba-ed5873fbb447)

Taking apart a device like this can be extremely hazardous if proper precautions are not taken into account. Many of the components present in the device, such as leaded solder, toxic potting compounds, and toxic photo-luminous phosphorus, are known to be carcinogenic and toxic.

It is important to note that disassembling the device beyond this point is not recommended so that is where I will stop. The image tube is vacuum-sealed and contains highly toxic powders and delicate components like the Micro Channel Plate and phosphorus screen. However, it is worth mentioning that the ocular lens does feature an intriguing fiber optic lens!

Image Intensifier in PVS-5B Housing|  Power Supply Disassembled
:-------------------------:|:-------------------------:
![](https://github.com/ComputerFish/MX-9916-Night-Vision/assets/52689119/fedc2d23-96e7-461a-a54b-4dcdb53b68fe)  |  ![](https://github.com/ComputerFish/MX-9916-Night-Vision/assets/52689119/46ba9d97-69f3-4d12-a121-e84284a7511b)

This has been a concise introduction to the MX-9916 and a disassembly of my personal unit. It is important to note that there is a vast amount of information and numerous technical details that have not been covered in this brief overview. These omissions were made to keep the discussion from becoming excessively lengthy.

For those interested in delving deeper, including access to schematics and technical diagrams from NASA, I recommend reviewing the other files in this repository.
