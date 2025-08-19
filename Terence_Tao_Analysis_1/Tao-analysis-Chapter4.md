# Chapter 4 Integers and rationals  
## 4.1 The integers  
### Definitions  
* 4.1.1 (Integers). An integer is an expression of the form $a \text{---} b$, where $a$ and $b$ are natural numbers. Two integers are considered to be equal, $a \text{---} b = c \text{---} d$, if and only if $a + d = c + b$. We let $Z$ denote the set of all integers.  
* 4.1.2. The sum of two integers, $(a \text{---} b)+(c \text{---} d)$, is defined by the formula $(a \text{---} b) + (c \text{---} d) := (a + c) \text{---} (b + d)$. The product of two integers, $(a \text{---} b) * (c \text{---} d)$, is defined by $(a \text{---} b) * (c \text{---} d) := (ac + bd) \text{---} (ad + bc)$.  
* (from proof of Lemma 4.1.3) The integers $n \text{---} 0$ behave in the same way as the natural numbers $n$; indeed one can check that $(n \text{---} 0) + (m \text{---} 0) = (n + m) \text{---} 0$ and $(n \text{---} 0)×(m \text{---} 0) = nm \text{---} 0$. Furthermore, $(n \text{---} 0)$ is equal to $(m \text{---} 0)$ if and only if $n = m$. (The mathematical term for this is that there is an isomorphism between the natural numbers $n$ and those integers of the form $n \text{---} 0$.) Thus we may identify the natural numbers with integers by setting $n \equiv n \text{---} 0$; this does not affect our definitions of addition or multiplication or equality since they are consistent with each other. In particular $0$ is equal to $0 \text{---} 0$ and $1$ is equal to $1 \text{---} 0$.  
* 4.1.4 (Negation of integers). If $(a \text{---} b)$ is an integer, we define the negation $−(a \text{---}  b)$ to be the integer $(b \text{---}  a)$. In particular if $n = n \text{---} 0$ is a positive natural number, we can define its negation $−n = 0 \text{---} n$.  
* (From Remark 4.1.7) We now define the operation of subtraction $x − y$ of two integers by the formula $x − y := x + (−y)$. One can easily check now that if $a$ and $b$ are natural numbers, then $a − b = a + (−b) = (a \text{---} 0) + (0 \text{---} b) = a \text{---} b$, and so $a \text{---} b$ is just the same thing as $a − b$.  
* 4.1.10 (Ordering of the integers). Let $n$ and $m$ be integers. We say that $n$ is greater than or equal to $m$, and write $n \ge m$ or $m \le n$, iff we have $n = m + a$ for some natural number $a$. We say that $n$ is strictly greater than $m$, and write $n > m$ or $m < n$, iff $n \ge m$ and $n \ne m$.  

### Lemma 4.1.3 (Addition and multiplication are well-defined). Let $a, b, a^\prime, b^\prime, c, d$ be natural numbers. If $(a \text{---} b) = (a^\prime \text{---} b^\prime)$, then $(a \text{---} b) + (c \text{---} d) = (a^\prime \text{---} b^\prime) + (c \text{---} d)$ and $(a \text{---} b) * (c \text{---} d) = (a^\prime \text{---} b^\prime) * (c \text{---} d)$, and also $(c \text{---} d) + (a \text{---} b) = (c \text{---} d) + (a^\prime \text{---} b^\prime)$ and $(c \text{---} d) * (a \text{---} b) = (c \text{---} d) * (a^\prime \text{---} b^\prime).$ Thus addition and multiplication are well-defined operations (equal inputs give equal outputs).  
* $(a \text{---} b) = (a^\prime \text{---} b^\prime) \Rightarrow a + b^\prime = a^\prime + b \Rightarrow a + b^\prime + c + d = a^\prime + b + c + d \Rightarrow (a + c) + (b^\prime + d) = (a^\prime + c) + (b + d) \Rightarrow (a + c) \text{---} (b + d) = (a^\prime + c) \text{---} (b^\prime + d) \Rightarrow (a \text{---} b) + (c \text{---} d) = (a^\prime \text{---} b^\prime) + (c \text{---} d)$.  

