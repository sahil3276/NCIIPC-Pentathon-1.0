#  USB - Ultra Secure Bank

## Description

Ultra Secure Bank was famous for being super safe — so safe that no one could break in. So the bank challenged the whole world to try to break in. Can you find your way into the most secure account and save the day? Find a way past its strong security? Show your skills and conquer the Ultra Secure Bank!
<br><br>
![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Ultra%20Secure%20Bank/Images/1.jpg)
## Solution
1. Visit the site. Try to **Register** as admin:admin <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Ultra%20Secure%20Bank/Images/3.jpg)
2. Intercept the Request and send that to **Repeater** & Forward it. <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Ultra%20Secure%20Bank/Images/4.jpg)
3. Now Visit the Login Page and enter the Credential admin:admin **[intercept it also.!]**  <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Ultra%20Secure%20Bank/Images/2.jpg) <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Ultra%20Secure%20Bank/Images/6.jpg)
4. **Forward this Request also.. at this time we will not get the flag. Even if we registered as admin :(**
5.**if we try to change password of the admin with hos 'uid' . it states that we need to be in localhost to change admin's Password [will give you explaination at the End.!]**
6. After spending more than **9 hours** on this challenge i tried this thing & it worked 4 me.
7. Both request which we have forwarded into repeater we need to send them simultaneously & we will get the flag
     <br> <br>   <br> **HERE IS HOW.!**
 * In Repeater 1st send /api/register Request we will get "Registration Successful"
 * Now Send /api/login request within 10 Seconds .. **We Got the Flag**

<br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Ultra%20Secure%20Bank/Images/8.jpg)

## Flag

flag{TqvzzbRTezy1gVtKwm1iRw==}
