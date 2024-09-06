# Encrypted Communication with SHA-256

## Project Overview
This project demonstrates a simple encrypted communication system using SHA-256 hashing. It allows a sender to send a message to a receiver, and the receiver can validate the message to ensure it hasn't been tampered with. This ensures the integrity of the communication.

The project is written in Python and demonstrates how hashing can be used in a back-and-forth communication system for message integrity.

## Features
- **Custom SHA-256 Hash Function**: Converts messages into unique SHA-256 hashes.
- **Message Sending**: Hashes the sender, receiver, and message into a unique identifier.
- **Message Receiving**: Validates the integrity of the message by checking if the hash matches the one sent by the sender.
- **Tamper Detection**: Demonstrates how tampered messages can be detected.

## Usage
1. **Sending a Message**: The sender's name, receiver's name, and the message are hashed together into a unique SHA-256 hash.
2. **Receiving a Message**: The receiver can validate the message by comparing the hash of the received message with the original hash.
3. **Tampered Messages**: The project detects if the message has been altered by comparing the hash of the altered message with the original.

## Example Code
```python
# Example usage: Adra sends a message to Future Game Engine Project
sender = 'Adra'
receiver = 'Future Game Engine Project'
message = 'Let’s build something great.'

# Encrypt the message and simulate sending
sent_hash = send_message(sender, receiver, message)
print(f"Message sent. Hash: {sent_hash}")

# Simulate receiving and verifying the message
is_valid = receive_message(sender, receiver, message, sent_hash)
print(f"Message valid: {is_valid}")

# Modify the message to test the integrity check
tampered_message = 'Let’s build something else.'
is_valid_tampered = receive_message(sender, receiver, tampered_message, sent_hash)
print(f"Tampered message valid: {is_valid_tampered}")
```

## Installation
Clone the repository and run the Jupyter Notebook to interact with the code.

```bash
git clone <repository-url>
cd <project-folder>
jupyter notebook Custom_Hashed_Function_Fixed.ipynb
```

## License
This project is licensed under the MIT License.

# YEAH I USED GPT FOR THE README, SUE ME!
