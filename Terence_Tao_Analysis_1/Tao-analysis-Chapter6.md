# Chapter 6 Limits of sequences  
## 6.1 Convergence and limit laws  
### Definitions  
* 6.1.1 (Distance between two real numbers). Given two real numbers $x$ and $y$, we define their distance $d(x, y)$ to be $d(x, y) := |x − y|$.  
* 6.1.2 ($\epsilon$-close real numbers). Let $\epsilon > 0$ be a real number. We say that two real numbers $x, y$ are $\epsilon$-close iff we have $d(y, x) \le \epsilon$.  
* 6.1.3 (Cauchy sequences of reals). Let $\epsilon > 0$ be a real number. A sequence $(a_n)^\infty_{n = N}$ of real numbers starting at some integer index $N$ is said to be $\epsilon$-steady iff $a_j$ and $a_k$ are $\epsilon$-close for every $j, k \ge N$. A sequence $(a_n)^\infty_{n = m}$ starting at some integer index $m$ is said to be eventually $\epsilon$-steady iff there exists an $N \ge m$ such that $(a_n)^\infty_{n = N}$ is $\epsilon$-steady. We say that $(a_n)^\infty_{n = m}$ is a Cauchy sequence iff it is eventually $\epsilon$-steady for every $\epsilon > 0$.  
* 6.1.5 (Convergence of sequences). Let $\epsilon > 0$ be a real number, and let $L$ be a real number. A sequence $(a_n)^\infty_{n = N}$ of real numbers is said to be $\epsilon$-close to $L$ iff an is $\epsilon$-close to $L$ for every $n \ge N$, i.e., we have $|a_n − L| \le ε$ for every $n \ge N$. We say that a sequence $(a_n)^\infty_{n = m}$ is eventually $\epsilon$-close to $L$ iff there exists an $N \ge m$ such that $(a_n)^\infty_{n = N}$ is $\epsilon$-close to $L$. We say that a sequence $(a_n)^\infty_{n = m}$ converges to $L$ iff it is eventually $\epsilon$-close to $L$ for every real $\epsilon > 0$.  
* 6.1.8 (Limits of sequences). If a sequence $(a_n)^\infty_{n = m}$ converges to some real number $L$, we say that $(a_n)^\infty_{n = m}$ is convergent and that its limit is $L$; we write $L = \lim_{n \rightarrow \infty} a_n$ to denote this fact. If a sequence $(a_n)^\infty_{n = m}$ is not converging to any real number $L$, we say that the sequence $(a_n)^\infty_{n = m}$ is divergent and we leave $\lim_{n \rightarrow \infty} a_n$ undefined.  
* 6.1.16 (Bounded sequences). A sequence $(a_n)^\infty_{n = m}$ of real numbers is bounded by a real number $M$ iff we have $|a_n| \le M$ for all $n \ge m$. We say that $(a_n)^\infty_{n = m}$ is bounded iff it is bounded by $M$ for some real number $M > 0$.  

### Proposition 6.1.4. Let $(a_n)^\infty_{n = m}$ be a sequence of rational numbers starting at some integer index $m$. Then $(a_n)^\infty_{n = m}$ is a Cauchy sequence in the sense of Definition 5.1.8 if and only if it is a Cauchy sequence in the sense of Definition 6.1.3.  
* If $(a_n)^\infty_{n = m}$ is a Cauchy sequence in the sense of Definition 5.1.8, then $\forall \epsilon \in R, \exists \epsilon^\prime \in Q, \ st. \ \epsilon^\prime < \epsilon$, and this is enough to get that $(a_n)^\infty_{n = m}$ is also a Cauchy sequence in the sense of Definition Definition 6.1.3.  
* If $(a_n)^\infty_{n = m}$ is a Cauchy sequence in the sense of Definition 6.1.3, simliarly, $\forall \epsilon \in Q, \exists \epsilon^\prime \in R, \ st. \ \epsilon^\prime < \epsilon$ which is also enough to get right conclusion.  

### Proposition 6.1.7 (Uniqueness of limits). Let $(a_n)^\infty_{n = m}$ be a real sequence starting at some integer index $m$, and let $L \ne L^\prime$ be two distinct real numbers. Then it is not possible for $(a_n)^\infty_{n = m}$ to converge to $L$ while also converging to $L^\prime$.  
* Suppoe $L \ne L^\prime$ and $(a_n)^\infty_{n = m}$ converges to $L, L^\prime$ both. Let $\epsilon = L - L^\prime$(suppose $L > L^\prime$), and $\epsilon / 3 > 0, \exists N \ st. \ |a_m - L| < \epsilon / 3, |a_m - L^\prime| < \epsilon / 3$ for all $m \ge N$. Then $|a_m - L| + |a_m - L^\prime| \ge |L - a_m + a_m - L^\prime| = |L - L^\prime| = \epsilon$, but we already have $|a_m - L| + |a_m - L^\prime| \le \epsilon / 3 + \epsilon / 3 = 2\epsilon / 3$ which get $\epsilon \le |a_m - L| + |a_m - L^\prime| \le 2\epsilon / 3$. This is a contradiction.  

### Proposition 6.1.11. We have $\lim_{n \rightarrow \infty} 1/n = 0$.  
* By Exercise 5.4.4, $\forall \epsilon \in R$ and $\epsilon > 0$, there exists $N$ such that $\epsilon > 1 / N$. Then for all $n \ge N$ we have $\epsilon > 1 / n \Rightarrow |1 / n| < \epsilon$ for all $n \ge N$. Thus $\lim_{n \rightarrow \infty} 1/n = 0$.  

