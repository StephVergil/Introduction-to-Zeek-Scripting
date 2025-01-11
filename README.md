# Introduction to Zeek Scripting

This project explores the fundamentals of Zeek scripting for processing and analyzing network traffic. Through hands-on exercises, the lab demonstrates how to use Zeek scripts for monitoring UDP and TCP traffic, customizing log streams, and organizing log files to improve network traffic analysis workflows. The objectives include starting and configuring Zeek, executing Zeek scripts for traffic analysis, modifying log streams, and organizing logs for specific protocols or events.

### Tools Used
**Zeek**: For traffic monitoring, analysis, and log generation.  
**Sample PCAP Files**: Test data for script execution.  
**Linux Shell Scripts**: For directory cleanup and script automation.

### Key Steps
1. **Starting a New Instance of Zeek**: Use the following command to initialize Zeek:  
   `cd $ZEEK_INSTALL/bin && sudo ./zeekctl start`
2. **Executing Zeek Scripts**:
   - **UDP Traffic Analysis**:
     - Navigate to the **Lab-Scripts** directory: `cd ~/Zeek-Labs/Lab-Scripts/`
     - Process a packet capture file using the UDP script:  
       `zeek –C –r ../Sample-PCAP/smallFlows.pcap ../Lab-Scripts/lab6_sec2-2.zeek`
   - **TCP Traffic Analysis**:
     - Display the content of the TCP Zeek script:  
       `nl ../Lab-Scripts/lab6_sec2-3.zeek`
     - Process a packet capture file using the TCP script:  
       `zeek –C -r ../Sample-PCAP/smallFlows.pcap ../Lab-Scripts/lab6_sec2-3.zeek`
3. **Modifying Zeek Log Streams**:
   - **Renaming Logs**:
     - Display the content of the renaming script:  
       `nl ../Lab-Scripts/lab6_sec3-1.zeek`
     - Process a PCAP file and generate updated logs:  
       `zeek –C -r ../Sample-PCAP/smallFlows.pcap ../Lab-Scripts/lab6_sec3-1.zeek`
   - **Creating Protocol-Specific Logs**:
     - Display the content of the protocol-specific log script:  
       `nl ../Lab-Scripts/lab6_sec3-2.zeek`
     - Generate a new log file for HTTP traffic:  
       `zeek –C -r ../Sample-PCAP/smallFlows.pcap ../Lab-Scripts/lab6_sec3-2.zeek`
4. **Cleanup and Shutdown**:
   - Use the cleanup script to remove temporary log files:  
     `./../Lab-Scripts/lab_clean.sh`
   - Stop Zeek after completing the lab:  
     `cd $ZEEK_INSTALL/bin && sudo ./zeekctl stop`

### Results
The analysis demonstrated the functionality of UDP and TCP Zeek scripts to capture specific traffic patterns and log details. Logs were renamed and segmented to separate HTTP traffic from general connection logs, improving the organization and clarity of network analysis results.

### Project Resources
- **Project Link**: [Introduction to Zeek Scripting](https://github.com/StephVergil/Introduction-to-Zeek-Scripting/blob/main/VNetLab3%20Lab06.docx.pdf)
- [Zeek Documentation](https://docs.zeek.org/)
- [PCAP Samples](https://wiki.wireshark.org/SampleCaptures)

### Conclusion
This lab demonstrates the versatility of Zeek scripting for analyzing and organizing network traffic logs. Through custom scripts, users can effectively segment and manage log files, making them highly tailored for specific protocols or events.

### Disclaimer
This project was conducted in a controlled environment. Unauthorized use of these techniques or tools outside such an environment may violate ethical guidelines and legal regulations.
