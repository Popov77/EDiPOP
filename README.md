# EDiPOP

![image](https://github.com/Popov77/EDiPOP/assets/59052047/09ec6bb1-3284-4f13-ae8d-0e5171de9561)

# Introduction

EDiPOP is a user-friendly OBD module which connects through WiFi to a mobile smart device. 
A set of various live engine data fetched from the ECU/TCU/Sensors is presented in the browser. The data assists in monitoring engine health and performance capacity. 

Start you engine and your ready to log and display data in the matter of seconds.  

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
• BLEND - external ethanol sensor measurement

![image](https://github.com/Popov77/EDiPOP/assets/59052047/2b763626-b84c-4de1-b87a-951e7223f6a9)

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

# Connections  
EDiPOP pin out enables for external connections, specific details found below. 
Connecting and wiring pins require electrical skills, EDiPOP can be damaged if you are not careful.  

**2** , Ethanol sensor for read out of fuel blend ratio        
**3** , 3.3V alarm event digital output signal   
**7** , 3.3V analog input signal  
**9** , 3.3V analog input signal     
**10** , MiPOP communication pin, see chapter MiPOP for further details    
**11** , MiPOP communication pin, see chapter MiPOP for further details    

![EDiPOP pin_out v2 (1)](https://github.com/Popov77/EDiPOP/assets/59052047/5dbf3732-422f-4744-acca-8da9d59de35b)

# Connect  
Your mobile smart device must be 2.4GHz Wi-Fi Hotspot compatible. New android and apple smart devices require data coverage to allow hotspot sharing. 
Follow these steps to connect EDiPOP upon your initial set up.  
1. Activate your hotspot sharing
2. Change your **SSID** name to Hotspot and password to **abcd1234** 
3. Identify the IP address of EDIPOP in the listed hotspot connections   

**Ethanol sensor**  
Picture below demonstrates how to wire the ethanol sensor.  
Connecting and wiring pins require electrical skills, EDiPOP can be damaged if you are not careful.  
![EDiPOP - Ethanol wiring (3)](https://github.com/Popov77/EDiPOP/assets/59052047/c4e59aa5-93ea-4f03-be82-2f99d3770e7b)

The following ethanol sensor is proven to work, GM 13577429 .  
Be carful as you purchase your sensor, several replicas out on the market.   
![d3880c617ad69f5d4275668f1da2f5c2 (2)](https://github.com/Popov77/EDiPOP/assets/59052047/372a540a-f05e-4a60-8e26-1eaa12474661)

# MiPOP  
MiPOP is a extension module with added inputs and outputs for future platform expansions. 
Following features are available when using MiPOP.  

**EGT1** , Exhaust gas temperature sensor, reading from 100-1000C  
**EGT2** , Exhaust gas temperature sensor, reading from 100-1000C    
**EMAP** , Exhaust backpressure sensor, 0-10bar  

**PWR** needs 12V, connect to a fused (10A) ignition controlled source.  
**COM** Connect **T** to pin **10** on the obd connector, OBD pin out available in the connection chapter.  

![20231017_062911](https://github.com/Popov77/EDiPOP/assets/59052047/b0762c45-b82c-42e4-9297-c451818235e9)

**Compatble sensors**  
The exahust gas temperature sensors need to be k-type and suitable for >1000C.  
PIC   

The exhaust backpressure sensor should have a linear output signal between 0,5-4,5 volt.  
PIC  









