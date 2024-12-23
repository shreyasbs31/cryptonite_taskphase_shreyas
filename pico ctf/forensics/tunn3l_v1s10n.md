# tunn3l v1s10n

**FLAG**: `picoCTF{qu1t3_a_v13w_2020}`

## Approach

1. The file wouldn't open since it was clearly corrupted (i had solved a similar challenge in oasisCTF so i quickly understood what had to be done)
2. So i opened up the file on a hex editor, and noticed that it is a corrupted BMP file. I had never heard of a BMP file before so i read up on it, and on checking how bmp files are meant to look. 
3. There were 2 places where there was supposed to be pixel data but instead there were the letters BAD written in its place, so i changed its values to `36` and `28` respectively as that's what a standard bmp file contains.
4. on saving it, i was able to open the file, but it opened an image which said `notaflag{sorry}`, so it wasn't a flag but atleast i fixed the image.
5. I had run into a similar issue in oasisCTF where i accidentally kept adjusting the height and width of the file, so instantly on seeing the false image, it instantly clicked that i had to change the height and width of the image. 
6. So i started messing around with the height and width of the image, and on changing the height to be equal to the width surprisingly i got the flag. 
##

## What I learnt
what a bmp file is and what the different parts of its hex mean.  
##

## References
1. [bmp](https://www.ece.ualberta.ca/~elliott/ee552/studentAppNotes/2003_w/misc/bmp_file_format/bmp_file_format.htm)
2. https://en.wikipedia.org/wiki/BMP_file_format

##

#


