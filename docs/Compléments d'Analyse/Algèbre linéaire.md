---  
share: true  
category: Compléments d'Analyse  
tags:  
  - matière  
created: 2024-05-31  
updated: 2024-06-05  
---  
# Espace vectoriel $X{}\subseteq \mathbb{R}^n$  
1. somme *commutative*  
2. multiplication *distributive*  
3. $\exists{}0_{X},1_{X}$ : neutres pour les 2 opérations  
&nbsp;  
&nbsp;  
# Application - opérateur  
$A:\mathfrak{D}(A)\subset X\to Y :A(x)=y{}$.      (Opérateur $X\to X{}$):  
  
- *linéaire* : $A\left( \sum\lambda_{i}x_{i} \right)=\sum\lambda _{i}A(x_{i}){}$   ~~. $\forall \lambda _{i}\in \mathbb{C},\forall x_{i}\in \mathfrak{D}(A){}$~~  
  
- *borné* : $| |A| |=\sup \limits_{\lvert \lvert x \rvert \rvert=1} \lvert \lvert A(x) \rvert \rvert<\infty$  = image d'une boule de rayon 1 bornée  
	- ⇔$\exists M>0:\forall x\in U: \lvert \lvert x \rvert \rvert\leq M{}$  
	- ⇒ A continue en 0  
	- ⇔ continue  
	- $\iff \mathfrak{D}(A) <\infty{}$  
	- ⇔ lipschitzienne  
	- th. *bolzano weirstrass* : E *infini* *borné* ⇒ admet points limite  
	- $A{}$ borné, $\mathfrak{D}(A){}$ dense dans X et Y complet ⇒ $A{}$ A admet prolongement continu unique à tout X entier (agrandit la domaine car continuité sur les bords)  
	- (intégration → *borné* ; derivation → *!borné*)  
  
- $\mathscr{L}(X,Y)$ ensemble applicatoin *linéaires bornées* :   
	1. norme  
	2. $(Y,\lvert \lvert \cdot* \rvert \rvert_{Y}){}$ complet ⇒ $\mathscr{L}{}$ complet  
	3. $X^*:=\mathscr{L}(X,\mathbb{C}){}$ complet  
  
- **kernel** $kerA$ : ensemble des entrées qui ont pour image $0$  
  
- soit $A(x)=Bx$ ⇒ $C(B)=ImA$ , $N(B)=KerA$  
# Projection et base dans un espace de hilbert  
  
- $\{ u_{j} \}_{j\in J}{}$ *base* de $E={}span\{ u_{j}: j\in J \}{}$(combili$u_{j}{}$): *génératrice* + *li-indé*  
	- famille *génératrice* de $E{}$ :  $\forall f\in E:f=\sum \langle u_{j},f \rangle{}u_{j}{}$  
	- famille *libre*, *li-indé* : $\sum \alpha_{j}u_{j}=0 \iff \alpha_{j}=0{}$   
  
- $\{ u_{j} \}_{j\in J}{}$ *orthonormé* : $\langle u_{i}, u_{j} \rangle= \delta_{i,j}:=\left\{\begin{aligned} 0:i\neq j \\1: i=j \end{aligned}\right. {}$  
	- $f_{\mid\mid}=\sum\langle u_{j},f \rangle u_{j}{}$ et $f_{\perp}=f - f_{\mid\mid}{}$   
	- $\langle f_{\mid\mid},f_{\perp} \rangle= \langle u_{j},f_{\perp} \rangle=0{}$  
	- $|| f||^2=|| f_{\mid\mid}||^2+|| f_{\perp }||^2{}$  
  
- *base orthonormée* de $\mathfrak{H}{}$ :   
	- $\iff{}\mathfrak{H}$ ensemble orthonormé maximal  
	- $\iff\{ f \in \mathfrak{H} \ | \ \forall j \in J, \langle u_j, f \rangle = 0 \} = \{0\}​{}$  
  
- $\mathfrak{H}{}$ → $\exists{}$*base* (séparable ⇒ *Gram-Schmidt*; sinon *Axiome du choix*)  
  
- *inégalité de Bessel* : $\{ u_{j} \}_{j\in J}{}$ *orthonormée* finie⇒$\forall f\in \mathfrak{H}{}:\sum\lvert \langle u_{j},f \rangle \rvert^2\leq \lvert \lvert f \rvert \rvert^{2}$  
	- (égal si *base orthonormée*)  
  
- **Projection** sur $M\subseteq \mathfrak{H}{}$: $P_{M}f=\sum \langle f,u_{i} \rangle u_{i} {}$ (linéaire borné)  
	- $P_{M}f \in M{}$  et $\forall g \in M:\langle f-P_{M}f,g \rangle=0{}$  
	- $\forall g\in M:\lvert \lvert P_{M}(f) -f\rvert \rvert\leq \lvert \lvert g-f \rvert \rvert{}$   
	- *Lemme de Riesz* : $l\in l(\mathfrak{H},\mathbb{C}):\exists g\in \mathfrak{H}:l(f)=\langle g,f \rangle \quad\forall f\in \mathfrak{H}{}$  
  
- $\hat{f}$ = limite de combinaisons linéaires de $\{u_j\}_{j\in J}$ ⇒ $\|\hat{f}-f\|^2 \geq \| f_\parallel - f \|^2$  
