![txt](https://j.top4top.io/p_311210ur10.png)

___


**Library link on the pypi platform:** **https://pypi.org/project/pazok/**


**install:** `pip install pazok`

___

# Let's start with the function tele_ms
### This function is designed to send messages to a specific Telegram user using the bot token and user's chat ID.
### The function supports sending formatted text using MarkdownV2. Here are
#### the supported formats:
```python
Bold text: *text*
Italic text: _text_
Strikethrough text: ~text~
Monospaced text: `text`
Text with a link: [text](url)
Spoiler text: ||text||
Code block: ```code```
```
### It also supports sending files and images via URL or file path. The function automatically detects whether the input is a path or URL and handles it accordingly. If the file or image includes text, it will be automatically added to the file or image description. Additionally, the function supports sending buttons of type types.InlineKeyboardButton, allowing multiple buttons in the same message or just one button. Let's start with examples.

```python
# Importing the library
import pazok

# Bot and user information
token = "token_bot"
id = "chat.id"

# Sending text only
text = "test" # Can be formatted with any supported telebot library format
pazok.tele_ms(token, id, txt=text)

# Sending text with a button
text = "test" # Can be formatted with any supported telebot library format
button = "name_button", "url_button"
# Sending multiple buttons in the same message
buttons = [
    "name_button1", "url_button1",
    "name_button2", "url_button2",
    "name_button3", "url_button3"
]
# Sending the button with text
pazok.tele_ms(token, id, txt=text, buttons=buttons)

# Sending a file or image using their path or URL with text and button
text = "text"
button = "name_button", "url_button"
file = "Link or path to the file"
image = "Link or image path"
pazok.tele_ms(token, id, txt=text, file=file, buttons=buttons)

# Note: It's possible to send either a file or an image in each message. It's not possible to send both an image and a file in the same message.

# Sending an image
pazok.tele_ms(token, id, txt=text, img=image, buttons=buttons)
```

___


# Now we have some simple functions.
### The first function is to create a random user agent in this format:
`Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36`
### Here's an example:
```python
import pazok
pazok.agnt()
```

___


# The second function is to create an Instagram-specific user agent in this format:
`Instagram 136.0.0.34.124 Android (23/6.0.1; 640dpi; 1440x2560; samsung; SM-G935; hero2lte; samsungexynos8890; en_US; 208061712)`
### Here's an example:
```python
import pazok
pazok.agnt_in()
```

___


# The third function is to obtain some cookies from the Instagram API. The cookie names that can be obtained are csrftoken and mid.
### Here's an example:
```python
import pazok
cok = pazok.cook()
print(cok.csrftoken)
print(cok.mid)

# Or like this:

print(pazok.cook().csrftoken)
print(pazok.cook().mid)
```

___


# Now we have some functions for text decoration.
#### A function to display text with a fading effect. This function changes the text color from black to white through all shades of these colors to create a smooth fading effect. You can also set the duration of the effect and format the text alignment if you want it centered on the screen or in its natural form. Here's an example:
```python
import pazok

text = "test" # The text
time = 0.05 # Duration of the effect
align = True # If you want it continuously centered, write False

pazok.tl(text, time, align)
```

___

# The second function
### The next function is to decorate English letters with 8 types.
### We can display the types using the command
```python
import pazok
pazok.info_motifs()

# This command will return to us

# - 1 - 𝗛𝗲𝗹𝗹𝗼 𝗪𝗼𝗿𝗹𝗱 𝟭𝟮𝟯
# - 2 - 𝙷𝚎𝚕𝚕𝚘 𝚆𝚘𝚛𝚕𝚍 𝟷𝟸𝟹
# - 3 - 𝐇𝐞𝐥𝐥𝐨 𝐖𝐨𝐫𝐥𝐝 𝟏𝟐𝟑
# - 4 - ʜᥱᥣᥣ᥆ ᴡ᥆ᖇᥣძ 𝟙𝟚𝟛
# - 5 - ᕼᗴᒪᒪO ᗯOᖇᒪᗪ 123
# - 6 - 𝕳𝖊𝖑𝖑𝖔 𝖂𝖔𝖗𝖑𝖉 123
# - 7 - 𝓗𝓮𝓵𝓵𝓸 𝓦𝓸𝓻𝓵𝓭 123
# - 8 - ℍ𝕖𝕝𝕝𝕠 𝕎𝕠𝕣𝕝𝕕 𝟙𝟚𝟛

# Now we can use the decoration function like this

print(pazok.motifs("text", 1)) # Note that I chose pattern number 1. I can change this number to 2 or 3 to others
```
___

# The third function
### This function consists of ready-made colors in the library. Using this function is different from other functions in that we must call the library in this way
```python
import pazok
from pazok import *

# We can display color names through this command

print(pazok.name_clo())

# This command will print

# o = orange
# b = blue
# m = white
# F = dark green
# Z = light red
# e = dark gray
# C = strong white
# p = wide line
# X = yellow
# j = pink
# E = light gray

# Each letter represents its color
# For example, if we write
print(f"{e} TEST")
# The word will print in dark gray
# And so on the rest of the colors
```
___

# The fourth function
### We have two functions that do the same job almost
#### The function is to display text with a waiting form and a certain period
#### The first is:
```python
import pazok
text = "text" # The text
staliy = "name_staliy" # The pattern
time = 1 # Time

pazok.pazok_rich(text, staliy, time)

# We can display the names of the patterns using this command

pazok.name_rich()

# Will return
# 1. arrow
# 2. christmas
# 3. circle
# 4. clock
# 5. hearts
# 6. moon
# 7. pong
# 8. runner
# 9. star
# 10. weather
```
___

## The second is:
```python
import pazok
text = "text" # The text
staliy = "bounce" # The pattern
time = 1 # Time

pazok.pazok_halo(text, staliy, time)

# We can display their special styles with this command
pazok.name_halo()

# Will print

# 1. dots
# 2. dots2
# 3. dots3
# 4. dots4
# 5. dots5
# 6. dots6
# 7. dots7
# 8. dots8
# 9. dots9
# 10. dots10
# 11. dots11
# 12. dots12
# 13. line
# 14. line2
# 15. pipe
# 16. simpleDots
# 17. simpleDotsScrolling
# 18. star
# 19. star2
# 20. flip
# 21. hamburger
# 22. growVertical
# 23. growHorizontal
# 24. balloon
# 25. balloon2
# 26. noise
# 27. bounce
# 28. boxBounce
# 29. boxBounce2
# 30. triangle
# 31. arc
# 32. circle
# 33. square
# 34. circleQuarters
# 35. circleHalves
# 36. squish
# 37. toggle
# 38. toggle2
# 39. toggle3
# 40. toggle4
# 41. toggle5
# 42. toggle6
# 43. toggle7
# 44. toggle8
# 45. toggle9
# 46. toggle10
# 47. toggle11
# 48. toggle12
# 49. toggle13
# 50. arrow
# 51. arrow2
# 52. arrow3
# 53. bouncyBall
# 54. bouncyBall2
# 55. smiley
# 56. monkey
# 57. hearts
# 58. clock
# 59. earth
# 60. moon
# 61. runner
# 62. pong
# 63. shark
# 64. dqpb
# 65. weather
# 66. emoji
# 67. fire
# 68. lioud
# 69. magic
# 70. curses
# 71. chrome
# 72. windows
# 73. eyes
# 74. action
# 75. mr.robot
# 76. dvd
# 77. pacman
# 78. audi
# 79. bing
# 80. mobile
# 81. data
# 82. bit
# 83. mark
# 84. bit10
# 85. mew
# 86. fbi
# 87. all
# 88. food
# 89. ztang
```
___

## The following functions are used to organize data and execute functions using threads. I'll start with the explanation.

### The first function is designed to convert curl commands into requests using the requests library. Here's an example:

#### Assuming this is a curl command: `curl http://en.wikipedia.org/`
```python
# Usage:
import pazok

curl_command = "curl http://en.wikipedia.org/"
print(pazok.cURL(curl_command))

# It will print the response similar to:
# https://t.me/b_azok
import requests

response = requests.get("http://en.wikipedia.org/").text

print(response)
```
___

# The second function organizes JSON responses into a vertical format. 

### Assuming we have this response:
`{'message': 'The password you entered is incorrect. Please try again.', 'status': 'fail', 'error_type': 'bad_password'}`
```python
# If we use the command:
pazok.json_req(response_variable)

# It will print:
# message: The password you entered is incorrect. Please try again.
# status: fail
# error_type: bad_password
```






