### Lemma 4.1.5 (Trichotomy of integers). Let $x$ be an integer. Then exactly one of the following three statements is true: (a) $x$ is zero; (b) $x$ is equal to a positive natural number $n$; or (c) $x$ is the negation $−n$ of a positive natural number $n$.  
* Let $a, b \in N, x = a \text{---} b$. Use trichotomy of natural numbers. If $a = b$, then $x = a \text{---} b = a \text{---} a = 0 \text{---} 0 = 0$. If $a > b$, then $a = b + n, n > 0 \Rightarrow a \text{---} b = n \text{---} 0 = n\Rightarrow x$ is a positive natural number. If $a < b$, then $a + n = b + 0 \Rightarrow a \text{---} b = 0 \text{---} n = -(n \text{---} 0) \Rightarrow x$ is the negation $-n$ of a pisitvie natural number $n$. Skip the rest.  

### Proposition 4.1.6 (Laws of algebra for integers). Let $x, y, z$ be integers. Then we have $x + y = y + x, (x + y) + z = x + ( y + z), x + 0 = 0 + x = x, x + (−x) = (−x) + x = 0, xy = yx, (xy)z = x(yz), x1 = 1 x = x, x(y + z) = xy + xz, (y + z)x = yx + zx$.  
* Let $x = a - b, y = c - d, z = e - f$.  
* $x + y = (a - b) + (c - d) = (a + c) - (b + d) = (c + a) - (d + b) = (c - d) + (a - b) = y + x$.  
* $(x + y) + z = ((a + c) - (b + d)) + (e - f) = (a + c + e) - (b + d + f)$, $x + (y + z) = (a - c) + ((b + e) - (d + f)) = (a + c + e) - (b + d + f) = (x + y) + z$.  
* $0 + x = (0 - 0) + (a - b) = (0 + a) - (0 + b) = a - b = x$.  
* $(a - b) + (- (a - b)) = (a - b) + (b - a) = (a + b) - (a + b) = 0 - 0 = 0$.  
* $xy = (a - b)(c - d) = (ac + bd) − (ad + bc) = (bd + ac) - (bc + ad) = (c - d)(a - b) = yx$.  
* $(xy)z=xyz=x(yz)$.  
*  $1x = (1 - 0)(a - b) = (1a - 0) - (0 + 1b) = a - b$.  
*  $x(y + z) = (a - b)((c + e) - (d + f)) = (a(c + e) + b(d + f)) - (a(d + f) - b(c + e)) = xy + xz$.  
*  $(y + z)x = x(y + z) = xy + xz = yx + zx$.  

### Proposition 4.1.8 (Integers have no zero divisors). Let $a$ and $b$ be integers such that $ab = 0$. Then either $a = 0$ or $b = 0$ (or both).  
* Suppose $a \ne 0, b \ne 0$, let $m, n, g, h \in N, a = m - n, b = g - h$, then $ab = (m - n)(g - h) = (mg + nh) - (mh + ng)$. This is a contradiction.  

### Corollary 4.1.9 (Cancellation law for integers). If $a, b, c$ are integers such that $ac = bc$ and $c$ is non-zero, then $a = b$.  
* $ac = bc$, because $ab,bc$ are integers,then $ac - bc = bc - bc \rightarrow ac - bc = 0$. c is non-zero, $ac - bc = 0 \rightarrow c(a - b) = 0$, use Proposition 4.1.8 we have $a - b = 0 \rightarrow a = b$.  

### Lemma 4.1.11 (Properties of order). Let $a, b, c$ be integers.  
(a) $a > b$ if and only if $a − b$ is a positive natural number.  
* if $a > b$, then $a = b + m, m$ is a positive natural number. Then $a - b = b + m - b \rightarrow a - b = m, m$ is positive, $a - b$ is also positvie.  