### Proposition 6.1.12 (Convergent sequences are Cauchy). Suppose that $(a_n)^\infty_{n = m}$ is a convergent sequence of real numbers. Then $(a_n)^\infty_{n = m}$ is also a Cauchy sequence.  
* Suppose $a_n$ is a convergent sequence, $L = \lim_{n \rightarrow \infty} a_n$. Let $\epsilon > 0 \Rightarrow \epsilon / 2 > 0 \Rightarrow \ \exist j \ st. \ n \ge j, |a_n - L| < \epsilon / 2 \Rightarrow \forall n, m \ge j, |a_n - a_m| = |a_n - L + L - a_m| \le |a_n - L| + |a_m - L| \le \epsilon / 2 + \epsilon / 2 \le \epsilon$. Then $a_n$ is a Cauchy seqencue.  

### Proposition 6.1.15 (Formal limits are genuine limits). Suppose that $(a_n)^\infty_{n = 1}$ is a Cauchy sequence of rational numbers. Then $(a_n)^\infty_{n = 1}$ converges to $LIM_{n \rightarrow \infty} a_n$.  
* See Exercise 6.1.6  
* Suppose $(a_n)^\infty_{n = 1}$ does not converges to $LIM_{n \rightarrow \infty} a_n = L$. Then $\exists \epsilon > 0, \forall N, \exists n \ge N \ st. \ |a_n - L| > \epsilon$.  
* If $L = 0$, then $|a_n| > \epsilon$ and $a_na_m > 0 \Rightarrow a_m > 0$ for all $m \ge N \Rightarrow LIM_{n \rightarrow \infty} a_n > L = 0$ which lead a contradiction.  

### Corollary 6.1.17. Every convergent sequence of real numbers is bounded.  
* By Proposition 6.1.12 convergent sequences are Cauchy sequences, and for every Cauchy sequence is bounded.  

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
Exercise 6.1.6. Prove Proposition 6.1.15, using the following outline. Let $(a_n)^\infty_{n = m}$ be a Cauchy sequence of rationals, and write $L := LIM_{n \rightarrow \infty} a_n$. We have to show that $(a_n)^\infty_{n = m}$ converges to $L$. Let $\epsilon > 0$. Assume for sake of contradiction that sequence $a_n$ is not eventually $\epsilon$-close to $L$. Use this, and the fact that $(a_n)^\infty_{n = m}$ is Cauchy, to show that there is an $N \ge m$ such that either $a_n > L + \epsilon/2$ for all $n \ge N$, or $a_n < L − \epsilon/2$ for all $n \ge N$. Then use Exercise 5.4.8.  
* Suppose $a_n$ is not converge to $L$, then $\exists \  \epsilon > 0 \ st. \ a_n$ is not eventually $\epsilon$-close to $L$. And $0 < \epsilon / 2 < \epsilon \Rightarrow |a_n - a_m| < \epsilon / 2$ for some $j \in N$ and $n, m \ge j$. Since $a_n$ is not eventually $\epsilon$-close to $L \Rightarrow \exist \ n^\prime, |a_{n^\prime} - L| > \epsilon$ and $|a_n - a_{n^\prime}| < \epsilon / 2 \Rightarrow a_n > L + \epsilon/2$ for all $n \ge j$, or $a_n < L − \epsilon/2$ for all $n \ge j$. Thus by Exercise 5.4.8 we could get $LIM_{n \rightarrow \infty} a_n < L$ or $LIM_{n \rightarrow \infty} a_n > L$ which all lead  contradiction with $LIM_{n \rightarrow \infty} a_n = L$.  

Exercise 6.1.7. Show that Definition 6.1.16 is consistent with Definition 5.1.12 (i.e., prove an analogue of Proposition 6.1.4 for bounded sequences instead of Cauchy sequences).  
* Suppose $m \in R$ and $|a_n| \le m$ by Definition 6.1.16, it's easy to get another $q \in Q, q \ge m$, then $|a_n| \le m \le q$ which also is satisfy the Definition 5.1.12. The rest is skip.  

Exercise 6.1.8. Prove Theorem 6.1.19. (Hint: you can use some parts of the theorem to prove others, e.g., (b) can be used to prove (c); (a),(c) can be used to prove (d); and (b), (e) can be used to prove (f). The proofs are similar to those of Lemma 5.3.6, Proposition 5.3.10, and Lemma 5.3.15. For (e), you may need to first prove the auxiliary result that any sequence whose elements are non-zero, and which converges to a non-zero limit, is bounded away from zero.)  
Exercise 6.1.9. Explain why Theorem 6.1.19(f) fails when the limit of the denominator is 0. (To repair that problem requires L’Hopital’s rule, see Section 10.5.)  
* Suppose $b_n$ converges to $0$ and $c_n = a_n / b_n$ also $L$, then $c_n * b_n = a_n$ and we will get $a_n$ converges to $0$ whatever $a_n$ is , which is obviously impossible. 

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
* 6.3.1 (Sup and inf of sequences). Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers. Then we define $sup(a_n)^\infty_{n = m}$ to be the supremum of the set $\lbrace a_n : n \ge m \rbrace$, and $inf(a_n)^\infty_{n = m}$ to the infimum of the same set $\lbrace a_n : n \ge m \rbrace$.  

### Proposition 6.3.6 (Least upper bound property). Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers, and let $x$ be the extended real number $x := sup(a_n)^\infty_{n = m}$. Then we have $a_n \le x$ for all $n \ge m$. Also, whenever $M \in R^∗$ is an upper bound for $a_n$ (i.e., $a_n \le M$ for all $n \ge m$), we have $x \le M$. Finally, for every extended real number $y$ for which $y < x$, there exists at least one $n \le m$ for which $y < a_n \le x$.  
* Suppose for all $a_n$ such that $a_n < y$, then $y$ is an upper bound for $a_n$ which will lead $y \ge x$. And this is a contradiction with $y < x$.  

### Remark 6.3.7. There is a corresponding Proposition 6.3.6 for infima, but with all the references to order reversed, e.g., all upper bounds should now be lower bounds, etc. The proof is exactly the same.  

