# CSA0483-OPREATING-SYSTEM
#1-> SYSTEM CALL INVOKING:-

ALGORITHAMIC STEPS:-

1)Include the necessary header files, such as stdio.h and unistd.h.

2)Declare two pid_t variables to store the process identifiers for the current process and the child process.

3)Use the fork() system call to create a new child process. The fork() system call will return the child's PID in the parent process and 0 in the child process.

4)Check the return value of fork():

5)If it's less than 0, the fork failed, and you should display an error message and exit.

6)If it's 0, it means you're in the child process, so you can display the child's PID using getpid() and the parent's PID using getppid().

7)If it's greater than 0, you're in the parent process, so you can display the parent's PID using getpid() and the child's PID, which is the value returned by fork().

8)Print the process identifiers and any other information you want to display.

9)End the program.

#2->COPY THE CONTENT OF ONE FILE TO OTHER:-

ALGORITHAMIC STEPS:-

1)Include the necessary header files, such as stdio.h, stdlib.h, unistd.h, and fcntl.h.

2)Define a buffer size (e.g., BUFFER_SIZE) to read and write data in chunks.

3)Declare variables to store file descriptors for the source and destination files (source_fd and dest_fd), as well as variables to store the number of bytes read and written (bytes_read and bytes_written), and a buffer to hold data.

4)Open the source file for reading using the open() system call with the O_RDONLY flag. Check for errors in opening the source file.

5)Open or create the destination file for writing using the open() system call with the O_WRONLY and O_CREAT flags. Specify file permissions (e.g., S_IRUSR | S_IWUSR) to allow reading and writing by the owner. Check for errors in opening/creating the destination file.

6)Use a loop to read data from the source file in chunks of BUFFER_SIZE bytes using the read() system call. Continue until the end of the source file is reached.Check for errors during reading.

7)Write the read data to the destination file using the write() system call. Check for errors during writing.

8)Close both the source and destination files using the close() system call.

9)Display a success message indicating that the file was copied successfully.

#3-> CPU SCHEDULING PROGRAM USING FCFS:-

ALGORITHM STEPS:-

1)Define a structure Process to represent a process with attributes like process_id, arrival_time, burst_time, completion_time, turnaround_time, and waiting_time.

2)Prompt the user to enter the number of processes (n).

3)Create an array of Process structures to store process information for n processes.

4)For each process from 1 to n:

a.Set process_id for the process.

b.Set arrival_time to 0 (since all processes start at time 0).

c.Prompt the user to enter the burst_time for the process.

5)Calculate the completion, turnaround, and waiting times for each process:

a.Initialize a variable total_waiting_time to 0.

b.For each process from 1 to n:

i.If it's the first process (i == 0), set completion_time to burst_time.

ii.Otherwise, set completion_time to the sum of the previous process's completion_time and the current process's burst_time.

iii.Calculate turnaround_time as completion_time - arrival_time.

iv.Calculate waiting_time as turnaround_time - burst_time.

v.Add the waiting_time to total_waiting_time.

6)Calculate the average waiting time as avg_waiting_time = total_waiting_time / n.

7)Print the table with columns: "Process," "Arrival Time," "Burst Time," "Completion Time," "Turnaround Time," and "Waiting Time."

8)For each process, print its details.

9)Display the average waiting time.

10)End

3.Design CPU scheduling algorithm with c using FCFStechnique
a.All process are activated time 0
b.Assume no process in I/O devices
Algorithm:-
step1:-Include libraries(header file like stdio.h)
step2:-Define process structure
step3:-Input process data
step4:-calculate waiting time and turnaroundtime
step5:-calculate average waiting time and turnaroundtime
step6:-Display process information
step7:-End of Algorithm

4.ccode for scheduling select waiting process with executiontime to execute next
Algorithm:-
step1:-Input given by user wih n number of process
step2:-sort process based on burst time
step3:-Initialise variables(current time,completed process)
step4:-process scheduling
step5:-display output
step6:-End of program

5.scheduling program with c select waitingprocess to execute next
Algorithm:-
step1:-Input(enter number of process)
step2:-sort process based on priority(highest to lowest)
step3:-Initialize variables(currenttime,completedprocess)
step4:-process scheduling
step5:-display the output
step6:-End of program

6.c program to implement preemptive priority scheduling algorithm
Algorithm:-
step1:-Input(enter number of process)
step2:-Initialise variables
step3:-process scheduling
step4:-display output
step5:-End of program

7.cprogram to implement nonpreemptive sjf algorithm
Algorithm:-
step1:-Input(Enter number of process)
step2:-sort the process based on their burst time in ascending order
step3:-Initialisation step4:-for each process from 1 to n
step5:-calculate average waiting time
step6:-calculate average turnaroundtime
step7:-End of program

8.cprogram to simulate roundrobin scheduling algorithm with c
Algorithm:-
step1:-Input(number of processes)
step2:-Initialise an empty queue to store process
step3:-while there are processed in queue or any process has remaining bursttime
step4:-End of program

11.c program for multithreading Algoritm:-
step1:-Include necessary header file
step2:-Define the threadfunction
step3:-create threads
step4:-join threads
step5:-compile and run program
step6:-End of program

12.cprogram for Dining Philosophers problem
Algorithm:-
step1:-Initialization
step2:-philospher behaviour
step3:-Handling forks
step4:-synchronization
step5:-Implementation using loop
step6:-End of program