(b) (Addition preserves order) If $a > b$, then $a + c > b + c$.  
* if $a > b$, then $a = b + m$, then $a + c = b + c + m$, then $a + c > b + c$.  

(c) (Positive multiplication preserves order) If $a > b$ and $c$ is positive, then $ac > bc$.  
* if $a > b$ and $c$ is positive, $a = b + m \rightarrow c * a = (b + m) * c \rightarrow ac = bc + cm \rightarrow ac > bc$.  

(d) (Negation reverses order) If $a > b$, then $−a < −b$.  
* if $a > b, a = b + m \rightarrow -a = (-b) + (-m) \rightarrow -a + m = (-b) + (-m) + m \rightarrow -a + m = -b \rightarrow -a < -b$.  

(e) (Order is transitive) If $a > b$ and $b > c$, then $a > c$.  
* if $a > b$ and $b > c, a = b + m, b = c + n \rightarrow a = c + n + m$, let $n + m = d$, then $a = c + d \rightarrow a > c$.  

(f) (Order trichotomy) Exactly one of the statements $a > b, a < b$, or $a = b$ is true.  

### Exercise  
Exercise 4.1.1. Verify that the definition of equality on the integers is both reflexive and symmetric.  
* $a \text{---} b = a \text{---} b \rightarrow a + b = a + b$(reflexive). If $a \text{---} b = c \text{---} d$, then $a + d = c + b \rightarrow a + d + c + b = c + b + a + d \rightarrow c + b = a + d \rightarrow c \text{---} d = a \text{---} b$(symmetric).  

Exercise 4.1.2. Show that the definition of negation on the integers is well-defined in the sense that if $(a \text{---} b) = (a^\prime \text{---} b^\prime)$, then $−(a \text{---} b) = −(a^\prime \text{---} b^\prime)$ (so equal integers have equal negations).  
* If $a - b = a^o - b^o$, $a - b = a^o - b^o \rightarrow b^o + a = b + a^o \rightarrow b - a = b^o - a^o \rightarrow -(a - b) = -(a^o - b^o)$.  

Exercise 4.1.3. Show that $(−1) * a = −a$ for every integer $a$.  
* 4.1.3 $(-1) * a + 1 * a = a(1 + (-1)) = a * 0 = 0$, then $(-1)*a = -a$.  

Exercise 4.1.4. Prove the remaining identities in Proposition 4.1.6. (Hint: one can save some work by using some identities to prove others. For instance, once you know that xy = yx, you get for free that x1 = 1 x, and once you also prove $x(y + z) = xy + xz$, you automatically get $(y + z)x = yx + zx$ for free.)
Exercise 4.1.5. Prove Proposition 4.1.8. (Hint: while this proposition is not quite the same as Lemma 2.3.3, it is certainly legitimate to use Lemma 2.3.3 in the course of proving Proposition 4.1.8.)  
Exercise 4.1.6. Prove Corollary 4.1.9. (Hint: there are two ways to do this. One is to use Proposition 4.1.8 to conclude that a − b must be zero. Another way is to combine Corollary 2.3.7 with Lemma 4.1.5.)  
Exercise 4.1.7. Prove Lemma 4.1.11. (Hint: use the first part of this lemma to prove all the others.)  
Exercise 4.1.8. Show that the principle of induction (Axiom 2.5) does not apply directly to the integers. More precisely, give an example of a property $P(n)$ pertaining to an integer $n$ such that $P(0)$ is true, and that $P(n)$ implies $P(n++)$ for all integers $n$, but that $P(n)$ is not true for all integers $n$. Thus induction is not as useful a tool for dealing with the integers as it is with the natural numbers. (The situation becomes even worse with the rational and real numbers, which we shall define shortly.)  

