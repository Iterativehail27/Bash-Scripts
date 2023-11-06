# Bash-Scripts
<b>Description:</b> This is a repository for bash scripts that I have created or will create that will make life easier for common processes that I use personally.
<br><br>
<h3> (1) Wifi Bash Scripts (Monitor Mode) & (Startup Recovery)</h3>
<br>
<h2> Requirements: </h2>
This only works with this specific setup mentioned here, I make no guarantees for any other setup without necessitating manual configuration. (Make sure all Network cards are plugged in before startup).
<br><br>
1. On-board wifi network card & an additional add-on wifi network card
<br><br>
2. Kali Linux or debian based installation
<br>
<h2> Installation </h2>
-to install simply create two new .sh files from your favorite text file editor (vim for example), name it whatever you like and copy the code from the bash script files in the main repository labeled Wifi bash script (Monitor Mode)/(Startup Recovery) then paste them separately to the .sh files that you had just made. Save the files.
<br><br>
-Now either leave the files where it they're at or use the "mv" command to move the files to a new directory that is convenient for you such as ~/Documents/Wifi_bash_scripts and execute the command "chmod +x (FILE-NAME-HERE)" for each file to make them executable. Additionally you can configure these now executable .sh files as hotkeys on your keyboard either through using the command "bind" or just going to system settings in Kali Linux and adding a hotkey then pointing to the individual files in their respective file path.
<br><br>
-The (Monitor Mode) file disables all network function including the wpa_supplicant & NetworkManager. It will disable the on-board wifi network card, rename the add-on network card to Wlan#mon and change it over to monitor mode then change its state to up.
<br><br>
-The (Starup Recovery) file disables all networking again by powering off all networkcards by flipping their states to down it then changes the name wlan#mon of the add-on wifi network card back to wlan# and changes its mode back to managed. It also changes the mac addresses to a random mac address for both cards before it re-enables the on-board wifi network card & the add-on network card in managed mode by flipping both of their states to up. Lastly it restarts wpa_supplicant and the network manager taking you to a default state you should normally be at on startup with all wifi network cards ready to use.

<br><br>
<h3> (2) Port Scanner </h3>
<br>
<h2> Disclaimer: </h2>
The following bash script makes use of Nmap and depending on what country you're in and who owns the network you are going to be port scanning on, you will require written permission to run this command, or it may not be allowed at all by law. Use discretion and make sure to only test this script on networks owned by you or make sure you have explicit written and signed permission from the owner and the CISO or chief technical officer if they have one, to use it to test their network for security purposes only.
<h2> Requirements: </h2>
1. Kali Linux is tested here but any Linux distribution of any kind should work or perform similarly with some tweaks.
<br><br>
2. Nmap.
<br>
<h2> Installation </h2>
-Navigate to the repository "Port Scanner" copy the code to a blank file of a name of your choosing, save the file.
<br><br>
-Next, find the file's directory and type in chmod +x (FILE-NAME-HERE) into the shell command line to make it an executable file.
<br><br>
-You can run the file locally or by using the filepath, for example, ./Documents/scripts/yourfilename OR you can use the $PATH command to find your local binaries folder, in my case it is /usr/local/bin. Just move it or copy it over to there and you will be able to type it into the shell command line by name and it will run from any directory you're currently in.
<br><br>
-You may have to use elevated privileges because of Nmap, prefixing sudo before typing in the command should allow you to run it.

<br><br>
<h3> (3) Ip_address_checker </h3>
<br>
-Simple bash script used to check the network addressable IP address of the linux machine and nothing else. It may need fine-tuning under the 'sed' tool section requiring the number n before 'p' to be changed based on the output of 'ip a' where the rows we are grabbing info from with grep are differentiated in the increasing sequence 1,2,3,4,5 and so on.
