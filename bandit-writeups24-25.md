Bandit level 24->25

A daemon is listening on port 30002 and it will give me the password for 25 level if i give it the password of 24 + the correct 4 digit pincode.

Enumeration

The combinations of the 4 digit pin code are 10000 in total so i need to brute force my way to find the correct one as it's not that hard for the computer to handle this much calcualtions.

First of all i am gonna try to connect to the daemon using netcat on the given port like this:

nc localhost 30002

I get a response telling me to input the 24 level password and the 4 digit password seperated by space.

I need to find a way to automate this, so im thinking of using a script to iterate from 0 to 10000 and test it with the daemon to see if its correct. 
So the script is like this :
