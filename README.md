# DES-Brute-force-Attack

This program allows for a DES brute-force attack over a network between clients and a server. The program can run on multiple client
machines in a client-server model. The program uses multiple POSIX threads to divide up the brute-force work. Every millionth
increase in the keyspace exploration is printed out in order to gauge the progress of the program. Since each thread is assigned an exclusive
keyspace, it is treated as a client capable of stopping the whole brute-force effort.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What you need to install the program:

```
1. C++ compiler (GCC, ...)
2. make tool (for easier compilation)
3. Linux environment 
     (Options include Bash Shell on Windows 10 
        or Linux virtualization software [Virtual Box] 
        or native environment)
4. IDE or source editor (Sublime Text, Atom, etc...) [optional since terminal tools can be used]
```

### Installing

In order to run the program, download the source code into a source folder and install a Linux environment followed 
by the appropriate C++ compiler. Then, type ** make ** in the terminal of the linux environment. Make sure your terminal path
points to the source folder.

### Running


```
1. Go to the "server/bin" folder and execute the "server" executable (this serves as the server for the clients connecting so make sure you run the server exectuable on the machine that should be the server). If the "server" executable is not recognized, then type
"make" in the terminal with the path pointing to the server folder to create an executable suitable for your operating system.

2. Fill out the keyspace of the client program in "src/des.cpp". This is just a 2D array to be used by the Pthreads.

3. Fill out the IP address of the server in "src/client.cpp" so that the client program can connect to it. The IP address of the server
 can be found by typing "ifconfig" (without the quotes) on the server's terminal.

4. Compile the program by typing "make". Install "make" if it is not already installed.

5. Run the client program by executing the "des" executable in the bin folder. Type "./bin/des" in the terminal to execute.

```

Note: The server program was not written by me so for further information on the server program, please go here:

https://github.com/rbaron/multichat


Happy Bruteforcing....


## Author

* **Mussie Habtemichael** - [mussieh](https://github.com/mussieh)

