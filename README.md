# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$


## Answer
1. We can start this by using $T\left(\frac{n}{13}\right) + 5$ to build iterations of the recurrence relation

   Once we have a few iterations we can look for a pattern to use in order solve for the base case

      - $T\left(\frac{n}{13^{i}}\right) + 5i$
      - $i = \log_{13}(n)$
   Using this we can see that the asymtotic time complexity is $T(n) \in \Theta(\log(n))$

2. For this question we basically follow the same steps as question

   Such as using the geometric series to find the dominant term in the summation
   
      - $T(n) = 13T(\frac{n}{13}) + 5$
      - $T(n) = 13^{i}(\frac{n}{13}) + 5\left(\frac{13^{k} - 1}{13 - 1}\right)$
      - $i = log_{13}(n)$

   Time compexity: $T(n) \in \Theta(n)$

3. We can use similar steps get get $T(n) \in \Theta(n\log(n))$

“I certify that I have listed all sources used to complete this exercise, including the use
of any Large Language Models. All of the work is my own, except where stated
otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is
suspected, charges may be filed against me without prior notice.”
