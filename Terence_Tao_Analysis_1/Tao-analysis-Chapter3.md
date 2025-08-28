# Chapter 3 Set theory  
## 3.1 Fundamentals  
### Axioms  
* 3.1 (Sets are objects). If $A$ is a set, then $A$ is also an object. In particular, given two sets $A$ and $B$, it is meaningful to ask whether $A$ is also an element of $B$.  
* 3.2 (Empty set). There exists a set $\varnothing$, known as the empty set, which contains no elements, i.e., for every object $x$ we have $x \in \varnothing$.  
* 3.3 (Singleton sets and pair sets). If $a$ is an object, then there exists $a$ set $\lbrace a \rbrace$ whose only element is $a$, i.e., for every object $y$, we have $y \in \lbrace a \rbrace$ if and only if $y = a$; we refer to $\lbrace a \rbrace$ as the singleton set whose element is $a$. Furthermore, if $a$ and $b$ are objects, then there exists a set $\lbrace a, b \rbrace$ whose only elements are $a$ and $b$; i.e., for every object $y$, we have $y \in \lbrace a, b \rbrace$ if and only if $y = a$ or $y = b$; we refer to this set as the pair set formed by $a$ and $b$.  
* 3.4 (Pairwise union). Given any two sets $A, B$, there exists a set $A \ \cup\  B$, called the union $A \ \cup\  B$ of $A$ and $B$, whose elements consists of all the elements which belong to $A$ or $B$ or both. In other words, for any object $x$, $x \in A \ \cup\  B \Leftrightarrow (x \in A \text{ \ or \ } x \in B)$.  
* 3.5 (Axiom of specification). Let $A$ be a set, and for each $x \in A$, let $P(x)$ be a property pertaining to $x$ (i.e., $P(x)$ is either a true statement or a false statement). Then there exists a set, called $\lbrace x \in A: P(x) \text{\ is\ true\ } \rbrace$ (or simply $\lbrace x \in A:P(x) \rbrace$ for short), whose elements are precisely the elements $x$ in $A$ for which $P(x)$ is true. In other words, for any object $y$, $y \in \lbrace x \in A: P(x) \text{\ is\ true\ } \rbrace \Leftrightarrow (y \in A \text{\ and\ } P(y) \text{\ is\ true})$.  
* 3.6 (Replacement). Let $A$ be a set. For any object $x \in A$, and any object $y$, suppose we have a statement $P(x, y)$ pertaining to $x$ and $y$, such that for each $x \in A$ there is at most one $y$ for which $P(x, y)$ is true. Then there exists a set $\lbrace y : P(x, y) \text{\ is\ true\ for\ some\ } x \in A \rbrace$, such that for any object $z, z \in \lbrace y: \exists x \in A \  st.\ P(x, y) \rbrace \Leftrightarrow P(x, z) \text{\ is\ true\ for\ some\ } x \in A$

### Definitions  
* 3.1.4 (Equality of sets). Two sets $A$ and $B$ are equal, $A = B$, iff every element of $A$ is an element of $B$ and vice versa. To put it another way, $A = B$ if and only if every element $x$ of $A$ belongs also to $B$, and every element $y$ of $B$ belongs also to $A$.  
* 3.1.15 (Subsets). Let $A, B$ be sets. We say that $A$ is a subset of $B$, denoted $A \subseteq B$, iff every element of $A$ is also an element of $B$, i.e. For any object $x, x \in A \Rightarrow x \in B$. We say that $A$ is a proper subset of $B$, denoted $A \subsetneq B$, if $A \subseteq B$ and $A \ne B$.  
* 3.1.23 (Intersections). The intersection $S_1 \ \cap\  S_2$ of two sets is defined to be the set $S_1 \ \cap\  S_2:= \lbrace x \in S_1: x \in S_2 \rbrace$. In other words, $S_1 \ \cap\  S_2$ consists of all the elements which belong to both S1 and S2. Thus, for all objects $x, x \in S_1 \ \cap\  S_2 \Leftrightarrow x \in S_1 \text{\ and\ } x \in S_2$.  
* 3.1.27 (Difference sets). Given two sets $A$ and $B$, we define the set $A − B$ or $A / B$ to be the set $A$ with any elements of $B$ removed: $A / B:= \lbrace x \in A : x \notin B \rbrace$.  

### Lemma 3.1.6 (Single choice). Let A be a non-empty set. Then there exists an object $x$ such that $x \in A$.
* Because the statment is that exists an object $x$ such that $x \in A$, so suppose that for every object $x$ have $x \notin A$, according to Axiom 3.2, we could get $A$ is empty set, then have a contradiction, so this lemma is true.  

### Lemma 3.1.13. If $a$ and $b$ are objects, then $\lbrace a, b \rbrace = \lbrace a \rbrace \ \cup\  \lbrace b \rbrace$. If $A, B, C$ are sets, then the union operation is commutative (i.e., $A \ \cup\ B = B \ \cup\ A$) and associative $(i.e., \  (A \ \cup\  B) \ \cup\  C = A \ \cup\  (B \ \cup\ C))$. Also, we have $A \ \cup\ A = A \ \cup\ \varnothing = \varnothing \ \cup\ A = A$.  
* Commutative, if $x$ is any element of $A \ \cup\  B$, we get $x \in A$ or $x \in B$, then it also means $x \in B$ or $x \in A$, and by this way get $x \in B \ \cup\  A$, then we know the elements of $A \ \cup\  B$ is equal to $B \ \cup\  A$.  
* Associative: $(A \ \cup\  B) \ \cup\  C = A \ \cup\  B \ \cup\  C = A \ \cup\  (B \ \cup\ C)$.  
* Suppose we have $A \ \cup\  A$. Obviously $A \ \cup\  A = A$. If we have $A \ \cup\  \varnothing$, then $A \ \cup\  \varnothing = \varnothing \ \cup\  A$ according to commutative, and because no element in $\varnothing$, then $A \ \cup\  \varnothing = A = A \ \cup\  A$.  

### Proposition 3.1.18 (Sets are partially ordered by set inclusion). Let $A,B,C$ be sets. If $A \subseteq B$ and $B \subseteq C$ then $A \subseteq C$. If $A \subseteq B$ and $B \subseteq A$, then $A = B$. Finally, if $A \subsetneq B$ and $B \subsetneq C$ then $A \subsetneq C$.  
* Suppose $A \subseteq B$ and $B \subseteq A$. If $A \ne B$, there exists some objects $x \in A$ and $x \notin B$ or $y \in B$ and $y \notin A$, whatever status will make a contradiction. Thus $A = B$.  
* Suppose $A \subsetneq B$ and $B \subsetneq C$. We already prove that $A \subseteq C$, just need prove that $A \ne C$. If $A = C$, we have $A \subsetneq B \Rightarrow C \subsetneq B$ and $B \subsetneq C$, which is a contradiction. Thus $A \subsetneq C$.  

### Proposition 3.1.28 (Sets form a boolean algebra). Let $A, B, C$ be sets,and let $X$ be a set containing $A, B, C$ as subsets.  
(a) (Minimal element) We have $A \ \cup\  \varnothing = A \text{\ and\ } A \ \cap\  \varnothing = \varnothing$.  
* $A \ \cap\  \varnothing$ means $x \in A$ and $x \in \varnothing$, because axiom 3.2, know that there is no element in $\varnothing$, so no element statisfy this property, then $A \ \cap\  \varnothing$ is a empty set, it means $A \ \cap\  \varnothing = \varnothing$.  

(b) (Maximal element) We have $A \ \cup\  X = X$ and $A \ \cap\  X = A$.  
* $\forall x \in A$, because $A \subset X$, then $x \in X$. Thus $x \in A$ and $x \in X$ is true, we have $A \subset A \ \cap\  X$.  

(c) (Identity) We have $A \ \cup\  A = A$ and $A \ \cap\  A = A$.  

(d) (Commutativity) We have $A \ \cup\  B = B \ \cup\  A$ and $A \ \cap\  B = B \ \cap\  A$.  

(e) (Associativity) We have $(A \ \cup\  B) \ \cup\  C = A \ \cup\  (B \ \cup\  C)$ and $(A \ \cap\  B) \ \cap\  C = A \ \cap\  (B \ \cap\  C)$.  

(f) (Distributivity) We have $A \ \cap\  (B \ \cup\  C) = (A \ \cap\  B) \ \cup\  (A \ \cap\  C)$ and $A \ \cup\  (B \ \cap\  C) = (A \ \cup\  B) \ \cap\  (A \ \cup\  C)$.  
* $\forall x \in A \ \cap\  (B \ \cup\  C) \Leftrightarrow x \in A$ and $x \in B \ \cup\  C \Leftrightarrow (x \in A$ and $x \in B)$ or $(x \in A \text{\ and\ } x \in C) \Leftrightarrow (A \ \cap\  B) \ \cup\  (A \ \cap\  C)$.  
* $\forall x \in A \ \cup\  (B \ \cap\  C) \Leftrightarrow x \in A$ or $x \in B \ \cap\  C \Leftrightarrow x \in A$ or $x \in A \ \cap\  B$ or $x \in A \ \cap\  C$ or $x \in B \ \cap\  C \Leftrightarrow x \in A \ \cup\  (A \ \cap\  B) \ \cup\  (A \ \cap\  C) \ \cup\  (B \ \cap\  C) \Leftrightarrow A \ \cup\  (A \ \cap\  B) \ \cup\  (C \ \cap\  (A \ \cup\  B)) \Leftrightarrow A \ \cup\  (A \ \cap\  B) \ \cup\  (C \ \cap\  (A \ \cup\  B)) \Leftrightarrow  (A \ \cap\  A) \ \cup\  (A \ \cap\  B) \ \cup\  (C \ \cap\  (A \ \cup\  B)) \Leftrightarrow (A \ \cap\  (A \ \cup\  B)) \ \cup\  (C \ \cap\  (A \ \cup\  B)) \Leftrightarrow (A \ \cap\  B) \ \cup\  (A \ \cap\  C)$.  

