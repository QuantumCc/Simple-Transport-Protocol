APPROACHES:
Began by getting a basic understanding of the project from the starter code, I decided to use a dictionary to contain the packets for the receiver, this worked well since dictionary does not allow duplicate packets, every time an EOF true flag is encountered, packets in the dictionary would be printed according to their sequence number. For the sender I created two dictionaries each representing buffered packets and sent packets. Every time a message was sent, the message will be added to the buffered packets. If an ack is received, the message will pop from the buffered packets and to the sent packets. At the end, by comparing the difference of the two dictionaries, it's easy to find out which packets failed in sending, I then resend those packets. Once everything is sent, the receiver would receive an true EOF from sender, it then prints out all the messages.

Tests:
I use the test cases provided in the VM to test.