## 4.2 The rationals  
### Definitions  
* 4.2.1. A rational number is an expression of the form $a//b$, where $a$ and $b$ are integers and b is non-zero; $a//0$ is not considered to be a rational number. Two rational numbers are considered to be equal, $a//b = c//d$ if and only if $ad = cb$. The set of all rational numbers is denoted $Q$.  
* 4.2.2. If $a//b$ and $c//d$ are rational numbers, we define their sum $(a//b) + (c//d) := (ad + bc)//(bd)$, their product $(a//b) ∗ (c//d) := (ac)//(bd)$ and the negation $−(a//b) := (−a)//b$. Note that if $b$ and $d$ are non-zero, then $bd$ is also non-zero, by Proposition 4.1.8, so the sum or product of two rational numbers remains a rational number.  
* (from proof of Lemma 4.2.3) We now define a new operation on the rationals: reciprocal. If $x = a//b$ is a non-zero rational (so that $a, b \ne 0$) then we define the reciprocal $x^{−1}$ of $x$ to be the rational number $x^{−1}:= b//a$. We leave the reciprocal of $0$ undefined.  
* (from proof of Lemma 4.2.3) we will identify $a$ with $a//1$ for each integer $a: a \equiv a//1$
* (from Remark 4.2.5) We can now define the quotient $x/y$ of two rational numbers $x$ and $y$, provided that $y$ is non-zero, by the formula $x/y := x * y^{−1}$.  
* 4.2.6. A rational number x is said to be positive iff we have $x = a/b$ for some positive integers $a$ and $b$. It is said to be negative iff we have $x = −y$ for some positive rational $y$ (i.e., $x = (−a)/b$ for some positive integers $a$ and $b$).  
* 4.2.8 (Ordering of the rationals). Let $x$ and $y$ be rational numbers. We say that $x > y$ iff $x − y$ is a positive rational number, and $x < y$ iff $x − y$ is a negative rational number. We write $x \ge y$ iff either $x > y$ or $x = y$, and similarly define $x \le y$.  


### Lemma 4.2.3. The sum, product, and negation operations on rational numbers are well-defined, in the sense that if one replaces $a//b$ with another rational number $a^\prime//b^\prime$ which is equal to $a//b$, then the output of the above operations remains unchanged, and similarly for $c//d$.  

### Proposition 4.2.4 (Laws of algebra for rationals). Let $x, y, z$ be rationals. Then he following laws of algebra hold: $x + y = y + x, (x + y) + z = x + ( y + z), x + 0 = 0 + x = x, x + (−x) = (−x) + x = 0, xy = yx, (xy)z = x(yz), x1 = 1x = x, x(y + z) = xy + xz, (y + z)x = yx + zx$. If x is non-zero, we also have $xx^{−1} = x^{−1}x = 1.$  

### Lemma 4.2.7 (Trichotomy of rationals). Let $x$ be a rational number. Then exactly one of the following three statements is true: (a) $x$ is equal to $0$. (b) $x$ is a positive rational number. (c) $x$ is a negative rational number.  

### Proposition 4.2.9 (Basic properties of order on the rationals). Let $x, y, z$ be rational numbers. Then the following properties hold.  
(a) (Order trichotomy) Exactly one of the three statements $x = y, x < y,$ or $x > y$ is true.  
* Let $x = a/b, y = c/d$ and $a,b,c,d \in Z, b \ge 0, d \ge 0$, then $x - y = ab - cd / bd$, $ab$ and $cd$ are in $Z$, use (f) of Lemma 4.1.11, $ab$ and $cd$ hold one of the three statements: $ab = cd, ab < cd$, or $ab > cd$, this will leads to rationals' order trichotomy.   

(b) (Order is anti-symmetric) One has $x < y$ if and only if $y > x$.  
(c) (Order is transitive) If $x < y$ and $y < z$, then $x < z$.  
(d) (Addition preserves order) If $x < y$, then $x + z < y + z$.  
(e) (Positive multiplication preserves order) If $x < y$ and $z$ is positive, then $xz < yz$.  

