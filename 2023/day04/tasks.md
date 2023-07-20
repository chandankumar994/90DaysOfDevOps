# Day 4 Task: Basic Linux Shell Scripting for DevOps Engineers.

 ## What is Kernel

 The kernel is a computer program that is the core of a computer’s operating system, with complete control over everything in the system.
 
 ## What is Shell

 A shell is special user program which provide an interface to user to use operating system services. Shell accept human readable commands from user and convert them into something which kernel can understand. It is a command language interpreter that execute commands read from input devices such as keyboards or from files. The shell gets started when the user logs in or start the terminal.
 
 ## What is Linux Shell Scripting?

 A shell script is a computer program designed to be run by a linux shell, a command-line interpreter. The various dialects of shell scripts are considered to be scripting languages. Typical operations performed by shell scripts include file manipulation, program execution, and printing text.

 **Tasks**

#### Task-1. Explain in your own words and examples, what is Shell Scripting for DevOps.
 
 **Ans:** A shell script is a text file that contains a sequence of commands for a UNIX-based operating system. It is called a shell script because it combines a sequence of commands, that would otherwise have to be typed into the keyboard one at a time, into a single script.

#### Task-2. What is `#!/bin/bash?` can we write `#!/bin/sh` as well?
**Ans:**  `#!/bin/bash` and `#!/bin/sh` are known as shebang lines, also called hashbangs. They are used in Unix-like operating systems to specify the interpreter that should be used to execute the script.
`#!/bin/bash` indicates that the script should be interpreted and executed using the Bash shell. Bash (Bourne Again SHell) is a popular and powerful shell that is backward-compatible with the Bourne shell (`/bin/sh`).

On most Unix-like systems, `/bin/sh` is a symbolic link or a small executable that points to the default system shell, which is often Bash or another compatible shell.

So, to answer your question, yes, you can use `#!/bin/sh` in a script as well. However, there are some differences between bash and sh. While Bash offers more features and capabilities, sh is meant to be a simpler, more standardized shell. If you use `#!/bin/sh`, your script will be interpreted using the system's default shell, which may or may not be Bash.

If you need specific features provided by Bash and want to ensure that your script works consistently across systems, using `#!/bin/bash` is a safer option. On the other hand, if you are writing a script that should be portable and run on various Unix-like systems, sticking to POSIX-compliant shell features and using #!/bin/sh is recommended.

In summary, both `#!/bin/bash` and `#!/bin/sh` are valid shebang lines, and the choice depends on your specific needs for the script.


#### Task-3. Write a Shell Script which prints `I will complete #90DaysOofDevOps challenge`
**Ans:**
```
#!/bin/bash
echo "I will complete #90DaysOfDevOps challenge"
```
Save the above code in a file, let's say devops_challenge.sh. To execute the script, you need to give it executable permissions using the following command:
```
chmod +x devops_challenge.sh
```
Then, you can run the script by simply typing:
```
./devops_challenge.sh
```
OutPut:
```
I will complete #90DaysOfDevOps challenge
```

#### Task-4. Write a Shell Script to take user input, input from arguments and print the variables.
**Ans:**
```
#!/bin/bash

# Take input from the user
echo "Enter your name:"
read user_name

# Check if any command-line argument is provided
if [ $# -gt 0 ]; then
  arg_name="$1"
else
  arg_name="No argument provided"
fi

# Print the variables
echo "User input: $user_name"
echo "Argument input: $arg_name"
```
Save the above code in a file, let's say user_input_script.sh. To execute the script, you need to give it executable permissions using the following command:
```
chmod +x user_input_script.sh
```
Then, you can run the script in two ways:

Without providing any command-line argument:
```
./user_input_script.sh
```
The script will prompt you to enter your name, and after entering your name, it will print both the user input and the argument input as "No argument provided".

Providing a command-line argument:
```
./user_input_script.sh John
```
The script will use "John" as the command-line argument and prompt you to enter your name. After entering your name, it will print both the user input and the argument input accordingly.

For example, if you enter "Alice" when prompted, the output will be:
```
User input: Alice
Argument input: John
```

#### Task-5. Write an Example of If else in Shell Scripting by comparing 2 numbers
**Ans:**
```
#!/bin/bash

# Input two numbers
echo "Enter the first number:"
read num1

echo "Enter the second number:"
read num2

# Compare the numbers using if-else
if [ "$num1" -eq "$num2" ]; then
  echo "Both numbers are equal."
elif [ "$num1" -gt "$num2" ]; then
  echo "The first number ($num1) is greater than the second number ($num2)."
else
  echo "The second number ($num2) is greater than the first number ($num1)."
fi
```
Save the above code in a file, let's say compare_numbers.sh. To execute the script, you need to give it executable permissions using the following command:
```
chmod +x compare_numbers.sh
```
Then, you can run the script, and it will prompt you to enter two numbers. After entering the numbers, it will compare them and display the result based on the comparison.

For example, if you enter "5" as the first number and "8" as the second number, the output will be:
```
Enter the first number:
5
Enter the second number:
8
The second number (8) is greater than the first number (5).
```


 Was it difficult?
 
 - Post about it on LinkedIn and Let me know :)
 Article Reference: [Click here to read basic Linux Shell Scripting](https://devopscube.com/linux-shell-scripting-for-devops/)
 YouTube Vedio: [EASIEST Shell Scripting Tutorial for DevOps Engineers](https://www.youtube.com/watch?v=_-D6gkRj7xc&list=PLlfy9GnSVerQr-Se9JRE_tZJk3OUoHCkh&index=3)
