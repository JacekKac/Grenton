# Grenton
Requirements 

1. Grenton HTTP module configured and working
2. Shelly device configured and working - be aware communication will take place from shelly device to grenton http module and the other way. Is the devices are in one subnet ok, if not you need to setup proper routing tables in your network hardware.

3. Network addreses examples

  Grenton HTTP module : 192.168.0.100
  Shelly device address: 192.168.0.120 
  Shelly device type: Switch 

4.** Shelly device preparation**. Go to http://192.168.0.120 -> Scripts -> Create a script -> Choose a name like "grenton webhook" past the script, save, turn on restart. In case it's a dobule switch add another script, changing the SwitchId field from 0 to 1.

This will cause shelly to send state updates after every change of input our output and every x minute as a heartbeat to synchronize status in case of grenton reboot etc. 

5. Grenton HTTP module preparation

a) Add virtual obcject HTTP Listener "HttpListener" with a choosen name put "/shelly" into Path variable.    
   
<img width="840" height="536" alt="image" src="https://github.com/user-attachments/assets/57780245-ad10-4781-8a8f-0751176ce10e" />


b) Create a response parsing script and attached it to onRequest event
<img width="843" height="281" alt="image" src="https://github.com/user-attachments/assets/a205320c-6af8-49b2-9595-f37b7aa7c325" />