### Exercise  
Exercise 4.2.1. Show that the definition of equality for the rational numbers is reflexive, symmetric, and transitive. (Hint: for transitivity, use Corollary 4.1.9.)  
Exercise 4.2.2. Prove the remaining components of Lemma 4.2.3.    
Exercise 4.2.3. Prove the remaining components of Proposition 4.2.4. (Hint: as with Proposition 4.1.6, you can save some work by using some identities to prove others.)  
Exercise 4.2.4. Prove Lemma 4.2.7. (Note that, as in Proposition 2.2.13, you have to prove two different things: firstly, that at least one of (a), (b), (c) is true; and secondly, that at most one of (a), (b), (c) is true.)   
Exercise 4.2.5. Prove Proposition 4.2.9.  
Exercise 4.2.6. Show that if $x, y, z$ are rational numbers such that $x < y$ and $z$ is negative, then $xz > yz$.
* if $x < y, z$ is negative. $x + d = y, d \in Q, d > 0 \Rightarrow x * z + d * z = y * z, d * z < 0 \Rightarrow xz > yz$.  

## 4.3 Absolute value and exponentiation  
### Definitions  
* 4.3.1 (Absolute value). If $x$ is a rational number, the absolute value $|x|$ of $x$ is defined as follows. If $x$ is positive, then $|x| := x$. If $x$ is negative, then $|x| := −x$. If $x$ is zero, then $|x| := 0$.  
* 4.3.2 (Distance). Let $x$ and $y$ be rational numbers. The quantity $|x − y|$ is called the distance between $x$ and $y$ and is sometimes denoted $d(x, y)$, thus $d(x, y) := |x − y|$.  
* 4.3.4 ($\epsilon$-closeness). Let $\epsilon > 0$ be a rational number, and let $x, y$ be rational numbers. We say that $y$ is $\epsilon$-close to $x$ iff we have $d(y, x) \le \epsilon$. This definition is not standard in mathematics text-books; we will use it as “scaffolding” to construct the more important notions of limits (and of Cauchy sequences) later on, and once we have those more advanced notions we will discard the notion of $\epsilon$-close.  
* 4.3.9 (Exponentiation to a natural number). Let $x$ be a rational number. To raise $x$ to the power $0$, we define $x^0 := 1$; in particular we define $0^0 := 1$. Now suppose inductively that $x^n$ has been defined for some natural number $n$, then we define $x^{n+ 1} := x^n * x$.  
* 4.3.11 (Exponentiation to a negative number). Let $x$ be a non-zero rational number. Then for any negative integer $−n$, we define $x^{−n} := 1/x^n$.  

### Proposition 4.3.3 (Basic properties of absolute value and distance). Let $x, y, z$ be rational numbers.  
(a) (Non-degeneracy of absolute value) We have $|x| \ge 0$. Also, $|x| = 0$ if and only if $x$ is $0$.  
(b) (Triangle inequality for absolute value) We have $|x + y| \le |x|+|y|$.  
(c) We have the inequalities $−y \le x \le y$ if and only if $y \ge | x|$. In particular, we have $−|x| \le x \le |x|$.  
(d) (Multiplicativity of absolute value) We have $|xy| = |x| * |y|$. In particular, $|−x| = |x|$.  
(e) (Non-degeneracy of distance) We have $d(x, y) \ge 0$. Also, $d(x, y) = 0$ if and only if $x = y$.
(f) (Symmetry of distance) $d(x, y) = d(y, x)$.  
(g) (Triangle inequality for distance) $d(x, z) \le d(x, y) + d(y, z)$.  

