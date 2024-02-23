# Protopie_Display
How to get a Protopie file running on a small Raspberry Pi Screen

# Hardware
- [Raspberry Pi 4B](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/) (approx. €50)
- [Waveshare 4.3inch HDMI LCD (B) - 800x480 - IPS - Capacitive touch](https://www.kiwi-electronics.com/en/4-3inch-hdmi-lcd-b-800x480-ips-capacitive-touch-4065) (approx. €70)
- If you're not comfortable working with SSH: keyboard & mouse
# Set-up
- Preferably start with a fresh [Raspi OS](https://www.raspberrypi.com/software/) install
- Right after SD card configuration (before you put the SD card back in the Raspi), open it on you computer and open the file `config.txt`
- Add this code to the bottom of the file: 
```
    hdmi_force_hotplug=1
    hdmi_group=2
    hdmi_mode=87
    hdmi_cvt 800 480 60 6 0 0 0
```
- Mount the screen on the raspi and connect the USB and HDMI parts with the connection pieces delivered witht he Waveshare screen [documentation](https://www.kiwi-electronics.com/en/4-3inch-hdmi-lcd-b-800x480-ips-capacitive-touch-4065)
- If you want to work  wireless, consider working with an external power source
- Now you can run Raspberry Pi on the screen, allowing you to work with the browser, hence with Protopie

# Protopie connection
## Simple cases
- Just share the Protopie Cloud URL and put on fullscreen
## Complex cases
- Run Protopie Connect on a server computer
- Make sure both server and raspberry pi are on the same network
- Get the `IP adress of the server` protopie connect > connect > IP adress)
- Get the `ID of the pie` (open the pie in the browser on your server and check the url)
- Access the protopies on your raspi using the following URL structure `http://{IP_of_the_server}:9981/pie?pieid={ID_of_the_pie}`
