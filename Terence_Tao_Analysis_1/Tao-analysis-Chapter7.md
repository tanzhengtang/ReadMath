# Chapter 7 Series  
## 7.1 Finite series  
### Definitions  
* 7.1.1 (Finite series). Let $m, n$ be integers, and let $(a_i)_{i=m}^i$ be a finite sequence of real numbers, assigning a real number ai to each integer $i$ between $m$ and $n$ inclusive (i.e., $m \le i \le n$). Then we define the finite sum (or finite series) $ \sum_{i=m}^i a_i$ by the recursive formula $\sum_{i=m}^n a_i := 0$ whenever $n < m$; $\sum_{i=m}^{n + 1} a_i := (\sum_{i=m}^n + a_{n + 1})$ whenever $n \ge m − 1$.  

### Lemma 7.1.4  
(a) Let $m \le n < p$ be integers, and let $a_i$ be a real number assigned to each integer $m \le i \le p$. Then we have $\sum_{i=m}^p a_i + \sum_{i=n+1}^p a_i = \sum_{i=m}^p a_i$.  
* Use induction by $p - m = N$.  

(b) Let $m \le n$ be integers, $k$ be another integer, and let $a_i$ be a real number assigned to each integer $m \le i \le n$. Then we have $\sum_{i=m}^n a_i = \sum_{j=m+k}^{n+k} a_{j - k}$.  
