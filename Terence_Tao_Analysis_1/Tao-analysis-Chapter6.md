# Chapter 6  
## 6.1 Convergence and limit laws  
### Definitions  
* 6.1.1 (Distance between two real numbers). Given two real numbers $x$ and $y$, we define their distance $d(x, y)$ to be $d(x, y) := |x − y|$.  
* 6.1.2 ($\epsilon$-close real numbers). Let $\epsilon > 0$ be a real number. We say that two real numbers $x, y$ are $\epsilon$-close iff we have $d(y, x) \le \epsilon$.  
* 6.1.3 (Cauchy sequences of reals). Let $\epsilon > 0$ be a real number. A sequence $(a_n)^\infty_{n = N}$ of real numbers starting at some integer index $N$ is said to be $\epsilon$-steady iff $a_j$ and $a_k$ are $\epsilon$-close for every $j, k \ge N$. A sequence $(a_n)^\infty_{n = m}$ starting at some integer index $m$ is said to be eventually $\epsilon$-steady iff there exists an $N \ge m$ such that $(a_n)^\infty_{n = N}$ is $\epsilon$-steady. We say that $(a_n)^\infty_{n = m}$ is a Cauchy sequence iff it is eventually $\epsilon$-steady for every $\epsilon > 0$.  
* 6.1.5 (Convergence of sequences). Let $\epsilon > 0$ be a real number, and let $L$ be a real number. A sequence $(a_n)^\infty_{n = N}$ of real numbers is said to be $\epsilon$-close to $L$ iff an is $\epsilon$-close to $L$ for every $n \ge N$, i.e., we have $|a_n − L| \le ε$ for every $n \ge N$. We say that a sequence $(a_n)^\infty_{n = m}$ is eventually $\epsilon$-close to $L$ iff there exists an $N \ge m$ such that $(a_n)^\infty_{n = N}$ is $\epsilon$-close to $L$. We say that a sequence $(a_n)^\infty_{n = m}$ converges to $L$ iff it is eventually $\epsilon$-close to $L$ for every real $\epsilon > 0$.  
* 6.1.8 (Limits of sequences). If a sequence $(a_n)^\infty_{n = m}$ converges to some real number $L$, we say that $(a_n)^\infty_{n = m}$ is convergent and that its limit is $L$; we write $L = \lim_{n \rightarrow \infty} a_n$ to denote this fact. If a sequence $(a_n)^\infty_{n = m}$ is not converging to any real number $L$, we say that the sequence $(a_n)^\infty_{n = m}$ is divergent and we leave $\lim_{n \rightarrow \infty} a_n$ undefined.  
* 6.1.16 (Bounded sequences). A sequence $(a_n)^\infty_{n = m}$ of real numbers is bounded by a real number $M$ iff we have $|a_n| \le M$ for all $n \ge m$. We say that $(a_n)^\infty_{n = m}$ is bounded iff it is bounded by $M$ for some real number $M > 0$.  

### Proposition 6.1.4. Let $(a_n)^\infty_{n = m}$ be a sequence of rational numbers starting at some integer index $m$. Then $(a_n)^\infty_{n = m}$ is a Cauchy sequence in the sense of Definition 5.1.8 if and only if it is a Cauchy sequence in the sense of Definition 6.1.3.  

### Proposition 6.1.7 (Uniqueness of limits). Let $(a_n)^\infty_{n = m}$ be a real sequence starting at some integer index $m$, and let $L \ne L^\prime$ be two distinct real numbers. Then it is not possible for $(a_n)^\infty_{n = m}$ to converge to $L$ while also converging to $L^\prime$.  

### Proposition 6.1.11. We have $\lim_{n \rightarrow \infty} 1/n = 0$.  

### Proposition 6.1.12 (Convergent sequences are Cauchy). Suppose that $(a_n)^\infty_{n = m}$ is a convergent sequence of real numbers. Then $(a_n)^\infty_{n = m}$ is also a Cauchy sequence.  
* Suppose $a_n$ is a convergent sequence, $L = \lim_{n \rightarrow \infty} a_n$. Let $\epsilon > 0 \Rightarrow \epsilon / 2 > 0 \Rightarrow \ \exist j \ st. \ n \ge j, |a_n - L| < \epsilon / 2 \Rightarrow \forall n, m \ge j, |a_n - a_m| = |a_n - L + L - a_m| \le |a_n - L| + |a_m - L| \le \epsilon / 2 + \epsilon / 2 \le \epsilon$. Then $a_n$ is a Cauchy seqencue.  

