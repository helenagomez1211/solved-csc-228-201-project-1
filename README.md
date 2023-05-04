Download Link: https://assignmentchef.com/product/solved-csc-228-201-project-1
<br>
<strong><u>Project 1</u>: Dynamic Array Implementation of the List ADT: </strong><strong>Doubling the List Size vs. </strong>

<strong>Incrementing the List Size by One: <em>Memory and Run Time Analysis</em> </strong>

<strong> </strong>We saw in the dynamic array implementation of the List ADT that for frequent insertion, increasing the size of the List by 1 (one) memory unit is more likely not a better option than doubling the size of the List, whenever needed. In this project, we will verify whether this hypothesis is true from the perspectives of both memory usage and actual run time.




You are given the code (posted in Canvas) for the dynamic array implementation of the List ADT. The main function has the timers setup to measure the time it takes to insert a sequence of integers at the end of the List.




<h1>Doubling the List (Case i)</h1>

The current implementation of the <em>insertAtIndex</em> function in the code given to you doubles the size of the List whenever needed (i.e., calls the <em>resize </em>function with a value 2*<em>maxSize</em>). You could run the code as it is and measure the average time per integer insertion (in nanoseconds, as setup in the main function) for list size values of 1000, 2000, 3000, …, 10000 (in increments of 1000). For each list size, you will run 50 trials and average the time per insertion. For all list sizes and trials, the range of integers is [1…5000]; that is, <em>maxValue</em> is 5000.




<h1>Incrementing the size of the List by One</h1>

<strong>Case ii: </strong>Modify the <em>insertAtIndex</em> function code such that it calls the resize function with a value maxSize + 1. After the modification, run the code and measure the average time per integer insertion (as is done for Case i) for list size values ranging from 1000 to 10000, in increments of 1000. For all the list size values, the number of trials is 50 and the range of integers is [1…5000].

You could notice that your program stops with a <em>bad_alloc</em> error message for a certain value of list size and larger values henceforth (say, for list size of 6000 and larger). In that case, do some online research (for bad_alloc error message in C++) and reason out why you got the error message.

Now, continue running the program for larger list size values even if you get the bad_alloc error message. Note down the trial number at which the bad_alloc error message appears and your program stops. You could notice that the number of trials your program ran successfully and then stopped (due to the bad_alloc problem) decreases with increase in the list size values.

<strong>Case iii:</strong> Enhance the given code such that the program will run (while incrementing the list size by 1) for all the 50 trials without stopping with a bad_alloc error message. Collect the run times (in nano seconds) for list size values of 1000 to 10000 in increments of 1000; the range of the integers is [1…5000].





