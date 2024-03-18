# Hold your marks

## Description

Experienced in the world of bug bounties, you stumble upon a markdown editor during your exploits. Your objective: infiltrate the server's defenses to access a concealed file, hidden away from external access. Can you leverage your skills to navigate through the editor's intricacies and uncover the secrets that lie within the server's depths?
![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Hold%20Your%20Marks/Images/hold-ur-marks.jpg)
## Solution

1. The page opens with 2 options for user input: One is a URL input to fetch markdown and one is a markdown editor <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Hold%20Your%20Marks/Images/HYM-2.jpg)
2. At first glace of the url input, the first thought i get is SSRF
3. I used BURP Collaborator to confirm my though process LOL.
4. luckily i got a response.<br><br>  ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Hold%20Your%20Marks/Images/HYM_colab.jpg)
5. But there is a catch! i.e. All localhost interaction is blocked
6. Bypass? Yes, the easisest and common bypass would be to use a URL redirect to http://localhost/flag (Why flag? I manually went to that dir to confirm that )
7. This was the code I came up with:
```python
from flask import Flask, redirect

app = Flask(__name__)

@app.route('/')
def index():
    return redirect('http://localhost/flag)

if __name__ == '__main__':
    app.run(debug=True)

```
8. This code was hosted on python server and that is connected to my NGROK server <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Hold%20Your%20Marks/Images/HYM-4.jpg)
9. so any request came through my ngrok server it will redirect to thier localhost/flag.! <br><br> ![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Hold%20Your%20Marks/Images/HYM-5.jpg)
10. That's it.. LET'S GO.
11. Paste the ngrok link and BOOMMM.. we got the flag.!
<br>
<br>

![ScreenShot](https://github.com/sahil3276/NCIIPC-W3B/blob/main/Web%20Challenges/Hold%20Your%20Marks/Images/HYM-6.jpg)

## Flag

flag(zyFE/JIZ1HnCJy+eGa5QmQ==)
