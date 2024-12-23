# Trivial Flag Transfer Protocol

**FLAG**: `picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}`


## Approach
The challenge provides in its name itself what needs to be done. It is a TFTP. 
I first looked up how to open a pcapng file and that got me to download wireshark, then through some youtube videos i understood how wireshark works and exported all TFTP packets which gave 3 pictures and 2 text files and 1 deb file. On opening the deb file, i found that the program they were using was steghide. So on my VM i installed steghide.
The instructions.txt file contained ```GSGCQBRFAGRAPELCGBHEGENSSVPFBJRZHFGQVFTHVFRBHESYNTGENAFSRE.SVTHERBHGNJNLGBUVQRGURSYNTNAQVJVYYPURPXONPXSBEGURCYNA```
which on running through cyberchef (using ROT13) i got ```TFTPDOESNTENCRYPTOURTRAFFICSOWEMUSTDISGUISEOURFLAGTRANSFER.FIGUREOUTAWAYTOHIDETHEFLAGANDIWILLCHECKBACKFORTHEPLAN```. 
The plan file contained another cypher ```VHFRQGURCEBTENZNAQUVQVGJVGU-QHRQVYVTRAPR.PURPXBHGGURCUBGBF```
which on decrypting said ```IUSEDTHEPROGRAMANDHIDITWITH-DUEDILIGENCE.CHECKOUTTHEPHOTOS```. 
On further searching online i got to know that steghide usually is used to hide data within photos and it often has a passkey which in this case must be `DUEDILIGENCE`. 
Now on using steghide on my VM, using `steghide extract -sf picture3.bmp`, i ran the same for all 3 images and gave the passkey, which gave me the flag file.
##

## What I learnt
1. that you can embed data in images which can be extracted using programs like steghide.
2. how systems like wireshark work
3. analysing every tiny detail and using it to the fullest 
##


#


