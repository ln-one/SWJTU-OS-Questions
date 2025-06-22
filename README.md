# Operating System Core Concepts (50 Questions)
# 操作系统核心概念（50题）

---

## Question 1  
**Define "Process". 定义"进程"。**  
**Answer:**  
A process is a program in execution. It is the basic unit of work in an operating system, consisting of program code, data, stack, and process control block.  
进程是正在执行的程序。它是操作系统中的基本工作单位，由程序代码、数据、栈和进程控制块组成。

---

## Question 2  
**What are the four necessary conditions for deadlock to occur? 死锁发生的四个必要条件是什么？**  
**Answer:**  
1. Mutual Exclusion: Resources cannot be shared
2. Hold and Wait: Processes hold resources while waiting for others
3. No Preemption: Resources cannot be forcibly taken
4. Circular Wait: A circular chain of processes waiting for resources

1. 互斥条件：资源不能共享
2. 持有并等待：进程持有资源的同时等待其他资源
3. 非抢占：资源不能被强制剥夺
4. 循环等待：存在一个进程等待资源的循环链

---

## Question 3  
**What is the difference between a process and a thread? 进程和线程的区别是什么？**  
**Answer:**  
Processes have separate memory spaces, while threads within the same process share memory. Processes are heavyweight with higher context switching overhead, while threads are lightweight. Each process has its own PCB, while threads share the PCB but have their own thread control blocks.  
进程拥有独立的内存空间，而同一进程内的线程共享内存。进程是重量级的，上下文切换开销高，而线程是轻量级的。每个进程有自己的PCB，而线程共享PCB但有自己的线程控制块。

---

## Question 4  
**What is "Virtual Memory"? 什么是"虚拟内存"？**  
**Answer:**  
Virtual memory is a memory management technique that provides an idealized abstraction of the storage resources actually available, enabling a process to execute with only a portion of its address space in main memory.  
虚拟内存是一种内存管理技术，提供实际可用存储资源的理想化抽象，使进程只需将其地址空间的一部分加载到主存中就能执行。

---

## Question 5  
**What are the three states of a process in the basic process state diagram? 基本进程状态图中进程的三种状态是什么？**  
**Answer:**  
1. Running: Process is executing on the CPU
2. Ready: Process is ready to execute when given CPU time
3. Blocked (Waiting): Process is waiting for an event or resource

1. 运行：进程正在CPU上执行
2. 就绪：进程准备好在获得CPU时间时执行
3. 阻塞（等待）：进程正在等待某个事件或资源

---

## Question 6  
**Define "Critical Section". 定义"临界区"。**  
**Answer:**  
A critical section is a segment of code where shared resources are accessed and modified. Only one process should execute in its critical section at a time to maintain data consistency.  
临界区是访问和修改共享资源的代码段。为了保持数据一致性，任何时候只能有一个进程在其临界区中执行。

---

## Question 7  
**What are the three requirements for a critical section solution? 临界区解决方案的三个要求是什么？**  
**Answer:**  
1. Mutual Exclusion: Only one process in critical section at a time
2. Progress: If no process is in the critical section, one waiting process must be able to enter
3. Bounded Waiting: A process cannot wait indefinitely to enter its critical section

1. 互斥：任何时候只有一个进程在临界区中
2. 进展：如果没有进程在临界区中，则必须让一个等待进程进入
3. 有限等待：一个进程不能无限期地等待进入其临界区

---

## Question 8  
**What is "Context Switch"? 什么是"上下文切换"？**  
**Answer:**  
A context switch is the process of saving the state (context) of a currently running process so it can be resumed later, and loading the state of another process for execution.  
上下文切换是保存当前运行进程的状态（上下文）以便稍后恢复，并加载另一个进程的状态以便执行的过程。

---

## Question 9  
**Define "Process Control Block (PCB)". 定义"进程控制块(PCB)"。**  
**Answer:**  
PCB is a data structure containing all the information about a process, including process state, program counter, CPU registers, memory management information, accounting information, and I/O status information.  
PCB是包含进程所有信息的数据结构，包括进程状态、程序计数器、CPU寄存器、内存管理信息、账户信息和I/O状态信息。

---

