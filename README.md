# Caesar Cipher

This project implements a Caesar Cipher encryption and decryption program. The Caesar Cipher is a simple substitution cipher where each letter in the plaintext is shifted a certain number of positions down the alphabet.

## Algorithm:

1. The program starts with an imported logo using the art library (not included here) for a visual introduction.

2. The alphabet is defined as a list containing lowercase letters twice, allowing for wrapping around the alphabet during encryption/decryption.
   
3. The caesar function takes three arguments:
  -  start_text: The original text to be encrypted or decrypted.
  -  shift_amount: The number of positions to shift the letters (positive for encryption, negative for decryption).
  -  cipher_direction: Indicates whether to "encode" (encrypt) or "decode" (decrypt) the text.

4. The function iterates through each character in the start_text:
  -  If the character is a letter (found in the alphabet list):
      * The function finds the index of the character in the alphabet list.
      * It then adds the shift_amount to the index, considering the cipher_direction to adjust for decryption.
      * A modulo operation (% 26) is applied to ensure the new position stays within the alphabet range (0 to 25).
      * The character at the new position in the alphabet list is retrieved and added to the end_text.
  -  If the character is not a letter (punctuation, space, etc.), it's directly added to the end_text without modification.

5. Finally, the function prints the encrypted or decrypted text (end_text) based on the cipher_direction.
