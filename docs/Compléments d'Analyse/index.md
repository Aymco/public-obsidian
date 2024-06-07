---  
share: true  
category: Compléments d'Analyse  
tags:  
  - regrouping  
title: Compléments d'Analyse  
created: 2024-02-07  
updated: 2024-06-06  
---  
→ [CA - questions de restitution](CA%20-%20questions%20de%20restitution.md)  
&nbsp;  
  
- [Ensembles](Ensembles.md)    ( [Suites et Séries](Suites%20et%20S%C3%A9ries.md))  
  
- [distance, norme, produit scalaire](distance,%20norme,%20produit%20scalaire.md)  
  
- [Espaces](Espaces.md)  
# Série de fourier  
  
- **Série de Fourier** $f:[-\pi,\pi]\to \mathbb{C}{}$ ⇒ $f(x)=\sum_{k\in \mathbb{Z}}^{}\hat{f}_{k}e^{ikx}{}$  
	- avec $\hat{f_k} = \frac{1}{2\pi} \int_{-\pi}^\pi e^{-iky}f(y) dy{}$  
	- $\langle f,g \rangle=\frac{1}{2\pi}\int_{-\pi}^{\pi} f^*g \, dx{}$   
	- ($L^{2}(-\pi,\pi)\to L^{2}{}$)     
	- $\{ e^{ikx} \}{}$ : *base orthonormée*   
	- **Sommes partielles** \[-n,n\] $S_{n}[f](x):=\sum_{k=-n}^{n}\hat{f}_{k}e^{ikx}$$=\frac{1}{2\pi}\int_{-\pi}^{\pi} D_{n}(x-y)f(y) \, dy{}$  
		- *noyeau de* **Dirichlet** $D_{n}(x)=\sum_{k=-n}^{n}e^{ikx}=\frac{\sin\left( x\left( n+\frac{1}{2} \right) \right)}{\sin\left( \frac{x}{2} \right)}{}$   
			- ($\int_{-\pi}^{\pi} D_{n}(x) \, dx=2\pi{}$) et $D_{n}(x) = D_{n}(x+2\pi){}$  
		- ⇒ $S_{n}[f](x)=\frac{1}{2\pi}\int_{-\pi}^{\pi} D_{n}(x-y)f(y) \, dy{}$  
	- **Sommes moyennées** $\tilde{S}_{n}[f]:=\frac{1}{n}\sum_{k=0}^{n-1}S_{n}[f]=\frac{1}{2\pi}\int_{-\pi}^{\pi} F_{n}(x-y)f(y) \, dy{}$   
		- *noyeau de* **Féjer** $F_{n}(x)=\frac{1}{n}\sum_{k=-n}^{n}D_{n}(x)=\frac{1}{n}\left( \frac{\sin\left( \frac{nx}{2} \right)}{\sin\left( \frac{x}{2} \right)} \right)^2{}$  
			- $\int_{-\pi}^{\pi} F_{n}(x) \, dx=2\pi{}$ et $F_{n}(x)=F_{n}(x+2\pi){}$  
		- $f{}$ *continue* + *période* $2\pi{}$ ⇒$\bar{S}_{n}f\to f{}$ *uniformement* (→ $\lim_{ n \to \infty }\tilde S _{n}[f]=f{}{}$)  
# Mesures  
  
- **Tribus** : $\Sigma \subseteq \mathbf{B}(X){}$;1. $\emptyset \in  \Sigma{}$ 2. $A,X\setminus A\in \Sigma{}$ 3. $\bigcap _{j\in \mathbb{N}}A_{j}\in \Sigma{}$  
	- ⇒ $\bigcup_{j}A_{j}=X\setminus\bigcap_{j\in \mathbb{N}}(X\setminus A_{j}) {}$   
	- tribu **Borélienne** : la plus petite tribu contenant les ouverts  
		- $\mathfrak{B}(X)=\{ B:=\text{ensemble borélien}\}{}$  
  
- **mesure** $\mu(A):\Sigma \to \mathbb{R}^+{}$ :  
	1. $\mu(\emptyset )=0{}$  
	2. $A_{j}{}$ disjoints : $\mu(\bigcup A_{j})= \sum\mu(A_{_{j}}){}$   ($<{}$si $A_{j}{}$ ! disjoints)  
  
- fonction **Borel-mesurable** : $f:X\to Y{}$  si $\forall A\in \mathcal{B}(Y),f^{-1}(A)\in \mathcal{B}(X){}$  
	- $\forall A\subseteq Y{}$ ouvert $f^{-1}(A)\in \mathcal{B}(X){}$ ⇒ mesurable  
	- $\forall A\subseteq Y{}$ ouvert : $f^{-1}(A)\subseteq X{}$ est ouvert ⇒ mesurable  
	- $f{}$ continue ⇒ mesurables  
  
- suite *croissante* : $A_{n}\subseteq A_{n+1}{}$ ⇒ $\mu(\cup A_{n})=\lim_{ n \to \infty }\mu(A_{n}){}$  
	- *décroissante*: $A_{n+1} \subseteq A_{n}$ et $\mu(A_1) < +\infty$⇒ $\mu(\bigcap_{n=1}^\infty A_n) = \lim_{n\to \infty} \mu(A_n)​$  
  
- $E{}$ ensemble **négligeable** :  $\exists A:\mu (A)=0, X\subseteq E{}$  
	- dénombrable ⇒ négligeable  
