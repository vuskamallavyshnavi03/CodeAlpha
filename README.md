import random

# Predefined responses
responses = {
    "hello": ["Hello! How can I help you today?", "Hi there! What can I do for you?"],
    "hi": ["Hi! How can I assist you?", "Hello! How can I help?"],
    "how are you?": ["I'm just a bot, but I'm doing great! How can I assist you?", "I'm good, thank you! How can I help you today?"],
    "what is your name?": ["I'm a simple chatbot created to assist you.", "I'm your friendly chatbot!"],
    "bye": ["Goodbye! Have a great day!", "See you later!"],
    "thanks": ["You're welcome! Anything else you need?", "No problem! Let me know if you have any other questions."],
}

def chatbot_response(user_input):
    # Convert the user input to lowercase to make the chatbot case insensitive
    user_input = user_input.lower()
    
    # Find the response, if user_input is not recognized, return a default message
    if user_input in responses:
        return random.choice(responses[user_input])
    else:
        return "I'm sorry, I don't understand that. Can you please rephrase?"

def main():
    print("Chatbot: Hello! Type 'bye' to exit the chat.")
    while True:
        # Get user input
        user_input = input("You: ")
        
        # Check if the user wants to exit
        if user_input.lower() == "bye":
            print("Chatbot: Goodbye! Have a great day!")
            break
        
        # Get the chatbot response
        response = chatbot_response(user_input)
        
        # Print the chatbot response
        print(f"Chatbot: {response}")

if _name_ == "_main_":
    main()
