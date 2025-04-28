# cs1550-project2--process-synchronization-solved
**TO GET THIS SOLUTION VISIT:** [CS1550 Project2 -Process Synchronization Solved](https://www.ankitcodinghub.com/product/cs1550-project2-process-synchronization-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;52031&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS1550 Project2 -Process Synchronization Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
Anytime we share data between two or more processes or threads, we run the risk of having race conditions and deadlocks. In race conditions, the shared data could become corrupted. In order to avoid these situations, we have discussed various mechanisms to ensure that one process’s critical regions are guarded from another’s.

One place that we might use parallelism is to simulate real-world situations that involve multiple independently acting entities, such as people. In this project, you will use the semaphore implementation that you finished in Project 1<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> to model the <strong>safe museum tour problem</strong>, whereby visitors and museum tour guides synchronize so that:

<ul>
<li>a visitor cannot tour a museum without a tour guide,</li>
<li>a tour guide cannot open the museum without a visitor,</li>
<li>a tour guide leaves when no more visitors are in the museum,</li>
<li>a tour guide cannot leave until all visitors in the museum leave, &nbsp;&nbsp;&nbsp; at most <strong>two</strong> tour guides can be in the museum at a time, and</li>
<li>each tour guide provides a tour for <strong>at most</strong> <strong>ten</strong></li>
</ul>
Your job is to write a program that (a) always satisfies the above constraints and (b) under no conditions will cause a deadlock to occur. A deadlock happens, for example, when the museum is empty, a tour guide and a visitor arrive, and they stay waiting outside the museum forever.

<h1><a name="_Toc9905"></a>Project Details</h1>
&nbsp;

You are to write (a) the visitor process, (b) the tour guide process, and (c) <strong><u>six</u></strong> functions called by these processes:&nbsp; (c1) visitorArrives(), (c2) tourMuseum(),&nbsp; (c3) visitorLeaves(), (c4) tourguideArrives(), (c5) openMuseum(), and (c6) tourguideLeaves(). You will also write two processes, (d) one for simulating tour guides’ arrival and (e) the other for simulating visitors’ arrival.

<h2><a name="_Toc9906"></a>visitorArrives() and tourguideArrives()</h2>
&nbsp;

In order to open a museum for tours, there need to be at least one tour guide and one visitor.

visitorArrives() is called by visitor processes and tourguideArrives() is called by tour guide processes. Both functions must <strong>block</strong> until a tour guide <strong>and</strong> a visitor both arrive.

An arriving visitor must wait if

<ul>
<li>the museum is closed or</li>
</ul>
&nbsp;

<ul>
<li>the maximum number of visitors has been reached</li>
</ul>
An arriving tour guide must wait if

<ul>
<li>the museum is closed, and no visitor is waiting outside or</li>
<li>the museum is open, and two tour guides are inside the museum.</li>
</ul>
While only one tour guide is inside the museum,

<ul>
<li>up to ten visitors may arrive (i.e., call visitorArrives()) and</li>
<li>a second tour guide may open the museum (i.e., call openMuseum()).</li>
</ul>
When a tour guide arrives, the following message is printed to the screen:

Tour guide %d arrives at time %d.

When a visitor arrives, the following message is printed to the screen:

Visitor %d arrives at time %d.

<h2><a name="_Toc9907"></a>tourMuseum() and openMuseum()</h2>
&nbsp;

After tourguideArrives() returns, the tour guide immediately calls openMuseum(). After visitorArrives() returns, the visitor immediately calls tourMuseum(). Each visitor takes <strong>2 seconds</strong> to tour the museum (you can implement that by calling nanosleep or sleep). A visitor inside tourMuseum() must not block another visitor who is also inside tourMuseum().

When a tour guide opens the museum, the following message is printed to the screen:

Tour guide %d opens the museum for tours at time %d.

When a visitor tours the museum, the following message is printed to the screen:

Visitor %d tours the museum at time %d.

<h2><a name="_Toc9908"></a>visitorLeaves() and tourguideLeaves()</h2>
&nbsp;

Tour guides that are inside the museum cannot leave until all visitors inside the museum leave.

When a tour guide leaves, the following message should be printed to the screen:

Tour guide %d leaves the museum at time %d

When a visitor leaves, the following message should be printed to the screen:

Visitor %d leaves the museum at time %d

&nbsp;

<h2><a name="_Toc9909"></a>Visitor Arrival Process</h2>
&nbsp;

The visitor arrival process creates <em>m</em> visitor processes. The number of visitors, <em>m</em>, is read from a command-line argument (e.g., ./museumsim -m 10). Visitors arrive in bursts. When a visitor arrives, there is a <em>pv</em> (e.g., 70%) chance that another visitor is immediately arriving after her, but once no visitors arrive, there is a <em>dv</em> seconds (e.g., 20 seconds) delay before any new visitor arrives. The first visitor always arrives at time 0. The probability <em>pv</em> and the delay <em>dv</em> are to be read from the command-line (e.g., ./museumsim -pv 70 -dv 20).

<h2><a name="_Toc9910"></a>Tour guide Arrival Process</h2>
&nbsp;

The tour guide arrival process creates <em>k</em> tour guide processes. The number of tour guides, <em>k</em>, is read from a command-line argument (e.g., ./museumsim -k 10). Tour guides arrive in bursts. When a tour guide arrives, there is a <em>pg</em> (e.g., 30%) chance that another tour guide is immediately arriving after<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a> her, but once no tour guides arrive, there is a <em>dg</em> second (e.g., 30 seconds) delay before any new tour guide arrives. The first tour guide always arrives at time 0. The probability <em>pa</em> and the delay <em>da</em> are to be read from the command-line (e.g., ./museumsim -pa 30 -da 30).

<h2><a name="_Toc9911"></a>Requirements</h2>
&nbsp;

Your solution must use semaphores, should not use busy waiting, and should be deadlock-free.

<h2><a name="_Toc9912"></a>Testing</h2>
&nbsp;

Make sure to run various test cases against your solution; for instance, create k tour guides and m visitors (with various values of <em>k </em>and <em>m</em>, for example <em>k &gt; m, m &gt; k, k == m</em>), different values for the probabilities and delays, etc. Note that the exact order of the output messages can vary, within certain boundaries. These boundaries are checked by the autograder scripts.

<h2><a name="_Toc9913"></a>Program and Output Specs</h2>
&nbsp;

Create a program, museumsim, which runs the simulation. Your program should run as follows.

<ul>
<li>Fork a process for visitor arrival and a process for tour guide arrival, each in turn forking visitor processes and tour guide processes, respectively, at the appropriate times as specified by the command-line arguments.</li>
<li>To get an 80% chance of something, you can generate a random number modulo 100 and see if its value is less than 80. It’s like flipping an unfair coin. You may refer to CS 449 materials for how to generate a random number.</li>
</ul>
&nbsp;

<ul>
<li>Have the following command-line arguments:</li>
<li>-m: number of visitors</li>
<li>-k: number of tour guides</li>
<li>-pv: probability of a visitor immediately following another visitor</li>
<li>-dv: delay in seconds when a visitor does not immediately follow another visitor</li>
<li>-sv: random seed for the visitor arrival process</li>
<li>-pg: probability of a tour guide immediately following another tour guide</li>
<li>-dg: delay in seconds when a tour guide does not immediately follow another tour guide</li>
<li>-sg: random seed for the tour guide arrival process</li>
<li>Make sure that your <strong>output</strong> shows all the necessary events. You should sequentially number each visitor and tour guide starting from 0. Visitor numbers are independent of tour guide numbers. When the museum is empty, your program should display:</li>
</ul>
&nbsp;

The museum is now empty.

&nbsp;

<ul>
<li>Print out messages in the form:</li>
</ul>
&nbsp;

The museum is now empty.

Tour guide %d arrives at time %d.

Visitor %d arrives at time %d.

Tour guide %d opens the museum for tours at time %d.

Visitor %d tours the museum at time %d.

Visitor %d leaves the museum at time %d.

Tour guide %d leaves the museum at time %d.

&nbsp;

<ul>
<li>The printed time is in <strong>seconds since the start of the program</strong>. You should use the function gettimeofday and use both the seconds and microseconds fields in struct timeval in your calculation of the number of elapsed seconds.</li>
</ul>
&nbsp;

&nbsp;

<h2><a name="_Toc9914"></a>Shared Memory in our simulation</h2>
&nbsp;

To make our shared data and our semaphores, what we need is for multiple processes to be able to share the same memory region. We can ask for N bytes of RAM from the OS directly by using mmap(): void *ptr = mmap(NULL, N, PROT_READ|PROT_WRITE, MAP_SHARED|MAP_ANONYMOUS, 0, 0);

The return value will be the address of the start of the allocated memory. We can then steal portions of the allocated memory to hold our variables much like the malloc() project from CS 0449. For example, if we wanted two integers to be stored in the allocated region, we could do the following to allocate and initialize them.

int *first_sem; int *second_sem; first = (int *) ptr; second_sem = first_sem + 1;

*first_sem = 0;

*second_sem = 0;

&nbsp;

At this point we have one process and some RAM that contains our variables. But we now need to share that memory region/variables with other processes. The good news is that a mmap’ed region (with the MAP_SHARED flag) remains accessible in the child process after a fork(). Therefore, do the mmap() in main before fork() and then use the variables in the appropriate way afterwards.

<h2><a name="_Toc9915"></a>Building and Running museumsim</h2>
&nbsp;

Please use the instructions in Project 1 for building and running the test program (named trafficsim in

Project 1) to build and run museumsim. Make sure that the QEMU VM is running the modified kernel (with the down and up syscalls). Whenever you make a change to museumsim.c, you only to scp it into QEMU but you don’t need to reboot QEMU.

<h2><a name="_Toc9916"></a>Debugging</h2>
&nbsp;

Please use the following steps to run gdb inside the QEMU virtual machine:

&nbsp;

<strong>Inside the QEMU VM:</strong>

&nbsp;

scp PITT_ID@thoth.cs.pitt.edu:/u/OSLab/original/gdb/* .

mv gdb /bin/ mv libncurses.so.5 /lib mv libtinfo.so.5 /lib

gdb &lt;program name&gt;

&nbsp;

<strong>On thoth:</strong>

You will have to add the -g flag to the compilation command (typed on thoth) for the museumsim program.

&nbsp;

<strong>To run valgrind inside the QEMU VM: </strong>

&nbsp;

<strong>On QEMU:</strong>

scp -r PITT_ID@thoth.cs.pitt.edu:/u/OSLab/original/valgrind/* .

mv bin/* /bin/ mv lib/* /lib/ echo export VALGRIND_LIB=/lib/valgrind &gt;&gt; ~/.bashrc bash

valgrind ./&lt;program name with command-line arguments&gt;

&nbsp;

<a href="#_ftnref1" name="_ftn1">[1]</a> If you haven’t finished Project 1 or are not sure if your solution is correct, please download and use the modified kernel from CourseWeb.

<a href="#_ftnref2" name="_ftn2">[2]</a> Recall that at most two tour guides can be in the museum at a time.
