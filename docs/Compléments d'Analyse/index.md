---  
share: true  
category: Compléments d'Analyse  
tags:  
  - regrouping  
title: Compléments d'analyse  
created: 2024-02-07  
updated: 2024-05-23  
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
	- $d(u,v)=| |u-v| |{}$  
  
- **Espace métrique** :$(X,d){}$ : Ensemble, distance (que 2 cond : *pseudo-métrique*)  
	- Espace *Complet* : tt suite de cauchy converge  
	- Espace *séparable* : $\exists{}$ sous espace dénombrable  
	- sous-espace *dense* : $\forall y\in Y, \exists x \in X\subset Y:d(x,y)<\epsilon{}$ ($\mathbb{Q} {}$ dense $\mathbb{R}{}$)  
  
- ****[Suites](Suites.md)**  
# Normes  
  
- **Norme** : $||\cdot||:X\to \mathbb{R}^+{}$  ex: $| | u| |_{p}=\sqrt{ \sum u_{i}^p }{}$  ; $| | u| |_{\infty}=max(u_{i}){}$  
	1. *définir positive* : $\lvert \lvert x \rvert \rvert=0\iff x=0{}$  
	2. *absolument homogene* : $\lvert \lvert \alpha x \rvert \rvert\leq \lvert \alpha \rvert\cdot \lvert \lvert x \rvert \rvert{}$   
	3. *inégalité triangulaire* : $||x+y||\leq||x||+||y||{}$  ~~.$\forall x,y{}$~~  
  
- **Espace Normé** : $(X, | | \cdot| |){}$  
  
- **Espace de Banach** $\mathfrak{B}$ : Normé + Complet ($d(u,v)=| |u-v| |{}$)  
  
- **Opérateurs** : $A:X\to Y :A(x)=y{}$  
	- *linéaire* : $A\left( \sum\lambda_{i}x_{i} \right)=\sum\lambda _{i}A(x_{i}){}$  
	- *borné* : $| |A| |<\infty \iff{}$ lipschitzien , A continu en 0,   
  
- $||u||=d(0,u){}=\sqrt{ \langle u,u \rangle }{}$  
# Produit scalaire  
  
- **Produit scalaire** : $\langle u,v \rangle:X\times X\to \mathbb{R}^+{}$  
	1. *bilinéaire* : $\langle 2u + w,v \rangle=2\langle u,v \rangle + \langle w,v \rangle{}$  
	2. *symétrique* : $\langle u,v \rangle= \langle v,u \rangle{}$  
	3. *défini positif* : $\langle u,v \rangle>0 : u,v\neq 0{}$  
  
- Produit scalaire **Complexe** : $\langle u,v \rangle:X\times X\to \mathbb{C}{}$  
	1. *sesquilinéaire* : 1er : *antilinéaire*(linéaire pdv conjugé) ; 2eme *linéaire* : $\langle \alpha f,\beta g \rangle=\alpha^*\langle f,\beta g \rangle = \alpha^*\beta\langle f,g \rangle{}$  
	2. *symétrie conjugée* : $\langle f,g \rangle= \langle g,f \rangle^*{}$  
  
- identité du parallélogramme : $||u+v||^2+||u-v||^2=2||u||^2+2||v||^2{}$  
	- si vrai ⇒ $\langle u,v \rangle=\frac{1}{4}(||u+v||^2-||u,v||^2){}$  
  
- **Espace préhilbertiens** : $(X, \langle \cdot,\cdot \rangle){}$  
  
- **Espace de Hilbert** $\mathfrak{H}{}$ : + Complet      (⇒ $\mathfrak{B}{}$)   
	- $\langle u,v \rangle=0\implies u\perp v{}$ *orthogonaux*  
	- $\exists \alpha:\alpha u=v\implies u\mid\mid v{}$ *parallèles*  
  
