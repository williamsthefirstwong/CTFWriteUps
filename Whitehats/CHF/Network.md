<b>*<H1>Challenge: Sshhhh</H1>*</b>

<b>*Question*</b>

Take control of our hacking machine!

User: ctfuser Host: box.whitehats.space Port: Any number from 2000 to 2100 Password: whitehats! You can find the flag in ~/releases/misc/CHFlag.txt

<b>*Answer*</b>

All we have to do is ssh into the machne and grab the flag

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/188261755-4ab859b3-d5ec-4ab1-bd64-f0dd4e92e8ed.png" width=650px></p>

<b>*Flag*</b>

```CHF{Ss5shFLagCaPtUr3D}```


<b>*<H1>Challenge: CommoN map</H1>*</b>

<b>*Question*</b>

I can be commonly found, talk to me using a network mapping and feline tool!

IP: 152.67.191.231

<b>*Answer*</b>

The hint was Nmap. I just ran a simple TCP connect scan to sift out any potential vulnerable ports. Next, using the hint feline tool, I thought of netcat and used it to scan port 8000 for a website.

<kbd>nmap 152.67.191.231 -sT</kbd>

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/189213812-18d460ad-f898-4b28-846b-c383282d8b60.png" width=450px></p>

<b>*Flag*</b>

```CHF{N3tw0rk_c4t_S4y5_Hi}```

<b>*<H1>Challenge: the Missing S</H1>*</b>

<b>*Question*</b>

A developer in Whitehats was creating an API for some testing purposes. Are you able to figure out what he was doing?

<b>*Answer*</b>

The hint was pcap file. Immediately, this calls for a wireshark analysis. One method to solve the case quickly is to use Edit -> Find Packet -> Change "Packet list" to "Packet Details" -> Enter CHF & Search. Another method is to analyse "Protocol Hierachy" (UDP Packets; which tells you something to do with export objects) and then "Export Objects" (a hint in teh flag that contains the word flag). Both methods will get you the flag hidden in <kbd>application/json</kbd> as shown below.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/189215551-6696c974-ba6f-4703-a7ba-cda4f6a8c1f0.png"></p>

<kbd>"how did you find me??? i guess here is the flag: CHF{HTTPisNOTsecure}"</kbd>

<b>*Flag*</b>

```CHF{HTTPisNOTsecure}```


<b>*<H1>Challenge: Rare Map</H1>*</b>

<b>*Question*</b>

This breed of cat is rarer in the wild, try harder to find me and use the feline tool to communicate with me. Some say that I can be found between 8000 and 9000.

IP: 152.67.163.184

<b>*Answer*</b>

The hint was implying it is a similar challenge to <kbd>CommoN map</kbd>. The only thing needed to change was now we can specify a specific range of ports.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/189217567-f35662e5-17f8-4477-8888-3cfaabe37bc5.png"></p>

<b>*Flag*</b>

```CHF{Th1s_Br33d_1s_M0re_Ex0t1c!!}```

