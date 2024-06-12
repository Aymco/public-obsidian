---  
share: true  
category: Optimisation  
tags:  
  - matière  
created: 2024-06-08  
updated: 2024-06-12  
---  
  
- opti $\min\limits_{x\in X} f(x){}$ avec $X\subseteq \mathbb{R}^n{}$ ($c_{i}(x)=\geq 0{}$) et $x^*{}$ optimum local  
	- → *solution optimale globale* / *locale*  
  
- (*Lagrangien* $\mathcal{L(x,\lambda):=f(x)-\sum\lambda _{i}c_{i}(x)}{}$)  
  
- **ILGCA** **I**ndépendance **L**inéaire des **G**radients des **C**ontraintes **A**ctives$\nabla c_{i}(x^*){}$*li-indé*  
  
- $\exists\lambda:{}$**KKT**(**K**arush-**K**uhn-**T**ucker): $\nabla f(x^*)=\sum\limits_{c_{i}(x^*)=0} \lambda_{i}\nabla c_{i}(x^*){}$ (ingégalités: $\lambda_{i}^*\geq 0{}$)  
  
- condition optimalité *non-contraint* (*libre*):   
	- $\nabla f(x^*)=0{}$  ⇐ *min local*     ($f\in \mathcal{C}^1{}$) (p critique)  
	- $\nabla^2 f(x^*)\succeq0{}$⇐ *min local*     ($f\in \mathcal{C}^2{}$)  
	- $\nabla f(x^*)=0{}$ et $\nabla^2 f(x^*)\succ0{}$ ⇒ *min local strict* ($f\in \mathcal{C}^2{}$)  
  
- condition optimalité *contraint* :   
	- $f,c\in \mathcal{C}^1{}$  et *ILGCA* : *KKT* ⇐ *min local*  
	- ! ILGCA⇒  *exceptions* ?  
CONVERGENCE :   
  
- conv *quadratique* : $\lvert \lvert x_{k}-x^* \rvert \rvert\leq c\lvert \lvert x_{k+1}-x^* \rvert \rvert^{2}{}$ avec $0<c{}$ ⇒  
	- $\exists k:\lvert \lvert x_{k}-x^* \rvert \rvert< \frac{1}{c}{}$ ⇒ conv locale  
  
- conv *super-linéaire* : $\lim_{ n \to \infty } \frac{\lvert \lvert x_{k+1}−x^*  \rvert \rvert}{\lvert \lvert x_{k}-x^* \rvert \rvert}=0{}$  ⇒  
  
- conv *linéaire* : $\lvert \lvert x_{k}-x^* \rvert \rvert\leq c\lvert \lvert x_{k+1}-x^* \rvert \rvert{}$  avec $0<c<1{}$ ⇒ conv globale  
## Opti Convexe  
pb convexe : $\min, f,dom{}$ *convexes* → sol *convexe*  
  
- *min local* ⇒ *global*  
  
- $c_{i}={}$ → *linéaire* et $\geq\leq{}$ → *concaves* ⇒ dom convexe  
  
- *KKT* ⇒ *min local* (*suffisantes*)   
  
- $\exists p{}$ de slater : _KKT_ ⇐ *min local* (sans ILGCA)   
	- **p de slater** : verif *strictement* les inégalités  
# Méthodes du premier ordre  
$x^*:\nabla f(x^*)=0{}$ soit $\phi(\alpha)=f(x_{k}+\alpha p_{k}){}$  
  
- **cdt de Lipschitz** : $\lvert \lvert \nabla f(x)-\nabla f(y) \rvert \rvert\leq L\lvert \lvert x-y \rvert \rvert{}$  
  
- **cdt de ZoutenDijk** : $\sum_{0}^{\infty}\cos ^{2}(\theta_{k})\lvert \lvert \nabla f (x_{k}) \rvert\rvert^{2}<\infty{}$ et $\theta_{k}:\text{angle :} p_{k}\to p_{k}^*{}$  
  
- **cdt de Wolfe** : $0<c_{1}<c_{2}<1{}$ : $\exists\alpha_{k}{}$ si $p{}$ descente et $f{}$ bornée inf  
	- *décroissance suffisante* : $\phi(\alpha)\leq \phi(0)+c_{1}\alpha \phi'(0){}$  
	- *courbure* : $\phi'(\alpha)\geq c_{2}\phi'(0){}$  
	- **Forte** : *courbure forte* :  $\lvert \phi'(\alpha) \rvert\leq c_{2} \lvert \phi'(0) \rvert{}$  
  
