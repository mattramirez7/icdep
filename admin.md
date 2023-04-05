# Administration

## **How can we send commands ("SLEEP", "RESTART", "ARE-YOU-THERE", etc) to individual 
nodes in the network, rather than treat them as pass-through intermediaries?**

If we want to send a command type such as "SLEEP", "RESTART", and "ARE-YOU-THERE",
we can introduce another type of header as expressed in the extension file that is 
unique to cards that are meant to give commands to a specific node. As also specified 
in the extension file, each node will have a unique 5-digit code identifier to confirm 
that it is the correct node for the intended command. An example header to send commands
would look like this (CMD=Command, 1c3r9= unique identifier) 

CMD, 1c3r9, "SLEEP"

Each node will check to see if there is a command and will only execute the command if the 
unique identifier matches its own. If not, it will pass it on.
