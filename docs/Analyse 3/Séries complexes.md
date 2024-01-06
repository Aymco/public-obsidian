---  
share: true  
category: Analyse 3  
tags:  
  - matière  
created: 2023-12-24  
updated: 2024-01-06  
title: Séries complexes  
---  
  
voir [Séries](S%C3%A9ries.md)  
# Série potentielle  
  
- définition : $\sum_{n=0}^{\infty}a_{n}(z-b)^n$  
  
- *Continuité* ⇔ tous termes continus  
  
- *Série exponentielle* : $e^z=\sum_{n=0}^{\infty} \frac{z^n}{n!}$  
  
- *décroissance géométrique* : $\exists t \in]0,1[,C>0,\rho>0:\forall n\in\mathbb{N} ,|a_{n}|\rho^n\leq Ct^n$ ⇒ il existe $t,C,\rho$ tel que $Ct^n$ borne les indices $a_{n}$ * $\rho^n$  
  
  
- *Rayon de convergence* : fonction de base $R=\left( \lim_{ n \to \infty } | \frac{a_{n+1}}{a_{n}}| \right)^{-1}$  
	- fonction de racine plus compliquée :$R=\left( \lim_{ n \to \infty } (sup_{m\geq n}| a_{m}|^{1/m} \right)^{-1}$ ($R=0$ fonctionne toujours mais ! intérêt )  
  
# Séries de Laurent  
approximation globale : $f(z)=\sum_{n=0}^{\infty}a_{n}(z-b)^n+\sum_{n=1}^{\infty}a_{-n}(z-b)^{-n}$  
  
- → *Séries géométriques* : $\frac{1}{1-w}=\sum_{n=1}^{\infty}w^n$ avec $|w|<1$  
  
- *Lemme décalage des coefficients* : $f(z)(z-c)^n=\sum_{k\geq 0}^{}a_{k-n}(z-c)^k +\sum_{k\leq-1}a_{k-n}(z-c)^k$  
  
- Calcul des termes $f:A(c, r, s) \to \mathbb{C}$ holomorphe  
	- ⇒ $a_{n}=\frac{1}{2\pi i}\int_{\partial B(c,t)} \frac{f(w)}{(w-c)^{n+1}}  \, dw$ (avec $t\in ]s,r[$ )  
