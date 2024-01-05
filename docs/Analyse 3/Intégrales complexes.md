---  
share: true  
category: Analyse 3  
tags:  
  - matière  
created: 2023-12-24  
updated: 2024-01-06  
title: Intégrales complexes  
---  
  
$\int _{\gamma}f(z) \, dz=\int_{a}^{b} f(\gamma(t))\gamma'(t) \, dt$  
avec chemin $\gamma$ cont déribable sur $[a,b]$ et la taille du chemin $l(\gamma):=\int_{a}^{b}|\gamma'(t)|  \, dt$  
  
- décomposer $\gamma$ non cont dérivable en $\gamma_{i}$ cont dérivables ⇒ sommer les intégrales  
  
- Borne $M$ : $|f(z)| \leq M$ ⇒ $|\int_{\gamma}f(z)  \, dz|\leq Ml(\gamma)$  
  
- convergence :  si $f_{n}$(suite de f cont) converge uniformément vers $f$ sur $\gamma$  
	- ⇒ $\int _{\gamma}f(z) \, dz=\lim_{ n \to \infty }\int _{\gamma}f_{n}(z) \, dz$  
  
- *Lemme de Goursat* : $f:\mathcal{A}\to \mathbb{C}$  dérivable et  $T\in A$ ⇒ $\int _{\partial T}f(z) \, dz=0$  
  
# Théorème des résidus  
  
$\oint_{\gamma}fdz=2\pi i\sum_{c}^{}ind(\gamma,c)res(f,c)$  
*Indice* $Ind(f,\gamma)$ : nb tour de $\gamma$ autour de $c$ (sens trigonométrique)  
*Résidu* : terme $a_{-1}=\frac{1}{2\pi i}\oint_{C(c,1)} f(z)\,dz$ de la série de Laurent  
  
- si $c$ est une singularité apparente : $a_{-1}=0$  
  
- $c$ est un pole d'ordre 1 : $a_{-1}=\lim_{ z \to c }(z-c)f(z)$  
	- $f=\frac{g}{h}$ alors $a_{-1}=\frac{g}{h'}$  
  
- $c$ est un pole d'ordre $n$ : $a_{-1}=\lim_{ z \to c } \frac{((z-c)^nf(z))^{(n-1)}}{(n-1)!}$ :  
	- $f=\frac{h}{(z-c)^n}$ et $h(z-c)\neq 0$  
  
- $c$ est une singularité essentielle : ? → série de Laurent explicite ou formule intégrale  
## Singularités  
point $c$ isolé ou $f$ n'est pas définie   
  
- **poles** d'ordre $n$ : $a_{-n}\neq 0; \forall k>n, a_{-k}=0$  
  
- Singularité **apparente** : $\forall k>0,a_{-k}=0$  
  
- Singularité **essentielle** : le reste (+complexe) ($e^{1/z}$)  
# Homotopie  
  
## Chemins homotopes  
**homotopie** : transformation continue : $\Gamma(t,s):[0,1]^{2}\to A$  
$\gamma_{1},\gamma_{2}:[0,1]\to A$ **homotopes** ssi existe une homotopie:   
  
- $\Gamma(t,0)=\gamma_{1}(t)$ et $\Gamma(t,1)=\gamma_{2}(t)$ avec $\forall t\in [0,1]$  
  
- chemin fermé : $\forall s \in[0,1],\Gamma(0,s)=\Gamma(1,s)$  
  
- chemin ouvert : $\Gamma_{s}(0,s)=\Gamma_{s}(1,s)=0$  
*Théorème de l'invariance* : soit $f$ holomorphe : $\int_{\gamma_{1}}^{} f(z) \, dz=\int_{\gamma_{2}}^{} f(z) \, dz$  
# Primitives  
$f$ primitivable : $F'=f$ :  
  
- $\int _{\Gamma}f(z) \, dz=F(\gamma(b))-F(\gamma(a))$  
  
Ensemble **étoilé** en $z_{0}$ : $\forall z\in D$ chemin droit $c:z_{0}\to z$, $c\in D$  
$\mathcal{A}\in \mathbb{C}$ ouvert, étoilé, $f:\mathcal{A}\to \mathbb{C}$ dérivable : $F(z):=\int_{z_{0}}^{z} f(x) \, dw$  
	⇒$F'(z)=f(z)$  
Ensemble **simplement connexe** : connexe et sans trou  
$\mathcal{A}\in \mathbb{C}$ ouvert, simplement connexe, $f:\mathcal{A}\to \mathbb{C}$ dérivable  
	⇒$F'(z)=f(z)$  
Ensemble **connexe** : E != réunion 2 ensembles fermés disjoints  
Ensemble **connexe par arcs** : tous les points sont reliés de façon continue  
  
## Creer une série candidate  
## Valider la série candidate  
## Théorème intégral de Cauchy  
