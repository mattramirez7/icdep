#Anti-Duplication
**How can we ensure that each card is received once and only once?**\

To ensure that no card is received more than once, we can attach each card with a unique number 
identifier than denotes which card in the card stack it is: 1/5, 2/5, 3/5, etc. Each receiver node 
will need to track the unique number identifier receiver for every index card that reaches it. If 
the unique number identifier has not been received, the node will accept the message, and if it has 
already been received, the message will be blocked. The cards will be passed in order to maintain
clarity between the different messages.
