### The repository contains 2 codes:
- A shell terminal implemented in C (Submission to [Operating Systems Assignment 1](https://vnit.ac.in/cse/index.php/oslab2/))
- A multi thread web server (Submission to [Operating Systems Assignment 2](https://vnit.ac.in/cse/index.php/OSlabwebserver/)

### Steps to run the codes:
1. myshell.c  
    - git clone https://github.com/Diksha942/Shell-and-MultiThread-Server.git 
    - Run myshell.c in your preferred IDE.
    - The terminal works for most of the linux commands and supports parallel and sequential execution of commands using '&&' and '||' respectively.
    - Supports redirection of output using '>' into a file.
    - Type 'exit', to exit the shell.

2. The multi-thread web server
    - git clone https://github.com/Diksha942/Shell-and-MultiThread-Server.git
    - Open the 'WebServer' folder in your preferred IDE.
    - Run the Makefile to create the executables, or type 'make' in the terminal inside folder.
    - Run 
    `./wserver [-d basedir] [-p port] [-t threads] [-b buffers] [-s schedalg]` 
    in the terminal, where
    
        **basedir**: this is the root directory from which the web server should operate. The server should try to ensure that file accesses do not access files above this directory in the file-system hierarchy. Default: current working directory (.).

        **port**: the port number that the web server should listen on; the basic web server already handles this argument. Default: 10000. 

        **threads**: the number of worker threads that should be created within the web server. Must be a positive integer. Default: 4.

        **buffers**: the number of request connections that can be added to the buffer at one time (must be a positive integer). Default: 64.

        **schedalg**: the scheduling algorithm to be performed. Uses integer values 0 (for First in First Out) and 1 (for Shortest File First). Default: 0.
        
        for e.g. `./wserver -d ~/myServer –p 8003`
        
    - The server is ready. Now to run the client and open another terminal and run
    `./wclient localhost 8003 /test1.html`
