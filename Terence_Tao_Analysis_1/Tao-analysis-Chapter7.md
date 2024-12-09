# Chapter 7 Series  
## 7.1 Finite series  
### Definitions  
* 7.1.1 (Finite series). Let $m, n$ be integers, and let $(a_i)_{i=m}^n$ be a finite sequence of real numbers, assigning a real number ai to each integer $i$ between $m$ and $n$ inclusive (i.e., $m \le i \le n$). Then we define the finite sum (or finite series) $ \sum_{i=m}^i a_i$ by the recursive formula $\sum_{i=m}^n a_i := 0$ whenever $n < m$; $\sum_{i=m}^{n + 1} a_i := (\sum_{i=m}^n + a_{n + 1})$ whenever $n \ge m − 1$.  
* 7.1.6 (Summations over finite sets). Let $X$ be a finite set with $n$ elements (where $n \in N$), and let $f : X \rightarrow R$ be a function from $X$ to the real numbers (i.e., $f$ assigns a real number $f(x)$ to each element $x$ of $X$). Then we can define the finite sum $\sum_{x \in X} f(x)$ as follows. We first select any bijection $g$ from $\lbrace i \in N : 1 \le i \le n \rbrace$ to $X$; such a bijection exists since $X$ is assumed to have $n$ elements. We then define $\sum_{x \in X} f(x) := \sum_{i = 1}^n f(g(i))$.  

### Lemma 7.1.4  
(a) Let $m \le n < p$ be integers, and let $a_i$ be a real number assigned to each integer $m \le i \le p$. Then we have $\sum_{i=m}^n a_i + \sum_{i=n+1}^p a_i = \sum_{i=m}^p a_i$.  
* Use induction by $p - m = N$.  

(b) Let $m \le n$ be integers, $k$ be another integer, and let $a_i$ be a real number assigned to each integer $m \le i \le n$. Then we have $\sum_{i=m}^n a_i = \sum_{j=m+k}^{n+k} a_{j - k}$.  

(c) Let $m \le n$ be integers, and let $a_i, b_i$ be real numbers assigned to each integer $m \le i \le n$. Then we have $\sum_{i=m}^n (a_i + b_i) = \sum_{i=m}^n a_i + \sum_{i=m}^n  b_i$.  

(d) Let $m \le n$ be integers, and let $a_i$ be a real number assigned to each integer $m \le i \le n$, and let $c$ be another real number. Then we have $\sum_{i=m}^n (ca_i) = c(\sum_{i=m}^n a_i)$.  

(e) (Triangle inequality for finite series) Let $m \le n$ be integers, and let $a_i$ be a real number assigned to each integer $m \le i \le n$. Then we have $|\sum_{i=m}^n a_i| \le \sum_{i=m}^n |a_i|$.  

(f ) (Comparison test for finite series) Let $m \le n$ be integers, and let $a_i, b_i$ be real numbers assigned to each integer $m \le i \le n$. Suppose that $a_i \le b_i$ for all $m \le i \le n$. Then we have $\sum_{i=m}^n a_i \le \sum_{i=m}^n b_i$.  

### Proposition 7.1.8 (Finite summations are well-defined). Let $X$ be a finite set with n elements (where $n \in N$), let $f : X \rightarrow R$ be a function, and let $g : \lbrace i \in N : 1 \le i \le n \rbrace \rightarrow X$ and $h : \lbrace i \in N : 1 \le i \le n \rbrace \rightarrow X$ be bijections. Then we have $\sum_{i = 1}^n f(g(i)) = \sum_{i = 1}^n f(h(i))$.  

### Proposition 7.1.11 (Basic properties of summation over finite sets)
(a) If $X$ is empty, and $f : X \rightarrow R$ is a function (i.e., $f$ is the empty function), we have $\sum_{x \in X} f(x) = 0$.  

(b) If $X$ consists of a single element, $X = \lbrace x_0 \rbrace$, and $f : X \rightarrow R$ is a function, we have $\sum_{x \in X} f(x) = f(x_0)$.  

(c) ( Substitution, part I ) If $X$ is a finite set, $f : X \rightarrow R$ is a function, and $g : Y \rightarrow X$ is a bijection, then $\sum_{x \in X} f(x) = \sum_{y \in Y} f(g(y))$.  

