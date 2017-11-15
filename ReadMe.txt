          -- Data Encryption Standard Algorithm Cipher Tool --

This program provides an implementation of the Data Encryption standard
Algorithm (DES) and a command line utility to manipulate data with it.  DES
is a symmetric key, block cipher that operates on 64 bit blocks and uses a 64
bit key.  The key is specified on the
command line.  To encrypt or decrypt data of arbitrary length either the
Electronic Code Book (ECB) or the Cipher Block Chaining (CBC) operation modes
must be used.

The program operates on an input string, encrypting or decrypting 64 bits at a
time and writing the result to the output file, until the end.  When this occurs, the data is padded with zeros to a multiple of 64
bits and the last round of encryption or decryption is performed before the
program exits. For reading or writing of ciphertext, it is first converted
from/to bits to avoid improper interpretation of binary data.


To build the software, simply run:

javac Des.java


once the file is complied, des.class file is created.
To access the code, run: java des

Eight random numbers are generated which are converted into bits.
Enter the string that has to be encrypted.
The input string is converted into bits which are divided into 64 bit blocks
Enter the 8 character key in strings which will be converted into 64 bits because 8*8=64
The first 64 bit block of the plaintext is encrypted first using the DES algorithm and then the second 64 bit block is encrypted. The process goes on.
The first 64 bit of the cipher text is xored with the key for 16 rounds to get the first 64 bit part of the plain text.
This entire process comes under ECB.

To encrypt and decrypt under CBC mode of operation, during the time of input, make sure the string repeats so that the CBC block is activated.
When this happens, string is encrypted and decrypted using CBC mode.

In the end the decrypted bits are displayed and the bits are converted back to the string format.

