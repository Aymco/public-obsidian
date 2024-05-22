---  
share: true  
category: Analyse 3  
created: 2023-10-22  
updated: 2024-02-12  
title: méthode des caractéristiques  
---  
# Méthode des caractéristiques  
transformer [EDP](EDP.md) en [EDO](EDO.md)  
condition initiale : $u(\Gamma(s))=f(s)$ (souvent $\Gamma(s)=(0,s)$)  
# Premier ordre : [EDP > EDP premier ordre](EDP.md#EDP%20premier%20ordre)  
## Verification du problème de Cauchy  
dérivée directionnelle :$\frac{du}{ds}=u_{x} \frac{dx}{ds}+u_{y} \frac{dy}{ds}$  
## Trouver les courbes caractéristiques :  
$\begin{vmatrix}P &Q\\\frac{dx}{ds} & \frac{dy}{ds}\end{vmatrix}=0$ → $Pdy=Qdx$ et on intègre sur $[\Gamma ; (x,y)]$  
  
- n'intersecte qu'une seule fois $\Gamma$  
  
- $R=0$ → $u$ est conservée le long des caractéristiques  
## Trouver l'EDO  
**Relations caractéristiques** : (vérifiées le long de chaque caractéristique)  
$Pdu=Rdx$ et $Qdu=Rdy$  
pseudo équation :  $\frac{P}{dx}=\frac{Q}{dy}=\frac{R}{du}$  (pour retenir)  
# EDP de transport : [EDP > EDP de transport](EDP.md#EDP%20de%20transport)  
**Forme conservative** : $\iff\frac{d}{dt}\int_{a}^b u \,dx =0 \iff [cu]_{a}^b = 0$  
  
- courbe caractéristique : $cdt=du$  
  
- $d(cu)=0$ : $cu$ est cst le long des caractéristiques (c indépendant de t)  
	- ⇒ $u(x,y)=\frac{c(s)}{c(x)}f(s)$  
# Equation onde 1 dimension : [EDP > Equation d'onde](EDP.md#Equation%20d'onde)  
  
- On a $u=c\frac{ \partial \phi }{ \partial x }$ et $v=\frac{ \partial \psi }{ \partial t }$  
  
- caractéristiques : $\pm cdt=dx$ ⇒ : $c^{2}du_{x}dt-du_{t}dx=0$  
  
- $c$ constant ⇒ $s=x\pm ct$  
  
- *Invariants de RIemann* : $u\pm v$ cst sur caracteristiques  
  
- *Factorisation* : $\left( c \frac{ \partial  }{ \partial x }-\frac{ \partial  }{ \partial t } \right)\left( c \frac{ \partial  }{ \partial x }+\frac{ \partial  }{ \partial t } \right)\phi=0$  
  
- ch de variable : $\begin{align} \xi=x-ct \\ \eta=x+ct  \end{align}$ ⇒ $\frac{ \partial^{2} \phi }{ \partial \xi \partial \eta }=0$  
⇒ $\phi=f_{1}(\xi) + f_{2}(\eta)$  
> [!check]- solution finale : $u=f(x+ct) - f(x-ct)$   
  
calculer $u_{s}$ via la CI : $u_{s}=u_{t}=-cf_{1}'(s) + cf_{2}'(s)$  
[Problème de Helmholtz](Probl%C3%A8me%20de%20Helmholtz.md)  
# Méthode générale  
2 direction tel que : $\begin{vmatrix}A & B & C \\dx & dy & 0 \\0 & dx & dy\end{vmatrix}=0$  
  
- <=> racines de $C\frac{ dx ^2 }{ dy }-B\frac{ dx }{ dy }+A=0$  
	- 2 racines : EDP hyperbolique  
	- 1 racines  : EDP parabolique  
	- 0 racines : EDP elliptique  
  
- Développer méthode des caractéristiques en partant de 2 points diff (On a remplacé une des colonnes du det par R, du, dv) :    
	- $Adudy1 + Cdvdx1 = Rdy1dx1$  
	- $Adudy2 + Cdvdx2 = Rdy2dx2$  
