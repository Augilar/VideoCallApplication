# VideoCallApplication

We are using webrtc internally to communicate between 2 browsers.

To understand how it works I have written some notes,

A technology which comes builtin in our browser. There can be interconnections between browsers and then share files, streams, and so on without limits and any other servers.
There will be some protocols being used for data transfer, like TCP, UDP, etc.
webrtc uses udp. Its fast and doesn’t require any other server. But there are cons for file transfer as it is not reliable but it is a good protocol for video chats.

## public IP and private IP
The device knows its own private IP address but doesn’t know its public IP address.
Each device is assigned a private IP by the router which is connected to the internet.  The IP address of the router will be known as public IP, which will be unique in the whole internet.

## Turn servers / ice servers
Whenever we ping these servers they will give a response of from which public IP address the request is been sent.

Now these public IP addresses will act as phone numbers for uniquely differentiating browsers.

So by some method we need to share each others IP addresses to each other. It is done using signaling.

We create a socket server for sharing the public IP addresses between devices.

Drawbacks

- there can only 2 persons who can connect with each other. p2p connection.
