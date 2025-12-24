# Chapter 5 The real numbers  
## 5.1 Cauchy sequences  
### Definitions  
* 5.1.1 (Sequences). Let $m$ be an integer. A sequence $(a_n)^\infty_{n = m}$ of rational numbers is any function from the set $\{n \in Z: n \ge m\}$ to $Q$, i.e., a mapping which assigns to each integer $n$ greater than or equal to $m$, a rational number $a_n$. More informally, a sequence $(a_n)^\infty_{n = 0}$ of rational numbers is a collection of rationals $a_m, a_{m + 1}, a_{m + 2}, ....$  
* 5.1.3 ($\epsilon$-steadiness). Let $\epsilon > 0$. A sequence $(a_n)^\infty_{n = 0}$ is said to be $\epsilon$-steady iff each pair $a_j, a_k$ of sequence elements is $\epsilon$-close for every natural number $j, k$. In other words, the sequence $a_0, a_1, a_2, ...$  is $\epsilon$-steady iff $d(a_j, a_k) \le \epsilon$ for all $j, k$.  
* 5.1.6 (Eventual $\epsilon$-steadiness). Let $\epsilon > 0$. A sequence $(a_n)^\infty_{n = 0}$ is said to be eventually $\epsilon$-steady iff the sequence $a_N, a_{N + 1}, a_{N + 2}, ...$  is $\epsilon$-steady for some natural number $N \ge 0$. In other words, the sequence $a_0, a_1, a_2, ...$ is eventually $\epsilon$-steady iff there exists an $N \ge 0$ such that $d(a_j, a_k) \le \epsilon$ for all $j, k \ge N$.  
* 5.1.8 (Cauchy sequences). A sequence $(a_n)^\infty_{n = 0}$ of rational numbers is said to be a Cauchy sequence iff for every rational $\epsilon > 0$, the sequence $(a_n)^\infty_{n = 0}$ is eventually $\epsilon$-steady. In other words, the sequence $a_0, a_1, a_2, ...$ is a Cauchy sequence iff for every $\epsilon > 0$, there exists an $N \ge 0$ such that $d(a_j, a_k) \le \epsilon$ for all $j, k \ge N$.  
* 5.1.12 (Bounded sequences). Let $M \ge 0$ be rational. A finite sequence $a_0, a_1, a_2, ...a_n$ is bounded by $M$ iff $|a_i| \le M$ for all $1 \le i \le n$. An infinite sequence $(a_n)^\infty_{n = m}$ is bounded by $M$ iff $|a_i| \le M$ for all $i \ge 1$. A sequence is said to be bounded iff it is bounded by $M$ for some rational $M \ge 0$.  

### Proposition 5.1.11. The sequence $a_1, a_2, a_3, ...$ defined by $a_n := 1/n$ (i.e., the sequence $1, 1/2, 1/3, ...$) is a Cauchy sequence.  
* $\forall \epsilon > 0 \Rightarrow 1 / \epsilon > 0 \Rightarrow m \le 1 / \epsilon \le m + 1, m \in N \Rightarrow 1 / (m + 1) \le \epsilon \le 1 / m$. Let $n = m + 1, \forall j, k \ge m + 1, j \ge k$, then $|1 / j - 1 / k| = |(j - k) / jk| = (j - k) / jk$. Because $1 / (m + 1) - ((j - k) / jk) \ge 0$, thus $|1 / j - 1 / k| \le 1 / (m + 1) \le \epsilon$.  

### Lemma 5.1.14 (Finite sequences are bounded). Every finite sequence $a_0, a_1, a_2, ...a_n$ is bounded.  

### Lemma 5.1.15 (Cauchy sequences are bounded). Every Cauchy sequence $(a_n)^\infty_{n = 1}$ is bounded.  
* If $a_n$ is a Cauchy sequences, then there exist an $N$ such that $d(a_i,a_j) \le ε$ for $i,j \ge N$. $a_1....a_{N - 1}$ is a finite sequence so has a limit value $M$, and for $n \ge N$, because of $d(a_i,a_j) \le ε$ for $i, j \ge N$, we could select $a_N$ as a base number, obviously for $n \ge N$, $|a_n| \le |a_N| + ε$. Then foa all $a_n, a_n \le max(M,a_N + ε)$.  

### Exercise  
Exercise 5.1.1. Prove Lemma 5.1.15. (Hint: use the fact that an is eventually $1$-steady, and thus can be split into a finite sequence and a $1$-steady sequence. Then use Lemma 5.1.14 for the finite part. Note there is nothing special about the number $1$ used here; any other positive number would have sufficed.)  

