Download Link: https://assignmentchef.com/product/solved-comp202-assignment-2
<br>
<span class="kksr-muted">Rate this product</span>




This programming assignment will test your knowledge and your implementation abilities of what you have learned in the Lists, Stacks, and Queues parts of the class.

This homework must be completed individually. Discussion about algorithms and data structures are allowed but group work is not. Any academic dishonesty, which includes taking someone else’s code or having another person doing the assignment for you will not be tolerated. By submitting your assignment, you agree to abide by the Ko ̧c University codes of conduct.

Description

This assignment is designed to assess your understanding of Arrays, Linked Lists, Stacks, and Queues and your implementation abilities. This assignment requires you to implement the Double Ended Queue – Deque data structure. Deque, which is pronounced as “deck”, is a generalization of the queue data structure that supports inserting and removing elements from either the front or the back of the data structure. The assignment will have two phases; (1) implementation of the data structures and (2) application of the data structures.

Part I

In the first part of the assignment, you will implement the deque ADT both using Arrays and Doubly Linked Lists. You will be given a deque interface and two starter files. These files have comments for your convenience. You are also given another interface for a simple container. This interface specifies three operations; (1) push, (2) pop and (3) peek. The details are in the comments but you can figure out that these methods resemble stack and queue operations. You are going to implement a stack and a queue that implement this interface. However, you will be required to implement these by using a deque; by wrapping the dequeue operations to achieve the desired input-output behavior. The type of deque will be given as a generic. See the relevant files and the main file for how they are used.

The code has comments about the assignment. Majority of what you need to do is actually in these comments so make sure you read them carefully. The descriptions for the provided files are below. Bold ones are the ones you need to modify and they are placed under the code folder, with the rest under given.

<ul>

 <li>iDeque.java: This is the interface that shows you the operations of the Deque ADT. You do not need to modify this file. The ArrayDeque and LLDeque classes implements this interface. Make sure you pay attention to the comments.</li>

 <li>ArrayDeque.java: You need to code the ArrayDeque class that implements the iDeque interface using a Dynamic Array in this file. Follow the instructions given in the code.</li>

 <li>LLDeque.java: You need to code the LLDeque class that implements the iDeque interface using a Doubly Linked Lists in this file. Follow the instructions given in the code.</li>

 <li>iSimpleContainer.java: This interface has three simple methods of a container that allow manip- ulation from a “single point”. You do not need to modify this file but make sure to read its comments.</li>

</ul>

1

<table>

 <tbody>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td></td>

  </tr>

 </tbody>

</table>

<ul>

 <li>Stack.java: You need to code the Stack class that implements the iSimpleContainer interface using a generic deque in this file. Look at the code to see how this is setup. This must have the last-in first-out behavior.</li>

 <li>Queue.java: You need to code the Queue class that implements the iSimpleContainer interface using a generic deque in this file. Look at the code to see how this is setup. This must have the first-in first-out behavior.</li>

 <li>Main.java: Gives printouts for you to check your implementation. Will change after the release of the second phase and the release of the autograder. You can compare the outputs with the example outputs.txt file.</li>

 <li>Util.java: This file includes utility functions. Do not worry about it, you will not need to use anything from this file in this assignment.Part IIIn the second part of the assignment, you are going implement an algorithm, given below, that finds the exit in a maze given a start coordinate. This algorithm uses containers which changes its behavior. If a stack is used the algorithm acts as a depth-first search and if a queue is used, it acts as a breadth-first search. The idea is to start from the start state and systematically search the maze. The containers hold the next states to be checked. The mazes are given as txt files where characters define the whether a cell is a wall, empty, a start state or an end state. The algorithm is as below:</li>

</ul>

Algorithm 1: solveMaze(maze,sc,deque)

Input: Maze (maze), initially empty container (sc), initially empty visited node storage (deque)

Output: Wheter a path to an exit cell is found, the filled visited node storage sc.push(maze startState)while sc is not empty do

currentState = sc.pop()if currentState is an exit state then

return trueelse if currentState is not visited then

mark currentState as visiteddeque.addBehind(currentState) foreach empty neighbor of currentState do

sc.push(neighbor) end

end

return false

For this part, you need to edit the following file:

• Maze.java: This file holds the maze information. Go over its comments carefully and understand what it does. You are going to fill in the solveMaze method. We defined additional methods to be helpful but they are not going to be checked.

<ul>

 <li> </li>

</ul>