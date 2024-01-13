---  
created: 2023-10-09  
updated: 2024-01-02  
share: true  
category: Physique 3  
title: ondes électro-magnétiques  
---  
  
![equations de Maxwell > Equations de maxwell](equations%20de%20Maxwell.md#equations-de-maxwell)  
  
# Equation d'ondes électromagnétiques  
## Cas $\vec{E}\perp \vec{H}$  
ondes transverses $\vec{E},\vec{B}$ avec $\vec{E}\perp \vec{B}$,   
**équation de propagation** (avec lois de Lenz Faraday) :  
$\frac{ \partial E_{y} }{ \partial x }=-\mu_{0}\frac{ \partial H_{z} }{ \partial t }$  
$\frac{ \partial H_{z} }{ \partial x }=-\epsilon_{0}\frac{ \partial E_{y} }{ \partial t }$  
**équation d'onde** : $\frac{ \partial^{2} }{ \partial t^{2} }E_{y}=c^{2}\frac{ \partial^{2}  }{ \partial x^{2} }E_{y}$ (pareil pour $H_{z}$)  
  
- ⇒ Solutions : $f(x,t)=f(x-vt)$ déplacement sur l'axe des x  
! prop de terme cst : $A(x - vt) = Z \cdot B(x - vt)= −Z · B(x + vt)$  
  
- superposition 2 ondes progr sens opposé ⇒ $0$  
## Cas $\vec{E} \not\perp \vec{H}$  
principe de **superposition des ondes** → résultat au dessus s'applique  
# Particularités  
$A=H_{z} \quad\qquad a=\epsilon_{0}$  
$B=E_{y} \quad \qquad b=\frac{1}{\mu_{0}}$  
  
  
- Vitesse de la lumière : $c=v=\sqrt{ \frac{b}{a} }=\sqrt{ \frac{1}{\mu_{0}\epsilon_{0}} }=2,9975\cdot 10^8$  
  
- *densité d'énergie* : $u=u_{E}+u_{M}=\epsilon E^{2}\;J/m^3$  
	- densité d'énergie Electrique : $u_{E}=\frac{\epsilon E^{2}}{2}=[J/m^3]$  
	- densité d'énergie Magnétique : $u_{M}=\frac{ B^{2}}{2\mu}=\frac{\epsilon E^{2}}{2}[J/m^3]$   
  
- *Intensité* d'une onde électromagnétique : $I:=cu=c\epsilon E^{2}=[W /m^{2}]$  
	- onde sinusoidale ⇒ $I_{\text{moyenne}}=\frac{\epsilon cE^{2}_{max}}{2}$  
  
- *Vecteur de Poynting* $\vec{S}=\vec{E}\times \vec{H}$ : direction propagation, norme : $I$  
  
- [Antennes - rayonnements](Antennes%20-%20rayonnements.md)  