(d) ( Substitution, part II ) Let $n \le m$ be integers, and let $X$ be the set $X := \lbrace i \in Z : n \le i \le m \rbrace$. If $a_i$ is a real number assigned to each integer $i \in X$, then we have $\sum_{i = n}^m f(x) = \sum_{i \in X} a_i$.  

(e) Let $X, Y$ be disjoint finite sets (so $X \cap Y = \empty$), and $f : X \cup Y \rightarrow R$ is a function. Then we have $\sum_{z \in X \cup Y} f(z) = (\sum_{x \in X} f(x)) + (\sum_{y \in Y} f(y))$.  

(f) ( Linearity, part I ) Let $X$ be a finite set, and let $f : X \rightarrow R$ and $g : X \rightarrow R$ be functions. Then $\sum_{x \in X} (f(x) + g(x)) = \sum_{x \in X} f(x) + \sum_{x \in X} g(x)$.  

(g) ( Linearity, part II ) Let $X$ be a finite set, let $f : X \rightarrow R$ be a function, and let $c$ be a real number. Then $\sum_{x \in X} cf(x) = c\sum_{x \in X} f(x)$.  

(h) ( Monotonicity) Let $X$ be a finite set, and let $f : X \rightarrow R$ and $g : X \rightarrow R$ be functions such that $f(x) \le g(x)$ for all $x \in X$. Then we have $\sum_{x \in X} f(x) \le \sum_{x \in X} g(x)$.  

(i) ( Triangle inequality) Let $X$ be a finite set, and let $f : X \rightarrow R$ be a function, then $|\sum_{x \in X} f(x)| \le \sum_{x \in X} |f(x)|$.  

### Lemma 7.1.13. Let $X, Y$ be finite sets, and let $f : X * Y \rightarrow R$ be a function. Then $\sum_{x \in X} (\sum_{y \in Y} f(x,y)) = \sum_{(x, y) \in X * Y} f(x, y)$.  

### Corollary 7.1.14 (Fubini’s theorem for finite series). Let $X, Y$ be finite sets, and let $f : X * Y \rightarrow R$ be a function. Then $\sum_{x \in X} (\sum_{y \in Y} f(x,y)) = \sum_{(x, y) \in X * Y} f(x, y) = \sum_{(y, x) \in Y * X} f(x, y) = \sum_{y \in Y} (\sum_{x \in X} f(x,y))$.  

### Exercises  
Exercise 7.1.1. Prove Lemma 7.1.4. (Hint: you will need to use induction, but the base case might not necessarily be at $0$.)  

Exercise 7.1.2. Prove Proposition 7.1.11. (Hint: this is not as lengthy as it may first appear. It is largely a matter of choosing the right bijections to turn these sums over sets into finite series, and then applying Lemma 7.1.4.)  

Exercise 7.1.3. Form a definition for the finite products $\prod_{i=1}^n a_i$ and $\prod_{x \in X} f(x)$. Which of the above results for finite series have analogues for finite products? (Note that it is dangerous to apply logarithms because some of the $a_i$ or $f(x)$ could be zero or negative. Besides, we haven’t defined logarithms yet.)  
* $ \prod_{i=1}^n a_i$ by the recursive formula $\prod_{i=1}^n a_i := 1$ whenever $n < i$; $\prod_{i=1}^{n + 1} a_i := (\prod_{i=1}^{n} a_i * a_{n + 1})$ whenever $n \ge m − 1$.  

Exercise 7.1.4. Define the factorial function $n!$ for natural numbers $n$ by the recursive definition $0! := 1$ and $(n + 1)! := n! * (n + 1)$. If $x$ and $y$ are real numbers, prove the binomial formula $(x + y)^n = \sum_{j = 0}^n \frac{n!}{j!(n - j)!}x^jy^{n - j}$ for all natural numbers $n$. (Hint: induct on $n$.)  

Exercise 7.1.5. Let $X$ be a finite set, let $m$ be an integer, and for each $x \in X$, let $(a_n(x))_{n=m}^\infty$ be a convergent sequence of real numbers. Show that the sequence $(\sum_{x \in X} a_n(x))_{n=m}^\infty$ is convergent, and $\lim_{n \rightarrow \infty} \sum_{x \in X} a_n(x) = \sum_{x \in X} \lim_{n \rightarrow \infty} a_n(x)$. (Hint: induct on the cardinality of $X$, and use Theorem 6.1.19(a).) Thus we may always interchange finite sums with convergent limits. Things however get trickier with infinite sums; see Exercise 11.47.11.  

