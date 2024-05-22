---  
share: true  
category: Compléments d'Analyse  
tags:  
  - regrouping  
title: Compléments d'analyse  
created: 2024-02-07  
updated: 2024-05-22  
---  
⅕ - ⅖ pondération des devoirs  
# [Ensembles et topologies](Ensembles%20et%20topologies.md)  
# Distances  
  
- **Distance** :$X\times X\to R^+{}$ 3 conditions :  
	1. $d(u,v)=d(v,u){}$  
	2. $d(u,v)\leq d(u,w)+d(w,v){}$  
	3. $d(u,v)=0\iff u=v{}$   
	- Distance *euclidienne* : $d_{e}(x,y)=\sqrt{ \sum_{i=0}^{n-1} (x_{i}-y_{i})^{2}}{}$  
	- distance de *manhattan* : $d_{m}(x,y)=\sum_{0}^{n-1}|x_{i}-y_{i}|{}$  
  
- **Espace métrique** :$(X,d){}$ : Ensemble, distance (que 2 cond : *pseudo-métrique*)  
	- Espace *Complet* : tt suites de cauchy convergent  
	- Espace *séparable* : $\exists{}$ sous espace dénombrable  
	- sous-espace *dense* : $\forall y\in Y, \exists x \in X\subset Y:d(x,y)<\epsilon{}$ ($\mathbb{Q} {}$ dense $\mathbb{R}{}$)  
  
- suite $a_{n}{}$ converge : $\exists N: \forall n>N:d(a_{n}, a)<\epsilon \quad(\forall\epsilon>0){}$ ⇒  
  
- suite de *Cauchy* : $\exists N:\forall m,n>N,d(a_{n},a_{m})<\epsilon{}$                     ⇒  
  
- *bornée* : $sup (x_{n})\leq \infty{}$   
  
- suite *sommable* <. > $\sum_{}^{\infty}x_{i}{}$ converge  
(voir [Analyse 1](Analyse%201.md))  
# Normes  
  
- **Norme** : $||\cdot||:X\to \mathbb{R}^+{}$  
	1. *définir positive* : $\lvert \lvert x \rvert \rvert=0\iff x=0{}$  
	2. *absolument homogene* : $\lvert \lvert \alpha x \rvert \rvert\leq \lvert \alpha \rvert\cdot \lvert \lvert x \rvert \rvert{}$  
	3. *inégalité triangulaire* : $||x+y||\leq||x||+||y||{}$  ~~.$\forall x,y{}$~~  
# Analyse fonctionnelle  
→ espaces de fonction / *dimensions infinies*  
fonctionnelle :  fonction sur les fonctions  
  
# Theorie de la mesure  
probabilités  
## Bases d'espaces vectoriels  
  
- (*Base de Hamel*) : tout veteur = combili finie  
  
# Mesures  
  
- **Tribus** (voir MDP) : $\sum\in \mathbf{B}(X){}$; $\emptyset , X \in  \sum{}$ 2. $A\in \sum \implies \bar{A}\in \sum{}$  
  
- tribu *Borélienne* (la plus petite) :$\mathcal{B}(X){}$   
