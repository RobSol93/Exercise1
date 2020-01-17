# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to a repository to complete the task. Remember to also submit your answers to Blackboard

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is when more than one task starts and runs at virtually the same time. The CPU scheduler interleaves the tasks by giving each task some CPU time before moving on to the next.
 
 > Parallelism is when tasks can physically be run at the same time on different CPU cores. 
 
 
 ### Why have machines become increasingly multicore in the past decade?
 > Increase performance by being able to run more seperate tasks at once.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Problems where several processes are happening at the same time. Cash withdrawal from an account.
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > It increases complexity, but makes it easier to solve problems that require concurrency.
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > 
 
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > 'pthread_create()' : creates a thread
 
 > 'threading.Tread()' : creates a thread
 
 > 'go' : 
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > It is preventing multiple threads from executing Python bytecodes at once. Memory management is not thread-safe, so lock is necessary.
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Using subprocesses instead of threads by using the multiprocessing package.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > It changes the maximum number of CPUs that can be executing simultaneously
 
 
 ### Task 4
 > The variable is somewhere in the range of +-1000000. There is no perfectly fair scheduling of the two threads, which results in 'i' not being zero (which one might assume it would be).