(g) (Partition) We have $A \ \cup\  (X / A) = X$ and $A \ \cap\  (X / A) = \varnothing$.  
* Suppose $A \ \cup\  (X / A) \ne X$, then $\exists x \in X \ st. \ x \notin A \ \cup\  (X / A)$. If $x \notin A$, and we have $x \in X$ then $x \in X / A$ which is a contradiction(also $x \notin X / A$). If $x \notin X / A$, then $x \in A$, which also a contradcition(also $x \notin A$).  

(h) (De Morgan laws) We have $X / (A \ \cup\  B) = (X / A) \ \cap\  (X / B)$ and $X / (A \ \cap\  B) = (X / A) \ \cup\  (X / B)$.  
* $\forall x \in X / (A \ \cup\  B) \Leftrightarrow x \in X$ and $x \notin A \ \cup\  B$, because $X$ contain the elements of $A \ \cup\  B$, which means that $X$ will remove the elements of $A$ and the elements of $B$, thus $x \notin A$ and $x \notin B$, we could get $X / (A \ \cup\  B) = (X / A) \ \cap\  (X / B)$.  
* $\forall x \in (X / A) \ \cup\  (X / B)$, suppose $x \in X / A$ with generality, then $x \in X$ and $x \notin A$, since $A = (A / B) \cup (A \cap B)$ we could get $x \notin A \cap B$. Thus $x \in X / (A \cap B)$.  
* $\forall x \in X / (A \ \cap\  B) \Rightarrow x \in X$ and $x \notin A \cap B$, because $A \subseteq X$ we could say $x \in A$ or $x \in X / A$ then we have $X / (A \ \cap\  B) \Rightarrow (A \ \cup \ X / A) / (A \ \cap\  B) \Rightarrow x \in A$ and $x \notin A \cap B$ ,or $x \in X / A$ and $x \notin A \cap B \Rightarrow x \in X / A$. Similarly, we could also get $x \in X / B$ from $x \in X / (A \ \cap\  B)$. Thus $X / (A \ \cap\  B) \Rightarrow (X / A) \cup (X / B)$.  

### Exercises 
Exercise 3.1.1. Show that the definition of equality in Definition 3.1.4 is reflexive, symmetric, and transitive.  
* $A = A$ is obviously true, so already be reflexive. And if $A = B$, then $B = A$. Accoding to Definition 3.1.4, so $A$ and $B$ have same element iff $A = B$, it's obviously $B = A$ iff $A$ and $B$ have same element, so the symmetric is true. If $A = B$ and $B = C$, then $A = C$. If A not equal to C, then $A$ have element $C$ not contain, and beacuse $B = C$, which means $A$ have element $B$ not contain, this is a contradiction to $A = B$, so transitive is true.  

Exercise 3.1.2. Using only Definition 3.1.4, Axiom 3.1, Axiom 3.2, and Axiom 3.3, prove that the sets $\varnothing, \lbrace \varnothing \rbrace, \lbrace \lbrace \varnothing \rbrace \rbrace$, and $\lbrace \varnothing, \lbrace \varnothing \rbrace \rbrace$ are all distinct (i.e., no two of them are equal to each other).  
* $\varnothing$ is a set which contains nothing, then $\varnothing$ is a object. $\lbrace \varnothing \rbrace$ is a set which contains $\varnothing$ (an object), then $\lbrace \varnothing \rbrace \ne \varnothing$ because $\lbrace \varnothing \rbrace$ has an element. The rest is skip.  

Exercise 3.1.3. Prove the remaining claims in Lemma 3.1.13.  
Exercise 3.1.4. Prove the remaining claims in Proposition 3.1.18.  
Exercise 3.1.5. Let $A, B$ be sets. Show that the three statements $A \subseteq B, A \ \cup\  B = B, A \ \cap\  B = A$ are logically equivalent (any one of them implies the other two).  
* If $A \subseteq B, \forall x \in A \ \cup\  B \Leftrightarrow x \in B$, then $A \ \cup\  B = B$. If $A \ \cup\  B = B$, then $A \subseteq A \ \cup\  B = B$. Thus we have $A \subseteq B \Leftrightarrow A \ \cup\  B = B$.  
* If $A \ \cup\  B = B, \forall x \in A \Rightarrow x \in B \Rightarrow x \in A \ \cap\  B$, then $A \ \cap\  B = A$. If $A \ \cap\  B = A, \forall x \in A \ \cup\  B \Rightarrow x \in A$ or $x \in B$, suppose $x \in A \Rightarrow x \in B$ since $A \ \cap\  B = A$, then we have $A \ \cup\  B = B$. Thus we have $A \ \cup\  B = B \Leftrightarrow A \ \cap\  B = A$.  

Exercise 3.1.6. Prove Proposition 3.1.28. (Hint: one can use some of these claims to prove others. Some of the claims have also appeared previously in Lemma 3.1.13.)  
Exercise 3.1.7. Let $A,B,C$ be sets. Show that $A \ \cap\  B \subseteq A$ and $A \ \cap\  B \subseteq B$. Furthermore,show that $C \subseteq A$ and $C \subseteq B$ if and only if $C \subseteq A \ \cap\  B$. In a similar spirit, show that $A \subseteq A \ \cup\  B$ and $B \subseteq A \ \cup\  B$, and furthermore that $A \subseteq C$ and $B \subseteq C$ if and only if $A \ \cup\  B \subseteq C$.  
* It's obviously that if we get any element in $A \ \cap\  B$, then immediately we can know that the element is in $A$ and $B$. So get $A \ \cap\  B \subseteq A$ and $A \ \cap\  B \subseteq B$.  
* If $C \subseteq A$ and $C \subseteq B$, it means every element in $C$ is also in $A$ and $B$, quickly implies that $C \subseteq A \ \cap\  B$. Skip the rest.  
* If $A \subseteq C$ and $B \subseteq C$, it means that every element in $A$ or every element in $B$, we can get the element is also in $C$, then $A \ \cup\  B \subseteq C$. Skip the rest.  

Exercise 3.1.8. Let A, B be sets. Prove the absorption laws $A \ \cap\  (A \ \cup\  B) = A$ and $A \ \cup\  (A \ \cap\  B) = A$.  
* $A \subseteq A \ \cup\  B$, use Exercise 3.1.5, we get $A \ \cap\  (A \ \cup\  B) = A$.  
* $A \ \cap\  B \subseteq A$, use Exercise 3.1.5 again, get $A \ \cup\  (A \ \cap\  B) = A$.  

Exercise 3.1.9. Let $A,B,X$ be sets such that $A \cup B = X$ and $A \cap B = \varnothing$. Show that $A = X / B$ and $B = X / A$.  
* It's obviously that $A \subseteq X$ and $B \subseteq X$, quckily get $A \cup B = X = B \cup (X / B) \Rightarrow (B \cup (X / B)) / B = (A \cup B) / B \Rightarrow ((X / B) / B) \cup (B / B) = (A / B) \cup (B / B)$, Because $A \cap B = \varnothing, A / B = A$ and $(X / B) / B = X / B \Rightarrow X / B \cup \varnothing = A \cup \varnothing$, then $X / B = A$. Skip the rest.  
* If $A \cap B = \varnothing, \forall x \in A$, we have $x \notin B$, then $x \in A$ and $x \notin B \Rightarrow A / B = A$.  

Exercise 3.1.10. Let $A$ and $B$ be sets. Show that the three sets $A / B, A \cap B$, and $B / A$ are disjoint, and that their union is $A \cup B$.
* Obviously, $A / B$ and $A \cap B$ are disjoint, $B / A$ and $A \cap B$ are also disjoint. Show that $A / B$ and $B / A$ are disjoint. It's obviously that any element in $A / B$ is not in $B$, but any element in $B / A$ is in $B$, so $A / B$ and $B / A$ are disjoint.  
* Show $(A / B) \cup (A \cap B) = A$. Suppose $(A / B) \cup (A \cap B) \ne A$, then there exists some elements $x$ such that $x$ belong to $A$ but not belong to $(A / B) \cup (A \cap B)$. If $x \notin A / B \Rightarrow x \in B \Rightarrow x \in A \cap B$, this is a contradiction. If $x \notin A \cap B \Rightarrow x \notin B \Rightarrow x \in A / B$, it's also a contradiction. Thus $(A / B) \cup (A \cap B) = A$.  
* $(A / B) \cup (A \cap B) \cup (B / A) = (A / B) \cup (A \cap B) \cup (B / A) \cup (A \cap B) = A \cup B$.   

Exercise 3.1.11. Show that the axiom of replacement implies the axiom of specification.  
* Let $A$ be a set and $P(x)$ is a property pertaining to some elements $x \in A$. Suppose $Q(x, y)$ is that $y = x$ when $P(x)$ is true, and axiom of replacement could imply the axiom of specification. Skip the rest.  

## 3.2 Russell’s paradox (Optional)  
### Axioms  
* 3.8 (Universal specification). (Dangerous!) Suppose for every object $x$ we have a property $P(x)$ pertaining to $x$ (so that for every $x$, $P(x)$ is either a true statement or a false statement). Then there exists a set $\lbrace x : P(x) \text{\ is\ true\ } \rbrace$ such that for every object $y$, $y \in \lbrace x: P(x) \text{\ is\ true\ } \rbrace \Leftrightarrow P(y)$ is true.   
* 3.9 (Regularity). If $A$ is a non-empty set, then there is at least one element $x$ of $A$ which is either not a set, or is disjoint from $A$.  

