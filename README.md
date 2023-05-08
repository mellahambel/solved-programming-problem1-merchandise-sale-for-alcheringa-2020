Download Link: https://assignmentchef.com/product/solved-programming-problem1-merchandise-sale-for-alcheringa-2020
<br>
<h1></h1>

The organizers of Alcheringa 2020 are planning to sell its merchandise. Write a program in java to assist the merchandise sale by collecting and processing orders. Consider the following for the system.

<ol>

 <li>The merchandise includes T shirts (of sizes S, M and L) and caps.</li>

 <li>A student can order only one item (either T shirt or cap) in a single order, but in any quantity.</li>

</ol>

<ul>

 <li>To simulate multiple orders at the same time, consider taking input in batch and process them together.</li>

</ul>

<ol>

 <li>Use the concept of concurrency and multithreading to process the orders of the batch concurrently.</li>

 <li>Display the inventory list to the user before the order.</li>

 <li>An order is successful if sufficient quantity of the item is available, otherwise it is failed.</li>

</ol>

<ul>

 <li>Use synchronization to avoid inconsistency in the inventory data.</li>

 <li>Once the order is completed (successful or failed), the status is displayed to the user immediately along with the new inventory list.</li>

</ul>

<strong><em>Sample Input: </em></strong>

Number of students ordering:  3

<ul>

 <li>S 5</li>

 <li>C 3</li>

 <li>M 2</li>

</ul>

[Sà T shirt small, Mà T shirt medium, Là T shirt large, Cà Cap]

<strong><em>Output: </em></strong>

Inventory —

<table width="532">

 <tbody>

  <tr>

   <td width="133">S</td>

   <td width="133">M</td>

   <td width="133">L</td>

   <td width="133">C</td>

  </tr>

  <tr>

   <td width="133">4</td>

   <td width="133">5</td>

   <td width="133">2</td>

   <td width="133">4</td>

  </tr>

 </tbody>

</table>




Order 2 is successful

Inventory —

<table width="532">

 <tbody>

  <tr>

   <td width="133">S</td>

   <td width="133">M</td>

   <td width="133">L</td>

   <td width="133">C</td>

  </tr>

  <tr>

   <td width="133">4</td>

   <td width="133">5</td>

   <td width="133">2</td>

   <td width="133">1</td>

  </tr>

 </tbody>

</table>




Order 1 failed

Inventory —

<table width="532">

 <tbody>

  <tr>

   <td width="133">S</td>

   <td width="133">M</td>

   <td width="133">L</td>

   <td width="133">C</td>

  </tr>

  <tr>

   <td width="133">4</td>

   <td width="133">5</td>

   <td width="133">2</td>

   <td width="133">4</td>

  </tr>

 </tbody>

</table>




Order 3 successful

Inventory —

<table width="532">

 <tbody>

  <tr>

   <td width="133">S</td>

   <td width="133">M</td>

   <td width="133">L</td>

   <td width="133">C</td>

  </tr>

  <tr>

   <td width="133">4</td>

   <td width="133">3</td>

   <td width="133">2</td>

   <td width="133">4</td>

  </tr>

 </tbody>

</table>




Write a brief report on the following:

 Specify the synchronization technique that you used in the program. Explain your implementation using code snippets.




<h1>Problem 2: Cold Drink Manufacturing</h1>




A cold drink manufacturing factory has a unit which takes care of packaging and sealing the bottles. The arrangement of the sub-units (packaging and sealing) is shown in the above figure. Consider the following points:

<ol>

 <li>The packaging unit wraps a plastic cover to the bottle and the sealing unit seals the bottle with a cap</li>

 <li>Both the above units take the bottles from the unfinished tray (tray containing bottles which are neither packaged nor sealed)</li>

</ol>

<ul>

 <li>The packaging unit receives two types of bottles B1 and B2. There are two trays from which bottles are supplied to packaging unit. Each tray contains only one type of bottle</li>

</ul>

<ol>

 <li>The tray which carries bottles of type B1 has a capacity of two and the tray which carries bottles of type B2 has a capacity of three.</li>

 <li>The packaging unit identifies and chooses appropriate package for the bottle. This unit can pack one bottle at a time.</li>

 <li>The sealing unit is used to seal a bottle irrespective of its type. It has a buffer tray of size two. It can accommodate both types of bottle.</li>

</ol>

<ul>

 <li>The order in which processing can occur between the above two units is random. The bottles are sent to the godown once the packaging and sealing are over.</li>

 <li>The priority of the trays containing bottles is higher than that of the unfinished tray.</li>

</ul>

<ol>

 <li>The number of bottles processed in each unit and those in the godown is stored in the database.</li>

 <li>The program should be written in such a way that the packaging and sealing units should incur minimum idle time.</li>

 <li>The time to package a bottle takes 2 sec, time to seal a bottle take 3 sec. Neglect all other times used for transferring the bottle from one unit to another.</li>

</ol>

<ul>

 <li>Initially, different types of bottles will be fed into the packaging and sealing units from the unfinished tray.</li>

 <li>Bottles will be fed into the packaging unit from the unfinished tray in an alternative manner (if current input is B1 next input will be B2). Similar will be the case for the sealing unit.</li>

 <li>The input to the packaging unit from the B1 and B2 tray is alternative in nature. Initially, the priority of B1 is higher.</li>

</ul>




Write a java program which will generate the status of the bottles at a particular time.

