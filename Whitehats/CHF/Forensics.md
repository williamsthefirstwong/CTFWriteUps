<b>*<H1>Challenge: Nyan Cat</H1>*</b>

<b>*Question*</b>

I am having trouble finding the answer in this file, can you help me find the flag?

<b>*Answer*</b>

Data can be stored in pictures as strings.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/188260097-3fc1cbbb-4b45-4bfc-9e32-a57c0c4016be.PNG"></p>

<b>*Flag*</b>

```CHF{str1ng5_are_fun!}```

<b>*<H1>Challenge: Thread Grabber</H1>*</b>

<b>*Question*</b>

The flag is somewhere in this list, can you help me find the flag?

<b>*Answer*</b>

Upon viewing the file, it just says data as its file type.

Thus, I went to open the file to view its contents in hopes of determining what the file contains.

Assuming the file is a list of passwords and the challenge states the flag is inside the file, I tried to find the flag.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/188260257-1b3dcbf0-105e-47dd-8675-87cf1df0ef2f.PNG"></p>

<b>*Flag*</b>

```CHF{gr3p_1s_c00l!}```

<b>*<H1>Challenge: Trashrun</H1>*</b>

<b>*Question*</b>

Michael Jackson invented moonwalk, but do you know Linux had its own version of walking as well?

<b>*Answer*</b>

The hint was linux and walking, thus I immediately thought of binwalk.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/188260500-a24cfff6-ed21-4313-b3b1-e1be302b60fc.png" width=500px height=500px></p>

<b>*Flag*</b>

```CHF{b1nw4lk_unh1d35_f1l35_4_y0u}```

<b>*<H1>Challenge: Where my Hash(Brown)</H1>*</b>

<b>*Question*</b>

An employee of Whitehats has created a system to write some challenges for an upcoming CTF. However, his user credentials were exposed by an attacker. Are you able to obtain his credentials from the provided memory image?

Please provide the flag in the following format: CHF{username:password}

Hint: volatility is a useful tool! It is also available on our remote SSH shell under volatility3!

<b>*Answer*</b>

The hint was volatility, thus it is used to inspect the memory dump file. Since the file did not state the operating system (os) of the file, use volatility to determine the possible os in the file.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/188260591-bee4cdb3-a5cd-4e9a-8b61-cc762b91658a.PNG"></p>

Upon seeing the os may be Win7SP1x64, Win7SP0x64, etc, I used the first option to find credentials in the memory dump file.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/188260597-d491d167-d706-4a45-9395-7be8c86041d8.PNG"></p>

After getting the hashes, it's time to crack! crack! crack! 

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/188260839-3871be1e-804f-41e8-bf8e-148c5cc544a3.PNG"></p>

Seeing that the password is ```password``` and the only users are ```Administrator```, ```Guest``` and ```whitehacks```, we just need to find the whitehats employee and <b>NOT</b> the Administrator of the network.

<b>*Flag*</b>

```CHF{whitehacks:password}```
