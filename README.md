import random

# Define a dictionary with some predefined responses
responses = {
    "hello": ["Hi there!", "Hello!", "Hey!"],
    "how are you?": ["I'm good, thanks!", "Feeling great!", "Awesome!"],
    "bye": ["Goodbye!", "See you later!", "Bye! Have a great day!"],
    "default": ["Sorry, I don't understand.", "I'm still learning. Can you rephrase that?"]
}

def chat():
    print("Welcome to the chatbox! (Type 'bye' to exit)")
    while True:
        user_input = input("You: ").lower()
        if user_input == 'bye':
            print(random.choice(responses["bye"]))
            break
        else:
            response = responses.get(user_input, responses["default"])
            print("Chatbot:", random.choice(response))

if __name__ == "__main__":
    chat()