Exemples :   
  
- mesure de *Jordan* : Lesbegue avec somme finie  
  
- mesure de *Lebesgue* : la plus petite mesure qui coincide avec le volume  
	- (m. ext. de L : $\lambda^{n,*}(A):=\inf\left\{\sum_{j=1}^\infty|R_j|\vert A\subseteq\bigcup_{j=1}^\infty R_j , R_j\in \mathcal{S}^n\right\}   {}$   
		- avec $\mathcal{S}^{n}{}$ ensemble de rectancles seme-fermés de $\mathbb{R}^n{}$  
	- ⇒ $\lambda^n:\mathfrak{B}(\mathbb{R}^n)\rightarrow[0,\infty[$ ⇒ $\lambda^n(A)=\lambda^{n,*}(A){}$  
  
- mesure de *Dirac* : $\mu_{x}(A) := \begin{cases}1 \ \text{ si } x \in A \\ 0 \ \text{ sinon}\end{cases}{}$  ($\mu : \mathfrak{P}(X) \to [0,+\infty]{}$)  
  
- E **Cantor**(-Smith-Volterra) $C=\cap^\infty C_{k}{}$ : $C_{0}=[0,1],C_{n}:2^n{}$ intervalles (on retire ⅓ au milieu a chaque fois)  
	- *non dénombrable* mais *négligeable*	(!*Jordan mesurable*)  
# Intégrales  
  
- $f{}$ **intégrable** sur $X{}$: $\int _{X}f \, d\mu<\infty{}$  
  
- $f:X\to Y{}$ *mesurable*  *borel-mesurable*:  
	- $\forall A\in \mathfrak{B}(Y):f^{-1}(A)\in \mathfrak{B}(X){}$  
  
- $\lim \int \neq \int \lim{}$ sauf si :  
	- th. de la **convergence monotone** : $f_{n}:X\to \mathbb{R}^+{}$ *décroissante*($f_{n}\leq f_{n+1}{}$)  et *mesurable* et *conv ponctuellement*  $\to f{}$  
	- th. de la **convergence dominée** :$f_{n}:X\to \mathbb{C}{}$ *mesurable* et *conv ponctuellement* $\to f{}$ et $\forall n\in N,|f_{n}|\leq g{}$  avec $g:X\to \mathbb{R}^+{}$  
  
- *pondérer* $v(A)=\int _{A}f \, d\mu{}$ avec $f{}$ le poids  
	- *théoreme de Radon-Nikodym* : $\mu{}$ dénombrable finie et $v{}$ abs continue pdv $\mu{}$ ⇒ $\exists f=\frac{dv}{d\mu} {}$  
  
- ch de variable$f_{*}\mu(A):=\mu (f^{-1}(A)){}$ avec $f:X\to Y{}$ et $\mu:X{}$  
  
- **fonction caractéristique** : $\chi_{A}=\left\{  1:x\in A,0 \}\right.{}$  
  
- vrai **presque partout**→$A\subseteq X:\exists E\subseteq A:\mu(E)=E{}$ et vrai dans $A\setminus E{}$  
	- $f=0{}$ presque partout ⇔ $\int _{X}f \, d\mu{}=0$  
## Définition (démo) intégrales  
  
- $s{}$ fonction simple : $s:\mathbb{R}\to X{}$  
  
- **Intégrales Simples** : $\int _{A}s \, d\mu=\sum^p\alpha_{i}\mu(A\cap s ^{-1}(\alpha_{i})){}$  avec $\alpha_{i}{}$ hauteurs  
	1. $\int _{A}s \, d\mu=\int _{X}\chi_{A} \, d\mu{}$  
	2. $\int _{A}s \, d\mu\leq \int _{B}s \, d\mu{}$ avec $A\subseteq B{}$  
	3. $\int _{A}s \, d\mu\leq \int _{A}t \, d\mu{}$ avec $s(x)\leq t(x){}$  
	4. $\int _{\cup A_{n}}s \, d\mu=\sum\int _{A_{n}}s \, d\mu{}$  E *disjoints* : *stabilité par union dénombrable*  
	5. $\int _{\cup A_{n}}s \, d\mu\leq\sum\int _{A_{n}}s \, d\mu{}$  E *quelquonques*  
	6. $\int _{A}\sum a_{i}s_{i} \, d\mu=\sum a_{i}\int _{A}s_{i} \, d\mu{}$  
  
- **Intégrales positives** : $\int _{A}f \, d\mu=sup\left\{  \int _{A}s \, d\mu, s\leq f  \right\}{}$ ($s:X\to[0,\infty]{}$simple → f)  
  
- **Intégrales** : $f=f^+{}-f^-$ ⇒ $\int f \, d\mu=\int f^+ \, d\mu-\int f^- \, d\mu{}$ ($f^+, f^-{}$intégrables)  
  
- **Intégrales Complexes** : $\int _{A}f \, d\mu{}=\int _{A} \mathfrak{R}(f)\, d\mu+i\int _{A} \mathfrak{I}(f)\, d\mu+$ ($\mathfrak{R,I}{}$ intégrables)  
# Bonus  
[Fonctions](Fonctions.md)   
  
- th. de *Weierstrass* : $\forall f:\exists f_{n}\to f{}$ (⇒ $I{}$ compact ⇒polynomes dense dans $C(I){}$)  
&nbsp;  
⅕ - ⅖ pondération des devoirs  