## 5.2 Equivalent Cauchy sequences  
### Definitions  
* 5.2.1 ($\epsilon$-close sequences). Let $(a_n)^\infty_{n = 0}$ and $(b_n)^\infty_{n = 0}$ be two sequences, and let $\epsilon > 0$. We say that the sequence $(a_n)^\infty_{n = 0}$ is $\epsilon$-close to $(b_n)^\infty_{n = 0}$ iff $a_n$ is $\epsilon$-close to $b_n$ for each $n \in N$. In other words, the sequence $a_0, a_1, a_2, ...$  is $\epsilon$-close to the sequence $b_0, b_1, b_2, ...$ iff $|a_n − b_n| \le \epsilon$ for all $n = 0, 1, 2, ....$  
* 5.2.3 (Eventually $\epsilon$-close sequences). Let $(a_n)^\infty_{n = 0}$ and $(b_n)^\infty_{n = 0}$ be two sequences, and let $\epsilon > 0$. We say that the sequence $(a_n)^\infty_{n = 0}$ is eventually $\epsilon$-close to $(b_n)^\infty_{n = 0}$ iff there exists an $N \ge 0$ such that the sequences $(a_n)^\infty_{n = N}$ and $(b_n)^\infty_{n = N}$ are $\epsilon$-close. In other words, $a_0, a_1, a_2, ...$ is eventually $\epsilon$-close to $b_0, b_1, b_2, ...$ iff there exists an $N \ge 0$ such that $|a_n − b_n| \le \epsilon$ for all $n \ge N$.  
* 5.2.6 (Equivalent sequences). Two sequences $(a_n)^\infty_{n = 0}$ and $(b_n)^\infty_{n = 0}$ are equivalent iff for each rational $\epsilon > 0$, the sequences $(a_n)^\infty_{n = 0}$ and $(b_n)^\infty_{n = 0}$ are eventually $\epsilon$-close. In other words, $a_0, a_1, a_2, ...$ and $b_0, b_1, b_2, ...$ are equivalent iff for every rational $\epsilon > 0$, there exists an $N \ge 0$ such that $|a_n − b_n| \le \epsilon$ for all $n \ge N$.  

### Proposition 5.2.8. Let $(a_n)^\infty_{n = 0}$ and $(b_n)^\infty_{n = 0}$ be the sequences $a_n = 1 + 10^ {−n}$ and $b_n = 1 − 10^{−n}$. Then the sequences $a_n, b_n$ are equivalent.  

### Exercise  
Exercise 5.2.1. Show that if $(a_n)^\infty_{n = 1}$ and $(b_n)^\infty_{n = 1}$ are equivalent sequences of rationals, then $(a_n)^\infty_{n = 1}$ is a Cauchy sequence if and only if $(b_n)^\infty_{n = 1}$ is a Cauchy sequence.  
* Suppose $(a_n)^\infty_{n = 1}$ is a Cauchy sequence. $\forall \epsilon > 0, \epsilon / 3 > 0, \exist N \ st. \ |a_i - a_j| \le \epsilon / 3$ and $|a_i - b_i| \le \epsilon / 3$ for all $i, j \ge N$. Then $|b_i - b_j| = |(b_i - a_i) + (a_i - b_j)| \le |b_i - a_i| + |a_i - b_j| \le \epsilon / 3   + |(a_i - a_j) + (a_j - b_j)| \le \epsilon / 3 + |a_i - a_j| + |a_j - a_j| \le \epsilon / 3 + \epsilon / 3 + \epsilon / 3 = \epsilon$. Thus $(b_n)^\infty_{n = 1}$ is also a Cauchy sequence.  

Exercise 5.2.2. Let $\epsilon > 0$. Show that if $(a_n)^\infty_{n = 1}$ and $(b_n)^\infty_{n = 1}$ are eventually $\epsilon$-close, then $(a_n)^\infty_{n = 1}$ is bounded if and only if $(b_n)^\infty_{n = 1}$ is bounded.  
* Suppose $(a_n)^\infty_{n = 1}$ is bounded. For $\epsilon > 0, \exist N \ st. \ |a_n - b_n| \le \epsilon$ for all $n \ge N \Rightarrow a_n - \epsilon \le b_n \le a_n + \epsilon$ for all $n \ge N \Rightarrow (b_n)^\infty_{n = 1}$ is bounded.  

## 5.3 The construction of the real numbers  
### Definitions  
* 5.3.1 (Real numbers). A real number is defined to be an object of the form $LIM_{n \rightarrow \infty} a_n$, where $(a_n)^\infty_{n = 1}$ is a Cauchy sequence of rational numbers. Two real numbers $LIM_{n \rightarrow \infty} a_n$ and $LIM_{n \rightarrow \infty} b_n$ are said to be equal iff $(a_n)^\infty_{n = 1}$ and $(b_n)^\infty_{n = 1}$ are equivalent Cauchy sequences.The set of all real numbers is denoted $R$.  
* 5.3.4 (Addition of reals). Let $x = LIM_{n \rightarrow \infty} a_n$ an and $y = LIM_{n \rightarrow \infty} b_n$ be real numbers. Then we define the sum $x + y$ to be $x + y := LIM_{n \rightarrow \infty} (a_n + b_n)$.  
* 5.3.9 (Multiplication of reals). Let $x = LIM_{n \rightarrow \infty} a_n$ an and $y = LIM_{n \rightarrow \infty} b_n$ be real numbers. Then we define the product $xy$ to be $xy := LIM_{n \rightarrow \infty} a_nb_n$.  
* 5.3.12 (Sequences bounded away from zero). A sequence $(a_n)^\infty_{n = 1}$ of rational numbers is said to be bounded away from zero iff there exists a rational number $c > 0$ such that $|a_n| \ge c$ for all $n \ge 1$.  
* 5.3.16 (Reciprocals of real numbers). Let $x$ be a non-zero real number. Let $(a_n)^\infty_{n = 1}$ be a Cauchy sequence bounded away from zero such that $x = LIM_{n \rightarrow \infty} a_n$ (such a sequence exists by Lemma 5.3.14). Then we define the reciprocal $x^{−1}$ by the formula $x^{-1} = LIM_{n \rightarrow \infty} a^{-1}_n$. (From Lemma 5.3.15 we know that $x^{−1}$ is a real number.)  

