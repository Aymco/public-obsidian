---  
share: true  
category: MDP  
tags:  
  - matière  
created: 2023-12-19  
updated: 2024-01-05  
---  
  
# Résumé combinatoires  
| x         | Repetition    | ~~répetition~~ |  
| --------- | ------------- | -------------- |  
| tout      | $Q^{a,b}_{n}=\frac{n!}{a!b!}$ | $Bij(n\to n)=n!$        |  
| ordre     | fonction : $n^k$     | $Inj(k\to n)=A^k_{n}=\frac{n!}{(n-k)!}$      |  
| ~~ordre~~ | $B^*(n,k):=B(n+k-1, k)$     | $B(n,k)=\frac{n!}{k!(n-k)!}$      |   
  
# Dénombrement  
  
- Ensembles *équipotents* $A \approx B$ si bijection de $A$ vers $B$ (mm nb éléments)  
	- $N\approx Z$ : $n\to \left\{\begin{align} \frac{{n+1}}{2}\quad\quad \frac{-n}{2} \end{align}\right.$  
  
- $A$ est *fini* : $A \approx \{ 1,2,..,n \}$, *infini dénombrable* $A\approx \mathbb{N}$  
	- $n$ *cardinal* de $A$ : $n=|A|=\#A \in N$  
  
- Argument diagonal de Cantor : Prouver que $[0,1[\not\approx \mathbb{N}$  
	- $f(i)=a_{i}=0, a_{i0}a_{i1}a_{i_{2}}, \dots$ binaire  
	- $b=0,b_{1}b_{2}b_{3}\dots$ avec $b_{i}\neq a_{i}i$  
	- $\not\exists i:f(i)=b$ ⇒ ! bijective  
  
- $|A|:=\sum_{a\in A} f(a)$ poids proba  
  
  
  
  
- **Binomiale** $B(n,k)$ ($\not O \not R$) $B(n,k)=C^k_{n}={n \choose k }=\frac{n!}{k!(n-k)!}=C^k_{n-1} +C^{k-1}_{n-1}=B(n,n-k)$  
  
- *Binômes de Newton* : $(x+y)^n=\sum_{k=0}^{n}C^k_{n}x^ky^{n-k}$  
  
- **Selection** : ($\not OR$) :  $k$-sélection d'un $n$-ensemble  
	- $B^*(n,k):=B(n+k-1, k)$  
  
## Fonctions  
  
- relation $R:A\to B$ est un ensemble $R\subset A\times B$  
  
- Fonction $A\to B$ : triple $(A,B,R)$ : $aRb$ unique  
  
- $|A|=n, |B|=k$ :   
	- fonction ($OR$) $B\to A$ : $n^k$  
	- **Injection** ($O\not R$) : $Inj(k\to n)=[n]_{k}:=\frac{n!}{(n-k)!}$ (A)  
	- **Bijection**, **Permutation** ($T\not R$): $Bij(n\to n)=n!$  
		- **Dérangements** ($f(a)\neq a$) : $d_{n}:=n!\sum_{r=0}^{k} \frac{(-1)^r}{r!}$  
	- **Surjections** : $Sur(n\to k)=\sum_{r=0}^{k}(-1)^rB(k,r)(k-r)^n$  
  
- Répartition $n$ el en $k$ sous ensembles disjoint et !vides $S(n,k):=\frac{1}{k!}Sur(n\to k)$  
	- Stirling : $S(n,k)=S(n-1, k-1)+kS(n-1,k)$  
	- Bell : $\sum_{r=0}^{k}S(n,k)=b_{n}$  
  
## Dénombrement Combinatoires - dénombrements  
  
  
- $f(x)=1 : |A|=\sum_{a\in A}^{}f(a)$  
  
- **Union** d'ensembles : $|A \cup B|=|A|+|B| - |A \cap B|$  
  
- **Composition**: $|A\times B|=|A||B|$  
## Dénombrer avec des génératrices  
![Fonction génératrice > Fonction génératrice définition](Fonction%20g%C3%A9n%C3%A9ratrice.md#fonction-generatrice-definition)  
  
$n$ éléments dans $N$ cases avec $A_{i}$ les valeurs acceptées pour la case $i$  
$f(x)=\prod_{i=1}^N \sum_{j\in A_{i}}x^j$ → réponses $f_{n}$  
#todo   
### Astuces  
  
- $\sum_{i=0}^{\infty}x^i=\frac{1}{1-x}$ et $\lim_{ x \to 1 }$  
  
- $\sum_{i=0}^{\infty}(i+1)x^i=\frac{1}{(1-x)^{2}}$  
  
- $\sum_{i=0}^{\infty}(i+1-a)x^i=\frac{x^a}{(1-x)^{2}}$  
  
### Équations de récurrences $\alpha v_{n+2}+\beta v_{n+1}+\gamma v_{n}=\dots$  
#todo   
  
## Fonctions de hachage  
$H:\{ 0,1 \}^*\to \{ 0,1 \}^n$ taille $?\to n$  
collision si 2 entrées donnent la même valeure  
### Blockchains  
Chaque bloque est le hash du block précédent et d'une donnée  
le block $h_{i}$ peut nous donner toutes les info précédentes  
graine $s$ : nombres aléatoire $a_{n}=H(s,n)$  