### Proposition 4.3.7. Let $x, y, z, w$ be rational numbers.  
(a) If $x = y$, then $x$ is $\epsilon$-close to $y$ for every $\epsilon > 0$. Conversely, if $x$ is $\epsilon$-close to $y$ for every $\epsilon > 0$, then we have $x = y$.  
(b) Let $\epsilon > 0$. If $x$ is $\epsilon$-close to $y$, then $y$ is $\epsilon$-close to $x$.  
(c) Let $\epsilon, \delta > 0$. If $x$ is $ε$-close to $y$, and $y$ is $\delta$-close to $z$, then $x$ and $z$ are $(\epsilon + \delta)$-close.  
(d) Let $\epsilon, \delta > 0$. If $x$ and $y$ are $\epsilon$-close, and $z$ and $w$ are $\delta$-close, then $x + z$ and $y + w$ are $(\epsilon + \delta)$-close, and $x − z$ and $y − w$ are also $(\epsilon + \delta)$-close.
(e) Let $\epsilon > 0$. If $x$ and $y$ are $\epsilon$-close, they are also $\epsilon^\prime$-close for every $\epsilon^\prime > \epsilon$.  
(f) Let $\epsilon > 0$. If $y$ and $z$ are both $\epsilon$-close to $x$, and $w$ is between $y$ and $z$ (i.e., $y \le w \le z$ or $z \le w \le y$), then $w$ is also $\epsilon$-close to $x$.
(g) Let $\epsilon > 0$. If $x$ and $y$ are $\epsilon$-close, and $z$ is non-zero, then $xz$ and $yz$ are $\epsilon|z|$-close.
(h) Let $\epsilon, \delta > 0$. If $x$ and $y$ are $ε$-close, and $z$ and $w$ are $\delta$-close, then $xz$ and $yw$ are $(\epsilon|z| + \delta|x| + \epsilon \delta)$-close.  
* $|xz - yw| = |xz - zy + zy - yw| =|z(x -y) + y(z - w)| \le |z(x - y)| + |y(z - w)| \le \epsilon|z| + |y(z - w)| = \epsilon|z| + |x(z - w) + y(z - w) - x(z - w)| \le \epsilon|z| + |x(z - w)| + |y(z - w) - x(z - w)| \le \epsilon|z| + \delta|x| + |(y - x)(z - w)| \le \epsilon|z| + \delta|x| + \epsilon \delta$.  

### Proposition 4.3.10 (Properties of exponentiation, I). Let $x, y$ be rational numbers, and let $n, m$ be natural numbers.  
(a) We have $x^nx^m = x^{n+m}, (x^n)^m = x^{nm}$, and $(xy)^n = x^ny^n$.  
* Use induction to prove. Suppose $m = 0, x^nx^m = x^n = x^{n + 0} = x^{n + m}$. Show when $m++$ also be true. $x^nx^{m++} = x^nx^{m + 1} = x^n * x * x^m = x^{n + 1}x^m = x^{n + m + 1} = x^{n + (m++)}$. Close the induction.  
* Aslo use induction to prove $(x^n)^m = x^{nm}$. Skip the preceding hypothesis steps, $(x^n)^{m+1} = (x^n)^m * (x^n) = x^{nm} * x^n = x^{nm + n} = x^{n(m++)}$. Closed.  
* Skip the preceding hypothesis steps, $(xy)^{n++} = (xy)^n * xy = x^n * y^n * x * y = x^{n++}y^{n++}$. Closed.  

(b) Suppose $n > 0$. Then we have $x^n = 0$ if and only if $x = 0$.  
* If $x^n = 0$ and suppose $x \ne 0$, then immediately contradiction with proposition 4.1.8.  

(c) If $x \ge y \ge 0$, then $x^n \ge y^n \ge 0$. If $x > y \ge 0$ and $n > 0$, then $x^n > y^n \ge 0$.  
(d) We have $|x^n| = |x|^n$.  
* Skip the preceding hypothesis steps of induction. $|x|^{n+1} = |x|^n|x| = |x^n||x| = |x^nx| = |x^{n+1}|$.  