## Question 10  
**What is "Paging"? 什么是"分页"？**  
**Answer:**  
Paging is a memory management scheme that divides physical memory into fixed-size blocks called frames and logical memory into blocks of the same size called pages. It eliminates external fragmentation and allows non-contiguous memory allocation.  
分页是一种内存管理方案，将物理内存分为称为帧的固定大小块，将逻辑内存分为相同大小的称为页的块。它消除了外部碎片化并允许非连续内存分配。

---

## Question 11  
**Define "Semaphore". 定义"信号量"。**  
**Answer:**  
A semaphore is a synchronization tool with an integer value and two atomic operations (wait/P and signal/V) used to control access to shared resources and coordinate process execution.  
信号量是一种同步工具，具有整数值和两个原子操作（wait/P和signal/V），用于控制对共享资源的访问并协调进程执行。

---

## Question 12  
**What is "CPU Scheduling"? 什么是"CPU调度"？**  
**Answer:**  
CPU scheduling is the process of determining which process in the ready queue should be allocated the CPU. It aims to optimize CPU utilization, throughput, and response time.  
CPU调度是确定就绪队列中哪个进程应该分配CPU的过程。它旨在优化CPU利用率、吞吐量和响应时间。

---

## Question 13  
**What are the five states in the extended process state transition diagram? 扩展进程状态转换图中的五种状态是什么？**  
**Answer:**  
1. New: Process is being created
2. Ready: Process is ready to be executed
3. Running: Process is being executed by CPU
4. Blocked: Process is waiting for an event
5. Exit: Process has finished execution

1. 新建：进程正在被创建
2. 就绪：进程准备好被执行
3. 运行：进程正在被CPU执行
4. 阻塞：进程正在等待一个事件
5. 退出：进程已完成执行

---

## Question 14  
**Define "Thrashing". 定义"抖动"。**  
**Answer:**  
Thrashing occurs when a system spends more time swapping pages in and out of memory (paging) than executing application code, drastically reducing system performance.  
抖动是指系统花费更多时间在内存中换入换出页面（分页）而不是执行应用程序代码，从而大幅降低系统性能的情况。

---

## Question 15  
**What is "Interrupt"? 什么是"中断"？**  
**Answer:**  
An interrupt is a signal to the processor indicating an event that needs immediate attention. It causes the processor to save its current execution state and transfer control to an interrupt handler routine.  
中断是向处理器发出的表示需要立即处理事件的信号。它导致处理器保存当前执行状态并将控制转移给中断处理程序。

---

## Question 16  
**Define "Mutex". 定义"互斥锁"。**  
**Answer:**  
A mutex (mutual exclusion) is a synchronization mechanism that allows only one thread to access a shared resource at a time. It has two states: locked and unlocked.  
互斥锁是一种同步机制，一次只允许一个线程访问共享资源。它有两种状态：锁定和未锁定。

---

## Question 17  
**What is the difference between preemptive and non-preemptive scheduling? 抢占式调度和非抢占式调度的区别是什么？**  
**Answer:**  
In preemptive scheduling, the CPU can be taken away from a process before it completes execution based on priority or time slice. In non-preemptive scheduling, once a process gets the CPU, it keeps it until completion or voluntarily yields it.  
在抢占式调度中，CPU可以基于优先级或时间片在进程完成执行之前被剥夺。在非抢占式调度中，一旦进程获得CPU，它将保持使用直到完成或自愿放弃。

---

## Question 18  
**What is "Segmentation"? 什么是"分段"？**  
**Answer:**  
Segmentation is a memory management technique that divides a program into logical segments (code, data, stack) of varying sizes. Each segment has a base address and length, supporting the programmer's view of memory.  
分段是一种内存管理技术，将程序划分为不同大小的逻辑段（代码、数据、栈）。每个段有一个基地址和长度，支持程序员对内存的视图。

---

## Question 19  
**Define "Race Condition". 定义"竞态条件"。**  
**Answer:**  
A race condition occurs when multiple processes or threads access and manipulate shared data concurrently, and the outcome depends on the particular order of execution.  
竞态条件是指多个进程或线程并发访问和操作共享数据，其结果取决于特定的执行顺序的情况。

---

