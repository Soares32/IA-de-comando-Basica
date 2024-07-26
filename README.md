import random


ai_responses = {
    
    "hello": ["Hello! How can I assist you today?", "Hi! What's on your mind?", "Hey! I'm here to help."],
    "how are you": ["I'm doing great, thanks!", "I'm good, thanks for asking!", "I'm awesome, thanks!"],
    "what's your name": ["My name is AI Assistant", "I'm called AI Bot", "You can call me AI"],
    "default": ["I didn't understand that. Can you please rephrase?", "Sorry, I'm not sure what you mean.", "Can you please provide more context?"]
}


def ai_assistant():
    while True:
        user_input = input("You: ").lower()
        for key in ai_responses.keys():
            if key in user_input:
                print("AI: " + random.choice(ai_responses[key]))
                break
        else:
            print("AI: " + random.choice(ai_responses["default"]))


ai_assistant()
