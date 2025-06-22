# Operating System Concept Definition Questions (15 Questions)

---

## Question 1  
**Define "Process". 定义"进程"。**  
**Answer:**  
A process is a program in execution. It is the basic unit for resource allocation and scheduling in an operating system.  
进程是正在执行的程序。它是操作系统中资源分配和调度的基本单位。

---

## Question 2  
**What is a "Thread"? 什么是"线程"？**  
**Answer:**  
A thread is a lightweight execution unit within a process. It shares memory with other threads in the same process but has its own stack and registers.  
线程是进程内的轻量级执行单元。它与同一进程中的其他线程共享内存，但拥有自己的栈和寄存器。

---

## Question 3  
**Define "Deadlock". 定义"死锁"。**  
**Answer:**  
Deadlock occurs when two or more processes are blocked forever, each waiting for resources held by the others.  
死锁是指两个或多个进程永远被阻塞，每个进程都在等待其他进程持有的资源。

---

## Question 4  
**What is "Virtual Memory"? 什么是"虚拟内存"？**  
**Answer:**  
Virtual memory is a technique that allows programs to use more memory than physically available by using disk storage as an extension of RAM.  
虚拟内存是一种技术，通过使用磁盘存储作为RAM的扩展，允许程序使用比物理可用内存更多的内存。

---

## Question 5  
**Define "Critical Section". 定义"临界区"。**  
**Answer:**  
A critical section is a code segment where shared resources are accessed. Only one process can execute in its critical section at a time.  
临界区是访问共享资源的代码段。在任何时候只有一个进程可以在其临界区中执行。

---

## Question 6  
**What is "Paging"? 什么是"分页"？**  
**Answer:**  
Paging divides memory into fixed-size blocks called pages (logical) and frames (physical). It eliminates external fragmentation.  
分页将内存划分为固定大小的块，称为页（逻辑）和帧（物理）。它消除了外部碎片。

---

## Question 7  
**Define "Semaphore". 定义"信号量"。**  
**Answer:**  
A semaphore is a synchronization tool with an integer value and two operations: wait() and signal(). It controls access to shared resources.  
信号量是一个同步工具，具有整数值和两个操作：wait()和signal()。它控制对共享资源的访问。

---

## Question 8  
**What is "System Call"? 什么是"系统调用"？**  
**Answer:**  
A system call is an interface that allows user programs to request services from the operating system kernel.  
系统调用是允许用户程序向操作系统内核请求服务的接口。

---

## Question 9  
**Define "Process Scheduling". 定义"进程调度"。**  
**Answer:**  
Process scheduling is the method of selecting which process runs next on the CPU from the ready queue.  
进程调度是从就绪队列中选择下一个在CPU上运行的进程的方法。

---

## Question 10  
**What is "Interrupt"? 什么是"中断"？**  
**Answer:**  
An interrupt is a signal that stops the current program execution and transfers control to an interrupt handler.  
中断是停止当前程序执行并将控制权转移给中断处理程序的信号。

---

## Question 11  
**Define "Mutual Exclusion". 定义"互斥"。**  
**Answer:**  
Mutual exclusion ensures that only one process can access a shared resource or critical section at any given time.  
互斥确保在任何给定时间只有一个进程可以访问共享资源或临界区。

---

## Question 12  
**What is "Context Switch"? 什么是"上下文切换"？**  
**Answer:**  
Context switch is the process of saving the state of a running process and loading the state of another process.  
上下文切换是保存正在运行进程状态并加载另一个进程状态的过程。

---

## Question 13  
**Define "File System". 定义"文件系统"。**  
**Answer:**  
A file system is a method for storing and organizing files on storage devices. It manages file allocation and access.  
文件系统是在存储设备上存储和组织文件的方法。它管理文件分配和访问。

---

## Question 14  
**What is "PCB (Process Control Block)"? 什么是"PCB（进程控制块）"？**  
**Answer:**  
PCB is a data structure that contains information about a process, including process state, program counter, and CPU registers.  
PCB是包含进程信息的数据结构，包括进程状态、程序计数器和CPU寄存器。

---

## Question 15  
**Define "Thrashing". 定义"抖动"。**  
**Answer:**  
Thrashing occurs when a system spends more time swapping pages than executing processes due to excessive page faults.  
当系统由于过多的页面错误而花更多时间交换页面而不是执行进程时，就会发生抖动。

---