### Proposition 6.3.8 (Monotone bounded sequences converge). Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers which has some finite upper bound $M \in R$, and which is also increasing (i.e., $a_{n+1} \ge a_n$ for all $n \ge m$). Then $(a_n)^\infty_{n = m}$ is convergent, and in fact $\lim_{n \rightarrow \infty} a_n = sup(a_n)^\infty_{n = m} \le M$.  One can similarly prove that if a sequence $(a_n)^\infty_{n = m}$ is bounded below and decreasing (i.e., $a_{n+1} \le a_n$ ), then it is convergent, and that the limit is equal to the infimum.   
* For all real number $\epsilon > 0$, by Proposition 6.3.6 we have $sup(a_n)^\infty_{n = m} - \epsilon < a_n \le sup(a_n)^\infty_{n = m}$ for some $n \ge m$, and because $a_n \le a_{n + 1} \le ... \le a_{n + k} \le sup(a_n)^\infty_{n = m}$ for all $k \ge 0$, then $|a_{n^\prime} - sup(a_n)^\infty_{n = m}| < \epsilon$ for all $n^\prime \ge n$. Thus $\lim_{n \rightarrow \infty} a_n = sup(a_n)^\infty_{n = m} \le M$.  

### Proposition 6.3.10. Let $0 < x < 1$. Then we have $\lim_{n \rightarrow \infty} x^n = 0$.  

### Exercise  
Exercise 6.3.1. Verify the claim in Example 6.3.4.  
* Example 6.3.4. Let $a_n := 1/n$; thus $(a_n)^\infty_{n = 1}$ is the sequence $1, 1/2, 1/3, ...$. Then the set $\lbrace a_n : n \ge 1 \rbrace$ is the countable set $\lbrace 1, 1/2, 1/3, 1/4, ... \rbrace$. Thus $sup(a_n)^\infty_{n = 1} = 1$ and $inf(a_n)^\infty_{n = 1} = 0$.  
* $a_n := 1/n$ is a decreasing sequence, then for every $n \in N, a_n \le a_1 \Rightarrow sup(a_n)^\infty_{n = 1} = 1$. If $inf(a_n)^\infty_{n = 1} \ne 0$ and $inf(a_n)^\infty_{n = 1} = \epsilon$, by Exercise 5.4.3, there exists $N$ such that $N \le \epsilon^{-1} < N + 1 \Rightarrow 1 / (N + 1) < \epsilon \le 1 / N$ which lead a contradiction $\epsilon \le a_n$ for all $n \in N$.  

Exercise 6.3.2. Prove Proposition 6.3.6. (Hint: use Theorem 6.2.11.)  
Exercise 6.3.3. Prove Proposition 6.3.8. (Hint: use Proposition 6.3.6, together with the assumption that $a_n$ is increasing, to show that an converges to $sup(a_n)^\infty_{n = m}$.)  
Exercise 6.3.4. Explain why Proposition 6.3.10 fails when $x > 1$. In fact, show that the sequence $(x^n)^\infty_{n = 1}$ diverges when $x > 1$. (Hint: prove by contradiction and use the identity $(1/x)^nx^n = 1$ and the limit laws in Theorem 6.1.19.) Compare this with the argument in Example 1.2.3; can you now explain the flaws in the reasoning in that example?  
* Suppose $(x^n)^\infty_{n = 1} (x > 1)$ converges to $L$, then $\lim_{n \rightarrow \infty} 1 / x^n$ also converges to $0$ by Proposition 6.3.8, $\lim_{n \rightarrow \infty} (1 / x)^n(x^n) = 1 = L*0$ which lead a obvious contradiction.  
* Note: Limit Laws will be used when sure the sequence is convergent.  

## 6.4 Limsup, Liminf, and limit points  
### Definitions  
* 6.4.1 (Limit points). Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers, let $x$ be a real number, and let $\epsilon > 0$ be a real number. We say that $x$ is $\epsilon$-adherent to $(a_n)^\infty_{n = m}$ iff there exists an $n \ge m$ such that $a_n$ is $\epsilon$-close to $x$. We say that $x$ is continually $\epsilon$-adherent to $(a_n)^\infty_{n = m}$ iff it is $\epsilon$-adherent to $(a_n)^\infty_{n = N}$ for every $N \ge m$. We say that $x$ is a limit point or adherent point of $(a_n)^\infty_{n = m}$ iff it is continually $\epsilon$-adherent to $(a_n)^\infty_{n = m}$ for every $\epsilon > 0$.  
* 6.4.6 (Limit superior and limit inferior). Suppose that $(a_n)^\infty_{n = m}$ is a sequence. We define a new sequence $(a_N^+)^\infty_{N = m}$ by the formula $a_N^+ = sup(a_n)^\infty_{n = N}$. More informally, $a_N^+$ is the supremum of all the elements in the sequence from $a^N$ onwards. We then define the limit superior of the sequence $(a_n)^\infty_{n = m}$, denoted $lim \ sup_{n \rightarrow \infty} a_n$, by the formula $lim \ sup_{n \rightarrow \infty} a_n = inf(a_N^+)^\infty_{N = m}$. Similarly, we can define $a_N^- = inf(a_n)^\infty_{n = N}$ and define the limit inferior of the sequence $(a_n)^\infty_{n = m}$, denoted $lim \ inf_{n \rightarrow \infty} a_n$, by the formula $lim \ inf_{n \rightarrow \infty} a_n = sup(a_N^+)^\infty_{N = m}$.

