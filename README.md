#Scheduling Algorithms
A Process Scheduler schedules different processes to be assigned to the CPU based on particular scheduling algorithms. There are four popular process scheduling algorithms which we are going to discus :-

1.First-Come, First-Served (FCFS) Scheduling
2.Shortest-Job-First (SJF) Scheduling
3.Priority Scheduling
4.Round Robin(RR) Scheduling

These algorithms are either non-preemptive or preemptive. Non-preemptive algorithms are designed so that once a process enters the running state, it cannot be preempted until it completes its allotted time, whereas the preemptive scheduling is based on priority where a scheduler may preempt a low priority running process anytime when a high priority process enters into a ready state.

##First Come First Serve (FCFS)
->Jobs are executed on first come, first serve basis.
->It is a non-preemptive, pre-emptive scheduling algorithm.
->Easy to understand and implement.
->Its implementation is based on FIFO queue.
->Poor in performance as average wait time is high.