<em>If synchronization is required, use a synchronization technique different from the one you used in Problem 1. </em>




<strong><em>Sample Input/Output: </em></strong>

Input: &lt;No. of bottle type B1, No. of bottle type B2, Time duration for observation (in sec.)&gt;           Eg. 50, 50, 10 Output:

<table width="258">

 <tbody>

  <tr>

   <td width="90"><strong>Bottle Type </strong></td>

   <td width="96"><strong>Status </strong></td>

   <td width="72"><strong>Count </strong></td>

  </tr>

  <tr>

   <td width="90">B1</td>

   <td width="96">Packaged</td>

   <td width="72">2</td>

  </tr>

  <tr>

   <td width="90">B1</td>

   <td width="96">Sealed</td>

   <td width="72">1</td>

  </tr>

  <tr>

   <td width="90">B1</td>

   <td width="96">In Godown</td>

   <td width="72">1</td>

  </tr>

  <tr>

   <td width="90">B2</td>

   <td width="96">Packaged</td>

   <td width="72">3</td>

  </tr>

  <tr>

   <td width="90">B2</td>

   <td width="96">Sealed</td>

   <td width="72">2</td>

  </tr>

  <tr>

   <td width="90">B2</td>

   <td width="96">In Godown</td>

   <td width="72">2</td>

  </tr>

 </tbody>

</table>




Write a brief report on the following:

<ul>

 <li>Discuss the importance of concurrent programming here.</li>

 <li>Using code snippets describe how you used the concurrency and synchronization in your program.</li>

 <li>How would the program be affected if synchronization is not used? Discuss</li>

</ul>

<strong> </strong>

<strong>   </strong>

<h1>       Problem 3: Automatic Traffic Light System</h1>

To assure the road safety in the campus, the IIT Guwahati administration has decided to install an automatic traffic light system in the T junction near old SAC.

<ol>

 <li>A) Write a program in java to simulate the system considering the following:</li>

</ol>

<ol>

 <li>There are three traffic lights T1,T2 and T3</li>

 <li>T1 is for vehicles moving from South to East; T2 is for vehicles moving from West to</li>

</ol>

South; T3 is for vehicles moving from East to West iii.         Vehicles moving from South to West, East to South, and West to East can always move freely without any signal

<ol>

 <li>If any of the traffic light is green, the other two must be red (eg. if T1 is green, T2 and T3 must be red)</li>

 <li>Each traffic light turns green for 60 seconds only and one vehicle takes 6 seconds to pass</li>

 <li>The traffic lights gets their turn in round robin manner</li>

</ol>

<ul>

 <li>User gives the input as (source direction, destination direction) for example (North, South). The system automatically assigns a number and the timestamp to the vehicle and process accordingly</li>

 <li>The program finds out weather to pass a vehicle or keep it waiting (keep an option to show the status of the vehicles to the user at any instant of time)</li>

</ul>

<em>If you think synchronization is needed for the program, use a synchronization technique other than the one/ones you used in Problem 1 and Problem 2. </em>

<ol>

 <li>B) Using java Swing package to create the GUI to show the simulation of the traffic light system</li>

</ol>

<strong>Sample Input/Output </strong>

<em>Input</em>: East to West




<em>Output</em>:

Vehicle: 21   Wait




[For status] <em>Output</em>:




<table width="313">

 <tbody>

  <tr>

   <td width="131">Traffic Light</td>

   <td width="121">Status</td>

   <td width="61">Time</td>

  </tr>

  <tr>

   <td width="131">T1</td>

   <td width="121">Red</td>

   <td width="61">—</td>

  </tr>

  <tr>

   <td width="131">T2</td>

   <td width="121">Green</td>

   <td width="61">15</td>

  </tr>

  <tr>

   <td width="131">T3</td>

   <td width="121">Red</td>

   <td width="61">—</td>

  </tr>

 </tbody>

</table>




<table width="601">

 <tbody>

  <tr>

   <td width="123">Vehicle</td>

   <td width="113">Source</td>

   <td width="113">Destination</td>

   <td width="119">Status</td>

   <td width="134">Remaining Time</td>

  </tr>

  <tr>

   <td width="123">21</td>

   <td width="113">E</td>

   <td width="113">W</td>

   <td width="119">Wait</td>

   <td width="134">45</td>

  </tr>

  <tr>

   <td width="123">25</td>

   <td width="113">W</td>

   <td width="113">S</td>

   <td width="119">Pass</td>

   <td width="134">—</td>

  </tr>

  <tr>

   <td width="123">27</td>

   <td width="113">S</td>

   <td width="113">W</td>

   <td width="119">Pass</td>

   <td width="134">—</td>

  </tr>

  <tr>

   <td width="123">23</td>

   <td width="113">E</td>

   <td width="113">W</td>

   <td width="119">Wait</td>

   <td width="134">51</td>

  </tr>

  <tr>

   <td width="123">19</td>

   <td width="113">S</td>

   <td width="113">E</td>

   <td width="119">Wait</td>

   <td width="134">105</td>

  </tr>

 </tbody>

</table>




Write a brief report on the following:

<ul>

 <li>Do you think the concept of concurrency is applicable while implementing the program? If yes, why? Explain using code snippets</li>

 <li>Did you use synchronization in the problem? If yes, explain with code snippets</li>

 <li>If instead of T-junction, it would have been a four way junction (i.e. another way towards old</li>

</ul>

SAC), will there be any change in the problem implementation? If yes, write the pseudocode