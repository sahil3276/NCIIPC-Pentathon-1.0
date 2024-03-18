# Local Bank Returns

## Description

Welcome back to your uncle's bank, this time with a twist. The sensitive file is hidden deeper within intricate security measures and cunning traps. Can you rise to the challenge once again, navigating through heightened defenses to uncover the coveted secrets? It's time to put your skills to the test and prove your mastery of digital espionage.

PS: I heard that your uncle doesn't like nano text editor.

![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Local%20Bank%20Returns/Images/1.jpg)

## My Thought Process + Steps

1. By looking at the Nginx.conf file attached with the challenge, we get that we a LFI is possible if we craft the payload very carefully.
2. The challenge description also has a note which says "PS: I heard that your uncle doesn't like nano text editor." and the hint says "If it is not nano, then he might be using vim to edit html files". This suggests that the challenge has something to do with these text editors. <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Local%20Bank%20Returns/Images/2.jpg)
3. Turns out, these text editors create a swap (.swp) file of files being edited which can stay on the disk if not manually deleted.
4. Therefore our goal it to get the index.html.swp file.
5. The final payload including the url is: **https://<id>.ch.eng.run/chall../chall/.index.html.swp** <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Local%20Bank%20Returns/Images/3.jpg)
6. This will download the file in our system and the flag can be found inside <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Local%20Bank%20Returns/Images/4.jpg)
7. We Got the Flag.!
<br><br>  ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Local%20Bank%20Returns/Images/5.jpg)
## Flag

flag{NginX_4li45_p4th_tr4v3r54l5_r_b4d!!!}
