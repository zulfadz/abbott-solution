---
title: "Solutions to Abbott's Understanding Analysis"
description: "Solutions to analysis"
author: "Zul-Fadzli Abu Bakar"
---
[Home](https://zul.rocks)

Solutions that need polishing are marked 🔄 and unfinished solutions are marked ❎

<a name="toc"></a>

# Table of contents

[Chapter 1](#c1)  | [Chapter 2](#c2) |
---|---|
[1.2.10](#1210) 🔄 | [2.2.1](#221)|
[1.2.11](#1211) 🔄 | [2.2.2](#222)|
[1.2.12](#1212) 🔄 | [2.2.3](#223)|
[1.2.13](#1213) 🔄 | [2.2.4](#224)|
[1.3.1](#131) 🔄 | [2.2.5](#225)| |
[1.3.2](#132) 🔄 | [2.2.6](#226)| |
[1.3.3](#133) 🔄 |[2.2.7](#227) | |
[1.3.4](#134) 🔄 | [2.2.8](#228)| |
[1.3.5](#135) 🔄 | [2.3.1](#231)| |
[1.3.6](#136) 🔄 |[2.3.2](#232) |
[1.3.7](#137) 🔄 |[2.3.3](#233) |
[1.3.8](#138) 🔄 | [2.3.4](#234)|
[1.3.9](#139) 🔄 | [2.3.5](#235)|
[1.3.10](#1310) 🔄 |[2.3.6](#236)|
[1.3.11](#1311) 🔄 |[2.3.7](#237) |
[1.4.1](#141) | [2.3.8](#238)|
[1.4.2](#142)|[2.3.9](#239)|
[1.4.3](#143)|[2.3.10](#2310)|
[1.4.4](#144)|[2.3.11](#2311)|
[1.4.5](#145)|[2.3.12](#2312)|
[1.4.6](#146)|[2.3.13](#2313)|
[1.4.7](#147)||
[1.4.8](#148)||
[1.5.1](#151) ||
[1.5.2](#152) ||
[1.5.3](#153) ||
[1.5.4](#154) ||
[1.5.5](#155) ||
[1.5.6](#156) ||
[1.5.7](#157) ||
[1.5.8](#158) ||
[1.5.9](#159) ||
[1.5.10](#1510) ||
[1.5.11](#1511) ||
[1.6.1](#161) ||
[1.6.2](#162) ||
[1.6.3](#163) ||
[1.6.4](#164) ||
[1.6.5](#165) ||
[1.6.6](#166) ||
[1.6.7](#167) ||
[1.6.8](#168) ||
[1.6.9](#169) ||
[1.6.10](#1610) ||




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

   2. $J_n = (1- 1/n , 1+1/n)$ which mean $\bigcap_{n \in \mathbf{N}} J_n = \{1\}$. I found conflicting [answer](https://uli.rocks/abbott/) so I may have to dig deeper if my answer is wrong. Also I really like the systematic approach given [here](https://math.stackexchange.com/questions/223322/give-an-example-of-open-nested-sets-such-that-the-intersection-is-closed-nonemp).

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
     

<a name="151"></a>

### [Exercise 1.5.1](#toc) 

Finish the following proof for Theorem 1.5.7

*Theorem 1.5.7* If $A \subseteq B$ and $B$ is countable, then $A$ is either countable or finite.

Assume $B$ is a countable set. Thus, there exists $f: \mathbf{N} \rightarrow B$, which is 1-1 and onto. Let $A \subseteq B$ be an infinite subset of $B$. We must show that $A$ is countable.

Let $n_1 = \text{min}\{n \in \mathbf{N}: f(n) \in A\}$. As a start to a definition of $g: \mathbf{N} \rightarrow A$, set $g(1) =f(n_{1})$. Show how to inductively continue this process to produce a 1-1 function $g$ from $\mathbf{N}$ onto $A$.

---

<span style="color:red">Took me too long to articulate this question, I ended up just looking for help online. Also how does the assumption that $A$ is infinite help in the proof? It helps because it narrows down the search of function to $f: \mathbf{N} \rightarrow B$.</span> 

Define $g(2) = f(n_{2})$ where $n_2 = \text{min}\{n \in \mathbf{N}: f(n) \in A/f(n_{1})\}$. 

More generally, for $x<y$, we have defined $g(x)$, and set $g(y)= f(n_{y})$ where $n_y = \text{min}\{n \in \mathbf{N}: f(n) \in A/ \{f(n_{1}), f(n_2), \cdots, f(n_{y-1})\}$.

The function is onto:

1. For any $s \in A$, there exists some $n* \in \mathbf{N}$ such that $f(n*) = s$ (since $f$ is onto).
2.  Therefore $n* \in \{n \in \mathbf{N}: f(n)\in A\}$.
3. After iteratively removing minimal element by $w-1 \in \mathbf{N}$ steps, $n*$ will be the minimal element. Hence, $g(w) = f(n*) =s$.

The function is 1-1:

1. For $x \neq y$, $g(x)$ corresponds to $f(n_{x})$ while $g(y)$ corresponds to $f(n_y)$.
2. $n_x \neq n_y$ (because they correspond to unique minimal elements, by construction of $g$).
3. $f(n_x) \neq f(n_y)$ (because $f$ is 1-1).

Note to myself: the construction of $g$, by iteratively removing minimal element is crucial because it helps to prove 1-1. The assumption that $f$ is 1-1 and onto also is crucial to prove the same for $g$.
     
<a name="152"></a>

### [Exercise 1.5.2](#toc) 

Review the proof of Theorem 1.5.6, part (ii) showing that $\mathbf{R}$ is uncountable, and then find the flaw in the following erroneous proof that $\mathbf{Q}$ is uncountable.

Assume for contradiction, that $\mathbf{Q}$ is countable. Thus we can write $\mathbf{Q} = \{r_1,r_2,...\}$ and, as before, construct a nested sequence of closed intervals with $r_n \notin I_n$. Our construction implies $\bigcap^{\infty}_{n=1}I_n = \emptyset$ while NIP implies $\bigcap^{\infty}_{n=1} I_{n} \neq \emptyset$. This contradiction implies $\mathbf{Q}$ must therefore be uncountable.

---

It doesn't work because NIP doesn't hold for $\mathbf{Q}$. Namely, the intersection need not have any rational numbers. For example, take the nested, closed intervals around $\pi$, $[3,4],[3.1,3.2],[3.12,3.13],...$, then the infinite intersection is nonempty but the only element it includes is [not rational](https://math.stackexchange.com/questions/1914901/false-proofs-claiming-that-mathbbq-is-uncountable).

_Extra_: Why doesn't the above work for integers? Since a bounded interval in $\mathbf{Z}$ has finite elements, the nested interval $I_n$ will be exhausted after finitely many steps. Thus, the construction [doesn't work](https://math.stackexchange.com/questions/2373901/is-abbotts-proof-of-the-uncountabilty-of-real-numbers-too-strong).


 Because if we have closed nested intervals $I_n \supset I_{n+1}$, and $I_i \neq \emptyset$, then there exists an $N$ such that $I_i = I_N$ for all $i>N$. Therefore, the sequence of nested intervals such that $r_n \notin I_n$ cannot be constructured. 

 _Note to myself_: How does the assumption that $\mathbf{R}$ is countable help in the proof of Theorem 1.5.6.? It helps by enabling us to index each real numbers with $n$. With this index in place, we are able to 
 
 1. construct the nested intervals, such that $r_n \notin I_n$ and 
 2. take countable intersection of the nested intervals, 
 
 which are then to show to be empty.


<a name="153"></a>

### [Exercise 1.5.3](#toc) 

Use the following outline to supply proofs for the statements in Theorem 1.5.8.

1. Prove if $A_1, \dots, A_m$ are countable sets then $A_1 \cup \dots \cup A_m$ is countable.

2. Explain why induction _cannot_ be used to prove that if each $A_n$ is countable, then $\bigcup_{n=1}^\infty A_n$ is countable.

3. Show how arranging $\mathbf{N}$ into the two-dimensional array
  $$\begin{array}{llllll}1 & 3 & 6 & 10 & 15 & \cdots \\ 2 & 5 & 9 & 14 & \cdots & \\ 4 & 8 & 13 & \cdots & & \\ 7 & 12 & \cdots & & & \\ 11 & \cdots & & & & \\ \vdots & & & & & \end{array}$$
  leads to a proof for the infinite case.

  ---

1. Suppose $A_1$ and $A_2$ are countable. Then there exist functions $f: A_1 \rightarrow N$ and $g: A_2 \rightarrow N$, both of which are onto and 1-1. Define $B_{2} = A_{2}\backslash A_{1} = \{x \in A_2: x \notin A_1 \}$. This means $A_1 \cup A_2 = A_1 \cup B_2$. Define function $h: A_1 \cup B_2 \rightarrow N$ as:

$$\begin{equation}
  h(x)=% 
  \begin{cases}
    f(x) &\text{if $x \in A_1$} \\
    g(x) &\text{if $x \in B_2$}.
  \end{cases}
\end{equation}$$

which are onto and 1-1. We can iteratively do this for $B_{3} \backslash (A_1 \cup A_2)$,... and we are done.

<span style="color:red">Some improvement: I should have started with finite case first. Consider $B_2 = \{b1, \cdots bm \}$. Also given $f: N \rightarrow A_1$. Then define $h: A_1 \cup B_2$ as  $$\begin{equation}
  h(x)=% 
  \begin{cases}
    b_{x} &\text{if $x \leq m$} \\
    f(x-m) &\text{if $x > m$}.
  \end{cases}
\end{equation}$$ </span>

<span style="color:red">If $B_2$ is infinite, then there exists $g: N \rightarrow B_2$. Then we can define $h$ by assigning odd numbers to function $f$, and even numbers to function $g$</span> 

<span style="color:red">To generalize to $m$ case, we already know it holds for two cases. Suppose this statement is true for $A_1 \cup A_2 \cup \cdots A_{m-1}$. Then $(A_1 \cup A_2 \cup \cdots A_{m-1}) \cup A_{m}$ is countable. </span> 



2. Induction is cannot be used for infinite number sets.

3. Each row represents a disjoint countable set. Their union will form the natural numbers. Therefore suppose $\{A_n\}$ are disjoint, then we can arrange them as follows:

$$\begin{array}{llllll}A_1= & a_{11} & a_{12} & \cdots & \cdots & \cdots \\ 
A_2= & a_{21} & a_{22} & \cdots & \cdots & \\ \vdots & & & & & \end{array}$$

which corresponds to 1-1 and onto mapping from $N$ to infinite unions of $A_n$.

If $\{A_n\}$ are not disjoint, iteratively construct $B_2, B_3 , \cdots$. Note that it is important to consider disjoint sets otherwise the sets may not be 1-1.

<span style="color:red"> Big pictures:

1. Use indexation $b_1, \cdots b_m$ when constructing the function $N \rightarrow \text{ some sets}$. In this question, this indexation is used to list down finite case for $B_2$ and infinite case for $A_1$. Besides, as shown in Exercise 1.5.2, indexation can also be used to construct an infinite case, which then can be used to come up with clever nested sets. Indeed, in part (iii) of this exercise, indexation is used to map $N$ to infinite union of $\{A_n\}$
2. Consider both countable and infinite case.
3. It is important to establish disjoint sets to ensure that the resulting function is 1-1. The way to do this is by excluding previous sets.
4. Exploiting the even and odd numbers of natural numbers can provide a neat trick to construct a bijection with $N$. 
5. Induction usually uses the same trick: Assume it works for 2 cases, assume it works for m cases, then m and m+1 will proceed accordingly.
6. Laying out disjoint rows of infinite sets can help with infinite number of sets, something that induction cannot.</span>

<a name="154"></a>

### [Exercise 1.5.4](#toc) 

1. Show $(a, b) \sim \mathbf{R}$ for any interval $(a, b)$.

2. Show that an unbounded interval like $(a, \infty)=\{x: x>a\}$ has the same cardinality as $\mathbf{R}$ as well.

3. Using open intervals makes it more convenient to produce the required 1-1, onto functions, but it is not really necessary. Show that $[0,1) \sim(0,1)$ by exhibiting a 1-1 onto function between the two sets.

---

1. Note that $(-\pi/2,\pi/2)$ has the same cardinality with $\mathbf{R}$ using function $ \tan x$. The latter is continuous and strictly increasing, $$ \lim_{\pm \pi/2} \tan x = \pm \infty $$ and thus is bijective.

We then need to establish that any open interval $(a,b)$ can be bijectively mapped to $(-\pi/2, \pi/2)$. This can be done by linear transformation as follow:

1. Apply the map $x-a$ so the endpoint is shift to the origin. That is, the image interval is $(0,b-a)$.
2. Rescale the interval to unit length by dividing $b-a$. The image interval is $(0,1)$.
3. Scale up the interval by the length $\pi/2 - (-\pi/2)$. The image interval is $(0, \pi)$.
4. Shift the endpoints by $-\pi/2$, The image interval is $(-\pi/2, \pi/2)$.

Composing these steps result in the bijective function $g(x) = -\pi/2 + \frac{\pi}{b-a}(x-a)$

<span style="color:red"> How do you actually establish cardinality with R? For N, we know we can index them, or lay them out in grid. For real numbers, one way is to use $\tan x$. Or linear transformation from other sets that we know have the same cardinality as R.</span>

Source: [SE1 -open interval with cardinality of $\mathbb R$ without trig identity ](https://math.stackexchange.com/questions/1434479/prove-any-open-interval-has-the-same-cardinality-of-bbb-r-without-using-tri), [SE2](https://math.stackexchange.com/questions/3320437/show-a-b-r-for-any-interval-a-b?rq=1), [Problem 1.5.4](http://www.ms.uky.edu/~ochanine/MA471G/HW_Problems.pdf), [SE3-linear transformation](https://math.stackexchange.com/questions/914823/shift-numbers-into-a-different-range), [Millersville](https://sites.millersville.edu/bikenaga/math-proof/cardinality/cardinality.pdf)

2. We will show this by sequentially mapping from $\mathbb R \to 
(a, \infty)$ as follows:

$\mathbb R \xrightarrow{f^{-1}} (-\pi/2, \pi/2) \xrightarrow{g} (0,1) \xrightarrow{h} (1, \infty) \xrightarrow{j} (a, \infty)$

From (1), we know that $f^{-1}(x) = \arctan (x)$ is a bijective function mapping $\mathbb R \mapsto (-\pi/2, \pi/2)$.

$g(x) = \dfrac{x + \pi/2}{\pi}$ is a bijection mapping $(-\pi/2, \pi/2) \mapsto (0,1)$.

$h(x) = 1/x$ is a bijection mapping $(0,1) \mapsto (1, \infty)$.

$j(x) = ax$ is a bijection mapping $(1, \infty) \mapsto (a, \infty)$.

Source: [SE1](https://math.stackexchange.com/questions/2283065/prove-that-the-intervals-0-1-and-0-infty-have-the-same-cardinality), [SE2 -open interval with cardinality of $\mathbb R$ without trig identity ](https://math.stackexchange.com/questions/1434479/prove-any-open-interval-has-the-same-cardinality-of-bbb-r-without-using-tri), [SE3 - mapping $(0, \infty)$ to $\mathbb R$](https://math.stackexchange.com/questions/573794/prove-that-mathbbr-and-the-interval-0-infty-have-the-same-cardinality),[Problem 1.5.4](http://www.ms.uky.edu/~ochanine/MA471G/HW_Problems.pdf)

3. Using open intervals makes it more convenient to produce the required 1-1, onto functions, but it is not really necessary. Show that $[0,1) \sim(0,1)$ by exhibiting a 1-1 onto function between the two sets.

Take countably infinite sequence $(x_{n})_{n \geq 1}$ of distinct elements between $0$ and $1$. Define $X$ as the set of the elements of this sequence. Let $x_{0} = 0$. Then we can construct a bijective function mapping $[0,1) \mapsto (0,1)$, $f$ by assigning $f(x_n) = x_{n+1}$ for every $n \geq 0$ and $f(x) = x$ for every $x$ in $(0,1) \backslash X$.

Source: [SE1](https://math.stackexchange.com/questions/160738/how-to-define-a-bijection-between-0-1-and-0-1)

<span style="color:red">Alternative answer:</span> Consider any sequence $0=x_1 < x_2 < \cdots < 1$. For example, consider $x_{n} = 1 - (1/n)$. Then we can define $f: [0,1) \to (0,1)$ by 

$$\begin{equation}
  f(x)=% 
  \begin{cases}
    x_{n+1} &\text{if $x =x_{n}$ for some $n \geq 1$} \\
    x &\text{if $x \neq x_{n}$}.
  \end{cases}
\end{equation}$$

Source: [Problem 1.5.4](http://www.ms.uky.edu/~ochanine/MA471G/HW_Problems.pdf)


<a name="155"></a>

### [Exercise 1.5.5](#toc) 


1. Why is $A \sim A$ for every set $A$?

2. Given sets $A$ and $B$, explain why $A \sim B$ is equivalent to asserting $B \sim A$.

3. For three sets $A, B$, and $C$, show that $A \sim B$ and $B \sim C$ implies $A \sim C$. These three properties are what is meant by saying that $\sim$ is an \emph{equivalence relation}.

---

1. Because $f(x)=x$ is a bijective function mapping $A \mapsto A$.

2. Trivial. 

3. Suppose $A \sim B$ and $B \sim C$, then there is 1-1, onto $f: A \to B$. Similarly, $g: B \to C$. 

Then if $a_1 \neq a_2$, then $f(a_{1}) \neq f(a_{2})$, which means $g(f(a_{1})) \neq g(f(a_{2}))$. Thus $g \circ f$ is 1-1.

By onto property, for all $c$, there is a $b$ such that $g(b)=c$, and there is $a$  such that $f(a) = b$, which means $g(b) = g(f(a)) = c$. This $g \circ f$ is onto.


<a name="156"></a>

### [Exercise 1.5.6](#toc) 

1. Give an example of a countable collection of disjoint open intervals.

2. Give an example of an uncountable collection of disjoint open intervals, or argue that no such collection exists.

---

1. $\{(1,1.5), (2,2.5), \cdots \}$.

2. By contradiction, suppose there is a collection of disjoint open intervals which is uncountable. We also know that each of these open intervals contain distinct element of rational numbers. Which means there are uncountable rational numbers. This contradicts Theorem 1.5.6(a).

<span style=color:red>Note 1: When they are disjoint open intervals, I could index them with $n$, which makes the collection countable. A strategy for this question is to list the elements of the collection, which means it is countable. By why is "disjoint, open" intervals a necessary conditions? What if they are either overlapping or closed? Which part of the proof will break down? </span>

<span style=color:red>Note 2: Think geometrically: There isn't enough room to fit uncountably many open intervals into $\mathbb R$ without some overlap. Source: [SE](https://math.stackexchange.com/questions/2803350/an-example-of-an-uncountable-collection-of-disjoint-open-intervals-possible) </span>

<span style=color:red>Note 3: This statement is unjustified: "Uncountable means in bijection with $\mathbb R$ ". This is essentially the continuum hypothesis, which is known to be neither provable nor disprovable. Source: [SE](https://math.stackexchange.com/questions/2803350/an-example-of-an-uncountable-collection-of-disjoint-open-intervals-possible) </span>

<span style=color:red>[Source](./pdf/mtht430f2019pm2sol.pdf)</span>

<a name="157"></a>

### [Exercise 1.5.7](#toc) 

Consider the open interval $(0,1)$, and let $S$ be the set of points in the open unit square; that is, $S=\{(x, y): 0<x, y<1\}$.

1. Find a 1-1 function that maps $(0,1)$ into, but not necessarily onto, $S$. (This is easy.)

2. Use the fact that every real number has a decimal expansion to produce a $1-1$ function that maps $S$ into $(0,1)$. Discuss whether the formulated function is onto. (Keep in mind that any terminating decimal expansion such as $.235$ represents the same real number as $.234999 \ldots .$)

---

1. $f(x) =(x, 0.5)$

2. $g(x,y) = \frac{x+y}{2}$ if $x \geq y$ and $\frac{x+y}{3}$ otherwise.

This is wrong because suppose we have $(0.2,0.2) \neq (0.3,0.1)$, but $g$ will map these into the same value. 

<span style=color:red> Answer: Suppose we have $ x  = 0.x_{1}x_{2}\cdots $ and $y = 0.y_{1}y_{2} \cdots $. Then $g(x,y) = 0.x_{1}y_{1}x_{2}y_{2} \cdots$ *(where we use terminating form over repeating 9s)* is 1-1 because given two distinct points $(x,y) \neq (s,t)$, then either $x \neq s$ or $y \neq t$, which means that at least in one decimal place we have $x_{i} \neq s_{i}$ or $y_{i} \neq t_{i}$. This function is not onto. Since the pair $x=0.79999\cdots$ and $y=0.65455\cdots$ are not allowed due to convention of terminating decimals, the point $0.7695949595\cdots$ is not in the range of $g$. Another example is the point $0.1$, which means a pair of $0.1$ and $0$ is needed, the latter is not in the domain $(0,1)$.</span>

<span style=color:red>Not too sure what this second question is trying to get at. My first thought is that given any $x, y$, we can map to $\frac{x+y}{2}$, but this is not unique, because it is equal to $\frac{y+x}{2}$. Or we can assign to $\frac{x+y}{2}$ if $x \geq y$ and $\frac{x+y}{3}$ otherwise (which is wrong due to reasons above). Alternatively, we can assign $f(x,y) = 0.xy$. But this is weird because if $x=0.9, y=0.99$, what does this lead to? (this is almost right, you just have to spell it out)</span>

<a name="158"></a>

### [Exercise 1.5.8](#toc) 

  Let $B$ be a set of positive real numbers with the property that adding together any finite subset of elements from $B$ always gives a sum of 2 or less. Show $B$ must be finite or countable.

---

The idea is to decompose $B$ into a countably many finite sets (i.e. the union of which will form $B$). This is made possible due to this condition:

> any finite subset of elements from $B$ always gives a sum of 2 or less.

The proof then is completed by theorem 1.5.8(ii).

There are a number of ways to show this. One way:

Define $B_{0}= \{x \in B \vert x>1  \}$. For each $n \in \mathbb N$, define $B_{n} = (\frac{1}{n+1},\frac{1}{n}]$. Note that each $B_{i}$ is finite because the number of distinct elements in each of them cannot exceed $2(n+1)$, otherwise the sum of the elements would be at least 2. Moreover, $B = \bigcup_{n \in \mathbb N} B_{i}$, is a union of countably many $B_{i}$. Source: [SE](https://math.stackexchange.com/questions/1724016/countability-of-set-of-positive-reals-with-bounded-sum-for-all-finite-subsets)

Second way:

Define $B_{n}= \{x \in B \vert x \geq \frac{2}{n}  \}$. Each $B_{n}$ is finite because the number of distinct elements cannot exceed $n$, otherwise the sum of the elements would be greater than 2. The proof is completed by noting that $B = \bigcup_{n \in \mathbb N} B_{i}$, is a union of countably many finite $B_{i}$. Source: [SE](https://math.stackexchange.com/questions/1724016/countability-of-set-of-positive-reals-with-bounded-sum-for-all-finite-subsets)



<span style= color:red> What does "adding together any finite subset of elements from $B$ always gives a sum of 2 or less" mean? My first thought is that given two finite subsets $(x_{1}, x_{2})$ and $(y_{1}, y_{2})$, the addition of these subsets $(x_{1}+y_{1}, x_{2}+y_{2})$ is 2 or less, which doesn't make sense. The more plausible explanation is given any finite subset of $B$, the summation of its elements is 2 or less. </span>

<span style= color:red> Damn this question must have obvious answer. I can't figure it out sigh. The solution is beautiful too. </span>

<span style = color:red> Old answer: Let $B$ be a set of positive real numbers. Assume that given any finite subset of $B$, its elements add to 2 or less. Assume that $B$ is infinite. We must show that $B$ is countable. From Theorem 1.5.8(ii), it suffices to show that each subset of $B$ is countable. </span>

<a name="159"></a>

### [Exercise 1.5.9](#toc) 

  A real number $x \in \mathbf{R}$ is called algebraic if there exist integers $a_{0}, a_{1}, a_{2}, \ldots, a_{n} \in \mathbf{Z}$, not all zero, such that
  $$
  a_{n} x^{n}+a_{n-1} x^{n-1}+\cdots+a_{1} x+a_{0}=0
  $$
  Said another way, a real number is algebraic if it is the root of a polynomial with integer coefficients. Real numbers that are not algebraic are called _transcendental_ numbers. Reread the last paragraph of Section 1.1. The final question posed here is closely related to the question of whether or not transcendental numbers exist.

 1. Show that $\sqrt{2}, \sqrt[3]{2}$, and $\sqrt{3}+\sqrt{2}$ are algebraic.
 
 2. Fix $n \in \mathbf{N}$, and let $A_{n}$ be the algebraic numbers obtained as roots of polynomials with integer coefficients that have degree $n$. Using the fact that every polynomial has a finite number of roots, show that $A_{n}$ is countable.
 
 3. Now, argue that the set of all algebraic numbers is countable. What may we conclude about the set of transcendental numbers?
  
  ---

  1. $x^{2} -2=0$; $x^{3} -2 =0$; $x = \sqrt{3}+\sqrt{2} \implies x^{2} = 5 + 2 \sqrt{6} \implies (x^{2}-5)^{2} = 24 \implies x^{4} -10x^{2} + 1 =0$

  2. Each polynomial has a finite number $k$ of roots. Moreover, each polynomial of degree $n$ can be represented by $(n+1)$-tuple of integers. Therefore $ \lvert A_{n} \rvert = k \lvert \mathbb Z^{n+1} \rvert$. But we know that $k \lvert \mathbb Z^{n+1} \rvert =k \lvert \mathbb N^{n+1} \rvert = \lvert \mathbb N^{n+1} \rvert$ as natural numbers can be bijectively mapped into integers. Finally, $\lvert \mathbb N^{n+1} \rvert = \lvert \mathbb N \rvert$ because given arbitrary element of $\lvert \mathbb N^{n+1} \rvert$, (e.g. $(a_{0}, \cdots, a_{n})$), consider its sum plus the length, and call this number as the "class" of the element. The key observation is that for each $k \in \mathbb N$, there are finite number of elements of class $k$. This is because for the element to have class $k$, the length of the element must be $\leq k$, and each member of the element must be $\leq k$. So there are at most $k^k$ elements of class $k$. We can construct an injective mapping to $\mathbb N$. We map each element of class 1 to the lowest natural numbers, then map each element of class 2 to the next lowest natural numbers and so on. (This last argument is obtained from [Nayuki](https://www.nayuki.io/page/countable-sets-and-kleene-star)).

  Alternative solution: Given a fixed $n,m \in \mathbb N$, consider the set of polynomials with integers $a_0, a_1, \cdots a_n$ such that that the sum of the absolute values is less than or equal to $m$ (alternatively, we can just take $a_0, a_1, \cdots a_n$ to be natural numbers, since $\mathbb Z$ map bijectively with $\mathbb N$). This set of polynomials of degree $n$ is finite because each integer must have absolute value less than or equal to $m$. 
  
  Let $A_{nm}$ be the set of roots of these polynomials. Since each polynomial of degree $n$ has at most $n$ roots, $\lvert A_{nm} \rvert$ is finite.

  Thus, $A_{n} = \bigcup_{n=1}^{\infty} A_{nm}$ is a union of finite sets, which by Exercise 1.5.3 implies that it is countable.

  <span style =color:green> 

  Reflection: This question teaches me new proving technique. Namely, when showing that that a n-tuple consisting of elements of a set $S$, is countable, I first must show that the that $S$ is finite. From which we can conclude that for a given $n$, the tuple is finite of order $\lvert S \rvert^{n} $. If $S$ is infinite, we can't do this. What we can, is to look at something else such that we can still map them bijectively with natural number. To do so, we replace $S$ with $N$ (possible since $S$ is countable). Then construct a class $k$ which corresponds to finite set of elements. This class $k$ can be the sum of the member of tuple plus its length. These conditions limit class $k$ size. Thus, there are $k^k$ elements. From here, we can simply list them and map with natural numbers.

  </span>

<span style =color:red> 

Earlier answer draft: 

  Every polynominal has a finite number of roots 

  $\implies$ There are countable polynomials with degree $n$

  $$\begin{array}{llllll}A_1= & a_{11} & a_{12} & \cdots & \cdots & \cdots \\ 
A_2= & a_{21} & a_{22} & \cdots & \cdots & \\ \vdots & & & & & \end{array}$$

First we show that there are countably many polynomials with degree. Given $n$, and integer $a_{ij}$ the following is the list of all possible polynomials of degree $n$:

 $$\begin{array}{llllll}\alpha_1= & a_{11} & a_{12} & \cdots & \cdots & a_{1n} \\ 
A_2= & a_{21} & a_{22} & \cdots & \cdots & \\ \vdots & & & & & \end{array}$$

</span>

3. As $A_n$ is countable, the infinite union of $A_n$, i.e. the set of algebraic numbers, is also countable by Exercise 1.5.3. 

Let $A$ be the set of algebraic numbers, and $T$ be the set of transcedental numbers. Clearly, $A \cup T = \mathbb R$. Thus $T$ cannot be countable, since otherwise it implies $R$ is countable.

<a name="1510"></a>

### [Exercise 1.5.10](#toc) 

1. Let $C \subseteq[0,1]$ be uncountable. Show that there exists $a \in(0,1)$ such that $C \cap[a, 1]$ is uncountable.
2. Now let $A$ be the set of all $a \in(0,1)$ such that $C \cap[a, 1]$ is uncountable, and set $\alpha=\sup A$. Is $C \cap[\alpha, 1]$ an uncountable set?
3. Does the statement in (a) remain true if "uncountable" is replaced by "infinite"?

---

1. Suppose by contradiction $\forall a \in (0,1), C \cap [a,1]$ is countable. It follows that $$ \bigcup_{n \geq 1} C \cap [\frac{1}{n},1]$$ is countable by Exercise 1.5.3. But this is equal to $C \cap [0,1]$, which is uncountable.

<span style=color:green>
Damn I fucked up this question. Took me so long to figure out. Anyhow, a lesson here is to look for a special case that I can generalize to the question. In this case, using  

$\frac{1}{n}$.

</span> 

<span style=color:red> 
Earlier draft:

$C$ is uncountable $\implies$ it is not bijectively mapped with $\mathbb N$

$C \subseteq [0,1] \implies C = [a,b]$ or $(a,b)$ for $a,b \in [0,1]$.

Suppose for all $a \in (0,1)$, $C \cap [a,1] = K $ is countable. Thus, there exist a bijective map $f: \mathbb N \to K$. Suppose $C$ is a closed interval. Then $K$ is a closed interval. And we know from exercise 1.5.4 that a closed interval is uncountable. Similarly, if $K$ is not a closed interval, then we know that is uncountable.

</span>

2. Suppose $C \cap [\alpha,1]$ is uncountable. . Given any arbitrary $\frac{1}{n} >0$, $C \cap [\alpha + \frac{1}{n}, 1]$ is countable. Which means $ \bigcup_{n \geq 1} C \cap [\alpha + \frac{1}{n}, 1]$ is countable by Exercise 1.5.3. But this is equal to $C \cap [\alpha,1]$, which is uncountable. This is a contradiction.

3. No. Take the sequence $1 = x_{1} > x_{2} > \cdots > 0$. For example, consider the sequence  $x_{n} = (\frac{1}{n})$. Let $X$ be the set of this sequence, and thus $X \subseteq [0,1]$ and it is infinite. It follows that $X \cap [a,1]$ is finite. This is because the intersection is equal to $\{x_{n0}, x_{n0-1}, \cdots, x_{1} = 1\}$ where $x_{n0} \geq a$.


<a name="1511"></a>

### [Exercise 1.5.11](#toc) 

Schröder-Bernstein Theorem:
  Assume there exists a 1-1 function $f: X \rightarrow Y$ and another 1-1 function $g: Y \rightarrow X .$ Follow the steps to show that there exists a 1-1, onto function $h: X \rightarrow Y$ and hence $X \sim Y$.
  The strategy is to partition $X$ and $Y$ into components
  $$
  X=A \cup A^{\prime} \quad \text { and } \quad Y=B \cup B^{\prime}
  $$
  with $A \cap A^{\prime}=\emptyset$ and $B \cap B^{\prime}=\emptyset$, in such a way that $f$ maps $A$ onto $B$, and $g$ maps $B^{\prime}$ onto $A^{\prime}$.

  1. Explain how achieving this would lead to a proof that $X \sim Y$.

  2. Set $A_{1}=X \setminus g(Y)=\{x \in X: x \notin g(Y)\}$ (what happens if $\left.A_{1}=\emptyset ?\right)$ and inductively define a sequence of sets by letting $A_{n+1}=g\left(f\left(A_{n}\right)\right)$. Show that $\left\{A_{n}: n \in \mathbf{N}\right\}$ is a pairwise disjoint collection of subsets of $X$, while $\left\{f\left(A_{n}\right): n \in \mathbf{N}\right\}$ is a similar collection in $Y$.
  
  3. Let $A=\bigcup_{n=1}^{\infty} A_{n}$ and $B=\bigcup_{n=1}^{\infty} f\left(A_{n}\right)$. Show that $f$ maps $A$ onto $B$.
  
  4. Let $A^{\prime}=X \setminus A$ and $B^{\prime}=Y \setminus B$. Show $g$ maps $B^{\prime}$ onto $A^{\prime}$.
 
  ---

  1. It will establish that there is a 1-1 function from $A$ onto $B$, and that there is a 1-1 function from $B^{\prime}$ onto $A^{\prime}$. Given that $A \cap A^{\prime}=\emptyset$ and $B \cap B^{\prime}=\emptyset$, we can establish a bijective mapping $A \to B$ as follows:
  $ h(x) = \begin{cases} 
      f(x) & x \in A \\
      g^{-1}(x) & x \in A^{\prime}   
   \end{cases} $

  2. If $A_{1}$ is empty, then $g(Y)$ bijectively mapped $Y$ to $X$. Suppose $A_{1}$ is not empty. Then for $i \geq 2$, $A_{1} \cap A_{i} = \emptyset$ because $A_{i} \subseteq g(Y)$.

  Given arbitrary $m,n$ and $1 <m < n$, suppose that $A_{m} \cap A_{n} \neq \emptyset$. Let $x$ be an element in both $A_m$ and $A_n$. Namely, $x \in A_m = g(f(A_{m-1}))$ and $x \in A_n = g(f(A_{n-1}))$. It follows that $f^{-1}(g^{-1}(x)) \in A_{m-1}$ and $f^{-1}(g^{-1}(x)) \in A_{n-1}$. Which means that $A_{m-1} \cap A_{n-1} \neq \emptyset$. But if we continue this way, $A_{1} \cap A_{m-n+1} \neq \emptyset$, which is a contradiction.

  Since $f$ is a 1-1 function, it follows that $\left\{f\left(A_{n}\right): n \in \mathbf{N}\right\}$ is also a collection of pairwise disjoint subsets in $Y$.

   <span style=color:green>Reflection: I wasn't too sure how to proceed at first. Mainly because I was trying to rationalize what on earth all these are for. And when I try to show $A_{1}$ and $A_{2}$ are disjoint, I try to visualise these, which make it all the more confusing. What helps is that I took an incremental step by step approach. A key observation is that $A_i$ for $i \geq 2$, these are a subset of $g(Y)$, which simplifies a lot of things. Another key observation is we make use of the fact that $A_{i}$ is built recursively, thus, it makes it easy to start from a general case, and simplifies it to a specific case of $A_{1}$.</span>

   <span style=color:red>Earlier draft: Trying to understand the big picture here. So $A_{1}=X \setminus g(Y)=\{x \in X: x \notin g(Y)\}$ is the set consisting of $x$ which are not paired with any $Y$ under $g$. Then we take these residual $x$, and map them back to $Y$ under $f$. These resulting $y$ are then mapped back to $X$ under $g$. This is called $A_{2}$. Then this is mapped back to $Y$ under $g$, before mapped again to $X$, under $f$. This is called $A_{3}$.... and why are we doing this? I don't understand. Isn't it obvious already $X$ and $Y$ can be bijectively mapped?</span>

  3. Given arbitrary $b \in B$, there is $f(A_{i})$ such that $b \in f(A_{n}) \subseteq B$. Moreover, since all $a \in A$ is in some $A_{n}$, there exist $a$ such that $b = f(a)$.

  4. Let $x \in A^{\prime}$. There exists some $b \in Y$ such that $g(b) = a^{\prime}$ since otherwise $a^{\prime}$ would be in $A_{1}=X \setminus g(Y)$. Suppose $b \in B$. Then $b \in f(A_{n})$ for some $n$. But this means that $a = g(b) \in g(f(A_{n})) = A_{n+1}$, which is a contradiction.
  
  <span style = color:green>It's also nice to show that $g$ indeed maps from $B^{\prime}$ to $A^{\prime}$. Suppose $g(b^{\prime}) = a \in A$. It follows that $g(b^{\prime}) \in g(f(A_{n}))$, which means $b^{\prime} \in f(A_{n})$, which is a contradiction. Got help from [SE1](https://math.stackexchange.com/questions/3982170/schröder-bernstein-theorem-proof-help?rq=1) and [SE2](https://math.stackexchange.com/questions/1726578/understanding-a-proof-of-schröder-bernstein-theorem).</span>

<a name="161"></a>

### [Exercise 1.6.1](#toc)

 Show that $(0,1)$ is uncountable if and only if $\mathbf{R}$ is uncountable.

 ---

 $\mathbb R \xrightarrow{f^{-1}} (-\pi/2, \pi/2) \xrightarrow{g} (0,1)$

From (1), we know that $f^{-1}(x) = \arctan (x)$ is a bijective function mapping $\mathbb R \mapsto (-\pi/2, \pi/2)$.

$g(x) = \dfrac{x + \pi/2}{\pi}$ is a bijection mapping $(-\pi/2, \pi/2) \mapsto (0,1)$.

Thus $\mathbb R \sim (0,1)$.

<a name="162"></a>

### [Exercise 1.6.2](#toc)

 Let $f : \mathbf{N} \to \mathbf{R}$ be a way to list every real number (hence show $\mathbf R$ is countable).

  Define a new number $x$ with digits $b_1b_2\ldots$ given by
  $$
  b_{n}= \begin{cases}2 & \text { if } a_{n n} \neq 2 \\ 3 & \text { if } a_{n n}=2\end{cases}
  $$

  1. Explain why the real number $x=. b_{1} b_{2} b_{3} b_{4} \ldots$ cannot be $f(1)$.
  2. Now, explain why $x \neq f(2)$, and in general why $x \neq f(n)$ for any $n \in \mathbf{N}$.
  3. Point out the contradiction that arises from these observations and conclude that $(0,1)$ is uncountable.

  ---

  1. Suppose the first digit in the decimal expansion of $f(1)$ is 2. Then $f(1)$ is different from $x$ because digit $b_{1}$ is 3. Similarly, if the first digit is other than $2$, then $f(1)$ is different from $x$ because digit $b_{1}$ is 2.

  2. The same argument as (1) (replace $1$ with $n$).

  3. $x$ is not in the array. This contradicts the assumption that every real number is in correspondance with $\mathbb N$.

<a name="163"></a>

### [Exercise 1.6.3](#toc)

Supply rebuttals to the following complaints about the proof
of Theorem 1.6.1.

1. Every rational number has a decimal expansion, so we could apply this same argument to show that the set of rational numbers between $0$ and $1$ is uncountable. However, because we know that any subset of $\mathbb Q$ must be countable, the proof of Theorem 1.6.1 must be flawed.

2. Some numbers have two different decimal representations. Specifically, any decimal expansion that terminates can also be written with repeating $9$’s. For instance, $1/2$ can be written as $.5$ or as $.4999 \cdots$. Doesn’t this cause some problems?

---

1. Decimal expansion of $\mathbb Q$ is terminating or repeating. Meanwhile the constructed $x$ is not guaranteed to be of this form.

2. Since our options are just $2$ and $3$, we avoid repeating $9$'s.


<a name="164"></a>

### [Exercise 1.6.4](#toc)

Let S be the set consisting of all sequences of $0$’s and $1$’s. Observe that S is not a particular sequence, but rather a large set whose elements are sequences; namely, $$ S = \{(a_{1}, a_{2}, a_{3}, \cdots) : a_{n} = 0 \text{ or } 1\}.$$ As an example, the sequence $(1,0,1,0,1,0,1,0,\cdots)$ is an element of $S$, as is the sequence $(1,1,1,1,1,1,\cdots)$. Give a rigorous argument showing that $S$ is uncountable.

---

Proceeding with Cantor's approach, we assume that there is a bijective correspondance with $\mathbb N$, and lay out all the elements in the following array, say,

$$\begin{array}{lllll}f(1)= & 0 & 1 & \cdots & \cdots  \\ 
f(2)= & 1& 1 & \cdots & \cdots \\ \vdots & & & &  \end{array},$$

which can be generalized to a doubly indexed array

$$\begin{array}{lllll}f(1)= & a_{11} & a_{12} & \cdots & \cdots  \\ 
f(2)= & a_{21} & a_{22} & \cdots & \cdots \\ \vdots & & & &  \end{array}$$

Define $x = b_{1}b_{2} \cdots$ such that:

$$b_{n} = \begin{cases} 
      1 & a_{nn} = 0 \\
      0 & a_{nn} = 1.   
   \end{cases}$$

Thus, $x$ is not in the array, which is a contradiction.

<a name="165"></a>

### [Exercise 1.6.5](#toc)

1. Let $A = \{a, b, c\}$. List the eight elements of $P(A)$. (Do not forget that $\emptyset$ is considered to be a subset of every set.)

2. If $A$ is finite with $n$ elements, show that $P(A)$ has $2^n$ elements.

---

1. $\{ \emptyset, \{a\}, \{b\}, \{c\}, \{a,b\}, \{a,c\},\{b,c\}, \{a,b,c\} \}$

2. For each element in $A$, it can either be in a subset or not. Since there are $n$ elements, there are $2^{n}$ possible combinations of distinct subsets.

<span style = color:red>Each subset is associated with a sequence of length $n$ of Yes or No</span>

<a name="166"></a>

### [Exercise 1.6.6](#toc)

1. Using the particular set $A = \{a, b, c\}$, exhibit two different 1–1 mappings from $A$ into $P(A)$.

2. Letting $C = \{1,2,3,4\}$, produce an example of a 1–1 map $g : C \to P(C)$.

3. Explain why, in parts (a) and (b), it is impossible to construct mappings that are _onto_.

---

1. Mapping 1: $a \to \{a\}$; $b \to \{b\}$; $c \to \{c\}$

Mapping 2: $a \to \{a,b\}$; $b \to \{b,c\}$; $c \to \{a,c\}$

2. $1 \to \{1\}$; $2 \to \{2\}$; $3 \to \{3\}$; $4 \to \{4\}$

3. Because there are more elements in $P(A)$ and $P(C)$ than $A$ and $C$.



<a name="167"></a>

### [Exercise 1.6.7](#toc)

Cantor's Theorem. Given any set $A$, there does not exist a function $f: A \to P(A)$ that is onto. For each element $a \in A$, $f(a)$ is a particular subset of $A$. The assumption that $f$ is onto means that every subset of $A$ appears as $f(a)$ for some $a \in A$. To arrive at a contradiction, we will produce a subset $B \subseteq A$ that is not equal to $f(a)$ for any $a \in A$.

Construct $B$ using the following rule. For each element $a \in A$, consider the subset $f(a)$. This subset of $A$ may contain the element $a$ or it may not. This depends on the function f. If $f(a)$ does not contain a, then we include $a$ in our set $B$. More precisely, let $$B = \{ a \in A : a \notin f ( a ) \}$$ .

Return to the particular functions constructed in Exercise 1.6.6 and construct the subset $B$ that results using the preceding rule. In each case, note that $B$ is not in the range of the function used.

---

$B = \{\emptyset\}$

<a name="168"></a>

### [Exercise 1.6.8](#toc)

We now focus on the general argument. Because we have assumed that our function $f : A \to P(A)$ is onto, it must be that $B = f(a^{\prime})$ for some $a^{\prime} \in A$. The contradiction arises when we consider whether or not $a^{\prime}$ is an element of $B$.

1. First, show that the case $a^{\prime} \in B$ leads to a contradiction.

2. Now, finish the argument by showing that the case $a^{\prime} \notin B$ is equally unacceptable.

---

1. Suppose $a^{\prime} \in B$. But this contradicts the definition of $B$ which excludes any $a \in f (a)$.

2. Suppose $a^{\prime} \notin B$. Which means $a^{\prime} \notin f(a^{\prime})$. But by definition of $B$, $a^{\prime} \in B$.

<a name="169"></a>

### [Exercise 1.6.9](#toc)

Using the various tools and techniques developed in the last two sections (including the exercises from Section 1.5), give a compelling argument showing that $P (N) \sim R$.

---

We use the fact that $(0,1)$ has the same cardinality as $\mathbb R$. We also will use the fact that $P(\mathbb N)$ has the same cardinality as the set $S$ of all sequences of $0$'s and $1$'s, namely $$S = \{(a_{1},a_{2},a_{3},\cdots) : a_{n} = 0 \text{ or } 1\}.$$ To prove the latter, for each $x \in P(\mathbb N)$, define an element of $s = (s_{1}, s_{2}, s_{3} \cdots)$ such that:

$$s_{n} = \begin{cases}
      1 & n \in x \\
      0 & n \notin x.
    \end{cases}$$

(or alternatively, define $f(x) = \sum_{n\in x} 10^{-n}$).

This correspondance is 1-1 because given different elements $x_{1}, x_{2} \in P(\mathbb N)$, there will be at least one natural number $n$ that is in one but not the other. It follows that the resulting $s$'s will differ in at least  one position, $s_n$.

It is also onto because given any $s \in S$, it corresponds to a unique subset of natural numbers, consisting of $n$th position of the non-zero elements.


We next show that there is a 1-1 correspondance from $S$ to $(0,1)$. Given $s = (s_{1}, s_{2}, s_{3}, \cdots)$ define $f(s) = .s_{1}s_{2}s_{3} \cdots$. Given $s \neq s^{\prime}$, they differ in at least one position $s_{i} \neq s_{i}^{\prime}$, which means $f(s) \neq f(s^{\prime})$. (Why is it not onto? Take $0.12344$. Then there is no corresponding element in $s$, which consists of only $1$'s and $0$'s)

Next we show that there is a 1-1 corresponding from $(0,1)$ to $S$. Given $x \in (0,1)$, we ascertain whether $x$ is in the bottom half $(0,0.5]$ or top half $(0.5,1)$. If it is in top half, define $s_{1} =1$, and $0$ otherwise. WLOG, suppose $x$ is in bottom half, identify whether $x$ is in the bottom half $(0,0.25]$ or the top half $(0.25, 0.5)$. If it is in the top half, let $s_{2} = 1$, and $0$ otherwise.  Continuing with this, we obtain a 1-1 correspondance because $s$ is uniquely determined for each $x$.

Our proof is completed using Schröder-Bernstein Theorem.

<span style = color:green>The mapping from $P(\mathbb N)$ and $S$ is interesting because one is a set (order or repetition doesn't matter) and the other is a tuple (order and repetition matter). So to ensure consistency, we use the $n$th position of the tuple, in which case we don't allow for any repetition, and there is only one unique order. This is different from the mapping from $S$ to $(0,1)$, because in both, repetition and order matter. Although the complication with $(0,1)$ is that a number can be represented differently in the form of repeating $9$'s, but this is not an issue here because we are dealing with $0$'s and $1$'s only. </span>

<span style =color:red>Wrong answer: Let an element of $P(\mathbb N)$ be $x=\{n_{1}, n_{2}, n_{3}, \cdots \}$. Establish a map $f: P(\mathbb N) \to (0,1)$ by setting $f(x) = .n_{1}n_{2}n_{3}\cdots$. $f$ is 1-1 because given two distinct elements of $P(\mathbb N)$, $f(x)$ will differ in at least one decimal place. $f$ is onto because given any $y=.n_{1}n_{2}n_{3}\cdots$, it corresponds to $x = \{n_{1}, n_{2}, n_{3}, \cdots\}$ thus $f(x) = y$. We also know that $(0,1)$ bijectively mapped to $\mathbb R$.

<span style=color:red>This is wrong. Think about $y_{1} = 0.442$ and $y_{2} = 0.422$. Both corresponds to $x = \{4,2\}$, which means $f(x)$ could have two images, therefore this is not a well-defined function. Similarly $f(x)$ can also equal $0.42$ or $0.24$.</span>

<span style = color:red> Discarded answer. Next we show that there is a 1-1 corresponding from $(0,1)$ to $S$. Given $x \in (0,1)$, we ascertain whether $x$ is in the bottom half $(0,0.5]$ or top half $(0.5,1)$. If it is in top half, define $s_{1} =1$, and $0$ otherwise. WLOG, suppose $x$ is in bottom half, identify whether $x$ is in the bottom half $(0,0.25]$ or the top half $(0.25, 0.5)$. If it is in the top half, let $s_{2} = 1$, and $0$ otherwise.  <span style = color:yellow>The next sentences are discarded because it doesn't take into account the top half. Also, we can simply assert 1-1 correspondance by stressing how $s$ is uniquely determined. </span> More generally, suppose after $n-1$ steps, identify whether whether $x$ is in the bottom half $(0, \frac{1}{2^{n}}]$ or the top half $(\frac{1}{2^{n}}{1})$, in which case $s_{n}$ is assigned $1$ if it's in the top half, and $0$ otherwise. This correspondence is 1-1 because given different $x$'s, after some finite steps of the iteration, one will be in the top while the other in the bottom half </span>

<a name="1610"></a>

### [Exercise 1.6.10](#toc)

As a final exercise, answer each of the following by establishing a 1–1 correspondence with a set of known cardinality.

1. Is the set of all functions from $\{0, 1\}$ to $\mathbb N$ countable or uncountable? 
2. Is the set of all functions from $\mathbb N$ to $\{0, 1\}$ countable or uncountable?
3. Given a set $B$, a subset $A$ of $P (B)$ is called an antichain if no element of $A$ is a subset of any other element of $A$. Does $P (\mathbb N)$ contain an uncountable antichain?

---
1. For preimage $0$, it can be mapped to $\mathbb N$ elements, and the same for preimage $1$. Thus there are $\mathbb N \times \mathbb N$ possibilities, which has the same cardinality as $\mathbb N$. This is countable.

2. For preimage $1$, it can be mapped to $2$ elements, and the same for preimage $2$, $3$, and so on. Thus there are $2^{\mathbb N}$ possibilities. But this is the same cardinality as $P(\mathbb N)$, which are uncountable.

3. To construct an element of antichain, we can consider each element  $P(\mathbb N)$ and categorize it into "include" or "exclude". Thus each element of antichain can be represented by a sequence of length $2^{\mathbb N}$ of "include" or "exclude". We also note that each element of $P(\mathbb N)$ is also an antichain of size 1. This implies cardinality of at least $2^{\mathbb N}$, which therefore is not countable.

<span style=color:green>Note to self: Antichain is the collection of subsets of $B$ which are not a subset of any other subsets in the collection. For $\mathbb N$, an example of antichain is $\{\{a\}\}, \{\{b\}\},\{\{a\}, \{b\}\}, \cdots$ </span>



<span style=color:red>Early draft: Funny thing is that I don't even know what the question means. Given a well-defined function $f$, it can be either many-1 -- in which case both $0$ and $1$ are mapped into the same $n \in \mathbb N$, which means there can be $\mathbb N$ such functions --  </span>

<a name="c2"></a>

## Chapter 2 


<a name="221"></a>

### [Exercise 2.2.1](#toc)

What happens if we reverse the order of the quantifiers in Definition 2.2.3?

_Definition: A sequence $(x_{n})$ verconges to $x$ if there exists an $\epsilon > 0$ such that for all $N \in \mathbb N$ it is true that $n \geq N$ implies $|x_{n} −x|< \epsilon$._

Give an example of a vercongent sequence. Is there an example of a vercongent sequence that is divergent? Can a sequence verconge to two different values? What exactly is being described in this strange definition?

***

Take the sequence $x_{n} =(1/n)_{n \geq 1}$. And consider $\epsilon =10$. Then for all $N \in \mathbb N$, $n \geq N$ implies $|x_{n} - 0| \leq 10$.

Take the sequence $(1, -1, 1, -1, \cdots)$ and $\epsilon = 10$. Again, it verconges to $0$.

It can converge to different value.  In the example above, the sequence also verconges to 2 for instance.

This resembles a bounded sequence such that there exists a positive number $\epsilon$ whereby $|x_{n} - x| < \epsilon$ for all $n \in \mathbb N$.


<a name="222"></a>

### [Exercise 2.2.2](#toc)

Verify, using the definition of convergence of a sequence, that the following sequences converge to the proposed limit.

1. $\lim \frac{2n+1}{5n+4} = \frac{2}{5}$

2. $\lim \frac{2n^{2}}{n^{3} +3}=0$

3. $\lim \frac{\sin (n^{2})}{\sqrt[3]{n}}=0$

***

1. $|\frac{2n+1}{5n+4} - \frac{2}{5} | = |\frac{10n+5-10n -8}{25n+20} | = |\frac{-3}{25n+20}|= \frac{3}{25n+20}< \epsilon$, which is equivalent to saying $3 < 25n \epsilon +20\epsilon \iff 25n\epsilon >3-20\epsilon \iff n > \frac{3-20\epsilon}{25\epsilon}.$ 

Thus given any $\epsilon>0$, let $N = \frac{3-20\epsilon}{25\epsilon}$. For $n \geq N$, $| \frac{2n+1}{5n+4} - \frac{2}{5} | = \frac{3}{25n+20} < \epsilon$.

2. $|\frac{2n^{2}}{n^{3}+3}|< \frac{2n^{2}}{n^{3}} = \frac{2}{n} < \epsilon \iff n > \frac{2}{\epsilon}.$

Thus given any $\epsilon$, let $N = \frac{2}{\epsilon}$. For any $n \geq N$, $|\frac{2n^{2}}{n^{3}+3}| < \epsilon.$

3. $|\frac{\sin(n^{2})}{\sqrt[3]{n}}| \leq \frac{1}{\sqrt[3]{n}}<\epsilon \iff n > \frac{1}{\epsilon^{3}}$.

Thus given any $\epsilon>0$, let $N = \frac{1}{\epsilon^{3}}$, then for $n \geq N$, $|\frac{\sin(n^{2})}{\sqrt[3]{n}}| \leq \frac{1}{\sqrt[3]{n}} < \epsilon.$ 

<a name="223"></a>

### [Exercise 2.2.3](#toc)

Describe what we would have to demonstrate in order to disprove each of the following statements.

- At every college in the United States, there is a student who is at least seven feet tall.
- For all colleges in the United States, there exists a professor who gives every student a grade of either A or B.
- There exists a college in the United States where every student is at least six feet tall.

***

- There exists a college in the United States such that all students are less than seven feet tall.
- There exists a college in the United States such that all professors don't give every student a grade of either A or B. (ie such at all professors gives some students a grade other than A or B)
- For all colleges in the United States, there exists a student who is less than six feet tall. 

<a name="224"></a>

### [Exercise 2.2.4](#toc)

Give an example of each or state that the request is impossible. For any that are impossible, give a compelling argument for why that is the case.

1. A sequence with an infinite number of ones that does not converge to one.

2. A sequence with an infinite number of ones that converges to a limit not equal to one.

3. A divergent sequence such that for every $n \in \mathbb N$ it is possible to find n consecutive ones somewhere in the sequence.

***

1. $(1, -1, 1, -1, \cdots)$

2. Impossible. Suppose the limit is some real number $k \neq 1$. Then for all $N \in \mathbb N$, there exist sequence terms $x_{n}$, $ n \geq N$ such that $|x_{n} - k| >0$. Setting $\epsilon = |x_{n} - k|/2$, these terms fall outside the $\epsilon$-neighborhood of $k$, $V_{\epsilon}(k)$.

3. $(1,-1,1,1,-1,1,1,1,-1, \cdots)$


<a name="225"></a>

### [Exercise 2.2.5](#toc)

Let $[[x]]$ be the greatest integer less than or equal to $x$. For example, $[[\pi]] = 3$ and $[[3]] = 3$. For each sequence, find $\lim_{a_{n}}$ and verify it with the definition of convergence.

1. $a_{n} = [[5/n]]$,
2. $a_{n} = [[(12 + 4n)/3n]]$.

Reflecting on these examples, comment on the statement following Definition 2.2.3 that “the smaller the $\epsilon$-neighborhood, the larger $N$ may have to be.”

***

1. The sequence is $(5, 3, 2, 2,1,1,1, \cdots)$. For any $epsilon>0$, let $N = 5$. Thus for all $n \geq N$, $[[5/n]]=1$, which means $|a_{n} -1|=0 < \epsilon$. The limit is therefore $1$.

2. $a_{n} = [[4/n + 4/3]]$, thus the sequence would be an infinite sequence of $2$'s for $n \geq 6$. The limit is $2$.

<a name="226"></a>

### [Exercise 2.2.6](#toc)


Prove Theorem 2.2.7. To get started, assume $(a_{n}) \to a$ and also that $(a_{n}) \to b$. Now argue $a = b$.

***

For all $\epsilon>0$, there exists $N_{1}$ such that $|a_{n} -a| < \epsilon$ for $n \geq N_{1}$. 

Similarly, $|a_{n}-b| < \epsilon$ for $n \geq N_{2}$ for some $N_{2}$. 

Let $N = \max \{N_{1}, N_{2}\}$. Suppose $a \neq b$, and let  $\epsilon = |b-a|/2$.

$|b-a|= |b-a_{n} + a_{n} -a| = |(b-a_{n}) + (a_{n} -a)| \leq |b-a_{n}| + |a_{n} -a| < 2\epsilon = 2|b-a|/2$, where the first inequality use Triangle Inequality. But this is a contradiction.

<a name="227"></a>

### [Exercise 2.2.7](#toc)

Here are two useful definitions:

1. A sequence $(a_{n})$ is eventually in a set $A \subseteq \mathbb R$ if there exists an $N \in \mathbb N$ such that $a_{n} \in A$ for all $n \geq \mathbb N$.

2. A sequence $(a_{n})$ is frequently in a set $A \subseteq \mathbb R$ if, for every $N \in \mathbb N$, there exists an $n\geq\mathbb N$ such that $a_{n} \in A$.

- Is the sequence $(−1)^{n}$ eventually or frequently in the set $\{1\}$?
- Which definition is stronger? Does frequently imply eventually or does eventually imply frequently?
- Give an alternate rephrasing of Definition 2.2.3B using either frequently or eventually. Which is the term we want?
- Suppose an infinite number of terms of a sequence $(x_{n})$ are equal to $2$. Is $(x_{n})$ necessarily eventually in the interval $(1.9,2.1)$? Is it frequently in $(1.9, 2.1)$?

***

- Frequently
- Eventually is stronger. It implies frequently
- A sequence $(a_{n})$ converges to $a$, if it is is eventually in any given $\epsilon$-neighborhood $V_{\epsilon}(a)$.
- It is not necessarily eventually, for example the sequence $(1,2,1,2, \cdots)$ has infinitely many $2$. It is frequently.

<a name="228"></a>

### [Exercise 2.2.8](#toc)

For some additional practice with nested quantifiers, consider the following invented definition:
    Let’s call a sequence $(x_{n})$ zero-heavy if there exists $M \in \mathbb N$ such that for all $N \in \mathbb N$ there exists $n$ satisfying $N \leq n \leq N + M$ where $x_{n} = 0$.

1. Is the sequence $(0, 1, 0, 1, 0, 1, \cdots)$ zero heavy?
2. If a sequence is zero-heavy does it necessarily contain an infinite number
of zeros? If not, provide a counterexample.
3. If a sequence contains an infinite number of zeros, is it necessarily zero- heavy? If not, provide a counterexample.
4. Form the logical negation of the above definition. That is, complete the sentence: A sequence is not zero-heavy if $\cdots$

***

1. Yup.
2. Yup. Suppose it does not contain an infinite number of zeros. Then for some $K \in \mathbb N$, $a_{n} \neq 0$ for all $n \geq K$.
3. Yup. <span style=color:red>Wrong. Let's rephrase this to disprove this statement: given any $M$, there exists $N$ such that for all $n$ satisfying $N \leq n \leq N + M$,  $x_{n} \neq 0$. Then it's clear that we can simply create a sequence of infinite $0$, with growing gaps between them; e.g. $(1,0,1,1,0,1,1,1,0,1,1,1,1, \cdots)$, or sequence of $(a_{n})$ such that $a_{n} =0$ if $n = 2^{k}$ for $k \in \mathbb N$, and $0$ otherwise. In the latter case, given any $M$, we pick $k$ such that $2^{k+1} - (2^{k}+1)>M$. It follows that $\{x_{n} | (2^{k}+1) \leq n \leq (2^{k}+1)+M\}$ are not zero.</span>
4. A sequence is not zero-heavy if for all $M \in \mathbb N$, there exists $N \in \mathbb N$ such that no $n$ satisfies $N \leq n \leq N+M$ where $x_{0}=0$.

<a name="231"></a>

### [Exercise 2.3.1](#toc)

Let $x_{n} \geq 0$ for all $n \in \mathbb N$.

1. If $(x_{n}) \to 0$, show that $(\sqrt{x_{n}}) \to 0$. 
2. If $(x_{n}) \to x$, show that $(\sqrt{x_{n}}) \to \sqrt{x}$.

***

1. $|x_{n}-0| = x_{n} < \epsilon^{2}$ for all $n \geq N$, for some $N$. Which implies $\sqrt{x_{n}} = |\sqrt{x_{n}}-0| <\epsilon$.

<span style="color:green"> Important concept: Applying increasing function to both sides of inequality preserves it, while applying decreasing function to both sides reverses it. </span>

<span style="color:red"> Wrong answer. $x_{n}^{2} \to 0$ by algebraic limit theorem (iii). And $\lim (\frac{x_{n}}{x_{n}^{2}}) =0/0$. But $b = 0$ though. </span>

2. Assume $x>0$, as otherwise this statement reduces to exercise (i). We want to show that  $|\sqrt{x_{n}}-\sqrt{x}|<\epsilon$ for all $n \geq N$ for some $N$. 

 Note that $|x_{n}-x|=|\sqrt{x_{n}}-\sqrt{x}||\sqrt{x_{n}}+\sqrt{x}|$, which implies $|\sqrt{x_{n}}-\sqrt{x}|=\frac{|x_{n}-x|}{|\sqrt{x_{n}}+\sqrt{x}|}$.

Since $|\sqrt{x_{n}}+\sqrt{x}|=\sqrt{x_{n}}+\sqrt{x}\geq \sqrt{x}$, this implies $|\sqrt{x_{n}}-\sqrt{x}|\leq \frac{|x_{n}-x|}{\sqrt{x}}$.

As $(x_{n}) \to x$, there exists some $N$ such that $|x_{n}-x| < \epsilon \sqrt{x}$ for all $n \geq N$. It follows that $|\sqrt{x_{n}}-\sqrt{x}|< \frac{\epsilon \sqrt{x}}{\sqrt{x}} =\epsilon$ for all $n \geq N$.


<span style="color:green"> Damn, all these basic identities which idc about are KEY to these qestions... ie $a^{2}-b^{2} = (a-b)(a+b)$. </span>

<span style="color:red"> Early draft: We know $x$ is positive from limit theorem. $|x_{n}-x| < \epsilon \implies |x_{n}| < |x| + \epsilon \implies  x_{n}<x+\epsilon \implies \sqrt{x_{n}} < \sqrt{x + \epsilon}$</span>

<span style="color:red">To find appropriate value of $\epsilon$, $x+ k = \epsilon^{2} \implies k = \epsilon^{2}-x$, but this is not necessarily positive for all $k$</span>

<a name="232"></a>

### [Exercise 2.3.2](#toc)

Using only Definition 2.2.3, prove that if $(x_{n}) \to 2$, then 
1.  $\frac{2x_{n}−1}{3} \to 1$;
2. $\frac{1}{x_{n}} \to \frac{1}{2}$

(For this exercise the Algebraic Limit Theorem is off-limits, so to speak.)

***

1. The goal is to find $N$ such that

$|\frac{2x_{n}-1}{3}-1| = |\frac{2x_{n}}{3}-\frac{4}{3}|=\frac{2}{3}|x_{n}-2|<\epsilon$ for all $n \geq N$.

But we know that $|x_{n}-2|<3\epsilon$/2 for all $n \geq N$ for some $N$. Plugging this in, we are done.

2. Similarly, $|\frac{1}{x_{n}}- \frac{1}{2}|=|\frac{2-x_{n}}{2x_{n}}|=|\frac{1}{2x_{n}}||2-x_{n}|$.


Since $x_{n}$ is convergent, it is bounded $|x_{n}| \leq M$, where $M>0$. Thus selecting $N$ such that $|2-x_{n}|<2\epsilon M$ for all $n \geq N$, we finish the proof by noting that $\frac{1}{2x_{n}}||2-x_{n}| < |\frac{1}{2M}||2\epsilon M| = \epsilon$


<a name="233"></a>

### [Exercise 2.3.3](#toc)

(Squeeze Theorem). Show that if $x_{n} \leq y_{n} \leq z_{n}$ for all $n \in \mathbb N$, and if $\lim x_{n} =\lim z_{n} =l$,then $\lim y_{n} =l$ as well.

***

By order limit theorem:

$x_{n} \leq y_{n}$ for all $n \in \mathbb N$ implies $\lim x_{n}=l \leq \lim y_{n}$.

$y_{n} \leq z_{n}$ for all $n \in \mathbb N$ implies $\lim y_{n} \leq \lim z_{n}=1$.

Thus $l \leq \lim y_{n} \leq l$, therefore $\lim y_{n}=l$

<a name="234"></a>

### [Exercise 2.3.4](#toc)
Let $(a_{n}) \to 0$, and use the Algebraic Limit Theorem to compute each of the following limits (assuming the fractions are always defined):

1. $\lim (\frac{1+2a_{n}}{1+3a_{n}-4a_{n}^{2}})$
2. $\lim \frac{(a_{n}+2)^{2}-4}{a_{n{}}}$
3. $\lim (\frac{\frac{2}{a_{n}}+3}{\frac{1}{a_{n}}+5})$

***

1. 1
2. $\frac{(a_{n}+2-2)(a_{n}+2+2)}{a_{n}}=a_{n}+4 \to 4$
3. $\frac{2+3a_{n}}{1+5a_{n}} \to 2$

<a name="235"></a>

### [Exercise 2.3.5](#toc)

Let $(x_{n})$ and $(y_{n})$ be given, and define $(z_{n})$ to be the “shuffled” sequence $(x_{1}, y_{1}, x_{2}, y_{2}, x_{3}, y_{3}, \cdots , x_{n}, y_{n}, \cdots)$. Prove that $(z_{n})$ is convergent if and only if $(x_{n})$ and $(y_{n})$ are both convergent with $\lim x_{n} = \lim y_{n}$.

***

Suppose $(x_{n})$ and $(y_{n})$ are both convergent to the same limit $l$. Then there exists $N_{x}$ and $N_{y}$ such that for any given $\epsilon>0$, $x_{n}$ and $y_{n}$ will be in the neighborhood $V_{e}(l)$ for all $n \geq N_{x}$ and $N_{y}$ (respectively). Take $N = \max\{N_{x}, N_{y}\}$.  It follows that both $x_{n}$ and $y_{n}$ will be in $V_{e}(l)$ for all $n \geq N$, thus $z_{n}$ converges to $l$.

Conversely, suppose $z_{n}$ converges to some limit $l$. Then given any $\epsilon>0$, there exists some point in the sequence, either $x_{N}$ or $y_{N}$, after which all the subsequent $x_{n}$'s and $y_{n}$'s is in $V_{e}(k)$. That is, both $x_{n}$ and $y_{n}$ are in $V_{e}(k)$ for all $n > N$. Hence each converges to $l$.

<a name="236"></a>

### [Exercise 2.3.6](#toc)

Consider the sequence given by $b_{n} = n − \sqrt{n^{2} + 2n}$. Taking $(1/n) \to 0$ as given, and using both the Algebraic Limit Theorem and the result in Exercise 2.3.1, show $\lim b_{n}$ exists and find the value of the limit.

***

$(n − \sqrt{n^{2} + 2n})(n + \sqrt{n^{2} + 2n}) =n^{2} -n^{2}-2n = -2n$.

Thus, $b_{n} = n − \sqrt{n^{2} + 2n}= \frac{-2n}{n+\sqrt{n^{2}+2n}}= \frac{-2}{1+ \sqrt{1+2/n}}$.

Therefore, $\lim b_{n} = \frac{-2}{1+ \sqrt{1+\lim 2/n}} = -1$.



<span style="color:red">Early draft: $b_{n} \leq n+1 − \sqrt{n^{2} + 2n+1}=n+1-(n+1) = 0$ and $b_{n} \geq n − \sqrt{n^{2} + 2n+1}=n-(n+1) = -1$</span>

<a name="237"></a>

### [Exercise 2.3.7](#toc)


Give an example of each of the following, or state that such a request is impossible by referencing the proper theorem(s):

1. sequences $(x_{n})$ and $(y{n})$, which both diverge, but whose sum $(x_{n} + y_{n)}$ converges;
2. sequences $(x_{n})$ and $(y{n})$, where $(x_{n})$ converges, $(y_{n})$ diverges, and $(x_{n}+y_{n})$ converges;
3. a convergent sequence $(b_{n})$ with $b_{n} \neq 0$ for all $n$ such that $(1/b_{n})$ diverges;
4. two sequences $(a_{n})$ and $(b_{n})$, where $(a_{n}b_{n})$ and $(a_{n})$ converge but $(b_{n})$ does not.

***

1. $(x_{n}) = (1,-1,1,-1,\cdots)$ and $(y_{n}) = (-1,1,-1,1,\cdots)$ sum up to a sequence of zeros.

2. Impossible. Suppose the sum converges. Then $y_{n} = (x_{n} + y_{n}) - x_{n}$ converges to $\lim(x_{n}+y_{n}) - \lim(x_{n})$ by algebraic limit theorem.

<span style="color:red">Suppose the sum converges to $l$, i.e. there exists $N_{1}$ such that $|x_{n}+y_{n} - l|<\epsilon$, for all $n \geq N_{1}$. At the same time, there exists $N_{2}$ such $|x_{n} -x|<\epsilon^{\prime}$, for all $n \geq N_{1}$, where $x$ is the limit. Take $N = \max \{N_{1},N_{2}\}$. Then, for any given $\epsilon,\epsilon^{\prime}>0$, $|x_{n}+y_{n} - l|\leq |y_{n} + x+ \epsilon^{prime} - l|<\epsilon$, for all $n\geq N$. This contradicts the assumption that $(y_{n})$ is divergent.</span>

3. $(1/n)_{n \geq 1}$, the reciprocal of which $(n)$ is divergent.

4. Suppose $a_{n}=0$ for all $n$, and $b_{n}=n$. Then the product is a sequence of zeros which  converges.


<a name="238"></a>

### [Exercise 2.3.8](#toc)

Let $(x_{n}) \to x$ and let $p(x)$ be a polynomial.

1. Show $p(x_{n}) \to p(x)$
2. Find an example of a function $f(x)$ and a convergent sequence $(x_{n}) \to x$ where the sequence $f(x_{n})$ converges, but not to $f(x)$.

***

1. Given any polynomial $p(x) = a_{m}x_{n}^{m} + a_{m-1}x_{n-1}^{m-1} + \cdots + a_{0}$, algebraic limit theorem implies it converges to a_{m}x^{m} + a_{m-1}x^{m-1} + \cdots + a_{0}$.

2. Let $x_{n}=0$ for all $n$ and $f(x_{n}) = x_{n}+1$. Then $f(x_{n}) \to 1$.

<a name="239"></a>

### [Exercise 2.3.9](#toc)

1. Let $(a_{n})$ be a bounded (not necessarily convergent) sequence, and assume $\lim b_{n} = 0$. Show that $\lim(a_{n}b_{n}) = 0$. Why are we not allowed to use the Algebraic Limit Theorem to prove this?

2. Can we conclude anything about the convergence of $(a_{n}b_{n})$ if we assume that $(b_{n})$ converges to some nonzero limit $b$?

3. Use (1) to prove Theorem 2.3.3, part (iii), for the case when $a = 0$.

***

1. $|a_{n}| \leq M, M>0$, for all $n \in \mathbb N$. Given any $\epsilon/M>0$, $|b_{n}|<\epsilon/M$ for $n \geq N$ for some $N$. Thus, $|a_{n}b_{n}|=|a_{n}||b_{n}|<(\epsilon/M)M=\epsilon$ for all $n \geq N$.

We cannot use algebraic limit theoroem because $(a_{n})$ diverges.

2. No. suppose $(a_{n})= (5,-5,5,-5,\cdots)$. Hence it's bounded $|a_{n}| \leq 5$ for all $n$. If we assume that $(b_{n})$ converges to some nonzero limit $b$ (e.g. $(b_{n})$ is a sequence of $1$), then for all $n \geq N$ for some $N$, the terms in the sequence will continue to be oscilating, hence not converging. 

<span style="color:red"> Early draft:
For some limit $K \neq 0$, $|b_{n}-K|<\epsilon$ for $n \geq N$ for some $N$. Thus $|b_{n}|< |K|+\epsilon$. Hence $|a_{n}b_{n}|=|a_{n}||b_{n}|<(|K| + \epsilon)/M$ for all $n \geq N$.

$$\begin{align*}
|a_{n}b_{n}| &\leq |a_{n}b_{n}-Mb_{n}|+|Mb_{n}-Mb| \\
&\leq |b_{n}||a_{n}-M|+M|b_{n}-b| \\
&< X|a_{n}-M|+MK \text{, where $X>0$ due to bounded property} \\
\end{align*}$$
</span>

3. This is too trivial, I'm legitimately wondering if I'm understanding this wrong. But, the theorem states $\lim (a_{n}b_{n}) = ab$. We know $a$ is zero. We also know $b_{n}$ converges, hence it is bounded. Thus $\lim (a_{n}b_{n}) = 0$.

<a name="2310"></a>

### [Exercise 2.3.10](#toc)

Consider the following list of conjectures. Provide a short proof for those that are true and a counterexample for any that are false. 

1. If $\lim (a_{n} −b_{n}) = 0$, then $\lim a_{n} = \lim b_{n}$.

2. If $(b_{n}) \to b$, then $|b_{n}| \to |b|$.

3. If $(a_{n}) \to a$ and $(b_{n} −a_{n}) \to 0$, then $(b_{n}) \to a$.

4. If $(a_{n}) \to 0$ and $|bn −b|\leq a_{n}$ for all $n \in \mathbb N$, then $(b_{n}) \to b$.

***

1. False. For example, let $a_{n} = n$ and $b_{n} =-n$.

<span style="color:red">Early draft. Wrong because i did not consider divergent sequences. $\lim (a_{n} −b_{n}) = \lim a_{n} - \lim b_{n} \text{ by algebraic limit theorem} =0$.</span>

2. True. We will show $||b_{n} -|b_{n}||\leq |b_{n}-b|$, from which the statement follows.

By triangle inequality, $|b_{n}|\leq |b_{n}-b|+|b| \implies |b_{n}|-|b|\leq|b_{n}-b|$.

Similarly, $|b|\leq |b-b_{n}| + |b_{n}|\implies |b|-|b_{n}|\leq|b-b_{n}|=|b_{n}-b|\implies |b_{n}|-|b|\geq -|b_{n}-b|.$

Therefore, $-|b_{n}-b|\leq |b_{n}|-|b| \leq |b_{n}-b|$.

<span style="color:red">Early draft: $|b_{n}-b| <\epsilon$ implies $|b_{n}|<|b|+\epsilon$ and $|b_{n}|>|b|-\epsilon$ (using triangle inequalities). This is just equal to saying $||b_{n}|-|b||<\epsilon$.<span>

3. True. 

Let $x_{n} =a_{n}$ and $y_{n} = b_{n} −a_{n}$. Thus $x_{n} \to a$ and $y_{n} \to 0$, therefore from Algebraic Limit Theorem, this implies $x_{n} + y_{n} \to a$. But $x_{n} + y_{n}=b_{n}$.

<span style="color:green">Alt answer: For all $n\geq N=\max\{N_{1},N_{2}\}$ , (1) + (2) $\implies -\epsilon^{\prime} -\epsilon<a - b_{n}<\epsilon^{\prime} + \epsilon$

$\implies -\epsilon^{\prime} - \epsilon<b_{n}-a<\epsilon^{\prime} +\epsilon$

$\implies |b_{n}-a|<\epsilon^{\prime\prime}$, for any given $\epsilon^{\prime\prime}$, for all $n>N$.
</span>


<span style="color:red">Early draft: There exists $N$ such that $|b_{n} -a_{n}|<\epsilon$ for all $n \geq N$. By triangle inequality, $|b_{n} -a+a-a_{n}|\leq |b_{n} -a|+|a-a_{n}|\leq |b_{n} -a|+\epsilon$</span>

4. True. $|a_{n}|<\epsilon$ for all $n\geq N$ for some $N$. Hence $|b_{n}-b|\leq a_{n} \leq \epsilon$ for all $n\geq N$.

<a name="2311"></a>

### [Exercise 2.3.11](#toc) Cesaro Means

1. Show that if $(x_{n})$ is a convergent sequence, then the sequence given by the averages $$y_{n} = \frac{x_{1} +x_{2} +···+x_{n}}{n}$$ also converges to the same limit.

2. Give an example to show that it is possible for the sequence $(y_{n})$ of averages to converge even if $(x_{n})$ does not.

***

1. Suppose $x_{n} \to l$. Then, there exists $N_{1}$ such that $|x_{n}-l|<\epsilon$ for all $n> N_{1}$. Thus,

$$\begin{align*}
|y_{n}-l| &=  |\frac{x_{1} +x_{2} +\cdots+x_{N_{1}}+\cdots+x_{n}-nl}{n}|\\
&\leq \frac{1}{n}(|x_{1}-l|+|x_{2}-l|+\cdots + |x_{N_{1}}-l|+\cdots+|x_{n}-l|) \text{ by triangle inequality}.
\end{align*}$$

Select $M > \max\{|x_{n}-l|:\forall n \in \mathbb N\}$ and $\epsilon^{\prime} = \epsilon/2.$ Hence $M>\epsilon^{\prime}$. It follows that

$$\begin{align*}
|y_{n}-l| &\leq \frac{1}{n}(M+M+\cdots + \epsilon^{\prime}+\cdots+\epsilon^{\prime}) \\
&\leq \frac{1}{n}(N_{1}M+(n-N_{1})\epsilon^{\prime}) \\
&=\frac{N_{1}M}{n}-\frac{N_{1}\epsilon^{\prime}}{n}+\epsilon^{\prime} \\
&=\frac{N_{1}(M-\epsilon^{\prime})}{n} +\epsilon^{\prime}.
\end{align*}$$

Select $N_{2}$ such that for all $n \geq N_{2}$, $0<\frac{N_{1}(M-\epsilon^{\prime})}{n}<\epsilon^{\prime}.$ Therefore, for all $n \geq \max\{N_{1},N_{2}\}$,

$$\begin{align*}
|y_{n}-l| &=\frac{N_{1}(M-\epsilon^{\prime})}{n} +\epsilon^{\prime} \\
&\leq \epsilon^{\prime} + \epsilon^{\prime} = 2\epsilon^{\prime} = \epsilon.
\end{align*}$$

<span style="color:red"> Early draft: Suppose $x_{n}$ converges to $l$, then there exists $N$ such that if $n \geq N$, then $$|y_{n}| \leq |1/n|(|x_{1}|+|x_{2}|+\cdots+|l|+1+|l|+1+\cdots |l|+1)$$

$|y_n -l|=|\frac{x_{1} +x_{2} +···+x_{n}}{n}-l|\leq n|\frac{x_{1} +x_{2} +···+x_{n}}{n}-l|$
</span>

2. $\frac{-1+1-1+1-1+\cdots}{n}$

<a name="2312"></a>

### [Exercise 2.3.12](#toc) 

A typical task in analysis is to decipher whether a property possessed by every term in a convergent sequence is necessarily inherited by the limit. Assume $(a_{n}) \to a$, and determine the validity of each claim. Try to produce a counterexample for any that are false.

1. If every $a_{n}$ is an upper bound for a set $B$, then $a$ is also an upper bound for $B$.

2. If every $a_{n}$ is in the complement of the interval $(0, 1)$, then a is also in the complement of $(0, 1)$.

3. If every $a_{n}$ is rational, then $a$ is rational.
***

1. True. If $a$ is not an upper bound of $B$, then there exists $b\in B$, $b>a$. We also know that $a_{n}\geq b$ for all $n$. Thus, $a_{n}-a>b-a>0$ for all $n$, hence $a_n$ cannot converge to $a$.

2. I thought this is false, but I can't think of an example. Let me try to prove the statement instead. By definition of limit, there exists $N$ such that for all $n>N$, $a_{n}\in V_{\epsilon}(a)$. Suppose $a$ is in $(0,1)$. Then there exist an entire neighborhood comprising of elements in $(0,1)$. But this contradicts $a_{n}$ being a complement of $(0,1)$.

<span style="color:green">Love this exercise!</span>

<span style="color:red">Looking online, I can also make explicit about my choice of neighborhood. Select some $0<\epsilon<\max(|a−0|,|a−1|)$. Source: [SE](https://math.stackexchange.com/questions/1647760/determine-whether-a-property-possessed-by-every-term-in-a-convergent-sequence-is)</span>

3. False. Consider the interval $I_{n} = (x-\pi,x+\pi)$. By density of rational numbers, there exists a rational number $r_{n} \in I_{n}$. The sequence $(r_{n})$ converges to $pi$. To prove this, given any $\epsilon$, select $N$ such that $1/N<\epsilon$. Then for any $n\geq N$, $|r_{n}=x|<1/n\leq 1/N<\epsilon$.

<span style="color:green">Freaking love this exercise. Also, this prove works for not just $\pi$, for any real number. Good stuff.</span>

<a name="2313"></a>

### [Exercise 2.3.13](#toc) (Iterated Limits)

Given a doubly indexed array $a_{mn}$ where $m, n \in \mathbb N$, what should $\lim_{m,n} \to \infty a_{mn}$ represent?

1. Let $a_{mn} = m/(m + n)$ and compute the iterated limits 
$$\lim_{n \to \infty} (\lim_{m \to \infty} a_{mn}) \text{ and} \lim_{m \to \infty} (\lim_{n \to \infty} a_{mn}).$$ 

Define $\lim_{m,n \to \infty} a_{mn} =a$ to mean that for all $\epsilon >0$ there exists an $N \in \mathbb N$ such that if both $m,n \geq N$, then $|a_{mn} −a|<\epsilon$.

2. Let $a_{mn} = 1/(m + n)$. Does $\lim_{m,n \to \infty} a_{mn}$ exist in this case? Do the two iterated limits exist? How do these three values compare? Answer these same questions for $a_{mn} =mn/(m^{2} +n^{2})$.

3. Produce an example where $\lim_{m,n \to \infty} a_{mn}$ exists but where neither iterated limit can be computed.

4. Assume $\lim_{m,n \to \infty} a_{mn} = a$, and assume that for each fixed $m \in \mathbb N, \lim_{n \to \infty}(a_{mn}) \to b_{m}$. Show $\lim_{m \to \infty} b_{m} = a$.

5. Prove that if $\lim_{m,n \to \infty} a_{mn}$ exists and the iterated limits both exist, then all three limits must be equal.

***

1. $\lim_{n \to \infty} (\lim_{m \to \infty} a_{mn})=\lim_{n \to \infty} (1)=1$ and $\lim_{m \to \infty} (\lim_{n \to \infty} a_{mn})=\lim_{m \to \infty} (0)=0.$

2. For sufficiently large $m$ or $n$, $\lim_{m,n \to \infty} a_{mn}=0$. To see this, assume the worst case scenario for $m$ (the smallest it could be is $1$), then we can find $n$ large enough to converge to $0$. Similar argument for $m$. Similar findings for $$\lim_{n \to \infty} (\lim_{m \to \infty} a_{mn}) \text{ and} \lim_{m \to \infty} (\lim_{n \to \infty} a_{mn}).$$ 

Consider $a_{mn} =mn/(m^{2} +n^{2})$. The iterated limits give zero: WLOG, fixing $m$, $\lim_{n \to \infty}mn/(m^{2}+n^{2})=0$. Thus, $\lim_{m \to \infty} 0=0$.

$\lim_{m,n \to \infty}a_{mn}$ doesn't exist in this case, as we can find different limits depending on how $n$ is defined relative to $m$. For instance, if $n=m$, then $a_{mn}=m^{2}/2m^{2}=1/2$. Meanwhile if $n = 2m$, then $2m^{2}/5m^{2}=2/5$.

Note: I get a lot of clarity reading explanation of doubly indexed limits [here](https://math.stackexchange.com/questions/2658208/why-iterated-limits-are-different-from-simultaneous-limits).

3. Consider the doubly-indexed array:

 $$\begin{array}{llllll}(-1/1) +(-1/1)& (-1/2)+(1/1) & (-1/3)+(-1/1) & \cdots & (-1/n)+((-1)^{n}/1) & \cdots \\ 
(1/1)+(-1/2) & (1/2)+(1/2) & (1/3)+(-1/2)& \cdots & (1/n)+((-1)^{n}/2) & \cdots\\ 
(-1/1)+(-1/3) & (-1/2)+(1/3) & (-1/3)+(1/3) & \cdots & (-1/n)+((-1)^{n}/3) & \cdots\\
\vdots & & & & & \end{array}$$

Index the rows by $m$ and the columns by $n$. Then represent this array by the sequence $(\frac{(-1)^{m}}{n}+\frac{(-1)^{n}}{m})$. Then fixing $m$, taking the limit $n \to \infty$, we find that there is no limit. Similarly if we fix $n$.

Meanwhile, if we consider both $m,n \to \infty$, the region of the array where the terms in the sequence will gravitate towards as $n,m \to \infty$ is somewhere in the bottom right, in which case, the terms can be made arbitrarily small and for any given $\epsilon$, they will be in the $\epsilon$-neighborhood around $0$ for all $m,n \geq N$ for some $N$.

Footnote: Note that all elements in the array have absolute value below $2/N$, thus they are smaller than any given $\epsilon>0$ if $n,m >N = \epsilon/2$.

<span style="color:green">Bro this is super interesting. Actually, easier sequence is $(-1)^{n}(1/m+1/n).$</span>

<span style="color:red">Early draft: I don't think this is possible bruh, since if $\lim_{m,n \to \infty} a_{mn}$ exists, it should equal to the two iterated limits.</span>

4. Taking the triangle inequality: $$|b_{m}-a| \leq |b_{m}-a_{mn}|+|a_{mn}-a|$$ for all $n,m$. 

Suppose by contradiction, $\lim_{m \to \infty} b_{m} \neq a$. Given any $N$, there exists $M>0$ such that $|b_{m}-a| \geq M$ for some $m\geq N$. Thus,

$$M \leq |b_{m}-a_{mn}|+|a_{mn}-a|.$$

Select $0<\epsilon<M$. Since $\lim_{n \to \infty}(a_{mn}) \to b_{m}$ given a fixed $m$, there exists $N_{1}$ such that for all $n \geq N_{1}$, $|a_{mn}-b_{m}|<\epsilon<M$.


It follows that $$M < |a_{mn}-a|+\epsilon$$ for some $m,n \geq N$.

But this means that for any given $N$, there exists $M-\epsilon>0$ such that 
$$|a_{mn}-a|>M-\epsilon>0$$ 

for some $m,n>N$. Therefore $a_{mn} \not\to a.$


Footnote: The negation of convergence: Given any $N$, there exist $K>0$ such that $|a_{mn}-a|>K$ for some $m,n>N$.

<span style="color:red">Earlier draft: Consider any $\epsilon/2>0$. Since $\lim_{m,n \to \infty} a_{mn} = a$, there exist $N$ such that if both $n,m \geq N$, $|a_{mn}-a|<\epsilon/2$. Similarly, given fixed $m \in \mathbb N$, consider any $\epsilon/2$. Since $\lim_{n \to \infty}(a_{mn}) \to b_{m}$, there exists $N_{1}$ such if $n \geq N_{1}$, $|a_{mn}-b_{m}|<\epsilon/2$. Note that by triangle inequality, $$|b_{m}-a| \leq |b_{m}-a_{mn}|+|a_{mn}-a|$$ for all $n,m$. Select $N_{2} = \max \{N,N_{1}\}$ and $n\geq N_{2}$. Then for all $m \geq N_{2}$, $$|b_{m}-a| \leq \epsilon/2 + \epsilon/2 =\epsilon$$. </span>

5. If iterated limits exist, then given a fixed $m$, $\lim_{n \to \infty}(a_{mn}) \to b_{m}$ is a well-defined sequence (otherwise, how could the iterated limits exist). Conversely, given a fixed $n$, $\lim_{m \to \infty}(a_{mn}) \to c_{n}$ is also a well-defined sequence. The proof follows from solution 4 above.