### Proposition 6.1.15 (Formal limits are genuine limits). Suppose that $(a_n)^\infty_{n = 1}$ is a Cauchy sequence of rational numbers. Then $(a_n)^\infty_{n = 1}$ converges to $LIM_{n \rightarrow \infty} a_n$.  
* See Exercise 6.1.6    

### Corollary 6.1.17. Every convergent sequence of real numbers is bounded.  

### Theorem 6.1.19 (Limit Laws). Let $(a_n)^\infty_{n = m}$ and $(b_n)^\infty_{n = m}$ be convergent sequences of real numbers, and let $x, y$ be the real numbers $x := \lim_{n \rightarrow \infty} a_n$ and $y := \lim_{n \rightarrow \infty} b_n$.  
(a) The sequence $(a_n + b_n)^\infty_{n = m}$ converges to $x + y$; in other words, $\lim_{n \rightarrow \infty} (a_n + b_n) = \lim_{n \rightarrow \infty} a_n + \lim_{n \rightarrow \infty} b_n$.  

(b) The sequence $(a_nb_n)^\infty_{n = m}$ converges to $xy$; in other words, $\lim_{n \rightarrow \infty} (a_n * b_n) = \lim_{n \rightarrow \infty} a_n * \lim_{n \rightarrow \infty} b_n$.  

(c) For any real number $c$, the sequence $(ca_n)^\infty_{n = m}$ converges to $cx$; in other words, $\lim_{n \rightarrow \infty} (ca_n) = c\lim_{n \rightarrow \infty} a_n$.  

(d) The sequence $(a_n - b_n)^\infty_{n = m}$ converges to $x − y$; in other words, $\lim_{n \rightarrow \infty} (a_n - b_n) = \lim_{n \rightarrow \infty} a_n - \lim_{n \rightarrow \infty} b_n$.  

(e) Suppose that $y \ne 0$ and that $b_n \ne 0$ for all $n \ge m$. Then the sequence $(b_n^{-1})^\infty_{n = m}$ converges to $y^{−1}$; in other words, $\lim_{n \rightarrow \infty} b_n^{-1} = (\lim_{n \rightarrow \infty} b_n)^{-1}$.  

(f) Suppose that $y \ne 0$ and that $b_n \ne 0$ for all $n \ge m$. Then the sequence $(a_n/b_n)^\infty_{n = m}$ converges to $x/y$; in other words, $\lim_{n \rightarrow \infty} (a_n / b_n) = \lim_{n \rightarrow \infty} a_n / \lim_{n \rightarrow \infty} b_n$.  

(g) The sequence $(max(a_n, b_n))^\infty_{n = m}$ converges to $max(x, y)$; in other words, $\lim_{n \rightarrow \infty} max(a_n + b_n) = max(\lim_{n \rightarrow \infty} a_n, \lim_{n \rightarrow \infty} b_n)$.  

(h) The sequence $(min(a_n, b_n))^\infty_{n = m}$ converges to $min(x, y)$; in other words, $\lim_{n \rightarrow \infty} min(a_n + b_n) = min(\lim_{n \rightarrow \infty} a_n, \lim_{n \rightarrow \infty} b_n)$.  

