DEVELOPING A NETWORK TRAFFIC ANALYSIS TOOL
INTODUCTION :
A network traffic analysis tool is a software or hardware solution that monitors and analyses network traffic to help network administrators, security professionals, and developers understand and troubleshoot network behaviour.
This tool can be of assistance in the following areas:
Network troubleshooting: Helping to identify and fix network connectivity problems, identify packet loss, and even troubleshoot performance-related issues. Security monitoring: Help to identify, investigate and respond/alert to potential security elevation problems like malware and unauthorized access, as well as other network-based threats such as denial-of-service (DoS) attacks. Network optimization: Can help additional network performance and latency, overall improving efficiency in a network. Compliance and auditing: being PCI-DSS, HIPAA, and GDPR sellers, monitoring and presenting log sources for publishing and analysing traffic between and decentralized.
OVERVIEW :
The intent behind this project is to create a tool that can assess network data traffic for impending security breaches. We will assess network data traffic using packet sniffing to survey network protocols, and data visualization techniques to describe network traffic behaviour.
Packet Sniffing :
Packet sniffing is an important part of our network traffic analyser. Packet sniffing involves capturing and analysing packets to examine packet transmission and assess security risks. 
How Packet Sniffing Works 
Packet sniffing works by capturing and logging packets as they travel across the network. Packet sniffing can be done using a packet sniffing library like scapy in Python or other programming or scripting-type libraries. 
The general process of packet sniffing is:
Packet Capture: The packet sniffing library captures packets on a noted network interface on a target machine (e.g., eth0)
Packet Analysis: The Packet Captured and is then analysed to get relevant packet information including, source/destination IP address, packet size, timestamp, and protocol. 
Packet Store: The "Packet Analysis" or packet data are stored in memory, database, or file for review for additional analysis. 

Types of Packet Sniffing 
There are two main types of packet sniffing: 
Passive Packet Sniffing: In passive packet sniffing, a user captures packets traveling across the networked without altering the packets or capturing other packets.
Active Packet Sniffing: In active packet sniffing the packet sniffer modifies or injects new packets into the network interchange to assess and extract additional packet sniffing information.
Data Visualization :
Data visualization is a critical component of our network traffic analysis tool. It involves using visual representations to communicate network traffic patterns and identify potential security threats.
Why Data Visualization?
Data visualization is essential for several reasons:
Pattern Identification: Visualizations help identify patterns and trends in network traffic that may indicate security threats.
Anomaly Detection: Visualizations enable the detection of unusual traffic spikes or suspicious packet activity.
Insight Generation: Visualizations provide insights into network traffic patterns, allowing for informed decisions about security measures.
Types of Data Visualization
Some common types of data visualization used in network traffic analysis include:
Line Charts: Used to display trends and patterns in network traffic over time.
Bar Charts: Used to compare packet sizes, protocol distributions, or other categorical data.
Scatter Plots: Used to identify correlations between packet attributes, such as source and destination IP addresses.
Heatmaps: Used to display packet density and identify hotspots in network traffic.
Data Visualization Tools
Some popular data visualization tools used in network traffic analysis include:
Matplotlib: A Python library for creating static and interactive visualizations.
Seaborn: A Python library for creating informative and attractive statistical graphics.
Plotly: A Python library for creating interactive, web-based visualizations.
D3.js: A JavaScript library for creating interactive, web-based visualizations
LIBRARIES USED :
!pip install scapy 
!pip install pandas
!pip install matplotlib
CODE EXPLANATION :
Here I imported the necessary libraries: scapy for packet sniffing, pandas for data manipulation, and matplotlib for data visualization.
Then defined the network interface to sniff (eth0) and the number of packets to capture (100).
And used scapy to sniff packets on the specified interface and stored the captured packets in the packets variable.
Here I created a pandas DataFrame to store packet information, including source IP addresses, destination IP addresses, protocols, and packet lengths.
And looped through the captured packets and extracted the relevant information, storing it in the packet_data list.
Created a pandas DataFrame from the packet_data list and stored it in the df variable.
Here I used the value_counts() method to get the top 10 source IP addresses and their packet counts, storing the result in the top_src_ips variable.
Finally, created a bar chart using matplotlib to visualize the top 10 source IP addresses and their packet counts.
OUTPUT :


NOTEBOOK LINK :
https://colab.research.google.com/drive/10gmghVgu0x1b8FMFzMLui-kAwsZyb-AG?usp=drive_link 
