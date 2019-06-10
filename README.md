# LibrarySystemsMonitorCompanionWebApplication
This project is a stripped-down verison of an application I built at work and primarily works in browsers that are updated to be compatible with HTML5 and CSS3. Tested and verified only in Chrome and Firefox.
<h2>Description</h2>
This web application is a companion app to the computer monitoring system that detects the statuses of the computer stations in each computer lab where I work. When a computer is detected as "offline" by the monitoring system, this application adds that computer's hostname to the list of offline computers and then highlights on the map which computer station it is. 

<h2>Overview</h2>
<img src="https://raw.githubusercontent.com/KodingKamp/LibrarySystemsMonitor/master/screenshot.PNG" width="70%">
This Javascript based application allows users to:
<ul>
  <li>view offline computers,</li>
  <li>select or highlight computers,</li>
  <li>deselect a selected computer,</li>
  <li>copy selected computer's hostname into clipboard, and</li>
  <li>debug the application with preprogrammed buttons.</li>
</ul>

<h2>GUI Entities</h2>
On the left side of the application, in red, is the Offline list; used to provide the user with a list of all the computers in that are showing up in the system as "Offline". On the far right, in green, is the debug menu; containing buttons used to display the application's abilities. In the center of the application, is where the map of the computer labs are displayed; each lab containing the computer lab's name and a varying amount of computer stations. Just above the map of the labs is a text field taht displayed the hostname of the most recently selected computer in the labs map.

<h2>Functionality and Benefits</h2>
When the system monitor detects that a computer is "offline", that computer's hostname is appended to the Offline list, on the left side of the screen in red. Visually, this is represented in the labs map by highlighting offline computers in red; 
this provides the user with the phyical location of the offline computer relative to the other computers in that lab reducing total service time for not having to search for or remember which computer corresponds to which computer hostname. The statuses of the computers would be captured, at a predetermined frequency, via XML get request responses from the system's server.
<br>
Users are able to click on a computer station in the map to highlight and selected it. Selecting a computer would display it's hostname in the Selected Station field above the labs maps and automatically copy that hostname to the clipboard, for easy pasting into reports. Only the most recently selected computer's hostname will display in the field but multiple computers can be selected to be highlighted. Selections can also be made from the Offline list; in the event of multiple computers going offline, this can be used to single out one station amoung all the red stations. Stations can be deselected by right-clicking on the computer in the map or by clicking the "Clear selected" button in the debug menu.
<br>
Within the Debug window, users shall be able to:
<ul>
  <li>clear the map of all selected stations,</li>
  <li>clear the map of all offline stations,</li> 
  <li>start a timer that will set a random computer as "Offline" every 3 seconds,</li>
  <li>stop the timer if it is started, and</li>
  <li>randomly set 5 or 10 or all of the available stations as "Offline"</li>     
</ul>
<h2>Final Notes</h2>
This web application is a companion app to the systems monitor we use at work and acts as a visual interface that reacts to the status of the monitoring system. However, since the original build requires communication with a private server using an authentication key, retrieving the computer statuses was not implemented in this skeleton project. Instead, the Debug Menu is used to simulate stations going "offline" randomly. The Debug Menu was created to quickly demonstrate the capabilities of the application and is not present in the original build.
<hr>
All code written by Kamp Duong with the aid of Jason Connor on CSS flex and grid.<br>
2019 KodingKamp