### Proposition 5.3.3 (Formal limits are well-defined). Let $x = LIM_{n \rightarrow \infty} a_n, y = LIM_{n \rightarrow \infty} b_n$, and $z = LIM_{n \rightarrow \infty} c_n$ be real numbers. Then, with the above definition of equality for real numbers, we have $x = x$. Also, if $x = y$, then $y = x$. Finally, if $x = y$ and $y = z$, then $x = z$.  

### Lemma 5.3.6 (Sum of Cauchy sequences is Cauchy). Let $x = LIM_{n \rightarrow \infty} a_n$ an and $y = LIM_{n \rightarrow \infty} b_n$ be real numbers. Then $x + y$ is also a real number (i.e., $(a_n + b_n)^\infty_{n = 1}$ is a Cauchy sequence of rationals ).  

### Lemma 5.3.7 (Sums of equivalent Cauchy sequences are equivalent). Let $x = LIM_{n \rightarrow \infty} a_n$ an and $y = LIM_{n \rightarrow \infty} b_n$, and $x^\prime = LIM_{n \rightarrow \infty} a^\prime_n$ be real numbers. Suppose that $x = x^\prime$. Then we have $x + y = x^\prime + y$.  
* Let $x + y = LIM_{n \rightarrow \infty} a_n + b_n = LIM_{n \rightarrow \infty} c_n, x^\prime + y = LIM_{n \rightarrow \infty} a_n^\prime + b_n = LIM_{n \rightarrow \infty} c_n^\prime$. Obviously, $|c_n - c_n^\prime| = |a_n - a_n^\prime|$, then $c_n, c_n^\prime$ are equivalent Cauchy sequences. Thus $x + y = x^\prime + y$.  

### 5.3.10 (Multiplication is well defined). Let $x = LIM_{n \rightarrow \infty} a_n, y = LIM_{n \rightarrow \infty} b_n$, and $x^\prime = LIM_{n \rightarrow \infty} a^\prime_n$ be real numbers. Then $xy$ is also a real number. Furthermore, if $x = x^\prime$, then $xy = x^\prime y$.  
* Let $\epsilon > 0, |a_n| \le q, |b_n| \le p$. For $\epsilon / 2q > 0, \epsilon / 2p > 0$ exists a natural number $M$ such that $\forall n \ge M, m \ge M, |a_n - a_m| \le \epsilon / p, |b_n - b_m| \le \epsilon / q$. Then $|a_nb_n - a_mb_m| = |a_nb_n - a_nb_m + a_nb_m - a_mb_m| = |a_n(b_n - b_m) + b_m(a_n - a_m)| \le |a_n||(b_n - b_m)| + |b_m||(a_n - a_m)| \le |q||(b_n - b_m)| + |p||(a_n - a_m)| \le (q)(\epsilon / 2q) + (p)(\epsilon / 2p) = \epsilon$. Closed.  

### Proposition 5.3.11. All the laws of algebra from Proposition 4.1.6 hold not only for the integers, but for the reals as well.  

### Lemma 5.3.14. Let $x$ be a non-zero real number. Then $x = LIM_{n \rightarrow \infty} a_n$ for some Cauchy sequence $(a_n)^\infty_{n = 1}$ which is bounded away from zero.  
* $x \ne 0 \Rightarrow (a_n)^\infty_{n = 1} \ne (0)^\infty_{n = 1} \Rightarrow \exists \epsilon > 0, \forall N, \exists n \ge N, \ st. \ |a_n - 0| > \epsilon$. And $(a_n)^\infty_{n = 1}$ is a Cauchy sequence, then $\exists N^\prime > 0, \ st. \ n, m \ge N^\prime, |a_n - a_m| \le \epsilon$. If $N \ge N^\prime$ then $\exists n \ st. \ |a_m - a_n| \le \epsilon$ and $|a_n| > \epsilon$ for all $m \ge N$. If $|a_m| = 0$ then $|a_n| \le \epsilon$ and $|a_n| > \epsilon$ will be a contradiction. Thus $|a_m| \ne 0$ for all $m \ge N$.  
* Let $c \ne 0$ and $\begin{matrix} b_n :=\begin{cases}c,&\text{if} ~ n < N \\a_n,&\text{if} ~ n \ge N\end{cases}\end{matrix}$. Obviously $b_n = a_n$, and $b_n$ is bounded away from zero.  

### Lemma 5.3.15. Suppose that $(a_n)^\infty_{n = 1}$ is a Cauchy sequence which is bounded away from zero. Then the sequence $(a_n^{-1})^\infty_{n = 1}$ is also a Cauchy sequence.  
* Obviously, $c \le |a_n| \le m$. Let $\epsilon > 0, c\epsilon > 0$ then $\exists N \ st. \ |a_n - a_m| \le c\epsilon$ for all $n, m \ge N$. Since $|\frac{1}{a_n} - \frac{1}{a_m}| = |\frac{a_n - a_m}{a_na_m}| \le \frac{|a_n - a_m|}{c} \le \epsilon$. Thus $(a_n^{-1})^\infty_{n = 1}$ is also a Cauchy sequence.  

