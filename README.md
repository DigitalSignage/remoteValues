<h5>by digitalsignage.com</h5> 
==========



RemoteValues, customer que management
---------------------------------------

With DigitalSignage.com and RemoteValues, you can easily integrate customer line queuing manager, a custom play score board, telemarketing progress board, or any other type of Digital Signage screen with custom labels.
The real power comes from your own scripting logic. In other words, you can develop your business logic that's right for your company and feed the values into any label on the public digital signage screen.
In this example we provide a working server to act as customer line counter; but this is just one example of many that could be incorporated.

With the Queue manager, employees control which number is being served, as well as provide your customers with the ability to scan a QR code on the Digital Signage screen and keep monitoring their status in line from a mobile device.
This means that your customers do not have to be confined in a room waiting to be served on, instead they can roam around and stay updated on current queue position.

We provide the working sample code powered by node.js web server that runs on Windows, Linux or Mac.
The application is organized into 3 modules.

- server software which manages the current queue as well as serves the HTML pages your employees and customer will interact with.
- terminal.html is the user interface your employees will use to manage the queue.
- nowServing.html is the user interface your customers will view to stay updated on current que position (using QR and mobile phone)

Server installation:
------------------------------------------------------------------------
To launch the server be sure to install node.js as well as the required modules:

<pre>
npm install express@3 (for express server v3.0)
npm install jquery
npm install underscore
npm install path
</pre>

Launch the server using:

<pre>
node server.js
</pre>

The server by default listens to connections on port 8080

User configuration and interaction
------------------------------------------------------------------------
Next edit terminal.html and nowServing.html and replace 'digitalsignage.com' with your server ip or DNS name.

for example:

<pre>
document.domain = 'digitalsignage.com';
var u = 'http://www.digitalsignage.com:8080/nowServing';
</pre>

<pre>
document.domain = 'digitalsignage.com';
$.ajax({
 url: 'http://www.digitalsignage.com:8080/' + step,
 ...
</pre>

Once the server is up and running you can launch:

http://[YOUR_IP]:8080/remoteValues/nowServing.html
http://[YOUR_IP]:8080/remoteValues/terminal.html

Be sure to follow the video tutorial at: http://www.digitalsignage.com/_html/signage_video.html?videoNumber=RemoteCounter
which will walk you through the StudioPro / SignagePlayer setup and configuration.


More help:
------------------------------------------------------------------------
- Landing page RemoteValues: http://www.digitalsignage.com/_html/remotevalues.html
- Landing page RemoteTouch: http://www.digitalsignage.com/_html/remotetouch.html
- RemoteValues: http://www.digitalsignage.com/_html/signage_video.html?videoNumber=RemoteValues
- RemoteTouch: http://www.digitalsignage.com/_html/signage_video.html?videoNumber=RemoteTouch

License:
------------------------------------------------------------------------
MIT


