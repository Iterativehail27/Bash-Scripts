# Bash-Scripts
<b>Description:</b> This is a repository for bash scripts that I have created or will create that will make life easier for common processes that I use personally.
<br><br>
<h3> (1) Wifi Bash Scripts (Monitor Mode) & (Startup Recovery)</h3>
<br>
<h2> Requirements: </h2>
This only works with this specific setup mentioned here, I make no guarantees for any other setup without manual configuration. (Make sure all Network cards are plugged in before startup).
<br><br>
1. On-board wifi network card & an additional add-on wifi network card
<br><br>
2. Kali Linux or debian based installation
<br>
<h2> Installation </h2>
<br>
-to install simply create two new .sh files from your favorite text file editor (vim for example), name it whatever you like and copy the code from the bash script files in the main repository labeled Wifi bash script (Monitor Mode)/(Startup Recovery) then paste them to their own .sh files. Save the file.
<br><br>
-Now either leave the file where it is at or use the mv command to move the file to a new directory that is convenient for you such as ~/Documents/Wifi_bash_scripts and execute the command chmod +x (FILE NAME HERE) to make it executable. Additionally you can configure these now executable .sh files as hotkeys on your keyboard either through using the command bind or just going to system settings in kali linux and adding a hotkey then pointing to the individual files in their respective file path.
<br><br>
-The (Monitor Mode) file disables all network function including the wpa_supplicant & NetworkManager. It will disable the on-board wifi network card, rename the add-on network card to Wlan#mon and change it over to monitor mode then change its state to up.
<br><br>
-The (Starup Recovery) file disables all networking again by powering off all networkcards by flipping their states to down it then changes the name wlan#mon of the add-on wifi network card back to wlan# and changes its mode back to managed. It also changes the mac addresses to a random mac address for both cards before it re-enables the on-board wifi network card & the add-on network card in managed mode by flipping both of their states to up. Lastly it restarts wpa_supplicant and the network manager taking you to a default state you should normally be at on startup with all wifi network cards ready to use.
