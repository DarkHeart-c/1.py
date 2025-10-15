# DarkHeart1.py
Little chat-bot

print("Hello! My name is Verin, your AI assistant for today.")
print("I am here to help you with anything you need.")

name = input("What's your name? ")
name = name.capitalize()
print(f"Hello {name}! It's nice to meet you!")

while True:
    help = input("Can I help you with anything you need? (Yes or No) ").strip().lower()
    if help == "yes":
        need = input("Great! What do you need help with? (Type 'exit' to quit) ").strip().lower()
        if need == "exit":
            print(f"Goodbye, {name}! Have a great day!")
            break
        elif "joke" in need:
            print("Why did the computer show up at work late? It had a hard drive!")
        elif "time" in need:
            from datetime import datetime
            print("The current time is:", datetime.now().strftime("%H:%M:%S"))
        else:
            print(f"I will do my best to help you with '{need}'.")
    elif help == "no":
        print(f"Okey dokey, {name}. Have a great day!")
        break
    else:
        print("I'm sorry, I didn't understand that. Please respond with 'Yes' or 'No'.")