## Question 20  
**What are the four strategies for handling deadlocks? 处理死锁的四种策略是什么？**  
**Answer:**  
1. Prevention: Ensure at least one of the four necessary conditions cannot occur
2. Avoidance: Dynamically examine resource allocation requests to ensure safety
3. Detection and Recovery: Allow deadlocks to occur, detect them, and recover
4. Ignorance: Pretend deadlocks never occur (ostrich algorithm)

1. 预防：确保四个必要条件中至少有一个不会发生
2. 避免：动态检查资源分配请求以确保安全
3. 检测和恢复：允许死锁发生，检测它们，并进行恢复
4. 忽略：假装死锁从不发生（鸵鸟算法）

---

## Question 21  
**Define "Monitor". 定义"管程"。**  
**Answer:**  
A monitor is a high-level synchronization construct containing shared variables and procedures that can only be accessed by one process at a time, providing mutual exclusion automatically.  
管程是一种高级同步构造，包含共享变量和过程，一次只能被一个进程访问，自动提供互斥。

---

## Question 22  
**What is "Demand Paging"? 什么是"请求分页"？**  
**Answer:**  
Demand paging is a virtual memory management technique where pages are loaded into physical memory only when they are referenced, rather than loading the entire process at once.  
请求分页是一种虚拟内存管理技术，仅当页面被引用时才将其加载到物理内存中，而不是一次加载整个进程。

---

## Question 23  
**What is "Page Fault"? 什么是"页面错误"？**  
**Answer:**  
A page fault occurs when a process references a page that is not currently in physical memory, causing the operating system to retrieve it from secondary storage.  
页面错误发生在进程引用当前不在物理内存中的页面时，导致操作系统从辅助存储器中检索它。

---

## Question 24  
**Define "Starvation". 定义"饥饿"。**  
**Answer:**  
Starvation is a problem where a process is indefinitely denied necessary resources due to allocation algorithms favoring other processes.  
饥饿是指由于分配算法偏向其他进程，导致一个进程被无限期地拒绝必要资源的问题。

---

## Question 25  
**What is "Round Robin Scheduling"? 什么是"轮转调度"？**  
**Answer:**  
Round Robin is a CPU scheduling algorithm where each process is assigned a fixed time slice in a cyclic order. If a process doesn't complete in its time quantum, it's placed at the end of the ready queue.  
轮转调度是一种CPU调度算法，每个进程按循环顺序分配固定的时间片。如果进程在其时间量子内没有完成，它将被放置在就绪队列的末尾。

---

## Question 26  
**Define "Priority Inversion". 定义"优先级反转"。**  
**Answer:**  
Priority inversion occurs when a higher-priority process is indirectly preempted by a lower-priority process, typically when the higher-priority process needs a resource held by a medium-priority process that is preempted by a lower-priority process.  
优先级反转发生在高优先级进程被低优先级进程间接抢占时，通常是当高优先级进程需要一个被中优先级进程持有的资源，而该中优先级进程被低优先级进程抢占。

---

## Question 27  
**What is "Page Replacement"? 什么是"页面替换"？**  
**Answer:**  
Page replacement is the process of selecting which page in memory should be swapped out when a new page needs to be brought in and memory is full.  
页面替换是在需要引入新页面且内存已满时，选择应该被换出的内存中页面的过程。

---

## Question 28  
**What are the three components of a Message Passing Interface? 消息传递接口的三个组成部分是什么？**  
**Answer:**  
1. Send operation
2. Receive operation
3. Message content/format

1. 发送操作
2. 接收操作
3. 消息内容/格式

---

## Question 29  
**Define "TLB (Translation Lookaside Buffer)". 定义"TLB（转换旁路缓冲器）"。**  
**Answer:**  
TLB is a memory cache that stores recent translations of virtual memory to physical memory addresses, speeding up the address translation process.  
TLB是一种内存缓存，存储虚拟内存到物理内存地址的最近转换，加速地址转换过程。

---

## Question 30  
**What are the three allocation methods for disk space? 磁盘空间的三种分配方法是什么？**  
**Answer:**  
1. Contiguous allocation: Files occupy contiguous blocks
2. Linked allocation: Each block contains a pointer to the next block
3. Indexed allocation: All pointers are stored in an index block

