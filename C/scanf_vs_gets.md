[Back](README)

17/11/2025

# scanf vs fgets
Both of these functions are used to get input from the user.

## scanf
Reads formatted input and stops at whitespace. Which if you are trying to get
multiple words from the users isn't going to work.
There is also a risk of bufferOverflow errors/attacks.


## fgets
Stands for file gets which can be used to read from standard input.
As you need to define the buffer length the risk of bufferOverflow is removed.
