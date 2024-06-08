---  
share: true  
category: Optimisation  
tags:  
  - matière  
created: 2024-06-08  
updated: 2024-06-08  
---  
  
- opti $\min\limits_{x\in X} f(x){}$ avec $X\subseteq \mathbb{R}^n{}$  
	- → *solution optimale globale* / *locale*  
&nbsp;  
  
- *Lagrangien* $\mathcal{L(x,\lambda):=f(x)-\sum\lambda _{i}c_{i}(x)}{}$  
  
- **ILGCA**: *I*ndépendance *L*inéaire des *G*radients des *C*ontraintes *A*ctives$\nabla c_{i}(x^*){}$*li-indé*  
  
- **KKT**(Karush-Kuhn-Tucker) : *ILGCA* + $x^*{}$ ⇒ $\exists\lambda^*:\lambda_{i}^*\geq 0{}{}$ :  $\nabla \mathcal{L}(x^*,\lambda^*)=0{}$ et $\lambda_{i}^*c_{i}(x^*)=0{}$  
  
- non-contraint :   
	- $f\in \mathcal{C}^1{}$ : *min local* ⇒ $\nabla f(x^*)=0{}$  
	- $f\in \mathcal{C}^2{}$ : *min local* ⇒ $\nabla^2 f(x^*)\succeq0{}$  
		- les 2 : ⇒ *min local*  
  
- contraint : …. ???  
  
- pb avec contraintes ⇒ **KKT**  
	- sinon : … ??  
## Opti Convexe  
$f,dom{}$ *convexes*  
  
- min local ⇒ global  
  
- E sol optimales : convexe  
  
- cdt opti 1er ordre (KKT, Lagrange, p critique) suffisantes⇒ solution  
  
- $\exists p{}$ de slater : solution ⇒sans exception(li indé) cdt opti 1er ordre   
	- p **de slater** : sol *admissible* : verif *strictement* les égalités  
&nbsp;  
  
- $c_{i}{}$ des égalité → affines et inégalités → concaves ⇒ E convexe  
&nbsp;  
## Méthodes du premier ordre  
$x^*:\nabla f(x^*)=0{}$  
  
- optimisation itérative :  
	- suite $x_{k}\to x^*{}$  
  
- **cdt de Lipschitz** : $\lvert \lvert \nabla f(x)-\nabla f(y) \rvert \rvert\leq L\lvert \lvert x-y \rvert \rvert{}$  
  
- **cdt de ZoutenDijk** : $\sum_{0}^{\infty}\cos ^{2}(\theta_{k})\lvert \lvert \nabla^f (x_{k}) \rvert\rvert^{2}<\infty{}$  
  
- **cdt de Wolfe** : $0<c_{1}<c_{2}<1{}$ : $\exists\alpha_{k}{}$ si $p{}$ descente et $f{}$ bornée inf  
	- *décroissance suffisante* : $\phi(\alpha)\leq \phi(0)+c_{1}\alpha \phi'(0){}$  
	- *courbure* : $\phi'(\alpha)\geq c_{2}\phi'(0){}$  
  
- m. **recherche en ligne** : choisite $x_{0}{}$ et $k=0{}$  
	1. direction $p_{k}{}$ : décroit $\phi'(0)<0\iff\nabla f(x)^Tp<0{}$   
		- m. du **gradient** : $p_{k}=-\nabla f(x_{k}){}$ (sauf si p stationnaire)  
	2. *pas* $\alpha_{k}:x_{k+1}=x_{k}+\alpha_{k}p_{k}{}$   
		- $\alpha_{k}{}$ minimiser : $\phi(\alpha)=f(x_{_{k}}+\alpha p_{k}){}$ (approx)  
	3. si critere pas satisfait → continuer 1.  
	- conv globale :  $f\in \mathcal{C}^1{}$ bornée inf et $p_{k}{}$ descente + *Lipschitz*  ⇒ *ZoutenDijk*  
		- ⇒ m. grad et m. : $p_{k}{}$ ! asymptotiquement orthogonal → conv globalement  
	- *vitesse* : m. gradient exacte(min vrmt):  
		- $f(x)=x^T{}Qx+c^Tx$ : conv de $\lvert \lvert x_{k}-x^* \rvert \rvert{}$ *linéaire* $c=\frac{\lambda _{n}-\lambda_{1}}{\lambda_{n}+\lambda_{1}}{}$   
			- (avec $0<\lambda _{i}<\lambda_{i+1}{}$ val propres de $Q{}$)  
		- conv *quadratique* $f(x_{k})-f(x^*){}$ : $c=r^{2}:r>\frac{\lambda _{n}-\lambda_{1}}{\lambda_{n}+\lambda_{1}}{}$   
			- (avec $0<\lambda _{i}<\lambda_{i+1}{}$ val propres de $\nabla^{2}f(x^*){}$)  
  
