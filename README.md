# About
this is a demo program that capture TCP and UDP packets on two different interfaces. each capture runs on its own thread and each thread dump captured traffic in a separate file in 'pcap' format in program directory. captured files are named as interfaces names and interfaces are not in promiscuous mode.

# Usage
```
# gcc -pthread -o packiffer packiffer.c -lpcap
# ./packiffer [-t tcp interface] [-u udp interface] [-c number of packets to capture]
```

we also need libpcap to compile program.

####Ubuntu

```# apt-get install libpcap-dev```

####Fedora

```# yum install libpcap-dev```

####FreeBSD [via Ports]

```
cd /usr/ports/net/libpcap/ && make install clean
pkg install libpcap
```

below command lists all of your interfaces.

```ifconfig -a```

# example
```# ./packiffer -t eth0 -u eth1 -c 1000```

# enviroment and compiler
i use vim editor and gcc compiler.