### Exercises
Exercise 3.2.1. Show that the universal specification axiom, Axiom 3.8, if assumed to be true, would imply Axioms 3.2, 3.3, 3.4, 3.5, and 3.6. (If we assume that all natural numbers are objects, we also obtain Axiom 3.7.) Thus, this axiom, if permitted, would simplify the foundations of set theory tremendously (and can be viewed as one basis for an intuitive model of set theory known as “naive set theory”). Unfortunately, as we have seen, Axiom 3.8 is “too good to be true”!  
* Axiom 3.2. Let a such object $X$, its property is no element in $X$, and call $X$ is empty set.  
* Axiom 3.3. Let $a, b$ are objects. First we can assign a such property to $X$, $X$ only contain one of $a$ and $b$. Second we can change this property, $X$ contain both $a$ and $b$.  
* Axiom 3.4. Let $A, B$ are objects. Object $X$ have such property that $X$ contain all elements in $A$ and $B$.  
* Axiom 3.5. Let $A$ be set. $X$ have such property that contain all the elements in $A$ which statisfy $P(a)$.  

Exercise 3.2.2. Use the axiom of regularity (and the singleton set axiom) to show that if $A$ is a set, then $A \notin A$. Furthermore, show that if $A$ and $B$ are two sets, then either $A \notin B$ or $B  \notin A$ (or both).  
* If $A \in A$, use axiom 3.3, we have $\lbrace A \rbrace$, let $\lbrace A \rbrace \cup A = A$, it's obviously contradiction to axiom 3.9.  
* If $A \in B$ and $B \in A, A \cup B = \lbrace A, B \rbrace = A$, then $\lbrace A, B \rbrace$ just contain $A$ which is not disjoint from itself, contradiction to axiom 3.9.  

Exercise 3.2.3. Show (assuming the other axioms of set theory) that the universal specification axiom, Axiom 3.8, is equivalent to an axiom postulating the existence of a “universal set” $\Omega$ consisting of all objects (i.e., for all objects $x$, we have $x \in \Omega$). In other words, if Axiom 3.8 is true, then a universal set exists, and conversely, if a universal set exists, then Axiom 3.8 is true. (This may explain why Axiom 3.8 is called the axiom of universal specification). Note that if a universal set $\Omega$ existed, then we would have $\Omega \in \Omega$ by Axiom 3.1, contradicting Exercise 3.2.2. Thus the axiom of foundation specifically rules out the axiom of universal specification.  
* If universal specification axiom, then we can assign such property that contain all objects to a set, get the $\Omega$ set. If $\Omega$ exists, use axiom 3.5, we can assign any property to the objects in $\Omega$ to get any set, so we get Axiom 3.8.   

## 3.3 Functions  
### Definitions  
* 3.1 (Functions). Let $X, Y$ be sets, and let $P(x, y)$ be a property pertaining to an object $x \in X$ and an object $y \in Y$ , such that for every $x \in X$, there is exactly one $y \in Y$ for which $P(x, y)$ is true (this is sometimes known as the vertical line test). Then we define the function $f: X \rightarrow Y$ defined by $P$ on the domain $X$ and range $Y$ to be the object which, given any input $x \in X$, assigns an output $f(x) \in Y$, defined to be the unique object $f(x)$ for which $P(x, f(x))$ is true. Thus, for any $x \in X$ and $y \in Y, y = f(x) \Leftrightarrow P(x, y)$ is true.  
* 3.3.7 (Equality of functions). Two functions $f: X \rightarrow Y, g: X \rightarrow Y$ with the same domain and range are said to be equal, $f = g$, if and only if $f(x) = g(x)$ for all $x \in X$.  
* 3.3.10 (Composition). Let $f: X \rightarrow Y$ and $g: Y \rightarrow Z$ be two functions, such that the range of $f$ is the same set as the domain of $g$. We then define the composition $g \circ f: X \rightarrow Z$ of the two functions $g$ and $f$ to be the function defined explicitly by the formula, $(g \circ f)(x) := g(f(x))$.  
* 3.3.14 (One-to-one functions). A function f is one-to-one (or injective) if different elements map to different elements: $x \ne x^{\prime} \Rightarrow f(x) \ne f(x^{\prime})$. Equivalently, a function is one-to-one if $f(x) = f(x^{\prime}) \Rightarrow x = x^{\prime}$.  
* 3.3.17 (Onto functions). A function $f$ is onto (or surjective) if $f(X) = Y$, i.e., every element in $Y$ comes from applying $f$ to some element in $X$: For every $y \in Y$, there exists $x \in X$ such that $f(x) = y$.  
* 3.3.20 (Bijective functions). Functions $f: X \rightarrow Y$ which are both one-to-one and onto are also called bijective or invertible. If $f$ is bijective, then for every $y \in Y$, there is exactly one $x$ such that $f(x) = y$ (there is at least one because of surjectivity, and at most one because of injectivity). This value of $x$ is denoted $f^{−1}(y)$; thus $f^{−1}$ is a function from $Y$ to $X$. We call $f^{−1}$ the inverse of $f$.  

### Lemma 3.3.12 (Composition is associative). Let $f: Z \rightarrow W, g: Y \rightarrow Z$, and $h: X \rightarrow Y$ be functions. Then $f \circ (g \circ h) = (f \circ g) \circ h$.   
* $f \circ (g \circ h)$ and $(f \circ g) \circ h$ have the same domain and range.  
* $(f \circ (g \circ h))(x) = (f \circ g \circ h)(x) = ((f \circ g) \circ h)(x)$, so $f \circ (g \circ h)=(f \circ g) \circ h$.  

### Exercises  
Exercise 3.3.1. Show that the definition of equality in Definition 3.3.7 is reflexive, symmetric, and transitive. Also verify the substitution property: if $f, f^{\prime}:X \rightarrow Y$ and $g, g^{\prime}: Y \rightarrow Z$ are functions such that $f = f^{\prime}$ and $g = g^{\prime}$, then $g \circ f = g^{\prime} \circ f^{\prime}$.  
* Let $f,g,h$ be function, it's obvious that $x = x, g = g$, and $h = h$. If $x = g$, then $g = x$ is also true obviuosly. If $x = g$ and $g = h$, because $f,g$ have the same domain and range, $g, h$ have the same domain and range, so $f, h$ have the same domain and range. And get any $x$ for $f$, we have $f(x) = g(x)$, and because $g = h$, so we have $g(x) = h(x)$, then $f(x) = h(x)$. So transitive is true.  
* Because $f = f^{\prime}$, then $g \circ f = g \circ f^{\prime}$, Beacuse $g = g^{\prime}, g \circ f^{\prime} = g^{\prime} \circ f^{\prime}$, so we get $g \circ f = g^{\prime} \circ f^{\prime}$.  

Exercise 3.3.2. Let $f: X \rightarrow Y$ and $g: Y \rightarrow Z$ be functions. Show that if $f$ and $g$ are both injective, then so is $g \circ f$, similarly, show that if $f$ and $g$ are both surjective, then so is $g \circ f$.  
* Let $x, y$ are different elements, then $f(x), f(y)$ is different, and $g$ is injective, so $g(f(x)), g(f(y))$ is different, then we know different $x$ and $y, g \circ f$ map different elements, so $g \circ f$ is injective.  
* Suppose $f, g$ are surjective. $\forall z \in Z$, could get some elements $y$ in $Y$ such that $g(y) = z$. Similarly, for $y$ we also get $x$ in $X$ such that $f(x) = y$. Thus $\forall z \in Z, \exists x \in X, (g \circ f)(x) = z$ and $g \circ f$ is surjective.  

Exercise 3.3.3. When is the empty function injective? surjective? bijective? Empty function is $f: \varnothing \rightarrow X$ from the empty set to an arbitrary set $X$.  
* If $X$ is empty, empty function is surjective and bijective.  
* If $X$ is none-empty, empty function is injective.  

Exercise 3.3.4. In this section we give some cancellation laws for composition. Let $f: X \rightarrow Y, f^{\prime}: X \rightarrow Y, g: Y \rightarrow Z$ and $g^{\prime}: Y \rightarrow Z$ be functions. Show that if $g \circ f = g \circ f^{\prime}$ and $g$ is injective, then $f = f^{\prime}$. Is the same statement true if $g$ is not injective? Show that if $g \circ f = g^\prime \circ f$ and $f$ is surjective, then $g = g^\prime$. Is the same statement true if $f$ is not surjective?  
* If $g \circ f = g \circ f^\prime, g \circ f$ and $g \circ f^\prime$ have the same domain and range,  $f$ and $f^\prime$ have the same domain. $\forall x \in X, g(f(x)) = g(f^\prime(x))$. Let $y = f(x), y^\prime = f^\prime(x)$, since $g$ is inective, $g(y) = g(y^\prime)$ when $y = y^\prime$. Then $f(x) = f^\prime(x)$ and $f = f^\prime$. If $g$ is not injective, the statment is not true.   
* Suppose $g \circ f = g^\prime \circ f$. $\forall y \in Y, \exists x \in X \  st.\  f(x) = y$. Because $g(f(x)) = g^\prime(f(x)) \Rightarrow g(y) = g^\prime(y)$ for every $y$ in $Y$. Thus $g = g^\prime$. If $f$ is not surjective, then there exist some $y^\prime \in Y \ st. \ \forall x \in X, f(x) \ne y^\prime$, but it's possible that $g(y^\prime) \ne g^\prime(y^\prime)$.  