### Lemma 5.3.17 (Reciprocation is well defined). Let $(a_n)^\infty_{n = 1}$ and $(b_n)^\infty_{n = 1}$ be two Cauchy sequences bounded away from zero such that $LIM_{n \rightarrow \infty} a_n = LIM_{n \rightarrow \infty} b_n$ (i.e., the two sequences are equivalent). Then $LIM_{n \rightarrow \infty} a_n^{-1} = LIM_{n \rightarrow \infty} b_n^{-1}$.  
* $LIM_{n \rightarrow \infty} b_n^{-1} = LIM_{n \rightarrow \infty} b_n^{-1} * LIM_{n \rightarrow \infty} a_n * LIM_{n \rightarrow \infty} a_n^{-1} = LIM_{n \rightarrow \infty} b_n^{-1} * LIM_{n \rightarrow \infty} b_n * LIM_{n \rightarrow \infty} a_n^{-1} = LIM_{n \rightarrow \infty} a_n^{-1}$.  

### Exercise  
Exercise 5.3.1. Prove Proposition 5.3.3. (Hint: you may find Proposition 4.3.7 to be useful.)  
Exercise 5.3.2. Prove Proposition 5.3.10. (Hint: again, Proposition 4.3.7 may be useful.)  
Exercise 5.3.3. Let $a, b$ be rational numbers. Show that $a = b$ if and only if $LIM_{n \rightarrow \infty} a = LIM_{n \rightarrow \infty} b$ (i.e., the Cauchy sequences $a, a, a, a, ...$ and $b, b, b, b ...$ equivalent if and only if $a = b$). This allows us to embed the rational numbers inside the real numbers in a well-defined manner.  
* If $LIM_{n\rightarrow \infty}a = LIM_{n\rightarrow \infty}b \rightarrow |a - b| < \epsilon$ for every $\epsilon > 0$. If $a \neq b$, we will find a rational number $\epsilon$ such that $|a - b| = d > ε$, then contradiction.  

Exercise 5.3.4. Let $(a_n)^\infty_{n = 0}$ be a sequence of rational numbers which is bounded. Let $(b_n)^\infty_{n = 0}$ be another sequence of rational numbers which is equivalent to $(a_n)^\infty_{n = 0}$. Show that $(b_n)^\infty_{n = 0}$ is also bounded. (Hint: use Exercise 5.2.2.)  
* Let $\epsilon > 0$, because $a_n = b_n$, them are eventually $\epsilon$-close, and $b_n$ is bounded by Exercise 5.2.2.  

Exercise 5.3.5. Show that $LIM_{n \rightarrow \infty} 1 / n = 0$.  
* Show $a_n = 1 / n$ and $b_n = 0$ are equivalent sequences.  

## 5.4 Ordering the reals  
### Definitions  
* 5.4.1 Let $(a_n)^\infty_{n = 1}$ be a sequence of rationals. We say that this sequence is positively bounded away from zero iff we have a positive rational $c > 0$ such that $a_n \ge c$ for all $n \ge 1$ (in particular, the sequence is entirely positive). The sequence is negatively bounded away from zero iff we have a negative rational $−c < 0$ such that $a_n \le − c$ for all $n \ge 1$ (in particular, the sequence is entirely negative).  
* 5.4.3. A real number $x$ is said to be positive iff it can be written as $x = LIM_{n \rightarrow \infty} a_n$ for some Cauchy sequence $(a_n)^\infty_{n = 1}$ which is positively bounded away from zero. $x$ is said to be negative iff it can be written as $x = LIM_{n \rightarrow \infty} a_n$ for some sequence $(a_n)^\infty_{n = 1}$ which is negatively bounded away from zero.  
* 5.4.5 (Absolute value). Let $x$ be a real number. We define the absolute value $|x|$ of $x$ to equal $x$ if $x$ is positive, $−x$ when $x$ is negative, and $0$ when $x$ is zero.  
* 5.4.6 (Ordering of the real numbers). Let $x$ and $y$ be real numbers. We say that $x$ is greater than $y$, and write $x > y$, if $x − y$ is a positive real number, and $x < y$ iff $x − y$ is a negative real number. We define $x \ge y$ iff $x > y$ or $x = y$, and similarly define $x \le y$.  

### Proposition 5.4.4 (Basic properties of positive reals). For every real number $x$, exactly one of the following three statements is true: (a) $x$ is zero; (b) $x$ is positive; (c) $x$ is negative. A real number $x$ is negative if and only if $−x$ is positive. If $x$ and $y$ are positive, then so are $x + y$ and $xy$.  
* For $0 \in R$, and $x = 0$ or $x \ne 0$ will be true. If $x \ne 0$, we could get $x = LIM_{n \rightarrow \infty} a_n$ which there exists $\epsilon > 0, \forall N , \exists n \ge N \ st. \ |a_n| > \epsilon$ (for $x \ne LIM_{n \rightarrow \infty} 0$). For this $\epsilon$ value, also have $M \in N \ st. \ |a_n - a_m| \le \epsilon$ for every $m \ge M$. Suppose $a_n > 0, a_m < 0$ in there, obviously will lead $|a_{n} - a_{m}| > \epsilon$ and this a contradiction with $|a_n - a_m| \le \epsilon$. Then for all $a_m$ must have the same sign (positive or negative).  
* For $a_n$ is a rational number, it only be one of being positive and negative, then we could get $a_n$ only be one of entirely positive and negative. Closed.  

### Proposition 5.4.7. All the claims in Proposition 4.2.9 which held for rationals, continue to hold for real numbers.  

### Proposition 5.4.8. Let $x$ be a positive real number. Then $x^{−1}$ is also positive. Also, if $y$ is another positive number and $x > y$, then $x^{−1} < y^{−1}$.  

