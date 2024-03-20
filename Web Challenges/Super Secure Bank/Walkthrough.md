# SSB - Super Secure Bank
Description

In this challenge, you'll put your code-breaking skills to the test! The once-impregnable Super Secure Bank has been hacked, its data encrypted. Your task is to crack the code, recover the data, and capture the hidden flag.

Image of the hacked Super Secure Bank website:  ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Super%20Secure%20Bank/Images/1.jpg)

1. Upon reading this code, we can assume three things:

  1. For each character of the func string XORed with our username, the variable buf adds a new char to itself.
  2. At the end, it will try to run the result of buf as actual code with eval(). We can tell that it will probably run a check and send us to the flag.
  3. The buf variable might have the text “password” since we don’t use the password in the main loop code

2. JavaScript Console Strategy:
```
    Define xor Function:
    JavaScript

    function xor(ori_chr, dst_chr) {
      return String.fromCharCode(ori_chr.charCodeAt() ^ dst_chr.charCodeAt());
    }
```
<br></br>
![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Super%20Secure%20Bank/Images/2.jpg)

Use code with caution.

    Brute-Force Username:
        With that noted, we can try to brute force all possibilities of the position of the string “password” in our buf

    Decode and Verify:
        Use the xor function to decrypt code with potential usernames.
        Look for document.location and valid JavaScript syntax to pinpoint the correct username.

3. Discover the Password:

    The eval(buf) statement likely holds a password check.
    Examine the decrypted code to reveal the password.
<br></br>
![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Super%20Secure%20Bank/Images/3.jpg)
4. Retrieve the Flag

        The results will give us all the possible usernames (even those with non-printable charcodes)
        that will gives us the string “password” in the buf variable.
        When testing all our usernames, we run the same code that builds the buf variable, but we do 
        not run eval() but instead print buf and check what result we get for each username we use.
        When looking at all the possibilities, one stands out

<br></br>
![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Super%20Secure%20Bank/Images/5.jpg)
   AND HERE IS THE FLAG.
                  flag{586f7249734e6f74536f6f533363757233}

Thank you.
