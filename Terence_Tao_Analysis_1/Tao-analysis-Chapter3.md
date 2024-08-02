# Chapter 3 Set theory  
## 3.1 Fundamentals  
### Axioms  
* 3.1 (Sets are objects). If $A$ is a set, then $A$ is also an object. In particular, given two sets $A$ and $B$, it is meaningful to ask whether $A$ is also an element of $B$.  
* 3.2 (Empty set). There exists a set $\varnothing$, known as the empty set, which contains no elements, i.e., for every object $x$ we have $x \in \varnothing$.  
* 3.3 (Singleton sets and pair sets). If $a$ is an object, then there exists $a$ set $\{a\}$ whose only element is $a$, i.e., for every object $y$, we have $y \in \{a\}$ if and only if $y = a$; we refer to $\{a\}$ as the singleton set whose element is $a$. Furthermore, if $a$ and $b$ are objects, then there exists a set $\{a, b\}$ whose only elements are $a$ and $b$; i.e., for every object $y$, we have $y \in \{a, b\}$ if and only if $y = a$ or $y = b$; we refer to this set as the pair set formed by $a$ and $b$.  
* 3.4 (Pairwise union). Given any two sets $A, B$, there exists a set $A ~\cup~ B$, called the union $A ~\cup~ B$ of $A$ and $B$, whose elements consists of all the elements which belong to $A$ or $B$ or both. In other words, for any object $x$, $x \in A ~\cup~ B \Leftrightarrow (x \in A \text{~or~} x \in B)$.  
* 3.5 (Axiom of specification). Let $A$ be a set, and for each $x \in A$, let $P(x)$ be a property pertaining to $x$ (i.e., $P(x)$ is either a true statement or a false statement). Then there exists a set, called $\{x \in A: P(x) \text{~is~true~}\}$ (or simply $\{x \in A:P(x)\}$ for short), whose elements are precisely the elements $x$ in $A$ for which $P(x)$ is true. In other words, for any object $y$, $y \in \{x \in A: P(x) \text{~is~true~}\} \Leftrightarrow (y \in A \text{~and~} P(y) \text{~is~true})$.  

### Definitions  
* 3.1.4 (Equality of sets). Two sets $A$ and $B$ are equal, $A = B$, iff every element of $A$ is an element of $B$ and vice versa. To put it another way, $A = B$ if and only if every element $x$ of $A$ belongs also to $B$, and every element $y$ of $B$ belongs also to $A$.  
* 3.1.15 (Subsets). Let $A, B$ be sets. We say that $A$ is a subset of $B$, denoted $A \subseteq B$, iff every element of $A$ is also an element of $B$, i.e. For any object $x, x \in A \Rightarrow x \in B$. We say that $A$ is a proper subset of $B$, denoted $A \subsetneq B$, if $A \subseteq B$ and $A \ne B$.  
* 3.1.23 (Intersections). The intersection $S_1 ~\cap~ S_2$ of two sets is defined to be the set $S_1 ~\cap~ S_2:= \{x \in S_1: x \in S_2\}$. In other words, $S_1 ~\cap~ S_2$ consists of all the elements which belong to both S1 and S2. Thus, for all objects $x, x \in S_1 ~\cap~ S_2 \Leftrightarrow x \in S_1 \text{~and~} x \in S_2$.  
* 3.1.27 (Difference sets). Given two sets $A$ and $B$, we define the set $A − B$ or $A / B$ to be the set $A$ with any elements of $B$ removed: $A / B:= \{x \in A : x \in B\}$.  

### Lemma 3.1.6 (Single choice). Let A be a non-empty set. Then there exists an object $x$ such that $x \in A$.
* Because the statment is that exists an object $x$ such that $x \in A$, so suppose that for every object $x$ have $x \notin A$, according to axiom 3.2, we could get $A$ is empty set, then have a contradiction, so this lemma is true.  

### Lemma 3.1.13. If $a$ and $b$ are objects, then $\{a, b\} = \{a\} ~\cup~ \{b\}$. If $A, B, C$ are sets, then the union operation is commutative (i.e., $A ~\cup~ B = B ~\cup~ A$) and associative (i.e., $(A ~\cup~ B) ~\cup~ C = A ~\cup~ (B ~\cup~ C)$). Also, we have $A ~\cup~ A = A ~\cup~ ∅ = ∅ ~\cup~ A = A$.  
* Commutative, if $x$ is any element of $A ~\cup~ B$, we get $x \in A$ or $x \in B$, then it also means $x \in B$ or $x \in A$, and by this way get $x \in B ~\cup~ A$, then we know the elements of $A ~\cup~ B$ is equal to $B ~\cup~ A$.  
* Associative: $(A ~\cup~ B) ~\cup~ C = A ~\cup~ B ~\cup~ C = A ~\cup~ (B ~\cup~ C)$.  
* Suppose we have $A ~\cup~ A$. Obviously $A ~\cup~ A = A$. If we have $A ~\cup~ ∅$, then $A ~\cup~ ∅ = ∅ ~\cup~ A$ according to commutative, and because no element in ∅, then $A ~\cup~ ∅ = A = A ~\cup~ A$.  

