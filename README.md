Download Link: https://assignmentchef.com/product/solved-lab-4-ospf-lab
<br>
Lab #4 Assignment TDC 363 Page 1TDC 363Lab #4 – OSPF LabASSIGNMENT DOCUMENTNote there is a separate Lab #4 Answers document that accompanies this assignment. You should type all answers into an Answers document and submit this according to instructions.BEFORE you go into the lab you should do the following:1. Read this Assignment Document completely.2. Examine and understand the network diagram.3. Type information about each of your subnets into Table #1: IP Subnet Design in Part 1 of your Answers document.4. Choose an IP address for each interface in your network based on IP addressing requirements. Type these into Table #2: IP Address Plan in Part 2 of your Answers document.Once you have completed these steps, you can implement the network below in one of two ways: (a) you can work on a Pod in the Network Security Lab in room 348, or (b) you can implement and test this network using Cisco Packet Tracer software, starting with file “TDC363-Lab4.pkt”. Either way, you will cable, implement and test the network by following the Network Implementation and Testing instructions below, answering questions and pasting screenshots into the Answers Document when directed to do so.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/770.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/770.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>

Lab #4 Network DiagramLab #4 Assignment TDC 363 Page 2IP Addressing RequirementsYou will use the following IP subnets for your IP addressing. ** The value of &lt;SN&gt; in each IP address should be replaced by your Student Number from the table at the end of the Lab #2 assignment. **• Subnet A – 10.10.&lt;SN&gt;.0/24Interfaces on Subnet A: Host #1, R1 Fa0/0.10The Host #1 IP address must be 10.10.&lt;SN&gt;.&lt;SN&gt;• Subnet B – 172.30.5.0/28Interfaces on Subnet B: R1 Fa0/0.20, F4 Fa0/0• Subnet C – 172.30.5.16/28Interfaces on Subnet C: R3 Fa0/0, R2 Fa0/0.20• Subnet D – 20.20.&lt;SN&gt;.0/24Interfaces on Subnet D: Host #2, R2 Fa0/0.10The Host #2 IP address must be 20.20.&lt;SN&gt;.&lt;SN&gt;• Link 1 – 200.0.0.4/30Interfaces on Link 1: R1 S0/2/0, R2 S0/2/0• Link 2 – 200.0.0.8/30Interfaces on Link 2: R3 S0/2/0, R4 S0/2/0Router interfaces should always be assigned either the first or second valid host IP in their subnet. Go fill out Table #1 and Table #2 in your Answers document.Network Implementation and TestingNow you can either (a) implement the network on a Pod in the Network Security lab – room 348 OR (b) use Packet Tracer software with the file “TDC363-Lab4.pkt” from D2L. TDC 363 students: Remember that at least 1 lab in this course must be done in room 348.1. Implement the network shown in the diagram by:a. Set hostname on each switch and router to an appropriate name followed by your initials (like “R1-GB”).b. Create VLAN #10 (Subnet A) and VLAN #20 (Subnet B) on Switch 1. Assign the switch port connecting to Host #1 to VLAN #10 and the switch port connecting to R4 Fa0/0 is on VLAN #20. The switch port connecting to R1 Fa0/0 is a trunk port.c. Use Router on a Stick to create subinterfaces Fa0/0.10 and Fa0/0.20 for VLAN #10 and #20 on router R1.d. Create VLAN #10 (Subnet D) and VLAN #20 (Subnet C) on Switch 3. Assign the switch port connecting to Host #2 to VLAN #10 and the switch port connecting to R3 Fa0/0 is on VLAN #20. The switch port connecting to R2 Fa0/0 is a trunk port.e. Use Router on a Stick to create subinterfaces Fa0/0.10 and Fa0/0.20 for VLAN #10 and #20 on router R2.f. Connect all cables.g. Configure all interface IPs on hosts and routers. Be sure to configure clock rate on DCE ends.h. Execute “show ip int brief” on each router to make sure that all interfaces have correct IP and mask assigned.i. Make sure you can successfully ping from each host to its default gateway.Lab #4 Assignment TDC 363 Page 3j. Make sure you can ping from each router to each of its 1-hop neighbor routers.k. Execute a “show ip route” on each router and make sure that each of its directly connected subnets is shown in the routing table.2. Configure OSPF process #20 on each of the 4 routers as follows:a. On each router, configure router ospf 20 and then:i. Set the router-id value on each router as follows:1. R1 router-id = 60.0.0.12. R2 router-id = 60.0.0.23. R3 router-id = 60.0.0.34. R4 router-id = 60.0.0.4ii. Configure enough network statements on each router so that all connected subnets are included in routing updates.iii. Configure the following interfaces as passive interfaces: Fa0/0.10 on R1, Fa0/0.10 on R2.b. Do a show ip protocol on each router to make sure that OSPF is active, and the correct IP subnets are being advertised.c. Do not configure anything else in OSPF at this time.3. Now complete Part 3.1 in your Answers.4. Now you will set the bandwidth values for each serial interface to match their clock rates as follows:a. On routers R1 and R2, go into interface configuration mode on interface S0/2/0 and execute bandwidth 2000, which sets the bandwidth to 2000 Kbps (or 2 Mbps) as shown for Link 1 on the network diagram.b. Similarly, on routers R3, and R4, execute bandwidth 4000 on the S0/2/0 interfaces so they match the 4 Mbps rate shown for Link 2 on the diagram.c. Execute show interface S0/2/0 on all 4 routers to make sure that the bandwidth values are set correctly.5. Now complete Part 3.2 in your Answers.6. You are finished.

