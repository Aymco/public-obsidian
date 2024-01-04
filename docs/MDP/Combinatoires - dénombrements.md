---  
share: true  
category: MDP  
tags:  
  - matière  
created: 2023-12-19  
updated: 2024-01-04  
---  
  
# Résumé combinatoires  
| x         | Repetition    | ~~répetition~~ |  
| --------- | ------------- | -------------- |  
| tout      | $Q^{a,b}_{n}=\frac{n!}{a!b!}$ | $P_{n}=n!$        |  
| ordre     | $B^p_{n}=n^p$     | $A^p_{n}=\frac{n!}{(n-p)!}$      |  
| ~~ordre~~ | $D^p_{n}=C^p_{n+p-1}$     | $C^p_{n} = {n \choose p}=\frac{n!}{k!(n-k)!}$      |   
  
# Développement  
## Combinaisons $C^p_{n}$  
~~repetition~~, ~~ordre~~  
$n \choose k$ $=B(n,k)=C^k_{n}=\frac{n!}{k!(n-k)!}=C^k_{n-1} +C^{k-1}_{n-1}$    
### Binômes de Newton  
$(x+y)^n=\sum_{k=0}^{n}C^k_{n}x^ky^{n-k}$  
## Selection $B^*(n,k)=D^p_{n}$  
repetition, ~~ordre~~  
choisir $p$ eléments parmi $n$ elements   
## Permutations $P_{n}=A^n_{n}$  
~~repetition~~, tout  
bijection entre 2 ensembles ( $n=|A|=|B|$)  
$Bij(n\to n) =P_{n}= n!$   
  
## Arrangement,. Assignations $A^p_{n}$  
! répetitoin, ordre  
  
$Inj(p\to n)$  
## Liste  
ordre, repetition  
$Fct(n\to p)=B^p_{n}=n^p$  
  
## Remplissages  
$p$ vetements dans $n$ tiroirs  
$C^{p-n}_{p-1}$ ??  
$Sur(n\to k)$  
## Dérangements  
permutation avec $f(a)=a$ :on retire les bijection  → $S=F- \cup Fi$  
$d_n=n!\sum_{r=0}^{n}\frac{-1^r}{r!}$  
  
## Partitions  
$n$ enfants → $k$ groupes  
$Par(n\to k)=S(n,k)=Sur(n\to k)$  
nombre de Stirling : $S(n,k) = S(n-1,k-1)+kS(n-1, k)$  
  
# Dénombrement  
## Equipotence $A \approx B$  
$\iff$ $\exists$ **bijection** entre $A$ et $B$ (mm nb éléments)  
$A$ est **fini** / infini : $A \approx \{ 1,2,..,n \}$  
	cardinal de $A$ : $n=|A|=\#A \in N$  
$A \approx N$ → ensemble infini **indénombrable**  
### $N\approx Z$ : $n\to \left\{\begin{align} \frac{{n+1}}{2}\\ \frac{-n}{2} \end{align}\right.$  
### $N \approx Q$  
Démo  
#todo   
### $N \approx R$  
Démo  
#todo   
  
## Dénombrement [Combinatoires - dénombrements](Combinatoires%20-%20d%C3%A9nombrements.md)  
  
$f(x)=1 : |A|=\sum_{a\in A}^{}f(a)$  
**Unions** d'ensembles : $|A \cup B|=|A|+|B| - |A \cap B|$  
(existe une formule générale)  
**Composition**: $|A\times B|=|A||B|$  
  
![Combinatoires - dénombrements > Résumé combinatoires](Combinatoires%20-%20d%C3%A9nombrements.md#resume-combinatoires)  
   
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
