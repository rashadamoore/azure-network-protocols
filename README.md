<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com/watch?v=Mu_2UnOdVHM)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

<h4><strong>A. Use Network Watcher’s Packet Capture</strong></h4>
<h4><strong>B. Deploy a Jump Box (Proxy VM)</strong></h4>
<h4><strong>C. Install Wireshark Directly on the VM</strong></h4>
<h4><strong>D. Enable NSG Flow Logs</strong></h4>

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h4><strong>Use Network Watcher’s Packet Capture</strong></h4>
<ol><li>Go to <strong>Azure Portal &gt; Network Watcher &gt; Packet Capture</strong>.</li><li>Select the target VM and configure:<ul><li>Protocols (TCP/UDP).</li><li>Capture size and duration.</li></ul></li><li>Start the capture and download the <code>.pcap</code> file.</li><li>Open the <code>.pcap</code> file in Wireshark for analysis.</li></ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h4><strong>Use a Jump Box (Proxy VM)</strong></h4>
<ol><li>Deploy a <strong>Jump Box</strong> in the same VNet as the target VM.</li><li>Install <strong>Wireshark</strong> on the Jump Box.</li><li>Redirect traffic to the Jump Box using:<ul><li>Network Security Groups (NSGs).</li><li>Routing rules.</li></ul></li><li>Capture and analyze traffic in Wireshark on the Jump Box.</li></ol>
</p>
<br />

<p>
  
![Screenshot (27)](https://github.com/user-attachments/assets/0d66622d-efa7-4332-9d21-04eb43cd441d)


</p>
<p>
<h4><strong>Install Wireshark Directly on the VM</strong></h4>
<ol><li>RDP (Windows) or SSH (Linux) into the VM.</li><li>Install Wireshark (Windows) or <code>tcpdump</code> (Linux).</li><li>Start a capture and export the <code>.pcap</code> file to analyze locally.</li></ol>
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h4><strong>Use NSG Flow Logs</strong></h4>
<ol><li>Enable <strong>NSG Flow Logs</strong> in Network Watcher.</li><li>Analyze logs using Azure <strong>Traffic Analytics</strong> for high-level insights.</li></ol>
</p>
<br />
