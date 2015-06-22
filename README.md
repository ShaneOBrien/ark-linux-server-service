# ark-linux-server-service
Auto starts the ARK server when your machine boots, easy commands to stop, update and start the server.
Modified from http://minecraft.gamepedia.com/Tutorials/Server_startup_script/Script?action=raw

Tested on Amazon EC2 AMI

<h2>Pre-requisites:</h2>

Get the server running as per official instructions at http://steamcommunity.com/app/346110/discussions/0/594820656471833280/

Screen:

yum install screen


<h2>Installation:</h2>
Create a file called ark in /etc/init.d/ and paste in the contents of the ark file above:

nano /etc/init.d/ark


Give the file the correct permissions:

chmod a+x /etc/init.d/minecraft


Add this to have it start automatically when the server starts:

chkconfig --add ark


<h2>Usage</h2>
Start: service ark start

Stop: service ark stop

Update: service ark update

Restart: service ark restart


<h2>Uninstall</h2>

chkconfig --del ark
