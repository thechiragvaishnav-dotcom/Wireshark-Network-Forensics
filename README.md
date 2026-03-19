# Wireshark-Network-Forensics

* $$\color{red}{\text{Page-1: Capture devices}}$$ --> ![View](https://github.com/thechiragvaishnav-dotcom/Wireshark-Network-Forensics/issues/1#issue-4080175510) 

  ![Alt text for the image](images/images.png)   
  * **1. The Capture Filter Bar** --> ![View](https://github.com/thechiragvaishnav-dotcom/Wireshark-Network-Forensics/issues/2#issue-4080409697)
     * you can start $$\color{orange}{\text{Filtering}}$$ before $$\color{orange}{\text{Capturing packets}}$$
     * | Feature | Capture Filters | Display Filters |
       | :--- | :--- | :--- |
       | When it's applied | Before you start capturing. | During or after the capture. |
       | Syntax |	BPF (Berkeley Packet Filter)	| Wireshark Display Syntax |
       | Primary Purpose	| Save disk space & memory.	| Visually analyze and sort captured data. |
       | Effect on Data |	$$\color{orange}{\text{Permanent.}}$$ Unmatched packets are discarded. |	$$\color{orange}{\text{Temporary.}}$$ Unmatched packets are just hidden. |
       | Example Syntax	| <code>host 192.168.1.5 and port 80</code> |	<code>ip.addr == 192.168.1.5 && tcp.port == 80</code> |

  * **2. 

* $$\color{red}{\text{Page-2: Capturing packets}}$$ --> ![View]() 
