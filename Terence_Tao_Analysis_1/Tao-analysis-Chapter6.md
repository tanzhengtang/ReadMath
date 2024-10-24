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
* 