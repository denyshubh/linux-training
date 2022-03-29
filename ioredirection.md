- Open a shell as user user and type cd without any arguments. This ensures that the home directory of this user is the current directory while working on this exercise. Type pwd to verify this.

- Type ls. You’ll see the ls command output onscreen.

- Type ls > /dev/null. This redirects the STDOUT to the null device, with the result that you will not see it.

- Type ls ilwehgi > /dev/null. This command shows a “no such file or directory” message onscreen. You see the message because it is not STDOUT, but rather an error message that is written to STDERR.

- Type ls ilwehgi 2> /dev/null. Now you will no longer see the error message.

- Type ls ilwehgi Documents 2> /dev/null. This shows the name of the Documents folder in your home directory while hiding the error message.

- Type ls ilwehgi Documents 2> /dev/null > output. In this command, you still write the error message to /dev/null while sending STDOUT to a file with the name output that will be created in your home directory.

- Type cat output to show the contents of this file.

- Type echo hello > output. This overwrites the contents of the output file.

- Type ls >> output. This appends the result of the ls command to the output file. Type cat output to verify.

- Type ls -R /. This shows a long list of files and folders scrolling over your computer monitor. (You might want to press Ctrl-C to stop [or wait some time]).

- Type ls -R | less. This shows the same result, but in the pager less, where you can scroll up and down using the arrow keys on your keyboard.

- Type q to close less. This will also end the ls program.

- Type ls > /dev/tty1. This gives an error message because you are executing the command as an ordinary user and ordinary users cannot address device files directly (unless you were logged in to tty1). Only the user root has permission to write to device files directly.
