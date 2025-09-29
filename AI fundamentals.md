#  				Fundamentals of AI

## SESSION 1::



in case of supervised learning. the labeled data is used for either prediction or classification

in unsupervised learning, unlabeled data generally for dimensionality reduction and clustering is used



Deep learning:

It is the subset of ML that is generally used for massive datasets which are broadly unstructured and require better computational algorithms to process the data mainly for classification task to improve the training accuracy using the neural networks.



NLP:

Covers the domain area with machine translations (linguistic, speech recognition, chatbots and sentiment analysis)



Generative AI:

which are trained prominently on unlabeled data with massive fine tuning to interpret and generate a new context based on image, audio, text



Responsible AI:

This implements the basic ethical principles like accountability and a better transparent and interpretable module that has minimal amount of biasness



Explainable AI:

This takes into consideration the AI ethics where a clear interpretation why that particular outcome has a specific analysis



Agentic AI:

AI driven applications on the basis of several agents trying to provide an optimal autonomous decision making

## 

## SESSION 2::



Agent are the smart devices which are able to percept the environment with the help of input sensors and can act accordingly using the different set of actions. The environment of the agent plays a significant role while evaluating PEAS(Performance measure, Environment, Actuators, Sensors).



Percept sequence contains the history of all the possible states that the agent can sense

Agent function is used to map the specific percept with the action these are derive generally with the help of rule based scenarios.



### Types of Environment:

1\. Fully observable and partial environment : The agent sensors have complete access to the entire state of the environment



2\. Deterministic -- Next state is completely determined by the current state

   Stochastic -- If the next state appears to be random for the partially observable environment



3\. Episodic -- The agent function is based on sperate episodes being mapped to specific set of actions that will not impact the future states (Eg: classification task)

   Sequential -- Current decision is impacted with the series of action that will control the future states (Eg: Chess playing robot)



