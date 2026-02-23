# Grenton
Requirements 

1. Grenton HTTP module configured and working
2. Shelly device configured and working - be aware communication will take place from shelly device to grenton http module and the other way. Is the devices are in one subnet ok, if not you need to setup proper routing tables in your network hardware.

3. Network addresses examples

  Grenton HTTP module : 192.168.0.100
  Shelly device address: 192.168.0.120 
  Shelly device type: Switch 

4. Shelly device preparation. Go to http://192.168.0.120 -> Scripts -> Create a script -> Choose a name like "grenton webhook" past the script, save, turn on restart.

   