## 7.2 Infinite series  
### Definitions  
* 7.2.1 (Formal infinite series). A (formal) infinite series is any expression of the form $\sum_{n = m}^\infty a_n$ where $m$ is an integer, and $a_n$ is a real number for any integer $n \ge m$. We sometimes write this series as $a_m + a_{m+1} + a_{m+2} + ...$.  
* 7.2.2 (Convergence of series). Let $\sum_{n = m}^\infty a_n$ be a formal infinite series. For any integer $N \ge m$, we define the $N$th partial sum $S_N$ of this series to be $S_N := \sum_{n=m}^N a_n$; of course, $S_N$ is a real number. If the sequence $(S_N)_{N=m}^\infty$ converges to some limit $L$ as $N \rightarrow \infty$ , then we say that the infinite series $\sum_{n = m}^\infty a_n$ is convergent, and converges to $L$; we also write $L = \sum_{n = m}^\infty a_n$, and say that $L$ is the sum of the infinite series $\sum_{n = m}^\infty a_n$. If the partial sums $S_N$ diverge, then we say that the infinite series $\sum_{n = m}^\infty a_n$ is divergent, and we do not assign any real number value to that series.  
* 7.2.8 (Absolute convergence). Let $\sum_{n = m}^\infty a_n$ an be a formal series of real numbers. We say that this series is absolutely convergent iff the series $\sum_{n = m}^\infty |a_n|$ is convergent. In order to distinguish convergence from absolute convergence, we sometimes refer to the former as conditional convergence.  

### Proposition 7.2.5. Let $\sum_{n = m}^\infty a_n$ be a formal series of real numbers. Then $\sum_{n = m}^\infty a_n$ converges if and only if, for every real number $\epsilon > 0$, there exists an integer $N \ge m$ such that $|\sum_{n = p}^q a_n| \le \epsilon$ for all $p, q \ge N$.  
* $S_N$ is also a Cauchy sequence, then for all $\epsilon >0, \exists N \ st. \ |S_p - S_q| < \epsilon$ for all $p, q \ge N$. And $S_p - S_q = \sum_{n = m}^p a_n - \sum_{n = m}^q a_n = \sum_{n = p}^q a_n$, which we want to prove.  
* If $S_N$ is not convergent, then $\exist \epsilon > 0, \forall N, \exist p, q \ge N \ st. \ |S_p - S_q| > \epsilon$ which lead a contradiction.  
* Seemly, the Proposition 6.1.12 is enough to prove this prosition.  

### Corollary 7.2.6 (Zero test). Let $\sum_{n = m}^\infty a_n$ be a convergent series of real numbers. Then we must have $\lim_{n \rightarrow \infty} a_n = 0$. To put this another way, if $\lim_{n \rightarrow \infty} a_n$ is non-zero or divergent, then the series $\sum_{n = m}^\infty a_n$ is divergent.  
* For all $\epsilon > 0, \exist N \ st. \ |\sum_{n = p}^q a_n| \le \epsilon$ for all $p, q \ge N$. Let $q = p, |\sum_{n = p}^q a_n| = |a_p| \le \epsilon$ for all $p \ge N$. Thus $\lim_{n \rightarrow \infty} a_n = 0$.  
* Suppose $\sum_{n = m}^\infty a_n$ is convergent, which will lead to $\lim_{n \rightarrow \infty} a_n = 0$, which is a contradiction with $\lim_{n \rightarrow \infty} a_n$ is non-zero or divergent.  