### Exercises  
Exercise 6.1.1. Let $(a_n)^\infty_{n = 0}$ be a sequence of real numbers, such that $a_{n+1} > a_n$ for each natural number $n$. Prove that whenever $n$ and $m$ are natural numbers such that $m > n$, then we have $a_m > a_n$. (We refer to these sequences as increasing sequences.)  
Exercise 6.1.2. Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers, and let $L$ be a real number. Show that $(a_n)^\infty_{n = m}$ converges to $L$ if and only if, given any real $\epsilon > 0$, one can find an $N \ge m$ such that $|a_n − L| \le \epsilon$ for all $n \ge N$.  
Exercise 6.1.3. Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers, let $c$ be a real number, and let $m^\prime \ge m$ be an integer. Show that $(a_n)^\infty_{n = m}$ converges to $c$ if and only if $(a_n)^\infty_{n = m^\prime}$ converges to $c$.  
Exercise 6.1.4. Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers, let $c$ be a real number, and let $k \ge 0$ be a non-negative integer. Show that $(a_n)^\infty_{n = m}$ converges to $c$ if and only if $(a_{n + k})^\infty_{n = m}$ converges to $c$.  
Exercise 6.1.5. Prove Proposition 6.1.12. (Hint: use the triangle inequality, or Proposition 4.3.7.)  
Exercise 6.1.6. Prove Proposition 6.1.15, using the following outline. Let $(a_n)^\infty_{n = m}$ be a Cauchy sequence of rationals, and write $L := LIM_{n \rightarrow \infty} a_n$. We have to show that $(a_n)^\infty_{n = m}$ converges to $L$. Let $\epsilon > 0$. Assume for sake of contradiction that sequence an is not eventually $\epsilon$-close to $L$. Use this, and the fact that $(a_n)^\infty_{n = m}$ is Cauchy, to show that there is an $N \ge m$ such that either $a_n > L + \epsilon/2$ for all $n \ge N$, or $a_n < L − \epsilon/2$ for all $n \ge N$. Then use Exercise 5.4.8.  
* Suppose $a_n$ is not converge to $L$, then $\exists \  \epsilon > 0 \ st. \ a_n$ is not eventually $\epsilon$-close to $L$. And $0 < \epsilon / 2 < \epsilon \Rightarrow |a_n - a_m| < \epsilon / 2$ for some $j \in N$ and $n, m \ge j$. Since $a_n$ is not eventually $\epsilon$-close to $L \Rightarrow \exist \ n^\prime, |a_{n^\prime} - L| > \epsilon$ and $|a_n - a_{n^\prime}| < \epsilon / 2 \Rightarrow a_n > L + \epsilon/2$ for all $n \ge j$, or $a_n < L − \epsilon/2$ for all $n \ge j$. Thus by Exercise 5.4.8 we could get $LIM_{n \rightarrow \infty} a_n < L$ or $LIM_{n \rightarrow \infty} a_n > L$ which all lead  contradiction with $LIM_{n \rightarrow \infty} a_n = L$.  

Exercise 6.1.7. Show that Definition 6.1.16 is consistent with Definition 5.1.12 (i.e., prove an analogue of Proposition 6.1.4 for bounded sequences instead of Cauchy sequences).  
* Suppose $m \in R$ and $|a_n| \le m$ by Definition 6.1.16, it's easy to get another $q \in Q, q \ge m$, then $|a_n| \le m \le q$ which also is satisfy the Definition 5.1.12. The rest is skip.  

Exercise 6.1.8. Prove Theorem 6.1.19. (Hint: you can use some parts of the theorem to prove others, e.g., (b) can be used to prove (c); (a),(c) can be used to prove (d); and (b), (e) can be used to prove (f). The proofs are similar to those of Lemma 5.3.6, Proposition 5.3.10, and Lemma 5.3.15. For (e), you may need to first prove the auxiliary result that any sequence whose elements are non-zero, and which converges to a non-zero limit, is bounded away from zero.)  
Exercise 6.1.9. Explain why Theorem 6.1.19(f) fails when the limit of the denominator is 0. (To repair that problem requires L’Hopital’s rule, see Section 10.5.)  
Exercise 6.1.10. Show that the concept of equivalent Cauchy sequence, as defined in Definition 5.2.6, does not change if $\epsilon$ is required to be positive real instead of positive rational. More precisely, if $(a_n)^\infty_{n = 0}$ and $(b_n)^\infty_{n = 0}$ are sequences of reals, show that $(a_n)^\infty_{n = 0}$ and $(b_n)^\infty_{n = 0}$ are eventually $\epsilon$-close for every rational $\epsilon > 0$ if and only if they are eventually $\epsilon$-close for every real $\epsilon > 0$. (Hint: modify the proof of Proposition 6.1.4.)  