### Proposition 5.4.9 (The non-negative reals are closed). Let $a_0, a_1, a_2, ...$  be a Cauchy sequence of non-negative rational numbers. Then $LIM_{n \rightarrow \infty} a_n$ is a non-negative real number.  

### Corollary 5.4.10. Let $(a_n)^\infty_{n = 1}$ and $(b_n)^\infty_{n = 1}$ be Cauchy sequences of rationals such that $a_n \ge b_n$ for all $n ≥ 1$. Then $LIM_{n \rightarrow \infty} a_n \ge LIM_{n \rightarrow \infty} b_n$.  

### Proposition 5.4.12 (Bounding of reals by rationals). Let $x$ be a positive real number. Then there exists a positive rational number $q$ such that $q \le x$, and there exists a positive integer $N$ such that $x \le N$.  

### Corollary 5.4.13 (Archimedean property). Let $x$ and $\epsilon$ be any positive real numbers. Then there exists a positive integer $M$ such that $M\epsilon > x$.  

### Proposition 5.4.14. Given any two real numbers $x < y$, we can find a rational number $q$ such that $x < q < y$.  
* If $x < y \rightarrow x + d = y$, $d$ is a positive real number, so we have $d > 1/N > 0$ by Exercise 5.4.4. Then $x < x + 1/N < x + d = y \Rightarrow x < \frac{Nx + 1}{N} < x + d$. For $Nx$ is a real number, $n \le Nx < n + 1 \Rightarrow \frac{n}{N} \le x < \frac{n + 1}{N}$, then use $n$ to substitute $Nx$, $x < \frac{Nx + 1}{N} < x + d \Rightarrow x < \frac{n + 1}{N} \le \frac{Nx + 1}{N} < x + d$, the $\frac{n + 1}{N}$ is the rational number we want.  

### Exercise  
Exercise 5.4.1. Prove Proposition 5.4.4. (Hint: if $x$ is not zero, and $x$ is the formal limit of some sequence $(a_n)^\infty_{n = 1}$, then this sequence cannot be eventually $\epsilon$-close to the zero sequence $(0)^\infty_{n = 1}$ for every single $\epsilon > 0$. Use this to show that the sequence $(a_n)^\infty_{n = 1}$ is eventually either positively bounded away from zero or negatively bounded away from zero.)  
Exercise 5.4.2. Prove the remaining claims in Proposition 5.4.7.  
Exercise 5.4.3. Show that for every real number $x$ there is exactly one integer $N$ such that $N \le x < N + 1$. (This integer $N$ is called the integer part of $x$, and is sometimes denoted $N =  \lfloor x \rfloor$.)  
* Suppose $x > 0$, by Proposition 5.4.12, $\exists n + 1 \in N, st.\ x < n + 1$. Let $S = \lbrace n: x < n + 1 \rbrace$ and $n = min(S)$, then $n \le x < n + 1$.  
* Suppose $x > 0$ and there has no natural number such that $N \le x < N + 1 \Rightarrow \forall n \in N, x < n$ and $x < n - 1$. Obviously, if $x < n - 1$ and $n - 1 \in N$, we also has $x < n - 1$ and $x < n - 2$ similarly, thus $(n, n - 1, n - 2,....)$ all the infinite descent natural number sequence is true for this statement, but in Exercise 4.4.2 (a) already prove that infinite descent natural number sequence is false. Contradiction.  

Exercise 5.4.4. Show that for any positive real number $x > 0$ there exists a positive integer $N$ such that $x > 1 / N > 0$.  
* $x > 0 \Rightarrow x^{-1} > 0 \Rightarrow x^{-1} < M + 1 = N \Rightarrow x > N^{-1}$.  

Exercise 5.4.5. Prove Proposition 5.4.14. (Hint: use Exercise 5.4.4. You may also need to argue by contradiction.)  
Exercise 5.4.6. Let $x, y$ be real numbers and let $\epsilon > 0$ be a positive real. Show that $|x − y| < \epsilon$ if and only if $y − \epsilon < x < y + \epsilon$, and that $|x − y| \le \epsilon$ if and only if $y − \epsilon \le x \le y + \epsilon$.  
Exercise 5.4.7. Let $x$ and $y$ be real numbers. Show that $x \le y + \epsilon$ for all real numbers $\epsilon > 0$ if and only if $x \le y$. Show that $|x − y| \le ε$ for all real numbers $\epsilon > 0$ if and only if $x = y$.  
* If $x \le y + ε$, suppose $x > y \Rightarrow x = y + d, d$ is a positive real number, we have $y + d \le y + \epsilon \Rightarrow d \le ε$ for all real numbers $ε > 0$, use Proposition 5.4.12, we could find a rational number $q$ such that $q \le d$. This is a contradiction. The rest is skip.  

Exercise 5.4.8. Let $(a_n)^\infty_{n = 1}$ be a Cauchy sequence of rationals, and let $x$ be a real number. Show that if $a_n \le x$ for all $n \ge 1$, then $LIM_{n \rightarrow \infty} a_n \le x$. Similarly, show that if $a_n \ge x$ for all $n \ge 1$, then $LIM_{n \rightarrow \infty} a_n \ge x$. (Hint: prove by contradiction. Use Proposition 5.4.14 to find a rational between $LIM_{n \rightarrow \infty} a_n$ and $x$, and then use Proposition 5.4.9 or Corollary 5.4.10.)  
* Let $a_n \le x$ for all $n \ge 1$ be the condition. Suppose $LIM_{n\rightarrow\infty}a_n = y$  and $y > x$, then have a rational number $y > q > x$. Let $(b_n)^\infty_{n = 1} = q$ for all $n \ge 1$, then $a_n \le x < b_n \Rightarrow LIM_{n\rightarrow\infty}a_n < LIM_{n\rightarrow\infty}b_n$ by Corollary 5.4.10, but already have $LIM_{n\rightarrow\infty}a_n > LIM_{n\rightarrow\infty}b_n$, contradiction.  