### Proposition 6.4.5 (Limits are limit points). Let $(a_n)^\infty_{n = m}$ be a sequence which converges to a real number $c$. Then $c$ is a limit point of $(a_n)^\infty_{n = m}$, and in fact it is the only limit point of $(a_n)^\infty_{n = m}$.  
* Let $\epsilon > 0$, then $\exists j \ st. \ |a_n - c| < \epsilon$ for all $n \ge j$ and $c$ is a limit point of $(a_n)^\infty_{n = m}$. Thus $\forall N \ge m, (a_n)^\infty_{n = N}, \exists n \ st. \ |a_n - c| \le \epsilon$.  
* Suppose $L^\prime$ is also a limit point of $a_n$. Let $L = c, \epsilon^\prime = L - L^\prime$, then $\exist j \ st. \ |a_j - L^\prime| \le \epsilon^\prime / 3$ and $|a_j - L| \le \epsilon^\prime$ too, we could get $|a_j - L^\prime| + |a_j - L| \ge |a_j - L^\prime - L + a_j| = |L - L^\prime| = \epsilon^\prime$ but $|a_j - L^\prime| + |a_j - L| \le \epsilon^\prime / 3 + \epsilon^\prime / 3 = 2\epsilon^\prime / 3 \Rightarrow \epsilon^\prime \le |a_j - L^\prime| + |a_j - L| \le 2\epsilon^\prime / 3$ is a obvious contradiction.  

### Proposition 6.4.12. Let $(a_n)^\infty_{n = m}$ be a sequence of real numbers, let $L^+$ be the limit superior of this sequence, and let $L^-$ be the limit inferior of this sequence (thus both $L^+$ and $L^-$ are extended real numbers).  
(a) For every $x > L^+$, there exists an $N \ge m$ such that $a_n < x$ for all $n \ge N$ (In other words, for every $x > L^+$, the elements of the sequence $(a_n)^\infty_{n = m}$ are eventually less than $x$.) Similarly, for every $y < L^-$ there exists an $N \ge m$ such that $a_n > y$ for all $n \ge N$.  
* By Proposition 6.3.6, $\exists N^\prime \ st. \ L^+ \le a_{N^\prime}^+ < x \Rightarrow sup(a_n)^\infty_{n = N^\prime} < x \Rightarrow \forall n \ge N^\prime, a_n \le sup(a_n)^\infty_{n = N^\prime} < x$.  

(b) For every $x < L^+$, and every $N \ge m$, there exists an $n \ge N$ such that $a_n > x$. (In other words, for every $x < L^+$, the elements of the sequence $(a_n)^\infty_{n = m}$ exceed $x$ infinitely often.) Similarly, for every $y > L^-$ and every $N \ge m$, there exists an $n \ge N$ such that $a_n < y$.  
* $x < L^+ \Rightarrow \forall N \ge m, x < a_N^+ \Rightarrow \forall N \ge m, x < sup(a_n)^\infty_{n = N}$, and by Proposition 6.3.6 again, we could get $N^\prime \ge m$ such that $x < a_{N^\prime} \le sup(a_n)^\infty_{n = N}$.  

(c) We have $inf(a_n)^\infty_{n = m} \le L^- \le L^+ \le sup(a_n)^\infty_{n = m}$.  
* Suppose $L^- > L^+$, then $L^- > a_N^+ \ge L^+$ for some $N$ and use (a) again we have $L^- \ge a_M^- > a_N^+ \ge L^+$. Let $Q = Max(M, N)$, then $a_Q \le a_N^+ < a_M^- \le a_Q$, which is a contradiction for $a_Q < a_Q$.  

(d) If $c$ is any limit point of $(a_n)^\infty_{n = m}$, then we have $L^- \le c \le L^+$.  
* Suppose $c > L^+$ or $c < L^-$. For one of those hypothesis about $c > L^+$, then there exists an $N \ge m$ such that $a_n < c$ for all $n \ge N$ and if let $\epsilon^\prime = a_n - c$, when $n \ge N$, we could find a $\epsilon < \epsilon^\prime$ such that $a_n$ is not $\epsilon$-close to $c$ which lead a contradiction with $c$ is a limit point.  

(e) If $L^+$ is finite, then it is a limit point of $(a_n)^\infty_{n = m}$. Similarly, if $L^-$ is finite, then it is a limit point of $(a_n)^\infty_{n = m}$.  
* $\forall \epsilon > 0, x = L^+ - \epsilon < L^+$, and use (b) for every $N \ge m$, there exists an $n \ge N$ such that $L^+ > a_n > x \Rightarrow d(L^+, a_n) < \epsilon$. Thus $L^+$ is a limit point.  

(f) Let $c$ be a real number. If $(a_n)^\infty_{n = m}$ converges to $c$, then we must have $L^+ = L^- = c$. Conversely, if $L^+ = L^- = c$, then $(a_n)^\infty_{n = m}$ converges to $c$.  
* Suppose $L^+$ is infinite, and let $\epsilon > 0$, since $(a_n)^\infty_{n = m}$ converges to $c$, there exists $m$ such that $\forall n \ge m, |a_n - c| < \epsilon$. But if $L^+$ is infinite, use (b) there always exists an $n \ge m$ such that $a_n > c + \epsilon$ since $c + \epsilon < L^+$ which lead a contradiction with $|a_n - c| < \epsilon$. Similarly, we could prove that $L^-$ is also finite. Thus by (e) and Proposition 6.4.5, we get $L^+ = L^- = c$.  
* Use (a) could prove that $a_n$ converges to $c$.  

### Lemma 6.4.13 (Comparison principle). Suppose that $(a_n)^\infty_{n = m}$ and $(b_n)^\infty_{n = m}$ are two sequences of real numbers such that $a_n \le b_n$ for all $n \ge m$. Then we have the inequalities 
(a) $sup(a_n)^\infty_{n = m} \le sup(b_n)^\infty_{n = m}$  
* Suppose $sup(a_n)^\infty_{n = m} > sup(b_n)^\infty_{n= m} \Rightarrow \exist \ N \ st. \ a_N > sup(b_n)^\infty_{n= m}$ which is a contradiction.  