## 6.2 The Extended real number system  
### Definitions  
* 6.2.1 (Extended real number system). The extended real number system $R^∗$ is the real line $R$ with two additional elements attached, called $+\infty$ and $-\infty$. These elements are distinct from each other and also distinct from every real number. An extended real number $x$ is called finite iff it is a real number, and infinite iff it is equal to $+\infty$ or $-\infty$. (This definition is not directly related to the notion of finite and infinite sets in Section 3.6, though it is of course similar in spirit.)  
* 6.2.2 (Negation of extended reals) . The operation of negation $x \mapsto -x$ on $R$, we now extend to $R^∗$ by defining $−(+\infty) := −\infty$ and $−(−\infty) := +\infty$.  
* 6.2.3 (Ordering of extended reals). Let $x$ and $y$ be extended real numbers. We say that $x \le y$, i.e., $x$ is less than or equal to $y$, iff one of the following three statements is true: (a) $x$ and $y$ are real numbers, and $x \le y$ as real numbers. (b) $y = + \infty$. (c) $x = −\infty$. We say that $x < y$ if we have $x \le y$ and $x \ne y$. We sometimes write $x < y$ as $y > x$, and $x \le y$ as $y \ge x$.  
* (Supremum of sets of extended reals). Let $E$ be a subset of $R^∗$. Then we define the supremum $sup(E)$ or least upper bound of $E$ by the following rule. (a) If $E$ is contained in $R$ (i.e., $+\infty$ and $−\infty$ are not elements of $E$), then we let $sup(E)$ be as defined in Definition 5.5.10. (b) If $E$ contains $+\infty$, then we set $sup(E) := + \infty$. (c) If $E$ does not contain $+\infty$ but does contain $−\infty$, then we set $sup(E) := sup(E / \lbrace−\infty\rbrace)$ (which is a subset of $R$ and thus falls under case (a)).  

### Proposition 6.2.5. Let $x, y, z$ be extended real numbers. Then the following statements are true.  
(a) (Reflexivity) We have $x \le x$.  
(b) (Trichotomy) Exactly one of the statements $x < y , x = y$, or $x > y$ is true.  
(c) (Transitivity) If $x \le y$ and $y \le z$, then $x \le z$.  
(d) (Negation reverses order) If $x \le y$, then $−y \le − x$.  

### Theorem 6.2.11. Let $E$ be a subset of $R^∗$. Then the following statements are true.  
(a) For every $x \in E$ we have $x \le sup(E)$ and $x \ge inf(E)$.  
(b) Suppose that $M \in R^∗$ is an upper bound for $E$, i.e., $x \le M$ for all $x \in E$. Then we have $sup(E) \le M$.  
(c) Suppose that $M \in R^∗$ is a lower bound for $E$, i.e., $x \ge M$ for all $x \in E$. Then we have $inf(E) \ge M$.  

### Exercises  
Exercise 6.2.1. Prove Proposition 6.2.5. (Hint: you may need Proposition 5.4.7.)  
Exercise 6.2.2. Prove Theorem 6.2.11. (Hint: you may need to break into cases depending on whether $+\infty$ or $−\infty$ belongs to $E$. You can of course use Definition 5.5.10, provided that $E$ consists only of real numbers.)  

## 6.3 Suprema and Infima of sequences  
### Definitions  
* 6.3.1 (Sup and inf of sequences). Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers. Then we define $sup((a_n))^\infty_{n = m}$ to be the supremum of the set $\lbrace a_n : n \ge m \rbrace$, and $inf((a_n))^\infty_{n = m}$ to the infimum of the same set $\lbrace a_n : n \ge m \rbrace$.  


### Proposition 6.3.6 (Least upper bound property). Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers, and let x be the extended real number $x := sup((a_n))^\infty_{n = m}$. Then we have $a_n \le x$ for all $n \ge m$. Also, whenever $M \in R^∗$ is an upper bound for $a_n$ (i.e., $a_n le M$ for all $n \ge m$), we have $x \le M$. Finally, for every extended real number $y$ for which $y < x$, there exists at least one $n \le m$ for which $y < a_n \le x$.  

### Proposition 6.3.8 (Monotone bounded sequences converge). Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers which has some finite upper bound $M \in R$, and which is also increasing (i.e., $a_{n+1} \ge a_n$ for all $n \ge m$). Then $(a_n)^\infty_{n = m}$ is convergent, and in fact $\lim_{n \rightarrow \infty} a_n = sup(a_n)^\infty_{n = m} \le M$.  
* Suppose $sup(a_n) = x$ and $\epsilon > 0$,

### Proposition 6.3.10. Let $0 < x < 1$. Then we have $\lim_{n \rightarrow \infty} x^n = 0$.  

