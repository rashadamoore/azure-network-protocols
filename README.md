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

<div data-message-author-role="assistant" data-message-id="0da90e9d-12b9-4e9b-9782-6402cab48b46" dir="auto" class="min-h-8 text-message flex w-full flex-col items-end gap-2 whitespace-normal break-words [.text-message+&amp;]:mt-5" data-message-model-slug="gpt-4o"><div class="flex w-full flex-col gap-1 empty:hidden first:pt-[3px]"><div class="markdown prose w-full break-words dark:prose-invert light"><p></p><hr><h3><strong>1. Prerequisites</strong></h3><ul><li>Install <strong>Wireshark</strong> on your local machine.</li><li>Ensure <strong>Azure Network Watcher</strong> is enabled for the VM's region.</li><li>Have administrative access to Azure and your VM.</li></ul><hr><h3><strong>2. Monitoring Methods</strong></h3><h4><strong>A. Use Network Watcher’s Packet Capture</strong></h4><ol><li>Go to <strong>Azure Portal &gt; Network Watcher &gt; Packet Capture</strong>.</li><li>Select the target VM and configure:<ul><li>Protocols (TCP/UDP).</li><li>Capture size and duration.</li></ul></li><li>Start the capture and download the <code>.pcap</code> file.</li><li>Open the <code>.pcap</code> file in Wireshark for analysis.</li></ol><hr><h4><strong>B. Use a Jump Box (Proxy VM)</strong></h4><ol><li>Deploy a <strong>Jump Box</strong> in the same VNet as the target VM.</li><li>Install <strong>Wireshark</strong> on the Jump Box.</li><li>Redirect traffic to the Jump Box using:<ul><li>Network Security Groups (NSGs).</li><li>Routing rules.</li></ul></li><li>Capture and analyze traffic in Wireshark on the Jump Box.</li></ol><hr><h4><strong>C. Install Wireshark Directly on the VM</strong></h4><ol><li>RDP (Windows) or SSH (Linux) into the VM.</li><li>Install Wireshark (Windows) or <code>tcpdump</code> (Linux).</li><li>Start a capture and export the <code>.pcap</code> file to analyze locally.</li></ol><hr><h4><strong>D. Use NSG Flow Logs</strong></h4><ol><li>Enable <strong>NSG Flow Logs</strong> in Network Watcher.</li><li>Analyze logs using Azure <strong>Traffic Analytics</strong> for high-level insights.</li></ol><hr><h3><strong></p></div></div></div>

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