(b) $inf(a_n)^\infty_{n = m} \le inf(b_n)^\infty_{n = m}$  
(c) $lim \ sup_{n \rightarrow \infty} a_n \le lim \ sup_{n \rightarrow \infty} b_n$  
(d) $lim \ inf_{n \rightarrow \infty} a_n \le lim \ inf_{n \rightarrow \infty} b_n$  
* Since $lim \ inf_{n \rightarrow \infty} a_n = sup(a_N^-)^\infty_{N = m}, lim \ inf_{n \rightarrow \infty} b_n = sup(b_N^-)^\infty_{N = m}$, and $\forall N, inf(a_n)^\infty_{n = N} \le inf(b_n)^\infty_{n = N}$ by (b) then $a_N^- \le b_N^-$ for all $N$, use (a) on $a_N^-$ and $b_N^-$ we have $sup(a_N^-)^\infty_{N = m} \le sup(b_N^-)^\infty_{N = m}$.  

### Corollary 6.4.14 (Squeeze test). Let $(a_n)^\infty_{n = m},(b_n)^\infty_{n = m},(c_n)^\infty_{n = m}$ be sequences of real numbers such that $a_n \le b_n \le c_n$ for all $n \ge m$. Suppose also that $(a_n)^\infty_{n = m}$ and $(c_n)^\infty_{n = m}$ both converge to the same limit $L$. Then $(b_n)^\infty_{n = m}$ is also convergent to $L$.  
* Use (c) and (d) of Lemma 6.4.13, $lim \ sup_{n \rightarrow \infty} a_n \le lim \ sup_{n \rightarrow \infty} b_n \le lim \ sup_{n \rightarrow \infty} c_n$ and $lim \ inf_{n \rightarrow \infty} a_n \le lim \ inf_{n \rightarrow \infty} b_n \le lim \ inf_{n \rightarrow \infty} c_n$, and by (f) of Proposition 6.4.12 $L \le lim \ sup_{n \rightarrow \infty} b_n \le L$ and $L \le lim \ inf_{n \rightarrow \infty} b_n \le L \Rightarrow (b_n)^\infty_{n = m}$ is also convergent to $L$.  

### Corollary 6.4.17 (Zero test for sequences). Let $(a_n)^\infty_{n = M}$ be a sequence of real numbers. Then the limit $lim_{n \rightarrow \infty} a_n$ exists and is equal to zero if and only if the limit $lim_{n \rightarrow \infty} |a_n|$ exists and is equal to zero.  
* If $lim_{n \rightarrow \infty} |a_n|$ exists and is equal to zero, then $lim_{n \rightarrow \infty} -|a_n|$ also exists and is equal to zero. And $-|a_n| \le a_n \le |a_n|$ for all $n \ge M$, by Corollary 6.4.14 we could get $lim_{n \rightarrow \infty} a_n$ exists and is equal to zero.  
* If $lim_{n \rightarrow \infty} a_n$ exists and is equal to zero $\Rightarrow \exist N \ge m \ st. \ \forall \epsilon > 0, |a_n| \le \epsilon$ for all $n \ge N$, obviously $|a_n| \le \epsilon \Rightarrow ||a_n|| \le \epsilon$ thus $lim_{n \rightarrow \infty} |a_n|$ exists and is equal to zero.  

### Theorem 6.4.18 (Completeness of the reals). A sequence $(a_n)^\infty_{n = 1}$ of real numbers is a Cauchy sequence if and only if it is convergent.  
* If $a_n$ is a Cauchy sequence, and suppose $L^+ = inf(a_N^+)^\infty_{N = 1}, L^- = sup(a_N^-)^\infty_{N = 1}$. If $L^+$ is infinite and $L^-$ is infinite, then for all $\epsilon / 2 > 0$ has a $N^\prime$ such that $|a_n - a_m| \le \epsilon / 2$ for all $n, m \ge N^\prime$ but use (b) of Proposition 6.4.12 we could find $n^\prime, m^\prime$ such that $a_{n^\prime} > \epsilon, a_{m^\prime} < \epsilon / 2$ since $\epsilon < L^+, \epsilon / 2 > L^-$ which lead $|a_{n^\prime} - a_{m^\prime}| > \epsilon / 2$ is a contradiction. If $L^+$ is infinite and $L^-$ is finite, similarly, $|a_n - a_m| \le \epsilon / 2$ for all $n, m \ge N^\prime$, then we could find $n^\prime, m^\prime$ such that $a_{n^\prime} > |L^-| + \epsilon, a_{m^\prime} < |L^-| + \epsilon / 2$ since $|L^-| + \epsilon < L^+, |L^-| + \epsilon / 2 > L^-$ which lead $|a_{n^\prime} - a_{m^\prime}| > \epsilon / 2$ again. The rest status of $L^+, L^-$ will all lead similar contradiction except $L^+, L^-$ are all finite. Now $L^+, L^-$ must be finite, suppose $L^+ \ne L^- \Rightarrow L^- + d = L^+$ for some $d > 0$, then has a $N^\prime \ge 0$ such that $|a_n - a_m| \le d / 3$ for all $n, m \ge N^\prime$, use (b) of Proposition 6.4.12 again, exist $n^\prime, m^\prime$ such that $a_{n^\prime} > |L^-| + 2d / 3, a_{m^\prime} < |L^-| + d / 3$ since $|L^-| + 2d / 3 < L^+, |L^-| + d / 3 > L^-$ which lead $|a_{n^\prime} - a_{m^\prime}| > d / 3$. Thus $L^+ = L^-$ and by (f) of Proposition 6.4.12 $a_n$ is convergent.  
* If $a_n$ is convergent then it's also a Cauchy seqencue by Proposition 6.1.12.  

