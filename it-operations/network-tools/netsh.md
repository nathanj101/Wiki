# Netsh

## Introduction <a href="#introduction" id="introduction"></a>

Netsh is a command-line scripting utility that allows you to display or modify the network configuration of a computer that is currently running. Netsh commands can be run by typing commands at the netsh shell and be used in batch files or scripts. Remote computers and the local computer can be configured by using netsh commands.

## Installation <a href="#installation" id="installation"></a>

**Requirements:**

* Functional computer running Windows

## Syntax <a href="#syntax" id="syntax"></a>

{% code fullWidth="false" %}
```
netsh [-a AliasFile] [-c Context] [-r RemoteMachine] [-u [DomainName\]UserName] [-p Password | *] [Command | -f ScriptFile]
```
{% endcode %}

## Usage <a href="#usage" id="usage"></a>

### Network Trace <a href="#network-trace" id="network-trace"></a>

Open Command Prompt as Administrator

Execute the following command to start the network capture and output to file

```plaintext
netsh trace start capture=yes tracefile=pathtofile\icmp_trace.etl
```

Execute the following command to stop the network capture

```plaintext
netsh trace stop
```

#### Convert .etl to .pcapng <a href="#convert-etl-to-pcapng" id="convert-etl-to-pcapng"></a>

Download etl2pcapng from the [official GitHub repository](https://github.com/microsoft/etl2pcapng)

Execute the following command to convert the .etl file to .pcapng format

```plaintext
etl2pcapng.exe in.etl out.pcapng
```

#### Viewing the PCAP <a href="#viewing-the-pcap" id="viewing-the-pcap"></a>

Use a packet analysis tool such as Wireshark

{% hint style="info" %}
In Wireshark, look for the "Process ID" (PID) information in the packet details. This information is not part of the standard packet headers (like IP or TCP headers) but is provided by the ETW (Event Tracing for Windows) data included in the ETL file. When you load the converted PCAPNG file in Wireshark, you should be able to see additional metadata, including the PID associated with each packet.
{% endhint %}

## Official Manual <a href="#official-manual" id="official-manual"></a>

[https://learn.microsoft.com/en-us/windows-server/networking/technologies/netsh/netsh-contexts](https://learn.microsoft.com/en-us/windows-server/networking/technologies/netsh/netsh-contexts)

## References <a href="#references" id="references"></a>

[https://learn.microsoft.com/en-us/windows-server/networking/technologies/netsh/netsh-contexts](https://learn.microsoft.com/en-us/windows-server/networking/technologies/netsh/netsh-contexts)
