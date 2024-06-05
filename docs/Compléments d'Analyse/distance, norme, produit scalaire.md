---  
share: true  
category: Compléments d'Analyse  
tags:  
  - matière  
created: 2024-05-31  
updated: 2024-06-05  
---  
# Distances  
  
- **Distance** :$X\times X\to R^+{}$ 3 conditions : ($d(u,v)=| |u-v| |{}$)  
	1. *symétrie* : $d(u,v)=d(v,u){}$  
	2. *inégalité triangulaire* : $d(u,v)\leq d(u,w)+d(w,v){}$  
		- $\iff{}$*inégalité triangulaire inverse* :$|d(u,w)-d(w,v)| \leq d(u,v){}$  
	3. $d(u,v)=0\iff u=v{}$   
  
- Distance *euclidienne* : $d_{e}(x,y)=\sqrt{ \sum_{i=0}^{n-1} (x_{i}-y_{i})^{2}}{}$  
  
- distance de *manhattan* : $d_{m}(x,y)=\sum_{0}^{n-1}|x_{i}-y_{i}|{}$  
# Norme  
  
- **Norme** : $||\cdot||:X\to \mathbb{R}^+{}$  (continue, convexe, k-Lipschitzienne)  
	1. *séparation* : $\lvert \lvert x \rvert \rvert=0 \implies x=0{}$   
	2. *absolue homogénéité* : $\lvert \lvert \alpha x \rvert \rvert = \lvert \alpha \rvert\cdot \lvert \lvert x \rvert \rvert{}$ ~~.$\forall \alpha \in \mathbb{R},\forall x\in X{}$ ~~  
	3. *inégalité triangulaire* : $||x+y||\leq||x||+||y||{}$  ~~.$\forall x,y{}$~~  
  
- norme *induite* : $||u||=d(0,u){}=\sqrt{ \langle u,u \rangle }{}$  
  
- n. euclidienne $| | u| |_{p}=\sqrt[p]{ \sum |u_{i}|^p }{}$  → sur f : $\lvert \lvert f \rvert \rvert_{p}=\sqrt[p]{  \int_{X} \lvert f \rvert^p \, d\mu} {}$  
  
- n. du maximum  $| | f| |_{\infty}=max_{x\in I}(f(x)){}$ ~~.$f\in C(I){}$ ~~  
# Produit scalaire  
  
- **Produit scalaire** : $\langle u,v \rangle:X\times X\to \mathbb{R}^+{}$  
	1. *bilinéaire* : $\langle \alpha u + w,v \rangle=\alpha\langle u,v \rangle + \langle w,v \rangle{}$  
	2. *symétrique* : $\langle u,v \rangle= \langle v,u \rangle{}$  
	3. *défini positif* : $\langle u,u \rangle>0 : u\quad \forall u\neq 0{}$  
  
- Produit scalaire **Complexe** : $\langle u,v \rangle:X\times X\to \mathbb{C}{}$  
	1. *sesquilinéaire* : 1er : *antilinéaire*(linéaire pdv conjugé) ; 2eme *linéaire* : $\langle \alpha f,\beta g \rangle=\alpha^*\langle f,\beta g \rangle = \alpha^*\beta\langle f,g \rangle{}$  
	2. *symétrie conjugée* : $\langle f,g \rangle= \langle g,f \rangle^*{}$  
  
- identité du **parallélogramme** : $||u+v||^2+||u-v||^2=2||u||^2+2||v||^2{}$  
	- ⇒$\langle u,v \rangle=\frac{||u+v||^2-||u-v||^2}{4} =\frac{||u+v||^2-||u||^2-||v||^2}{2}{}$  
	- (th. *Fréchet-Von Neumann-Jordan* )  
  
- prop. *Cauchy-Schwarz* : $\lvert \langle f,g \rangle \rvert\leq \lvert \lvert f \rvert \rvert\cdot \lvert \lvert g \rvert \rvert{}$  
  
- *orthogonaux* : $\langle u,v \rangle=0\implies u\perp v{}$   
  
- *parallèles* : $\exists \alpha:\alpha u=v\implies u\mid\mid v{}$  
