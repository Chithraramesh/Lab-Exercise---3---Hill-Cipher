# Lab-Exercise---3---Hill-Cipher
Hill Cipher using with different key values
# Aim:
To develop a simple C program to implement Hill Cipher.
# Procedure:
# Step 1:
Design of Hill Cipher algorithm
# Step 2:
Implementation using C or Python code.
# Step 3:
Testing algorithm with different key values.

# Algorithm Description:
The Hill Cipher is a substitution cipher invented by Lester S. Hill in 1929. Each letter is represented by a number modulo 26. To encrypt a message, each block of n letters is multiplied by an invertible n x n matrix, again modulus 26. To decrypt the message, each block is multiplied by the inverse of the matrix used for encryption. The matrix used for encryption is the cipher key, and it should be chosen randomly from the set of invertible n x n matrices(modulo 26). The Cipher can be adapted to an alphabet with any number of letters. All arithmetic just needs to done modulo the number of letters instead of modulo 26. 

# Program:
```
key = [[3, 3],
       [2, 5]]

plaintext = input("Enter plaintext: ").upper().replace(" ", "")

if len(plaintext) % 2 != 0:
    plaintext += "X"

ciphertext = ""

for i in range(0, len(plaintext), 2):
    a = ord(plaintext[i]) - ord('A')
    b = ord(plaintext[i + 1]) - ord('A')

    c1 = (3 * a + 3 * b) % 26
    c2 = (2 * a + 5 * b) % 26

    ciphertext += chr(c1 + ord('A'))
    ciphertext += chr(c2 + ord('A'))

print("Plaintext:", plaintext)
print("Ciphertext:", ciphertext)
```
# Output:
<img width="367" height="200" alt="image" src="https://github.com/user-attachments/assets/af964081-edc9-4057-99cc-06dd0c9316e5" />

# Result:
The program is executed successfully.
