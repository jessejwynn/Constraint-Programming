# Assignment 2 Specification - Compare Solvers

In this assignment you will compare the performance of two styles of solver on a graph-defense problem related to the firefighter problem that we will discuss in lecture.  You will implement both:
- a CP model for this problem in MiniZinc (callable within Python), and 
- an ILP model callable in Python using either OR-tools or PuLP 

I will provide stub code that shows how I will run your models.  The correctness of your models will be assessed automatically, so it is important that your code runs exactly as I would expect it to.  

## The Problem:
You will implement both a CP and an ILP model for the Infectious Defence Firefighter Problem.  In this problem, you are given as input a graph $G = (V, E)$ with a root $r$ denoting the starting point of the fire.  Then, on each turn the following happens in this order:
1. You choose an additional unburning vertex to defend
2. All undefended vertices that are adjacent to a burning vertex catch fire
3. All unburning and undefended vertices that are adjacent to a defended vertex become defended.  

The process ends when there are no burning vertices adjacent to undefended unburning vertices - that is, the fire can spread no further.  The number of vertices *saved* is the number of unburning vertices at the end of the process.  Note that the main difference between this process and the firefighter game that we discussed in lecture is that here the defence spreads.

## Task 1: (weighted 10\%)
Implement a CP model for this problem in MiniZinc.  Details of code that will call your model (in Python) to follow.  I will assess the correctness and efficiency of your model automatically.

## Task 2: (weighted 10\%)
Implement an ILP model for this problem using either PuLP or OR-Tools.  Details of code that will call your model (in Python) to follow.  I will assess the correctness and efficiency of your model automatically.

## Task 3: (weighted 80\%)
Write *at most one page* comparing the performance of your CP and your ILP models.  This should include a short section describing any interesting insights that you used in designing your models, a section outlining your experimental pipeline and why you have chosen to design it as you have, a plot or table showing the performances of the two models, and a section describing what you see in the results.  Submit this as a PDF.  Do not submit more than one page.  We will only read and mark one page.  
