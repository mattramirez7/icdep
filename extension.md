#Extension
##**How can we add additional features to the protocol without breaking previous functionality?**\

To ensure the ability to add additional features to the protocol without breaking its previous
functionality, I would create a header containing metadata on each card that a node receiving 
such card must recognize before accepting the card or pass it along if the header is not recognized.
This allows for new features to be implemented with their own specific header format pertaining 
to only itself, allowing all other nodes without the updated functionality to ignore the card. 
New features may be added, so long as the format of their unique header identifier is not overlapping 
with another feature.

###Send to any individual on the whole UW campus
For a sender to be able to send to any individual on the UW campus, each card must be equipped with a 
lat/long location identifier followed by the person's first and last name converterd to it's numerical 
representation separated by a '/', where A = 1, B = 2, C = 3, etc. This will be located on the back top 
left corner. An example header for sending a card to John Doe on UW campus would be:

47.655548, -122.303200, 10/15/8/14, 4/15/5 

The nodes will receive the card and pass the card to the node in the direction of the specified lat/long
location. Once the location is reached, the node will use the name information to pass to nearby nodes 
until a node recognizes the numerical name representation.


###Specify whether contents are ASCII text, Unicode text, or binary values
To specify whether contents are ASCII text, Unicode text, or binary values each encoding type will be 
assigned a unique value located in the back top right corner of the card. For these examples, the code 
will look like this respectively (CT = Content-Type:)

CT: ASCII
CT: Unicode
CT: Binary

For new content types in the future, their code will be denoted by some section of their name, so long
as none of them are duplicates of previously established content type codes.


###Keep a record of what nodes the card has passed through.
To keep a record of what nodes the card has passed through, we will equip eahc node with a unique identifier
code. When the card is passed through a node, the node will write starting on the bottom left of the backside
of the card its unique identifier code (ex. 1c3r9). The codew will be written from left to write, which also 
allows for knowing the order in which the card was passed through.



   
   
