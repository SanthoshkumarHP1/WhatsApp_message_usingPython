Description:

```python
import pywhatkit
import time

class Birthday:

    @staticmethod
    def wish():
        messages = []
        for i in range(1, 1000):
            if i == 100:
                messages.append(f"{i} HII..")
            else:
                messages.append(f"{i}. Happy birthday..")

        return "\n".join(messages)

# Create the message
message = Birthday.wish()

# Define the phone number (replace with the recipient's phone number)
phone_number = "+91XXXXXXXXXX"  # Replace with the target phone number

# Number of times to send the message
num_times = 1

for i in range(num_times):
    # Send the message via WhatsApp
    pywhatkit.sendwhatmsg_instantly(phone_number, message)
    # Optional: Add a delay to avoid being flagged as spam
    time.sleep(0.1)  # 0.1 seconds delay between messages
```

### GitHub Repository Description

# Birthday Wisher

This Python script sends automated birthday wishes via WhatsApp using the `pywhatkit` library. You can customize the message and specify the recipient's phone number.

## Features

- Sends a series of birthday messages.
- Uses the `pywhatkit` library to send WhatsApp messages instantly.
- Simple and easy-to-use script.

## Usage

1. Install the required library:
    ```bash
    pip install pywhatkit
    ```

2. Customize the message and recipient's phone number in the script:
    ```python
    # Define the phone number (replace with the recipient's phone number)
    phone_number = "+91XXXXXXXXXX"  # Replace with the target phone number
    ```

3. Run the script:
    ```bash
    python birthday_wisher.py
    ```

4. Optionally, add a YouTube video link or any other link to the message:
    ```python
    message += "https://www.youtube.com/watch?v=FLvxuM1_rDk"  # Replace with your video link
    ```

## Disclaimer

Use this script responsibly. Sending a high volume of messages in a short period may result in your account being flagged as spam. Adjust the `time.sleep()` delay as necessary to avoid this.
