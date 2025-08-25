# Chapter 2 Starting at the beginning: the natural numbers  
## 2.1 The Peano Axioms  
### Axiom  
* 2.1 $0$ is a natural number.  
* 2.2 If $n$ is a natural number, then $n++$ is also a natural number.  
* 2.3 $0$ is not the successor of any natural number; i.e., we have $n++ \ne 0$ for every natural number $n$.  
* 2.4 Different natural numbers must have different successors; i.e., if $n, m$ are natural numbers and $n \ne m$, then $n++ \ne m++$ . Equivalently, if $n++ = m++$, then we must have $n = m$.  
* 2.5 Principle of mathematical induction. Let $P(n)$ be any property pertaining to a natural number $n$. Suppose that $P(0)$ is true, and suppose that whenever $P(n)$ is true, $P(n++)$ is also true. Then $P(n)$ is true for every natural number $n$.  

### Definition  
* 2.1.1 (Informal)  A natural number is any element of the set $N := \lbrace 0, 1, 2, 3, ....\rbrace$.  

### 2.1.4 Proposition: 3 is a natural number   
* We know that $2$ is natural number, and $3$ is $2++$,so $3$ is natural number.  

### 2.1.6 Proposition: 4 is not equal to 0   
* $4$ is $3++$,so $4$ is not equal to $0$.  

### 2.1.8 Proposition: 6 is not equal to 2
* $6$ is 5++,and $2$ is $1++, 5$ is not equal to $1$, so $6$ is not equal to $2$.  

### 2.1.11 Proposition: A certain property $P(n)$ is true for every natural number $n$  
* According to the proposition, $P(0)$ is true, if $P(n)$ is true. Use Axiom 2.5, we must to show $P(n++)$ is true. Because $n++$ is a natural number, $P(n++)$ is also true, so the proposition is true.  

### 2.1.16 Proposition(Recursive definitions): Suppose for each natural number $n$, we have some function $f_n: N \rightarrow N$ from the natural numbers to the natural numbers. Let $c$ be a natural number. Then we can assign a unique natural number $a_n$ to each natural number $n$, such that $a_0 = c$ and $a_{n++}$ = $f_n(a_n)$ for each natural number $n$.  
* The proof is focus on 'unique natural number'. If $a_0$ is set to $c$, according to the proposition, other $a_n$ can not be $c$, because axiom 2.3. If there exist $a_n$ equal to $a_0$, the $n$ must be 0. Now we suppose $a_n$ is true for this property, we can show $a_{n++}$ is also true, because $n++$ is a natural number, and $n++$ is not equal to $n$.  

## 2.2 Addition  
### Definition  
* 2.2.1 Addition of natural numbers. Let $m$ be a natural number. To add $0$ to $m$, we define $0 + m := m$. Now suppose inductively that we have defined how to add $n$ to $m$. Then we can add $n++$ to $m$ by defining $(n++) + m := (n + m)++$.  
* 2.2.7 Positive natural numbers. A natural number $n$ is said to be positive iff it is not equal to $0$.  
* 2.2.11 Ordering of the natural numbers. Let $n$ and $m$ be natural numbers. We say that $n$ is greater than or equal to $m$, and write $n \ge m$ or $m \le n$, iff we have $n = m + a$ for some natural number $a$. We say that $n$ is strictly greater than $m$, and write $n > m$ or $m < n$, iff $n \ge m$ and $n \ne m$.  

### 2.2.2 Lemma: For any natural number $n$, $n + 0 = n$  
* Let $n = 0$, $n + 0 = 0 + 0 = 0 = n$, assume $n + 0 = n$ is true, show $(n++) + 0 = (n + 0)++ = (n++)$ is also true.  

### 2.2.3 Lemma: For any natural numbers $n$ and $m$, $n + (m++) = (n + m)++$    
* Let $n = 0$, $0 + (m++) = (m++) = (0 + m)++$, suppose $n + (m++) = (n+m)++$ is true. Show $(n++) + (m++) = (n + m(++))++ = ((n + m)++)++ = ((n++) + m)++$ is also true.

### 2.2.4 Proposition: (Addition is commutative). For any natural numbers $n$ and $m$, $n+m=m+n$   
* Let $n = 0$, $n + m = 0 + m = m = m + 0 = m + n$, suppose $n + m = m + n$ is true. Show $(n++) + m = (n + m)++ = (m + n)++ = m + (n++)$ is also true.  

