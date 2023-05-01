Download Link: https://assignmentchef.com/product/solved-csc3002f-assignment4-synchronization
<br>
This assignment aims to give you experience in thread (and, by extension, process) synchronization using <strong>semaphores</strong>. In this project, you will write multithreaded programs in Java to solve <strong>three classic synchronization problems</strong>, using only semaphores.  A secondary aim is to give you experience in reading, understanding and correcting existing code.  The assignment is in three parts, increasing in difficulty.  The first part is described below.

<h1>1 Part I: Simple barrier with semaphores</h1>

In this first part of the assignment, you will implement a simple barrier in Java, using only<strong> semaphores</strong>.

A barrier is a synchronization construct that forces threads to wait until a fixed number of threads (<em>n) </em>have arrived at the barrier, whereupon they may all continue with their next step.

The <strong>synchronization requirement</strong> is that no thread may proceed until <em>n </em>threads have reached the barrier.  When the first <em>n-1</em> threads arrive, they should block until the <em>n</em>th thread arrives, whereupon all threads may proceed.

Note that for this task <strong>you must only implement a simple barrier</strong>, not a reusable barrier.   The barrier implemented <strong>must be deadlock free</strong>.

1.1 Code skeleton: BarrierS

You <strong>must use</strong> and extend the BarrierS <strong>package provided</strong>, correctly implementing the Barrier    class (and the           b_wait()     method), so that the BarrierTest class will execute correctly, <strong>always</strong>.   This will not require many lines of code. <strong>Do not alter</strong> the            BarrierTest          or the   BThread classes in the package (although you must submit them).  You will need to inspect the various classes to see how they work – this is part of the assignment and no explanation other than the code will be given.

An example of a correct execution of BarrierTest          is:

<ul>

 <li>java BarrierS.BarrierTest 5 5</li>

</ul>

Starting simulation with 5 threads, barrier size 5

Parent thread completed

Thread 1 waiting at barrier.

Thread 3 waiting at barrier.

Thread 0 waiting at barrier.

Thread 2 waiting at barrier.

Thread 4 waiting at barrier.

Thread 4 passed barrier.

Thread 1 passed barrier.

Thread 2 passed barrier.

Thread 0 passed barrier.

Thread 3 passed barrier.

<h1>1 Code requirements</h1>

You will code your solutions in Java, adding to the skeleton code provided.

You may only use the <strong>Semaphore</strong> class in the java.util.concurrent library: <strong>no other Java synchronization constructs at all</strong>.

All code must be <strong>deadlock free. </strong>

The output must comply with the stated synchronization constraints and with the examples shown.