<p style="text-align: center;">TDC 363

<p style="text-align: center;">Lab #4 – OSPF Lab

<p style="text-align: center;"><strong>ANSWERS DOCUMENT</strong>

<p style="text-align: center;"><strong> </strong>

<p style="text-align: center;"><strong>Your Name: </strong>




You should read the Lab #4 Assignment Document before reading this one.  You can type your answers into this document or create a separate one.  When complete, save answers file as PDF and submit for your Lab #4 assignment on D2L.

<ol>

 <li><strong>IP Subnet Design</strong></li>

</ol>

Enter the Subnet information for all lab subnets into Table #1 below.

<strong>Table #1: IP Subnet Design</strong>




<table width="541">

 <tbody>

  <tr>

   <td width="87"><strong>Subnet Name</strong></td>

   <td width="113"><strong>Subnet Network Address</strong></td>

   <td width="72"><strong>Prefix Length</strong><strong>(/n)</strong></td>

   <td width="66"><strong>Size</strong><strong>= 2<sup>[32-n]</sup></strong></td>

   <td width="102"><strong>First Valid Host IP</strong></td>

   <td width="102"><strong>Last Valid Host IP</strong></td>

  </tr>

  <tr>

   <td width="87">Subnet A</td>

   <td width="113"></td>

   <td width="72"></td>

   <td width="66"></td>

   <td width="102"></td>

   <td width="102"></td>

  </tr>

  <tr>

   <td width="87">Subnet B</td>

   <td width="113"></td>

   <td width="72"></td>

   <td width="66"></td>

   <td width="102"></td>

   <td width="102"></td>

  </tr>

  <tr>

   <td width="87">Subnet C</td>

   <td width="113"></td>

   <td width="72"></td>

   <td width="66"></td>

   <td width="102"></td>

   <td width="102"></td>

  </tr>

  <tr>

   <td width="87">Subnet D</td>

   <td width="113"></td>

   <td width="72"></td>

   <td width="66"></td>

   <td width="102"></td>

   <td width="102"></td>

  </tr>

  <tr>

   <td width="87">Link 1</td>

   <td width="113"></td>

   <td width="72"></td>

   <td width="66"></td>

   <td width="102"></td>

   <td width="102"></td>

  </tr>

  <tr>

   <td width="87">Link 2</td>

   <td width="113"></td>

   <td width="72"></td>

   <td width="66"></td>

   <td width="102"></td>

   <td width="102"></td>

  </tr>

 </tbody>

</table>







<ol start="2">

 <li><strong>IP Address Plan</strong></li>

</ol>




Now, based on your IP Subnet Design above and the network diagram, assign a specific IP address and subnet mask to each interface and enter it into the table below.




<strong>Table #2: IP Address Plan</strong>




