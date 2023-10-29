# EDiPOP

![184566707_2064185513723466_4226522359891638157_n (1)](https://github.com/Popov77/EDiPOP/assets/59052047/8b256e4f-fe04-46b0-a9ae-b84b460ad3ec)  


# Introduction

EDiPOP is a user-friendly OBD module which connects through WiFi to a mobile smart device. 
A set of various live engine data fetched from the ECU/TCU/Sensors is presented in the browser. The data assists in monitoring engine health and performance capacity. 

Start you engine and you're ready to log and display data in the matter of seconds.  

• OBD dongle format, easy to install. No need for permanent installation and wiring  
• 2-5 times faster refresh rate compared to other similar market leading tools   
• Multiple pre-defined screens with essential live engine/transmission data values   
• Compatible with external flex fuel sensor, displaying ethanol content and temperature  
• Capable of measuring acceleration times, 0-100, 100-200   
• ECU/TCU diagnostic trouble code monitoring  
• Graph view for enhanced logging capability and sharing  
• Free updates  

**Preconditions**  
• 2.4GHz Wi-Fi Hotspot mobile smart device sharing compatibility  
• Google Chrome or Safari web browser, other browsers might work   
• Ethernet access  

**Compatibility**   
• Simos 18.1  
• Simos12   
• MED17.1.62  
• MG1CS163  

**EDiPOP versions**   

EDiPOP comes in two versions, v1 and v2. The primary distinction between them is that v2 is equipped with an SD card reader/writer and a buzzer. With v2, you have the capability to save logs, which can be easily shared via email for more in-depth analysis and study.  
V1 has been discontinued but remains supported.

**Disclaimer, EDiPOP cannot be the cause of technical issues and will not be liable for any damages when used incorrectly!**  
  
# Interface

**Screens views**  
• TEMP - engine temperatures  
• TIMING - cylinder timing pull  
• BOOST - boost, wg control, oil pressure   
• FUELING - injection, lambda and pressure  
• KNOCK - knock voltage  
• MISFIRES - misfire count  
• MULTI - lambda, ignition, boost and max timing pull    
• TURBO - ignition, boost and external EGT/EMAP sensor measurements   
• TCU - transmission pressure, temperature and launch count  
• TIMES - acceleration measurements  
• BLEND - external ethanol sensor measurement and fuel trims. Including a blend ratio calculator 

![Untitled](https://github.com/Popov77/EDiPOP/assets/59052047/2f81678f-2400-4933-82f6-b58b6420b510)  

**Hz**  
Hz = how many times all parameters are refreshed per second.  
The Hz indicator shows the speed of the can bus data and sensors shown in the screen view. It will be different between screen views as the ECU/TCU has different response time depending on the parameters requested. The ECU/TCU model also has a large impact on the read out speed of parameters.  
The update frequencey of the Hz indicator itself has intentionally been slowed down to avoid high speed flickering, making it easier to read.   

Following indicators can be displayed by the Hz counter.  
**-** , Engine not running   
**=** , Running engine  
**e1** , Communication loss  

Reconnect EDiPOP and check your mobile smart device connections if you get the **e1** indication.     

**DTC indication**  
EDiPOP checks if any ECU/TCU DTC's are present when shifting in-between screen views. E represents ECU, T represents TCU  
**-** , No diagnostic trouble codes present    
**D** , One or multiple diagnostic trouble codes present   
**M** , Indicates there is no TCU available, likely a manual transmission.  

# Connect  
Your mobile smart device must be 2.4GHz Wi-Fi Hotspot compatible. New android and apple smart devices require data coverage to allow hotspot sharing. 
Follow these steps to connect EDiPOP upon your initial set up.  
1. Activate your hotspot sharing  
2. Set to 2.4GHz broadband  
3. Change your SSID name to **Hotspot** and password to **abcd1234**  
4. Connect EDiPOP to the OBD connector    
5. Identify the IP address of EDIPOP in the listed hotspot connections  
6. Start your browser and enter your IP number, example: **192.168.34.188/0**  

EDiPOP should auto connect next time you go for a ride if the above settings have not changed.  

Some smart devices will not present you the option of listing connected hotspots. Download a separate network analyzer app to assist in finding the IP address of EDiPOP. The Network Scanner app has been tested and proven to work.  

![276194466-dca41941-f04b-4a7f-948a-e340f1bdcd5d_55](https://github.com/Popov77/EDiPOP/assets/59052047/c7e40149-c2b3-400e-ae35-e3be905245d8)

# Logging  

Logging is physically only possible on the EDiPOP v2 as it requires a micro SD card.   
Select a micro SD card with a 100MB/s writing speed or higher to prevent slowing down the refresh rates.  

![276218277-2aad8026-5a92-4c3c-9a14-33f1b314b8f0_22](https://github.com/Popov77/EDiPOP/assets/59052047/07134e18-1d38-4ee0-84d9-e394301422ff)

Before proceeding, make sure you format your micro SD card as FAT32. Use a software tool like SD Card Formatter to complete the formatting.  
Available for download: https://www.sdcardformatter.com/  

![Captureykyu](https://github.com/Popov77/EDiPOP/assets/59052047/e285fadd-0f1c-4a57-81fa-1660abf78757)

# Updates  
You can update EDiPOP in two ways, over the air (OTA) or via an micro SD card.    

Micro SD card updates are only available for EDiPOP v2 users as EDiPOP lacks a SD card reader/writer. Using a micro SD card enables you to update the EDiPOP firmware, you'll require a **.bin** file for this process. Remove all pre-existing files from the micro SD card, leaving only the update firmware **.bin** file. This step will help EDiPOP identify the firmware upload file.

![Screenshot_20231027_225125_Chrome (1)](https://github.com/Popov77/EDiPOP/assets/59052047/e7e92863-f3a0-41c9-a8bc-a4ef743ae80a)

OTA updates are used to update both the EDiPOP firmware and filesystem. ElegantOTA is an external service, acessed from the menu system of EDiPOP. On some occasions, the automatic forwarding to ElegantOTA may fail. In such cases, you can force it by appending **/update** to your IP address.

![Screenshot_20231027_225207_Chrome (1)_55](https://github.com/Popov77/EDiPOP/assets/59052047/a6914ca2-0399-40fb-84a5-c0e86e1eebd6)

To perform an OTA update, you'll need two files: **.bin** and **.spiffs** . Updating the filesystem is not always necessary, typically only the firmware requires an update. The release notes will inform you whether both the firmware and filesystem need to be updated.  
 
The necessary files, along with release notes, are published whenever new updates are released.  
**Caution when updating EDiPOP, a mishappening can brick EDiPOP and require you to send it back!**   

# Connections  
EDiPOP pin out enables for external connections, specific details found below. 
Connecting and wiring pins require electrical skills, EDiPOP can be damaged if you are not careful.  

**2** , Ethanol sensor for read out of fuel blend ratio        
**3** , 3.3V/40mA digital output signal   
**7** , 3.3V analog input signal  
**9** , 3.3V analog input signal     
**10** , MiPOP communication pin, see chapter MiPOP for further details    
**11** , MiPOP communication pin, see chapter MiPOP for further details    

![EDiPOP pin_out v2_25](https://github.com/Popov77/EDiPOP/assets/59052047/1e82b2fd-891a-4315-86a6-15d7d5bde97c)

**Ethanol sensor**  
Picture below demonstrates how to wire the ethanol sensor.  
Connecting and wiring pins require electrical skills, EDiPOP can be damaged if you are not careful.  
![EDiPOP - Ethanol wiring_25](https://github.com/Popov77/EDiPOP/assets/59052047/a6efc5f3-f7e4-45a1-a7f6-1df695684831)

The following ethanol sensor is proven to work, GM 13577429 .  
Be carful as you purchase your sensor, several replicas out on the market. 
![d3880c617ad69f5d4275668f1da2f5c2 _83](https://github.com/Popov77/EDiPOP/assets/59052047/80ea8b69-257b-4979-8f96-a761c9475f0f)

# MiPOP  
MiPOP is a extension module with added inputs and outputs for future platform expansions. 
Following features are available when using MiPOP.  

**EGT1** , Exhaust gas temperature sensor, reading from 100-1000C  
**EGT2** , Exhaust gas temperature sensor, reading from 100-1000C    
**EMAP** , Exhaust backpressure sensor, 0-10bar  

**PWR** needs 12V, connect to a fused (10A) ignition controlled source    
**COM** Connect **T** to pin **10** on the obd connector, OBD pin out available in the connection chapter    

![20231017_062911](https://github.com/Popov77/EDiPOP/assets/59052047/6299f174-a1fb-4272-81d0-b1c2dc984979)

**Compatible sensors**  
The exahust gas temperature sensors has to be a 2 wire k-type and suitable for >1000C.  

![20231018_110958](https://github.com/Popov77/EDiPOP/assets/59052047/c50a7678-6c61-49a3-87e1-355d92f29b8c)


The exhaust backpressure sensor must have a linear output signal between 0,5-4,5 volt. 3 wires needed, 5V/Signal/GND.    
 
![20231018_110945](https://github.com/Popov77/EDiPOP/assets/59052047/94b1c2b9-5672-463f-a522-81e091b2870d)









