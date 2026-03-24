# Wireshark-Network-Forensics

* $$\color{red}{\text{Page-1: Capture devices}}$$
  
  ![Alt text for the image](images/image1.png)   
  * **1. The Capture Filter Bar:**
 
    ![](images/image2.png)
     * you can start $$\color{orange}{\text{Filtering}}$$ before $$\color{orange}{\text{Capturing packets}}$$
     * | Feature | Capture Filters | Display Filters |
       | :--- | :--- | :--- |
       | When it's applied | Before you start capturing. | During or after the capture. |
       | Syntax |	BPF (Berkeley Packet Filter)	| Wireshark Display Syntax |
       | Primary Purpose	| Save disk space & memory.	| Visually analyze and sort captured data. |
       | Effect on Data |	$$\color{orange}{\text{Permanent.}}$$ Unmatched packets are discarded. |	$$\color{orange}{\text{Temporary.}}$$ Unmatched packets are just hidden. |
       | Example Syntax	| <code>host 192.168.1.5 and port 80</code> |	<code>ip.addr == 192.168.1.5 && tcp.port == 80</code> |

  * **2. NICs (Network Interface Cards):**
 
     ? Which Network Interface Cards are picking up traffic ?
    
     --> This Cards
     ![](images/image3.png)
     * you have to be Connected to the Networks with your Device, that you want to look at.
     * Generally, you are going to look at your Ethernet or Wifi.
     * Double click on, one of this to Open next page.
       
* $$\color{red}{\text{Page-2: Capturing packets}}$$

  ![](images/image4.png)
  * When we double-click, Immediately wireshark starts capturing packets & We can let it go & Capture packets for as long as we like.
  * So, If you're troubleshooting a particular website or Something like that, You wonna to try & Acess that website now while it's capturing.
  * & Then once you think you have enough data, Once enough time has gone by, You can click on $$\color{red}{\text{Red Square Button}}$$ up here at the top left.
  ![](images/image5.jpg)
  * you can see at the very bottom of the screen here, It tells us that it captured  
  ![](images/image6.jpg)
  * 
  