### Proposition 4.3.12 (Properties of exponentiation, II). Let $x, y$ be non-zero rational numbers, and let $n, m$ be integers.  
(a) We have $x^nx^m = x^{n+m}, (x^n)^m = x^{nm}$, and $(xy)^n = x^ny^n$.  
(b) If $x \ge y > 0$, then $x^n \ge y^n > 0$ if $n$ is positive, and $0 < x^n \le y^n$ if $n$ is negative.  
* $x \ge y \Rightarrow x = y + d, d \ge 0 \Rightarrow x^{-1}y^{-1} * x = x^{-1}y^{-1} * (y + d) = y^{-1} = x^{-1} + x^{-1}y^{-1}d, x^{-1}y^{-1}d \ge 0 \Rightarrow x^{-1} \le y^{-1}$. If $n$ is negative, then let $-m = n$ for some natural number $m$, and $x^n = (1/x)^m, y^n = (1/y)^m, 1/y \ge 1/x \Rightarrow (1/y)^m \ge (1/x)^m > 0 \Rightarrow 0 < x^n \le y^n$.  

(c) If $x, y > 0, n \ne 0$, and $x^n = y^n$, then $x = y$.  
* Suppose $x \ne y$, then $x > y$ or $x < y$. If $x > y \Rightarrow x = y + d, d > 0 \Rightarrow x^n = (y + d)^n \Rightarrow (y + d)^n \ge y^n + d^n \ge y^n \Rightarrow x^n \ge y^n$ which is a contradiction with $x^n = y^n$.     

(d) We have $|x^n| = |x|^n$.  

### Exercise  
Exercise 4.3.1. Prove Proposition 4.3.3. (Hint: while all of these claims can be proven by dividing into cases, such as when $x$ is positive, negative, or zero, several parts of the proposition can be proven without such a tedious division into cases. For instance one can use earlier parts of the proposition to prove later ones.)  
Exercise 4.3.2. Prove the remaining claims in Proposition 4.3.7.  
Exercise 4.3.3. Prove Proposition 4.3.10. (Hint: use induction.)  
Exercise 4.3.4. Prove Proposition 4.3.12. (Hint: induction is not suitable here. Instead, use Proposition 4.3.10.)   
Exercise 4.3.5. Prove that $2^N ≥ N$ for all positive integers $N$. (Hint: use induction.)  
* If $N = 0, 2^N = 1 \ge N = 0$. Show $N++(N \ge 0)$ is true. $2^{N++} = 2^N* 2 \ge N * 2 = N + N \ge N + 1 \Rightarrow 2^{N++} \ge N++$.  

## 4.4 Gaps in the rational numbers  

### Proposition 4.4.1 (Interspersing of integers by rationals). Let $x$ be a rational number. Then there exists an integer $n$ such that $n \le x < n + 1$. In fact, this integer is unique (i.e., for each $x$ there is only one $n$ for which $n \le x < n + 1$). In particular, there exists a natural number $N$ such that $N > x$ (i.e., there is no such thing as a rational number which is larger than all the natural numbers).  
* Proposition 2.3.9 (Euclidean algorithm). Let $n$ be a natural number, and let $q$ be a positive number. Then there exist natural numbers $m, r$ such that $0 \le r < q$ and $n = mq + r$.  
* Suppose $x > 0, x = n / q$ and $n, q \in N, q > 0 \Rightarrow n = mq + r, 0 \le r < q \Rightarrow x = (mq + r) / q = m + r / q \Rightarrow m \le x = m + r / q \le m + 1$.  
* Suppose $x < 0, x = n / q$ and $n, q\in Z, n < 0, q > 0$. Let $-n = p, p > 0, x = -(-n/q) = -(p/q)$. Obviously, we have $m \le p/q \le m + 1 \Rightarrow -(m + 1) \le -(p/q) \le -m$. Let $-(m + 1) = m^\prime \Rightarrow -m = m^\prime + 1$ then $-(m + 1) \le -(p/q) \le -m \Rightarrow m^\prime \le -(p/q) \le m^\prime + 1$.  
* Suppose $x = 0 \Rightarrow 0 \le x \le 0 + 1$.  

