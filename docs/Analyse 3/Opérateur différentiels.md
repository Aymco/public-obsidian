---  
share: true  
category: Analyse 3  
tags:  
  - matière  
created: 2023-12-29  
updated: 2024-01-08  
title: Opérateur différentiels  
---  
  
# Opérateur différentiel $L$  
linéaire si : $L(au + bv) = aL(u) + bL(v)$  
  
soit fonctions propres $X_{n}(x)$, valeurs propres $k_{n}$  
**Produit scalaire** : $\langle X_{m}, X_{n} \rangle=\int_{0}^{L} X_{n}(x)X_{m}(x) \, dx$  
**Auto-adjoint** $L$ : $\langle X_{m},L(X_{n}) \rangle=\langle X_{n},L(X_{m}) \rangle$  
  
- → orthogonaux : $\langle X_{n},X_{m} \rangle=0$  
  
pb matriciel $Ax + \lambda x = 0$:  
  
- vecteurs propres d'une matrices orthogonaux  
  
- A symétrique si $\langle x,Ay \rangle=\langle y,Ax \rangle$  
[nabla](nabla.md)  
## Coordonnées planes  
  
- **Gradient** : $\nabla u=\frac{ \partial u }{ \partial x }\vec{e}_{x}+\frac{ \partial u }{ \partial y }\vec{e}_{y}$  
  
- **divergence** :  $\nabla \cdot u = \frac{ \partial u }{ \partial x }+\frac{ \partial u }{ \partial y }$  
  
- **Laplacien** : $\Delta f=\nabla^{2}f=\nabla\cdot(\nabla f)=\frac{ \partial^{2} u }{ \partial x^{2} }+\frac{ \partial^{2} u }{ \partial y^{2} }$  
## Coordonnées polaires  
  
- **Gradient** : $\nabla u =\frac{ \partial u }{ \partial r }\vec{e}_{r}+\frac{1}{r}\frac{ \partial u }{ \partial \theta }\vec{e}_{\theta}$  
  
- **Divergence** :  $\nabla \cdot u=\frac{1}{r}\left( \frac{ \partial u_{r}r }{ \partial r } + \frac{ \partial u_{\theta} }{ \partial \theta }\right)$  
  
- **Laplacien** : $\Delta f=\nabla^{2}f=\nabla\cdot(\nabla f)=\frac{1}{r} \frac{ \partial  }{ \partial r }\left( r\frac{ \partial f }{ \partial r }  \right)+\frac{1}{r^{2}}\frac{ \partial^{2} f }{ \partial \theta^{2} }$  
## Coordonnées sphériques …  