## 5.5 The least upper bound property  
### Definitions  
* 5.5.1 (Upper bound). Let $E$ be a subset of $R$, and let $M$ be a real number. We say that $M$ is an upper bound for $E$, iff we have $x \le M$ for every element $x$ in $E$.  
* 5.5.5 (Least upper bound). Let $E$ be a subset of $R$, and $M$ be a real number. We say that $M$ is a least upper bound for $E$ iff (a) $M$ is an upper bound for $E$, and also (b) any other upper bound $M^\prime$ for $E$ must be larger than or equal to $M$.  
* 5.5.10 (Supremum). Let $E$ be a subset of the real numbers. If $E$ is non-empty and has some upper bound, we define $sup(E)$ to be the least upper bound of $E$ (this is well-defined by Theorem 5.5.9). We introduce two additional symbols, $+\infty$ and $−\infty$. If $E$ is non-empty and has no upper bound, we set $sup(E) := +\infty$; if $E$ is empty, we set $sup(E) := −\infty$. We refer to $sup(E)$ as the supremum of $E$, and also denote it by sup $E$.  

### Proposition 5.5.8 (Uniqueness of least upper bound). Let $E$ be a subset of $R$. Then $E$ can have at most one least upper bound.  
* Suppose $M, M^\prime$ are least upper bounds, according to the definition, we have $M \ge M^\prime$ and $M \le M^\prime$, then $M = M^\prime$.  

### Theorem 5.5.9 (Existence of least upper bound). Let $E$ be a non-empty subset of $R$. If $E$ has an upper bound, (i.e., $E$ has some upper bound $M$), then it must have exactly one least upper bound.  
* Suppose the upper bound of $E$ is $M$.

### Proposition 5.5.12. There exists a positive real number $x$ such that $x^2 = 2$.  

### Exercise  
Exercise 5.5.1. Let $E$ be a subset of the real numbers $R$, and suppose that $E$ has a least upper bound $M$ which is a real number, i.e., $M = sup(E)$. Let $−E$ be the set $−E := \{−x : x \in E\}$. Show that $−M$ is the greatest lower bound of $−E$, i.e., $−M = inf( −E)$.  
* $\forall x \in E, x \le M \Rightarrow -x \ge -M$. Let $x^\prime = -x$, obviously $x^\prime \in -E$ and $x^\prime \ge -M$, then $-M$ is a lower bound of $-E$. Suppose there exists a lower bound $-M^\prime$ of $-E$ such that $-M^\prime > -M$, then we could get $M^\prime < M$ which will lead $M$ is not the least upper bound of $E$. This a contradiction.  

Exercise 5.5.2. Let $E$ be a non-empty subset of $R$, let $n \ge 1$ be an integer, and let $L < K$ be integers. Suppose that $K / n$ is an upper bound for $E$, but that $L/n$ is not an upper bound for $E$. Without using Theorem 5.5.9, show that there exists an integer $L < m \le K$ such that $m / n$ is an upper bound for $E$, but that $(m − 1) / n$ is not an upper bound for $E$. (Hint: prove by contradiction, and use induction. It may also help to draw a picture of the situation.)  
* Suppose $n = 1$ and all the elements in $\{m: L < m \le K  \}$ are upper bounds of $E$ and $(m - 1)$ are also upper bounds of $E$. Obviously, $L + 1$ is in this set but $L$ is not an upper bound of $E$, then a contradiction. Thus when $n = 1$, there exists some elements such that the conclusion of this exercise. Skip the step of hypothesis, we show the conclusion when $n = k++$.  
* Suppose $L / (k++)$ is an not upper bound for $E$, $K / (k++)$ is an upper bound for $E$. Let $E^\prime = kE$, then $L / k$ is an not upper bound for $E^\prime$, $K / k$ is an upper bound for $E^\prime$(Skip the proof of this statement). For $E^\prime$, we have an integer $m(L < m \le K)$ that $m / k$ is an upper bound for $E^\prime$, but that $(m − 1) / k$ is not an upper bound for $E^\prime$. Obviously, $m / (k++)$ is an upper bound for $E$, but $(m - 1) / (k++)$ is not an upper bound(Skip the proof of this statement).  

Exercise 5.5.3. Let $E$ be a non-empty subset of $R$, let $n \ge 1$ be an integer, and let $m, m^\prime$ be integers with the properties that $m / n$ and $m^\prime / n$ are upper bounds for $E$, but $(m − 1) / n$ and $(m^\prime − 1) / n$ are not upper bounds for $E$. Show that $m = m^\prime$. This shows that the integer $m$ constructed in Exercise 5.5.2 is unique. (Hint: again, drawing a picture will be helpful.)  
* Suppose $m \ne m^\prime$, and let $m - 1 < m \le m^\prime - 1 < m^\prime$, then $m / n$ could not be a an upper bound since $m / n \le (m^\prime - 1) / n$, this is a contradiction with $m / n$ is an upper bound for $E$.  

