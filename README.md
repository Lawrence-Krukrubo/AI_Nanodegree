<h1 align='center'>AI_Nanodegree: Building a Sudoku Solver in Python</h1>
<P align="center"><b>This is the first project in the Artificial Intelligence Nanodegree program at Udacity.</b></P>

<p align="center">
  <img width="500" height="450" src="https://github.com/Lawrence-Krukrubo/AI_Nanodegree_Project_Sudoku/blob/master/image/sudoku.png?raw=true" alt="Sudoku">
</p>
<p>
Sudoku is one of the most popular puzzle games of all time. The goal of Sudoku is to fill a 9×9 grid with numbers so that each row, column and 3×3 section contain all of the digits between 1 and 9. As a logic puzzle, Sudoku is also an excellent brain game. If you play Sudoku daily, you will soon start to see improvements in your concentration and overall brain power. <a href="https://sudoku.com/">Sudoku.com</a>.
</p>
<p>In this project I will build a sudoku solver by first defining a few methods and then combining these methods to solve any Sudoku puzzle</p>

<h2>Goals of this project</h2>
The main goal of this project is to build an intelligent agent that will solve every sudoku while applying two powerful techniques that are used throughout the field of AI:
<h4>1. Constraint Propagation</h4>
<h4>2. Search</h4>
<h4>Constraint Propagation:</h4>
<p>
When trying to solve a problem, it's possible that there are some local constraints to each square. These constraints help us narrow the possibilities for the answer, which can be very helpful. It's important to know how to extract the maximum information out of these constraints in order to get closer to the solution. Additionally, one can repeatedly apply simple constraints to iteratively narrow the search space of possible solutions. Constraint propagation can be used to solve a variety of problems such as calendar scheduling, and cryptographic puzzles.
</p>
<h4>Search:</h4>
<p>
In the process of problem solving, I may get to the point where two or more possibilities are available. What do I do? What if I branch out and consider both of them? Maybe one of them will lead to a position in which three or more possibilities are available. Then, I can branch out again. At the end, I can create a whole tree of possibilities and find ways to traverse the tree until I find our solution. This is an example of how search can be used.<br>
  <b>What is the search algorithm?</b> Simple: first make sure we haven't already found a solution or a contradiction, and if not, choose one unfilled square and consider all its possible values. One at a time, try assigning the square each value, and searching from the resulting position. In other words, we search for a value d such that we can successfully search for a solution from the result of assigning square s to d. If the search leads to an failed position, go back and consider another value of d. This is a recursive search, and we call it a <a href='https://en.wikipedia.org/wiki/Depth-first_search'>depth-first-search</a> because we (recursively) consider all possibilities under values[s] = d before we consider a different value for s.
</p>

<h4>Constraint Satisfaction Problems</h4>
<p>
Constraint satisfaction is a general problem solving technique for solving a class of combinatorial optimization problems by imposing limits on the values in the solution. The goal of this exercise is to practice formulating some classical example problems as constraint satisfaction problems (CSPs), and then to explore using a powerful open source constraint satisfaction tool called Z3 from Microsoft Research to solve them. Practicing with these simple problems will help you to recognize real-world problems that can be posed as CSPs; some solvers even have specialized utilities for specific types of problem (vehicle routing, planning, scheduling, etc.).
</p>
<p>
There are many different kinds of CSP solvers available for CSPs. Z3 is a "Satisfiability Modulo Theories" (SMT) solver, which means that unlike the backtracking and variable assignment heuristics discussed in lecture, Z3 first converts CSPs to satisfiability problems then uses a boolean satisfiability (SAT) solver to determine feasibility. Z3 includes a number of efficient solver algorithms primarily developed to perform formal program verification, but it can also be used on general CSPs. Google's OR tools includes a CSP solver using backtracking with specialized subroutines for some common CP domains.
</p>
<p>Other resources for Constraint Satisfaction Problems solving include:-</p>

* <b>Software Packages:</b>
<ul>
  <li><a href="https://github.com/Z3Prover/z3/wiki#background">Microsoft Research Z3</a></li>
  <li><a href="https://developers.google.com/optimization/cp/cp_solver">Google OR Tools</a></li>
</ul>
<br>

* <b>References:</b>
<ul>
  <li><a href="https://yurichev.com/writings/SAT_SMT_by_example.pdf">SAT/SMT by Example</a></li>
  <li><a href="https://hal.archives-ouvertes.fr/hal-01230685">Tractability in Constraint Satisfaction Problems: A Survey</a></li>
  <li><a href="https://www.cs.cornell.edu/gomes/papers/satsolvers-kr-handbook.pdf">Satisfiability Solvers</a></li>
  <li><a href="http://www.optimization-online.org/DB_FILE/2012/02/3378.pdf">Non-Convex Mixed-Integer Nonlinear Programming: A Survey</a></li>
  <li><a href="https://www.andrew.cmu.edu/user/vanhoeve/papers/alldiff.pdf">The Alldifferent Constraint: A Survey</a></li>
</ul>