### Exercise  
Exercise 6.4.1. Prove Proposition 6.4.5.  
Exercise 6.4.2. State and prove analogues of Exercises 6.1.3 and 6.1.4 for limit points, limit superior, and limit inferior.  
Exercise 6.4.3. Prove parts (c),(d),(e),(f) of Proposition 6.4.12. (Hint: you can use earlier parts of the proposition to prove later ones.)  
Exercise 6.4.4. Prove Lemma 6.4.13.  
Exercise 6.4.5. Use Lemma 6.4.13 to prove Corollary 6.4.14.  
Exercise 6.4.6. Give an example of two bounded sequences $(a_n)^\infty_{n = 1}$ and $(b_n)^\infty_{n = 1}$ such that $a_n < b_n$ for all $n \ge 1$, but that $sup(a_n)^\infty_{n = 1} \not < sup(b_n)^\infty_{n = 1}$. Explain why this does not contradict Lemma 6.4.13.  
* Let $a_1 = 0.9, a_2 = 0.99, ..., a_n = 0.9999....999$ and $b_n = a_{n + 1}$, then $a_n < b_n$ for all $n \ge 1$, obviously $sup(a_n) = sup(b_n) = 1$.  
*  In Lemma 6.4.13 $sup(a_n)^\infty_{n = m} \le sup(b_n)^\infty_{n = m}$ contain the $sup(a_n)^\infty_{n = m} = sup(b_n)^\infty_{n = m}$.  
 
Exercise 6.4.7. Prove Corollary 6.4.17. Is the corollary still true if we replace zero in the statement of this Corollary by some other number?  
* If the limit of $a_n$ is a negative real number, the Corollary 6.4.17 will be not true since $|a_n|$ is always greater or equal zero.  

Exercise 6.4.8. Let us say that a sequence $(a_n)^\infty_{n = M}$ of real numbers has $+\infty$ as a limit point iff it has no finite upper bound, and that it has $-\infty$ as a limit point iff it has no finite lower bound. With this definition, show that $lim \ sup_{n \rightarrow \infty} a_n$ is a limit point of $(a_n)^\infty_{n = M}$ , and furthermore that it is larger than all the other limit points of $(a_n)^\infty_{n = M}$; in other words, the limit superior is the largest limit point of a sequence. Similarly, show that the limit inferior is the smallest limit point of a sequence. (One can use Proposition 6.4.12 in the course of the proof.)  

Exercise 6.4.9. Using the definition in Exercise 6.4.8, construct a sequence $(a_n)^\infty_{n = 1}$ which has exactly three limit points, at $-\infty, 0$, and $+\infty$.  

Exercise 6.4.10. Let $(a_n)^\infty_{n = N}$ be a sequence of real numbers, and let $(b_m)^\infty_{m = M}$ be another sequence of real numbers such that each $b_m$ is a limit point of $(a_n)^\infty_{n = N}$. Let $c$ be a limit point of $(b_m)^\infty_{m = M}$. Prove that $c$ is also a limit point of $(a_n)^\infty_{n = N}$. (In other words, limit points of limit points are themselves limit points of the original sequence.)  
* $\forall \epsilon > 0, \exists j, i \ st. \ |b_j - c| \le \epsilon / 2, |a_i - b_j| \le \epsilon / 2 \Rightarrow |a_i - c| = |a_i - b_j + b_j - c| \le |a_i - b_j| + |b_j - c| \le \epsilon$. Thus $c$ is a limit point of $(a_n)^\infty_{n = N}$.  

## 6.5 Some standard limits  
### Corollary 6.5.1. We have $lim_{n \rightarrow \infty} 1/n^{1/k} = 0$ for every integer $k \ge 1$.  
* Obviously, $a_n = (1 / n)^{1 / k}$ is a decreasing sequence, and $0 \le a_n \le 1$, thus by Proposition 6.3.8, $a_n$ is convergent. We already know that $lim_{n \rightarrow \infty} 1 / n = 0$, use Theorem 6.1.19, $(a_n)^k = 1 / n \Rightarrow (lim_{n \rightarrow \infty} 1/n^{1/k})^k = lim_{n \rightarrow \infty} 1 / n = 0 \Rightarrow lim_{n \rightarrow \infty} 1/n^{1/k} = 0$.  

### Lemma 6.5.2. Let $x$ be a real number. Then the limit $lim_{n \rightarrow \infty} x^n$ exists and is equal to zero when $|x| < 1$, exists and is equal to $1$ when $x = 1$, and diverges when $x = -1$ or when $|x| > 1$.  
* If $|x| < 1$, then $b_n = |x|^n$ is a decreasing sequence and $0 \le |x|^n \le 1$, thus by Proposition 6.3.8, $b_n$ is convergent. Let $b = lim_{n \rightarrow \infty} |x|^n, c_n = |x|^{n + 1}$. Since $\forall \epsilon > 0, \exists N \ st. \ |b_n - b| \le \epsilon$ for all $n \ge N$ and $c_n = b_{n + 1}$ then we also get $|c_n - b| \le \epsilon$ for all $n \ge N + 1$. Now $lim_{n \rightarrow \infty} b_n = lim_{n \rightarrow \infty} c_n = lim_{n \rightarrow \infty} x * b_n = x lim_{n \rightarrow \infty} b_n \Rightarrow b = x * b \Rightarrow b * (x - 1) = 0 \ and \ x - 1 \ne 0 \Rightarrow b = 0 \Rightarrow lim_{n \rightarrow \infty} |x|^n = 0$. And use Corollary 6.4.17 we could get $lim_{n \rightarrow \infty} x^n = 0$ when $|x| < 1$.  
* If $|x| > 1$, let $y = 1 / x$ and $|y| < 1$, for previous proof we could get $y^n$ is convergent. Suppose $x^n$ is convergent then $lim_{n \rightarrow \infty} x^n * y^n = lim_{n \rightarrow \infty} 1 = lim_{n \rightarrow \infty} x^n * lim_{n \rightarrow \infty} y^n = lim_{n \rightarrow \infty} x^n * 0 = 0 \Rightarrow 1 = 0$ which is a contradiction. Thus $x^n$ is not convergent.  

