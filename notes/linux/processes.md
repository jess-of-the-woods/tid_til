[terminal](terminal.md)

## processes
- [signals](#signals)
- [states](#states)
- [niceness](#niceness)
- [ps](#ps-process-status)
- [kill](#kill)
- [pkill](#pkill)
- [/proc filesystem](#proc-filesystem)



- `top`: display linux processes (by CPU usage)
- `htop`: interactive process viewer (needs to be installed)
- `pstree`: display a tree of processes

All processes have an ID (PID: process id). All processes have a parent except init which has PID: 1. It is the initialisation process which boots the pc and runs through start up scripts. Init is the 'mummy' to all processes whose parents have died.

The kernel is a layer between the processes & the hardware. Each process has a UID which is the user that owns that process. Effective User Id (EUID) is a way of giving a process different permissions than the user that spawned it.

### signals
Signals are used by processes to communicate with the kernel, & also how the kernel communicates info about the state of the system to processes.

Processes need CPU time & the kernel manages when they get access to that in a smart way.

### states
4 States a process can be in:
- runnable (eligible to be scheduled for CPU time, has all the info it needs)
- sleeping (waiting for something)
- zombie state: a process that has finished doing what it is doing, waiting to give back the info it has come up with & then be killed by kernel
- stopped: has received a SIGSTOP, waiting for a SIGCONT (resume/continue)

### niceness
The niceness of a process is how high the priority of the process, therefore how 'nice' or respectful it is to other processes. The higher the number the lower the priority. Range is from about -20 to 19.
e.g. `nice -n 15 /not/important/task` or `nice -n -5 <PID>`

or if a process is already running, `renice -n -5 <PID>`

### ps (process status)
- `ps aux`: report snapshot of current processes.

**examples**:
- `ps aux | grep nginx`: check CPU usage for a process (nginx)
- `ps -p <PID>`: to find the process having the PID
- `ps -p "$$"`: to do this in one command

**switches**:
- `a`: all
- `u`: convert userid's to usernames
- `x`: show processes not attached to a terminal (tty)

[ps: Clean way to only get parent processes?](https://stackoverflow.com/questions/12373309/ps-clean-way-to-only-get-parent-processes) - Stack Overflow

PPID: parent process id

### kill
- `kill -l`: list all types of kill commands. kill 15 is the default (or implied) which is SIGTERM.
- `kill 9 <PID>`: use with caution, can cause damage. 9 is SIGKILL

### pkill
look up or signal processes based on name & other attributes
- `sudo pkill -u user`: kill processes owned by user

### '/proc' filesystem
Where the kernel writes information about running processes. A virtual filesystem where the kernel is able to communicate with the user & any other program on the machine about the state of processes that are running. There will be a directory in /proc for each running process.
