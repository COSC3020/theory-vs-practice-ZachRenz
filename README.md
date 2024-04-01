[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  1) The definition of asymptotics tells us that we can find a $f(n)$ that satisfies $T(n)$ ($\leq$ or $\geq$ or both) $cf(n)$. We don't know what $c$ is in any given analysis, and of course $3f(n)$ is different than $10,000f(n)$, and can misrepresent the runtime of $T(n)$ in practice. 

  2) The definition of asymptotics tells us that it works for all $n \geq n_0$. We get to pick the $n_0$ that works here. That means our $n_0$ can be too big than needed, leaving some room for error estimating real practice. 

  3) For $O$ and $\Omega$, these complexities are essentially upper and lower bounds for an algorithm. We could say that for an algorithm there is a $O(n)$ complexity associated to it, but we can say that for many many other algorithms when better, or "tighter", complexities can be made for it. These complexities can be out of the ballpark for estimating real performance. 

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  The complexity for search in a binary tree is $O(log_2(n))$. $log_2(1,000) = 9.966$ and $log_2(10,000) = 13.288$. From here we can use fractions $\frac{5}{9.966} = \frac{n}{13.288} \Rightarrow 9.666n = 66.439 \Rightarrow 6.666...$. So I would guess it takes about 7 seconds to find the same element in a binary tree of 10,000. 

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  1) this algorithm could be run on a different machine than the last test. The first one might have been done on a lab computer during work and then the second on a machine with significantly less computation power, maybe a ti-84 calculator if you were very dedicated. 

  2) These elements may be extremely big too, say we're searching for a movie based on the clip of a scence in it. This would take a lot longer to anaylize than just numbers. Changing the size by adding 9,000 more movies can significanlty increase the runtime.

  3)  The algorithm could also have a memory leak that we don't know about. If left unchecked we can have meaningless memory allocated that could even eat through the ram and start using the hard drive for memory while running the algorithm, taking a huge hit to performance and runtime. This and other issues that an algorithm may have could be a reason. 