### Lemma 6.5.3. For any $x > 0$, we have $lim_{n \rightarrow \infty} x^{1/n} = 1$.  
* If $x = 1$, obviously $lim_{n \rightarrow \infty} x^{1/n} = 1$.  
* If $x > 1$, $x^{1 / n} \ge 1$ because if $x^{1 / n} < 1 \Rightarrow (x^{1 / n})^n = x < 1$ contradiction with $x > 1$. Suppose $f = inf(x^{1 / n}) > 1$, by Lemma 6.5.2, $f^n$ is diverges and the limit of $f^n$ is $+\infty$, then we could find a $N$ such that $f^N > x \Rightarrow f > x^{1 / N}$ which will lead a contradiction with $inf(x^{1/n}) = f \le x^{1 / N}$. Thus $inf(x^{1/n}) = 1$. Since $\frac{x^{1/n}}{x^{1/(n + 1)}} = x^{1 / n(n + 1)} > 1 \Rightarrow \frac{x^{1 / n}}{x^{1 / (n + 1)}} > 1 \Rightarrow x^{1 / n} > x^{1 / (n + 1)} \Rightarrow x^n$ is a decreasing sequence. Use Proposition 6.3.8 we could get $lim_{n \rightarrow \infty} x^{1/n} = 1$.  
* If $0 < x < 1$, the proof is also like $x > 1$ by using Proposition 6.3.8. Skip.  

### Exercises  
Exercise 6.5.1. Show that $lim_{n \rightarrow \infty} 1/n^q = 0$ for any rational $q > 0$. (Hint: use Corollary 6.5.1 and the limit laws, Theorem 6.1.19.) Conclude that the limit $lim_{n \rightarrow \infty} n^q$ does not exist. (Hint: argue by contradiction using Theorem 6.1.19(e).)  
* Let $q = j / k$ which $j, k \in Z, k \ge 1$. By Corollary 6.5.1, $lim_{n \rightarrow \infty} 1/n^{1 / k} = 0$. And use the limit laws $lim_{n \rightarrow \infty} (1/n^{1 / k})^j = lim_{n \rightarrow \infty} 1/n^q = (lim_{n \rightarrow \infty} 1/n^{1 / k})^j = (0)^j = 0$.  
* If the limit $lim_{n \rightarrow \infty} n^q$ exists, then $lim_{n \rightarrow \infty} (n^q)^{-1}$ also exist, and $lim_{n \rightarrow \infty} (n^q)^{-1} = (lim_{n \rightarrow \infty} n^q)^{-1} \Rightarrow 0 = (lim_{n \rightarrow \infty} n^q)^{-1}$. Obviously, this is a contradiction.

Exercise 6.5.2. Prove Lemma 6.5.2. (Hint: use Proposition 6.3.10, Exercise 6.3.4, and the squeeze test.)  

Exercise 6.5.3. Prove Lemma 6.5.3. (Hint: you may need to treat the cases $x \ge 1$ and $x < 1$ separately. You might wish to first use Lemma 6.5.2 to prove the preliminary result that for every $\epsilon > 0$ and every real number $M > 0$, there exists an $n$ such that $M^{1/n} \le 1 + \epsilon$.)  

## 6.6 Subsequences  
### Definitions  
* 6.6.1 (Subsequences). Let $(a_n)^\infty_{n = 0}$ and $(b_n)^\infty_{n = 0}$ be sequences of real numbers. We say that $(b_n)^\infty_{n = 0}$ is a subsequence of $(a_n)^\infty_{n = 0}$ iff there exists a function $f : N \rightarrow N$ which is strictly increasing (i.e., $f(n + 1) > f (n)$ for all $n \in N$) such that $b_n = a_{f(n)}$ for all $n \in N$.  

### Lemma 6.6.4. Let $(a_n)^\infty_{n = 0}, (b_n)^\infty_{n = 0}$, and $(c_n)^\infty_{n = 0}$ be sequences of real numbers. Then $(a_n)^\infty_{n = 0}$ is a subsequence of $(a_n)^\infty_{n = 0}$. Furthermore, if $(b_n)^\infty_{n = 0}$ is a subsequence of $(a_n)^\infty_{n = 0}$, and $(c_n)^\infty_{n = 0}$ is a subsequence of $(b_n)^\infty_{n = 0}$, then $(c_n)^\infty_{n = 0}$ is a subsequence of $(a_n)^\infty_{n = 0}$.  
* Let $f(n) = n, a_{f(n)}$ is a subsequence of $a_n$ and it's easy to see $a_{f(n)} = a_n$. Thus $(a_n)^\infty_{n = 0}$ is a subsequence of $(a_n)^\infty_{n = 0}$.  
* Let $a_{f(n)} = b_n, b_{g(n)} = c_n, \forall n \in N, b_{f(n)} = c_n$ and $a_{f(g(n))} = b_{f(n)} = c_n$. It's obvious that $g \circ f$ is an increasing function. Thus $(c_n)^\infty_{n = 0}$ is a subsequence of $(a_n)^\infty_{n = 0}$.  

### Proposition 6.6.5 (Subsequences related to limits). Let $(a_n)^\infty_{n = 0}$ be a sequence of real numbers, and let $L$ be a real number. Then the following two statements are logically equivalent (each one implies the other):  
(a) The sequence $(a_n)^\infty_{n = 0}$ converges to $L$.  
(b) Every subsequence of $(a_n)^\infty_{n = 0}$ converges to $L$.  
* If $(a_n)^\infty_{n = 0}$ converges to $L$, then $\forall \epsilon, \exists i \in N \ st. \ |a_n - L| < \epsilon$ for all $n \ge i$. Let $a_{f(n)} = b_n, f$ is an increasing function from $N$ to $N$, thus for $i \in N$, the set $S = \lbrace j \in N: f(j) = i \rbrace$ is not empty, and we could have $m = inf(S)$. For $b_n$, if $n \ge m$ then $f(n) \ge i$ and $b_n \in \lbrace a_n: n \ge i \rbrace$. Thus $\forall \epsilon$ and for every $b_n$ we could find a $m$ such that $|b_n - L| < \epsilon$ for all $n \ge m$.  
* Suppose the sequence $(a_n)^\infty_{n = 0}$ not converges to $L$. Then $f(n) = n + 1, b_n = a_{f(n)}, b_n$ also not converges to $L$ which make a contradiction.  

