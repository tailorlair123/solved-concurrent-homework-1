Download Link: https://assignmentchef.com/product/solved-concurrent-homework-1
<br>
The purpose of this project is to get you used learn how to do a performance evaluation on a machine like Beocat.

<strong>Task(s)</strong>

Your first task is to take an existing program and indicate how the performance improves through using using two standard techniques – tiling and loop unrolling – in this serial code. In my directory on Beocat ~dan/625, there is a program called pt0.c, which creates a large array of characters and then counts them. Make yourself a copy and modify this code (in particular, the count_array() function) into two variants (pt0-tiled.c and pt0-unrolled.c). Your second task is to do a performance evaluation across a range of array sizes to see how the various versions match up in terms of run times, CPU efficiency, memory utilization, etc. You’ll want to keep the machines constant, so use the ‘-q *@@elves’ flag to confine your jobs to only the ‘elf’ class nodes.

I’ve provided code in the file mytime.c to illustrate how to time portions of code. Note that it also illustrates how to retrieve data from the program’s environment (in this case, SLURM_NTASKS, which is the number of cores you have). Also note – and <strong>this is important</strong> – the format of the output makes it easy to extract the data (using the ‘grep’ command) into a .csv file, which can be opened directly.

So if you wanted to be efficient about things, you would modify the various programs to accept the size of the array to be tested as an input argument, then use a script like the 625/mass_sbatch.sh to submit a bunch of jobs simultaneously, and then a ‘grep’ into a .csv file to quickly graph the output in Excel or a similar tool.

Read the discussion of performance analysis on Canvas, and make sure you discuss the applicable elements. You should run your jobs multiple times per data point and then average them to help smooth out individual variations. You should make sure you discuss how you selected the block size for your tiled implementation and the degree of loop unrolling (a graph to prove your point as to which was optimal would be great), and how you chose the array dimensions to do a reasonable evaluation of the algorithms’ performance.

<strong>Resources</strong>

Tiling – <a href="https://en.wikipedia.org/wiki/Loop_nest_optimization">https://en.wikipedia.org/wiki/Loop_nest_optimization</a>

Loop unrolling – <a href="https://en.wikipedia.org/wiki/Loop_unrolling">https://en.wikipedia.org/wiki/Loop_unrolling</a>




For help using the Beocat scheduler and its command lines, see the general help page

<a href="https://support.beocat.ksu.edu/BeocatDocs/index.php/Main_Page">https://support.beocat.ksu.edu/BeocatDocs/index.php/Main_Page</a>

and the scheduler help page

<a href="https://support.beocat.ksu.edu/BeocatDocs/index.php/SGEBasics">https://support.beocat.ksu.edu/BeocatDocs/index.php/SGEBasics</a>

Compute node specifications are at

<a href="https://support.beocat.ksu.edu/BeocatDocs/index.php/Compute_Nodes">https://support.beocat.ksu.edu/BeocatDocs/index.php/Compute_Nodes</a>




You will probably need to install a shell program on your Windows machine – I use PuTTY, and program to transfer files back and forth (I use WinSCP, but other options are fine). Linux and Mac OS have terminal and file transfer programs installed by default.