<table width="421">

 <tbody>

  <tr>

   <td width="79"><strong>Device</strong></td>

   <td width="84"><strong>Interface</strong></td>

   <td width="132"><strong>IP Address</strong></td>

   <td width="126"><strong>Mask</strong></td>

  </tr>

  <tr>

   <td width="79">R1</td>

   <td width="84">Fa0/0.10</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">R1</td>

   <td width="84">Fa0/0.20</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">R1</td>

   <td width="84">S0/2/0</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">R2</td>

   <td width="84">Fa0/0.10</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">R2</td>

   <td width="84">Fa0/0.20</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">R2</td>

   <td width="84">S0/2/0</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">R3</td>

   <td width="84">Fa0/0</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">R3</td>

   <td width="84">S0/2/0</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">R4</td>

   <td width="84">Fa0/0</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">R4</td>

   <td width="84">S0/2/0</td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">Host #1</td>

   <td width="84"></td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

  <tr>

   <td width="79">Host #2</td>

   <td width="84"></td>

   <td width="132"></td>

   <td width="126"></td>

  </tr>

 </tbody>

</table>




<ol start="3">

 <li><strong>Lab Implementation</strong></li>

</ol>




Now, follow directions in the Lab #4 Assignment document to implement the lab network.  Answer questions in each part below only when instructed to do so in the assignment document.

Note: when you are asked for a screenshot, make sure that the <u>complete output</u> from the specified command is showing in the window.  Resize the window if some of the output scrolled off the top so you can see it all.  You will also lose points if any screenshots have “—More—“ at the bottom, indicating that all the output is not shown.

<h1>Part 3.1:</h1>

<ol>

 <li>On Host #1, ping to Host #2. It should succeed.  Paste results here.</li>

 <li>On Host #1, execute <strong>tracert</strong> to Host #2. Paste results here.

  <ol>

   <li>For each IP address in the tracert output, tell me

    <ol>

     <li>Which IP subnet (either A, B, C, D, Link1 or Link2) contains this IP address.</li>

     <li>Which device (either Host1, Host2, R1, R2, R3 or R4) has an interface with this IP address.</li>

    </ol></li>

   <li>On Switch 1, execute <strong>show vlan brief</strong> and paste results here.</li>

   <li>On Router R1, execute <strong>show ip route</strong> and paste results here.

    <ol>

     <li>What is the OSPF metric value in this routing table for Subnet D? This is the OSPF path cost from router R1 to Subnet D.</li>

    </ol></li>

   <li>What is the OSPF Link Cost for each of these subnets?

    <ol>

     <li>Link 1</li>

     <li>Subnet D</li>

    </ol></li>

   <li>On Router R1, execute <strong>show ip protocol</strong> and paste results here.</li>

   <li>On Router R1, execute <strong>show ip ospf neighbor</strong> and paste results here.

    <ol>

     <li>Which routers (out of R2, R3 and R4) are OSPF neighbors with R1?</li>

    </ol></li>

   <li>Return to assignment document before answering questions in Part 3.2.</li>

  </ol></li>

</ol>

<h1>Part 3.2: (answer after setting interface bandwidths)</h1>

<ol start="9">

 <li>On Host #1, ping to Host #2. It should succeed.  Paste results here.</li>

 <li>On router R3, execute <strong>show interface s0/2/0</strong> and paste results here.</li>

 <li>On Host #1, execute <strong>tracert</strong> to Host #2. Paste results here.

  <ol>

   <li>For each IP address in the tracert output, tell me

    <ol>

     <li>Which IP subnet (either A, B, C, D, Link1 or Link2) contains this IP address.</li>

     <li>Which device (either Host1, Host2, R1, R2, R3 or R4) has an interface with this IP address.</li>

    </ol></li>

   <li>Does the tracert from question #11 show the same path as the tracert from question #2? If not, what is the difference and why has it changed?</li>

   <li>On Router R1, execute <strong>show ip route</strong> and paste results here.

    <ol>

     <li>What is the OSPF metric value (path cost) in this routing table for Subnet D?</li>

    </ol></li>

   <li>Execute <strong>show ip route</strong> on R2, R3 and R4 and paste results here.</li>

  </ol></li>

</ol>

Convert this file to PDF format, review the resulting file to ensure that all answers and screenshots are readable, and submit on D2L.

That’s it for Lab #4!!