# iPerf

## Introduction <a href="#introduction" id="introduction"></a>

iPerf 3.0 is a powerful, open-source tool used for measuring the maximum TCP and UDP bandwidth performance of a network. It allows users to conduct comprehensive network performance tests between two endpoints, providing valuable insights into network throughput, jitter, and packet loss. With its simple command-line interface and support for multiple operating systems, iPerf 3.0 is an essential tool for network administrators, IT professionals, and anyone looking to optimise their network for maximum efficiency and performance.

## Installation <a href="#installation" id="installation"></a>

```
sudo apt install iperf3         [On Debian, Ubuntu and Mint]
sudo yum install iperf3         [On RHEL/CentOS/Fedora and Rocky/AlmaLinux]
sudo emerge -a net-misc/iperf   [On Gentoo Linux]
sudo apk add iperf3             [On Alpine Linux]
sudo pacman -S iperf3           [On Arch Linux]
sudo zypper install iperf3      [On OpenSUSE]
```

{% hint style="info" %}
You need to install iPerf on both machines to perform a network performance test because iPerf operates in a client-server model. One machine acts as the server, while the other acts as the client.
{% endhint %}

## Usage <a href="#usage" id="usage"></a>

### Server <a href="#server" id="server"></a>

To begin, establish a connection with the remote machine acting as the server. Start iperf3 in server mode using the -s flag, which will default to listening on port 5201. You can customize the reporting format (k, m, g for Kbits, Mbits, Gbits or K, M, G for KBytes, Mbytes, Gbytes) using the -f switch:

```powershell
iperf3 -s -f K
```

If port 5201 is already in use, you can specify a different port (e.g., 3000) using the -p switch:

```powershell
iperf3 -s -p 3000
```

Optionally, you can run the server as a daemon using the -D flag and write server messages to a log file:

```powershell
iperf3 -s -D > /tmp/logfile
```

### Client <a href="#client" id="client"></a>

On your local machine, which acts as the client for benchmarking, run iperf3 in client mode using the -c flag and specify the host where the server is running (either by IP address, domain, or hostname):

```powershell
iperf3 -c 192.168.2.1 -f K
```

## Documentation <a href="#documentation" id="documentation"></a>

[https://iperf.fr/iperf-doc.php#3doc](https://iperf.fr/iperf-doc.php#3doc)

## References <a href="#references" id="references"></a>

[https://iperf.fr/iperf-doc.php](https://iperf.fr/iperf-doc.php)