### Proposition 4.4.3 (Interspersing of rationals by rationals). If $x$ and $y$ are two rationals such that $x < y$, then there exists a third rational $z$ such that $x < z < y$.  

### Proposition 4.4.4. There does not exist any rational number $x$ for which $x^2 = 2$.  

### Proposition 4.4.5. For every rational number $\epsilon > 0$, there exists a non-negative rational number $x$ such that $x^2 < 2 < (x + \epsilon)^2$.  
* Suppose $\epsilon^2 > 2$, let $x = 0 \Rightarrow x^2 < 2$ and $2 < \epsilon^2 + x^2 \le \epsilon^2 + 2x\epsilon + x^2 = (x + \epsilon)^2$.  
* Suppose $1 \le \epsilon < 2$, let $x = 1 \Rightarrow 0 < 1 < 2 < (1 + \epsilon)^2 \Rightarrow 0 < x^2 < 2 < (x + \epsilon)^2$.  
* Suppose $0 < \epsilon < 1$, let $\epsilon = p / q$ which $q = p + d$ and $p > 0, q > 0, d > 0$. Let $x = 1 + d / p + 1 / (p + 1)$

### Exercise  
Exercise 4.4.1. Prove Proposition 4.4.1. (Hint: use Proposition 2.3.9.)  
Exercise 4.4.2. A definition: a sequence $a_0, a_1, a_2, ...$ of numbers (natural numbers, integers, rationals, or reals) is said to be in infinite descent if we have $a_n > a_{n+1}$ for all natural numbers $n$ (i.e., $a_0 > a_1 > a_2 > ....$).  
(a) Prove the principle of infinite descent: that it is not possible to have a sequence of natural numbers which is in infinite descent. (Hint: assume for sake of contradiction that you can find a sequence of natural numbers which is in infinite descent. Since all the $a_n$ are natural numbers, you know that $a_n \ge 0$ for all $n$. Now use induction to show in fact that $a_n \ge k$ for all $k \in N$ and all $n \in N$, and obtain a contradiction.)  
* Suppose there exists a sequence($a_n$) of natural numbers which is in infinite descent. Since $a_n \in N$ then $a_n \ge 0$, and Suppose $a_n \ge k$ consider $a_n \ge k++$. $a_n > a_{n + 1} \ge k \Rightarrow a_n \ge k ++$. Thus $a_n \ge k$ for all $k \in N$ and all $n \in N$. Let $a_n = k^\prime, k^\prime \in N$, we could find $k^\prime ++ > k^\prime$, contradiction.  

(b) Does the principle of infinite descent work if the sequence $a_1, a_2, a_3, ...$ is allowed to take integer values instead of natural number values? What about if it is allowed to take positive rational values instead of natural numbers? Explain.  
* Taking integer values instead of natural number values is allowed. For example, $a_{n + 1} = a_n - 1, a_n \in Z$.  
* Taking positive rational values instead of natural numbers is allowed. For example, $a_{n + 1} = a_n / 2, a_n \in Z$.  

Exercise 4.4.3. Fill in the gaps marked (why?) in the proof of Proposition 4.4.4.  
(a) Every natural number is either even or odd, but not both (why?)  
* If a is even and odd, then $a = 2k + 1 = 2f$, which $k$ and $f$ is natural number, $2k + 1 = 2f$, but we could find this equation is no solution in natural number, so contradiction.  

(b) If $p$ is odd, then $p^2$ is also odd (why?)  
* $p  = 2k + 1, p^2 = p * p = (2k + 1)(2k + 1) = 4k^2 + 4k + 1 = 4k(k + 1) + 1 = 2 * 2k(k+1) + 1$, let $2k(k+1)$ is a natural number $f$, we have $2*f + 1$, which also a odd number.  

(c) Since $p^2 = 2q^2$, we have $q < p$ (why?)  
* $p^2 = q^2 + q^2 \rightarrow q^2 < p^2 \rightarrow q < p$.  