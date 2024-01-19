---
sr-due: 2024-01-11
sr-interval: 1
sr-ease: 230
---

#review 
2. **Adding Redundancy Bits**: The first step in creating a Hamming Code is to add redundancy bits to the original data bits. These redundancy bits are extra bits added at specific positions in the original data to create a new, longer set of bits.
    
2. **Position of Redundancy Bits**: The positions of these redundancy bits are typically powers of 2 (i.e., positions 1, 2, 4, 8, 16, etc.). The rest of the positions are filled with the original data bits.
    
3. **Calculating Redundancy Bits**: Each redundancy bit is calculated based on a subset of the data bits. The idea is that each redundancy bit checks the parity (even or odd) of a specific group of bits. For example, the first redundancy bit (at position 1) checks the parity of bits that have the least significant bit in their position set to 1 (i.e., bits 1, 3, 5, 7, 9, etc.).
    
4. **Transmission**: The combined set of original data bits and redundancy bits (Hamming Code) is then transmitted or stored.
    
5. **Error Detection and Correction**: When the Hamming Code is received or read, the system recalculates the parities using the same subsets of bits used to calculate the redundancy bits initially. If the recalculated parity doesn't match the transmitted parity for any redundancy bit, it indicates an error.
    
6. **Correcting Errors**: The position of the error can be determined by analyzing which parity checks failed. For example, if parity checks related to redundancy bits in positions 1 and 2 fail, but the check for position 4 passes, it indicates an error in bit position 3 (since 1 + 2 = 3). The system then flips the bit at this position to correct the error.
    
7. **Limitations**: The Hamming Code can correct any single-bit error and detect two-bit errors, but it cannot correct more than one error simultaneously. If more than one bit error occurs, the system may incorrectly correct a non-erroneous bit based on the error indication.