Each nonvertical [[Line]] has a *slope*, which we can calculate from [[Increments]] in coordinates.

Let $L$ be a nonvertical line in the plane and $P_1(x_1,y_1)$ and $P_2(x_2,y_2)$ two points on $L$.
![[calcbcfig1-1.png]]
```tikz
\usepackage{tikz}
\begin{document}
\begin{tikzpicture}

@Axes
\draw[thick,->] (-0.5, 0) -- (4.5,0) node[anchor=west] {$x$};
\draw[thick,->] (0,-0.5) -- (0,4.5) node[anchor=south] {$y$};
\path (0, 0) node[anchor=north east] {$O$};

\draw[cyan, line width=2pt, line cap=round, dash pattern = on 8pt off 4pt] (0.75, -5/16) -- (5, 5) node[anchor=south east] {$L$};
\draw[cyan, line width=2pt, line cap=round] (2, 5/4) -- (4, 15/4);
\fill [fill=cyan, opacity=0.2] (2, 1.25) node[circle, fill=cyan, opacity = 1, inner sep = 2pt, minimum size=1pt, label=left:{$P_1(x_1,y_1)$}] {}
-- (4, 3.75) node[circle, fill=cyan, opacity = 1, inner sep = 2pt, minimum size=1pt, label=left:{$P_2(x_2,y_2)$}] {}
-- (4, 1.25) node[circle, fill=cyan, opacity = 1, inner sep = 2pt, minimum size=1pt, label=right:{$Q(x_2,y_1)$}] {};

\end{tikzpicture}
\end{document}
```

We call $\Delta y=y_2-y_1$ the **rise** from $P_1$ to $P_2$ and $\Delta x=x_2-x_1$ the **run** from $P_1$ to $P_2$. Since $L$ is not vertical, $\Delta x\ne0$ and we define the slope of $L$ to be the amount of rise per unit of run. It is conventional to denote the slope by the letter $m$.

A [[Line]] that goes uphill as $x$ increases has a positive slope. A line that goes downhill as $x$ increases has a negative slope. A horizontal line has slope zero since all of its points have the same y-coordinate, making $\Delta y=0$. For vertical lines, $\Delta x=0$ and the ratio $\Delta y/\Delta x$ is undefined. We express this by saying that vertical lines *have no slope*.
>[!definition]
Let $P_!(x_1, y_1)$ and $P_2(x_2,y_2)$ be points on a nonvertical line, $L$. The **slope** of $L$ is
$$m=\frac{rise}{run}=\frac{\Delta y}{\Delta x}=\frac{y_2-y_1}{x_2-x_1}$$

