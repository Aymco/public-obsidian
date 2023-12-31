---  
share: true  
category: Analyse 3  
tags:  
  - matière  
created: 2023-12-24  
updated: 2024-01-08  
title: Fonctions complexes  
---  
  
$f:\mathbb{C}\to \mathbb{C}:z \to f(z)$  
*Fonction conforme* : préserve les angles orientés $\iff$ $f$ est une bijection holomorphe  
## Limite  
  
- définition : $\lim_{ z \to w }f(z)=y$ si $\forall\epsilon>0,\exists\delta>0,z\in B_{*}(w,\delta)\to f(z)\in B(y,\epsilon)$  
  
- soit $w\in dom f$ ouvert, alors $\lim_{ \delta_{R}\in \mathbb{R}, \delta_{R} \to 0 } f(w + \delta_{R}z) = y$  
  
- *Théorème de l'unicité de la limite* : $\lim_{ z \to w }f(z)$ valeur unique  
## Dérivées  
  
- dérivée : $f'(z)=\frac{ df }{ dz }z=\lim_{ \Delta \to 0 } \frac{{f(z+\Delta)-f(z)}}{\Delta}$  
  
- *Condition de Cauchy-Riemann* : $f(x,y)=u(x,y)+iv(x,y)$ derivable $\iff \left\{\begin{align} u_{x}&=v_{y}\\u_{y}&=-v_{x} \end{align}\right.$  
  
- $f$ *holomorphe* : *dérivable* infiniment sur $A$ ($\mathbb{C}:f$ dérivable ⇒ dérivable infiniment)  
### Principe des zeros isolés  
  
- $z_{0}$ **zéro isolé** ⇔ $f(z_{0})=0$ et $\forall z\in B^*(z_{0},\epsilon), f(z)\neq 0$ avec $f:\mathcal{A}\to \mathbb{C}$ un ensemble ouvert connexe, holomorphe  
  
- *tous zéros isolés*  -ou-  $f(z)=0$  
	- si $h=f-g$ et $f,g$ possèdent 2 points non isolés de meme image → $f=g$  
## Fonction analytique  
  
- analytique ⇒ holomorphe sur $A$  
  
- ⇔ définie localement avec une série potentielle (série converge)  
  
- ⇔ définie partout aver une série de Laurent (série converge)  
  
- $\exists w\in A :f(w)\neq 0$ et zéro non-isolé ⇒ f ! analytique  
# Fonctions multiformes  
retourne un ensemble $f:\mathbb{C}\to A\subset \mathbb{C}$  
  
- Exemple : $|z|=arg(z)=\arctan (\frac{b}{a})+2k\pi$ (, , racine carrée)  
	- $arg(zw)=arg(z)+arg(w)$  
	- logarithme : $\log(z)=\log(|z|)+i\cdot arg(z)$  
  
- **branche** $\bar{f}$  
  
- **point de branchement** : (point singulier)( → arg(z) : 0)  
	- image de f d'un tour de est une courbe non fermée   
  
- **coupure** : couper notre région pour isoler → arg(z) : $[0,2\pi[$  
  
  
  
- fonction **entière** : définie partout  
