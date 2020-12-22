# EAI320_Practical2
## Scenario
Genetic Algorithm(GA) are numerical techniques that attempt to imitate evolution and
natural selection. The motivation for this approach is the remarkable way in which natural
systems adapt to their environments [3]. GAs have been applied to a very wide range of
problems including optimisation [4], [5], computer programming [6], circuit design [6], the
traveling salesman problem [4], and training of neural networks [7].

This assignment will require students to find a pseudo-optimal strategy for a rock-paperscissors (RPS) agent by using a GA. 
The same RPS framework that was used for the previous assignment will be used again [8].

In accordance with the naming conventions used in the prescribed textbook, the string
representing an individual will comprise 81 genes. Each gene will correspond to the object
that an individual will play given a history of 2 moves (i.e. 4 objects). Fig. 1 provides a
visual representation of an individual string. The histories, corresponding to the 81 different
objects, should be in the same order as they would be visited by breadth first search (BFS)
in a search tree of depth 4. 

## Instuctions
### A. Task
Each student has to implement a GA that can be used to find a pseudo-optimal strategy for
a RPS agent, given some historical game data. More information can be found in Section 4.1,
and more specifically Section 4.1.4, of the prescribed textbook [1].

The student is expected to experiment with different population sizes and mutation rates,
and all students should ensure that they answer the questions that are listed below as part of
their discussion.
- How does the size of the population affect the performance of the GA?
- How is the selection step in the GA performed?
- How is the crossover step in the GA performed?
- How is the mutation step in the GA performed?
- How many iterations of the algorithm is required to find a good solution?
- What is the pseudo-optimal strategy that was found by the GA?

The technical report should also contain a graph where the fitness of the best individual
from each generation is plotted against the number of generations. The average fitness of the
population for each generation should also be overlayed onto this plot.

The historical game data is provided in comma-separated values (CSV) files, data1.csv
and data2.csv. If we let agent 1 be the agent that the GA is trying to optimise and let agent
2 be the opposing agent, then we can represent the objects that agent 1 and agent 2 will play
in the current round by xt and yt respectively. The history contained in the first column of
data1.csv and data2.csv is then in the form [xt_2, yt_2, xt_1, yt_1], and the second column
represents the next object that the opponent played given the two game history. 

The optimal move for a given history is thus the move that will beat the opponent’s move in the second
column. The student may use this information in any way to design an evaluation function
that can be used to identify strong and weak individuals during training.
Each student will have to submit three files for this assignment.

- A short, yet thorough, technical report with the Python code that was used to implement
the GA added to the end of the report in the Appendix.
- A CSV file containing the optimal strategy found by the GA when using data1.csv.
This file should contain 81 objects (R, P, or S), each separated only be a comma.
- A CSV file containing the optimal strategy found by the GA when using data2.csv.
This file should contain 81 objects (R, P, or S), each separated only by a comma.

In summary, a program must be written to implement a GA that can be trained on a dataset
(data1.csv or data2.csv) to generate a sequence of 81 moves. This sequence must then be
written to a file using the same format as the file rock_sequence.txt shown in Listing 2
in section C. This file is read in by agent.py and used to determine the agent’s next move
against an opponent. The code for agent.py is shown in Listing 1 in section B.

## References
[1] S. J. Russell and P. Norvig, Artificial intelligence: A modern approach, 3rd ed. Prentice
Hall, 2010.

[2] L. Strydom, EAI 320 – Practical 2 Guide, University of Pretoria, 13 Feb. 2019.

[3] W. P. du Plessis, “A genetic algorithm for impedance matching network design,” Master’s
thesis, University of Pretoria, 2003.

[4] D. E. Goldberg, Genetic algorithms in search, optimization, and machine learning. New
York, USA: Addison-Wesley, 1989.

[5] Z. Michalewicz, Genetic algorithms + data structures = evolution programs. Berlin,
Germany: Springer-Verlag, 1992.

[6] J. R. Koza, F. H. Bennet, D. Andre, and M. A. Keane, Genetic programming III. San
Francisco, USA: Morgan Kaufmann, 1999.

[7] X. Yao, “A review of evolutionary artificial neural networks,” Int. Journal Intelligent
Systems, vol. 8, no. 2, pp. 539–567, Jun. 1993.

[8] B. Knoll. (2011, 6 Feb.) Rock paper scissors programming competition. [Online].
Available: [rpsContest](http://www.rpscontest.com/)
