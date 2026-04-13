# Wireshark-Network-Forensics

* $$\color{red}{\text{Page-1: Capture devices}}$$

  * Open ==> <code>Wireshark</code>
  
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
  
   * Double-click <code>NICs / Wifi</code>
   
     ![](images/image4.png)
  * When we double-click, Immediately wireshark starts capturing packets & We can let it go & Capture packets for as long as we like.
  * So, If you're troubleshooting a particular website or Something like that, You wonna to try & Acess that website now while it's capturing.
  * & Then once you think you have enough data, Once enough time has gone by, You can click on $$\color{red}{\text{Red Square Button}}$$ up here at the top left.
  ![](images/image5.jpg)

  * you can see at the very bottom of the screen here, It tells us that it captured 433 packets
  ![](images/image6.png)
  If we click the $$\color{red}{\text{Red Square Button,}}$$ it will stop capturing.

  * **? What is a packet ?**
 
    --> Each of the rows that you see on the screen here
    ![](images/image7.png)
    Is a $$\color{orange}{\text{single "Packet"}}$$ of information.

  * Whenever information is transferred over a network, It's transferred via packets.
  * That means that every time you load a webpage, Every time you upload or download something, Packets of information are being transferred between you computer & A web server.
  
* $$\color{red}{\text{Page-3: Bird's eye view}}$$

  * Go inside ==> <code>Statistics / Conversations</code>
  
    ![](images/image8.png)

  * We have some tabs up here, <code>Ethernet . 1</code>, <code>IPv4 . 3</code>, <code>...</code> and so on, To go through the different protocols.

    ![](images/image9.png)
    View of everything going on in wireshark. But, We actually use this screen to start $$\color{orange}{\text{filtering our packets.}}$$

  * Any time you're doing network analysis, It's a good idea to know some of the IP addresses on your network.
  * Settings / Network & internet / Wifi / "your Wifi name"
  * Scroll down to <code>IPv4</code> address = IP address of your PC\

    ![](images/image10.png)\
    & If there's a particular device that you're trying to troubleshoot, It's a good to know maybe the Mac address of that device.
  * So I have my IP address ( <code>10.24.12.20</code> ) & I want to find where it's in this <code>Address A</code>
  * $$\color{red}{\text{right-click}}$$ on your IP address/Apply as Filter/Selected/A <--> Any
    ![](images/image11.png)\
    A is either sending or receiving from any IP address.

* $$\color{red}{\text{Page-4: Right-click filtering}}$$

  * So when I click on this\
    ![](images/image11.png)
    
  * you'll notice that a filter is now automatically put here in the top $$\color{green}{\text{green line}}$$
    ![](images/image12.jpg)

  * because we have click on <code>Port A(column)/46481</code> the filter($$\color{green}{\text{green line}}$$) include the port( <code>&& tcp.port==46481</code> )

    ![](images/image13.jpg)

  * $$\color{red}{\text{you can do that from anywhere in Wireshark}}$$ <code>right-click/Apply as Filter</code>
  
    ![](images/image14.png)

  * also on which column you <code>right-click/Apply as Filter/Sujest a filter as per column on which you click</code>
  
    ![](images/image15.jpg)

  * $$\color{red}{\text{right-click(Single packet) = There's a lot of valuable options from there}}$$

# What to look for ?

  * Generally
  * ex 1:$$\color{red}{\text{Device Not Connecting}}$$
    a device not working on your network, & maybe you can use Wireshark to see if there's any communication at all.
    
  * ex 2:$$\color{red}{\text{Phishing Investigation}}$$
    may be someone at your organization think they have been phished, So you want to reopen the link that they got in the sketchy email while capturing with Wireshark, obviously on a safe machine, to see what information can be gathered.
     
  * ex 3:$$\color{red}{\text{Increase Bandwidth}}$$
    maybe just to see what devices are canstantly communicating on your network to see if you can improve your bandwidth.

  * Wireshark can help with all of these situations, but the filters that you use & the packets that you focus on will be different.
