# System Processes

## Explanation

A process (or job) is a program being executed.  

### Process Memory

Process memory is made up of four different parts:

1. text - compiled code read from storage upon launch
2. data - global and static variables created before execution
3. heap - dynamic memory for calls from the process
4. stack - temporary data for params and local vars

![Process Memory](../../../_assets/Process_Memory.jpg "A process in memory")

### Process States

Processes exist in one of five states:

1. New - process is being created
2. Ready - process is ready to run, but is not
3. Running - process is running 
4. Waiting - process is ready to run, but cannot because it is waiting for resources to become available (keyboard input, disk access, timer, etc)
5. Terminated - process is done running

![Process States](../../../_assets/Process_States.jpg "Possible process states")

### Process Control Block

Each process has a **Process Control Block** (PCB) made up of the following:

- Process state - one of the five listed above
- Process ID - unique numeric identifier
- Pointer - pointer to parent process (nearly all processes have a parent)
- Program counter - pointer to address of next instruction in process
- CPU registers - where process is running; used when process is interrupted
- CPU-scheduling info - priority and pointers to queues
- Memory-management information - info about base and limit registers, page table
- Accounting information - resources used by system
- I/O status - IO devices allocated to the process

Each process has its own unique PCB and each OS will handle PCBs differently

### Threads

A thread is a segment of a process which represents a basic unit of processer time and has three possible states:

1. running
2. ready
3. blocked

Threads take less time to terminate and do not isolate

## Importance

Everything that happens on an OS happens as a process; processes are the basis of all higher level computation.

## Example

View active processes on Windows:

1. *Win Key*
2. Type "cmd"
3. Run as administrator
4. Type "tasklist" in the command prompt

View active processes on Linux:

Type "ps" in terminal (or "htop" or "top")

## Resources

- [UIC CS - Processes](https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/3_Processes.html)
- [Study Tonight - Process in Operating System](https://www.studytonight.com/operating-system/operating-system-processes)
- [TutorialsPoint - Process](https://www.tutorialspoint.com/operating_system/os_processes.htm)
- [BinaryTerms - Process in Operating System](https://binaryterms.com/process-in-operating-system.html)
- [Microsoft Learn - Proecsses and Threads](https://learn.microsoft.com/en-us/windows/win32/procthread/processes-and-threads)
- [Geeks4Geeks - Difference between Process and Thread](https://www.geeksforgeeks.org/difference-between-process-and-thread/)