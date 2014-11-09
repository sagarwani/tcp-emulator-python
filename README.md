TCP Emulator (Python)
=====================
An implementation of a stop-and-go version of the TCP protocol.

This app runs on top of a lossy network emulator, whereby we are able to simulate lost packets, duplicate packets, corrupted packets, etc. A UDP socket is used to transmit file data so we don't invoke the built-in features of Python's TCP implementation.

Because this is a model, not all TCP flags included in normal TCP headers are used. 

How to run
----------
Sender/server:
```
python Sender.py example-file-small.jpg 127.0.0.1 5000 20001 sender-log.txt 1
```

Receiver/client:
```
python Receiver.py received-1.jpg 20000 127.0.0.1 20001 receiver-log.txt
```

Example newudpl usage:
```
./newudpl -o localhost:20000 -i localhost:20001 -p 5000:6000 -L 5
```