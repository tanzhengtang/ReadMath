---
title: Terecent Tao Analysis I Chapter4 & Exercise
date: 2023-7
mathjax: true
categories: 
- Math
tags: 
- Math
---
# Chapter 4  
* Just to record my own thought and answer,if there has any error,please leave a message in the comment area. 
## 4.1 The integers
### Lemma 4.1.5 (Trichotomy of integers). Let x be an integer. Then exactly one of the following three statements is true: (a) x is zero; (b) x is equal to a positive natural number n; or (c) x is the negation − n of a positive natural number n.  
* First, it's easy to prove (a), (b) and (c) is at least one true, consider x is consist of some natural number a and b, a and b have three relationship: $a = b, a \le b, b \le a$. Second, obviously when (a) is true, it has contradiction with other two statements, as well as each other.  

### Proposition 4.1.8 (Integers have no zero divisors). Let a and b be integers such that ab=0. Then either a=0 or b=0 (or both).  
* If $a \neq 0, b \neq 0$, then it's easy to prove $ab \neq 0$. So proposition 4.1.8 is true.  

### Corollary 4.1.9 (Cancellation law for integers). If a, b, c are integers such that ac = bc and c is non-zero, then a = b.  
* If $ac = bc$, because ab,bc are integers,then $ac - bc = bc - bc \rightarrow ac - bc = 0$. c is non-zero, $ac - bc = 0 \rightarrow c(a - b) = 0$, use Proposition 4.1.8 we have $a - b = 0 \rightarrow a = b$.  

### Exercise
* 4.1.1 $a - b = a - b \rightarrow a + b = a + b$(reflexive). If $a - b = c - d$, then $a + d = c + b \rightarrow a + d + c + b = c + b + a + d \rightarrow c + b = a + d \rightarrow c - d = a - b$(symmetric).  
* 4.1.2 If $a - b = a^o - b^o$, $a - b = a^o - b^o \rightarrow b^o + a = b + a^o \rightarrow b - a = b^o - a^o \rightarrow -(a - b) = -(a^o - b^o)$.  
* 4.1.3 $(-1) * a + 1 * a = a(1 + (-1)) = a * 0 = 0$, then $(-1)*a = -a$  
* 4.1.4 let x = a - b, y = c - d, z = e - f.  
(a) $x + y = (a - b) + (c - d) = (a + c) - (b + d) = (c + a) - (d + b) = (c - d) + (a - b) = y + x$  
(b) $(x + y) + z = ((a + c) - (b + d)) + (e - f) = (a + c + e) - (b + d + f)$, $x + (y + z) = (a - c) + ((b + e) - (d + f)) = (a + c + e) - (b + d + f) = (x + y) + z$.  
(c) According to (b), it's easy to know that $0 + x = x + 0$. $0 + x = (0 - 0) + (a - b) = (0 + a) - (0 + b) = a - b = x$.  
(d) $(a - b) + (- (a - b)) = (a - b) + (b - a) = (a + b) - (a + b) = 0 - 0 = 0$  
(e) $xy = (a - b)(c - d) = (ac + bd) − (ad + bc) = (bd + ac) - (bc + ad) = (c - d)(a - b) = yx$.  
(f) $(xy)z=xyz=x(yz)$.  
(g) $1x = (1 - 0)(a - b) = (1a - 0) - (0 + 1b) = a - b$.  
(h) $x(y + z) = (a - b)((c + e) - (d + f)) = (a(c + e) + b(d + f)) - (a(d + f) - b(c + e)) = xy + xz$.  
(i) $(y + z)x = x(y + z) = xy + xz = yx + zx$.  

* 4.1.5 See previous.  
* 4.1.6 See previous.  
* 4.1.7 (a) if a > b, then a = b + m, m is a positive natural number. Then $a - b = b + m - b \rightarrow a - b = m$, m is positive, a - b is also positvie.  
(b) if a > b, then a = b + m, then a + c = b + c + m, then a + c > b + c.  
(c) if a > b and c is positive, $a = b + m \rightarrow c*a = (b + m) * c \rightarrow ac = bc + cm \rightarrow ac > bc$.  
(d) if a > b, $a = b + m \rightarrow -a = (-b) + (-m) \rightarrow -a + m = (-b) + (-m) + m \rightarrow -a + m = -b \rightarrow -a < -b$.  
(e) if a > b and b > c, $a = b + m, b = c + n \rightarrow a = c + n + m$, let n + m = d, then $a = c + d \rightarrow a > c$.  
(f) like lemma 4.1.5, for any integer a,b, we could know that at least one of a > b, a < b, and a = b is true. It's obvious that if one of them is true, then other two statment are false.  

* 4.1.8 No idea.  

## 4.1 The rationals  
### Lemma 4.2.3. The sum, product, and negation operations on rational numbers are well-defined, in the sense that if one replaces a//b with another rational number a′//b′ which is equal to a//b, then the output of the above operations remains unchanged, and similarly for c//d.  
* Skip.  

