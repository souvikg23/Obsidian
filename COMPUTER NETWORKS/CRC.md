---
sr-due: 2024-01-11
sr-interval: 1
sr-ease: 230
---

#review #flashcards 

?
- Cyclic Redundancy Check
- 1. **Polynomial Representation**: CRC employs a mathematical approach using polynomial representation of the binary data. A specific polynomial, agreed upon by the communication system, is used for this purpose. This polynomial is known as the 'generator polynomial'.
    
2. **Appending Zeros**: The CRC process begins with the sender appending a number of zeros to the end of the data block. The number of zeros added is typically one less than the degree of the generator polynomial.
    
3. **Division**: The data block (including the appended zeros) is then divided by the generator polynomial using binary division. The remainder of this division is the CRC.
    
4. **Transmission**: The CRC is appended to the end of the original data block and this entire packet is sent to the receiver.
    
5. **Verification at Receiver**: Upon receiving the packet, the receiver performs a similar polynomial division using the same generator polynomial. It divides the received data (including the received CRC) by the generator polynomial.
    
6. **Error Detection**: If the division at the receiver's end results in a non-zero remainder, it indicates that an error has occurred in transmission. If the remainder is zero, the data is considered to be error-free (though it's important to note that while unlikely, it is still possible for errors to go undetected).
    

The strength of a CRC algorithm depends largely on the choice of the generator polynomial. The polynomial should be chosen to maximize the likelihood of detecting common types of errors, such as burst errors. Commonly used CRC standards include CRC-32, CRC-16, and CRC-CCITT.