Exercise 5.5.4. Let $q_1, q_2, q_3, ...$  be a sequence of rational numbers with the property that $|q_n − q_{n^\prime}| \le 1 / M$ whenever $M \ge 1$ is an integer and $n, n^\prime \ge M$. Show that $q_1, q_2, q_3, ...$ is a Cauchy sequence. Furthermore, if $S := LIM_{n\rightarrow\infty}q_n$, show that $|q_M − S| \le 1 / M$ for every $M \ge 1$. (Hint: use Exercise 5.4.8.)  
* $\forall \epsilon > 0, \exists m \in N \ st. \ \epsilon < m \Rightarrow 1 / \epsilon < 1 / m \Rightarrow |q_n - q_{n^\prime}| \le 1 / m < 1 / \epsilon$ and $n, n^\prime \ge m$. let $1 / \epsilon = \epsilon^\prime$ and for all $\epsilon^\prime > 0$, we could find a $m \in N$ such that $|q_n − q_{n^\prime}| < \epsilon^\prime$ for all $n, n^\prime \ge m$. Thus $q_n$ is a Cauchy sequence.  
* $|q_n - q_M| \le 1 / M \Rightarrow q_n - 1 / M \le q_M \le q_n + 1 / M$ for all $n \ge M$. Let $\begin{matrix} p_n :=\begin{cases}q_M,&\text{if} ~ n < M \\q_n,&\text{if} ~ n \ge M\end{cases}\end{matrix}$. Obviously $LIM_{n\rightarrow\infty}q_n = LIM_{n\rightarrow\infty}p_n = S$ and $p_n - 1 / M \le q_M \le p_n + 1 / M$ for all $n \ge 1$. Use Exercise 5.4.8, $p_n - 1 / M \le q_M \le p_n + 1 / M \Rightarrow S - 1 / M \le q_M \le S + 1 / M \Rightarrow |q_M − S| \le 1 / M$.  

Exercise 5.5.5. Establish an analogue of Proposition 5.4.14, in which “rational” is replaced by “irrational”.   
* let $d = y - x$, and $\sqrt{2}$ is an irrational number. Obviously, $\sqrt{2} > 1 \Rightarrow d / \sqrt{2} < d \Rightarrow x < x + d / \sqrt{2} < x + d < y$. Show the $x + d / \sqrt{2}$ is irrational. If $x$ is rational, then $x = q / j$ for $q, j$ are integers.

## 5.6 Real exponentiation, Part I  
### Definitions  
* 5.6.1 (Exponentiating a real by a natural number). Let $x$ be a real number. To raise $x$ to the power $0$, we define $x^0 := 1$. Now suppose recursively that $x^n$ has been defined for some natural number $n$, then we define $x^{n + 1} := x^n * x$.  
* 5.6.2 (Exponentiating a real by an integer). Let $x$ be a non-zero real number. Then for any negative integer $-n$, we define $x^{-n} := 1/x^{n}$.  
* 5.6.4 Let $x \ge 0$ be a non-negative real, and let $n \ge 1$ be a positive integer. We define $x^{1 / n}$, also known as the $n^{th}$ root of $x$, by the formula $x^{1 / n} := sup \lbrace y \in R: y \ge 0 \ and \ y^n \le x \rbrace$.  
* 5.6.7. Let $x > 0$ be a positive real number, and let $q$ be a rational number. To define $x^q$, we write $q = a/b$ for some integer $a$ and positive integer $b$, and define $x^q := (x^{1/b})^a$.  

### Proposition 5.6.3. All the properties in Propositions 4.3.10 and 4.3.12 remain valid if $x$ and $y$ are assumed to be real numbers instead of rational numbers.  

### Lemma 5.6.5 (Existence of $n^{th}$ roots). Let $x \ge 0$ be a non-negative real, and let $n \ge 1$ be a positive integer. Then the set $E := \lbrace y \in R : y \ge 0 \ and \ y^n \le x \rbrace$ is non-empty and is also bounded above. In particular, $x^{1/n}$ is a real number.  

### Lemma 5.6.6 Let $x, y \ge 0$ be non-negative reals, and let $n, m \ge 1$ be positive integers.  
(a) If $y = x^{1/n}$, then $y^n = x$.  
(b) Conversely, if $y^n = x$, then $y = x^{1/n}$.  
* Let $d = x^{1/n}$, by (a), we have $d^n = x = y^n \Rightarrow d = y = x^{1/n}$.  

(c) $x^{1/n}$ is a positive real number.  
(d) We have $x > y$ if and only if $x^{1/n} > y^{1/n}$.  
* Suppose $a^n = x, b^n = y$. If $x > y \Rightarrow a^n > b^n \Rightarrow a > b \Rightarrow x^{1/n} > y^{1/n}$.  

(e) If $x > 1$, then $x^{1/k}$ is a decreasing function of $k$. If $x < 1$, then $x^{1/k}$ is an increasing function of $k$. If $x = 1$ , then $x^{1/k} = 1$ for all $k$.  
* Suppose $k, j, d \in N, k = j + d, d > 0, a^j = x, b^k = x$.  
* $x > 1  \Rightarrow a, b > 1$ and $a^ja^d > b^k = x \Rightarrow a^j > b^j \Rightarrow a > b \Rightarrow x^{1/j} > x^{1/k}$. 

