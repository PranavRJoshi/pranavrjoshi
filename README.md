## Hi there 👋

I am a Software Engineer with over 3 years of experience, specializing in Systems and Network Engineering. My expertise includes implementing security at both the infrastructure and application levels, with a strong focus on compliance. I have hands-on experience with FIPS enablement across service images, libraries, and packages to ensure full FIPS compliance.

In addition, I possess a solid background in Blockchain and Web3 technologies. I have developed decentralized applications (dApps) and smart contracts for both Web3 startups and enterprise clients, contributing to secure and scalable blockchain-based solutions.

- 🔭 Books I've read so far:

    | Title                            | Author's Site                                  | ISBN-10       |
    | -------------------------------- | ---------------------------------------------- | ------------- |
    | C Programming: A Modern Approach | [knking[dot]com](http://knking.com/index.html) | 0-393-97950-4 |
    | Unix Network Programming         | [kohala[dot]com](http://www.kohala.com/start/) | 0-13-949876-1 |

- 🌱 I’m currently learning software portability from _The Goat Book_: [GNU Autoconf, Automake, and Libtool](https://sourceware.org/autobook/) by G.V. Vaughan, B. Elliston, T. Tromey, and I.L. Taylor.
- 👯 I’m looking to collaborate on remote software engineering projects or long-term opportunities where I can contribute my skills in C/C++, systems programming, and backend development.
- 💬 Ask me about C, C++, System, Network, and Blockchain.

### Projects' Quick Review

Below are some of the projects I've worked on, and their brief description.

1. Keen Price Tracker:

    * Language: Python
    * Tools: Kivy, Selenium
    * Usage: A simple price tracker for products found on e-commerce sites. Provides functionality to notify the user when the price of products lowers to that of threshold price required by user.

2. DapsBid:

    * Language: Solidity and JavaScript
    * Tools: React, Ethers, and Hardhat
    * Usage: A decentralized voting application which lets user create multiple polls. Information about the poll and its status are all stored in the Ethereum blockchain. 
  
3. C Programming, A Modern Approach:

    * Language: C
    * Tools: GCC/Clang, GDB/LLDB, Makefiles
    * Description: Most of the exercises and projects found in the book including: 

        1. Data structures using Abstract Data Type (ADT).
        2. Inventory application with numerous changes; dynamically allocating memory if previous allocation is exhausted, command-line options, and other safer idioms to handle input in a defined behavior.
        3. Departure time application that analyzes the given time and determines the closest departure time. It is also one of the recurring problem throughout the text and modifications done as required.
        4. Reminder application. Another recurring problem which utilizes various aspects of the lanuages as we proceed the chapters.
        5. Paragraph justification is a simple programs which justifies the paragraph provided as input. The chapter which introduces this program also introduces the input and output redirection operator provided by the shell process.
        6. A sample program to illustrate how to return arrays, functions, and array elements. All through the use of pointers as in normal scenario, such return types are illegal.
        7. Sorting words: through the use of `qsort(3)`, or by creating a custom function to handle the sorting.
        8. Wrapper for many of the functions defined in `string` library header, and wrapper for memory related calls such as `malloc(3)` and `free(3)` to avoid common problems such as "dangling pointers" and "double free".
        9. Macros and the C preprocessor. Creating "generic" functions through parameterized macros, using variable length paramterized macros, and using the compiler driver to expand the source file to inspect the macro expansion, sent during compilation.
        10. and many more!

4. Time protocol and Daytime protocol client and server implementation (UNP):

    * Language: C
    * Tools: GCC/Clang, GDB/LLDB, Makefile
    * Usage: Implements RFC 867 and RFC 868 to provide a client and server application to fetch the time and daytime. Provides implementation for both TCP and UDP. Reliability in UDP is achieved by determining the round-trip time (RTT). Other UDP based projects below also utilizes RTT to add reliability to the application.

5. Packet InterNet Groper (PING) program (UNP):

    * Language: C
    * Tools: GCC/Clang, GDB/LLDB, Makefile
    * Description: Basic implementation of standard `ping(1)` program available in most Unices and other OSes. Worked on IP based and XNS based ping program.
    * Usage: To test the reachability of the host by `ping`ing the respective host. Also implemented a feature (included in the exercise) to trace the route (similar to `traceroute(1)`, but uses ICMP packets) by utilizing the "time-to-live" or ttl field in IP datagrams. Raw sockets were used to send and receive ICMP packets. Also browsed through the mechanics of `make(1)` with it's ability to create dependency files--through compiler options--for the source files and structuring projects.

6. Trivial File Transfer Protocol (TFTP) client and server implementation (UNP):

    * Language: C
    * Tools: GCC/Clang, GDB/LLDB, Makefile, `tcpdump(1)`/Wireshark
    * Usage: A simple file transfer application with no inherent security like FTP. Both TCP and UDP implementation are done. Implemented functionality described in exercise of text to handle final acknowledgement packet as well as use multi-buffer approach to optimally invoke system calls during file reads and writes. Command `tcpdump(1)` and GUI application Wireshark were used to trace the network packets between the client and server.

7. Line Printer Spooler client and server implementation (UNP):

    * Language: C
    * Tools: GCC/Clang, GDB/LLDB, Makefile, `tcpdump(1)`/Wireshark
    * Description: The program presented in text is originally for Print Spooler programs--`lpr(1)` for 4.3BSD and `lp(1)` for System V. Modern Unices tend to use `cups(1)` subsystem to interact with printing devices. In spite of such compatibility issues, the fundamental point of the chapter was properly received: job control in a network environment. Along with this, various output filters, usage of various symbolic representation in control files, and security considerations were discussed.
    * Usage: Provides the client program that contacts the `lpd(8)` daemon on remote host to print the files given as command line argument. The server was implemented as an addendum; a proof of concept, due to absence of `lpd(8)` in newer OSes.

8. Remote Command Execution client and server implementation (UNP):

    * Language: C
    * Tools: GCC/Clang, GDB/LLDB, Makefile, `tcpdump(1)`/Wireshark
    * Description: Implemented remote shell (rsh) and it's server counter-part (rshd, more clearly termed as rcmdd by the author) to execute command on remote host. The `rcmd(3)` function implemented is used for other BSD's "r-programs". Unlike `ssh(1)` client programs that can use any port to establish a connection with remote shell, 4.3BSD's remote shell requires the client to use reserved port.
    * Usage: Implemented the client and server programs for remote command execution. Utilizes custom `ruserok(3)` function to authenticate the user and custom `rresvport(3)` to get a socket using reserved port. As described in the exercise of text, implemented the version of program using both Unix pipes (`pipe(2)`) and Unix streams pipes (`socketpair(2)`). Also learnt about logging subsystem on macOS and on Linux.

9. Remote Login client and server implementation (UNP):

    * Language: C
    * Tools: GCC/Clang, GDB/LLDB, Makefile, `tcpdump(1)`/Wireshark
    * Description: Although the remote shell imitates the shell process, command such as `tty(1)` and use of editors such as `vi(1)` will notify that the shell process invoking these commands do not have terminal device attached to it. 4.3BSD has the server `rlogind` which listens for `login(1)` request from the client user using `rcmd(3)`. Such program requires various considerations such as terminal characteristics, environment setup, user authentication, signal handling, and many more. The secure alternative `slogin(1)`--usually a symlink to `ssh(1)`--is particularly different from `rlogin(1)` as it does not rely on `exec`uting the `login(1)` program, but rather works with PAM modules and other secure environment managing subsystems to invoke the `sh`ell process. Both approach uses the concept of pseudo-terminal device. Lasltly, the BSD's `rlogin(1)` program is also compared with TELNET facility, as required by the exercise.
    * Usage: Implemented client and server programs for remote login. Although BSD's terminal API is shown in text, my implementation uses POSIX defined `termios(4)` API to handle the terminal characteristics. Other significant modification includes: POSIX defined technique (similar to System V) to obtain pseudo-terminal, wrappers for various historical signal handling functions, and use of new socket interface as described in RFC 3493.

10. Implementing library functions:

    * Language: C
    * Description: Below are some of the library functions that I've implemented based on their functionality as described in respective manual:

        1. `strcpy(3)`/`strncpy(3)`: K.N. King's text showed various idioms for `for` block; used for these functions.
        2. `strtol(3)`: Created my implementation of this function when I was reading Chapter 6 of UNP.
        3. `strcmp(3)`/`strncmp(3)`: K.N. King's text for strings showed this functionality.
        4. `rresvport(3)`: UNP described the details of this call, which I later implemented.
        5. `ruserok(3)`: Chapter 9 of UNP showed this function.
        6. `readv(2)`/`writev(2)`: These system calls were discussed in UNP. Later read the manual and implemented it. Similar to original system call, uses `struct iovec` instead of the usual buffer.

    * 

11. Sic Shell Library:

    * Language: C
    * Tools: m4, Automake, Autoconf, GCC/Clang
    * Description: As seen in _The Goat Book_, it describes the functionalities for a simple shell library. Includes functionality such as: builtin commands for shell, evaluate command line, simple list data structure, syntax table, macros for `malloc(3)` and `free(3)`, and other functionality. Custom macros were defined (using m4) for `configure.ac` file. 

12. Libtool Libraries:

    * Language: C
    * Tools: GNU libtool, bash
    * Description: Through the use of GNU libtool, created various libraries: shared, static, and convenience. Also used other features provided by GNU libtool such as installing library, understanding intermediate files generated during library creation, and a bit of bash scripting to automate repetitive tasks.

13. 


**Reach me on:**
- 🌐 <a href="https://www.linkedin.com/in/pranavramjoshi/">LinkedIn</a>

### 🏆GitHub

[![Pranav's GitHub stats](https://github-readme-stats-sigma-five.vercel.app/api?username=PranavRJoshi&include_all_commits=true&count_private=true&theme=monokai&show_icons=true)](https://github.com/PranavRJoshi)

![](https://github-profile-trophy.vercel.app/?username=PranavRJoshi&theme=monokai&no-frame=false&no-bg=false&margin-w=4)