### Proposition 3.1.18 (Sets are partially ordered by set inclusion). Let $A,B,C$ be sets. If $A \subseteq B$ and $B \subseteq C$ then $A \subseteq C$. If $A \subseteq B$ and $B \subseteq A$, then $A = B$. Finally, if $A \subsetneq B$ and $B \subsetneq C$ then $A \subsetneq C$.  
* Suppose $A \subseteq B$ and $B \subseteq A$. If $A \ne B$, there exists some objects $x \in A$ and $x \notin B$ or $y \in B$ and $y \notin A$, whatever status will make a contradiction. Thus $A = B$.  
* Suppose $A \subsetneq B$ and $B \subsetneq C$. We already prove that $A \subseteq C$, just need prove that $A \ne C$. If $A = C$, we have $A \subsetneq B \Rightarrow C \subsetneq B$ and $B \subsetneq C$, which is a contradiction. Thus $A \subsetneq C$.  

### Proposition 3.1.28 (Sets form a boolean algebra). Let $A, B, C$ be sets,and let $X$ be a set containing $A, B, C$ as subsets.  
(a) (Minimal element) We have $A ~\cup~ \varnothing = A \text{~and~} A ~\cap~ \varnothing = \varnothing$.  
* $A ~\cap~ \varnothing$ means $x \in A$ and $x \in \varnothing$, because axiom 3.2, know that there is no element in $\varnothing$, so no element statisfy this property, then $A ~\cap~ \varnothing$ is a empty set, it means $A ~\cap~ \varnothing = \varnothing$.  

(b) (Maximal element) We have $A ~\cup~ X = X$ and $A ~\cap~ X = A$.  
* $\forall x \in A$, because $A \subset X$, then $x \in X$. Thus $x \in A$ and $x \in X$ is true, we have $A \subset A ~\cap~ X$.  

(c) (Identity) We have $A ~\cup~ A = A$ and $A ~\cap~ A = A$.  

(d) (Commutativity) We have $A ~\cup~ B = B ~\cup~ A$ and $A ~\cap~ B = B ~\cap~ A$.  

(e) (Associativity) We have $(A ~\cup~ B) ~\cup~ C = A ~\cup~ (B ~\cup~ C)$ and $(A ~\cap~ B) ~\cap~ C = A ~\cap~ (B ~\cap~ C)$.  

(f) (Distributivity) We have $A ~\cap~ (B ~\cup~ C) = (A ~\cap~ B) ~\cup~ (A ~\cap~ C)$ and $A ~\cup~ (B ~\cap~ C) = (A ~\cup~ B) ~\cap~ (A ~\cup~ C)$.  
* $\forall x \in A ~\cap~ (B ~\cup~ C) \Leftrightarrow x \in A$ and $x \in B ~\cup~ C \Leftrightarrow (x \in A$ and $x \in B)$ or $(x \in A \text{~and~} x \in C) \Leftrightarrow (A ~\cap~ B) ~\cup~ (A ~\cap~ C)$.  
* $\forall x \in A ~\cup~ (B ~\cap~ C) \Leftrightarrow x \in A$ or $x \in B ~\cap~ C \Leftrightarrow x \in A$ or $x \in A ~\cap~ B$ or $x \in A ~\cap~ C$ or $x \in B ~\cap~ C \Leftrightarrow x \in A ~\cup~ (A ~\cap~ B) ~\cup~ (A ~\cap~ C) ~\cup~ (B ~\cap~ C) \Leftrightarrow A ~\cup~ (A ~\cap~ B) ~\cup~ (C ~\cap~ (A ~\cup~ B)) \Leftrightarrow A ~\cup~ (A ~\cap~ B) ~\cup~ (C ~\cap~ (A ~\cup~ B))$

(g) (Partition) We have $A ~\cup~ (X / A) = X$ and $A ~\cap~ (X / A) = \varnothing$.  

(h) (De Morgan laws) We have $X / (A ~\cup~ B) = (X / A) ~\cap~ (X / B)$ and $X / (A ~\cup~ B) = (X / A) ~\cup~ (X / B)$.  

### Exercise 
* 3.1.1. Show that the definition of equality in Definition 3.1.4 is reflexive, symmetric, and transitive  
Use Definition 3.1.4 (Equality of sets). Two sets A and B are equal, A = B, iff every element of A is an element of B and vice versa. To put it another way, A = B if and only if every element x of A belongs also to B, and every element y of B belongs also to A.  
*Proof:* A = A is obviously true, so already be reflexive. And if A = B, then B = A. Accoding to Definition 3.1.4, so A and B have same element iff A = B, it's obviously B = A iff A and B have same element, so the symmetric is true. If A = B and B = C, then A = C. If A not equal to C, then A have element C not contain, and beacuse B = C, which means A have element B not contain, this is a contradiction to A = B, so transitive is true.  

* Using only Definition 3.1.4, Axiom 3.1, Axiom 3.2, and Axiom 3.3, prove that the sets ∅, {∅}, {{∅}}, and {∅, {∅}} are all distinct (i.e., no two of them are equal to each other).  
Axiom 3.1 (Sets are objects). If A is a set, then A is also an object. In particular, given two sets A and B, it is meaningful to ask whether A is also an element of B.  
*Proof*: Frist I want to show that ∅, {∅}, {{∅}}, and {∅, {∅}} exist. Because of axiom 3.2, ∅ exist and it's a object becuase of axiom 3.1. So use axiom 3.3, we can get {∅}, {{∅}}, and {∅, {∅}}. Second, ∅ can be thought a {} object, {∅}, {{∅}}, and {∅, {∅}} are sets contain elements, then ∅ is not equal to others. Skip the rest.  

