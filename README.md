# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$


## Answer
1.  - We can start this by using $T\left(\frac{n}{13}\right) + 5$ to build iterations of the recurrence relation
    - Once we have a few iterations we can look for a pattern to use in order solve for the base case

      - $T\left(\frac{n}{13^{i}}\right) + 5i$
      - $i = \log_{13}(n)$

    - Using this we can see that the asymtotic time complexity is $T(n) \in \Theta(\log(n))$
  
2. - 
