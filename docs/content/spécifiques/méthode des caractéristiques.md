---  
created: 2023-10-22  
updated: 2024-01-01  
share: "true"  
---  
  
transformer [[../thematiques/EDP|EDP]] en [[../EDO|EDO]]  
condition initiale : $u(\Gamma(s))=f(s)$ (souvent $\Gamma(s)=(0,s)$)  
# Premier ordre : [[../thematiques/EDP#EDP premier ordre. $Pu_x+Qu_y=R$|EDP > EDP premier ordre. $Pu_x+Qu_y=R$]]  
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
# EDP de transport : [[../thematiques/EDP#EDP de transport $(cu)_{x}+u_{t}= 0$|EDP > EDP de transport $(cu)_{x}+u_{t}= 0$]]  
**Forme conservative** : $\iff\frac{d}{dt}\int_{a}^b u \,dx =0 \iff [cu]_{a}^b = 0$  
- courbe caractéristique : $cdt=du$  
- $d(cu)=0$ : $cu$ est cst le long des caractéristiques (c indépendant de t)  
	- → $u(x,y)=\frac{c(s)}{c(x)}f(s)$  
# Equation onde 1 dimension : [[../thematiques/EDP#Equation d'onde $c {2} nabla {2}u-u_{tt}=0$ - hyperbolique|EDP > Equation d'onde $c {2} nabla {2}u-u_{tt}=0$ - hyperbolique]]  
conditions initiales : $u(\Gamma(s))=f(s)$  et  $u_{n}(\Gamma(s))=g(s)$  
avec $n$ la direction normale de $\Gamma$  
- caractéristiques : $\pm cdt=dx$  
## Triangularisation : trouver $u(x,y)$  
le long des caractéristiques, on a : $c^{2}du_{x}dt-du_{t}dx=0$  
on remplace $\phi=u_{x}$ et $\psi = \frac{u_{t}}{c}$ → $\left\{\begin{align} d(\phi - \psi) = 0 \\ d(\phi + \psi) = 0 \end{align}\right.$  
## Factoriser l'équation  
→ quadrillage horizontal et vertical   $\begin{align} \xi=x-ct \\ \eta=x+ct  \end{align}$  
→ on factorise   
$\frac{ \partial u }{ \partial \xi }=\frac{ \partial u }{ \partial x }-\frac{1}{c}\frac{ \partial u }{ \partial t }$  
au final $\frac{ \partial^{2} u }{ \partial \xi x \partial \eta } = 0$ → donc $u=f_{1}(\xi) + f_{2}(\eta)$  
  
calculer $u_{s}$ via la CI : $u_{s}=u_{t}=-cf_{1}'(s) + cf_{2}'(s)$  
  
> [!check]- solution finale : $u=f(x+ct) - f(x-ct)$   
  
[[./Problème de Helmholtz|Problème de Helmholtz]]  
  
# Méthode générale  
2 direction tel que : $\begin{vmatrix}A & B & C \\dx & dy & 0 \\0 & dx & dy\end{vmatrix}=0$  
- <=> racines de $C\frac{ dx ^2 }{ dy }-B\frac{ dx }{ dy }+A=0$  
	- 2 racines : EDP hyperbolique  
	- 1 racines  : EDP parabolique  
	- 0 racines : EDP elliptique  
- Développer méthode des caractéristiques en partant de 2 points diff (On a remplacé une des colonnes du det par R, du, dv) :    
	- $Adudy1 + Cdvdx1 = Rdy1dx1$  
	- $Adudy2 + Cdvdx2 = Rdy2dx2$