---
title: Terecent Tao Analysis I Chapter5 & Exercise
date: 2023-8
mathjax: true
categories: 
- Math
tags: 
- Math
---
# Chapter 5  
* Just to record my own thought and answer,if there has any error,please leave a message in the comment area. 
## 5.1 Cauchy sequences
### Exercise  
* 5.1.1 If $a_n$ is a Cauchy sequences, then there exist a N such that $d(a_i,a_j) \le ε$ for $i,j \ge N$. $a_i....a_{N - 1}$ is finite sequence so has a limit value M, and for $n \ge N$, because of $d(a_i,a_j) \le ε$ for $i,j \ge N$, we could select $a_N$ as base number, obviously for $n \ge N$, $|a_n| \le |a_N| + ε$. Then all $a_n \le max(M,a_N + ε)$.  

## 5.2 Equivalent Cauchy sequences  
### Exercise  
* 5.2.1 Skip.   
* 5.2.2 Skip.  

## 5.3 The construction of the real numbers  
### Lemma 5.3.14 Since we already know that $|b_{n0} − b_n| ≤ ε/2$ for all n ≥ N, we thus conclude from the triangle inequality (how?)  
* $ε/2 \ge |b_{n0} − b_n| \ge ||b_{n0}| − |b_n|| \rightarrow ||b_{n0}| − |b_n|| \le ε/2 \rightarrow -ε/2 \le |b_{n0}| − |b_n| \le ε/2 \rightarrow -ε/2 + |b_{n0}| \le |b_n|$, we know that $|b_{n0}| > ε \rightarrow |b_{n0}| - ε/2 > ε - ε/2 \rightarrow |b_{n0}| - ε/2 > ε/2$, then $ε/2 < -ε/2 + |b_{n0}| \le |b_n|$  

### Exercise  
* 5.3.1 Skip.  
* 5.3.2 Skip.  
* 5.3.3 If $\lim_{n\rightarrow \infty}a = \lim_{n\rightarrow \infty}b \rightarrow |a - b| < ε$ for every $ε > 0$. If $a \neq b$, we will find a ration number ε such that $|a - b| = d > ε$, then contradiction.  
* 5.3.4 Because $a_n = b_n$, them are eventually ε-close, and use 5.2.2 $''
aszwsqb_n$ is bounded.  
* 5.3.5 Skip.  

## 5.4 Ordering the reals  
### Exercise  
* 5.4.1 Skip.  
* 5.4.2 Skip.  
* 5.4.3 Like Proposition 4.4.2. We could set the real number x be a rational number sequence $a_n$ and use the Proposition 5.4.4, the rest skip.  
* 5.4.4 If $x > 0 \rightarrow x^{-1} > 0 \rightarrow x^{-1} < M + 1 = N \rightarrow x > N^{-1}$.  
* 5.4.5 If $x < y \rightarrow x + d = y$, d is a positive number, so we have $d > 1/n > 0$, q and r is rational number. Then $x < x + 1/N < x + d = y \rightarrow x < \frac{Nx + 1}{N} < x + d$, $Nx$ is a real, we have $n \le Nx < n + 1 \rightarrow \frac{n}{N} < x < \frac{n + 1}{N}$, then use $n$ to substitute $Nx$, $x < \frac{Nx + 1}{N} < x + d \rightarrow x < \frac{n + 1}{N} \le \frac{Nx + 1}{N} < x + d$, the $\frac{n + 1}{N}$ is the rational number we want.   
* 5.4.6 Skip.  
* 5.4.7 If $x \le y + ε$, suppose $x > y \rightarrow x = y + d$, d is a positive real, we have $y + d \le y + ε \rightarrow d \le ε$ for all real numbers $ε > 0$, use Proposition 5.4.12, we could always find a number r(r > 0) such that $r \le d$. Contradiction. The rest is skip.  
* 5.4.8 Suppose $\lim_{n\rightarrow\infty}a_n = y > x$, then have a rational number $y > q > x$, suppose $(b_n) = q$, then we have $b_n = q > x \ge a_n \rightarrow b_n > a_n$, use Corollary 5.4.10, we could deduce that $lim_{n\rightarrow\infty}b_n > lim_{n\rightarrow\infty}a_n$, contradiction. The rest is skip.  

## 5.5 The least upper bound property  
### Exercise  
* 5.5.1 Because M is sup(E), $M \ge x$ which x is in E. Then we could have $-M \le -x$ which x is in E. The set -E is -x which x in E, so -M is inf(-E).  
* 5.5.2 Suppose there exists a natural number m ($L<m<K$) such that, $m/n$ and $(m - 1)/n$ are upper bound of E. If such property is true, then let $m - 1 = n$, we could deduce $n - 1$ is also an upper bound of E, induction on m eventually we could get L is an upper bound of E which is a contradiction to question setting.  
* 5.5.3 Suppose $m \neq m^o$, then $m > m^o$ or $m < m^o$. We coulde select $m > m^o$ to prove. If $m > m^o$, then $m - 1 \ge m^o$, we know that $\frac{m - 1}{n}$ is not upper bounds for E, so $\frac{m - 1}{n} \ge \frac{m^o}{n}$ and $\frac{m^o}{n}$ is also not an upper bound for E which contradiction to question setting.  
* 5.5.4 First question is no idea. The second question have a try: let such sequence $a_n = |q_m - q_n|$ for every $n \ge M \ge 1$, accordint to question setting we have $a_n = |q_m - q_n| \le \frac{1}{M}$ for every $n \ge 1$, use Exercise 5.4.8 get $a_n \le \frac{1}{M}$