13.c program for various memory allocation strategies\
Algorithm:-\
step1:-Input(enter memorysize)\
step2:-Initialisation(set found flag to 0)\
step3:-loop through memoryblocks\
step4:-if 'found'flag is 1,memory allocated successfully\
step5:-if 'found'flag is 0,not enough space is available for allocation\
step6:-End of program

14.c program for organisefile using singlelevel directory\
Algorithm:-\
step1:-file structure\
step2:-Directory structure(not needed for single level directory)\
step3:-operation(like create newfile,delete file,list file,search file,Exit)\
step4:-Enter the operation to perform step5:-file can be created ,listed,updated it continue till exit\
step6:-End of program

15.c program to organize file using two level directory structure\
Algorithm:-\
step1:-file structure(structfile contain attributes suchas name,size)\
step2:-struct directory(directory attribute suchas name,list of files)\
step3:-Enter directoryname and parent directory\
step4:-perform operation(create directory,create file,delete file,listfile,exit)\
step5:-Initialize filesystem\
step6:-End of program

#16->IMPLEMENTING RANDOM ACCESS FILES FOR PROCESSING EMPLOYEE DETAILS:-

ALGORITHM STEPS:-

Open or Create File:

Try to open the file in read and write mode (r+).

If the file does not exist, create a new one in read and write mode (w+).

Menu Loop:

Display a menu with options:

-Add Employee

-Display Employees

-Update Employee

-Delete Employee

-Exit

User Input:

-Take the user's choice as input.

Switch on User's Choice:

-For each option, perform the following:

-Add Employee (Option 1):

-Take input for Employee ID, Name, and Salary.

-Use fseek to move to the position corresponding to the given Employee ID.

-Write the employee data using fwrite.

-Display Employees (Option 2):

-Use rewind to move the file position indicator to the beginning.

-Read and display each employee's details using fread.

Update Employee (Option 3):

-Take input for the Employee ID to update.

-Use fseek to move to the position corresponding to the given Employee ID.

-Read the existing employee data using fread.

-Take input for the new Name and Salary.

-Use fseek again to move to the position corresponding to the given Employee ID.

-Write the updated employee data using fwrite.

Delete Employee (Option 4):

-Take input for the Employee ID to delete.

-Use fseek to move to the position corresponding to the given Employee ID.

-Read the existing employee data using fread.

-Clear the record by setting the Employee ID to 0.

-Use fseek again to move to the position corresponding to the given Employee ID. Write the cleared employee data using fwrite.

-Exit (Option 0):

Display an exit message and break out of the loop.

Invalid Choice:

-Display a message for an invalid choice.

Close File:

-Close the file using fclose.

#18-> SIMULATING PRODUCER-CONSUMER PROBLEM USING SEMAPHORES:-

ALGORITHM STEPS:-

Initialize Semaphores and Mutex:

-Initialize semaphores empty and full to the buffer size and 0, respectively.

-Initialize a mutex for mutual exclusion.

2)Initialize Shared Buffer and Indices:

-Initialize the shared buffer and set producer (in) and consumer (out) indices to 0.

Producer Function:

-In the producer thread function:

-Generate a random item.

-Wait for an empty slot in the buffer (sem_wait(&empty)).

-Acquire the mutex for mutual exclusion (pthread_mutex_lock(&mutex)).

-Insert the item into the buffer.

-Update the producer index (in).

-Print a message indicating the produced item.

-Release the mutex (pthread_mutex_unlock(&mutex)).

-Signal that a slot in the buffer is now full (sem_post(&full)).

-Sleep to simulate variable production time.

Consumer Function:

In the consumer thread function:

-Wait for a filled slot in the buffer (sem_wait(&full)).

-Acquire the mutex for mutual exclusion (pthread_mutex_lock(&mutex)).

-Remove the item from the buffer.

-Update the consumer index (out).

-Print a message indicating the consumed item.

-Release the mutex (pthread_mutex_unlock(&mutex)).

-Signal that a slot in the buffer is now empty (sem_post(&empty)).

-Sleep to simulate variable consumption time.

Main Function:

-Initialize threads for the producer and consumer functions.

-Join the threads (this will never be reached in this simple example).

Clean Up:

-Destroy semaphores and mutex.

#21-> IMPLEMENTING WORST FIT ALGORITHM OF MEMORY MANAGEMENT:-

ALGORITHM STEPS:-

Initialization

Define a Free Block Structure:

-Create a structure to represent free memory blocks. This structure should have fields such as start (starting address of the block), size (size of the block), and a pointer to the next free block.

Initialize Free Memory List:

-Create a pointer to the head of the free memory list.

-Initialize it with a single free block representing the entire available memory.

Allocation Function

-Define Allocation Function:

-Create a function to allocate memory using the worst fit algorithm.

-Traverse the free memory list to find the largest available block that can accommodate the process.

-If a suitable block is found, allocate memory and update the free memory list.

Allocate Memory:

-In the allocation function:

-Traverse the free memory list.

-Keep track of the worst fit (largest block).

-If a suitable block is found, allocate memory:

-Update the free memory list.

-Print allocation information.

Deallocation Function

-Define Deallocation Function:

-Create a function to deallocate memory.

-Create a new free block and add it to the free memory list.

-Print deallocation information.

Main Program

Main Function:

-In the main program:

-Initialize free memory.

-Allocate memory for processes.

-Deallocate memory.
