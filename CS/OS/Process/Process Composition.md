- Memory
	- [[Code]]
	- [[Data]]
	- [[Stack]]
	- [[Heap]]
- Registers
	- Program Counter
	- [[Stack]] Pointer
		- [[Stack]]의 최상단을 point하여 다음에 들어올 것이 저장될 위치를 가리킴

```
// the registers xv6 will save and restore
// to stop and subsequently restart a process

struct context {
	int eip; // Index pointer register
	int esp; // Stack pointer register
	int ebx; // Called the base register
	int ecx; // Called the counter register
	int edx; // Called the data register
	int esi; // Source index register
	int edi; // Destination index register
	int ebp; // Stack base pointer register
};
// the different states a process can be in
enum proc_state {UNUSED, EMBRYO, SLEEPING, RUNNABLE, RUNNING, ZOMBIE};

/*
UNUSED: UNUSED
EMBRYO: INIT
SLEEPING: BLOCKED
RUNNABLE: READY
RUNNING: RUNNING
ZOMBIE: ZOMBIE
*/

// the information xv6 tracks about each process
// including its register context and state

struct proc {

	char *mem; // Start of process memory
	uint sz; // Size of process memory
	char *kstack; // Bottom of kernel stack for this process

	enum proc_state state; // Process state
	int pid; // Process ID
	struct proc *parent; // Parent process
	void *chan; // If non-zero, sleeping on chan
	int killed; // If non-zero, have been killed
	struct file *ofile[NOFILE]; // Open files
	struct inode *cwd; // Current directory
	struct context context; // Switch here to run process
	struct trapframe *tf; // Trap frame for the current interrupt
};
```
