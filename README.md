# HexSoftwares_AI_Powered-Virtual-Assistant


###  **Task 1: Virtual Assistant using Python**

Developed a Python-based **AI Virtual Assistant** capable of understanding user commands, answering questions using the OpenAI API, telling the time and setting or showing reminders. This project simulates real-life AI assistant behavior using simple logic and language processing.


##  Features

* ⏰ Greets the user based on the time of day
* 🕒 Tells the current time
* 📝 Sets reminders and stores them in a JSON file
* 📋 Displays saved reminders
* 💬 Uses OpenAI to answer any question dynamically
* ❌ Exits gracefully when the user types "bye" or "exit"



##  Step-by-Step Implementation

### 1. **Import Required Libraries**

```python
import datetime, json, os
import openai
```

### 2. **Setup OpenAI Key via `.env`**

```python
from dotenv import load_dotenv
load_dotenv()
openai.api_key = os.getenv("OPENAI_API_KEY")
```

### 3. **Create Helper Functions**

* `greet_user()` – Greets based on current time.
* `tell_time()` – Returns current system time.
* `set_reminder(task, time_str)` – Stores reminders in a file.
* `read_reminders()` – Reads and displays all reminders.
* `ask_openai(question)` – Sends question to OpenAI GPT and returns the answer.

### 4. **Handle Input Logic**

Handles command-based input such as:

* `"hi"` or `"hello"` → greeting
* `"time"` → current time
* `"set reminder"` → prompt for task and time
* `"show reminders"` → display all
* Fallback → ask OpenAI

### 5. **Main Function**

```python
def virtual_assistant():
    print("AI Virtual Assistant Ready. Type 'exit' to quit.")
    while True:
        user_input = input("You: ")
        response = handle_input(user_input)
        print("Assistant:", response)
        if "Goodbye" in response:
            break
```

##  Files in the Repo

```
AI_Virtual_Assistant/
├── assistant.py             # Main Python logic
├── reminders.json           # Stores all reminders
├── requirements.txt         # Required packages
├── .env                     # API key storage
└── README.md                # Project overview
```


##  Requirements (`requirements.txt`)

```
openai
python-dotenv
```

##  Sample Commands to Try

* "Hi"
* "What time is it?"
* "Set reminder"
* "Show reminders"
* "Tell me about Python"
* "Exit" or "Bye"

## Conclusion

This project demonstrates how to build a **simple yet effective AI Virtual Assistant** using Python. It combines basic programming concepts with OpenAI’s powerful NLP model to create an interactive assistant. The project can be extended to include **voice control, GUI interface**, or **calendar integration** for real-world usability.


