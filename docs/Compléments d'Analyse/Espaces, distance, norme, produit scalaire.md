---  
share: true  
category: Compléments d'Analyse  
tags:  
  - matière  
created: 2024-05-31  
updated: 2024-06-01  
---  
# Distances  
  
- **Distance** :$X\times X\to R^+{}$ 3 conditions : ($d(u,v)=| |u-v| |{}$)  
	1. *symétrie* : $d(u,v)=d(v,u){}$  
	2. *inégalité triangulaire* : $d(u,v)\leq d(u,w)+d(w,v){}$  
		- $\iff{}$*inégalité triangulaire inverse* :$|d(u,w)-d(w,v)| \leq d(u,v){}$  
	3. $d(u,v)=0\iff u=v{}$   
	- Distance *euclidienne* : $d_{e}(x,y)=\sqrt{ \sum_{i=0}^{n-1} (x_{i}-y_{i})^{2}}{}$  
	- distance de *manhattan* : $d_{m}(x,y)=\sum_{0}^{n-1}|x_{i}-y_{i}|{}$  
&nbsp;  
  
- **Espace métrique** :$(X,d){}$ : Ensemble, distance (aussi espace topologique)  
	- (que 2 cond dist: *pseudo-métrique*)  
	- $X{}$ **Complet** : tt suite de cauchy converge vers $x^*{}$ ($\mathbb{R},\mathbb{C}, l^p, l^\infty,\not \mathbb{Q}{}$)  
		- $\exists i:X\to \overline{ X }{}$ complet : $d(x,y)=\bar{d}(i(x),i(y)){}$ et $\overline{ i(X) }={}\bar{X}{}$  
	- *compact* ⇔ *séquentiellement Compact* ⇔ *Complet* + *séparable*  
	- *fermé* ⇔ *séquentiellement fermé*  
	- th. *point fixe* : *complet* + $f{}$ *contractante* ⇒$\exists{}$ unique point fixe:$f(x)=x{}$  
	- *connexe* : seuls ouverts+fermé : $\emptyset,X {}$  
	- *connexe par arcs* : $\exists\gamma_{\text{continue}}:\gamma(0)=x, \gamma(1)=y\quad\forall x,y\in X{}$  
  
- th. *valeures extremes* (bornes atteintes): $(X,d){}$ *compact*,$f{}$continue ⇒ min, max  
  
- **[Suites et Séries](Suites%20et%20S%C3%A9ries.md)**  
&nbsp;  
# Normes  
  
- **Norme** : $||\cdot||:X\to \mathbb{R}^+{}$  (continue, convexe, k-Lipschitzienne)  
	1. *séparation* : $\lvert \lvert x \rvert \rvert=0 \implies x=0{}$   
	2. *absolue homogénéité* : $\lvert \lvert \alpha x \rvert \rvert = \lvert \alpha \rvert\cdot \lvert \lvert x \rvert \rvert{}$ ~~.$\forall \alpha \in \mathbb{R},\forall x\in X{}$ ~~  
	3. *inégalité triangulaire* : $||x+y||\leq||x||+||y||{}$  ~~.$\forall x,y{}$~~  
	- n. euclidienne $| | u| |_{p}=\sqrt[p]{ \sum |u_{i}|^p }{}$  → sur f : $\lvert \lvert f \rvert \rvert_{p}=\sqrt[p]{  \int_{X} \lvert f \rvert^p \, d\mu} {}$  
	- n. du maximum  $| | f| |_{\infty}=max_{x\in I}(f(x)){}$ ~~.$f\in C(I){}$ ~~  
  
- norme induite : $||u||=d(0,u){}=\sqrt{ \langle u,u \rangle }{}$  
  
- **Espace Normé** : $(X, | | \cdot| |){}$  espace vectoriel  
	- $X{}$ *séparable* $\iff{}\exists$ famille de $X{}$ totale.  
  
- **Espace de Banach** $\mathfrak{B}$ : Normé + *Complet* (ex: $\mathbb{R}^n, l^p(\mathbb{N}),l^\infty(\mathbb{N}){}$)  
	- critère de *Weierstrass* : $f{}$ conv ponctuellement ⇒ conv uniformément  
  
- espace *convexe* : norme *convexe*  
# Produit scalaire  
  
- **Produit scalaire** : $\langle u,v \rangle:X\times X\to \mathbb{R}^+{}$  
	1. *bilinéaire* : $\langle \alpha u + w,v \rangle=\alpha\langle u,v \rangle + \langle w,v \rangle{}$  
	2. *symétrique* : $\langle u,v \rangle= \langle v,u \rangle{}$  
	3. *défini positif* : $\langle u,u \rangle>0 : u\quad \forall u\neq 0{}$  
  