### Proposition 7.2.9 (Absolute convergence test). Let $\sum_{n = m}^\infty a_n$ be a formal series of real numbers. If this series is absolutely convergent, then it is also conditionally convergent. Furthermore, in this case we have the triangle inequality $|\sum_{n = m}^\infty a_n| \le \sum_{n = m}^\infty |a_n|$.  
* First to prove $|\sum_{n = m}^N a_n| \le \sum_{n = m}^N |a_n|$ by induction on $p$ of $N = m + p$ and (e) of Proposition 7.1.4.  
* If $\sum_{n = m}^\infty |a_n|$ is convergent, by Proposition 7.2.5 $|\sum_{n = p}^q |a_n|| \le \epsilon$ for all $p, q \ge N$ and $|\sum_{n = p}^q a_n| \le \sum_{n = p}^q |a_n|  = |\sum_{n = p}^q |a_n|| \le \epsilon$, then by Proposition 7.2.5 again, the $\sum_{n = m}^\infty a_n$ is convergent as desired.  

### Proposition 7.2.12 (Alternating series test). Let $(a_n)_{n=m}^\infty$ be a sequence of real numbers which are non-negative and decreasing, thus $a_n \ge 0$ and $a_n \ge a_{n+1}$ for every $n \ge m$. Then the series $\sum_{n = m}^\infty (-1)^na_n$ is convergent if and only if the sequence $a_n$ converges to $0$ as $n \rightarrow \infty$.  

### Proposition 7.2.14 (Series laws).  
(a) If $\sum_{n = m}^\infty a_n$ is a series of real numbers converging to $x$, and $\sum_{n = m}^\infty b_n$ is a series of real numbers converging to $y$, then $\sum_{n = m}^\infty (a_n + b_n)$ is also a convergent series, and converges to $x+y$. In particular, we have $\sum_{n = m}^\infty (a_n + b_n) = \sum_{n = m}^\infty a_n + \sum_{n = m}^\infty b_n$.  

(b) If $\sum_{n = m}^\infty a_n$ is a series of real numbers converging to $x$, and $c$ is a real number, then $\sum_{n = m}^\infty ca_n$ is also a convergent series, and converges to $cx$. In particular, we have $\sum_{n = m}^\infty ca_n = c\sum_{n = m}^\infty a_n$.  

(c) Let $\sum_{n = m}^\infty a_n$ be a series of real numbers, and let $k \ge 0$ be an integer. If one of the two series $\sum_{n = m}^\infty a_n$ and $\sum_{n = m + k}^\infty a_n$ are convergent, then the other one is also, and we have the identity $\sum_{n = m}^\infty a_n = \sum_{n = m}^{m + k - 1} a_n + \sum_{n = m + k}^\infty a_n$.  
* Use Proposition 7.2.5 to prove $\sum_{n = m}^\infty a_n$ is convergent iff $\sum_{n = m + k}^\infty a_n$ is convergent.  
* $(S_N)_{N = m + k}^\infty + \sum_{n = m}^{m + k - 1} a_n = (S_N)_{N = m}^\infty$ for every $N$. Thus $\sum_{n = m}^\infty a_n = \sum_{n = m}^{m + k - 1} a_n + \sum_{n = m + k}^\infty a_n$.  

(d) Let $\sum_{n = m}^\infty a_n$ be a series of real numbers converging to $x$, and let  $k$ be an integer. Then $\sum_{n = m + k}^\infty a_{n - k}$ also converges to $x$.  

### Lemma 7.2.15 (Telescoping series). Let $(a_n)_{n=0}^\infty$ be a sequence of real numbers which converge to $0$, i.e., $\lim_{n \rightarrow \infty} a_n = 0$. Then the series $\sum_{n = 0}^\infty (a_n - a_{n + 1})$ converges to $a_0$.  
* Note that $\lim_{n \rightarrow \infty} a_n = 0$ does not certainly make $\sum_{n = 0}^\infty a_n$ convergent.  
* $\sum_{n = 0}^\infty (a_n - a_{n + 1}) = \lim_{n \rightarrow \infty} a_0 - a_{n + 1} =  a_0 - 0 = a_0$.  

### Exercises  
Exercise 7.2.1. Is the series $\sum_{n = 1}^\infty (-1)^n$ convergent or divergent? Justify your answer. Can you now resolve the difficulty in Example 1.2.2?  
* $\sum_{n = 1}^\infty (-1)^n$ is divergent. If $\sum_{n = 1}^\infty (-1)^n$ is convergent, then $\lim_{n \rightarrow \infty} a_n = 0$, but it's not true then $\sum_{n = 1}^\infty (-1)^n$ is divergent.  