1. 连续分配：文件占用连续的块
2. 链接分配：每个块包含指向下一个块的指针
3. 索引分配：所有指针存储在索引块中

---

## Question 31  
**Define "Spooling". 定义"假脱机"。**  
**Answer:**  
Spooling (Simultaneous Peripheral Operation On-Line) is a technique where data for a slow I/O device is temporarily held in a buffer, allowing the CPU to continue processing without waiting for the device.  
假脱机（外围设备联机同步操作）是一种将慢速I/O设备数据临时保存在缓冲区的技术，允许CPU继续处理而不必等待设备。

---

## Question 32  
**What is "Long-term Scheduling"? 什么是"长期调度"？**  
**Answer:**  
Long-term scheduling (job scheduling) decides which jobs to admit into the system for processing. It controls the degree of multiprogramming by determining how many processes should be in memory.  
长期调度（作业调度）决定哪些作业被允许进入系统处理。它通过确定内存中应有多少进程来控制多道程序设计的程度。

---

## Question 33  
**Define "Bounded-Buffer Problem". 定义"有界缓冲区问题"。**  
**Answer:**  
The bounded-buffer problem involves a shared fixed-size buffer where producers must wait if the buffer is full, and consumers must wait if the buffer is empty, requiring synchronization.  
有界缓冲区问题涉及一个共享的固定大小缓冲区，若缓冲区满，生产者必须等待；若缓冲区空，消费者必须等待，需要同步机制。

---

## Question 34  
**What is "Banker's Algorithm"? 什么是"银行家算法"？**  
**Answer:**  
Banker's Algorithm is a deadlock avoidance algorithm that determines if granting a resource request would leave the system in a safe state by simulating resource allocation and checking if all processes can still complete.  
银行家算法是一种死锁避免算法，通过模拟资源分配并检查所有进程是否仍能完成，来确定授予资源请求是否会使系统处于安全状态。

---

## Question 35  
**Define "Process Migration". 定义"进程迁移"。**  
**Answer:**  
Process migration is the act of transferring a process from one computer to another while it is executing, typically used in distributed systems for load balancing and resource utilization.  
进程迁移是指在进程执行时将其从一台计算机转移到另一台计算机，通常用于分布式系统中的负载平衡和资源利用。

---

## Question 36  
**What is "Cache Coherence"? 什么是"缓存一致性"？**  
**Answer:**  
Cache coherence ensures that multiple copies of the same memory block across different caches remain consistent when the block is updated by any processor in a multiprocessor system.  
缓存一致性确保当多处理器系统中的任何处理器更新内存块时，不同缓存中相同内存块的多个副本保持一致。

---

## Question 37  
**What are the four main components of a computer system? 计算机系统的四个主要组成部分是什么？**  
**Answer:**  
1. Hardware: CPU, memory, I/O devices
2. Operating System: Controls and coordinates hardware use
3. Application Programs: Define ways system resources are used
4. Users: People, machines, other computers

1. 硬件：CPU、内存、I/O设备
2. 操作系统：控制和协调硬件使用
3. 应用程序：定义系统资源的使用方式
4. 用户：人员、机器、其他计算机

---

## Question 38  
**Define "RAID (Redundant Array of Independent Disks)". 定义"RAID（独立磁盘冗余阵列）"。**  
**Answer:**  
RAID is a technology that combines multiple disk drives into a logical unit for data redundancy and/or performance improvement, offering various configurations (levels) with different balances of protection, performance, and cost.  
RAID是一种技术，将多个磁盘驱动器组合成一个逻辑单元，用于数据冗余和/或性能改进，提供不同配置（级别），平衡保护、性能和成本。

---

## Question 39  
**What is "File System Mounting"? 什么是"文件系统挂载"？**  
**Answer:**  
File system mounting is the process of making a file system accessible to users by attaching it to an existing directory structure at a mount point.  
文件系统挂载是通过将文件系统附加到现有目录结构的挂载点，使文件系统可供用户访问的过程。

---

## Question 40  
**Define "Resident Set". 定义"驻留集"。**  
**Answer:**  
The resident set is the portion of a process's address space that is currently in physical memory rather than swapped out to secondary storage.  
驻留集是进程地址空间中当前在物理内存中而非被换出到辅助存储的部分。