- m. **coord par coord** : $\forall x_{i}{}:\min \limits_{x_{i}}f(x){}$ puis recommencer   
	- conv lente et pas sur (Aitken : meme ordre; Gauss-southwell: +grande der. part.)  
&nbsp;  
## Méthodes du second ordre  
avec $\nabla^{2}f{}$  
  
- **m. de Newton** : $x_{k+1}=x_k -\alpha_k\nabla^2f(x_k)^{-1}\nabla f(x_k){}$(*itérative*)  
	- (min du p. de taylor de degré 2 de f autour de $x_{k}{}$)  
	- (eq : newton-raphson → $\nabla f=0{}$)  
  
- **m. de Quasi-Newton** : rapide mais couteuse en stockage et calcul et !conv garantie  
	- $x_{k+1}=x_{k}-B_{k}^{-1}\nabla f(x_{k}){}$ avec approx $B_{k}\approx\nabla^{2}f(x_{k}){}$  
	- mis a jour de rang faible : $B_{k}\to B_{k+1}{}$  
	- $f\in \mathcal{C}^{2}{}$ bornée inf, cdt de *lipschitz* et $\forall k:B_{k}\succ 0{}$ et $\exists M:\lvert \lvert B_{k} \rvert \rvert \lvert \lvert B_{k}^{-1} \rvert \rvert\leq M{}$ et $\alpha_{k}{}$ cdt de *Wolfe* ⇒ *conv globale*  
	- plus efficace :  $x_{k+1}=x_{k}-H_{k}\nabla f(x_{k}){}$avec $H_{k}\approx \nabla^{2}f(x_{k})^{-1}{}$  
		- mis a jour de rang faible : $H_{k}\to H_{k+1}{}$  
  
- **mis a jour de rang faible** : rang 1   
	- *cdt de la sécante* : $s_{k}=x_{k+1}-x_{k}{}$ et $y_{k}=\nabla f(x_{k+1})-\nabla f(x_{k}){}$  
		- $B_{k+1}s_{k}=y_{k}{}$ ou  $s_{k}=H_{k+1}y_{k}{}$  
	- *Mis a jour SR1* : $B_{k+1}=B_{k}+\frac{(y_{k}-B_{k}s_{k})(y_{k}-B_{k}s_{k})^T}{s_{k}(y_{k}-B_{k}s_{k})^T}{}$ ($B_{0}=\alpha I{}$)  
		- $\not\exists{:}$dénom$=0{}$ ,  !garantie $B_{k},H_{k}{}$positive, conv globale ou superlinéaire  
  
- **Mise a jour BFGS** rang 2:  (on pose $p_{k}=(y_{k}^Ts_{k})^{-1}{}$)  
	- $B_{k+1}=B_k+\frac{y_ky_k^T}{y_k^Ts_k}- \frac{B_ks_ks_k^Tb_k}{s_k^TB_ks_k}$   
	- $H_{k+1}=(I-\rho_ks_ky_k^T)H_k(I-\rho_ky_ks_k^T)+\rho_ks_ks_k^T{}$  
		- $H_{k}\succ 0\implies H_{k+1}\succ 0{}$  
		- CONV *globalement* ; $H_{0}\succ 0\implies{}$CONV *superlinéaire*  
	- conditions : $f\in \mathcal{C}^{2}{}$  ; $\nabla^{2}f{}$ cdt lipschitz; $x:f(x)\leq f(x_{0}){}$ convexe; $\lambda{}$ bornés sur $x{}$  
