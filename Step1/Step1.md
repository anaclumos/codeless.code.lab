# Codeless Code Lab

## Script

Welcome to Codeless Code Lab where you will learn computer science knowledge without a bunch of codes.

In this section of codeless code lab, by solving the problem "Jumping Stairs," you will understand the concept of dynamic programming, recursion, memoization, and tabulation.

This video also has a Korean Version, linked in the description.

So let's explore the "Jumping stairs" problem. A rabbit is in front of a 6 step stair. On the top of the stair, there is a carrot. The rabbit wants to get the carrot. However, rabbit can only jump one or two steps at a time. Rabbit can ask itself; how many distincts ways are there to climb the stairs and get the carrot?

For example, the rabbit can jump 1 steps 6 times. Or maybe, it can jump two steps first and then jump 1 step 5 times. There are several combinations like this. This problem is too complex to solve at once, since we may forget to count some cases.

So, rather than jumping into a huge problem at first, let's water down the problem. Let's think of a smaller cases. What about a staircase of 1 step? The answer would be "climb up 1 step." So the total combination number would be 1.

Now let's take a look at a staircase of 2 steps. The rabbit can jump one step twice, or jump two steps once. So the total combination number would be two.

Staircase of 3 steps will be similar. Rabbit can jump 1 step 3 times, 1 step and then 2 steps, or reversed. The rabbit needs to climb three steps, so the steps of each jumps should add up to three total steps. There are three distinct combinations of this.

For staircase with 4 steps, Rabbit can jump 1 step 4 times, two 1 step and then 2 steps rearranged, or two steps twice. Similarly, the steps of each jumps should add up to four total steps. There are five distinct combinations of this.

For staircase with 5 steps, there are 8 combinations. Those who are curious with the combinations, please pause the video.
Now, you may find out some pattern.

1 plus 2 is 3. 2 plus 3 is 5 as well. 3 plus 5 is 8. This seems strange. Each staircase combination is the addition of two previous staircases. So, we can guess that staircase of 6 will have 13 distinct ways of climbing the stairs, which is correct. Try to find all the combination of climbing staircase of step 6. You will get the same answer.

But why does this happen? To figure out, let's explore the case of staircase of 4 steps. Initally, the rabbit has two choices. It can jump up one step. I will call this choice 1. Or, it can jump up two steps. I will call this choice 2. Since there are no other choice the rabbit can make at the beginning, we can say this. Staircase problem of step 4, Denoted as SP(4), is the addition of total case number from choice 1 and total case number of choice 2. We can say this because selecting choice 1 or 2 is mutually exclusive, but completely exhaustive. Two choices are distinct, but they include all the cases.

So let's explore the first choice. After climbing one step, the first floor is meaningless. So less remove this part. Removing this part, you will see that the remaining problem is the exact same problem with finding staircase problem with 3 steps. Also considering choice 2, let's ignore the previous two steps. Then you will figure that this is the exact same problem with staircase problem with two steps. Just like this, we can generalize this to SP(N) is SP(N-1) plus SP(N-2), where N is a natural number bigger than 2. SP(N-1) is from choice 1, anc SP(N-2) is from choice 2. Let's generalize this method to find the value of SP(N). Although there is a general solution for this SP(N), a fibonacci sequence, but for the sake of explaining the computer science concepts, let's explore this topic.

To find SP(N), we can approach from two sides. Top-down, and bottom-up. Let's explore from the first step. 

## Sources

Wikipedia
Geeksforgeeks
Stackoverflow