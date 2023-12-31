---
created: 2023-12-03
updated: 2023-12-29
---

# Application : [[../thematiques/EDP#Equation de Laplace ${} nabla {2}u=0$ - Elliptique|EDP > Equation de Laplace ${} nabla {2}u=0$ - Elliptique]] et Poisson
## Sur un pavé
**fonctions univariées** : $u(x,y)=X(x)\cdot Y(y)$
équation en 2 dimensions : $u_{xx}+u_{yy}=0  \implies \frac{X''}{X}+\frac{Y''}{Y}=0$ 
### Trouver X et Y
on applique le théorème : $\frac{X''}{X}=-\frac{Y''}{Y}=\lambda$ voir : [[./problème aux valeures propres|problème aux valeures propres]]
- solution : $u(x, y) = \sum_{1}^{\infty} X(x)Y (y)$
### Contraindre aux condition non-homogènes
- On multiplie l’égalité par $\sin(kmx)$ (ou autre fonction orthogonale sur $[0,L]$)
- On intègre pour trouver les $E_{n}$ 
- $u=\sum u_{i}$ : chaque solution $u_{i}$ prends 1 condition non-homogène
### Lien avec fonction holomorphe
$\exists f(x,y)=u(x,y)+iv(x,y)$ holomorphe : $\mathbb{R}(f)=u$
- $\nabla u,\nabla v$ orthogonaux
- *lignes de champ* : $\frac{ d\xi(t) }{ dt }=\nabla u$  → $v(\xi (t))=cst$
## Dans un secteur
pour un cercle : $u_{rr}+\frac{u_{r}}{r}+\frac{u_{\theta\theta}}{r^{2}}=0$
$u(r,\theta)=R(r)\Theta(\theta)$ ⇒ $\frac{{r^{2}R''+rR'}}{R}=-\frac{\Theta''}{\Theta}=\lambda$
- $\Theta$ de période $2\pi$ 
- $R_{n}(r)=C_{n}r^{k_{n}}+D_{n}r^{-k_{n}}$ ([[./équation d'Euler|équation d'Euler]] d'ordre 2)
	- $R(0)$ est fini ⇒ $D_{n}=0$
	- $k=0$ ⇒ $R_{n}(r)=C_{n}\ln(r)+D_{n}$
- *Théorème de la valeur moyenne* : valeur au centre d’un cercle compris dans le domaine $\Omega$ est égal à la moyenne sur le cercle
- *Théorème du maximum-minimum* : La valeur maximale (minimale) de $u$ est toujours atteinte sur la frontière du domaine
# Application : [[../thematiques/EDP#Equation d'onde $c {2} nabla {2}u-u_{tt}=0$ - hyperbolique|EDP > Equation d'onde $c {2} nabla {2}u-u_{tt}=0$ - hyperbolique]]
## Sur un pavé (2 dimensions)
séparation des variables : $u(x,y,t)=\phi(x,y)T(t)$
équation de base : $c^{2}T\nabla^{2}\phi-T''\phi=0$
→ $\frac{\nabla^{2}\phi}{\phi}=\frac{T''}{c^{2}T}=\lambda$
eq onde oscillent : $\lambda=-k^{2}$
- comme $\lambda<0$ : $T(t)=A\cos(kct)+B\sin(kct)$
	(fréquence  $f=\frac{kc}{2\pi}$)
- 2eme equation : $\nabla^{2} \phi+k^{2}\phi=0$ [[./Problème de Helmholtz|Problème de Helmholtz]]
### Recomposer $u$
$u_{mn}=\phi_{mn}T_{mn}$
$u(x,y,t)=\sum_{}^{m}\sum_{}^{n}u_{mn}$

### Determiner les coefficients
## Sur un anneau
$u(r,\theta,t)=R(r,\theta)T(t)$
- pour $R$ :$z^{2}R''+zR' +(z^{2} -m^{2})R=0$ [[./Problème de Bessel|Problème de Bessel]]
- $T$: trivial
# Application : [[../thematiques/EDP#Equation de diffusion ${} alpha nabla {2}u-u_{t}=0$ - Parabolique|EDP > Equation de diffusion ${} alpha nabla {2}u-u_{t}=0$ - Parabolique]]
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