* 3.1.3. Prove the remaining claims in Lemma 3.1.13.  
* 3.1.4. Prove the remaining claims in Proposition 3.1.18.  
* 3.1.5. Let A,B be sets. Show that the three statements A ⊆ B, A ∪ B = B, A ∩ B = A are logically equivalent (any one of them implies the other two).  
*Proof:* If A ⊆ B, it means every element in A is also in B, A ∪ B means that element in A or in B, because every element of A is in B, so every element in A ∪ B is in B, so get A ∪ B = B, and if A ∩ B not equal to A, means that A have some element not in B, this a contradiction to A ⊆ B, then we get A ∩ B = A. Skip the rest.  

* 3.1.6. Prove Proposition 3.1.28. (Hint: one can use some of these claims to prove others. Some of the claims have also appeared previously in Lemma 3.1.13.)  

* 3.1.7. Let A,B,C be sets. Show that A ∩ B ⊆ A and A ∩ B ⊆ B. Furthermore,show that C ⊆ A and C ⊆ B if and only if C ⊆ A ∩ B. In a similar spirit, show that A ⊆ A ∪ B and B ⊆ A ∪ B, and furthermore that A ⊆ C and B ⊆ C if and only if A ∪ B ⊆ C.  
*Proof:*  
It's obviously that if we get any element in A ∩ B, then immediately we can know that the element is in A and B. So get A ∩ B ⊆ A and A ∩ B ⊆ B.  
If C ⊆ A and C ⊆ B, it means every element in C is also in A and B, quickly implies that C ⊆ A ∩ B. Skip the rest.  
If A ⊆ C and B ⊆ C, it means that every element in A or every element in B, we can get the element is also in C, then A ∪ B ⊆ C. Skip the rest.  

* 3.1.8. Let A, B be sets. Prove the absorption laws A ∩ (A ∪ B) = A and A ∪ (A ∩ B) = A.  
*Proof:* If A ∩ (A ∪ B), we know A $\subset$ A ∪ B, so use (b) of Proposition 3.1.18, we get A ∩ (A ∪ B) = A. Obviously, A ∩ B $\subset$ A, by the same way, we get A ∪ (A ∩ B) = A.  

* 3.1.9. Let A,B,X be sets such that A ∪ B = X and A ∩ B = ∅. Show that A = X \ B and B = X \ A  
*Proof:* Use (g) and (h) of Proposition 3.1.18. It's obviously that A $\subset$ X and B $\subset$ X, beacuse of (g), quckily get A ∪ B = X = B ∪ X \ B, (B ∪ X \ B) \ B = (A ∪ B) \ B, ((X \ B) \ B) ∪ (B \ B) = (A \ B) ∪ (B \ B), Because A ∩ B = ∅, A \ B = A and (X \ B) \ B = X \ B is true, so get X \ B ∪ ∅ = A ∪ ∅, then X \ B = A. Skip the rest.  

* 3.1.10. Let A and B be sets. Show that the three sets A \ B, A ∩ B, and B \ A are disjoint, and that their union is A ∪ B.
*Proof:* Obviously, A \ B and A ∩ B are disjoint, B \ A and A ∩ B are also disjoint. Show that A \ B and B \ A are disjoint. It's obviously that any element in A \ B is not in B, but any element in B \ A is in B, so A \ B and B \ A are disjoint.  

* 3.1.11. Show that the axiom of replacement implies the axiom of specification.  
*Axiom 3.6 (Replacement).* Let A be a set. For any object x ∈ A, and any object y, suppose we have a statement P(x,y) pertaining to x and y, such that for each x ∈ A there is at most one y for which P(x,y) is true. Then there exists a set {y : P (x, y) is true for some x ∈ A}.  
*Axiom 3.5 (Axiom of specification).* Let A be a set, and for each x ∈ A, let P(x) be a property pertaining to x (i.e., P(x) is either a true statement or a false statement). Then there exists a set, called {x ∈ A : P(x) is true} (or simply {x ∈ A : P(x)} for short), whose elements are precisely the elements x in A for which P(x) is true.  
*Proof:* Let y is in A, assume exists such P(x,y) which statisfy axiom 3.6 that x not equal to y, so the condition "at most one y for which P(x,y)" will be a contradiction.Thought if x not equal y, P(x,y) also can be P(x,x) because x is also statisfy such property. Then we could find the P(x,y) actually is only decided by x and the property. So we get Axiom 3.5.  

## 3.2 Russell’s paradox (Optional)
### Exercises
* Show that the universal specification axiom, Axiom 3.8, if assumed to be true, would imply Axioms 3.2, 3.3, 3.4, 3.5, and 3.6. (If we assume that all natural numbers are objects, we also obtain Axiom 3.7.) Thus, this axiom, if permitted, would simplify the foundations of set theory tremendously (and can be viewed as one basis for an intuitive model of set theory known as “naive set theory”). Unfortunately, as we have seen, Axiom 3.8 is “too good to be true”!  
Use Axiom 3.8 (Universal specification). (Dangerous!) Suppose for every object x we have a property P(x) pertaining to x (so that for every x, P(x) is either a true statement or a false statement).  
Axiom 3.2. Let a such object x, its property is no element in x, and call x is empty set.  
Axiom 3.3. Let a,b are objects. First we can assign a such property to x, x only contain one of a and b. Second we can chage this property, x contain both a and b.  
Axiom 3.4. Let A,B are objects. Object x have such property that x contain all elements in a and b.  
Axiom 3.5. Let A are objects. X have such property that the element in X also statisfy P(A).  

