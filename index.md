---
title: "Solutions to Abbott's Understanding Analysis"
description: "Solutions to analysis"
author: "Zul "
---
[Home](https://zul.rocks)

Solutions that need polishing are marked 🔄 and unfinished solutions are marked ❎

<a name="toc"></a>

# Table of contents

[Chapter 1](#c1)  | Chapter 2 
:------------ | :-------------
[1.2.10](#1210) 🔄 | 
[1.2.11](#1211) 🔄 | 
[1.2.12](#1212) 🔄 | 
[1.2.13](#1213) 🔄 | 
[1.3.1](#131) 🔄 | 
[1.3.2](#132) 🔄 | 
[1.3.3](#133) 🔄 | 
[1.3.4](#134) 🔄 | 
[1.3.5](#135) 🔄 | 
[1.3.6](#136) 🔄 | 
[1.3.7](#137) 🔄 | 
[1.3.8](#138) 🔄 | 
[1.3.9](#139) 🔄 | 
[1.3.10](#1310) 🔄 |
[1.3.11](#1311) 🔄 | 
[1.4.1](#141) | 
[1.4.2](#142)|
[1.4.3](#143)|
[1.4.4](#144)|
[1.4.5](#145)|
[1.4.6](#146)|
[1.4.7](#147)|
[1.4.8](#148) 🔄 |


<a name="c1"></a>

## Chapter 1 

<a name="1210"></a>

### [1.2.10](#toc) 

Decide which of the following are true statements. Provide a short justification for those that are valid and a counterexample for those that are not:

   1. Two real numbers satisfy $a<b$ if and only if $a<b+\epsilon$ for every $\epsilon>0$.
   2. Two real numbers satisfy $a<b$ if $a<b+\epsilon$ for every $\epsilon>0$.
   3. Two real numbers satisfy $a \leq b$ if and only if $a<b+\epsilon$ for every $\epsilon>0$.
  
---

1. False. Let $a=b$. In this case, although $a<b+ \epsilon$ for each $\epsilon>0$, $a$ is not smaller than $b$. (Note that for the other way around, it is true: if $a<b$, then $a<b+\epsilon$ for every $\epsilon>0$. Assume there is some $\epsilon$ such that $a \geq b+ \epsilon$. Then $a-b \geq \epsilon >0$, which means $a>b$, which is a contradiction).
2. False, as above.
3. First, show that if $a \leq b$, then $a < b + \epsilon$ for each $\epsilon >0$. This has already been shown in 1. Second, show that if $a<b+\epsilon$ for every $\epsilon>0$, then $a \leq b$. Assume that $a > b$. Take $\epsilon_0 = a-b$. This means that $a<b + \epsilon_0 = b + a -b = a$, which is a contradiction.



<a name="1211"></a>

### [1.2.11](#toc) 

Form the logical negation of each claim. One trivial way to do this is to simply add "It is not the case that..." in front of each assertion. To make this interesting, fashion the negation into a positive statement that avoids using the word "not" altogether. In each case, make an intuitive guess as to whether the claim or its negation is the true statement.

  1. For all real numbers satisfying $a<b$, there exists an $n \in \mathbf{N}$ such that $a+1 / n<b$.
  2. There exists a real number $x>0$ such that $x<1 / n$ for all $n \in \mathbf{N}$.
  3. Between every two distinct real numbers there is a rational number.
  
---

1. There exist some real numbers $a<b$ such that for all $n \in \mathbf{N}$, $a+ 1/n >b$. I think the claim is the true statement, and the negation is false.
2. For all real number $x>0$, $x \geq 1/n$ for some $n \in \mathbf{N}$. The negation is true.
3. There exist two distinct real numbers between which there is no rational number. I think the claim is true, and the negation is false.


<a name="1212"></a>

### [1.2.12](#toc) 

 Let $y_{1}=6$, and for each $n \in \mathbf{N}$ define $y_{n+1}=\left(2 y_{n}-6\right) / 3$

1. Use induction to prove that the sequence satisfies $y_{n}>-6$ for all $n \in \mathbf{N}$.
2. Use another induction argument to show the sequence $\left(y_{1}, y_{2}, y_{3}, \ldots\right)$ is decreasing.
  
---

1. The statement is obviously true when $n=1$. Assume $y_{n}>-6$ is true, and we need to show that this is true for $y_{n+1}$ as well.

$$\begin{align*}
y_{n+1}&= (2 y_{n}-6)/3  \\
 &> (2(-6) -6 )/3   \\
& > (-12 -6)/3 \\
&> -6
\end{align*}$$

2. Since $y_2 = (2(6)-6)/3=2$, $y_1 > y_2$. Assume $y_{n-1} > y_{n}$, and we need to show that $y_{n} > y_{n+1}$.

Answer 1:

$$\begin{align*}
 y_{n+1} &= 2y_{n}/3 -2 \\
 &<0.8y_n -2 \\
 &<0.8y_n \\
 &<y_n
 \end{align*}$$

 Answer 2: Simply multiply 2 across the inequality, minus 6, and divide 3, to get
 $$\begin{align*}
 \left(2 y_{n-1}-6\right) / 3 &> \left(2 y_{n}-6\right) / 3 \\
 y_{n}&>y_{n+1}
 \end{align*}$$

 
<a name="1213"></a>

### [1.2.13](#toc) 

For this exercise, assume Exercise 1.2.5 has been successfully completed.
  1. Show how induction can be used to conclude that $$ (A_1 \cup A_{2}\cup \cdots \cup A_{n})^{c}=A_{1}^{c} \cap A_{2}^{c} \cap \cdots \cap A_{n}^{c}$$ for any finite $n \in \mathbf{N}$. 
 
  2. It is tempting to appeal to induction to conclude $$\left(\bigcup_{i=1}^{\infty} A_{i}\right)^{c}=\bigcap_{i=1}^{\infty} A_{i}^{c}$$  but induction does not apply here. Induction is used to prove that a particular statement holds for every value of $n \in \mathbf{N}$, but this does not imply the validity of the infinite case. To illustrate this point, find an example of a collection of sets $B_{1}, B_{2}, B_{3}, \ldots$ where $\bigcap_{i=1}^{n} B_{i} \neq \emptyset$ is true for every $n \in \mathbf{N}$, but $\bigcap_{i=1}^{\infty} B_{i} \neq \emptyset$ fails.
   
  3. Nevertheless, the infinite version of De Morgan's Law stated in (b) is a valid statement. Provide a proof that does not use induction.
  
---

1. From Exercise 1.2.5, we know that the base case $$(A_1 \cup A_2)^c = A_1^c \cap A_2^c$$ holds. Assume that $$(A_1 \cup A_2 \cup \cdots \cup A_n)^c = A_1^c \cap A_2^c \cap \cdots \cap A_n^c$$ <span style="color:red">Thinking the solution to this is taking longer than expected, so refer to online solutions. By associative laws, $$(A_1 \cup A_2 \cup \cdots \cup A_n \cup A_{n+1})^c = ((A_1 \cup A_2 \cup \cdots \cup A_n) \cup A_{n+1})^c $$ which by Exercise 1.2.5. implies $$(A_1 \cup A_2 \cup \cdots \cup A_n)^c \cap A_{n+1}^c $$ From assumption, this is equal to $$ A_1^c \cap A_2^c \cap \cdots \cap A_n^c \cap A_{n+1}^c$$</span>

2. Let 

$$\begin{align*}
B_1 &= \mathbf{N} = \{1,2,3, \cdots\} \\
B_2 &= \{2,3,4,\cdots\} \\
B_3 &= \{3,4,5,\cdots\}
\end{align*}$$ 
We see that $$B_1 \cap B_2 = B2$$ and we will prove using induction that $$ \bigcap_{i=1}^{n} B_{i}=B_n$$ Assume the above is true for $n$. In the case of $n+1$, by associative law, $$B_1 \cap B_2 \cap  \cdots B_n \cap B_{n+1} =  (B_1 \cap B_2 \cap  \cdots B_n) \cap B_{n+1}$$ which means $$B_n \cap B_{n+1} $$ which is equal to $B_{n+1}$. Therefore $\bigcap_{i=1}^{n} B_{i}=B_n$ holds for all $n \in \mathbf{N}$.

Nonetheless, this does not hold for infinite case, because $$ \bigcap_{i=1}^{\infty} B_{i}=\emptyset$$ To see why, suppose there is $x \in \mathbf{N}$ which satisfies $x \in \bigcap_{i=1}^{\infty} B_{i}$. This means that $x$ is an element of $B_i$ for all $i \in \mathbf{N}$. However, this is a contradiction because $x$ is not an element of $B_{x+1}$.

3. Let 

$$x \in \left(\bigcap_{i=1}^\infty A_i\right)^c$$

meaning 

$$x \notin \left(\bigcap_{i=1}^\infty A_i\right)$$ 

implying that $x$ is not an element of $A_i$ for all $i$.<span style="color:red">Alternatively $x\in A_i^c$ for all $i$.</span> This means that $x \in \bigcup_{i=1}^\infty A_i^c$ which implies 

$$\left(\bigcap_{i=1}^\infty A_i\right)^c \subseteq \bigcup_{i=1}^\infty A_i^c.$$ 

Conversely, let 

$$x \in \bigcup_{i=1}^\infty A_i^c $$ 

which means that $x \in A_i^c$ for all $i$, which is the same as $x\notin A_i$ for all $i$. This implies that $x \notin \bigcap_{i=1}^\infty A_i$, meaning $x \in \left(\bigcap_{i=1}^\infty A_i\right)^c.$ This implies 

$$\bigcup_{i=1}^\infty A_i^c \subseteq \left(\bigcap_{i=1}^\infty A_i\right)^c  .$$ 


<a name="131"></a>

### [1.3.1](#toc) 

1. Write a formal definition in the style of Definition 1.3.2 for the infimum or greatest lower bound of a set.
2. Now, state and prove a version of lemma 1.3.8 for glb.

---

1. A real number $g$ is the greatest lower bound for a set $A \subseteq \mathbf{R}$ if it meets the following two criteria:
    * $g$ is a lower bound for $A$.
    * if $b$ is any lower bound for $A$, then $g \geq b$. 

2. Lemma. Assume $g \in \mathbf{R}$ is a lower bound for a set $A \subseteq \mathbf{R}$. Then $g = \text{inf }A$ if and only if for every choice $\epsilon >0$, there exists an element $a \in A$ satisfying $g + \epsilon > a.$
    * Assume $g = \text{inf } A$. Then $g \leq a$ for all $a$. Because $g$ is the greatest lower bound, $g + \epsilon$ cannot be $\leq a$ for all $a$. Otherwise, this will contradict statement ii of definition of $g$. Thus, there exists some $a$ such that $g + \epsilon > a.$
    * Assume $g \leq a$ for all $a$, and that for all $\epsilon >0$, $g + \epsilon > a$ for some $a$. If $b$ is a lower bound of $A$, and it is greater than $g$, let $\epsilon_0 = b-g$. Meaning $b = g + \epsilon_0 > a$, thus this is not possible. Therefore $g \geq b$.

<a name="132"></a>

### [1.3.2](#toc) 

Give an example of each of the following, or state that the request is impossible.
1. A set $B$ with $\text{inf }B \geq \text{sup }B$.
2. A finite set that contains its infimum but not its supremum.
3. A bounded subset of $\mathbf{Q}$ that contains its supremum but not its infimum.

---

1. $B = \{1\}$.
2. Not possible
3. $\{1, 1/2, 1/3, \cdots \}$.

<a name="133"></a>

### [1.3.3](#toc) 

1. Let $A$ be nonempty and bounded below, and define $B = \{b\in \mathbf{R}: b \text{ is a lower bound for }A \}$. Show that $\text{sup }B = \text{inf }A$.
2. Use the above to explain why there is no need to assert that greatest lower bounds exist as part of the Axiom of Completeness.

---

1. 

$\rightarrow$ Let $s= \text{sup }B$, and $g= \text{inf }A$. First we show that $s \leq g$. Suppose $s > g$. Meaning by Lemma 1.3.8 and taking $\epsilon_0 = s-g$, $g = s - \epsilon_0 < b$ for some $b$. By definition, $b < a$ for all $a$, and we just show that $b$ is bigger than $g$. But this is a contradiction of statement (ii) of definition 1.3.2. 

$\leftarrow$ Next we show that $s \geq g$. Suppose $s <g$. Then $s <(s+g)/2 < g$, which means that $(s+g)/2$ is a lower bound of A. Which means $(s+g)/2 \in \mathbf{B}$. However, this is a contradiction because $s$ by definition is greater than or equal to all $b \in \mathbf{B}$.

<span style="color:red">Alternative, better answer: Because $A$ is bounded below, $B$ is not empty. Moreover, $B$ is bounded above by $A$. By Axiom of Completion, we can say that $s = \text{sup }B$ exists. Now we need to show that $s = \text{inf }A$, by proving that $s$ is a lower bound of A, and if any $k$ is a lower bound $A$, $k \leq s$.</span>  

<span style="color:red">On the first part, since $A$ is an upper bound of $B$, by statement (ii) of definition 1.3.2, $s \leq a$ for all $a \in A$. Therefore $s$ is a lower bound of A.</span> 


<span style="color:red">Secondly, if any $k$ is a lower bound of $A$, then $k \in B$. By statement (i) of definition 1.3.2, $k \leq s$.</span> 



2. The axiom states that every nonempty set, bounded above has a least upper bound. The above shows the least upper bound is simply the greatest lower bounds of the set of all upper bound the the earlier set.

<span style="color:red">Better answer: By proving that the infimum of A is equal to the supremum of another set, we use that the existence of least upper bounds to assert the existence of greatest lower bound.</span> 

<a name="134"></a>

### [1.3.4](#toc) 

Let $A_1, A_2, A_3, \cdots$ be a collection of nonempty sets, each of which is bounded above.

1. Find a formula for sup ($A_1 \cup A_2$). Extend this to sup ($\cup_{k=1}^{n} A_k$).
2. Consider sup($\cup_{k=1}^{\infty} A_k$). Does the formula in (a) extend to the infinite case?

---

1. Straight-up intuition: max {sup $A_1$, sup $A_2$, ... $A_n$}.

Proof: Let A = $\cup_{k=1}^{n} A_k$. Let M = max {sup $A_1$, sup $A_2$, ..., $A_n$}. We have 

$$ \forall x \in A, x \leq M$$


Let $\epsilon > 0$. Suppose M = sup $A_1$

then $$ \exists a \in A_1 : M - \epsilon < a \leq M $$

$$ \implies \exists a \in A : M - \epsilon < a \leq M $$

The proof follows from lemma 1.3.8.

<span style="color:red">Better answer: Let $m_k$ = sup $A_k$. Let M = sup {$m_1$, $m_2$, ..., $m_n$}. Let $a \in \cup_{k=1}^{n} A_k$. Then $a \in A_k$ for some k. Thus $ a \leq m_k \leq M$. Therefore M is an upper bound of $\cup_{k=1}^{n} A_k$. If b is another upper bound of $\cup_{k=1}^{n} A_k$, then it is also an upper bound of each $A_k$. By statement ii of definition 1.3.2, this means $s_k \leq b$ for each k. By statement ii of definition 1.3.2, this again means that $s \leq b$. </span> 

2. Yes, i think. 


<a name="135"></a>

### [1.3.5](#toc) 

Let A $\subseteq \mathbf{R}$ be nonempty and bounded above and let c be a real number. Define the set cA = {ca : a $\in$ A}.

1. If $c \geq 0$, show that sup(cA) = csup(A).
2. Postulate a similar type of statement for the case c<0.

---

1. Let s = sup A. Then for all a $\in$ A, a $\leq s$. Multiplying c on both sides show that cs is an upper bound of cA. Let b be another upper bound of cA; i.e., $ca \leq b$ for all a. This is equivalent to $a \leq b/c$ if c is not zero. Because s is least upper bound of $a$, $s \leq b/c \implies sc \leq b.$ This proves cs is the least upper bound of cA. If c =0, then sup (cA) = sup (0.A) = 0 = 0. sup(A) = c.sup(A).

2. If $c < 0$, sup(cA) = c inf(A). 

Let s = inf A. Then for all a $\in$ A, a $\geq s$. Multiplying c on both sides show that cs is an upper bound of cA. If b is another upper bound of cA; i.e., $ca \leq b$ for all a. This is equivalent to $a \geq b/c$. Because s is greatest lower bound of $a$, $s \geq b/c \implies sc \leq b.$ This proves cs is the least upper bound of cA.

<a name="136"></a>

### [1.3.6](#toc) 

Given sets $A$ and $B$, define A+B = {a +b : a $\in$ A and b $\in$ B}. Follow these steps to prove that if A and B are nonempty and bounded above, then sup(A+B)=sup A + sup B.

1. Let s = sup A and t = sup B. Show s + t is an upper bound for A + B.
2. Now let $u$ be an arbitrary upper bound for $A+B$, and temporarily fix $a \in A$. Show $t \leq u -a$.
3. Finally show sup $(A+B) = s+t$.
4. Construct another proof of the same fact using lemma 1.3.8.


---

1. For any a $\in$ A, $a \leq s$, and for any b $\in$ B, $b \leq t$. 

Therefore $a + b \leq s + t$.


2. For any a $\in$ A, and any b $\in$ B, $a + b \leq u$. 

$$ \implies b \leq u -a $$

By definition ii of 1.3.2, this means $t \leq u -a$.

From 1, we have shown that s+t is an upper bound of A + B. 

Let $u$ = sup (A+B). From definitin 1 of 1.3.2, $u \leq s+t$.

From 2, we shown that $t + a \leq u$. 

Similarly, $s + b \leq u$.

Adding this up,we will get $s+t+a+b \leq 2u \implies a+b \leq 2u - s -t.$

From definition 1 of 1.3.2, $u \leq 2u - s -t \implies s + t \leq u$.

4. Using lemma 1.3.8, sup (A+B) = sup A + sup B $\iff$ for every $\epsilon > 0$, there exist $a+b$ such that sup A + sup B - $\epsilon$ < a+b.

Take any $\epsilon > 0$, and consider sup A + sup B - $\epsilon$

$\implies$ (sup A - $\epsilon$/2) + (sup B - $\epsilon$/2)

$\implies$ (sup A - $\epsilon$/2) < a and (sup B - $\epsilon$/2) < b

Adding these inequalities completes the proof.

<a name="137"></a>

### [1.3.7](#toc) 

Prove that if $a$ is an upper bound for $A$, and if $a$ is also an element of $A$, then it must be that $a = \text{sup }A$.

---

$a$ is an upper bound.

Suppose $b$ is another upper bound and $b <a$. But this is a contradiction since $a \in A$. Therefore either $b$ is not an upper bound, or $b \leq a$.

<span style="color:red">Easier: Suppose $b$ is another upper bound of $A$. By definition $b \geq a$ since $a$ is an element of $A$. </span> 

<a name="138"></a>

### [1.3.8](#toc) 

Compute without proofs the suprema and infima (if they exist) of the following sets:

1. $\{m/n: m,n \in \mathbf{N} \text{ with } m<n\}$
2. $\{(-1)^m/n: m,n \in \mathbf{N}\}$
3. $\{n/(3n+1): n \in \mathbf{N}\}$
4. $\{m/(m+n): m , n \in \mathbf{N}\}$

---

1. Supremum don't exist. Infimum is 0

<span style="color:red">Missed $m<n$. Thus supremum is 1. </span> 

2. Supremum is $1$. Infimum is $1$.

This is equal to 1/((3+1/n). Supremum is 1/3. Infimum is 1/4

3. This is equal to 1/(1 + n/m). Supremum is 1. Infimum is 0.

<a name="139"></a> 
   
### [1.3.9](#toc) 

1. If sup A < sup B, show that there exists an element $b\in B$ that is an upper bound for A.

2. Given an example to show that this is not always the case if we only assume sup A $\leq$ sup B.

---

1. Let $\epsilon$ be such that sup $A =$ sup $B - \epsilon$. By Lemma 1.3.8, there exists $b \geq$ sup $A \geq a$ for all $a$.

2. Consider $A = [0,1]$ and $B= (0,1)$. sup B $\geq$ sup A.  But there is no element in $B$ whereby it is an upper bound of A.

<a name="1310"></a>

### [Exercise 1.3.10 (Cut property)](#toc) 

If $A$ and $B$ are nonempty, disjoint sets with $A \cup B = \mathbf{R}$ and $a < b$ for all $a \in A$ and $b \in B$, then there exists $c \in R$ such that $x \leq c$ whenever $x \in A$ and $x \geq c$ whenever $x \in B$.

1. Use the Axiom of Completeness to prove the Cut Property.
2. Show that the implication goes the other way; that is, assume $\mathbf{R}$ possesses the Cut Property and let $E$ be a nonempty set that is bounded above. Prove sup E exists.
3. Give a concrete example showing that the Cut Property is not a valid statement when $\mathbf{R}$ is replace by $\mathbf{Q}$.


---

1. Since $A$ is nonempty and bounded above, by the Axiom, it has a least upper bound $s_1$. Thus, when $x \in A$, $x \leq s_1$.

By definition of supremum, all upper bounds of $A$ is greater or equal to $s$. In other words, for all $x \in B$, $x \geq s$.
 
2. Let $B$ be the set of all the upper bound of $E$. Let $B^c = \mathbf{R} - B$. Suppose $E$ does not have a least upper bound.

$\implies$ $E$ is disjointed from $B$, i.e., $E \cap B = \emptyset$ because otherwise there exist sup E.

$\implies$ $E \subseteq B^c$. Therefore, by the Cut Property, there exists $c$ such that $x \leq c$ whenever $x \in E$, and $x \geq c$ whenever $x \in B$.

$\implies$ $c$ cannot be in $E$ since $E$ does not have supremum. Therefore, $c$ is in $B$. But this also is not possible because otherwise it means that $c$ is the smallest upper bound of $E$ -- a contradiction.

3. $\{x: x^2 < 2, x \in \mathbf{Q} \}$ and $\{x: x^2 > 2, x \in \mathbf{Q} \}$.

<a name="1311"></a>

### [Exercise 1.3.11](#toc)  

Decide if the following statements about suprema and infima are true or false. Give a short proof for those that are true. For any that are false, supply an example where the claim in question does not hold.

1. If $A$ and $B$ are nonempty, bounded and satisfy $A \subseteq B$, then sup $A \leq$ sup $B$
2. If sup $A <$ inf $B$ for sets $A$ and $B$,  then there exists $c \in \mathbf{R}$ satisfying $a < c <b$ for all $a \in A$ and $b \in B$.
3. If there exists $c \in \mathbf{R}$ satisfying $a<c<b$ for all $a \in A$ and $b \in B$, then sup $A <$ inf $B$.

---

1. True. Suppose sup $A >$ sup $B$. 


$\implies$ Take $\epsilon = (\text{sup }A - \text{sup }B)/2$

$\implies$ $a_0 \geq \text{sup }A - \epsilon$, for some $a_0 \in A$ from Lemma 1.3.8. Moreover, sup $A - \epsilon > \text{sup } B \geq b$, for all $b \in B$.

$\implies$ $a \notin B$, which is a contradiction.


<span style="color:red">Easier: $a \leq$ sup $A$, and $a \leq$ sup $B$,  since all $a$ is in $B$. By definition of sup $A$, sup $A$ $\leq$ sup $B$. </span> 

2. Yes. Just find the average of sup $A$ and inf $B$. This number is bigger than the former, but smaller than the latter. By definition of sup and inf, the proof is completed.

3. $A = (0,1)$ and $B = (1,2)$. Taking $c=1$, all $a$ is less than $c$, which is less than all $b$. But $c=$ sup $A =$ inf $B$.


<a name="141"></a>

### [Exercise 1.4.1](#toc) 

Recall that $\mathbf{I}$ stands for the set of irrational numbers.
  
  1. Show that if $a, b \in \mathbf{Q}$, then $a b$ and $a+b$ are elements of $\mathbf{Q}$ as well.
  2. Show that if $a \in \mathbf{Q}$ and $t \in \mathbf{I}$, then $a+t \in \mathbf{I}$ and $a t \in \mathbf{I}$ as long as $a \neq 0$.
  3. Part (a) can be summarized by saying that $\mathbf{Q}$ is closed under addition and multiplication. Is $\mathbf{I}$ closed under addition and multiplication? Given two irrational numbers $s$ and $t$, what can we say about $s+t$ and $s t$?
  
---

1. Let $a = m/n$ and $b=k/l$, where $m,n$ are integers, and $k,l$ are non-zero integers. $$ab = mk/nl$$ is in $\mathbf{Q}$ because $mk$ is integer given that integer is closed under multiplication. Similarly, $nk$ is integer and nonzero. $$a+b = m/n + k/l= (ml + nk)/(nk)$$ $ml + nk$ is integer, while $nk$ is nonzero integer.

2. Suppose $a + t \in \mathbf{Q}$.
 Then adding this by $-a$ means that $t \in \mathbf{Q}$ by part 1, which is a contradiction. Similarly, suppose $at \in \mathbf{Q}$, then multiplying this by $1/a$ means that $t \in \mathbf{Q}$ by part 1, which is a contradiction.

 3. $\sqrt{2} \times \sqrt{2}$ is $2$, so $\mathbf{I}$ is not closed under multiplication. Meanwhile take $s = -t$, then $t+s$ = 0, which is rational. So it is not closed under addition.

<a name="142"></a>

### [Exercise 1.4.2](#toc) 

 Let $A \subseteq \mathbf{R}$ be nonempty and bounded above, and let $s \in \mathbf{R}$ have the property that for all $n \in \mathbf{N}, s+\frac{1}{n}$ is an upper bound for $A$ and $s-\frac{1}{n}$ is not an upper bound for $A$. Show $s=\sup A$.

---

Given arbitrary $\epsilon >0$, there exists a natural number $n$ such that $1/n < \epsilon$ by Archimedean Property. Thus $s - \epsilon<s- 1/n< a$ for some $a \in \mathbf{A}$, where the second equality is given. We are done by Lemma 1.3.8.

<a name="143"></a>

### [Exercise 1.4.3](#toc) 


Prove that $\bigcap_{n=1}^{\infty}(0,1 / n)=\emptyset$. Notice that this demonstrates that the intervals in the Nested Interval Property must be closed for the conclusion of the theorem to hold.


---

Suppose $k$ is a solution, meaning $k$ is contained in $(0,1/n)$ for all $n$. Meaning $k>0$ and $k<1/n$ for all $n$. But this contradict Archimedean Property.

<a name="144"></a>

### [Exercise 1.4.4](#toc) 

Let $a<b$ be real numbers and consider the set $T=\mathbf{Q} \cap[a, b]$. Show $\sup T=b$

---

$T$ is not empty because by density of $\mathbf{Q}$ in $\mathbf{R}$, there is a rational number between $a$ and $b$. It is also bounded above, thus sup $T$ exists. 

1. Suppose sup $T$ $<$ $b$. Then, there exists rational number $r$ in between, which is larger than sup $T$. Contradiction.
2. Suppose sup $T > b$. Then there exists rational number $r$ in between, whereby $r$ is smaller than sup $T$ but is an upper bound of $T$. Contradiction.

Thus sup $T = b$.

<a name="145"></a>

### [Exercise 1.4.5](#toc) 

  Using Exercise 1.4.1, supply a proof that $\mathbf{I}$ is dense in $\mathbf{R}$ by considering the real numbers $a-\sqrt{2}$ and $b-\sqrt{2}$. In other words show for every two real numbers $a<b$ there exists an irrational number $t$ with $a<t<b$.

---

Refer to my [blogpost](https://zul.rocks/density-irrational). 

<a name="146"></a>

### [Exercise 1.4.6](#toc) 

  Recall that a set $B$ is dense in $\mathbf{R}$ if an element of $B$ can be found between any two real numbers $a<b$. Which of the following sets are dense in $\mathbf{R}$ ? Take $p \in \mathbf{Z}$ and $q \in \mathbf{N}$ in every case.

 1. The set of all rational numbers $p / q$ with $q \leq 10$.
 
 2. The set of all rational numbers $p / q$ with $q$ a power of 2 .
 
 3. The set of all rational numbers $p / q$ with $10|p| \geq q$.

 ---

 1. No. The minimum positive is $1/10$. The set cannot be found between $1/11$ and $1/12$.

 2. <span style="color:red">Yes. The idea is that you can find $1/2^{n}$ so small, such that given $(a,b)$, you can start from origin, and move in step size of $1/2^{n}$ towards $(a,b)$, and eventually falling in between $a$ and $b$.</span> 

 3. No. $|p|/q \geq 1/10$. The set cannot be found between $1/11$ and $1/12$.


<a name="147"></a>

### [Exercise 1.4.7](#toc) 

  Finish the proof of Theorem 1.4.5 by showing that the assumption $\alpha^{2}>2$ leads to a contradiction of the fact that $\alpha=\sup T$.

  ---

Suppose $\alpha^2 >2$. Then

$$\begin{align*}
(a- 1/n)^{2} &= \alpha^2 - 2\alpha/n + 1/n^2 \\

&> \alpha^2 - 2\alpha/n.

\end{align*}$$

Find $n$ large enough such that $1/n <(\alpha^2 -2)2\alpha$, and such an $n$ exists from Archimedean property. This implies $2\alpha/n <(\alpha^2 -2)$, therefore

$$ (a- 1/n)^{2}> \alpha^2 - 2\alpha/n > \alpha^2 - (\alpha^2-2) = 2.$$

Thus $\alpha - 1/n$ is an upper bound of  $T$, which contradicts the fact that $a$ is the least upper bound.

<a name="148"></a>

### [Exercise 1.4.8](#toc) 

 Give an example of each or state that the request is impossible. When a request is impossible, provide a compelling argument for why this is the case.
  
  1. Two sets $A$ and $B$ with $A \cap B=\emptyset, \sup A=\sup B, \sup A \notin A$ and $\sup B \notin B$.
  
  2. A sequence of nested open intervals $J_{1} \supseteq J_{2} \supseteq J_{3} \supseteq \cdots$ with $\bigcap_{n=1}^{\infty} J_{n}$ nonempty but containing only a finite number of elements.
  
  3. A sequence of nested unbounded closed intervals $L_{1} \supseteq L_{2} \supseteq L_{3} \supseteq \cdots$ with $\bigcap_{n=1}^{\infty} L_{n}=\emptyset$. (An unbounded closed interval has the form $[a, \infty)=$ $\{x \in R: x \geq a\} .)$
  
  4. A sequence of closed bounded (not necessarily nested) intervals $I_{1}, I_{2}$, $I_{3}, \ldots$ with the property that $\bigcap_{n=1}^{N} I_{n} \neq \emptyset$ for all $N \in \mathbf{N}$, but $\bigcap_{n=1}^{\infty} I_{n}=\emptyset$.

  ---

  1. <span style="color:red">$\mathbf{Q} \cap (0,1)$ and $\mathbf{I} \cap (0,1)$. This follows from Thereom 1.4.3, Exercise 1.4.4 and Corollary 1.4.4.</span> 

   2. $J_n = (1- 1/n , 1+1/n)$ which mean $\bigcap_{n \in \mathbf{N}} J_n = \{1\}$. I found conflicting [answer](https://uli.rocks/abbott/) so I may have to dig deeper if my answer is wrong. 

   3. $L_1 = [1, \infty), L_2 = [2, \infty)$ and so on.

  4. Impossible. Let $J_n = (I_1 \cap \cdots \cap 1_n)$. 
     
      + Each $J_n$ contains $J_{n+1}$ since $J_n \supseteq J_n \cap (I_1 \cap \cdots \cap 1_{n+1})$. Hence it is a nested sequence.
      + $J_n$ is nonempty since   $\bigcap_{n=1}^{N} I_{n} \neq \emptyset$ 
      + $J_n$ is closed interval, since intersection of closed intervals is closed.
      $$\begin{align*}
       \bigcap_{n=1}^{\infty} I_{n} &= (I_1 \cap \cdots \cap 1_n \cap \cdots) \\
       &= I_1 \cap (I_1 \cap I_2) \cap (I_1 \cap I_2 \cap I_3) \cdots \\
       &= \bigcap_{n=1}^{\infty} J_{n} \neq \emptyset
       \end{align*}$$

      where last inequality is due to Nested Interval Theorem.

      Note: Damn (4) is interesting as hell. what it is saying is that nested interval theorem can apply to non-nested intervals, as long the finite intersections are nonempty.
     

     