### Proposition 6.6.6 (Subsequences related to limit points). Let $(a_n)^\infty_{n = 0}$ be a sequence of real numbers, and let $L$ be a real number. Then the following two statements are logically equivalent.
(a) $L$ is a limit point of $(a_n)^\infty_{n = 0}$. 
(b) There exists a subsequence of $(a_n)^\infty_{n = 0}$ which converges to $L$.  
* Hint: to show that (a) implies (b), define the numbers $n_j$ for each natural numbers $j$ by the formula $n_j := min \lbrace n > n_{j-1} : |a_n - L| \le 1/j \rbrace$, with the convention $n_0 := 0$, explaining why the set $\lbrace n > n_{j-1} : |a_n - L| \le 1/j \rbrace$ is non-empty. Then consider the sequence $a_{n_j}$.  
* Let $b_j = a_{n_j}$, and it's easy to see $b_j$ is a subsequence of $a_n$. $\forall \epsilon > 0, \exists k \in N, k \ge 1 / \epsilon \Rightarrow 1 / k \le \epsilon$. Then $|a_{n_k}(b_k) - L| \le 1 / k \le \epsilon \Rightarrow b_j$ converges to $L$.  
* Let $b_n$ be the subsequence of $(a_n)^\infty_{n = 0}$ which converges to $L$ and $f$ denote the increasing function such that $b_n = a_{f(n)}$. $\forall \epsilon, \forall N, \exists k \ge N \ st. \ |b_k - L| \le \epsilon$. Since $a_{f(k)} = b_k$, we have to show that $f(k) \ge k$. If $f(k) < k$, then $f(0) < 0$ which make a contradiction with $f(n) \ge 0$. Thus $f(k) \ge k \ge N$ and $L$ is a limit point of $(a_n)^\infty_{n = 0}$.  

### Theorem 6.6.8 (Bolzano-Weierstrass theorem). Let $(a_n)^\infty_{n = 0}$ be a bounded sequence (i.e., there exists a real number $M > 0$ such that $|a_n| \le M$ for all $n \in N$). Then there is at least one subsequence of $(a_n)^\infty_{n = 0}$ which converges.  
*  Let $L^+$ denoted the limit superior of the sequence $(a_n)^\infty_{n = m}$. Since $a_n$ is bounded, $L^+$ is finite and by (e) of Proposition 6.4.12, $L^+$ is also a limit point of $a_n$. Then use Proposition 6.6.6 we could conclude that Theorem 6.6.8 is true.  

### Exercises  
Exercise 6.6.1. Prove Lemma 6.6.4.  
Exercise 6.6.2. Can you find two sequences $(a_n)^\infty_{n = 0}$ and $(b_n)^\infty_{n = 0}$ which are not the same sequence, but such that each is a subsequence of the other?  
* $a_n = 1,0,1,0,......$ and $b_n = 0,1,0,1,0,.....$

Exercise 6.6.3. Let $(a_n)^\infty_{n = 0}$ be a sequence which is not bounded. Show that there exists a subsequence $(b_n)^\infty_{n = 0}$ of $(a_n)^\infty_{n = 0}$ such that $lim_{n \rightarrow \infty} 1 / b_n$ exists and is equal to zero. (Hint: for each natural number $j$, recursively introduce the quantity $n_j := min \lbrace n \in N : |a_n| \ge j; n > n_{j - 1} \rbrace$ (omitting the condition $n > n_{j - 1}$ when $j = 0$), first explaining why the set $\lbrace |a_n| \ge j; n > n_{j - 1} \rbrace$ is non-empty. Then set $b_j := a_{n_j}$.)  
* $\forall \epsilon > 0$, let $j \in N, j \ge 1 / \epsilon \Rightarrow b_j \ge j \ge 1 / \epsilon \Rightarrow 1 / b_j \le \epsilon$. Thus $lim_{n \rightarrow \infty} 1 / b_n$ exists and is equal to zero.  

Exercise 6.6.4. Prove Proposition 6.6.5. (Note that one of the two implications has a very short proof.)  
Exercise 6.6.5. Prove Proposition 6.6.6. (Hint: to show that (a) implies (b), define the numbers $n_j$ for each natural numbers $j$ by the formula $n_j := min \lbrace n > n_{j-1} : |a_n - L| \le 1/j \rbrace$, with the convention $n_0 := 0$, explaining why the set $\lbrace n > n_{j-1} : |a_n - L| \le 1/j \rbrace$ is non-empty. Then consider the sequence $a_{n_j}$.)  

## 6.7 Real exponentiation, part II  
### Definitions  
* 6.7.2 (Exponentiation to a real exponent). Let $x > 0$ be real, and let $\alpha$ be a real number. We define the quantity $x^\alpha$ by the formula $x^\alpha = lim_{n \rightarrow \infty} x^{q_n}$, where $(q_n)^\infty_{n = 1}$ is any sequence of rational numbers converging to $\alpha$.  

### Lemma 6.7.1 (Continuity of exponentiation). Let $x > 0$, and let $\alpha$ be a real number. Let $(q_n)^\infty_{n = 1}$ be any sequence of rational numbers converging to $\alpha$. Then $(x^{q_n})^\infty_{n = 1}$ is also a convergent sequence. Furthermore, if $(q_n^\prime)^\infty_{n = 1}$ is any other sequence of rational numbers converging to $\alpha$, then $(x^{q_n^\prime})^\infty_{n = 1}$ has the same limit as $(x^{q_n})^\infty_{n = 1}$: $lim_{n \rightarrow \infty} x^{q_n} = lim_{n \rightarrow \infty} x^{q_n^\prime}$.  

### 6.7.3. All the results of Lemma 5.6.9, which held for rational numbers $q$ and $r$,continue to hold for real numbers $q$ and $r$.  

### Exercises  
Exercise 6.7.1. Prove the remaining components of Proposition 6.7.3.  