Exercise 7.2.2. Prove Proposition 7.2.5. (Hint: use Proposition 6.1.12 and Theorem 6.4.18.)  
Exercise 7.2.3. Use Proposition 7.2.5 to prove Corollary 7.2.6.  
Exercise 7.2.4. Prove Proposition 7.2.9. (Hint: use Proposition 7.2.5 and Proposition 7.1.4(e).)  
Exercise 7.2.5. Prove Proposition 7.2.14. (Hint: use Theorem 6.1.19.)  
Exercise 7.2.6. Prove Lemma 7.2.15. (Hint: First work out what the partial sums $\sum_{n = 0}^N (a_n - a_{n + 1})$ should be, and prove your assertion using induction.) How does the proposition change if we assume that an does not converge to zero, but instead converges to some other real number $L$?  
* If $a_n$ converges to $L$, the partial sum is $a_0 - L$.  

## 7.3 Sums of non-negative numbers  
### Proposition 7.3.1. Let $\sum_{n = m}^\infty a_{n}$ an be a formal series of non-negative real numbers. Then this series is convergent if and only if there is a real number $M$ such that $\sum_{n = 1}^N a_{n} \le M$ for all integers $N \ge M$.  

### Corollary 7.3.2 (Comparison test). Let $\sum_{n = m}^\infty a_{n}$ and $\sum_{n = m}^\infty b_{n}$ be two formal series of real numbers, and suppose that $|a_n| \le b_n$ for all $n \ge m$. Then if $\sum_{n = m}^\infty b_{n}$ is convergent, then $\sum_{n = m}^\infty a_{n}$ is absolutely convergent, and in fact $|\sum_{n = m}^\infty a_{n}| \le \sum_{n = m}^\infty |a_{n}| \le \sum_{n = m}^\infty b_{n}$.  
* If $\sum_{n = m}^\infty b_{n}$ is convergent, $\sum_{n = m}^\infty |a_{n}|$ is also convergent by Proposition 7.2.5.  
* Prove $\sum_{n = m}^N |a_n| \le \sum_{n = m}^N b_n$ by induction on $p$ of $N = m + p$.  
* Use Proposition 7.2.9 we could get $|\sum_{n = m}^\infty a_{n}| \le \sum_{n = m}^\infty |a_{n}| \le \sum_{n = m}^\infty b_{n}$.  

### Lemma 7.3.3 (Geometric series). Let $x$ be a real number. If $|x| \ge 1$, then the series $\sum_{n = 0}^\infty x^{n}$ is divergent. If however $|x| < 1$, then the series is absolutely convergent and $\sum_{n = 0}^\infty x^{n} = 1 / (1 - x)$.  
* If $|x| \ge 1$, then $x^n$ is divergent or convergent to $1$. Thus $\sum_{n = 0}^\infty x^{n}$ is divergent by zero test.  

### Proposition 7.3.4 (Cauchy criterion). Let $(a_n)_{n=1}^\infty$ be a decreasing sequence of non-negative real numbers (so $a_n \ge 0$ and $a_{n+1} \le a_n$ for all $n \ge 1$). Then the series $\sum_{n = 1}^\infty a_{n}$ is convergent if and only if the series $\sum_{k = 0}^\infty 2^{k}a_{2^k} = a_1 + 2a_2 + 4a_4 + 8a_8 + ...$ is convergent.  

### Lemma 7.3.6. Let $S_N := \sum_{n = 1}^N a_{n}$ and $T_K := \sum_{k = 0}^K 2^{k}a_{2^k}$ in Proposition 7.3.4. For any natural number $K$, we have $S_{2^{K+1}−1} ≤ T_K ≤ 2S_{2^K}$.  

### Corollary 7.3.7. Let $q > 0$ be a rational number. Then the series $\sum_{n = 1}^\infty 1 / n^q$ is convergent when $q > 1$ and divergent when $q \le 1$.  