Exercise 3.3.5. Let $f: X \rightarrow Y$ and $g: Y \rightarrow Z$ be functions. Show that if $g \circ f$ is injective, then $f$ must be injective. Is it true that $g$ must also be injective? Show that if $g \circ f$ is surjective, then $g$ must be surjective. Is it true that $f$ must also be surjective?  
* Suppose $f$ is not injective, then there exists differnt elements $x, x^\prime$ in $X$ such that $f(x) = f(x^\prime)$, and it will cause that $g(f(x)) = g(f(x^\prime))$ which means that $g \circ f$ is not injective, contradiction. If $g$ is not injective and $f$ is injective, $g \circ f$ is also injective.  
* Suppose $g$ is not surjective, then $\exists z \in Z \ st. \ \forall y \in Y, g(y) \ne z$, because $y = f(x)$ then we could not find a $x$ such that $g(f(x)) = z$. Thus $g \circ f$ is not surjective, contradiction. It's true for that $f$ could not be surjective.  

Exercise 3.3.6. Let $f: X \rightarrow Y$ be a bijective function, and let $f^{−1}: Y \rightarrow X$ be its inverse. Verify the cancellation laws $f^{−1}(f(x)) = x$ for all $x \in X$ and $f(f^{−1}(y)) = y$ for all $y \in Y$. Conclude that $f^{−1}$ is also invertible, and has $f$ as its inverse (thus $(f^{−1})^{−1} = f$).  
* $\forall x \in X, f(x) = y$ and $f^{-1}(y) = x$ thus $f^{−1}(f(x)) = x$. $\forall y \in Y, f^{-1}(y) = x$ and $f(x) = y$, thus $f(f^{−1}(y)) = y$.  
* $f^{-1}(y) = x$ then its inverse $(f^{−1})^{−1}(x) = y$, and because $f^{-1}$ is $f$ inverse function then $f(x) = y = (f^{−1})^{−1}(x)$. Thus $(f^{−1})^{−1} = f$.  

Exercise 3.3.7. Let $f: X \rightarrow Y$ and $g: Y \rightarrow Z$ be functions. Show that if $f$ and $g$ are bijective, then so is $g \circ f$ and we have $(g \circ f)^{−1} = f^{−1} \circ g^{−1}$.  
* Use Exercise 3.3.5 could prove that $g \circ f$ is bijective.  
* $\forall z \in Z, g^{-1}(z) = y, f^{-1}(y) = x \Rightarrow (f^{−1} \circ g^{−1})(z) = x$. Because $f$ and $g$ is inverse we could have $f(x) = y$ and $g(y) = x \Rightarrow (f \circ g)(x) = z \Rightarrow ((g \circ f)^{−1})(z) = x = (f^{−1} \circ g^{−1})(z)$. Thus $(g \circ f)^{−1} = f^{−1} \circ g^{−1}$.  

Exercise 3.3.8. If $X$ is a subset of $Y$ , let $l_{X \rightarrow Y}: X \rightarrow Y$ be the inclusion map from $X$ to $Y$, defined by mapping $x \mapsto x$ for all $x \in X$,i.e., $l_{X \rightarrow Y}(x) := x$ for all $x \in X$. The map $l_{X \rightarrow X}$ is in particular called the identity map on $X$.  
(a) Show that if $X \subseteq Y \subseteq Z$ then $l_{Y \rightarrow Z} \circ l_{X \rightarrow Y} = l_{X \rightarrow Z}$.  
(b) Show that if $f: A \rightarrow B$ is any function, then $f = f \circ l_{A \rightarrow A}  = l_{B \rightarrow B} \circ f$.  
(c) Show that, if $f: A \rightarrow B$ is a bijective function, then $f \circ f^{−1} = l_{B \rightarrow B}$ and $f^{−1} \circ f = l_{A \rightarrow A}$.  
(d) Show that if $X$ and $Y$ are disjoint sets,and $f: X \rightarrow Z$ and $g: Y \rightarrow Z$ are functions, then there is a unique function $h: X \cup Y \rightarrow Z$ such that $h \circ l_{X \rightarrow X \cup Y} = f$ and $h \circ l_{Y \rightarrow X \cup Y} = g$.  
* Let $h(X) = f(X)$ and $h(Y) = g(Y)$. Then we coulde the result.  

## 3.4 Images and inverse images  
### Axioms  
* 3.10 (Power set axiom). Let $X$ and $Y$ be sets. Then there exists a set, denoted $Y^X$, which consists of all the functions from $X$ to $Y$, thus $f \in Y^X \Leftrightarrow$ ($f$ is a function with domain $X$ and range $Y$).  
* 3.11 (Union). Let $A$ be a set, all of whose elements are themselves sets. Then there exists a set $\bigcup A$ whose elements are precisely those objects which are elements of the elements of $A$, thus for all objects $x, x \in \bigcup A \Leftrightarrow$ ($x \in S$ for some $S \in A$).   
### Definitions  
* 3.4.1 (Images of sets). If $f: X \rightarrow Y$ is a function from $X$ to $Y$ , and $S$ is a set in $X$, we define $f(S)$ to be the set $f(S) := \lbrace f(x): x \in S \rbrace$. We sometimes call $f(S)$ the forward image of $S$.  
* 3.4.4 (Inverse images). If $U$ is a subset of $Y$ , we define the set $f^{−1}(U)$ to be the set $f^{−1}(U) := \lbrace x \in X: f(x) \in U \rbrace$. We call $f^{-1}(U)$ the inverse image of $U$.  
   
### Lemma 3.4.9. Let $X$ be a set. Then the set $\lbrace Y: Y \subset X \rbrace$ is a set.  
* Hint: start with the set $\lbrace 0, 1 \rbrace^X$ and apply the replacement axiom, replacing each function $f$ with the object $f^{−1}(\lbrace 1 \rbrace)$  
* Let $f: \lbrace 0, 1 \rbrace \rightarrow X$, and use Axiom 3.10 we have $F = \lbrace 0, 1 \rbrace^X$, then for any $f \in F$ give a $P(f, y)$ that $y$ is the set(object) of all object $x$ which $f(x) = 1$. By the replacement axiom, we have a set $\lbrace f^{-1}(1): f \in F \rbrace$. According to the inverse images for every $f \in F$, $f^{-1}(1)$ is a subset of $X$. And for any $Y \subseteq X$, we could built a function that $g(x) = 1$ if $x \in Y$ and $g(x) = 0$ if $x \notin Y$, obviously $g \in F$. Thus $\lbrace f^{-1}(1): f \in F \rbrace = \lbrace Y: Y \subset X \rbrace$ is a set.  

### Exercises  
Exercise 3.4.1 Let $f: X \rightarrow Y$ be a bijective function, and let $f^{−1} : Y \rightarrow X$ be its inverse. Let $V$ be any subset of $Y$. Prove that the forward image of $V$ under $f^{−1}$ is the same set as the inverse image of $V$ under $f$; thus the fact that both sets are denoted by $f^{−1}(V)$ will not lead to any inconsistency.  
* The forward image of $V$ under $f^{−1}$ is $\lbrace f^{-1}(y): y \in V \rbrace = F$, the inverse image of $V$ under $f$ is $\lbrace x \in X: f(x) \in V \rbrace = I$. If $x \in \lbrace f^{-1}(y): y \in V \rbrace, x = f^{-1}(y)$, because $y \in V$, $f(f^{-1}(y)) = y$ also in $V$, so $\forall x \in \lbrace f^{-1}(y): y \in V \rbrace$ we could have $f(x) \in V$ and $x \in X$, get $F \subseteq I$. Similarly, we could get $I \subseteq F$.  

Exercise 3.4.2 Let $f: X \rightarrow Y$ be a function from one set $X$ to another set $Y$ , let $S$ be a subset of $X$, and let $U$ be a subset of $Y$. What, in general, can one say about $f^{−1}(f(S))$ and $S$? What about $f(f^{−1}(U))$ and $U$?  
* $\forall x \in S$, obviously $x \in X$ and $f(x) \in f(S)$, then we have $S \subseteq f^{−1}(f(S))$.  
* $\forall y \in f(f^{−1}(U))$ and let $y = f(x), x \in \lbrace x \in X: f(x) \in U \rbrace$, then it's easy to see that $f(x) \in U \Rightarrow y \in U \Rightarrow f(f^{−1}(U)) \subseteq U$.   

Exercise 3.4.3. Let $A, B$ be two subsets of a set $X$, and let $f: X \rightarrow Y$ be a function. Show that $f(A \cap B) \subseteq f(A) \cap f(B)$, that $f(A) / f(B) \subseteq f(A / B), f(A \cup B) = f(A) \cup f(B)$. For the first two statements, is it true that the $\subseteq$ relation can be improved to $=?$
* $\forall y \in f(A \cap B) = \lbrace f(x): x \in A \cap B \rbrace$, because $x \in A \cap B$, we have $x \in A$ then $y = f(x)$ also in $f(A)$. Similarly, we could get $y \in f(B)$. Thus $f(A \cap B) \subseteq f(A) \cap f(B)$.  
* $\forall y \in f(A) / f(B)$, let $y = f(x), f(x) \in f(A) \Rightarrow x \in A$ and $f(x) \notin f(B) \Rightarrow x \notin B$, then $y = f(x)$ which $x \in A / B \Rightarrow y \in f(A / B)$. Thus $f(A \cap B) \subseteq f(A) \cap f(B)$.  
* Suppose $y = f(x) \in f(A \cup B)$, if $x \in A \Rightarrow y = f(x) \in f(A)$ and if $x \in B \Rightarrow y = f(x) \in f(B)$. Thus $y \in f(A) \cup f(B)$. Skip the rest.  
* If $f$ is injective, then the $\subseteq$ relation can be improved to $=$.  

