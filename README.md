# DynamiteLab Traffic Analysis for DDoS Detection

## Overview
This repository contains a project demonstrating hands-on network traffic analysis using DynamiteLab Community (the rebranded successor to PacketTotal) to detect a SYN flood Distributed Denial of Service (DDoS) attack. The project leverages the public PCAP file `SYNFlooding_flag.pcapng` to apply Wireshark-style filters, identify malicious traffic patterns, and document findings.

## Project Details
- **Platform**: DynamiteLab
- **Dataset**: `SYNFlooding_flag.pcapng` (Public Repository PCAP)
- **Date Completed**: April 27, 2025
- **Author**: Michael Ampo
- **Skills Demonstrated**: Network traffic analysis, DDoS detection, Wireshark filter application, documentation

## How to Explore
Since this project was conducted online using DynamiteLab, no local setup is required. However, you can:
1. Visit lab.dynamite.ai and search for `SYNFlooding_flag.pcapng` to replicate the analysis.
2. Use the following filters in the "Search for domain, IP..." bar:
   - `tcp.flags.syn == 1 && tcp.flags.ack == 0` (Detects SYN flood)
   - `http` (Checks for HTTP correlation)
3. Review the provided proof document for detailed findings and screenshots.

## Findings
- **SYN Flood Detection**: Identified over 1,000 SYN packets without ACK responses, indicating a DDoS attack from 57,634 unique IPs.
- **Traffic Volume**: Analyzed 37,669 total packets, with 100% TCP traffic, confirming a high-volume attack.
- **HTTP Analysis**: Minimal HTTP traffic (~50 packets) with no significant correlation to the SYN flood.
- **Risk Assessment**: HIGH - Potential network saturation attempt.
- **MITRE ATT&CK Mapping**: T1499 (Network Denial of Service)

## Installation & Requirements
- No installation needed; project was executed via browser.
- Access to DynamiteLab requires only a web browser (tested on mobile).
- Optional: Familiarity with Wireshark filters for deeper exploration.

## Usage
1. Navigate to lab.dynamite.ai
2. Search for `SYNFlooding_flag.pcapng` and open the PCAP.
3. Apply the provided filters to observe the SYN flood pattern.
4. Document your results (screenshots recommended).

## Proof of Work
- Detailed findings and screenshots are documented in a Google Docs report
- Screenshots include:
  - Filtered packet list showing ~1,200 SYN packets.
  - Flow graph highlighting 100% TCP traffic.

## Contributing
This is an individual educational project. However, contributions or suggestions for enhancing the analysis (e.g., additional filters, PCAPs) are welcome. Please open an issue or submit a pull request with your ideas.

## License
This project is for educational purposes only and is not licensed for commercial use. Feel free to fork and adapt for personal learning.


## Contact
- **Author**: Michael Ampo
- **Email**: imykee85@gmail.con
- **GitHub**: https://github.com/imykee85
- **LinkedIn**: http://linkedin.com/in/michael-ampo-b9181219b

## Project Status
Completed on April 27, 2025, at 12:04 PM GMT. Open for future enhancements.
