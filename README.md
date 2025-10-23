# Ex-4 Rail-Fence-Program

# IMPLEMENTATION OF RAIL FENCE – ROW & COLUMN TRANSFORMATION TECHNIQUE

# AIM:

 To write a python program to implement the rail fence transposition technique.

# DESCRIPTION:

In the rail fence cipher, the plain text is written downwards and diagonally on successive "rails" of an imaginary fence, then moving up when we reach the bottom rail. When we reach the top rail, the message is written downwards again until the whole plaintext is written out. The message is then read off in rows.

# ALGORITHM:

STEP-1: Read the Plain text.

STEP-2: Arrange the plain text in row columnar matrix format.

STEP-3: Now read the keyword depending on the number of columns of the plain text.

STEP-4: Arrange the characters of the keyword in sorted order and the corresponding columns of the plain text.

STEP-5: Read the characters row wise or column wise in the former order to get the cipher text.

# PROGRAM:
```
message = input("Enter the message: ").replace(" ", "").upper()
rails = int(input("Enter number of rails: "))
fence = [''] * rails
row = 0
down = True

for char in message:
    fence[row] += char
    # Move down or up
    if down:
        row += 1
    else:
        row -= 1
    if row == rails - 1 or row == 0:
        down = not down

cipher_text = ''.join(fence)
print("Encrypted Text:", cipher_text)
```
# OUTPUT:

<img width="392" height="76" alt="image" src="https://github.com/user-attachments/assets/d4d44cfc-9cfe-4fa9-90a1-d017c66fff24" />

# RESULT:
  Thus the implementation of vigenere cipher had been executed successfully.