* 3.2.2. Use the axiom of regularity (and the singleton set axiom) to show that if A is a set, then A $\notin$ A. Furthermore, show that if A and B are two sets, then either A $\notin$ B or B  $\notin$ A (or both).  
*Proof:* 
If A $\in$ A, use axiom 3.3, we have {A}, let {A} ∪ A = A, it's obviously contradiction to axiom 3.9.  
If A $\in$ B and B $\in$ A, A ∪ B = {A,B}, {A,B} just contain two sets, contradiction to axiom 3.9.  

* 3.2.3. Show (assuming the other axioms of set theory) that the universal specification axiom, Axiom 3.8, is equivalent to an axiom postulating the existence of a “universal set” Ω consisting of all objects (i.e., for all objects x, we have x ∈ Ω). In other words, if Axiom 3.8 is true, then a universal set ex- ists, and conversely, if a universal set exists, then Axiom 3.8 is true. (This may explain why Axiom 3.8 is called the axiom of universal specification). Note that if a universal set Ω existed, then we would have Ω ∈ Ω by Axiom 3.1, contradicting Exercise 3.2.2. Thus the axiom of foundation specifically rules out the axiom of universal specification.  
*Proof:*  
If universal specification axiom, then we can assign such property that contain all objects to a set, get the Ω set. If Ω exists, use axiom 3.5, we can assign any property to  the objects in Ω to get any sets, so we get axiom 3.8.   

## 3.3 Functions
### Lemma 3.3.12 (Composition is associative). Let f : Z → W, g : Y → Z, and h : X → Y be functions. Then f ◦ (g ◦ h)=(f ◦ g) ◦ h.  
* Use Definition 3.3.7 (Equality of functions). Two functions f:X→Y, g:X→Y with the same domain and range are said to be equal, f = g, if and only if f(x) = g(x) for all x ∈ X.  
* Definition 3.3.10 (Composition). Let f : X → Y and g : Y → Z be two functions, such that the range of f is the same set as the domain of g. We then define the composition g ◦ f : X → Z of the two functions g and f to be the function defined explicitly by the formula: $(g ◦ f)(x) := g(f(x))$  
* (f ◦ (g ◦ h))(x) = (f ◦ g ◦ h)(x) = ((f ◦ g) ◦ h)(x), so f ◦ (g ◦ h)=(f ◦ g) ◦ h.  

### Exercises  
* 3.3.1. Show that the definition of equality in Definition 3.3.7 is reflexive, symmetric, and transitive. Also verify the substitution property: if $f$,$f^o$:X→Y and $g$,$g^o$:Y →Z are functions such that f = $f^o$ and g = $g^o$, then $g$ ◦ $f$ = $g^o$ ◦ $f^o$.  
*Proof:*  
Let f,g,h be function, it's obvious that x = x, g = g, and h = h. If x = g, then g = x is also true obviuosly. If x = g and g = h, because f,g have same domain and range, g,h have same domain and range, so f,h have same domain and range. And get any x for f, we have f(x) = g(x), and because g = h, so we have g(x) = h(x), then f(x) = h(x). So transitive is true.  
Because f = $f^o$, then $g$ ◦ $f$ = $g$ ◦ $f^o$, Beacuse g = $g^o$, $g$ ◦ $f^o$ = $g^o$ ◦ $f^o$, so we get $g$ ◦ $f$ = $g^o$ ◦ $f^o$.  

* 3.3.2. Let f : X → Y and g : Y → Z be functions. Show that if f and g are both injective, then so is g ◦ f, similarly, show that if f and g are both surjective, then so is g ◦ f.  
*Proof:*  
Use Definition 3.3.14 (One-to-one functions). A function f is one-to-one (or injective) if different elements map to different elements.  
Use Definition 3.3.17 (Onto functions). A function f is onto (or surjective) if f(X) = Y , i.e., every element in Y comes from applying f to some element in X.  
Let x,y are different elements, then f(x),f(y) is different, and g is injective, so g(f(x)),g(f(y)) is different, then we know different x and y, g ◦ f map different elements, so g ◦ f is injective.  
Let g:Y -> Z, f:X -> Y, beacuse g is onto, g(Y) = Z, and f(X) = Y, use substitution, then g(f(X)) = Z, so we get (g ◦ f)(X) = Z, then g ◦ f is onto.  

* 3.3.3. When is the empty function injective? surjective? bijective?  
Example 3.3.9. A rather boring example of a function is the empty function f : ∅ → X from the empty set to an arbitrary set X. Since the empty set has no elements, we do not need to specify what f does to any input. Nevertheless, just as the empty set is a set, the empty function is a function, albeit not a particularly interesting one. Note that for each set X, there is only one function from ∅ to X, since Definition 3.3.7 asserts that all functions from ∅ to X are equal (why?).  
Test to explain the 'why', every function from ∅ to X have same domain and range, then verify that f(x) = g(x) for all x ∈ ∅. Because there is no element in ∅, this is vacuously true. So all functions are equal.  
*Speculation:* 
Function is injective means that different x in domain map to different y in range. ∅ have no elements means that there no different elements in domain, so that if there is no different element in range, it may be injective. Then suppose a function f: ∅->∅. This may be also true for bijective.  
Function is surjective means that every element in range can map to element in domain. It seems be vacuously true because there is no elements in empty set.  