### Exercises  
Exercise 7.3.1. Use Proposition 7.3.1 to prove Corollary 7.3.2  
Exercise 7.3.2. Prove Lemma 7.3.3. (Hint: for the first part, use the zero test. For the second part, first use induction to establish the geometric series formula $\sum_{n = 0}^\infty x^{n} = (1 - x^{N + 1})/(1 - x)$ and then apply Lemma 6.5.2.)  
Exercise 7.3.3. $\sum_{n = 0}^\infty a_{n}$ be an absolutely convergent series of real numbers such that $\sum_{n = 0}^\infty |a_{n}| = 0$. Show that $a_n = 0$ for every natural number $n$.  
* Suppose there exist a $m$ such that $a_m \ne 0$, thus $|a_m| > 0$. Use (c) of 7.2.14, $\sum_{n = 0}^\infty |a_{n}| = \sum_{n = 0}^m |a_{n}| + \sum_{n = m + 1}^\infty |a_{n}|$. Since $\sum_{n = 0}^m |a_{n}| > 0$ and $\sum_{n = m + 1}^\infty |a_{n}| \ge 0 \Rightarrow \sum_{n = 0}^\infty |a_{n}| > 0$ which is a contradiction.  

## 7.4 Rearrangement of series  
### Proposition 7.4.1. Let $\sum_{n = 0}^\infty a_{n}$ be a convergent series of non-negative real numbers, and let $f : N \rightarrow N$ be a bijection. Then $\sum_{m = 0}^\infty a_{f(m)}$ is also convergent, and has the same sum: $\sum_{n = 0}^\infty a_{n} = \sum_{m = 0}^\infty a_{f(m)}$.  

### Proposition 7.4.3 (Rearrangement of series). Let $\sum_{n = 0}^\infty a_{n}$ be an absolutely convergent series of real numbers, and let $f : N \rightarrow N$ be a bijection. Then $\sum_{m = 0}^\infty a_{f(m)}$ is also absolutely convergent, and has the same sum: $\sum_{n = 0}^\infty a_{n} = \sum_{m = 0}^\infty a_{f(m)}$.  

### Exercises  
Exercise 7.4.1. Let $\sum_{n = 0}^\infty a_{n}$ be an absolutely convergent series of real numbers. Let $f : N \rightarrow N$ be an increasing function (i.e., $f(n + 1) > f (n)$ for all $n \in N$). Show that $\sum_{n = 0}^\infty a_{f(n)}$ is also an absolutely convergent series. (Hint: try to compare each partial sum of $\sum_{n = 0}^\infty a_{f(n)}$ with a (slightly different) partial sum of $\sum_{n = 0}^\infty a_{n}$.).  
* If $f : N \rightarrow N$ be an increasing function, then $f(n) \ge n$. Use Proposition 7.2.5 for every real number $\epsilon > 0$, there exists an integer $N \ge 0$ such that $|\sum_{n = p}^q |a_n|| \le \epsilon$ for all $p, q \ge N$. And obviously $\sum_{n = f(p)}^{f(q)} |a_n| \le \epsilon$. Consider $\lbrace f(n): p \le n \le q \rbrace \subseteq \lbrace f(p) \le m \le f(q) \rbrace$, thus $\sum_{n = p}^q |a_{f(n)}| = \sum_{n \in \lbrace f(n): p \le n \le q \rbrace} |a_n| \le \sum_{n = f(p)}^{f(q)} |a_n| \le \epsilon$. And use Proposition 7.2.5 again, we conclude that $\sum_{n = 0}^\infty a_{f(n)}$ is also an absolutely convergent series.  

## 7.5 The root and ratio tests  
### Theorem 7.5.1 (Root test). Let $\sum_{n = m}^\infty a_{n}$ be a series of real numbers, and let $\alpha := \lim sup_{n \rightarrow \infty} |a_n|^{1/n}$.  
(a) If $\alpha < 1$, then the series $\sum_{n = m}^\infty a_{n}$ is absolutely convergent (and hence conditionally convergent).  
(b) If $\alpha > 1$, then the series $\sum_{n = m}^\infty a_{n}$ is not conditionally convergent.(and hence cannot be absolutely convergent either).  
(c) If $\alpha = 1$, we can not assert any conclusion.  

Lemma 7.5.2. Let $(c_n)_{n=m}^\infty$ be a sequence of positive numbers. Then we have $\lim inf_{n \rightarrow \infty} \frac{c_{n + 1}}{c_n} \le \lim inf_{n \rightarrow \infty} c_n^{1/n} \le \lim sup_{n \rightarrow \infty} c_n^{1/n} \le \lim sup_{n \rightarrow \infty} \frac{c_{n + 1}}{c_n}$.  
