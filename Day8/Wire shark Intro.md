# Wireshark introduction
Wireshark is a network analyzer that allows you to see what is going on with your network. Wireshark allows you to dissect network packets at a microscopic level, including detailed information on individual packets.

Wireshark was first made available in 1998. Back then, it was considered Ethereal. Wireshark is compatible with all major operating systems. Most businesses and government agencies also use Wireshark as a primary network analyzer.

Wireshark is now fully open-source, thanks to the global network engineering ecosystem. While most security systems are command-line-based, Wireshark has an excellent user interface.

#OSI Model

The Open Systems Interconnection (OSI) paradigm standardises the manner in which two or more computers communicate with one another. The OSI Model classifies network architecture into seven layers:

Application, Presentation, Session, Transport, Network, Datalink, and Physical.


Here is what each layer does:


**OSI Model Layers**
If you want to read more about the OSI model, check out this [comprehensive essay](https://dev.to/vishwasnarayan5/cyber-secutiry-3c8a).

# Packets

Now that you understand the OSI model, let's look at network packets. When data is transmitted from one device to another, it is divided into smaller units known as packets.

When you download a file from the internet, the data is transmitted as packets from the server. Your machine reassembles these packets to send you the original file.

#IPV4 Packet

A packet can contain the following data:
*source and destination IP addresses
protocol
* source and destination ports
* Data
* Length, flags, TTL, etc.
* protocol

Each packet includes important information about the devices involved in the packet transfer. Thousands, if not millions, of these data packets are transmitted between the source and destination devices for each data connection.

You can now understand the significance of Wireshark. Wireshark allows you to catch and search each of these packets for details.

A network engineer's equivalent of a biologist's microscope is Wireshark. Wireshark allows you to ‘listen' to a live network (after connecting to it), record, and inspect packets on the move.

You may use Wireshark as a network engineer or ethical hacker to debug and protect the networks. As a bad guy (which I do not recommend), you can sniff network packets and grab information such as credit card purchases.

This is why connecting to a public network such as Starbucks and doing financial transfers or accessing private data is risky. Even though HTTPS sites can encrypt the packets, they are still readable across the network.

If someone is determined enough, they will be able to break it.
Wireshark Fundamentals
Let's take a look at how you can use Wireshark. Wireshark can be downloaded and installed from this page.
Unlike other penetration testing software, Wireshark provides an excellent graphical user interface. This is how Wireshark appears when you launch it.

Wireshark displays a list of the networks to which you are linked, and you can choose one of them to begin listening to the network.

**Wireshark UI**
There are three panes in Wireshark.
Packet List Pane

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/s1goim6suk41ewj9xuk0.png)

The listing of packages in Wireshark is by default displayed using the following columns:
Package Number
Time
Source IP (Your device IP when sending packages, see the following tutorial if you’re unfamiliar with IP’s: https://youtu.be/oieIGwUPaKE)
Destination IP (Your device IP when receiving Packages)
Network Protocol used (Typically TCP or UDP, see the following video if you’re in doubt of the difference between these: https://youtu.be/0-MldfyhIuo)
Package Length
Info (Information not listed in one of the above columns)


**Packet List Pane**

This window shows the collected packets. Each line represents a separate packet, which you can click on and examine in greater depth using the other two panes.

**Packet Details Pane**

Selecting a packet allows you to examine the packet information in greater depth using the Packet Details pane. It shows information such as IP addresses, ports, and other data from the packet.

**Packet Bytes Pane**

This pane displays the raw data of the chosen packet in bytes. The data is presented as a hex dump, which is binary data in hexadecimal format.

**Filters**

Filters in Wireshark assist you in narrowing down the kind of data you are searching for. Filters are classified into two types: capture filters and display filters.

**Traffic Filtering**

Wireshark supports filters based on a broad range of criteria to reduce the amount of information shown at the start. The filters can be applied directly in the search bar of the Wireshark programme, as seen below with a TCP protocol filter.

**Capture Filter**

Until beginning to evaluate a network, you should apply a catch filter. When a catch filter is set, it only catches packets that fit the capture filter.

For eg, if you only need to listen to the packets being sent and received from an IP address, you can set a capture filter as follows.
host 192.168.0.1
Once you set a capture filter, you cannot change it till the current capture session is completed.

**Display Filters**

To grab packets, display filters are used. For eg, if you just want to see requests coming from a certain IP address, you can do so. you can apply a display filter as follows:
ip.src==192.168.0.1

Show filters can be modified on the fly when they are added to collected data.
In a nutshell, capture filters allow you to filter the traffic, while view filters add certain filters to the captured packets. Wireshark is good for debugging because it can catch hundreds of packets on a busy network.

**Wireshark's Main Features**

Now that you've mastered the fundamentals of Wireshark, let's take a look at some main features. You can do it with Wireshark.

Recognize network security risks and malicious activities
Debug dynamic networks by observing network traffic.
Filter traffic according to protocols, ports, and other criteria.
Capture packets and store them in a **Pcap** file for later review.
To improve research, apply coloring rules to the packet list.
Captured data can be exported to an XML, CSV, or plain text format.


**Conclusion**

Every year, Wireshark is ranked in the top ten network security software. Wireshark is simple to understand and use thanks to its simple but efficient user interface. It is an important weapon in the arsenal of any penetration tester.
