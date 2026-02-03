# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

# PROGRAM:

## C Program to create new process using Linux API system calls fork() and getpid() , getppid() and to print process ID and parent Process ID using Linux API system calls

```
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>
#include <sys/wait.h>

int main() {
    int pid = fork();

    if (pid == 0) {
        printf("I am child, my PID is %d\n", getpid());
        printf("My parent PID is %d\n", getppid());
        sleep(2);   // keep child alive
    } else {
        printf("I am parent, my PID is %d\n", getpid());
        wait(NULL);
    }
    return 0;
}

```

## OUTPUT
<img width="796" height="219" alt="Screenshot 2026-02-03 074855" src="https://github.com/user-attachments/assets/39420bc3-7c15-41d5-b5b7-e3d08bed72ce" />



## C Program to execute Linux system commands using Linux API system calls exec() , exit() , wait() family

```

```

## OUTPUT
<img width="1427" height="307" alt="Screenshot 2026-02-03 081217" src="https://github.com/user-attachments/assets/7c4d6223-2238-48b2-aba2-f65903e26601" />




# RESULT:
The programs are executed successfully.