Exercise 3.4.4. Let $f: X \rightarrow Y$ be a function from one set $X$ to another set $Y$, and let $U, V$ be subsets of $Y$. Show that $f^{−1}(U \cup V) = f^{−1}(U) \cup f^{−1}(V)$, that $f^{−1}(U \cap V) = f^{−1}(U) \cap f^{−1}(V)$, and that $f^{−1}(U / V) = f^{−1}(U) / f^{−1}(V)$.  
* Easy to prove. Skip.  

Exercise 3.4.5. Let $f: X \rightarrow Y$ be a function from one set $X$ to another set $Y$. Show that $f(f^{−1}(S)) = S$ for every $S \subseteq Y$ if and only if $f$ is surjective. Show that $f^{−1}(f(S)) = S$ for every $S \subseteq X$ if and only if $f$ is injective.  
* Combine with Exercise 3.4.2.  
* Suppose $f$ is surjective. If $y \in S$, then there exists some element $x$ in $X$ such that $f(x) = y$. Now we think about $x$, because $f(x) = y$, then $x \in \lbrace x \in X: f(x) \in S \rbrace$. Thus $y \in f(f^{−1}(S)) \Rightarrow S \subseteq f(f^{−1}(S))$.  
* Suppose $S \subseteq f(f^{−1}(S))$, $\forall y \in Y$, because $Y \subseteq Y$, we have $Y \subseteq f(f^{−1}(Y))$, also $y \in f(f^{−1}(Y))$, then $y = f(x), x \in f^{-1}(Y) \Rightarrow$ for each $y$ there exists some elements $x \in X$ such that $y = f(x)$, thus $f$ is surjective.   
* Suppose $f$ is injective. Suppose $f^{−1}(f(S)) \not\subseteq S$ and let $x \in f^{−1}(f(S))$ and $x \notin S$. Also $f(x) \in f(S)$. Then suppose $x^\prime \in S \ st. f(x^\prime) = f(x)$, because $f$ is injective we have $x = x^\prime \Rightarrow x \in S$ which is a contradiction. Thus $f^{−1}(f(S)) \subseteq S$.  
* Suppose $f^{−1}(f(S)) \subseteq S$. If $f$ is not injective, let $f(x) = f(x^\prime), x \in S, x^\prime \in S^\prime, S \cap S^\prime = \varnothing$, obviously $x^\prime \in f^{−1}(f(S))$ and $x^\prime \notin S$ which is a contradiction with $f^{−1}(f(S)) = S$ for every $S \subseteq X$. Thus $f$ is injective.  

Exercise 3.4.6. Prove Lemma 3.4.9. (Hint: start with the set $\lbrace 0, 1 \rbrace^X$ and apply the replacement axiom, replacing each function $f$ with the object $f^{−1}(\lbrace 1 \rbrace)$.)See also Exercise 3.5.11.  

Exercise 3.4.7. Let $X, Y$ be sets. Define a partial function from $X$ to $Y$ to be any function $f: X^\prime \rightarrow Y^\prime$ whose domain $X^\prime$ is a subset of $X$, and whose range $Y^\prime$ is a subset of $Y$. Show that the collection of all partial functions from $X$ to $Y$ is itself a set.(Hint: use Exercise 3.4.6, the power set axiom, the replacement axiom, and the union axiom.)  
* $S := \lbrace X^\prime: X^\prime \subseteq X \rbrace, L := \lbrace Y^\prime: Y^\prime \subseteq Y \rbrace, F := \lbrace (Y^\prime)^{X^\prime} \rbrace$. And $\bigcup_{X^\prime \in S}\bigcup_{Y^\prime \in L} (Y^\prime)^{X^\prime}$.  

Exercise 3.4.8. Show that Axiom 3.4 can be deduced from Axiom 3.1, Axiom 3.3 and Axiom 3.11.  
* Give two sets $A, B$. $A$ and $B$ are objects by Axiom 3.1, and we have $\lbrace A, B \rbrace$ by Axiom 3.3, then we could get the set $A \cup B$ exists by Axiom 3.11.  

Exercise 3.4.9. Show that if $\beta$ and $\beta^\prime$ are two elements of a set $I$, and to each $\alpha \in I$ we assign a set $A_\alpha$, then $\lbrace x \in A_\beta: x \in A_\alpha \text{\ for\ all\ } \alpha \in I \rbrace = \lbrace x \in A_{β^\prime} : x \in A_\alpha \text{\ for\ all\ } \alpha \in I \rbrace$, and so the definition of $\bigcap_{\alpha \in I} A_\alpha$ defined in (3.3) does not depend on $\beta$. Also explain why (3.4) is true.  
* 3.3 equation is $\bigcap_{\alpha \in I} A_\alpha := \lbrace x \in A_\beta: x \in A_\alpha \text{\ for\ all\ } \alpha \in I \rbrace$, 3.4 is $y \in \bigcap_{\alpha \in I} A_\alpha \Leftrightarrow$ ($y \in A_\alpha$ for all $\alpha \in I$).  
* If the definition of $\bigcap_{\alpha \in I} A_\alpha$ defined in (3.3) does not depend on $\beta$, let $\beta = \alpha \in I$, then $y \in \lbrace x \in A_\alpha: x \in A_\alpha \text{\ for\ all\ } \alpha \in I \rbrace$, by specificatiom axiom geting the $y \in A_\alpha$ for all $\alpha \in I$ is true.  

Exercise 3.4.10. Suppose that $I$ and $J$ are two sets, and for all $\alpha \in I \cup J$ let $A_\alpha$ be a set. Show that $(\bigcup_{\alpha \in I} A_\alpha) \cup (\bigcup_{\alpha \in J} A_\alpha) = \bigcup_{\alpha \in I \cup J} A_\alpha$. If $I$ and $J$ are non-empty, show that $(\bigcap_{\alpha \in I} A_\alpha) \cap (\bigcap_{\alpha \in J} A_\alpha) = \bigcap_{\alpha \in I \cup J} A_\alpha$.  
* $x \in (\bigcup_{\alpha \in I} A_\alpha) \cup (\bigcup_{\alpha \in J} A_\alpha) \Leftrightarrow x \in A_\alpha \text{\ for\ some\ } \alpha \in I$ or $x \in A_\alpha \text{\ for\ some\ } \alpha \in J \Leftrightarrow x \in A_\alpha \text{\ for\ some\ } \alpha \in I \text{\ or\ } \alpha \in J \Leftrightarrow x \in \bigcup_{\alpha \in I \cup J} A_\alpha$.  
* $x \in (\bigcap_{\alpha \in I} A_\alpha) \cap (\bigcap_{\alpha \in J} A_\alpha) \Leftrightarrow x \in A_\alpha \text{\ for\ all\ } \alpha \in I$ and $x \in A_\alpha \text{\ for\ all\ } \alpha \in J \Leftrightarrow x \in A_\alpha \text{\ for\ every\ elements\ } \alpha \text{\ both\ in\ I\ and\ J\ } \Leftrightarrow x \in A_\alpha \text{\ for\ all\ } \alpha \in I \cup J$.  

Exercise 3.4.11. Let $X$ be a set, let $I$ be a non-empty set, and for all $\alpha ∈ I$, let $A_\alpha$ be a subset of $X$. Show that $X / \bigcup_{\alpha \in I} A_\alpha = \bigcap_{\alpha \in I} (X / A_\alpha)$ and $X / \bigcap_{\alpha \in I} A_\alpha = \bigcup_{\alpha \in I} (X / A_\alpha)$. This should be compared with de Morgan’s laws in Proposition 3.1.28 (although one cannot derive the above identities directly from de Morgan’s laws, as $I$ could be infinite).  
* $\forall x \in X / \bigcup_{\alpha \in I} A_\alpha \Leftrightarrow x \in X$ and $x \notin \bigcup_{\alpha \in I} A_\alpha \Leftrightarrow x \in X$ and $x \notin A_\alpha$ for all $\alpha \in I \Leftrightarrow \bigcap_{\alpha \in I} (X / A_\alpha)$.  

## 3.5 Cartesian products  
### Definitions  
* 3.5.1 (Ordered pair). If $x$ and $y$ are any objects (possibly equal), we define the ordered pair $(x, y)$ to be a new object, consisting of $x$ as its first component and $y$ as its second component. Two ordered pairs $(x, y)$ and $(x^\prime, y^\prime)$ are considered equal if and only if both their components match, i.e $(x, y) = (x^\prime, y^\prime) \Leftrightarrow (x = x^\prime \text{\ and\ } y = y^\prime)$.  
* 3.5.4 (Cartesian product). If $X$ and $Y$ are sets, then we define the Cartesian product $X * Y$ to be the collection of ordered pairs, whose first component lies in $X$ and second component lies in $Y$ , thus $X * Y = \lbrace (x, y): x \in X, y \in Y \rbrace$ or equivalently $a \in (X, Y) \Leftrightarrow (a = (x, y) \text{\ for\ some\ } x \in X \text{\ and\ } y \in Y)$.  
* 3.5.7 (Ordered $n$-tuple and $n$-fold Cartesian product). Let $n$ be a natural number. An ordered $n$-tuple$\ (x_i)_{1 \leq i \leq n}$ (also denoted $(x_1, ..., x_n)$) is a collection of objects $x_i$, one for every natural number $i$ between $i$ and $n$; we refer to $x_i$ as the ith component of the ordered $n$-tuple. Two ordered $n$-tuples $(x_i)_{1 \le i \le n}$ and $(y_i)_{1 \le i \le n}$ are said to be equal iff $x_i = y_i$ for all $1 \le i \le n$. If $(X_i)_{1 \le i \le n}$ is an ordered $n$-tuple of sets, we define their Cartesian product $\prod_{1 \le i \le n} X_i$ (also denoted $\prod_{i = 1}^n X_i \text{\ or\ } X_1 * . . . * X_n$) by $\prod_{1 \le i \le n} X_i := \lbrace (x_i)_{1 \le i \le n} : x_i \in X_i \text{\ for\ all\ } 1 \le i \le n \rbrace$.  