4\. Static -- There is not bound to the passage of time(Eg: chess playing without timer)

   Semi-dynamic -- (Where the environment is controlled with the passage of time(Eg: Chess with timer)

   Dynamic (The complete environment continuously changes with the passage of time (Eg: Self driving car)



5\. Discrete -- Finite number of case

   Continuous -- The series of actions have uncountable states



6\. Single agent -- Only 1 agent is involved to maximize the performance measure

   Multi agent -- Multiple agents are involved to maximize the performance measure



7\. Unknown ,known



### Types of agents:

1. Single reflex agent: They are rule based, operate on only eh current percept and do not have the memory. Eg: Automatic doors
2. Model base reflex agents: They operate on the observed set of accept sequence, knowledge base can be upgraded.
3. Role based agents:  They have a predefined goal where possible states and specific actions are used to map the goal.
4. Utility based agents: The Performance measure is associated with a utility number to reach that specific goal
5. Learning agents: These generally operate through the unobservable and adapt to the changing environment, learn from the percept sequence and using the feedbacks they improve their performance over the span of time



### Problem saving agents and goal formulation

Formulate, search an execute are the main targets while designing the problem solving agents. The four components are:

1. Initial state
2. Sequence of states with possible actions
3. Goal state
4. Path cost



A.  8 Puzzle Problem (or n puzzle problem)





B.  n queens problem:  (1.8 \* 10^14 possible sequences)

State --> any arrangement of 0-8 queens on the board

Initial --> no queens on the board

Action --> add a queen to a empty square

Goal --> 8 queens are on the board, none attached



C.  Block world problem in AI:

Initial --> configuration of the blocks

State --> Arrangement of the blocks using actions

Action --> Stacking , Unstacking, Placing on the ground

Goal --> Specific configuration of blocks should be obtained on table top



D.  Crypt Arithmetic:

The given words in the form of alphabets are mapped to the arithmetic numbers which follow the correct arithmetic operator to define the logical relationship



E. Water Jug problem in AI:

Given 2 jugs 4L and 3L with initial state as (0,0) for empty jugs. The goal state is to fill 4L of jug with exactly 2L of water. The constraint that the jugs do not have any marking.

Action --> Drain the water from one jug to another, Drain water to ground, Unlimited supply of water



F. Missionaries and Cannibals problem in AI

State -->

Initial --> All the missionaries, cannibals and boat are on the left side (3,3,1)

Action --> Boat positioning,

Goal --> (0,0,0) all are transported safely, constraint being that missionaries are not outnumbered by the cannibals.



G. Map coloring problem in AI:

Coloring the map with no adjacent boundaries having the same color with constraint satisfaction problem



H. Travelling Salesman problem:

State --> A salesman need to traverse from the start position of his office and travel the nearby cities and finally return back to his office using the optimal path

Initial --> Traversing the entire map starting from the arid

Action -->

Goal --> Reaching to a goal using the optimal distance



State space diagram:

These are generally implemented by

Either trees(acyclic) or graphs(cyclic) can be used to represent the state diagram for a problem. Graphs are preferable for network topology or maps	1





## SESSION 3 + 4 ::

#### 

#### Uniformed search

* This type of search strategy do not require any heuristic information
* Only the goal state is given without any prior information of the path cost to reach the goal node



1. ###### BFS

* Level wise expansion, queue data structures is used to store the data elements
* Solution is always guaranteed while expanding the shallowest node
* Elements will be stored in the specific data structures and would be visited or expanded according to the property of data structure till the goal node is reached
* Time complexity is O(b^d+1]) where b is the branching factor and d is depth of the tree
* Space complexity is also same



###### 2\. DFS

* Fails in infinite depth spaces, spaces with loops
* Solution is not guaranteed

###### 

###### 3\. Depth limited search

* In this type of DFS, a bound is given while expanding the left side of the tree, once the limit is reached it will backtrack to the predecessors until the goal is found

###### 

###### 4\. Iterative deepening search

* The depth limit is implemented until the goal state is achieved. The backtracking will be done from the depth limit in every iteration
* The time complexity is O(b^d) and space complexity is O(bd)
* It is optimal if step cost = 1



###### 5\. Uniform cost search

* Expand the least cost node first
* Priority queue is used
* Equivalent to DFS if path cost is 1
* The path cost is evaluated from the root towards a sepecific node, it is not equivalent to the heuristic information

###### 

###### 6\. Bisirectional search

* The traversal is done from both ends



ASsignment 3,

Q1 ----> TREE

Q2 ----> No table but draw block diagram

Q3 ----> Tree in block shapee

Q4 ---->







## SESSION 5 ::



##### Informed search

The evaluation function can be assessed for every node. Main types of informed search elbow:



###### 1\. Best first search (greedy search)

f(n)= h(n), where f(n) is the evaluation function, h(n) is the heuristic function/value





###### 2\. A \* algorithm

f(n)= h(n)+g(n),and g(n) is path cost/actual cost

The estimation of the heuristic value should never overestimate the actual cost i.e it should be admissible

The informed search category or the classical search requires a larger amount of space complexity (more memory cells are required to store the state) therefore local search algortihms



In case of tic tac toe board h(n) = p(x)-p(0) where the goal state is to win the game



Hill climbing:

Always select the next move with respect to maximum value of objective function

The random restart hill climbing can be used to save form the infinite state or local maxima

For the block world problem while using hill climbing, using the local objective function there are chances of getting trapped so a global heuristic function can be used to climb the hill with the steepest ascent



## SESSION 6 ::

Simulated annealing algo in AI is a somewhat a variant of stochastic hill climbing but along the downward movement and evaluating the objective function (bound by temperature criteria)

The probability decreases as the temperature goes down, therefore worst solutions are likely to be adaptable for higher values of temperatures and the probability becomes unlikely as temp. decreases.



###### Genetic algorithms:



Probability of a state

The parent states will result into the new child states



These algo are the game playing agents that work in fully observable environment with 2 players having alternate moves and a utility number associate with the last outcomes



Min-max algo:

It is based on DFS with backtracking , one player as max and other as min

While revolving the utility numbers that are allocated from the terminal nodes must be having the criteria that max will select the max value and min will select the min value

Limitations:

The memory requirement rose exponentially as there some nodes which are unused and they will never be visited for the optimal solutions

alpha - beta pruning is better option

alpha is used with the maximizer and its initial value is -infinity

beta is used with the minimizer and its initial value is +infinity

The algo will prune those nodes on the criteria that alpha >= beta

Node values will be passed to the upper nodes instead of values of alpha and beta. We pass the alpha beta values to the child nodes



###### **Automated pipeline using apache airflow**



Account on docker hub

Installation of docker desktop with (wsl --install) enabled and (wsl --update) if docker desktop not installing

Account on GitHub and installation of git bash

Install JDK-17 and execute the Jenkins war file, in case installation fails disable firewalls, local host 8080 will be used to instantiate Jenkins

Command to start (java -jar jenkins.war)

Create account on AWS



## SESSION 7 ::

#### Constraint satisfaction problem

In the search space the problem is resolved by considering all the conflicts and using finite set of variables which can take different domain values. All the possibilities are explored with respect to the different constraints in the problem.

After CSP, a specific type of search strategy is used via forward tracking or backtracking to reach the goal state in the tree diagram

Eg: Drift Arithmetic



 	S E N D

      + M O R E

   =  M O N E Y



Eg: Map coloring problem

Given minimal number of colors, You need to color the map with different colors on the adjacent neighbours



#### Knowledge representation and Analysis

Components of knowledge based agent:

1. Knowledge base (KB)
2. Inference Engine
3. Learning/Updating KB



Different ways to represent the knowledge base:

First order logic are the efficient base to represent the KB

which are connecting the complex sentences with the help of different logical connectors

