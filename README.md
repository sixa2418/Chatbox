from os import supports_bytes_environ
print("🤖 SupportBot: Hi! I'm your customer support assistant. Type 'exit' to end.\n")

print("Enter the exact question to get proper response.\n")
print("* what are your working hours\n")
print("* how can i reset my password\n")
print("* what is your refund policy\n")
print("* how can i contact support\n")
print("* where is my order\n")
print("* why am i unable to login my id\n")

# Define some common support questions and responses
support_data = {
    "what are your working hours": "Our working hours are 9 AM to 6 PM, Monday to Friday.",
    "how can i reset my password": "You can reset your password by clicking on 'Forgot Password' on the login page.",
    "what is your refund policy": "We offer a 7-day refund policy for unused services.",
    "how can i contact support": "You can email us through our company email or call for help.",
    "where is my order": "Please provide your order ID so we can check the status.",
    "why am i unable to login my id" : "sorry for the problem please try again after 12 hours"
}

while True:
    user_input = input("You: ").lower()

    if user_input == "exit":
        print("SupportBot: Thank you! Have a great day.")
        break
    elif user_input in support_data:
        print("SupportBot:", support_data[user_input])
    else:
        print("SupportBot: I'm sorry, I didn't understand that. Please try a different question.")