### Lemma 3.5.12 (Finite choice). Let $n \ge 1$ be a natural number, and for each natural number $1 \le i \le n$, let $X_i$ be a non-empty set. Then there exists an $n$-tuple $(x_i)_{1 \le i \le n}$ such that $x_i \in X_i$ for all $1 \le i \le n$. In other words, if each $X_i$ is non-empty, then the set $\prod_{1 \le i \le n} X_i$ is also non-empty.  
* Use induction to prove.  

### Exercise  
Exercise 3.5.1. Suppose we define the ordered pair $(x, y)$ for any objects $x$ and $y$ by the formula $(x, y) := \lbrace \lbrace x \rbrace, \lbrace x, y \rbrace \rbrace$ (thus using several applications of Axiom 3.3). Thus for instance $(1, 2)$ is the set $\lbrace \lbrace 1 \rbrace, \lbrace 1, 2 \rbrace \rbrace, (2, 1)$ is the set $\lbrace \lbrace 2 \rbrace, \lbrace 2, 1 \rbrace \rbrace$, and $(1, 1)$ is the set $\lbrace \lbrace 1 \rbrace \rbrace$. Show that such a definition indeed obeys the property (3.5), and also whenever $X$ and $Y$ are sets, the Cartesian product $X * Y$ is also a set. Thus this definition can be validly used as a definition of an ordered pair. For an additional challenge, show that the alternate definition $(x, y) := \lbrace x, \lbrace x, y \rbrace \rbrace$ also verifies (3.5) and is thus also an acceptable definition of ordered pair. (For this latter task one needs the axiom of regularity, and in particular Exercise 3.2.2.)  
* Formula 3.5 is $a \in (X, Y) \Leftrightarrow (a = (x, y) \text{\ for\ some\ } x \in X \text{\ and\ } y \in Y)$.  
* We need to prove that $(x, y) := \lbrace \lbrace x \rbrace, \lbrace x, y \rbrace \rbrace$ is a ordered pair. If $(x, y) = (x^\prime, y^\prime) \Rightarrow \lbrace \lbrace x \rbrace, \lbrace x, y \rbrace \rbrace = \lbrace \lbrace x^\prime \rbrace, \lbrace x^\prime, y^\prime \rbrace \rbrace \Rightarrow x = x^\prime, y = y^\prime$. If $x = x^\prime, y = y^\prime$, then $(x, y) = \lbrace \lbrace x \rbrace, \lbrace x, y \rbrace \rbrace = \lbrace \lbrace x^\prime \rbrace, \lbrace x^\prime, y^\prime \rbrace \rbrace = (x, y)$. Thus $\lbrace \lbrace x \rbrace, \lbrace x, y \rbrace \rbrace$ is ordered pair.  
* The rest is skip.  

Exercise 3.5.2. Suppose we define an ordered $n$-tuple to be a surjective function $x:\lbrace i \in N: 1 \le i \le n \rbrace \rightarrow X$ whose range is some arbitrary set $X$ (so different ordered $n$-tuples are allowed to have different ranges); we then write $x_i$ for $x(i)$, and also write $x$ as $(x_i)_{1 \le i \le n}$. Using this definition, verify that we have $(x_i)_{1 \le i \le n} = (y_i)_{1 \le i \le n}$ if and only if $x_i = y_i$ for all $1 \le i \le n$. Also, show that if $(X_i)_{1 \le i \le n}$ are an ordered $n$-tuple of sets, then the Cartesian product, as defined in Definition 3.5.7, is indeed a set. (Hint: use Exercise 3.4.7 and the axiom of specification.)  
* See $x$ and $y$ as functions, their domain is $1 \le i \le n$ and range is $X$. If $(x_i)_{1 \le i \le n} = (y_i)_{1 \le i \le n}$, then obviously that $x_i = y_i$ for all $1 \le i \le n$. If $x_i = y_i$ for all $1 \le i \le n$, then $\forall j \in \lbrace 1 \le i \le n \rbrace$, we have $x(j) = y(j)$, thus $x = y$.  
* Let $1 \le i \le n$ be domain, the $X$ be range, use Exercise 3.4.7 we have a set $F$ contain all the partial functions from the subset of $1 \le i \le n$ to the subset of $X$. Use the axiom of specification, we select the functions which is a surjective function $x:\lbrace i \in N: 1 \le i \le n \rbrace \rightarrow X$ with range of some arbitrary subset of $X$.  

Exercise 3.5.3. Show that the definitions of equality for ordered pair and ordered $n$-tuple obey the reflexivity, symmetry, and transitivity axioms.  

Exercise 3.5.4. Let $A, B, C$ be sets. Show that $A * (B \cup C) = (A * B) \cup (A * C)$, that $A * (B \cap C) = (A * B) \cap (A * C)$, and that $A * (B / C) = (A * B) / (A * C)$. (One can of course prove similar identities in which the roles of the left and right factors of the Cartesian product are reversed.)  
* $\forall (x, y) \in A * (B \cup C) \Leftrightarrow x \in A$ and $y \in B \cup C \Leftrightarrow (x \in A \text{\ and\ } y \in B) \text{\ or\ } (x \in A \text{\ and\ } y \in C) \Leftrightarrow (x, y) \in (A * B) \cup (A * C)$.  
* Skip the rest.  

Exercise 3.5.5. Let $A, B, C, D$ be sets. Show that $(A * B) \cap (C * D) = (A \cap C) * (B \cap D)$. Is it true that $(A * B) \cup (C * D) = (A \cup C) * (B \cup D)$? Is it true that $(A * B) / (C * D) = (A / C) * (B / D)$?  
* $\forall (x, y) \in (A * B) \cap (C * D) \Leftrightarrow (x, y) \in A * B \text{\ and\ } (x, y) \in C * D \Leftrightarrow (x \in A \text{\ and\ } y \in B) \text{\ and\ } (x \in C \text{\ and\ } y \in D) \Leftrightarrow (x, y) \in (A \cap C) * (B \cap D)$.  
* $(A * B) \cup (C * D) = (A \cup C) * (B \cup D)$ is false.  
* $(A * B) / (C * D) = (A / C) * (B / D)$ is false.  

Exercise 3.5.6. Let $A, B, C, D$ be non-empty sets. Show that $A * B \subseteq C * D$ if and only if $A \subseteq C$ and $B \subseteq D$, and that $A * B = C * D$ if and only if $A = C$ and $B = D$. What happens if the hypotheses that the $A, B, C, D$ are all non-empty are removed?  
* If the hypotheses that the $A, B, C, D$ are all non-empty are removed, those proposition will not be true.  

Exercise 3.5.7. Let $X, Y$ be sets, and let $\pi_{X * Y \rightarrow X}: X * Y \rightarrow X$ and $\pi_{X * Y \rightarrow Y}: X * Y \rightarrow Y$ be the maps $\pi_{X * Y \rightarrow X}(x, y) := x$ and $\pi_{X * Y \rightarrow Y} (x, y) := y$; these maps are known as the coordinate functions on $X * Y$ . Show that for any functions $f: Z \rightarrow X$ and $g: Z \rightarrow Y$ , there exists a unique function $h: Z \rightarrow X * Y$ such that $\pi_{X * Y \rightarrow X}  \circ h = f$ and $\pi_{X * Y \rightarrow Y}  \circ h = g$. (Compare this to the last part of Exercise 3.3.8, and to Exercise 3.1.7.) This function $h$ is known as the direct sum of $f$ and $g$ and is denoted $h = f \oplus g$.  
* $\forall z \in Z, h(z) := (f(z), g(z))$, then $h = f \oplus g$.  

Eercise 3.5.8. Let $X_1,...,X_n$ be sets. Show that the Cartesian product $\prod_{i = 1}^n X_i$ is empty if and only if at least one of the $X_i$ is empty.  
* If at least one of the $X_i$ is empty, then $(x_i)_{1 \le i \le n}$ could not be a object since $X_i$ does not contain any object for consisting an $n$-tuple ordered pair. Thus none-object in $\prod_{i = 1}^n X_i$.  
* If $\prod_{i = 1}^n X_i$ is empty, suppose all of the $X_i$ is none-empty, then we could get that at least one object in $\prod_{i = 1}^n X_i$, which is a contradiction.  

Exercise 3.5.9. Suppose that $I$ and $J$ are two sets, and for all $\alpha \in I$ let $A_\alpha$ be a set, and for all $\beta \in J$ let $B_\beta$ be a set. Show that $(\bigcup_{\alpha \in I} A_\alpha) \cap (\bigcup_{\beta \in J} B_\beta) = \bigcup_{(\alpha, \beta) \in I * J} (A_\alpha \cap B_\beta)$.  

Exercise 3.5.10 If $f: X \rightarrow Y$ is a function, define the graph of $f$ to be the subset of $X * Y$ defined by $\lbrace (x, f(x)): x \in X \rbrace$. Show that two functions $f:X \rightarrow Y,f^\prime: X \rightarrow Y$ are equal if and only if they have the same graph. Conversely, if $G$ is any subset of $X * Y$ with the property that for each $x \in X$, the set $\lbrace y \in Y: (x,y) \in G \rbrace$ has exactly one element (or in other words, $G$ obeys the vertical line test), show that there is exactly one function $f: X \rightarrow Y$ whose graph is equal to $G$.  
* If there exists such set $G$, suppose for each $x \in X, f(x) \in \lbrace y \in Y: (x, y) \in G \rbrace$, because $\lbrace y \in Y: (x, y) \in G \rbrace$ contain exactly one element, thus $f(x) = y$. Thus $(x, f(x)) = (x, y)$ for each $x \in X$ and $G = \lbrace (x, f(x)): x \in X \rbrace$.  