- m. **recherche en ligne** : choisite $x_{0}{}$ et $k=0{}$ (*itérative*) : répéter → satifsait :  
	1. *direction* $p_{k}{}$ : svt *descente* : $\phi'(0)<0\iff\nabla f(x)^Tp<0{}$   
		- m. du **gradient** : $p^*_{k}=-\nabla f(x_{k}){}$ +forte pente (sauf si p stationnaire)  
	2. *pas* $\alpha_{k}:x_{k+1}=x_{k}+\alpha_{k}p_{k}{}$   
		- $\alpha_{k}{}$ : minimiser $\phi(\alpha){}$ (approx)  
	- $f\in \mathcal{C}^1{}$ bornée infer. +$\nabla{}$ *Lipschitz* + $p_{k}{}$ descente + $\alpha_{k}{}$ *Wolfe* ⇒ *ZoutenDijk*   
		- ⇒ m. grad et m. : $p_{k}{}$ ! asymptotiquement orthogonal ⇒ *conv globalement*  
	- **vitesse** : m. *gradient exacte*:   
		- $f(x)=x^T{}Qx+c^Tx$ : conv *linéaire* de $\lvert \lvert x_{k}-x^* \rvert \rvert{}$ selon $c=\frac{\lambda _{n}-\lambda_{1}}{\lambda_{n}+\lambda_{1}}{}$   
			- (avec $0<\lambda _{i}<\lambda_{i+1}{}$ val propres de $Q\succeq 0{}$)  
		- conv *linéaire* de $f(x_{k})-f(x^*){}$ selon $c=r^{2}: \forall r>\frac{\lambda _{n}-\lambda_{1}}{\lambda_{n}+\lambda_{1}}{}$   
			- (avec $0<\lambda _{i}<\lambda_{i+1}{}$ val propres de $\nabla^{2}f(x^*)\succeq 0{}$)  
  
- m. **coord par coord** : $\forall x_{i}{}:\min \limits_{x_{i}}f(x){}$ puis recommencer   
	- conv lente et pas sur (Aitken :→ ordre; Gauss-southwell: +grande der. part.)  
# Méthodes du second ordre  
avec $\nabla^{2}f{}$  
  
- **m. de Newton** : $x_{k+1}=x_k -\alpha_k\nabla^2f(x_k)^{-1}\nabla f(x_k){}$(*itérative*)  
	- (min taylor d=2 de f($x_{k}{}$)) (eq : newton-raphson → $\nabla f=0{}$)  
	- $a_{k}=1{}$, $\nabla^{2}{}$ lipschitz + $\nabla^{2}f\succ 0{}$ : conv *quadratique* selon $c=L\lvert \lvert \nabla^{2}f(x^*)^{-1} \rvert \rvert{}$  
  
- **m. de Quasi-Newton** : rapide mais couteuse en stockage et calcul et !conv garantie  
	1. $x_{k+1}=x_{k}-B_{k}^{-1}\nabla f(x_{k}){}$  
	2. *mis a jour de rang faible* : $B_{k}\to B_{k+1}{}$ ( $B_{k}\approx\nabla^{2}f(x_{k}){}$)  
	- $f\in \mathcal{C}^{2}{}$ bornée inf, $\nabla{}$ *lipschitz* et $\forall k:B_{k}\succ 0{}$ et $\exists M:\lvert \lvert B_{k} \rvert \rvert \lvert \lvert B_{k}^{-1} \rvert \rvert\leq M{}$ et $\alpha_{k}{}$ *Wolfe* ⇒ *conv globale*  
	- $x_{k+1}=x_{k}-H_{k}\nabla f(x_{k}){}$  plus efficace  
  
- **mis a jour de rang faible** : (rang 1) avec $B_{k} \leftrightarrow H_{k }\iff y_{k}\leftrightarrow s_{k}{}$  
	- *cdt de la sécante* : $B_{k+1}s_{k}=y_{k}{}$  
		- $s_{k}=x_{k+1}-x_{k}{}$ et $y_{k}=\nabla f(x_{k+1})-\nabla f(x_{k}){}$ ⇒  
	- *Mis a jour SR1* : $B_{k+1}=B_{k}+\frac{(y_{k}-B_{k}s_{k})(y_{k}-B_{k}s_{k})^T}{(y_{k}-B_{k}s_{k})^Ts_{k}}{}$ ($B_{0}=\alpha I{}$)  
		- $\not\exists{:}$dénom$=0{}$ ,   $B_{k},H_{k}?\succ 0{}$, ?conv globale,superlinéaire  
  
- **Mise a jour BFGS** : (rang 2)   
	- $H_k\succ 0\implies H_{k+1}\succ 0{}$   
	- $H_{0}\succ 0{}$ ⇒ CONV *globalement* ;   
	- $f\in \mathcal{C}^2{}$ +$\nabla{}$Lipschits + $\lambda{}$ bornés sur $\{x :f (x) \leq f (x_0)\}{}$ *convexe* ⇒ CONV *superlinéaire*  
	- pas connaitre : (on pose $p_{k}=(y_{k}^Ts_{k})^{-1}{}$)  
		- $B_{k+1}=B_k+\frac{y_ky_k^T}{y_k^Ts_k}- \frac{B_ks_ks_k^Tb_k}{s_k^TB_ks_k}$   
		- $H_{k+1}=(I-\rho_ks_ky_k^T)H_k(I-\rho_ky_ks_k^T)+\rho_ks_ks_k^T{}$  
			- $H_{k}\succ 0\implies H_{k+1}\succ 0{}$  