- Ensembles *orthonormés* : $\langle u_{i}, u_{j} \rangle=\left\{\begin{aligned} 0:i\neq j \\1: i=j \end{aligned}\right.{}$  
	- ⇒ base orthonormée : $\forall f:f=\sum c_{j}u_{j}{}$ ($c_{j}= \langle f,u_{j} \rangle{}$)  
	- …  
  
- $f=f_{\mid\mid}+f_{\perp}{}$ ⇒ $|| f||^2=|| f_{\mid\mid}||^2+|| f_{\perp }||^2{}$  
  
- **Projection** : $f_{i}= \langle f,u_{i} \rangle u_{i}\implies Prf=\sum f_{i}u_{i}{}$  
  
- **Série de Fourier** $L^{2}(-\pi,\pi)\to L^{2}{}$  avec $\langle f,g \rangle=\frac{1}{2\pi}\int_{-\pi}^{\pi} f^*g \, dx{}$  
	- base orthonormée : $\{ e^{ikx} \}{}$ ⇒ $f(x)=\sum_{k\in \mathbb{Z}}^{}\hat{f}_{k}e^{ikx}{}$  
	- *Sommes partielles* de -n à n $S_{n}[f](x)=\sum_{k=-n}^{n}\hat{f}_{k}e^{ikx}=\frac{1}{2\pi}\int_{-\pi}^{\pi} D_{n}(x-y)f(y) \, dy{}$   
		- *noyeau de Dirichlet* $D_{n}(x)=\sum_{k=-n}^{n}e^{ikx}=\frac{\sin\left( x\left( n+\frac{1}{2} \right) \right)}{\sin\left( \frac{x}{2} \right)}{}$ ($\int_{-\pi}^{\pi} D_{n}(x) \, dx=2\pi{}$)  
	- *Sommes moyennées* → $\lim_{ n \to \infty }\tilde S _{n}[f]=f{}{}$ : $\tilde{S}_{n}[f]=\frac{1}{n}\sum_{k=0}^{n-1}S_{n}[f]=\frac{1}{2\pi}\int_{-\pi}^{\pi} F_{n}(x-y)f(y) \, dy{}$   
		- *noyeau de Féjer* $F_{n}(x)=\sum_{k=-n}^{n}D_{n}(x)=\frac{1}{n}\left( \frac{\sin\left( \frac{nx}{2} \right)}{\sin\left( \frac{x}{2} \right)} \right)^2{}$  
  
# Mesures  
  
- **Tribus** : $\sum\in \mathbf{B}(X){}$;1. $\emptyset , X \in  \sum{}$ 2. $A,\bar{A}\in \sum{}$ 3. $\bigcup_{\alpha}, \bigcap _{\alpha}\in \sum{}$  
  
- tribu *Borélienne* (la plus petite) :$\mathcal{B}(X){}$   
  
- **mesure**   
	1. $\mu(A):\sum\to R^+{}$  
	2. $\mu(\emptyset )=0{}$  
	3. $\mu(\bigcup A_{j})\leq \sum\mu(A_{_{j}}){}$ (égal si $A_{j}{}$ disjoints)  
  
- fonction *Borel-mesurable* : $f:X\to Y{}$  si $\forall A\in \mathcal{B}(Y),f^{-1}(A)\in \mathcal{B}(X){}$  
	- $\forall A\subseteq Y{}$ ouvert $f^{-1}(A)\in \mathcal{B}(X){}$ ⇒ mesurable  
	- $\forall A\subseteq Y{}$ ouvert : $f^{-1}(A)\subseteq X{}$ est ouvert ⇒ mesurable  
	- $f{}$ continue ⇒ mesurables  
   
  
- $s{}$ fonction simple : $s:\mathbb{R}\to X{}$  
  
- **Intégrales Simples** : $\int _{A}s \, d\mu=\sum^p\alpha_{i}\mu(A\cap s ^{-1}(\alpha_{i})){}$  avec $\alpha_{i}{}$ hauteurs  
	1. $\int _{A}s \, d\mu=\int _{X}\chi_{A} \, d\mu{}$ avec $\chi=\left\{  1:x\in A,0 \}\right.{}$  
	2. $\int _{A}s \, d\mu\leq \int _{B}s \, d\mu{}$ avec $A\subseteq B{}$  
	3. $\int _{A}s \, d\mu\leq \int _{A}t \, d\mu{}$ avec $s(x)\leq t(x){}$  
	4. $\int _{\cup A_{n}}s \, d\mu=\sum\int _{A_{n}}s \, d\mu{}$  E disjoints  
	5. $\int _{\cup A_{n}}s \, d\mu\leq\sum\int _{A_{n}}s \, d\mu{}$  E quelquonques  
	6. $\int _{A}\sum a_{i}s_{i} \, d\mu=\sum a_{i}\int _{A}s_{i} \, d\mu{}$  
  
- **Intégrales positives** : $\int _{A}f \, d\mu=sup\left\{  \int _{A}s \, d\mu, s\leq f  \right\}{}$ (s fct simple → f)  
  
- **Intégrales** : $f=f^+{}-f^-$ ⇒ $\int f \, d\mu=\int f^+ \, d\mu-\int f^- \, d\mu{}$  
  
- **Intégrales Complexes** : $\int _{A}f \, d\mu{}=\int _{A} \mathfrak{R}(f)\, d\mu+i\int _{A} \mathfrak{I}(f)\, d\mu+$  
  
- $\lim \int \neq \int \lim{}$ sauf si :  
	- *théorème de la convergence monotone* : $f_{n}\leq f_{n+1}{}$ mesurable et converge ponctuellement vers $f{}$  
	- *théorème de la convergence dominée* :$f_{n}{}$ conv ponctuellement $\to f{}$ et $\forall n\in N,|f_{n}|\leq g{}$  avec $g:X\to[0,\infty[{}$  
  
- *ponderer* $v(A)=\int _{A}f \, d\mu{}$ avec $f{}$ le poids  
	- *théoreme de Radon-Nikodym* : $\mu{}$ dénombrable finie et $v{}$ abs continue pdv $\mu{}$ ⇒ $\exists f=\frac{dv}{d\mu} {}$  
  
- ch de variable$f_{*}\mu(A):=\mu (f^{-1}(A)){}$ avec $f:X\to Y{}$ et $\mu:X{}$  
# Analyse fonctionnel. e  
→ espaces de fonction / *dimensions infinies*  
fonctionnelle :  fonction sur les fonctions  
  
# Theorie de la mesure  
probabilités  
## Bases d'espaces vectoriels  
  
- (*Base de Hamel*) : tout veteur = combili finie  