Exercise 3.5.11 Show that Axiom 3.10 can in fact be deduced from Lemma 3.4.9 and the other axioms of set theory, and thus Lemma 3.4.9 can be used as an alternate formulation of the power set axiom. (Hint: for any two sets $X$ and $Y$, use Lemma 3.4.9 and the axiom of specification to construct the set of all subsets of $X * Y$ which obey the vertical line test. Then use Exercise 3.5.10 and the axiom of replacement.)  
* Let $C = X * Y$, use Lemma 3.4.9, $H = \lbrace M: M \subset C \rbrace$. And use specification axiom to select all sets which statisfy the condition of $G$ in exercise 3.5.10 to construct a set $P$. Then $\forall G \in P$ exist a function $f$ such that whose graph is equal to $G$ to construct a set $F$ by replacement axiom. Suppose a arbitrary function $f^\prime: X \rightarrow Y$, then that could have a set $G^\prime = \lbrace (x, f(x)): x \in X, f(x) \in Y \rbrace$, obviously $G^\prime \subset C$ and $G \in P$, so the $F$ is the set $Y^X$.  

Exercise 3.5.12. This exercise will establish a rigorous version of Proposition 2.1.16. Let $f: N * N \rightarrow N$ be a function, and let $c$ be a natural number. Show that there exists a function $a: N \rightarrow N$ such that $a(0) = c$ and $a(n++) = f(n, a(n))$ for all $n \in N$, and furthermore that this function is unique. (Hint: first show inductively, by a modification of the proof of Lemma 3.5.12, that for every natural number $n \in N$, there exists a unique function $a_n : {n^\prime \in N : n^\prime \le n} \rightarrow N$ such that $a_n(0) = c$ and $a_n(n^\prime ++) = f(n, a(n^\prime))$ for all $n^\prime \in N$ such that $n^\prime < n$.) For an additional challenge, prove this result without using any properties of the natural numbers other than the Peano axioms directly (in particular, without using the ordering of the natural numbers, and without appealing to Proposition 2.1.16). (Hint: first show inductively, using only the Peano axioms and basic set theory, that for every natural number $n \in N$, there exists a unique pair $A_n, B_n$ of subsets of $N$ which obeys the following properties: (a) $A_n \cap B_n = \varnothing$, (b) $A_n \cup B_n = N$, (c) $0 \in A_n$, (d) $n++ \in B_n$, (e) Whenever $n^\prime \in B_n$, we have $n^\prime++ \in B_n$. (f) Whenever $n^\prime \in A_n$ and $n^\prime \ne n$, we have $n^\prime++ \in A_n$. Once one obtains these sets, use $A_n$ as a substitute for $\lbrace n^\prime \in N : n^\prime \le n \rbrace$ in the previous argument).  
* Suppse $n = 0$, let $A_n = \lbrace 0 \rbrace, B_n = \lbrace 1, 2, .... \rbrace$. Obviously, the $A_n, B_n$ obey the five properties and also be a unique pair. Suppose when $n = k$ that also get unique pair $A_k, B_k$. Consider the status of $A_n, B_n$ when $n = k++$.  
* Use sepcification and union axim, $A_{k++} = \lbrace A_k \rbrace \cup \lbrace k++ \rbrace, B_{k++} = B_k / \lbrace k++ \rbrace$. Obviously, $A_{k++}, B_{k++}$ is obey the five properties. Now show the pair is unique. Suppose another pair $A_{k++}^\prime, B_{k++}^\prime$, and $A_{k++}^\prime, B_{k++}^\prime$ must be $A_{k++}^\prime = \lbrace A_k^\prime \rbrace \cup \lbrace k++ \rbrace, B_{k++}^\prime = B_k^\prime / \lbrace k++ \rbrace$, then we already have when $n = k$ that only one unique pair $A_k, B_k$. Thus $A_k^\prime =  A_k, B_k^\prime = B_k$ and $A_{k++}, B_{k++}$ is one unique pair.  

Exercise 3.5.13. The purpose of this exercise is to show that there is essentially only one version of the natural number system in set theory (cf. the discussion in Remark 2.1.12). Suppose we have a set $N^\prime$ of “alternative natural numbers”, an “alternative zero” $0^\prime$, and an “alternative increment operation” which takes any alternative natural number $n^\prime \in N^\prime$ and returns another alternative natural number $n^\prime++^\prime \in N^\prime$, such that the Peano axioms (Axioms 2.1-2.5) all hold with the natural numbers, zero, and increment replaced by their alternative counterparts. Show that there exists a bijection $f: N \rightarrow N^\prime$ from the natural numbers to the alternative natural numbers such that $f(0) = 0^\prime$, and such that for any $n \in N$ and $n^\prime \in N^\prime$, we have $f(n) = n^\prime$ if and only if $f(n++) = n^\prime++^\prime$. (Hint: use Exercise 3.5.12.)  

## 3.6. Cardinality of sets  

### Definitions  
* 3.6.1 (Equal cardinality). We say that two sets $X$ and $Y$ have equal cardinality iff there exists a bijection $f: X \rightarrow Y$ from $X$ to $Y$.  
* 3.6.10 (Finite sets). A set is finite iff it has cardinality $n$ for some natural number $n$; otherwise, the set is called infinite. If $X$ is a finite set, we use $\#(X)$ to denote the cardinality of $X$.  

### Proposition 3.6.4. Let $X, Y, Z$ be sets. Then $X$ has equal cardinality with $X$. If $X$ has equal cardinality with $Y$ , then $Y$ has equal cardinality with $X$. If $X$ has equal cardinality with $Y$ and $Y$ has equal cardinality with $Z$, then $X$ has equal cardinality with $Z$.  

### Proposition 3.6.8 (Uniqueness of cardinality). Let $X$ be a set with some cardinality $n$. Then $X$ cannot have any other cardinality, i.e., $X$ cannot have cardinality $m$ for any $m \ne n$.  
* Suppse $X$ has two different cardinality $m, n$ and $m < n$. For some $d \in N$ such that $m + d = n$. Let $M, N$ denote the cardinality set, if we use Lemma 3.6.9, then $M$ remove $d$ times elements, and we could get a new set $M^\prime$ has cardinality $n$. Obviously, $M^\prime$ and $M$ could not have a bijection function, then this is a contradiction.  

### Lemma 3.6.9. Suppose that $n ≥ 1$, and $X$ has cardinality $n$. Then $X$ is non-empty, and if $x$ is any element of $X$, then the set $X − \lbrace x \rbrace$ (i.e., $X$ with the element $x$ removed ) has cardinality $n − 1$.  
* If $X$ is empty, it's impossible for that there exists a bijection function from empty set to non-empty set. Because only function from $\varnothing$ to $\varnothing$ could be surjective.     

### Theorem 3.6.12. The set of natural numbers $N$ is infinite.  
* If $N$ is finite, so it has a sure cardinality $n^\prime$ which means it has a bijection mapped to $N^\prime$ and $n^\prime$ is a natural number, but according to the definition of $N$, every natural number $n$ in $N$ has its sucessor $n++$, so that $n^\prime++$ is in $N$ but not in $N^\prime$, contradction.  

### Proposition 3.6.14 (Cardinal arithmetic).  
(a) Let $X$ be a finite set, and let $x$ be an object which is not an element of $X$. Then $X \cup \lbrace x \rbrace$ is finite and $\#(X \cup \lbrace x \rbrace) = \#(X) + 1$.  

(b) Let $X$ and $Y$ be finite sets. Then $X \cup Y$ is finite and $\#(X \cup Y) \le \#(X) + \#(Y)$. If in addition $X$ and $Y$ are disjoint (i.e., $X \cap Y = \varnothing$), then $\#(X \cup Y) = \#(X) + \#(Y)$.  

(c) Let $X$ be a finite set, and let $Y$ be a subset of $X$. Then $Y$ is finite, and $\#(Y) \le \#(X)$. If in addition $Y \ne X$ (i.e., $Y$ is a proper subset of $X$), then we have $\#(Y) < \#(X)$.  
* If $Y \subseteq X$, then $Y \cup (X/Y) = X$. Obviously,$\#(Y) \leq \#(Y) + \#(X/Y)$. Use (b) we have $\#(Y) + \#(X/Y) \leq \#(Y \cup (X/Y) = \#(X))$, then we have $\#(Y) \leq\#(X)$. If $Y \neq X$, which means that $\#(X/Y) \neq 0$, then $\#(Y) < \#(Y) + \#(X/Y) \le \#(Y \cup (X/Y)) = \#(X)$, then $\#(Y) < \#(X)$.  

(d) If $X$ is a finite set, and $f: X \rightarrow Y$ is a function, then $f(X)$ is a finite set with $\#(f(X)) \le \#(X)$. If in addition $f$ is one-to-one, then $\#(f(X)) = \#(X)$.  
* If $f$ is not one-to-one, then at least have two different elements $x, y \in X$ such that $f(x) = f(y)$. Suppose $X^\prime = X - \lbrace x \rbrace$ and $g: X^\prime \rightarrow Y, g(x) = f(x)$, then $f(X) = g(X^\prime)$. Because $g$ is a bijection, $\#(f(X)) = \#(g(X^\prime)) = \#(X^\prime) < \#(X)$.  

