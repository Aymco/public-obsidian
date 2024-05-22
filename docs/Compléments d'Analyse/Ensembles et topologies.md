---  
share: true  
category: Compléments d'Analyse  
tags:  
  - matière  
created: 2024-01-05  
updated: 2024-05-22  
title: Ensembles et topologies  
---  
## Ensembles  
### Proriétés  
  
- *sous-ensemble* : $B\subseteq A:\forall x \in B,x\in A{}$  
  
- ensemble *ouvert* / *fermé* contient (aucun / tous) points frontieres  
  
- $n$ *cardinal* de $A$ : $n=|A|=\#A \in N$ : taille d'un ensemble  
	- $|\emptyset |<|\{ 0,1 \}|<|\mathbb{N}|<|2^\mathbb{N}|=|\mathbb{R}|<|2^{2^\mathbb{R}}|{}$  
  
- Ensembles *équipotents* $A \approx B \iff |A|=|B|$ si bijection de $A$ vers $B$   
	- $N\approx Z$ : $n\to \left\{\begin{align} \frac{{n+1}}{2}\quad\quad \frac{-n}{2} \end{align}\right.$  
  
- $A$ est *fini* : $A \approx \{ 1,2,..,n \}$ ($A\approx \mathbb{N}$ → *infini*  )  
  
- Ensemble *infini* : jamais en bijection avec l'ensemble de ses parties  
  
- Ensemble *dénombrable* (*énumérable*) : bijection avec les naturels  
	- $\iff |A|=|\mathbb{N}|{}$  (exemples :  $\mathbb{N}, \mathbb{Z}, \mathbb{Q}{}$, paires et n-upplets)  
	- $\subseteq, \cup, \cap, \bigcup_{\infty \text{ enumérable}} {}$ d'E énumérables ⇒ *enumérable*  
		- $\bigcup_{\infty \text{ non-énumérable}}$ d'E énumérables ⇒ ! énumérable  
### Types d'ensembles  
  
- ensemble de *fonctions* : $A^B{}:=\{ f:B\to A \}$ et $n^X=\{ 0,n-1 \}^X{}$  
	- Espace $C(a,b){}$ : fct continues de $a{}$ à $b{}$  
	- Espace $L^{2}(a,b)=\left\{  f:]a,b[\to \mathbb{C}:\int_{a}^{b} \lvert f(x)^{2} \rvert \, dx<\infty  \right\}{}$ : fct : l’intégrale de leur carré est finie (Lebesgue)  
		- suites → $l^{2}(\mathbb{N})=\left\{  a\in \mathbb{R}^\mathbb{N}:\sqrt{ \sum a_{i}^{2} }<\infty  \right\}{}$   
  
- ensemble de *vecteurs* : $\mathbb{R}^3=\mathbb{R}\times \mathbb{R}\times \mathbb{R}{}$  
### Ensembles numériques  
  
- $\mathbb{N,Z,Q,R,C}{}$  ($R_{0}=R\setminus \{ 0 \}{}$) ($N = \{ 1,2,\dots \}{}$ ; $N_{0}=N\cup \{ 0 \}$)  
  
- *intervalle* $I=[a,b]=\{ x\in R,a\leq x\leq b \}{}$  
  
### Collections : Ensemble d'Ensembles  
  
- **Collection** : ensemble d'ensemble  
  
- **Topologie** :  Collection $\mathcal{O}{}$ d'ensembles ouverts : (ex: $\mathcal{P}(X){}$)  
	1. $X,\emptyset \in \mathcal{O}{}$  
	2. $O_{1}\cap O_{2}\in \mathcal{O}{}$  
	3. $\forall \{ O_{\alpha} \} \subseteq \mathcal{O},\bigcup_{\alpha}O_{\alpha}\in \mathcal{O}{}$ (intersection $\infty{}$ peut être fermé)  
  
- **espace Topologique** : doté d'une topologie  
	- $R{}$ *recouvrement* de $Y{}$: Collection : $Y\subseteq\bigcup_{\alpha}R_{\alpha}{}$  
## Opérateurs topologiques :  
  
- **Union** : $A\cup B=\{ x\in X:x \in A \text{ ou } x \in B \}{}$  
	- $|A \cup B|=|A|+|B| - |A \cap B|$  
  
- **disjonction**, **Intersection** :  $A\cup B=\{ x\in X:x \in A \text{ et } x \in B \}{}$  
  
- **Exclusion** :  $A\cup B=\{ x\in X:x \in A \text{ et } x \not\in B \}{}$  
  
  
- **Complémentaire** : $A^*=X \setminus A{}$  
  
- **frontière** : $\partial A=\{ x \in  X: \exists r > 0:B_{r}(x) \cap A\not=\emptyset \text{ et } \cap A^{*} \not=\emptyset  \}{}$  
  
- **Adhérence** : $\bar{A}=A\cup \partial A{}$  
  
- **intérieur** : $\underline{A}=A \setminus \partial A{}$  
  
- **extérieur** : $ext(A)=(\bar{A})^*=\underline{(A^*)}{}$  
  
- **Composition**: $|A\times B|=|A||B|$  
  
  
  
  
## Définitions d'ensembles  
  
- Ensemble **étoilé** en $z_{0}$ : $\forall z\in D$ chemin droit $c:z_{0}\to z$, $c\in D$  
	$\mathcal{A}\in \mathbb{C}$ ouvert, étoilé, $f:\mathcal{A}\to \mathbb{C}$ dérivable : $F(z):=\int_{z_{0}}^{z} f(x) \, dw$  
		⇒$F'(z)=f(z)$  
  
- Ensemble **simplement connexe** : connexe et sans trou  
	$\mathcal{A}\in \mathbb{C}$ ouvert, simplement connexe, $f:\mathcal{A}\to \mathbb{C}$ dérivable  
		⇒$F'(z)=f(z)$  
  
- Ensemble **connexe** : E != réunion 2 ensembles fermés disjoints  
  
- Ensemble **connexe par arcs** : tous les points sont reliés de façon continue  
