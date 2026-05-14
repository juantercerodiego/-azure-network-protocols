<p align="center">
<img width="1280" height="550" alt="1747463229673" src="https://github.com/user-attachments/assets/52dc0029-286b-4560-8c9b-3ee4f8305e46" />
</p>

<h1>Network Security Groups (NSGs) and Inspecting Network Traffic</h1>
This lab demonstrates how to monitor and control the flow of data within a cloud environment. I used Wireshark to see live traffic and configured digital firewalls (NSGs) to manage which connections are allowed.<br />




<h2>Environments and Technologies Used</h2>

- **Microsoft Azure** (Virtual Machines)
- **Remote Desktop** (RDP)
- **Network Security Groups** (Cloud Firewalls)
- **Wireshark** (Network Protocol Analyzer)

<h2>Operating Systems Used </h2>

- **Unbuntu Server** (Linux)
- **Windows 11**

<h2>High-Level Deployment and Configuration Steps</h2>

- **Step 1:** Setting up the "Microscope" (Wireshark)
- **Step 2:** Watching the "Ping" (ICMP Traffic)
- **Step 3:** Slamming the Door (Configuring NSGs)
- **Step 4:** Watching the Door Open (Allowing Traffic)
<h2>Deployment and Configuration Steps</h2>
<h2>Step 1: Setting up the "Microscope" (Wireshark)</h2>

<p>
<img width="1001" height="550" alt="step 1" src="https://github.com/user-attachments/assets/5d0d973a-0b01-443d-a542-1eaca247c96a" />




</p>
<p>
To see what’s happening on the network, I installed Wireshark on my Windows workstation. Think of this as a digital microscope—it allows me to capture and inspect every "packet" of data entering or leaving the computer in real-time
</p>
<br />
<h2>Step 2: Watching the "Ping" (ICMP Traffic) </h2>
<p>
<img width="783" height="500" alt="Screenshot 2026-05-13 115239" src="https://github.com/user-attachments/assets/269985ec-2a11-4ad2-a58f-f8af5521ac7c" />

</p>
<p>
I started by "pinging" a Linux server from my Windows computer. In Wireshark, I could see the ICMP traffic—the digital equivalent of shouting "Are you there?" and hearing a "Yes, I am!" back. This confirms the two machines can talk to each other.
</p>
<br />
<h2>Step 3: Slamming the Door (Configuring NSGs)</h2>
<p>
<img width="808" height="548" alt="Screenshot 2026-05-13 120309" src="https://github.com/user-attachments/assets/5f565de1-eace-4bd0-bdf0-4ee7670fff02" />



</p>
<p>
Now for the security part. I went into the Azure Portal and slammed the gate shut by blocking ICMP traffic. Immediately, the "pings" stopped working and started timing out. This shows how an admin can instantly cut off specific communication to protect a server.
</p>
<br />
<h2>Step 4: Watching the Door Open (Allowing Traffic)</h2>
<p>
<img width="623" height="570" alt="Screenshot 2026-05-13 123209" src="https://github.com/user-attachments/assets/f2ffb586-702b-463e-9161-3ca84411c913" />



</p>
<p>
To finish the test, I removed the block. As soon as the rule was changed, the traffic started flowing again. This lab proves that I can control exactly who is allowed into my network and verify it using live monitoring tools.
</p>
<br />