(e) Let $X$ and $Y$ be finite sets. Then Cartesian product $X * Y$ is finite and $\#(X * Y) = \#(X) * \#(Y)$.  
* $X * Y = \lbrace (x,y):x\in X \ and \ y\in Y \rbrace = \bigcup \lbrace (x,y_i):x \in X, 1 \le i \le \#(Y) \rbrace$, let $Y_i = ((x,y_i):x \in X, 1 \le i \le \#(Y))$, then $\#(X * Y) = \#(Y_1 \cup Y_2 .... \cup Y_{\#(Y)})$. Obviously $Y_1......Y_{\#(Y)}$ is disjoint with each other, so $\#(X * Y) = \#(Y_1 \cup Y_2 .... \cup Y_{\#(Y)}) = \#(Y_1) + \#(Y_2) + ......+ \#(Y_{\#(Y)})$. It's easy to find a bijection from $X$ to $Y_i$, then $\#(Y_i) = \#(X)$. So that we get $\#(X * Y) = \#(Y_1) + \#(Y_2) + ......+ Y_{\#(Y)} = \#(X) * \#(Y)$.  

(f) Let $X$ and $Y$ be finite sets. Then the set $Y^X$ (defined in Axiom 3.10) is finite and $\#(Y^X) = \#(Y)^{\#(X)}$.  
* Suppose $X$ has $n$ cardinality and $Y$ has $m$ cardinality, thus $X = \lbrace x_1, ...., x_n \rbrace, Y = \lbrace y_1, ...., y_m \rbrace$ and $X * Y = \lbrace (x, y): x \in X, y \in Y \rbrace$, use the axiom of specification $X_{i(1 \le i \le n)} = \lbrace (x_i, y): y \in Y \rbrace$ and $\#(X_i) = \#(Y) = m$. By Exercise 3.5.10, the graph of function is equal to function itself, then for one specific function(denote $f$) graph is $\lbrace (x_1, f(x_1)), ...., (x_n, f(x_n)) \rbrace$. The graph also has $n$ cardinlity and its every element from $X_{i(1 \le i \le n)}$, so the all function graph could be $\prod_1^n X_i = \lbrace (g_i): g_i \in X_i, 1 \le i \le n \rbrace$. One of element in $\prod_1^n X_i$ repsent a function graph with domain $X$ and range $Y$. Thus we have $\#(\prod_{i = 1}^n X_i)= \#(Y^X)$.  
* $\#(\prod_{i = 1}^n X_i) = \#(X_1 * X_2 *......* X_n)$, use (e) of Proposition 3.6.14 $n$ times(could be proved by induction), $\#(\prod_{i = 1}^n X_i) = \#(X_1 * X_2 *......* X_n) = m * m .... * m = m^n = \#(Y)^{\#(X)}.$  

### Exercises  
Exercise 3.6.1. Prove Proposition 3.6.4.  
Exercise 3.6.2. Show that a set $X$ has cardinality $0$ if and only if $X$ is the empty set.  
* If X has cardinality $0$, according to the definition of cardinality, it has no element in $X$, so $X$ is empty set.  

Exercise 3.6.3. Let $n$ be a natural number, and let $f: \lbrace i \in N : 1 \le i \le n \rbrace \rightarrow N$ be a function. Show that there exists a natural number $M$ such that $f(i) \le M$ for all $1 \le i \le n$. (Hint: induct on $n$. You may also want to peek at Lemma 5.1.14.) Thus finite subsets of the natural numbers are bounded.  
* If $n$ is equal to $0$, the conclusion of 3.6.3 will be vacuously true. If $n == 1$, there has just one element and suppose $f(1) = j, j \in N$, we could find $j++$ is larger than $j$, then $f(i) \le j$ is true. Show that $n++$ is true, let $f(n++) = K$, if $K \le M$, then we could say $f(i) \le M \ \text{for} \ 1 \le i \le p++$, if $M \le K$, we will find $K < K++$, then $f(i) < K++ \ for \ 1 \le i \le p++$.  
* Suppose have a finite subset of $N$, we could say this set $A$ has $m$ cardinality, which means $A$ has a bijection $g$ to $B = \lbrace i \in N:1 \le i \le n \rbrace$ for some natural number $n$. And $g^{-1}$ is from $B$ to $A$, obviously $g^{-1}(B) = A \subseteq N$, now we could say $g^{-1}(i) \le M \ \text{for} \ 1 \le i \le n$ which means $A$ is bounded.  

Exercise 3.6.4. Prove Proposition 3.6.14.  
Exercise 3.6.5. Let $A$ and $B$ be sets. Show that $A * B$ and $B * A$ have equal cardinality by constructing an explicit bijection between the two sets. Then use Proposition 3.6.14 to conclude an alternate proof of Lemma 2.3.2.  
* Lemma 2.3.2 (Multiplication is commutative). Let $n, m$ be natural numbers. Then $n * m = m * n$.  
* Skip.  

Exercise 3.6.6. Let $A, B, C$ be sets. Show that the sets $(A^B)^C$ and $A^{B * C}$ have equal cardinality by constructing an explicit bijection between the two sets. Conclude that $(a^b)^c = a^{bc}$ for any natural numbers $a, b, c$. Use a similar argument to also conclude $a^b * a^c = a^{b+c}$.  
* $(A^B)^C = \lbrace f: \text{\ the domain is} \ C \text{\ and the range is} \ A^B  \rbrace, A^{B * C} = \lbrace g: \text{\ the domain is} \ B * C \text{\ and the range is} \ A \rbrace$. Let $H: A^{B * C} \rightarrow (A^B)^C, H(g) = f$ when for every $(b, c) \in B * C$ has $g(b, c) = f(c)(b)$. Suppose $H(g) = H(g^\prime)$, use $f^\prime$ to denote $H(g)$ or $H(g^\prime)$, then for every $(b, c) \in B * C$ has $g(b, c) = f(c)(b) = g^\prime(b, c) \Rightarrow g = g^\prime$ and $H$ is one-to-one. Suppose $f \in (A^B)^C, \forall c \in C, f(c) = f^\prime (f^\prime \in A^B)$ and $\forall b \in B, f^\prime(b) = a \Rightarrow \forall (b, c) \in B * C, f(c)(b) = a$. If we see $f(c)(b)$ as a new function, then this function must be in $A^{B * C}$. Thus $H$ is suejective.  
* Show that $A^B * A^C$ and $A^{B \cup C}$ have equal cardinality by constructing an explicit bijection between the two sets. Let $B \cap C = \varnothing$, $H: A^B * A^C \rightarrow A^{B \cup C}, H((g, f)) = h$ when $\forall b \in B$ and $\forall c \in C$ has $g(b) = h(b)$ and $f(c) = h(c)$. Obviously, the $H$ is a bijection function. Skip the rest.  

Exercise 3.6.7. Let $A$ and $B$ be sets. Let us say that A has lesser or equal  cardinality to $B$ if there exists an injection $f: A \rightarrow B$ from $A$ to $B$. Show that if $A$ and $B$ are finite sets, then $A$ has lesser or equal cardinality to $B$ if and only if $\#(A) \le \#(B)$.  
* If $\#(A) \le \#(B)$, by defintion we could say $\#(A) = a$ and $\#(B) = b$, so $A$ and $B$ are finite sets. Suppose $g$ is bijection from $N_a$ to $A$ and $f$ is bijection from $N_b$ to $B$. Let such function $h: A \rightarrow B, h(a) = f(g^{-1}(a))$, it's easy to find $h$ is a injection from $A$ to $B$, thus $A$ has lesser or equal cardinality to $B$.  

Exercise 3.6.8. Let $A$ and $B$ be sets such that there exists an injection $f: A \rightarrow B$ from $A$ to $B$ (i.e., $A$ has lesser or equal cardinality to $B$). Show that there then exists a surjection $g: B \rightarrow A$ from $B$ to $A$. (The converse to this statement requires the axiom of choice; see Exercise 8.4.3.)  

Exercise 3.6.9. Let $A$ and $B$ be finite sets. Show that $A \cup B$ and $A \cap B$ are also finite sets, and that $\#(A) + \#(B) = \#(A \cup B) + \#(A \cap B)$.  
* Suppose $\#(A) = a, \#(B) = b$, and $\#(A \cap B) = k$. $A \cup B = A/A \cap B + A \cap B + B/A \cap B$. Use (b) of proposition 3.6.14 could get $\#(A/A \cap B)= \#(A) - \#(A \cap B)$. Then $\#(A \cap B) + \#(A \cup B) = \#(A \cap B) + \#(A/A \cap B + A \cap B + B/A \cap B) = \#(A \cap B) + \#(A) - \#(A \cap B) + \#(A \cap B) + \#(B) - \#(A \cap B) = k + a - k + b - k = a + b = \#(A) + \#(B)$.  

Exercise 3.6.10. Let $A_1,..., A_n$ be finite sets such that $\#(\bigcup_{i \in \lbrace 1,...,n \rbrace}A_i) > n$. Show that there exists $i \in \lbrace 1, ..., n \rbrace$ such that $\#(A_i) \ge 2$. (This is known as the pigeonhole principle.)  
* 3.6.10 Use (b) of proposition 3.6.14, then $\#(\bigcup_{i \in (1,....,n)}A_i) = \#(A_1 \bigcup A_2.......\bigcup A_n) \le \#(A_1)+.....+ \#(A_n)$, and $\#(\bigcup_{i \in (1,....,n)}A_i) > n$, so $\#(A_1)+.....+ \#(A_n) > n$, If there does not exist $i \in \lbrace 1, ..., n \rbrace$ such that $\#(A_i) ≥ 2$, then every $\#(A_i)\le 1$, obviously $\#(A_1)+.....+ \#(A_n) \le n$, it's a contradiction.  