---

## Question 41  
**What are the five main services provided by an operating system? 操作系统提供的五个主要服务是什么？**  
**Answer:**  
1. Program execution
2. I/O operations
3. File system manipulation
4. Communications
5. Error detection and response

1. 程序执行
2. I/O操作
3. 文件系统操作
4. 通信
5. 错误检测和响应

---

## Question 42  
**Define "Short-term Scheduling". 定义"短期调度"。**  
**Answer:**  
Short-term scheduling (CPU scheduling) decides which process in the ready queue should be allocated the CPU. It occurs very frequently, making decisions in milliseconds.  
短期调度（CPU调度）决定就绪队列中哪个进程应该分配CPU。它非常频繁地发生，以毫秒为单位做出决策。

---

## Question 43  
**What is "Readers-Writers Problem"? 什么是"读者-写者问题"？**  
**Answer:**  
The readers-writers problem involves synchronizing multiple processes where some read from a shared resource (readers) and others modify it (writers). Multiple readers can access simultaneously, but writers need exclusive access.  
读者-写者问题涉及同步多个进程，其中一些从共享资源读取（读者）而其他进程修改它（写者）。多个读者可以同时访问，但写者需要独占访问。

---

## Question 44  
**Define "Kernel Mode". 定义"内核模式"。**  
**Answer:**  
Kernel mode is a privileged execution mode of the CPU where the executing code has complete and unrestricted access to the underlying hardware and can execute any instruction and reference any memory address.  
内核模式是CPU的特权执行模式，执行代码对底层硬件有完全且无限制的访问权，可以执行任何指令并引用任何内存地址。

---

## Question 45  
**What is "Medium-term Scheduling"? 什么是"中期调度"？**  
**Answer:**  
Medium-term scheduling involves temporarily removing processes from memory (swapping) to reduce system load and improve the degree of multiprogramming, based on criteria like priority and memory needs.  
中期调度涉及基于优先级和内存需求等标准，暂时从内存中移除进程（交换），以减少系统负载并改善多道程序设计程度。

---

## Question 46  
**Define "I/O-Bound Process". 定义"I/O密集型进程"。**  
**Answer:**  
An I/O-bound process spends more time doing I/O operations than computations, often blocking for I/O and using only short CPU bursts.  
I/O密集型进程花费更多时间进行I/O操作而不是计算，经常因I/O而阻塞，只使用短暂的CPU突发。

---

## Question 47  
**What are the three main design issues for semaphores? 信号量的三个主要设计问题是什么？**  
**Answer:**  
1. Mutual exclusion enforcement
2. Progress requirement satisfaction
3. Bounded waiting implementation

1. 互斥执行的强制
2. 进展需求的满足
3. 有限等待的实现

---

## Question 48  
**Define "Fragmentation". 定义"碎片化"。**  
**Answer:**  
Fragmentation is the phenomenon where memory or disk space is divided into small, non-contiguous blocks. Internal fragmentation occurs when allocated memory is larger than requested, while external fragmentation occurs when free memory is available in small, scattered chunks.  
碎片化是内存或磁盘空间被分割成小的、非连续块的现象。当分配的内存大于请求的内存时发生内部碎片化，当可用内存以小的、分散的块存在时发生外部碎片化。

---

## Question 49  
**What is "Optimal Page Replacement Algorithm"? 什么是"最优页面替换算法"？**  
**Answer:**  
The optimal page replacement algorithm replaces the page that will not be used for the longest period of time in the future. It guarantees the lowest possible page fault rate but is not implementable in practice since it requires future knowledge.  
最优页面替换算法替换未来最长时间内不会被使用的页面。它保证最低可能的页面错误率，但在实践中无法实现，因为它需要未来的知识。

---

## Question 50  
**Define "Distributed System". 定义"分布式系统"。**  
**Answer:**  
A distributed system is a collection of independent computers that appears to users as a single coherent system. These systems share resources, use communication networks for coordination, and aim for transparency, reliability, and improved performance.  
分布式系统是对用户表现为单一连贯系统的独立计算机的集合。这些系统共享资源，使用通信网络进行协调，并追求透明性、可靠性和性能提升。