### Exercise  
* 4.2.1 Skip.  
* 4.2.2 Skip.  
* 4.2.3 Skip.  
* 4.2.4 Skip.  
* 4.2.5 Skip.  
* 4.2.6 if x < y, z is negative, and -z is positive. Then $(-z)*x < (-z)*y \rightarrow (-z) * y - (-z) * x = d  > 0 \rightarrow z * y - z * x = - d$, -d is negative, so $xz > yz$.  

## 4.3 Absolute value and exponentiation  
### Exercise  
* 4.3.1 (a) If $|X| = 0$, 0 is not positive and negative, then x is must be 0.  
(b) Skip.  
(c) Skip.  
(d) Skip.  
(e) Skip.  
(f) Skip.  
(g) $d(x,z) = |x - z| = |(x - y) + (y - z)|$, use (b), get $|(x - y) + (y - z)| \le |(x - y)| + |(y - z)| = d(x,y) + d(y,z)$.  

* 4.3.2 (a) If x is ε-close to y for every ε > 0, means that $d(x,y) \le ε$. If $x \neq y$, we could find a number d such that $d(x,y) = d > 0$, but for every ε > 0 we could still find a number ε < d, which means a contradiction, then x = y.  
(b) $d(x,y) = d(y,x) \le ε$.  
(c) $d(x,z) = |x - z| = |x - y + y - z| \le |x - y| + |y - z| \le ε + δ$.  
(d) Like (c), skip.  
(e) Skip.  
(f) $z \le w \le y\rightarrow z - x \le w - x \le y - x$, and $|y - x| \le ε, |z - x| \le ε \rightarrow -ε \le y - x \le ε, -ε \le z - x \le ε$, then $-ε \le z - x \le w - x \le y - x \le ε \rightarrow -ε \le w - x \le ε \rightarrow |w - x| \le ε$.  
(g) $|y - x| \le ε \rightarrow |z||y - x| \le |z|ε \rightarrow |zy - zx| \le |z|ε$.  
(h) No idea.  

* 4.3.3 (a) Skip.  
(b) If $x^n = 0$, $x^{n - 1}*x = 0$, $x = 0 \ or\  x^{n - 1} = 0$, induction on n - 1, still get x = 0. If x = 0, obviously $x^n = 0$.  
(c) If $x \ge 0$, $x * x \ge 0$, then $x^n \ge 0$. If $x \ge y$, $x*y \ge y *y$ and $x*x \ge x*y \rightarrow x*x \ge x*y \ge y*y$, thus $x^n \ge y^n$. Thus $x^n \ge y^n \ge 0$.  
(d) If x = 0, obviously $|x^n| = |x|^n = 0$. If $x \neq 0$, $|x|^{n+1} = |x|^n|x| = |x^n||x| = |x^nx| = |x^{n+1}|$.  

* 4.3.4 (a) If $n < 0 ,m > 0$, we could get $d = |n| = -n$ and $x^n = 1/x^d$, $x^nx^m=1/x^d * x^m$, if $m \ge d$ which means $m = d + s$, $1/x^d * x^m = 1/x^d * x^d * x^s = x^s$, $s = m - d = m + n$, then $x^s = x^{m + n}$. If $m < d$, same result.  The rest is skipped.  
(b) If $x \ge y$, it's easy to prove $1/x \le 1/y$. The rest is skipped.  
(c) 
(d) If n = 0, $|x^n| = 1 = |x|^n$. If n < 0, let m > 0 and m = -n, $|x|^n = (1/|x|)^m = |1|/|x|^m = |1/x|^m = |(1/x)^m = |x^n||$.  

* 4.3.5 If N = 0, $2^N = 1 \ge N = 0$.  Show N++(N > 0) is true. $2^{N++} = 2^N* 2 \ge N * 2 = N + N \ge N + 1 \rightarrow 2^{N++} \ge N++$.  

## 4.4 Gaps in the rational numbers  
### Exercise  
* 4.4.1 Let x = a/b, which a,b are integers. Whatever a and b are positive or negative, it's obviously we could set a = n*b + d or b = a + f, which n is integer number, and finally get x = a/b = n + d/b or 1 - f/b, then it's easy to get which n is $n \le x < n + 1$. The rest is skipped.  

* 4.4.2 (a) No idea.  
(b) First question is yes. Second is also yes. We could see $n+1/n*2$ is a proper infinite descent sequence. I think that rational number's denseness property cause it.  

* 4.4.3 (a) Every natural number is either even or odd, but not both (why?)  
If a is even and odd, then a = 2k + 1 = 2f, which k and f is natural number, 2k + 1 = 2f, but we could find this equation is no solution in natural number, so contradiction.  
(b) If p is odd, then $p^2$ is also odd (why?)  
p  = 2k + 1, $p^2 = p * p = (2k + 1)(2k + 1)=4k^2 + 4k + 1 = 4k(k + 1) + 1 = 2 * 2k(k+1) + 1$, let 2k(k+1) is a natural number f, we have $2*f + 1$, which also a odd.  
(c) Since $p^2 = 2q^2$, we have q < p (why?)  
$p^2 = q^2 + q^2 \rightarrow q^2 < p^2 \rightarrow q < p$.  