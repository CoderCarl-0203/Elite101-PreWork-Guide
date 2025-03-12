# Elite101-PreWork-Guide
This project involves creating a simple chatbot using Python, designed to simulate a conversation in a retail store scenario. 


# Simple Chatbot Template for Elite 101 Project
# This chatbot will welcome the user, ask for their name and age, and present a list of options
# The user can choose an option to continue the conversation or exit

def welcome_message():
    print("Hello! Welcome to our chatbot service.")
    print("I'm here to assist you. Let's get started!")

def get_user_info():
    name = input("What's your name? ")
    age = input(f"Hi {name}, how old are you? ")
    return name, age

def show_menu():
    print("\nHow can I help you today?")
    print("1. Ask about store hours")
    print("2. Ask about product availability")
    print("3. Inquire about prices")
    print("4. Exit")

def handle_choice(choice):
    if choice == '1':
        print("Our store is open from 9 AM to 9 PM every day.")
    elif choice == '2':
        print("We have a variety of products available. Please specify what you're looking for!")
    elif choice == '3':
        print("Prices vary by product. You can ask about a specific product.")
    elif choice == '4':
        print("Thank you for chatting with us! Goodbye!")
        exit()
    else:
        print("Invalid choice. Please select a valid option.")

def chatbot():
    welcome_message()
    name, age = get_user_info()

    while True:
        show_menu()
        user_choice = input("Please enter a number from the menu: ")
        handle_choice(user_choice)

# Ensure that the chatbot starts when the script is executed
if __name__ == "__main__":
    chatbot()
