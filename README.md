# Day16-of-43-of-Teachersdaychallenge
. A. Xenia and Ringroad
Problem Description: Xenia starts at house 1 on a ringroad with n houses. She has m tasks to complete in a specific order at houses a1, a2, ..., am. The ringroad is one-way (clockwise). Find the minimum total time needed to complete all tasks, where each move to an adjacent house takes one unit of time.

Key Idea/Logic:

This problem can be solved with a greedy approach and a running sum.

We can track Xenia's current position and the total time elapsed.

Start at position 1 and time 0.

Iterate through the m tasks. For each task i at house ai:

Calculate the time needed to travel from the current_house to the next_house (ai).

If ai >= current_house, the time taken is simply ai - current_house.

If ai < current_house, Xenia must travel all the way around the ring. The time taken is (n - current_house) + ai.

Add this travel time to the total time.

Update current_house = ai.

Print the total time after all tasks are completed.

Example:
Input:

4 3
3 2 3
Output: 6
Explanation:

Start at house 1.

Task 1: Go to house 3. Time = 3-1 = 2. Total time = 2. Current house = 3.

Task 2: Go to house 2. Time = (4-3)+2 = 3. Total time = 2+3 = 5. Current house = 2.

Task 3: Go to house 3. Time = 3-2 = 1. Total time = 5+1 = 6. Current house = 3.

A. I Wanna Be the Guy
Problem Description: Little X can pass p levels and Little Y can pass q levels. Given the indices of the levels they can each pass, determine if they can collectively pass all n levels of a game (numbered 1 to n).

Key Idea/Logic:

The problem is to find if the union of the levels Little X can pass and Little Y can pass contains all levels from 1 to n.

The most efficient way to check for all unique levels is to use a set data structure.

Approach:

Create an empty set.

Read the levels Little X can pass and insert each level into the set.

Read the levels Little Y can pass and insert each level into the set.

After inserting all levels from both friends, check if the size of the set is equal to n.

If set.size() == n, print "I become the guy.". Otherwise, print "Oh, my keyboard!".

Time Complexity: O(P+Q) where P and Q are the number of levels Little X and Little Y can pass, as set insertions take, on average, constant time.

Space Complexity: O(N) in the worst case to store all n levels in the set.

Example:
Input:

4
3 1 2 3
2 2 4
Output: I become the guy.
Explanation:

Little X can pass levels {1, 2, 3}.

Little Y can pass levels {2, 4}.

The union is {1, 2, 3, 4}.

The size of the union is 4, which equals the total number of levels n.

Time Complexity: O(M) where M is the number of tasks, as we process each task once.

Space Complexity: O(M) to store the list of tasks, or O(1) if they are processed as they are read.
