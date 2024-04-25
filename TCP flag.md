### Capturing packets with tcpdump


You're telling `tcpdump` to capture packets on the `eth0` interface and print each packet's content in ASCII format, including both the packet header and payload.

- The `-i` option, it specifies the network interface to capture packets from. In your command, `eth0` is the network interface specified.

- The `-A` option tells `tcpdump` to print each packet in ASCII format, displaying both the packet's header and its payload as ASCII characters.

#### Run tcdump on the vsFTPd 2.3.4 Exploitation shell

```
$ tcpdump -i eth0 -A

```

Look at the packets and you'll find the FLAG:TCP.

![[tcpdump.png]]

The flag is {FLAG:TCP:8fb04648d6b2bd40af6581942fcf483e}