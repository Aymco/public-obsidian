---  
share: true  
category: Physique 3  
tags:  
  - matière  
created: 2023-12-23  
updated: 2024-01-13  
title: puits et barrières de potentiel  
---  
  
$V$ change brutalement de valeur  
voir aussi [Fonction d'onde de Schrödinger](Fonction%20d'onde%20de%20Schr%C3%B6dinger.md)  
# Puits Infinis  
puit : $[0,L]$ avec $U(x)=\left\{\begin{align} 0 \;&\text{si}\;x \in P\\\infty \;& \end{align}\right.$  
  
- mode $n$ (cas d'onde stationnaire) : $\psi_{n}=\sqrt{ \frac{2}{L} }\sin\left( \frac{n\pi x}{L} \right)\in P$   
  
- Energie propre : $E_{n}=\frac{n^{2}h^{2}}{8mL^{2}}$   
	- ⇒+Dimensions :$\psi=\prod\psi_{n_{i}}$ et $E=\sum E_{n_{i}}$  
# Puit Fini  
$P=\left[ -\frac{L}{2}; \frac{L}{2}\right]$ avec $U(x)=\left\{\begin{align} -U_{0} \;&\text{si}\;x \in P\\0 \;& \end{align}\right.$ avec $U_{0}$ le travail de sortie  
  
- si $E>U_{0}$ alors particule indépendante du puit  
  
- solution  $\psi(x)=\left\{\begin{align} Ae^{\alpha x}\;&\text{si}\;x<L /2\\C\cos(\beta x)\;&\text{si}\; x \in P\\Be^{-\alpha x}\;&\text{si}\;x>L /2 \end{align}\right.$ (sym $\cos$ → asymétrique: $\sin$)  
		avec $A,B,C,\alpha,\beta$ liés entre eux  
  
- énergie $E_{n}=-\frac{\hbar^{2}\alpha^{2}_{n}}{2m}$  
> [!note] un electron peut quitter le puits sans avoir l'énergie nécéssaire  
# Barrière de potentiel  
barrière : $[0,L]$ avec $U(x)=\left\{\begin{align} U_{0} \;&\text{si}\;x \in B\\0 \;& \end{align}\right.$  
  
- Solution : $\psi(x)=\left\{\begin{align} Ae^{ikx}+B^{-ikx}\;&\text{si}\;x<0\\Ce^{\alpha x}+De^{-\alpha x}\;&\text{si}\;x \in B\\Fe^{ikx}\;&\text{si}\;L<x \end{align}\right.$  (contraintes de continuité)  
	- $Ae^{ikx}$ onde *incidente*  
	- $B^{-ikx}$ onde *réfléchie*  
	- $Fe^{ikx}$ onde *transmise*  
  
- si $E>U_{0}$ : particule quasi libre (barrières fines parfois plus réfléchissantes que les grosses)  
  
- *Effet tunnel*  $E<U_{0}$ : la particule peut traverser la barrière (si $F \neq 0$)  
	- proba rebondisse $R$  - traverse $T$ → $T+R=1$ :   
  
  
$$  
T=\frac{4E(U_{0}-E)}{4E(U_{0}-E)+U_{0}^{2}\sinh ^{2}\left( \frac{L}{\hbar}\sqrt{ 2m(U_{0}-E) } \right)}  
  
  
$$  
  
- ⇒ microscope a effet tunnel   