### 2.2.5 Proposition: (Addition is associative). For any natural numbers $a,b,c$, we have $(a+b)+c=a+(b+c)$  
* Let $a = 0$,$(a + b) + c = 0 + b + c = 0 + (b + c) = a + (b + c)$, suppose $(a + b) + c = a + (b + c)$ is true, show $((a++) + b) + c = ((a + b)++) + c = ((a + b) + c)++ = (a + (b + c))++ = (a++) + (b + c)$ is also true.  

### 2.2.6 Proposition: (Cancellation law). Let $a,b,c$ be natural numbers such that $a + b = a + c$. Then we have $b = c$   
* Let $a = 0$, if $a + b = b + c$, then $0 + b = 0 + c$, then $b = c$. Assume this property is true for $a$, show $a++$ is also true for this property.  
* If $(a++) + b = (a++) + c$, then $(a + b)++ = (a + c)++$, according to axiom 2.4, different natural numbers must have different successors, so $(a + b)$ must be equal to $(a + c)$, according to the assumption, so for $a++$, also get the $b = c$. 

### 2.2.8 Proposition: If $a$ is positive and $b$ is a natural number, then $a + b$ is positive (and hence $b + a$ is also, by Proposition 2.2.4)  
If $a$ is positive,then $a$ is not equal to $0$, and $b \ge 0$(informal), so $a + b$ must be successor of natural number, and according to Axiom 2.3, $a + b$ can not be 0, then $a + b$ is positive.  

### 2.2.9 Corollary: If a and b are natural numbers such that $a + b = 0$, then $a = 0$ and $b = 0$  
* If $a$ not equal to 0 or $b$ not equal to $0$, use 2.2.8, then $a + b$ is positive.  

### 2.2.10 Lemma : Let a be a positive number. Then there exists exactly one natural number b such that $b++ = a$  
* Let $b = 0$, $0++ = 1$, and $1$ is positive. Assume $n$ is positive and exists exactly $m++ = n$ is true. Show $n++$ also have a natural number $m^o$ such that $m^o++ = n++$. Let $m^o = m++$, and $m^o ++$ is also natural number, then $m^o ++ = (m++)++ = n++$. Closed.  

### 2.2.12 Proposition: (Basic properties of order for natural numbers).  
(a) (Order is reflexive) $a \ge a$.  
* $a \geq a$, because $a + 0 = a$, and $0$ is an natural number.  

(b) (Order is transitive) If $a \ge b$ and $b \ge c$, then $a \ge c$.  
* If $a \geq b$ and $b \geq c$, then $a \geq c$. Because $b + m = a$, $c + n = b$, use $c + n$ to substitute $b$, have $c + n + m = a$, so $a \ge c$.  

(c) (Order is anti-symmetric) If $a \ge b$ and $b \ge a$, then $a = b$.  
* If $a \ge b$ and $b \ge a$, then $a = b$. We have $a + n = b$ and $b + m = a$, then $a + n + m =  a = a + 0$, thought $n + m$ is a natural number, use 2.2.6 proposition, then have $n + m = 0$, use 2.2.9 corollary, then $n = m = 0$, so we get $a = b$.  

(d) (Addition preserves order) $a ≥ b$ if and only if $a + c \ge b + c$.  
* $a≥b$ if and only if $a+c≥b+c$. If $b + n = a$, we can have $a + c = b + n + c = b + c + n$, according to 2.2.11 definition, so $a + c \ge b + c$. If we have $a + c \ge b + c$, then $a + c = b + c + n = b + n + c$, think $b + n$ is a number, use 2.2.6 proposition, so $a = b + n$, and then $a \ge b$.  

(e) $a < b$ if and only if $a++ \le b$.  
* $a < b$ if and only if $a++ \le b$. If $a < b$, according to 2.2.11 definition, we have $a + n = b$ and $n$ not equal to 0, use 2.2.10 lemma for $n$($n$ is positive), there must be a natural number such that $m++ = n$, now we have $a + (m++) = b$, then $(a++) + m = b$, because $m$ is a natural number, So $a++≤b$. If we have $a++ \le b$, then $(a++) + m = b$, then $a + (m++) = b$, because $m++$ can not be 0, then $a < b$.  

(f) $a < b$ if and only if $b = a + d$ for some positive number $d$.  
* $a<b$ if and only if $b = a + d$ for some positive number $d$. If $a < b$, we have $a + d = b$ and $a$ not equal to $b$, assume $d$ is 0, it will get $a = b$, this is a contradiction, so $d$ not equal to 0, then $d$ is positive number. If we have $b = a + d$ for some positive number $d$,so $a \le b$, because $d$ is positive, then $a$ not equal to $b$, so $a < b$ is true.  

