- ![INF2D_CW1.pdf](../assets/INF2D_CW1_1677681348473_0.pdf)
- ((63ff6363-4539-4ff4-ad7a-5862ab8eb0b1))
-
- # Part A
- ### (a) (5 points) 
  Write down the variables and the domain (before applying any of the constraints) to translate this into a CSP problem.
	-
	- \begin{algorithm}
	  \caption{Finds the most efficient path through the goals}
	  \begin{algorithmic}
	  \Function{Greedy}{$start, goals$}
	  \State $order \gets [start]$
	  \State $pos \gets start$
	  \While{$goals \neq \emptyset$}
	      \State $minDistance \gets \infty$
	      \State $minGoal \gets null$
	      \For{$goal \;in\; goals$}
	          \State $d \gets DISTANCE(pos,goal)$
	          \If{$d < minDistance$}
	              \State $minDistance \gets d$
	              \State $minGoal \gets goal$
	          \EndIf
	      \EndFor
	      \State $pos \gets minGoal$
	      \State $order.add(pos)$
	  \EndWhile
	  \State \textbf{return} $T$
	  \EndFunction
	  \end{algorithmic}
	  \end{algorithm}