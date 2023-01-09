# ECE1175_Lab4
Lab 4 project for Embedded Systems class 

Realize rate monotonic scheduling algorithm.

You are required to realize earliest deadline first scheduling algorithm.

You are required to implement a program that can demonstrate priority inheritance.

For "do some work" in design chart, you may choose to print some messages to terminal. For example: "Thread 1 in", "Thread 1 starts", "Thread 1 ends" and "Thread 1 out" are used to simply describe the work each thread will do.
Please think carefully on what priority inheritance is, e.g., the advent order of each thread. For example, if thread 1 has the lowest priority and thread 3 has the highest priority. The definition of priority inheritance is that thread 1 should be earlier than thread 3 and thread 2 is later than thread 3.
General recommendations:
Run your program with privilege (run as "root" or using "sudo"). This may circumvent permission issues (if any) when configuring thread priorities.
Consider whether limiting the number of CPU cores your program may use is necessary. You may limit it by setting CPU affinity and disallow placing multiple threads on different CPU cores.
The following libraries, data types and functions may be useful when writing your code:
Library and header files:
"stdio.h", "stdlib.h", "unistd.h", "pthread.h" and "sched.h"

Data types:
pthread_t: thread variable

pthread_mutex_t: mutex variabl

pthread_mutexattr_t: mutex attribute variable

sched_param: structure variable for buffering thread priority

Functions:
pthread_mutexattr_setprotocol(): set protocol for mutex attribute variable

pthread_mutex_init(): initialize mutex variable

pthread_mutex_lock(): lock mutex variable

pthread_mutex_unlock():unlock mutex variable

pthread_create(): create a thread

pthread_setschedparam(): set priority, policy for a thread

pthread_getschedparam(): get priority, policy of a thread

pthread_join(): wait for all threads to finish before main() can exit

pthread_setaffinity_np, pthread_getaffinity_np: get/get CPU affinity of a thread

sched_setaffinity, sched_getaffinity - set and get a thread's CPU affinity mask
