<b>*<H1>Not My friend's Password</H1>*</b>

<b>*Question*</b>

decode this password: 98df1b3e0103f57a9817d675071504ba

submit flag as CHF{<Insert Password>}

<b>*Answer*</b>

This challenge was straight forward. I used an online hash cracker to fasten the process.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/190655671-1076575d-1eb7-4d4d-b324-98320cc7fe65.png"></p>

<b>*Flag*</b>

```CHF{mickeymouse}```

<b>*<H1>Rip it open</H1>*</b>

<b>*Question*</b>

Some sussy zip file right here :O open it?

<b>*Answer*</b>
  
There are two steps to this challenge. FIrst get the hash of the file. 

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/190658372-71ec37b2-22e3-4543-a18c-820ac90a65dc.png"></p>
  
Next, get the attack number of the hash type from hashcat as shown below. Since there are two hash type that cannot be distinguished, try both of both.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/190658201-a128cdf0-4192-474b-8711-765ddf58b010.png"></p>
  
Either one of the hash type will get you the answer.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/190658063-b63ecd35-843a-4ad1-af2c-66d39b384ce5.png"></p>

<b>*Flag*</b>

```CHF{hellokitty}```
  
<b>*<H1>Crackme 1</H1>*</b>

<b>*Question*</b>

This challenge was straight forward. I used an online hash cracker to fasten the process.

<b>*Answer*</b>
  
<p align="center"><img src="https://user-images.githubusercontent.com/66903347/190659289-f717c418-96fb-4df8-a9f7-eb55af033712.png"></p>

<b>*Flag*</b>

```CHF{double_rainbow}```
  
<b>*<H1>Crackme 2</H1>*</b>

<b>*Question*</b>

areulost 6359c3ccbb3fb21b59d3e24c37fe2d7d

Please include CHF{} before submission.

Tip: hashcat

<b>*Answer*</b>

The hint was indeed "areulost" and "6359c3ccbb3fb21b59d3e24c37fe2d7d". I must say this was quite the challenge for those like me who spent hours trying to figure out what the hash type was. I tried searching for its hash type. But to no avail these hash types didn't work as shown below.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/190652659-6277eeea-4a59-4dd5-b85a-c2a13d6df8fb.png" width=300px></p>

It took some cracking of brain juice to find out there were some hash and salt formatted that hashcat could deliver.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/190653326-23a2b853-d7c3-4308-87f5-5375e7cb4e10.png" width=500px></p>

Thus, I went on to format the hash and used "areulost" as the salt. After a few attempts of trying, it worked.

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/190653752-fda9b1b9-ca05-414e-a31c-795b6e029cf0.png"></p>

<b>*Flag*</b>

```CHF{babygurl}```

<b>*<H1>Weird Base</H1>*</b>

<b>*Question*</b>

My teacher told me there are many bases, but I thought I could score a home run by running 4 bases?

hash: VTFVMVJsSlZNREpOTVdoSVZGWnNXVkpXY0VST01ERkxWVlpTVEZSV2NGZFVSRlpXVm5wU1lWRnNVa2hVYkU1SlRXb3dPVkJSUFQwPQ==

<b>*Answer*</b>

The hint was "running 4 bases". It told me the hash was encrypted 4 times by base** hashes. There are a few base** hashes in total and I tried an error unitl I got the correct sequence. 

<b><i>BASE64 -> BASE64 -> BASE64 -> BASE32</i></b>

<p align="center"><img src="https://user-images.githubusercontent.com/66903347/190653983-6835b6a2-a334-4449-8d9f-4790dfaab0f2.png" width=800px></p>

<b>*Flag*</b>

```CHF{w31rd_ba535_ind33d}```
