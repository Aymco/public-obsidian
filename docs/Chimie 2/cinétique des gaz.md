---  
share: true  
category: Chimie 2  
created: 2023-10-23  
updated: 2024-01-06  
tags:  
  - matière  
title: cinétique des gaz  
---  
  
[notations chimie](notations%20chimie.md)  
théorie cinétique des gaz  
# Théorie de Bernoulli - gaz  
  
- molécules : sphère (diamètre $d$, masse $m$)  
  
- $d\ll\lambda\ll L$  
  
- mouvements indépendant des autre mol  
  
- $E_{c}$ constante (mécanique classique)  
  
- parois n'absorbent pas d'énergie  
  
  
- molécules triées par vitesse (? position)  
## Propriétés  
  
- **pression** $p=\frac{1}{3}\rho\overline{c^2}$ (choc des molécules sur les parois $\frac{\sum F}{A}$)  
  
- **Température** : $\bar{k}=\frac{3}{2}k_{B}T$  
  
- **Énergie interne** - énergie cinétique : $U=\frac{3}{2}nRT$  
  
- **libre Parcours moyen** : $\lambda=\frac{RT}{4\sqrt{ 2 }r^{2}\pi pN_{A}}=\frac{\bar{c}}{z}$ ($z$:choc/sec)  
	- distance moyenne parcourue par une mol avant d'en rencontrer une autre  
  
- **Effusion** :  $\frac{dN}{dt}=\frac{pAN_{A}}{\sqrt{ RT_{2}\pi M_{m} }}$ gaz qui traverse une paroi poreuse ($N$ mol)  
	- → pression : $p(t)=p_{0}e^{ -At/V \sqrt{ \frac{RT}{2\pi M_{m}} }}$  
  
- *Distribution de Maxwell-Boltzmann*  
	- $c_{p}=\sqrt{ \frac{2RT}{M_{m}} }$    **vitesse la plus probable**  
	- $\bar{c}=\sqrt{ \frac{4}{\pi} }c_{p}$       **vitesse moyenne**  
	- $\bar{c^2}=\frac{3}{2}c_{p}$           **vitesse quadratique moyenne**  
  
- Distribution de Maxwell : milieu gazeux homogène (!position), isotrope (!direction)  
	- $\phi_{i}(x)$ = probabilité d’avoir vitesse $C_{i}$ inférieure à $x$  
  
# Limites de validité  
  
- **Facteur de compression** : $Z=\frac{pV_{m}}{RT}$ ([gaz parfait](gaz%20parfait.md) ⇒$Z=1$)  
![Pasted image 20231101185536.png](Pasted%20image%2020231101185536.png)  
**température de Boyle** : température ou le gaz agit comme un gaz parfait $p\ll$   
équation de Van der Waals : $(p+AV^{-2}_{m})(V_{m}-b)=RT$  
  
# Démo : Pression $p$  
on cherche la pression d'un gaz  $p = \frac{F}{s}$  
  
  
$$  
\begin{aligned}  
F_{T}&=\sum \frac{1}{t}\int_{0}^{t} F_{i} \, dt &\text{force à un moment t}   
\end{aligned}  
  
  
$$  
or on sait que  
  
  
$$  
\int_{0}^{t} F_{i} \, dt = 2m_{iCi,x}   \hspace{50px}\text{car  } F = ma =m \cdot vdt  
  
  
$$  
Donc  
  
  
$$  
\begin{aligned}  
F_{T}&=\sum \frac{2}{t}m_{i}c_{i,x} &\text{on remplace}    
\end{aligned}  
  
  
$$  
soit un cube de longueur $L$ et   
  
  
$$  
\begin{aligned}  
p  & = \frac{F_{T}}{s} = \frac{F_{T}}{L^{2}}  = \frac{\rho L F_{T}}{mn} &\text{densité : } \rho=\frac{nm}{V} \\  
 & =  \frac{\rho}{mn}  \sum \underbrace{ \frac{2L}{t} }_{ c_{x} }m_{i}c_{i,x} & c_{x} = \frac{2L}{dt}\\   
& =  \frac{\rho }{n}  \sum c_{i,x}^{2} \\  
& = \rho  \cancel{ \frac{n }{n} }  \overline{c_{x}^{2}}  &\text{avec }\overline{c_{x}^{2}} \text{ la moyenne des vitesses}  \\  
& = \frac{\rho \overline{c^{2}}}{3}   & \text{car } \overline{c^{2}} = \frac{\overline{c_{x}^{2}}}{3}\\   
\end{aligned}  
  
  
$$  
  
on a donc la **pression** $p=\frac{1}{3}\rho\overline{c^2}$  
