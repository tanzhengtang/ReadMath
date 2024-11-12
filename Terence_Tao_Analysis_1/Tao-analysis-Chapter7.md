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
* Skip the preconditions. $(x + y)^{n + 1} = (x + y)^n(x + y) = \sum_{j = 0}^n \frac{n!}{j!(n - j)!}x^jy^{n - j} * (x + y) = \sum_{j = 0}^n \frac{n!}{j!(n - j)!}x^jy^{n - j} * x + \sum_{j = 0}^n \frac{n!}{j!(n - j)!}x^jy^{n - j} * y = $  
* $\sum_{j = n + 1}^{n + 1} \frac{n!}{j!(n - j)!}x^jy^{n - j} = x^{n + 1} $

Exercise 7.1.5. Let $X$ be a finite set, let $m$ be an integer, and for each $x \in X$, let $(a_n(x))_{n=m}^\infty$ be a convergent sequence of real numbers. Show that the sequence $(\sum_{x \in X} a_n(x))_{n=m}^\infty$ is convergent, and $\lim_{n \rightarrow \infty} \sum_{x \in X} a_n(x) = \sum_{x \in X} \lim_{n \rightarrow \infty} a_n(x)$. (Hint: induct on the cardinality of X, and use Theorem 6.1.19(a).) Thus we may always interchange finite sums with convergent limits. Things however get trickier with infinite sums; see Exercise 11.47.11.  