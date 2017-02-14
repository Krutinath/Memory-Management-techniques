# Deadlock
A deadlock is a situation in which two computer programs sharing the same resource are effectively preventing each other from accessing the resource, resulting in both programs ceasing to function. The earliest computer operating systems ran only one program at a time.

##Deadlock Prevention
Deadlock prevention algorithms ensure that at least one of the necessary conditions (Mutual exclusion, hold and wait, no preemption and circular wait) does not hold true. However most prevention algorithms have poor resource utilization, and hence result in reduced throughputs.

**1.Mutual Exclusion**  
Not always possible to prevent deadlock by preventing mutual exclusion (making all resources shareable) as certain resources are cannot be shared safely.

**2.Hold and Wait**  
We will see two approaches, but both have their disadvantages.  
A resource can get all required resources before it start execution. This will avoid deadlock, but will result in reduced throughputs as resources are held by processes even when they are not needed. They could have been used by other processes during this time.  
Second approach is to request for a resource only when it is not holing any other resource. This may result in a starvation as all required resources might not be available freely always.

**3.No preemption**  
We will see two approaches here. If a process request for a resource which is held by another waiting resource, then the resource may be preempted from the other waiting resource. In the second approach, if a process request for a resource which are not readily available, all other resources that it holds are preempted.    
The challenge here is that the resources can be preempted only if we can save the current state can be saved and processes could be restarted later from the saved state.

**4.Circular wait**  
To avoid circular wait, resources may be ordered and we can ensure that each process can request resources only in an increasing order of these numbers. The algorithm may itself increase complexity and may also lead to poor resource utilization.

##Deadlock Detection  
If deadlock prevention and avoidance are not done properly, as deadlock may occur and only things left to do is to detect the recover from the deadlock.  
If all resource types has only single instance, then we can use a graph called wait-for-graph, which is a variant of resource allocation graph.So the system can maintain a wait-for-graph and check for cycles periodically to detect any deadlocks.  
The wait-for-graph is not much useful if there are multiple instances for a resource, as a cycle may not imply a deadlock. In such a case, we can use an algorithm similar to Banker’s algorithm to detect deadlock.