(f) We have $(xy)^{1/n} = x^{1/n}y^{1/n}$.  
* Suppose $a = x^{1/n}, b = y^{1/n}$, then $(ab)^n = xy \Rightarrow (xy)^{1/n} = ab = x^{1/n}y^{1/n}$.  

(g) We have $(x^{1/n})^{1/m} = x^{1/nm}$.  
* Suppose $x^{1/nm} = a$, we have $x^{1/nm} = a\Longleftrightarrow a^{nm} = x \Longleftrightarrow (a^n)^m = x \Longleftrightarrow x^{1/m} = a^n \Longleftrightarrow (x^{1/m})^{1/n} = a$, and we have $x^{1/nm} = a$, then $(x^{1/m})^{1/n} = a = x^{1/nm} \Longleftrightarrow (x^{1/m})^{1/n} = x^{1/nm}$.  

### Lemma 5.6.8. Let $a, a^\prime$ be integers and $b, b^\prime$ be positive integers such that $a/b = a^\prime/b^\prime$, and let $x$ be a positive real number. Then we have $(x^{1/b^\prime})^{a^\prime} = (x^{1/b})^a$.  
* $x^{1/ab^\prime} = x^{1/a^\prime b} \Leftrightarrow x^{1/b^\prime} = (x^{1/a^\prime b})^a \Leftrightarrow (x^{1/b^\prime})^{a^\prime} = (x^{1/a^\prime b})^{aa^\prime} \Leftrightarrow (x^{1/b^\prime})^{a^\prime} = (x^{1/b})^a$

### Lemma 5.6.9 Let $x, y > 0$ be positive reals, and let $q, r$ be rationals.  
(a) $x^q$ is a positive real.  
(b) $x^{q+r} = x^qx^r$ and $(x^q)^r = x^{qr}$.  
* Suppose $q = a/b$, $r = c/d$, $x^{q+r} = x^{ad+bc/bd} = (x^{1/bd})^{ad+bc} = (x^{1/bd})^{ad}(x^{1/bd})^{bc} = x^qx^r$.  
* $x^{qr} = x^{ac/bd} = (x^{1/bd})^{ac} = ((x^{1/bd})^a)^c = (x^{a/bd})^c$. Now show $x^{a/bd} = (x^{a/b})^{1/d}$, because $(x^{a/bd})^d = x^{a/b} = ((x^{a/b})^{1/d})^d \Rightarrow x^{a/bd} = (x^{a/b})^{1/d}$. Thus $(x^{a/bd})^c = ((x^{a/b})^{1/d})^c = (x^{a/b})^{c/d} = (x^q)^r$.  

(c) $x^{-q} = 1 /x^q$.  
* Suppose $q = a/b$, $x^{-q} = (x^{1/b})^{-1*a} = ((x^{1/b})^a)^{-1} = 1/((x^{1/b})^a) = 1/x^q$.  

(d) If $q > 0$, then $x > y$ if and only if $x^q > y^q$.  
* Let $q = a/b$. If $x > y$, we have $x^q = (x^{1/b})^a$ and $y^q = (y^{1/b})^a$, then $x^{1/b} > y^{1/b}$ according to Lemma5.6.6 (d), and we have $x^q > y^q$. The rest is skipped.  

(e) If $x > 1$, then $x^q > x^r$ if and only if $q > r$. If $x < 1$, then $x^q > x^r$
if and only if $q < r$.  
* Suppose $x > 1$, $ q = a/b$ and $r = c/d$. If $q > r \Rightarrow q = r + d$ which $d > 0$, we have $x^q - x^r = x^{d+r} - x^r = x^rx^d - x^r = x^r(x^d - 1)$, obviously $x > 1$ and $d > 0$ we have $x^d > 1$, then $x^r(x^d - 1) > 0 \Rightarrow x^q > x^r$. If $x^q > x^r$, suppose $q = r$ or $q < r$. If $q = r \Rightarrow x^q = x^r$,contradiction. If $q < r$, by what we already proved, get $x^q < x^r$, also contradiction.  

### Exercises
Exercise 5.6.1. Prove Lemma 5.6.6. (Hints: review the proof of Proposition 5.5.12. Also, you will find proof by contradiction a useful tool, especially when combined with the trichotomy of order in Proposition 5.4.7 and Proposition 5.4.12. The earlier parts of the lemma can be used to prove later parts of the lemma. With part (e), first show that if $x > 1$ then $x^{1/n} > 1$, and if $x < 1$ then $x^{1/n} < 1$.)  
Exercise 5.6.2. Prove Lemma 5.6.9. (Hint: you should rely mainly on Lemma 5.6.6 and on algebra.)  
Exercise 5.6.3. If $x$ is a real number, show that $|x| = (x^2)^{1/2}$.  
* If $x = 0$, $x^2 = 0 \Rightarrow (x^2)^{1/2} = 0 \Rightarrow (x^2)^{1/2} = x = 0$.  
* If $x > 0, (x^2)^{1/2} = y \Rightarrow x^2 = y^2 \Rightarrow x = y = (x^2)^{1/2}$.  
* If $x < 0$, let $x = -y$ which $y > 0$, $(x^2)^{1/2} = (-y * -y)^{1/2} = (y^2)^{1/2}$, by what we already proved $y > 0 \Rightarrow y = (y^2)^{1/2}$, then $|x| = -x = y = (-y*-y)^{1/2} = (x^2)^{1/2} \Rightarrow |x| = (x^2)^{1/2}.$  