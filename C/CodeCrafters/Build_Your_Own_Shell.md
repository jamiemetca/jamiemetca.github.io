17/11/2025

# Build your own shell
## Handle invalid commands
The requirement is to capture the users input and reply with

```c
    abc: command not found
```

Where abc is the command entered by the user.
I initially user scanf to get the users input but after reviewing the sample
code which uses fgets I have updated my code to also use fgets.
[Here](/C/scanf_vs_gets) is why. In shorts it's safer.


