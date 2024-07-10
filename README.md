

___


# Storing Data in a File using the `save_data` Function
## After storing any data in the file, the function will move to a new line to store the next data.
### Here is an example:
```python
import pazok

nesme_file = "text_file_name.txt"
data = "data to be saved in the file"

pazok.save_data(nesme_file, data)
```

___


# The `check_tele` Function
## This function checks if a user is subscribed to a specific Telegram channel using the channel's username.
### Note: You need to have a bot token, and the bot must be an administrator in the channel.
### To check a user's subscription, you need the Telegram user's chat ID.
### Here is an example:
```python
import pazok

token_bot = "0000"
channel_username = "@username"
chat_ID = "id_user"

test = pazok.check_tele(token_bot, channel_username, chat_ID)

print(test)
```

___


### The function will return `True` if the user is subscribed, `False` if not subscribed, and `bot is not administrator` if the bot is not an administrator in the channel.

# The `art_ar` Function
## This function converts Arabic text into beautiful art.
### The function supports any type of Arabic or English fonts.
### Here is an example:
```python
import pazok

text = "Arabic or English text"

line_path = ""  # Enter the desired path or leave it empty to use the default font

size = 25  # Or leave it empty to use the default value

style = 1  # There are two styles, you can leave it empty or set it to 2
```

___


# The `img_txt` Function
## This function extracts text from images supported by Google.
### The function needs the image path to extract the text from it.
### Here is an example:
```python
import pazok

image_path = "path to the image"
test = pazok.img_txt(image_path)
print(test)
```