* 3.3.4. In this section we give some cancellation laws for composition. Let f:X→Y, $f^o$:X→Y, g:Y→Z, and $g^o$:Y→Z be functions. Show that if g ◦ f = g ◦ $f^o$ and g is injective, then f = $f^o$. Is the same statement true if g is not injective? Show that if g ◦ f = $g^o$ ◦ f and f is surjective, then g = $g^o$. Is the same statement true if f is not surjective?  
*Proof:*  
If g ◦ f = g ◦ $f^o$, g ◦ f and g ◦ $f^o$ have same domain and range, so that f and $f^o$ have same domain. (g ◦ f)(x) = (g ◦ $f^o$)(x), g(f(x)) = g($f^o$(x)), g is injective, then f(x) = $f^o$(x), so f and $f^o$ have same range and for every x have f(x) = $f^o$(x). If g is not injective, there may be have two different element let g(x) = g($x^o$), even f and $f^o$ have same different domain, them may have different range, this can also make g ◦ f = g ◦ $f^o$.  
If g ◦ f = $g^o$ ◦ f, and f have same domain and g(f(X)) = $g^o$(f(X)), then g and $g^o$ have same domain and range. For every element in X, we have f(x) = f(x) and g(f(X)) = $g^o$(f(X)), it's obviously whatever function f is, g must equal to $g^o$.  

* 3.3.5. Let f : X → Y and g : Y → Z be functions. Show that if g ◦ f is injective, then f must be injective. Is it true that g must also be injective? Show that if g ◦ f is surjective, then g must be surjective. Is it true that f must also be surjective?  
*Proof:*  
If f is not injective, there has f(x) = f($x^o$), then g(f(x)) = g(f($x^o$)), this is a contradiction. If g is not injective and f is injective, let g(y) = g($y^o$) and y is not equal $y^o$, then if y = f(x) and $y^o$ = f($x^o$), obviously that x is not equal to $x^o$, but we also have g(f(x)) = g(f($x^o$)), so that g must be injective.  
If g is not surjective, not every element in range could find a element in domain of g, so that g ◦ f would be not surjective, this is a contradiction. If g is surjective and f is not surjective, every element in range of g could find a f(x) map to, if the f(x) exist no matter what function f is, we could find a element in domain of f. Then we have every element in range of g ◦ f, we could find a element map to in domain of g ◦ f. Then f is not must be surjective.  

* 3.3.6. Let f : X → Y be a bijective function, and let $f^{−1}$ : Y → X be its inverse. Verify the cancellation laws $f^{−1}$(f(x)) = x for all x ∈ X and f($f^{−1}$(y)) = y for all y ∈ Y . Conclude that $f^{−1}$ is also invertible, and has f as its inverse (thus $(f^{−1})^{−1}$ = f).  
Use definition of bijective, If f is bijective, then for every y ∈ Y , there is exactly one x such that f(x) = y. This value of x is denoted $f^{−1}$(y); thus $f^{−1}$ is a function from Y to X. We call $f^{−1}$ the inverse of f.  
*Proof:*  
Let x is any element in X, and have f(x) = y, according to the definition, then we have $f^{−1}$(y) = x, use substitution, we have $f^{−1}$(f(x)) = x. Similarly, we can prove f($f^{−1}$(y)) = y.  
Obviously $(f^{−1})^{−1}$ and f have same domain and range.  Let g = $f^{-1}$, g also is bijective, obviously g($g^{−1}$(x)) = x, and we have g($f$(x)) = x, becuase g is injective, then $g^{-1}$ = f, use subtitution, get $(f^{−1})^{−1}$ = f.  

* 3.3.8. If X is a subset of Y , let ιX→Y : X → Y be the inclusion map from X to Y, defined by mapping x → x for all x ∈ X,i.e.,ιX→Y(x):=x for all x ∈ X. The map ιX→X is in particular called the identity map on X.  
(a)Show that if X ⊆ Y ⊆ Z then ιY → Z ◦ ιX → Y = ιX → Z.  
*Proof:* let g = ιX → Y, f = ιY → Z, h = ιX → Z. According to the definition, we have g(X) = X, f(Y) = Y, h(X) = X. Because g(X) = X and X ⊆ Y, then f ◦ g(X) = X and h(X) = X, so we get f ◦ g = h.  
(b) Show that if f : A → B is any function, then f = f ◦ ιA→A = ιB→B ◦ f.  
*Proof:* For f ◦ ιA→A, ιA→A(x) = x, then (f ◦ ιA→A)(x) = f(x). For ιB→B ◦ f, ιB→B(y) = y, then (ιB→B ◦ f)(x) = ιB→B(f(x)) = f(x).  Then we get f = f ◦ ιA→A = ιB→B ◦ f.  
(c) Show that, if f : A → B is a bijective function, then f ◦ $f^{−1}$ = ιB→B and $f^{−1}$ ◦ f = ιA→A.  
*Proof:* Skiped.  
(d) Show that if X and Y are disjoint sets,and f:X → Z and g:Y → Z are functions, then there is a unique function h: X ∪ Y → Z such that h ◦ ιX→X∪Y = f and h ◦ ιY→X∪Y = g.  
*Proof:* Let h(X) = f(X) and h(Y) = g(Y). Beacuse X ⊆ X ∪ Y and Y ⊆ X ∪ Y, use the conclusion in (b), (h ◦ ιX→X∪Y)(X) = h(X) = f(X) and (h ◦ ιY→X∪Y)(Y) = h(Y) = g(Y).  