### Exercise  
Exercise 6.3.1. Verify the claim in Example 6.3.4.  
* example 6.3.4. Let $a_n := 1/n$; thus $(a_n)^\infty_{n = 1}$ is the sequence $1, 1/2, 1/3, ...$. Then the set {an : n ≥ 1} is the countable set {1, 1/2, 1/3, 1/4, . . . }. Thus $sup((a_n))^\infty_{n = 1} = 1$ and $inf(a_n)^\infty_{n = 1} = 0$.  

Exercise 6.3.2. Prove Proposition 6.3.6. (Hint: use Theorem 6.2.11.)  
Exercise 6.3.3. Prove Proposition 6.3.8. (Hint: use Proposition 6.3.6, together with the assumption that $a_n$ is increasing, to show that an converges to $sup(a_n)^\infty_{n = m}$.)  
Exercise 6.3.4. Explain why Proposition 6.3.10 fails when $x > 1$. In fact, show that the sequence $(x_n)^\infty_{n = 1}$ diverges when $x > 1$. (Hint: prove by contradiction and use the identity $(1/x)^nx^n = 1$ and the limit laws in Theorem 6.1.19.) Compare this with the argument in Example 1.2.3; can you now explain the flaws in the reasoning in that example?  

## 6.4 Limsup, Liminf, and limit points  
### Definitions  
* 6.4.1 (Limit points). Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers, let $x$ be a real number, and let $\epsilon > 0$ be a real number. We say that $x$ is $\epsilon$-adherent to $(a_n)^\infty_{n = m}$ iff there exists an n ≥ m such that an is ε-close to x. We say that x is continually $\epsilon$-adherent to $(a_n)^\infty_{n = m}$ iff it is $\epsilon$-adherent to $(a_n)^\infty_{n = N}$ for every $N \ge m$. We say that $x$ is a limit point or adherent point of $(a_n)^\infty_{n = m}$ iff it is continually $\epsilon$-adherent to $(a_n)^\infty_{n = m}$ for every $\epsilon > 0$.  
* 6.4.6 (Limit superior and limit inferior). Suppose that $(a_n)^\infty_{n = m}$ is a sequence. We define a new sequence $(a_N^+)^\infty_{N = m}$ by the formula $a_N^+ = sup(a_n)^\infty_{n = N}$. More informally, $a_N^+$ is the supremum of all the elements in the sequence from $a^N$ onwards. We then define the limit superior of the sequenc $(a_n)^\infty_{n = m}$, denoted $lim \ sup_{n \rightarrow \infty} a_n$, by the formula $lim \ sup_{n \rightarrow \infty} a_n = inf(a_N^+)^\infty_{N = m}$. Similarly, we can define $a_N^- = inf(a_n)^\infty_{n = N}$ and define the limit inferior of the sequence $(a_n)^\infty_{n = m}$, denoted $lim \ inf_{n \rightarrow \infty} a_n$, by the formula $lim \ inf_{n \rightarrow \infty} a_n = sup(a_N^+)^\infty_{N = m}$.

### Proposition 6.4.5 (Limits are limit points). Let $(a_n)^\infty_{n = m}$ be a sequence which converges to a real number $c$. Then $c$ is a limit point of $(a_n)^\infty_{n = m}$, and in fact it is the only limit point of $(a_n)^\infty_{n = m}$.  
* Let $\epsilon > 0$, then $\exists j \ st. \ |a_n - c| < \epsilon$ for all $n \ge j$. Thus $\forall N \ge m, (a_n)^\infty_{n = N}, \exists n \ st. \ |a_n - c| \le \epsilon$.  
* Suppse there another limit point $d$, 

### Proposition 6.4.12. Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers, let $L^+$ be the limit superior of this sequence, and let $L^−$ be the limit inferior of this sequence (thus both $L^+$ and $L^−$ are extended real numbers).  
(a) For every $x > L^+$, there exists an $N \ge m$ such that $a_n < x$ for all $n \ge N$. (In other words, for every $x > L^+$, the elements of the sequence $(a_n)^\infty_{n = m}$ are eventually less than $x$.) Similarly, for every $y < L^−$ there exists an $N \ge m$ such that $a_n > y$ for all $n \ge N$.  
(b) For every $x < L^+$, and every $N \ge m$, there exists an $n \ge N$ such that $a_n > x$. (In other words, for every $x < L^+$, the elements of the sequence $(a_n)^\infty_{n = m}$ exceed $x$ infinitely often.) Similarly, for every $y > L^−$ and every $N \ge m$, there exists an $n \ge N$ such that $a_n < y$.  