import random
import string


# Function to generate password
def generate_password(length, use_upper, use_lower, use_digits, use_symbols):
    characters = ""

    if use_upper:
        characters += string.ascii_uppercase
    if use_lower:
        characters += string.ascii_lowercase
    if use_digits:
        characters += string.digits
    if use_symbols:
        characters += string.punctuation

    # If no option selected
    if not characters:
        return "Error: No character types selected!"

    password = "".join(random.choice(characters) for _ in range(length))
    return password


# Main program
def main():
    print("====== PASSWORD GENERATOR ======")

    try:
        length = int(input("Enter password length: "))

        print("\nInclude in password?")
        use_upper = input("Uppercase letters (A-Z)? (y/n): ").lower() == 'y'
        use_lower = input("Lowercase letters (a-z)? (y/n): ").lower() == 'y'
        use_digits = input("Digits (0-9)? (y/n): ").lower() == 'y'
        use_symbols = input("Special characters (!@#)? (y/n): ").lower() == 'y'

        password = generate_password(length, use_upper, use_lower, use_digits, use_symbols)

        print("\nGenerated Password:")
        print(password)

    except ValueError:
        print("Please enter a valid number for length.")


if __name__ == "__main__":
    main()