## 3.4 Images and inverse images  
### Definition 3.4.1 (Images of sets). If f : X → Y is a function from X to Y , and S is a set in X, we define f(S) to be the set,  f(S) := {f(x) : x ∈ S}.  
`Ex: Note that the set f(S) is well-defined thanks to the axiom of replacement (Axiom 3.6). One can also define f(S) using the axiom of specification (Axiom 3.5) instead of replacement, but we leave this as a challenge to the reader.`  
*Thought:*  In the condition, If we have f, X and Y. In my personal opinion, if we have Y, we can assign the f(x) = y is a property Q(n), so according to 3.5 axiom, Y is a set we can get such elements in Y which is statisfy Q(n) to bulid a set f(S).    

### Lemma 3.4.9. Let X be a set. Then the set  $Y: Y\subset X$ is a set.  
*Thought:*  This means all subsets of X together is a set. Obviously, the author want us to use axiom 3.10, so I guess that use 3.10 that can immediately get a set which is consists of all $X^X$ functions. So, the range of function is subset of X, in another words, we may use some way to get all subset of X from this set of funcions.  

### Exercise  
* 3.4.1 Let f : X → Y be a bijective function, and let $f^{−1}$ : Y → X be its inverse. Let V be any subset of Y. Prove that the forward image of V under $f^{−1}$ is the same set as the inverse image of V under f; thus the fact that both sets are denoted by $f^{−1}(V)$ will not lead to any inconsistency.  
*Proof:*  
Use the definition, we can get $f^{−1}(V)$ is such set F $(x \in V \ and \ f^{−1}(x))$, and the inverse iamge of V is I $(x \in X \ and \ f(x) \in V)$.   
Let guess that f(I) and f(F). I is all the elements in X which statisfy $f(x) \in V$, because of bijective, every element in V is maped to a element of X, I is all of elements which $f(x) \in V$, thus f(I) = V. Next is F, F is consist of elements in X, which is every $y \in V$ and $f^{-1}(y)$ is mapped to, and f(F) is every $y \in Y$ is mapped to $x \in F$ by f, use bijective, get f(F) = V. Then f(F) = f(I), I = F.  

* 3.4.2 Let f : X → Y be a function from one set X to another set Y , let S be a subset of X, and let U be a subset of Y. What, in general, can one say about $f^{−1}(f(S))$ and S? What about $f(f^{−1}(U))$ and U?  
*Proof*: For a in $f^{−1}(f(S))$, by definition, is that $(x \in X: f(x) \in f(S))$, choose x from X, which has such property of f(x) = a and a is in f(S). If have such a set $S^o(x\in X:x\in S)$, we can easily find every element in $S^o$ could be statisfied such property of f(x) = a and a in f(S), so we get $S \subseteq f^{−1}(f(S))$.  
For a in $f(f^{−1}(U))$, by definition, is that $(f(y): y \in (x \in X: f(x) \in U))$, for any a, if there in X exists one y, we could find such y which statisfy property of $f(y) \in U$ and $y \in X$, so we could get $f(y) \in U$ from $f(f^{−1}(U))$. Then we have $f(f^{−1}(U)) \subseteq U$.  


## 3.5 Cartesian products

### Exercise
* 3.5.10 If f : X → Y is a function, define the graph of f to be the subset of X × Y defined by {(x, f(x)) : x ∈ X}. Show that two functions f:X→Y, $f^o$ :X→Y are equal if and only if they have the same graph. Conversely, if G is any subset of X × Y with the property that for each x ∈ X, the set {y ∈ Y : (x,y) ∈ G} has exactly one element (or in other words, G obeys the vertical line test), show that there is exactly one function f : X → Y whose graph is equal to G.  
*Proof:* Frist, if f and $f^o$ is equal, for any x in their domain X, have $f(x) = f^o(x)$, then for any $(x,f(x))$ and $(x,f^o(x))$ also equal, which means their graph is equal. Conversely, we can induce $f = f^o$ from graph equal.  
Second, 

* 3.5.11 Show that Axiom 3.10 can in fact be deduced from Lemma 3.4.9 and the other axioms of set theory, and thus Lemma 3.4.9 can be used as an alternate formulation of the power set axiom. (Hint: for any two sets X and Y, use Lemma 3.4.9 and the axiom of specification to construct the set of all subsets of X × Y which obey the vertical line test. Then use Exercise 3.5.10 and the axiom of replacement.)  
*Proof:*  

## 3.6. Cardinality of sets  

### Remark 3.6.3 Explain why the map f:X→Y defined by f(n):=2n is a bijection from X to Y, for X is the set of N and Y is the set of even N.  
* First, show the function is injection. For every x, $x^o$ in X, if x is equal to $x^o$, then f(x) = 2x = 2$x^o$ = f($x^o$), so the function is injection. Second, show the function is surjection. The set of even natural number is f(N), so that for every y in Y, we could find at least a number in X(My thought is that use induction could prove this one).  