- Produit scalaire **Complexe** : $\langle u,v \rangle:X\times X\to \mathbb{C}{}$  
	1. *sesquilinéaire* : 1er : *antilinéaire*(linéaire pdv conjugé) ; 2eme *linéaire* : $\langle \alpha f,\beta g \rangle=\alpha^*\langle f,\beta g \rangle = \alpha^*\beta\langle f,g \rangle{}$  
	2. *symétrie conjugée* : $\langle f,g \rangle= \langle g,f \rangle^*{}$  
  
- identité du *parallélogramme* : $||u+v||^2+||u-v||^2=2||u||^2+2||v||^2{}$  
	- ⇒$\langle u,v \rangle=\frac{||u+v||^2-||u-v||^2}{4} =\frac{||u+v||^2-||u||^2-||v||^2}{2}{}$  
	- (th. *Fréchet-Von Neumann-Jordan* )  
  
- prop. *Cauchy-Schwarz* : $\lvert \langle f,g \rangle \rvert\leq \lvert \lvert f \rvert \rvert\cdot \lvert \lvert g \rvert \rvert{}$  
  
- *orthogonaux* : $\langle u,v \rangle=0\implies u\perp v{}$   
  
- *parallèles* : $\exists \alpha:\alpha u=v\implies u\mid\mid v{}$  
&nbsp;  
&nbsp;  
  
- Espace **préhilbertiens** : $(X, \langle \cdot,\cdot \rangle){}$ espace vectoriel  
  
- Espace de **Hilbert** $\mathfrak{H}{}$ : préhilbertiens + Complet      (⇒ $\mathfrak{B}{}$)   
&nbsp;  
## Projection et base  
  
- **Projection** sur $M\subseteq \mathfrak{H}{}$: $P_{M}f=\sum \langle f,u_{i} \rangle u_{i} {}$   
	- $P_{M}f \in M{}$  et $\forall g \in M:\langle f-P_{M}f,g \rangle=0{}$  
  
- $\{ u_{j} \}_{j\in J}{}$ *base* de $E={}span\{ u_{j}: j\in J \}{}$(combili$u_{j}{}$): *génératrice* + *li-indé* (*de hamel*)  
	- famille *libre*, *li-indé* : $\sum \alpha_{j}u_{j}=0 \iff \alpha_{j}=0{}$   
	- famille *génératrice* de $E{}$ :  $\forall f\in E:f=\sum \langle u_{j},f \rangle{}u_{j}{}$  
  
- $\{ u_{j} \}_{j\in J}{}$ *orthonormé* : $\langle u_{i}, u_{j} \rangle= \delta_{i,j}:=\left\{\begin{aligned} 0:i\neq j \\1: i=j \end{aligned}\right. {}$  
  
- *base orthonormée* de $\mathfrak{H}{}$ :   
	- $\iff{}\mathfrak{H}$ ensemble orthonormé maximal  
	- $\iff{}$*identité de parseval* $\forall f \in \mathfrak{H}, \|f\|^2 = \sum_{j \in J} |\langle u_j, f \rangle|^2{}$   
	- $\iff\{ f \in \mathfrak{H} \ | \ \forall j \in J, \langle u_j, f \rangle = 0 \} = \{0\}​{}$  
  
- $\mathfrak{H}{}$ → $\exists{}$*base* (séparable ⇒ *Gram-Schmidt*; sinon *Axiome du choix*)  
  
- soit $f_{\mid\mid}=\sum\langle u_{j},f \rangle u_{j}{}$ et $f_{\perp}=f - f_{\mid\mid}{}$ ($f=f_{\mid\mid}+f_{\perp}{}$)  
	- $\langle f_{\mid\mid},f_{\perp} \rangle= \langle u_{j},f_{\perp} \rangle=0{}$  
	- $|| f||^2=|| f_{\mid\mid}||^2+|| f_{\perp }||^2{}$  
  
- *inégalité de Bessel* : $\{ u_{j} \}_{j\in J}{}$ *orthonormé*⇒$\forall f\in \mathfrak{H}{}:\sum\lvert \langle u_{j},f \rangle \rvert^2\leq \lvert \lvert f \rvert \rvert^{2}$  
	- (égal si base orthonormée)  
  
- *Lemme de Riesz* : $Y\subset X{}$ s espace vectoriel fermé : $\exists u\in X:\lvert \lvert u \rvert \rvert=1,d(u,f)\geq r < 1{}$   
  
- $\hat{f}$ = limite de combinaisons linéaires de $\{u_j\}_{j\in J}$ ⇒ $\|\hat{f}-f\|^2 \geq \| f_\parallel - f \|^2$  
