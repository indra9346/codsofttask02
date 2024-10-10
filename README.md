# codsofttask02
 PASSWORD GENERATOR
 A password generator is a useful tool that generates strong and
 random passwords for users. This project aims to create a
 password generator application using Python, allowing users to
 specify the length and complexity of the password.
 User Input: Prompt the user to specify the desired length of the
 password.
 Generate Password: Use a combination of random characters to
 generate a password of the specified length.
 Display the Password: Print the generated password on the screen.
 
 code:
 import random
import string
def generate_password(length, use_uppercase=True, use_numbers=True, use_special_chars=False):
    characters = string.ascii_lowercase
    if use_uppercase:
        characters += string.ascii_uppercase
    if use_numbers:
        characters += string.digits
    if use_special_chars:
        characters += string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def main():
    password_length = int(input("Enter the length of the password: "))
    use_uppercase = input("Include uppercase letters? (y/n): ").lower() == 'y'
    use_numbers = input("Include numbers? (y/n): ").lower() == 'y'
    use_special_chars = input("Include special characters? (y/n): ").lower() == 'y'

    password = generate_password(password_length, use_uppercase, use_numbers, use_special_chars)
    print("Generated Password:", password)

if __name__ == "__main__":
    main()
