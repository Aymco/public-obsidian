---  
created: 2023-12-03  
updated: 2024-01-05  
share: "true"  
category: Analyse 3  
---  
  
# Application : [EDP > Equation de Laplace](EDP.md#equation-de-laplace) et Poisson  
## Sur un pavé  
**fonctions univariées** : $u(x,y)=X(x)\cdot Y(y)$  
équation en 2 dimensions : $u_{xx}+u_{yy}=0  \implies \frac{X''}{X}+\frac{Y''}{Y}=0$   
  
- ⇒ $\frac{X''}{X}=-\frac{Y''}{Y}=\lambda$ voir : [problème aux valeures propres](probl%C3%A8me%20aux%20valeures%20propres.md)  
  
- solution : $u(x, y) = \sum_{1}^{\infty} X(x)Y (y)$  
  
- *condition non-homogènes* : multiplie par $\sin(kmx)$ (f orthogonale sur $[0,L]$)  
	- On intègre pour trouver les $E_{n}$   
	- $u=\sum u_{i}$ : chaque solution $u_{i}$ prends 1 condition non-homogène  
  
- Lien avec *fonction holomorphe*: $\exists f(x,y)=u(x,y)+iv(x,y)$ holomorphe :  
	- $\mathbb{R}(f)=u$ et $\nabla u,\nabla v$ orthogonaux  
  
- *lignes de champ* : $\frac{ d\xi(t) }{ dt }=\nabla u$  → $v(\xi (t))=cst$  
## Dans un secteur  
pour un cercle : $u_{rr}+\frac{u_{r}}{r}+\frac{u_{\theta\theta}}{r^{2}}=0$  
$u(r,\theta)=R(r)\Theta(\theta)$ ⇒ $\frac{{r^{2}R''+rR'}}{R}=-\frac{\Theta''}{\Theta}=\lambda$  
  
- $\Theta$ de période $2\pi$   
  
- $R_{n}(r)=C_{n}r^{k_{n}}+D_{n}r^{-k_{n}}$ ([équation d'Euler](%C3%A9quation%20d'Euler.md) d'ordre 2)  
	- $R(0)$ est fini ⇒ $D_{n}=0$  
	- $k=0$ ⇒ $R_{n}(r)=C_{n}\ln(r)+D_{n}$  
  
- *Théorème de la valeur moyenne* : valeur au centre d’un cercle compris dans le domaine $\Omega$ est égal à la moyenne sur le cercle  
  
- *Théorème du maximum-minimum* : La valeur maximale (minimale) de $u$ est toujours atteinte sur la frontière du domaine  
# Application : [EDP > Equation d'onde](EDP.md#equation-donde)  
## Sur un pavé (2 dimensions)  
séparation des variables : $u(x,y,t)=\phi(x,y)T(t)$  
équation de base : $c^{2}T\nabla^{2}\phi-T''\phi=0$ → $\frac{\nabla^{2}\phi}{\phi}=\frac{T''}{c^{2}T}=\lambda$  
eq onde oscillent : $\lambda=-k^{2}$  
  
- comme $\lambda<0$ : $T(t)=A\cos(kct)+B\sin(kct)$  
	(fréquence  $f=\frac{kc}{2\pi}$)  
  
- 2eme equation : $\nabla^{2} \phi+k^{2}\phi=0$ [Problème de Helmholtz](Probl%C3%A8me%20de%20Helmholtz.md)  
  
- Recomposer $u$ : $u_{mn}=\phi_{mn}T_{mn}$ → $u(x,y,t)=\sum_{}^{m}\sum_{}^{n}u_{mn}$  
  
- Determiner les coefficients  
## Sur un anneau  
$u(r,\theta,t)=R(r,\theta)T(t)$  
  
- pour $R$ :$z^{2}R''+zR' +(z^{2} -m^{2})R=0$ [Problème de Bessel](Probl%C3%A8me%20de%20Bessel.md)  
  
- $T$: trivial  
# Application : équation de diffusion  
  
- [EDP > Equation de diffusion](EDP.md#equation-de-diffusion)  
solution de régime et transitoire : $u=R+\Theta$  
sol de régime :  
  
- on pose : $\frac{ \partial U }{ \partial t }=0$  
  
- résoudre EDP  
solution transitoire : injecte $u=R+\Theta$ dans EDP  
  
# Plus  
### Théorème des fonction indépendantes  
  
  
$$  
\begin{align}  
p(x) + g(y)&=c \\  
p'(x) =g'(y)&= 0  
\end{align}  
  
  
$$  