### Proposition 3.6.4. Let X, Y, Z be sets. Then X has equal cardinality with X. If X has equal cardinality with Y , then Y has equal cardinality with X. If X has equal cardinality with Y and Y has equal cardinality with Z, then X has equal cardinality with Z.  
* Essentially, the equal cardinality is bijection between two sets. So if X and Y have a relationship about bijection, Y and Z also have a such relationship, it's obvious that X and Z could have such a bijection between them, so we prove X has equal cardinality with Z.  

### Remark 3.6.6 Explain why the set {i ∈ N : i < n} and the set {i ∈ N : 1 ≤ i ≤ n} have equal cardinality.  
* Let such function f:X→Y defined by f(n) = n + 1, X is the set {i ∈ N : i < n} and Y is the set {i ∈ N : 1 ≤ i ≤ n}. Obviously, the function is bijection, so that X and Y have equal cardinality.  

### Lemma 3.6.9. Suppose that n ≥ 1, and X has cardinality n. Then X is non-empty, and if x is any element of X, then the set X − {x} (i.e., X with the element x removed ) has cardinality n − 1.  
`Explain why there is no bijection from the empty set to a non-empty set.`  
* Thought: Beacuse bijection is a one-to-one and onto function between two sets, empty set has no element, so that empty set has no element could map to element in non-empty set, then we can not find such a function is bijection between empty set and a non-empty set`  
`We have a bijection f from X to {i ∈ N : 1 ≤ i ≤ N}, now define the function g : X − {x} to {i ∈ N:1 ≤ i ≤ n−1} by the following rule: for any y ∈ X − {x}, we define g(y) := f(y) if f(y) < f(x), and define g(y) := f(y) − 1 if f(y) > f(x). Check g is a bijection function.`  
* In X, if we removed $x^o$ and we could easily create another function $f^o$ which domain is X - {x} but $f^o(x) = f(x)$, when X mapped to N under $f^o$, we can see such forward image $1 \leq f(x) < f(x^o) \ and \ f(x^o) < f(x) \leq N$, when y in X - {x} statisfied f(y) < f(x) under g, g is equal to f which is bijection and range is $1 \leq f(x) < f(x^o)$, and when y statisfied f(y) > f(x), g is equal to f(x) - 1 which is also bijection and range is $f(x^o) \leq f(x) \leq N - 1$, so that the range of X - {x} under g is $1 \leq g(y) \leq N - 1$, and g is bijection, then X - {x} has cardinality n - 1.  

### Theorem 3.6.12. The set of natural numbers N is infinite.  
* If N is finite, so it has a sure cardinality $n^o$ which means it has a bijection mapped to $N^o$ and $n^o$ is a natural number, but according to the definition of N, every natural number n in N has its sucessor n++, so that $n^o++$ is in N but not in $N^o$, contradction.  

### Proposition 3.6.14 (Cardinal arithmetic).
* (a) If X be a finite set, there is a bijection f between X and $1 \leq n \leq$ #$(X)$. If there has X ∪ {x}, we could create a function g mapped to $1 \leq n \leq$ #$(X) + 1$. If y is in X, g(y) = f(y). If y = x, g(y) = #(X) + 1. Obviously, g is a bijection. Then X ∪ {x} is finite and #(X ∪ {x}) = #(X) + 1. If X be empty set, obviously X ∪ {x} = {x}, and the set {x} is finite and #(X ∪ {x}) = #({x}) = 1 = 0 + 1 = #(X) + #({x}).
* (b) X ∪ Y could be equal to $X/(X \cap Y) + X \cap Y + Y/(X \cap Y)$. Let suppose X has cardinality x, Y has cardinality y, and $X \cap Y$ has n elements, use lemma 3.6.9 we could get $X/(X \cap Y)$ cardinality x - n, and $Y/(X \cap Y)$ cardinality y - n, use (a) we could know that $X \cap Y$ cardinality n. Use (a) again we could know that #$(X/(X \cap Y) + X \cap Y + Y/(X \cap Y)) = x - n + n + y - n = x + y - n$. Obviously $x + y - n \leq x + y$, when n is equal to 0, that $x + y - n = x + y$, which means that X and Y are disjoint.  
* (c) If $Y \subseteq X$, then $Y \cup (X/Y) = X$. Obviously,$\#(Y) \leq \#(Y) + \#(X/Y)$. Use (b) we have $\#(Y) + \#(X/Y) \leq \#(Y \cup (X/Y) = \#(X))$, then we have $\#(Y) \leq\#(X)$. If $Y \neq X$, which means that $\#(X/Y) \neq 0$, then $\#(Y) < \#(Y) + \#(X/Y) \le \#(Y \cup (X/Y)) = \#(X)$, then $\#(Y) < \#(X)$.  
* (d) Suppose X has cardinality x, we could have such a bijection $b(n)$ from N mapped to X. Obviously, we could have such set $B$ {b(n):$1\le n \le \#(X)$} equal to X. So from 1 to #(X), $f(B) = f(X)$, with using (a) we could combine elements from f(b(n)) one by one, so the f(X) is finite. Then $\#(f(X)) = \#(f(b(n_1)) \cup f(b(n_2))...... \cup f(b(n_{\#(X)}))) \le \#(f(b(n_1))) + \#(f(b(n_2))) + ...... + \#(f(b(n_{\#(X)}))) = \#(X)$, we could get $\#(f(X)) \le \#(X)$.  
* (e) $X$ x $Y$ = {$(x,y):x\in X \ and \ y\in Y$} = $\bigcup${$(x,y_i):x \in X, 1 \le i \le \#(Y)$}, let $Y_i = ((x,y_i):x \in X, 1 \le i \le \#(Y))$, then $\#(X$x$Y) = \#(Y_1 \cup Y_2 .... \cup Y_{\#(Y)})$. Obviously $Y_1......Y_{\#(Y)}$ is disjoint with each other, so $\#(X$x$Y) = \#(Y_1 \cup Y_2 .... \cup Y_{\#(Y)}) = \#(Y_1) + \#(Y_2) + ......+ \#(Y_{\#(Y)})$. It's easy to find a bijection from $X$ to $Y_i$, then $\#(Y_i) = \#(X)$. So that we get $\#(X$x$Y)$ = $\#(Y_1) + \#(Y_2) + ......+ Y_{\#(Y)} = \#(X)$x$\#(Y)$.  
* (f) If X,Y are finite, we could assign x,y cardinality to X,Y respectively. According to the definition of cardinality, we could assign a serial number to every element in X. Yet in this way, we could see there has a bijection function $g(i) = x_i$ where we could assign a serial number to every element in X. Now for every function f in $Y^X$, could be converted to a new function $\phi(i)$ in $Y^N$. Because of ordered pair, We could assign $(y)_{1 \le i \le \#(X)}:y \in Y$ to represent every $\phi(i)$ which is one-to-one mapped to every f.According to the definition of cartesian products, this is equal to $Y$x$Y$....x$Y$, and use (e) we could have $\#($$Y$x$Y$....x$Y)$ = $\#(Y)$x$\#(Y)$.....x$\#(Y)$ = $y^x$ = $\#(Y)^{\#(X)}$.  

### Exercises  
* 3.6.1 Prove Proposition 3.6.4, please see the previous in proposition 3.6.4.  
* 3.6.2 If X has cardinality 0, according to the definition of cardinality, it has no element in X, so X is empty set.  
* 3.6.3 If n is equal to 0, the 3.6.3 will be vacuously true. If n is 1, there has just one element and suppose f(1) = j, j is natural number, we could find j++ is larger than j, then $f(i) \le j$ is true. Suppose when n = p is true(in this situation, f(i) is less than or equal to M), show that p++ is true. Let f(p++) = k, if $k \le M$, then we could say $f(i) \le M \ for \ 1 \le i \le p++$, if $M \le k$, we will find $k\le k++$, then $f(i) \le k \ for \ 1 \le i \le p++$. If there is a finite subset of N, we could say this set A has m cardinality, which means A has a bijection g to B={$i \in N:1 \le i \le n$} for some natural number n. And $g^{-1}$ is from B to A, obviously $g^{-1}(B) = A \in N$, now we could say $g^{-1}(i) \le M \ for\  1 \le i \le n$ which means A is bounded.  
* 3.6.4 Prove Proposition 3.6.14, see the previous.  
* 3.6.5 Let a is any element in A, b is any element in B. We have (a ,b) in A x B and (b,a) in B x A. Consider such function f((a,b)) = (b,a) is a bijection. If $(a^o,b^o) = (a,b)$, $f((a^o,b^o)) = f((a,b))$, f is injective. Obviously, for any (b,a) in B x A, we could find a (a,b) in A x B, the f is surjection and bijection.   
* 3.6.6 Sorry, have no idea about this question.  
* 3.6.7 If $\#(A) \le \#(B)$, by defintion we could say #(A) = a and #(B) = b, so A and B are finite sets. Suppose g is bijection from N to a and f is bijection from N to b. Suppose such function h(A) = $f(g^-1(A))$, it's easy to find h is a injection from A to B, then we could say A and B are finite sets, then A has lesser or equal cardinality to B.  
* 3.6.8 No idea  
* 3.6.9 Suppose #(A) = a,#(B) = b, and $\#(A \bigcap B) = k$. $A \bigcup B = A/A \bigcap B + A \bigcap B + B/A \bigcap B$. Use (a) of proposition 3.6.14 could prove $\#(A/A \bigcap B)= \#(A) - \#(A \bigcap B)$. Then $\#(A \bigcap B) + \#(A \bigcup B) = \#(A \bigcap B) + \#(A/A \bigcap B + A \bigcap B + B/A \bigcap B) = \#(A \bigcap B) + \#(A) - \#(A \bigcap B) + \#(A \bigcap B) + \#(B) - \#(A \bigcap B) = k + a - k + b - k = a + b = \#(A) + \#(B)$.  
* 3.6.10 Use (b) of proposition 3.6.14, then $\#(\bigcup_{i \in (1,....,n)}A_i) = \#(A_1 \bigcup A_2.......\bigcup A_n) \le \#(A_1)+.....+ \#(A_n)$, and $\#(\bigcup_{i \in (1,....,n)}A_i) > n$, so $\#(A_1)+.....+ \#(A_n) > n$, If there does not exist i ∈ {1,...,n} such that $\#(A_i) ≥ 2$, then every $\#(A_i)\le 1$, obviously $\#(A_1)+.....+ \#(A_n) \le n$, it's a contradiction.  