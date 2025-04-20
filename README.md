
logo = """
 ██████╗ █████╗ ███████╗ █████╗ ██████╗     ██████╗██╗███████╗███████╗███████╗██████╗ 
██╔════╝██╔══██╗╚══███╔╝██╔══██╗██╔══██╗   ██╔════╝██║██╔════╝██╔════╝██╔════╝██╔══██╗
██║     ███████║  ███╔╝ ███████║██████╔╝   ██║     ██║█████╗  █████╗  █████╗  ██████╔╝
██║     ██╔══██║ ███╔╝  ██╔══██║██╔═══╝    ██║     ██║██╔══╝  ██╔══╝  ██╔══╝  ██╔══██╗
╚██████╗██║  ██║███████╗██║  ██║██║        ╚██████╗██║██║     ██║     ███████╗██║  ██║
 ╚═════╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝╚═╝         ╚═════╝╚═╝╚═╝     ╚═╝     ╚══════╝╚═╝  ╚═╝
"""

print(logo)
print(" Welcome to the *MAGIC* Caesar Cipher Tool! \n")
print(" Encrypt or decrypt your secret messages with ease! \n")

alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z',]

direction = input("Type 'encode' to encrypt, or 'decode' to decrypt:\n ").lower()
text = input(" Type your secret message:\n ").lower()
shift = int(input(" Enter the magic shift number:\n "))

def caesar(plain_text, shift_amount, direct):
    cipher_text = ""
    for letter in plain_text:
        position = alphabet.index(letter)
        if direct == "encode":
            new_position = position + shift_amount
        else:
            new_position = position - shift_amount
        new_letter = alphabet[new_position]
        cipher_text += new_letter
    
    print(f"\n THE {direct.upper()}D MESSAGE IS:  {cipher_text} ")

caesar(plain_text=text, shift_amount=shift, direct=direction)

print("\n Thank you for using the Magic Cipher Tool! Keep your secrets safe! ")