### 2.2.13 Proposition: (Trichotomy of order for natural numbers). Let a and b be natural numbers. Then exactly one of the following statements is true: $a<b, a=b$, or $a>b$  
n
### 2.2.14 Proposition: (Strong principle of induction). Let $m_0$ be a natural number, and let $P(m)$ be a property pertaining to an arbitrary natural number $m$. Suppose that for each $m \ge m_0$, we have the following implication: if $P(m^{\prime})$ is true for all natural numbers $m_0 \le m^{\prime} < m$, then $P(m)$ is also true. (In particular, this means that $P(m_0)$ is true, since in this case the hypothesis is vacuous.) Then we can conclude that $P(m)$ is true for all natural numbers $m ≥ m_0$.  
* Hint: define $Q(n)$ to be the property that $P(m)$ is true for all $m_0 ≤ m < n$. Let $n = 0$ then $Q(n)$ is vacuous true(In fact, $Q(n)$ is equal to that if $m_0 ≤ m < n$ then $P(m)$ is true). Skip the hypothesis of induction, show that $Q(n++)$ is true. Since $Q(n)$ is true, we have $P(m)$ is true for $m_0 \le m < n$ and by the implication of 2.2.14 Proposition, $P(n)$ is also true. Now $P(m)$ is true for that $m_0 \le m \le n < n++$ which means that $Q(n++)$ is true. For each natural number $n \ge m_0$ we have $Q(n)$ is true and conclude that $P(m)$ is true for $m_0 \le m < n \Rightarrow P(n)$ is true for $m_0 \le n$ by the implication of 2.2.14 Proposition again. Closed.  
* If no anwser, please see: https://solverer.com/library/terence_tao/analysis_i/exercise_2-2-5.  


### Exercise
Exercise 2.2.1 Prove Proposition 2.2.5
Exercise 2.2.2 Prove Lemma 2.2.10
Exercise 2.2.3 Prove Proposition 2.2.12
Exercise 2.2.4 Justify the three statements marked (why?) in the proof of Proposition 2.2.13.  
* First why (When $a = 0$ we have $0 ≤b$ for all $b$): this means for all natural number $b$ we have $b \ge 0$, use axiom 2.5, obviously when $b = 0$, this is true, suppose $b = n$ is true, we can also get $n + 1 > n \ge 0$ is true, so $b \ge 0$.  
* Second why (If $a > b$,then $a++ > b$): use $a > b$, we have $b + n = a$, and $n$ is positvie, and $b + n + 1 = a + 1 = a++$, this is $b + 1 < a++$, and because $b < b + 1$, so $b < a++$.  
* Third why (If $a = b$,then $a++ > b$): becasue $a++ = a + 1 = b + 1$, and 1 is positive, so $a++ > b$ is true.  

Exercise 2.2.5 Prove Proposition 2.2.14  
Exercise 2.2.6 Let $n$ be a natural number, and let $P(m)$ be a property pertaining to the natural numbers such that whenever $P(m++)$ is true, then $P(m)$ is true. Suppose that $P(n)$ is also true. Prove that $P(m)$ is true for all natural numbers $m ≤ n$; this is known as the principle of backwards induction. (Hint: apply induction to the variable $n$.)  
* Let $Q(n)$ is such property that $P(m)$ is true for all natural numbers $m \leq n$ when $P(n)$ is true.  
* Let $n = 0$, so $m$ must be 0, so $P(m) = P(n)$ is true, then $Q(n)$ is true when $n = 0$. Suppose $Q(n)$ is true, consider $Q(n++)$.  
* So we have $m \leq n < n++$, because $P(n++)$ is true, then $P(n)$ is true, then $P(m)$ is true (because suppose $Q(n)$ is true), so $Q(n++)$ is true.  

## 2.3 Multiplication  
### Definition  
* 2.3.1 (Multiplication of natural numbers). Let $m$ be a natural number. To multiply zero to $m$, we define $0 * m := 0$. Now suppose inductively that we have defined how to multiply $n$ to $m$. Then we can multiply $n++$ to $m$ by defining $(n++) * m := (n * m) + m$.  
* 2.3.11 (Exponentiation for natural numbers). Let $m$ be a natural number. To raise $m$ to the power $0$, we define $m^0 := 1$; in particular, we define $0^0 := 1$. Now suppose recursively that $m^n$ has been defined for some natural number $n$, then we define $m^{n++} := m^n × m$.  

