Download Link: https://assignmentchef.com/product/solved-eecs-281-lab-9-assignment
<br>






<strong>Note: ​</strong>This lab assignment contains a multiple choice quiz and a coding portion. Submit your quiz answers to the​  lab​          9​ Canvas​ ​quiz and your code to the autograder.​ ​You​ ​will​ ​have​ ​<strong>three​</strong> ​attempts on the quiz.




<sup> </sup><strong><em>You ​<u>MUST</u> include the following assignment identifier at the top of every file you submit to the autograder as a comment. This includes all source files, header files, and your Makefile (if there is one). If there is no autograder assignment, you may ignore this.</em></strong>

Assignment Identifier: 472D3C8289DE4915774A47683EC45FFBA373B980







<strong> </strong>

<h1>Part A: Graphs and Searching Algorithms (3 points)</h1>

<strong> </strong>




For questions 1-2, use the graph below:

<h2>9.1 – Running Prim’s Algorithm (0.5 points)</h2>

<strong> </strong>

What is the sequence of vertices added to the MST for the graph above when running Prim’s algorithm, if you start with vertex 7?

<ol>

 <li>7, 2, 0, 5, 1, 3, 4, 6 <strong>B. </strong>7, 2, 0, 5, 3, 1, 6, 4 <strong>C. </strong>7, 2, 0, 3, 5, 1, 6, 4 <strong>D. </strong>7, 2, 5, 4, 0, 1, 3, 6</li>

 <li>7, 2, 5, 4, 0, 3, 1, 6</li>

</ol>




<h2>9.2 – Running Kruskal’s Algorithm (0.5 points)</h2>

<strong> </strong>

What is the sequence of edges added to the MST for the graph above when running Kruskal’s algorithm? Use the edges’ weights as their label for this question.

<ol>

 <li>1, 4, 9, 2, 3, 5, 7 <strong>B. </strong>1, 2, 4, 5, 3, 9, 7 <strong>C. </strong>1, 2, 4, 3, 5, 7, 9</li>

 <li>1, 2, 3, 4, 5, 7, 9</li>

 <li>1, 2, 3, 4, 5, 6, 7, 8, 9</li>

</ol>

<h2>9.3 – Finding Your Flight (0.5 points)</h2>

<strong> </strong>

You currently have a graph that represents several airports (vertices) and the flights that connect these airports (edges), weighted by the distance of each flight. You decide to implement this graph using an adjacency list. Let ​<em>V</em> represent the number of vertices in this graph, and let ​<em>E</em> represent the number of edges. If you are given an airport ​<em>X​</em>, what is the worst-case time complexity of determining if ​<em>any​</em> flights depart from airport ​<em>X​</em>?

<ol>

 <li>Θ(1)</li>

 <li>Θ(<em>E​</em>​<em><sub> ​</sub></em>)</li>

 <li>Θ(<em>V​</em>​<em><sub> ​</sub></em>)</li>

 <li>Θ(1 + ​<em>E​</em>/​<em>V​</em><em><sub> ​</sub></em>)</li>

 <li>Θ(<em>V​</em>​<em><sup> ​2</sup></em>)<em><sup>​</sup></em></li>

</ol>




<h2>9.4 – Stacks and Queues (0.75 points)</h2>

<strong> </strong>

Which of the following statements is/are ​<strong>true​</strong>? ​<em>Select all that apply. </em>

<ol>

 <li>a stack is a good data structure to use for a depth-first search (DFS)</li>

 <li>a stack is a good data structure to use for a breadth-first search (BFS)</li>

 <li>a stack is a good data structure for conducting a level-order traversal of a binary tree</li>

 <li>a queue is a good data structure to use for a depth-first search (DFS)</li>

 <li>a queue is a good data structure to use for a breadth-first search (BFS)</li>

 <li>a queue is a good data structure for conducting a level-order traversal of a binary tree</li>

</ol>

<strong> </strong>

<h2>9.5 – Memory Trees (0.75 points)</h2>

<strong> </strong>

Suppose you have a binary tree of height 281, where leaf nodes have height 1, and you want to search for an element ​<em>k​</em>. You know that ​<em>k</em> exists as a distinct element in this tree, and that it is a leaf node. Which of the following statements is/are ​<strong>true​</strong>? Select all that apply.

<ol>

 <li>if you conduct a depth-first search for ​<em>k​</em>, you’ll never have to store more than 281 nodes in memory</li>

 <li>if you conduct a breadth-first search for ​<em>k​</em>, you’ll never have to store more than 281 nodes in memory</li>

 <li>if you are concerned about the memory efficiency of the search, you should use a queue to conduct this search instead of a stack</li>

 <li>the path from the root to the element ​<em>k</em> returned by a breadth-first search will always be shorter than the path returned by a depth-first search</li>

 <li>while a breadth-first search will always find the element ​<em>k​</em>, it is possible that a depth-first search may fail to find ​<em>k​</em> since depth-first searches do not always visit every element</li>

