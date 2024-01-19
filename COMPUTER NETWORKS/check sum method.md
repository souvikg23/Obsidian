---
sr-due: 2024-01-11
sr-interval: 1
sr-ease: 230
---

#review 
- It involves calculating a value based on the sum of the bytes in a data packet, which is then sent along with the packet. The receiver performs the same calculation on the received data and compares the result with the transmitted checksum value to detect errors.
- 1. **Summation**: The sender adds up all the bytes of data in the packet. The addition is usually done using one's complement arithmetic, where all the bits are inverted, including the carry bits.
    
2. **Checksum Calculation**: Once the sum is obtained, the checksum is calculated, typically by taking the one's complement of the sum. This means flipping all the bits in the sum to generate the checksum.
    
3. **Appending Checksum**: The calculated checksum is appended to the original data packet and sent to the receiver.
    
4. **Verification at Receiver**: Upon receiving the packet, the receiver adds up all the bytes in the packet (including the received checksum). This calculation is again done using one's complement arithmetic.
    
5. **Error Detection**:
    
    - If the packet is intact and error-free, the sum at the receiver's end (including the received checksum) should be all ones (in binary). It's a way to confirm that the total sum of the packet plus the checksum has no errors.
    - If the sum contains any zeros, it indicates that errors have occurred in the packet during transmission.
6. **Limitations**: While checksums are easy to implement and require minimal processing power, they are less reliable for detecting errors compared to more sophisticated methods like Cyclic Redundancy Check (CRC). Checksums are more prone to missing certain types of errors, especially in cases where errors cancel each other out. They are more suitable for detecting random errors rather than systematic errors or burst errors.1. **Summation**: The sender adds up all the bytes of data in the packet. The addition is usually done using one's complement arithmetic, where all the bits are inverted, including the carry bits.
    
2. **Checksum Calculation**: Once the sum is obtained, the checksum is calculated, typically by taking the one's complement of the sum. This means flipping all the bits in the sum to generate the checksum.
    
3. **Appending Checksum**: The calculated checksum is appended to the original data packet and sent to the receiver.
    
4. **Verification at Receiver**: Upon receiving the packet, the receiver adds up all the bytes in the packet (including the received checksum). This calculation is again done using one's complement arithmetic.
    
5. **Error Detection**:
    
    - If the packet is intact and error-free, the sum at the receiver's end (including the received checksum) should be all ones (in binary). It's a way to confirm that the total sum of the packet plus the checksum has no errors.
    - If the sum contains any zeros, it indicates that errors have occurred in the packet during transmission.
6. **Limitations**: While checksums are easy to implement and require minimal processing power, they are less reliable for detecting errors compared to more sophisticated methods like Cyclic Redundancy Check (CRC). Checksums are more prone to missing certain types of errors, especially in cases where errors cancel each other out. They are more suitable for detecting random errors rather than systematic errors or burst errors.