### Lemma 2.3.2 (Multiplication is commutative). Let $n, m$ be natural numbers. Then $n * m = m * n$.  
* Use principle of mathematical induction we could prove that for all natural number $m$ has $m * 0 = 0$.  
* Suppose $n * m = m * n$ is true, show $(n++) * m = m * (n++)$.  
* $(n++) * m = (n * m) + m = (m * n) + m =$.  

### Lemma 2.3.3 (Positive natural numbers have no zero divisors). Let $n, m$ be natural numbers. Then $n * m = 0$ if and only if at least one of $n, m$ is equal to zero. In particular, if n and m are both positive, then $nm$ is also positive.  
* If $n,m$ are both positive, then $\exist n^{\prime}, m^{\prime} \in N, st. n^{\prime}++ = n, m^{\prime}++ = m$. $nm = (n^{\prime}++)(m^{\prime}++) = (n^{\prime}(m^{\prime}++)) + (m^{\prime}++)$, because $m^{\prime}++ > 0 \Rightarrow (n^{\prime}(m^{\prime}++)) + (m^{\prime}++) > 0 \Rightarrow nm > 0$.  
* If $n * m = 0$, suppose $n \ne 0, m \ne 0$, then we could get $n * m \ne 0$ which is a contradiction. Thus if $n * m = 0$ then at least one of $n, m$ is equal to zero.  

### Proposition 2.3.4 (Distributive law). For any natural numbers $a, b, c$, we have $a(b + c) = ab + ac$ and $(b + c)a = ba + ca$.  

### Proposition 2.3.5 (Multiplication is associative). For any natural numbers $a, b, c$, we have $(a * b) * c = a * (b * c)$.  

### Proposition 2.3.6 (Multiplication preserves order). If $a, b$ are natural numbers such that $a < b$, and $c$ is positive, then $ac < bc$.  
* If $a < b$, we have $a = b + m, m > 0$. $a * c = (b + m) * c = bc + mc$, because $c > 0 \Rightarrow mc > 0 \Rightarrow ac > ab$.  

### Corollary 2.3.7 (Cancellation law). Let $a, b, c$ be natural numbers such that $ac = bc$ and $c$ is non-zero. Then $a = b$.  
* Suppose $a \ne b$, then $a < b$ or $b > a$. Suppose $a < b$ and $c > 0$ then $ac < bc$, which is a contradiction with $ac = bc$. Thus $a = b$.  

### Proposition 2.3.9 (Euclidean algorithm). Let $n$ be a natural number, and let $q$ be a positive number. Then there exist natural numbers $m, r$ such that $0 \le r < q$ and $n = mq + r$.  
* If $n < q$, let $m = 0, r = n < q$, then $0 * q + r = r = n$.  
* If $n = q$, let $m = 1, r = 0 < q$, then $mq + r = 1 * q + 0 = n$.  
* If $n > q$, then $n > q \ge 1 \Rightarrow n \ge 2$. Suppose $n = 2$, then $q$ must be $1$. Let $m = 2, r = 0$, $m * q + r = 1 * 2 + 0 = 2 = n$. Suppose when $n = p \ge 2$ proposition 2.3.9 is true, consider the status of proposition 2.3.9 when $n = p++$. (Use strong principle of induction.)  
*  Suppose $n = p++$. If $0 \le r < q - 1$, then let $m^{\prime} = m, r^{\prime} = r + 1 < q$, we have $m^{\prime}q + r^{\prime} = mq + r + 1 = n + 1 = n++$. If $r = q - 1 < q$, let $m^{\prime} = m + 1, r = 0$, then $m^{\prime}q + r^{\prime} = (m + 1)q + 0 = mq + q = mq + r + 1 = p + 1 = p++$. Thus the proposition 2.3.9 is true.  

### Exercises  
Exercise 2.3.1. Prove Lemma 2.3.2. (Hint: modify the proofs of Lemmas 2.2.2, 2.2.3 and Proposition 2.2.4.)  
Exercise 2.3.2. Prove Lemma 2.3.3. (Hint: prove the second statement first.)  
Exercise 2.3.3. Prove Proposition 2.3.5. (Hint: modify the proof of Proposition 2.2.5 and use the distributive law.)  
Exercise 2.3.4. Prove the identity $(a + b)^2 = a^2 + 2ab + b^2$ for all natural numbers $a, b$.  
* $(a + b)^2 = (a + b)(a + b) = a(a + b) + b(a + b) = a^2 + ab + ab + b^2 = a^2 + 2ab + b^2$.  

Exercise 2.3.5. Prove Proposition 2.3.9. (Hint: fix $q$ and induct on $n$.)  