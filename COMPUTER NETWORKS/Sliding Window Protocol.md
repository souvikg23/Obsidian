#review #flashcards 
explain Sliding window protocol
?
1. **Window Concept**: The 'window' in the Sliding Window Protocol refers to the range of sequence numbers that are allowed to be sent or received at any given time. The window 'slides' as data is transmitted and acknowledged.
    
2. **Sender's Window**: The sender has a window that defines the number of frames it can send before needing an acknowledgment from the receiver. This window size can vary depending on the network conditions and the receiver's capability.
    
3. **Receiver's Window**: The receiver's window indicates how many frames it is ready to receive. The receiver sends acknowledgments for received frames, which informs the sender about the successful delivery and the readiness to receive more data.
    
4. **Operation**:
    
    - When the sender transmits a frame, it starts a timer. If the acknowledgment isn't received within a specific time frame, the sender assumes the frame is lost or corrupted and resends it.
    - The window slides forward when acknowledgments are received. For example, if the sender's window size is 4, it can send frames 0, 1, 2, 3. Upon receiving an acknowledgment for frame 0, the window slides, and the sender can now send frame 4.
    - The protocol can be implemented as either 'Stop-and-Wait' (where the sender waits for an acknowledgment after sending each frame) or as a more efficient 'Go-Back-N' or 'Selective Repeat' approach (where multiple frames are sent before receiving acknowledgments).
5. **Flow Control**: The protocol effectively manages the flow of data by adjusting the window size. If the receiver is overwhelmed, it can reduce the window size, thus slowing down the sender. Conversely, if the receiver can handle more data, it can increase the window size.
    
6. **Error Control**: The Sliding Window Protocol also assists in error control by ensuring that lost or corrupted frames are retransmitted. It keeps track of which frames have been successfully transmitted and acknowledged.