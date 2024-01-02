---  
share: true  
category: Physique 3  
tags:  
  - matière  
created: 2023-12-23  
updated: 2024-01-02  
---  
  
  
$V$ change brutalement de valeur  
infini ou fini  
voir aussi [Fonction d'onde de Schrödinger](Fonction%20d'onde%20de%20Schr%C3%B6dinger.md)  
# Puits Infinis  
puit : $[0,L]$ avec $V(x)=\left\{\begin{align} 0 \;&\text{si}\;x \in B\\\infty \;& \end{align}\right.$  
mode $n$ (cas d'onde stationnaire) : $\psi_{n}=\sqrt{ \frac{2}{L} }\sin\left( \frac{n\pi x}{L} \right)\in B$   
Energie propre : $E_{n}=\frac{n^{2}h^{2}}{8mL^{2}}$  
# Puits Finis  
 $B=\left[ -\frac{L}{2}; \frac{L}{2}\right]$ avec $V(x)=\left\{\begin{align} -V_{0} \;&\text{si}\;x \in B\\0 \;& \end{align}\right.$ avec $V_{0}$ le travail de sortie  
  
- si $E>V_{0}$ alors particule indépendante du puit  
  
- solution **symétrique** :  $\psi(x)=\left\{\begin{align} Ae^{\alpha x}\;&\text{si}\;x<L /2\\C\cos(\beta x)\;&\text{si}\; x \in B\\Be^{-\alpha x}\;&\text{si}\;x>L /2 \end{align}\right.$  
	avec $A,B,C,\alpha,\beta$ liés entre eux  
  
- solution **asymétrique** : $\sin$ au lieu de $\cos$  
> [!note] un electron peut quitter le puits sans avoir l'énergie nécéssaire  
# Barrière de potentiel  
barrière : $[0,L]$ avec $U(x)=\left\{\begin{align} U_{0} \;&\text{si}\;x \in B\\0 \;& \end{align}\right.$  
  
- Solution : $\psi(x)=\left\{\begin{align} Ae^{ikx}+B^{-ikx}\;&\text{si}\;x<0\\Ce^{\alpha x}+De^{-\alpha x}\;&\text{si}\;x \in B\\Fe^{ikx}\;&\text{si}\;L<x \end{align}\right.$  
	coeff liés par contraintes de continuité  
	- $Ae^{ikx}$ onde incidente  
	- $B^{-ikx}$ onde réfléchie  
	- $Fe^{ikx}$ onde transmise  
  
- si $E>U_{0}$ : particule quasi libre (barrières fines parfois plus réfléchissantes que les grosses)  
## Effet tunnel avec $E<U_{0}$  
si $F \neq 0$ la particule peut avoir traversé la barrière  
proba rebondisse $R$ , proba traverse $T$ → $T+R=1$  
$$  
T=\frac{4E(U_{0}-E)}{4E(U_{0}-E)+U_{0}^{2}\sinh ^{2}\left( \frac{L}{\hbar}\sqrt{ 2m(U_{0}-E) } \right)}  
$$  