</ol>




<strong> </strong>

<h1>Part B: Coding Assignment (10 points)</h1>

<h2>9.6 – Number of Islands (10 points)</h2>

<strong> </strong>

In this problem, you will be implementing the ​number_of_islands() function, as shown below:​




int​ number_of_islands​(​std​::​vector​&lt;​std​::​vector​&lt;char&gt;​&gt;&amp;​ grid​);




This function takes in a 2-D grid map filled with land (represented using the character ​’o’)​ and water (represented using the character ​’.’)​ and ​<strong>returns the number of islands that exist in the map. ​</strong>An island is formed by connecting adjacent land characters either horizontally or vertically. In other words, if two land characters are adjacent to each other horizontally or vertically, then they are a part of the same island.




<strong>Example: ​</strong>Given the following 2-D map:




o…oo.ooo.ooooo. .ooo.oo..oo..oooo …o.o.ooo…..oo oo.ooo..oooo..o..

o….o….ooooo.o ooo….oooo….oo ….ooooo…ooo.o ooo.oo.oooo.o.ooo .ooo….oo……o

…oooooo…oo.oo




the ​number_of_islands() function should return 7, since there are 7 islands in this map:​




<strong>o</strong>​…​<strong>oo</strong>​.​<strong>ooo</strong>​.​<strong>ooooo</strong>​. .​<strong>ooo</strong>​.​<strong>oo</strong>​..​<strong>oo</strong>​..​<strong>oooo</strong> …​<strong>o</strong>​.​<strong>o</strong>​.​<strong>ooo</strong>​…..​<strong>oo</strong> <strong>oo</strong>​.​<strong>ooo</strong>​..​<strong>oooo</strong>​..​<strong>o</strong>​.. <strong>o</strong>​….​<strong>o</strong>​….​<strong>ooooo</strong>​.​<strong>o </strong><strong>ooo</strong>​….​<strong>oooo</strong>​….​<strong>oo</strong> ….​<strong>ooooo</strong>​…​<strong>ooo</strong>​.​<strong>o</strong> <strong>ooo</strong>​.​<strong>oo</strong>​.​<strong>oooo</strong>​.​<strong>o</strong>​.​<strong>ooo</strong>

.​<strong>ooo</strong>​….​<strong>oo</strong>​……​<strong>o</strong> …​<strong>oooooo</strong>​…​<strong>oo</strong>​.​<strong>oo </strong>

<strong> </strong>

Implement your solution in the ​islands.h starter file provided. You can download the file on either Canvas or ​​  <a href="https://gitlab.umich.edu/eecs281/lab-9">GitLab</a>.​ To submit to the autograder, create a ​.tar.gz file containing just ​​        islands.h by running the following command:​




<strong>   tar -czvf lab9.tar.gz islands.h  </strong><em>(</em>​ <em>you can also run “make fullsubmit” using the Makefile we provide) </em>

<strong> </strong>

If you are working with a partner, ​<strong><em>both partners must submit to the autograder​</em></strong>.<em> ​</em>Only students who submit code to the autograder will receive points. It’s fine if both of you submit the same code for this assignment. If you do end up working with a partner, make sure to put both of your names at the top of the file you are submitting.




<u>Hints ​<em>(try to work the problem on your own before you look at this)</em></u>

The purpose of this exercise is to give you practice with graph searching algorithms (BFS and DFS) before the final exam. There are two primary methods that you can use to solve this problem: either by using a ​<em>breadth-first search</em> (BFS) or a ​<em>depth-first search​</em> (DFS). A summary of the algorithm is as follows:

<ol>

 <li>Initialize a counter to keep track of the number of islands.</li>

 <li>Iterate over every cell of the 2-D vector (a double ​for loop is okay).​</li>

 <li>If the cell you are currently visiting is a land character (​’o’):​</li>

</ol>

○ Increment your counter by one.

○ Mark the cell as visited. (You do <u>​<em>not</em></u><em> ​</em>need to create a separate container to keep track of whether a cell has been visited or not! Hint: you can directly modify the values in the map.)

○ Complete a BFS or DFS of the entire island you are on. To do this, push any adjacent land locations into a queue or stack (make sure that you aren’t accessing out of bounds). In other words, you would push into a queue or stack the coordinates directly to your north, east, south, and west, as long as they are also land locations. Mark any coordinates as visited, if necessary. If you are doing a DFS, you can either explicitly initialize a ​std::stack or use recursion, which utilizes the program stack.​

○ After the BFS or DFS is complete, continue iterating the 2-D vector. Keep on repeating steps 2 and 3 until the entire 2-D vector is processed.




You do not need to solve this problem using both BFS and DFS, but you are encouraged to practice both algorithms for the exam (since you may get a problem that can only be solved using one method and not the other).