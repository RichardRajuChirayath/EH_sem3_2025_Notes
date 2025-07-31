<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
</head>
<body>

<h1>🛡️ ASSIGNMENT 20: PERSONAL SECURITY AUDIT USING SHODAN</h1>
<p><strong>Submitted by:</strong> Richard Raju<br />
<strong>Date:</strong> 30/07/2025</p>

<hr />

<h2>1. 🎯 Objective</h2>

  <p>
    The objective of this audit is to evaluate the public exposure of my internet-connected devices by utilizing Shodan, a search engine for discovering internet-facing services and vulnerabilities. By identifying what information and services are accessible from an external perspective, the audit aims to uncover potential security risks and outline effective measures to strengthen the overall security posture of my network.
  </p>
<hr/>

<h2>2. 📖 Introduction</h2>
<p>
  The purpose of this audit is to determine what information about my own internet connection is publicly visible to attackers using Shodan, a search engine for internet-connected devices. Understanding what services and devices are exposed on the public IP helps identify potential vulnerabilities and allows me to take steps to harden the network. The audit follows a personal security perspective to see my network from an attacker's viewpoint.
</p>

<hr />

<h2>3. 🧰 Methodology</h2>
<ul>
  <li>First, I identified my public IP address by visiting trusted websites (e.g., whatismyipaddress.com).</li>
  <li>Then, I visited Shodan.io, a web-based tool that scans the internet-exposed devices and services.</li>
  <li>I searched my public IP on Shodan to check about my IP address.</li>
</ul>

<hr />

<h2>4. 🔍 Findings</h2>
<ul>
  <li>Shodan detected the presence of Distributed Hash Table (DHT) nodes and peer-to-peer (BitTorrent) activity associated with my public IP address. This indicates that certain peer-to-peer applications or services are active and accessible externally.</li>
  <li>No traditional internet-facing services such as HTTP (port 80), SSH (port 22), or FTP (port 21) were found to be exposed on my public IP address.</li>
  <li>The exposure of peer-to-peer activity implies that my device participates in decentralized file-sharing networks, making the IP address visible to external observers within those networks.</li>
  <li>The absence of commonly targeted service ports reflects a secure network configuration, reducing the risk of direct remote attacks via these services.</li>
  <li>While participation in peer-to-peer networks is not inherently a severe vulnerability, it does carry potential privacy concerns and modest exposure to targeted scanning or attacks specifically related to peer-to-peer protocols.</li>
</ul>

<h4>📸 Screenshot:</h4>

<img width="1918" height="935" alt="image" src="https://github.com/user-attachments/assets/5824e0f7-d173-445c-9107-b69b107a6997" />
(IP MASKED)
<hr />

<h2>5. 🛠️ Recommendations to Harden the System</h2>
<p>The following are the recommendations to harden the system:</p>
<ol>
  <li><strong>Review and Restrict Peer-to-Peer/BitTorrent Usage:</strong> Limit or disable BitTorrent and other P2P applications unless absolutely needed, as these services make your IP visible to external networks.</li>
  <li><strong>Enable and Configure Your Firewall:</strong> Ensure that both your router’s firewall and any device-level firewalls are active. Only allow essential ports; block unsolicited incoming traffic by default.</li>
  <li><strong>Disable UPnP (Universal Plug and Play):</strong> Turn off UPnP on your router to prevent applications from automatically opening ports that could expose services without your knowledge.</li>
  <li><strong>Avoid Unnecessary Port Forwarding:</strong> Do not forward ports from your router to your internal devices unless required for specific purposes. Remove or close any port forwarding rules no longer in use.</li>
  <li><strong>Update Firmware and Software Regularly:</strong> Keep your router, IoT devices, operating systems, and any installed software up to date with the latest patches and security updates.</li>
</ol>

<hr />

<h2>6. ✅ Conclusion</h2>
<p>
  Through this audit using Shodan, I confirmed that some services on my public IP address are visible on the internet. While HTTPS interfaces provide encrypted access, the existence of SSH and HTTP interfaces publicly accessible can be a risk if not well secured.
</p>
<p>
  By applying recommended hardening measures—closing unnecessary ports, enforcing strong authentication including MFA, keeping software updated, and restricting remote access—I can significantly reduce my attack surface and make it harder for attackers to compromise my network.
</p>
<p>
  Regularly monitoring my exposure with tools like Shodan provides ongoing insight into what is visible externally and helps address new risks promptly. This proactive approach to security auditing is essential for maintaining a secure network infrastructure in today's threat landscape.
</p>

</body>
</html>
