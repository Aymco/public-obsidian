---  
share: "true"  
category: Analyse 3  
created: 2023-10-18  
updated: 2024-01-05  
---  
  
[Opérateur différentiels](Op%C3%A9rateur%20diff%C3%A9rentiels.md)  
→ [EDP](EDP.md) : $L(u)=f$  
Linéaire si $L$ linéaire et $f$ connu => combili solution est solution  
  
# Equation aux dérivées partielles  
equation liant u(x, y, …) et $u_x$ ( dérivée partielle)  
chemin : $\Gamma(s)=(x(s),y(s))$  
u sur le chemin := $f(s)$  
  
  
- EDP **homogène** : contient uniquement termes impliquant u et ses dérivées  
  
- EDP **linéaire** : est linéaire par rapport à toutes ses dérivées partielles    
  
- EDP **quasi-linéaire** : est linéaire par rapport aux dérivées partielles de l’ordre le plus élevé  
## Conditions aux limites  
de **Dirichlet** : u               $u(x,0)=f(x)$  
de **Neumann** :  dérivée de u.   $u_y(x,0)=f(x)$  
de **Robin** :  u et dérivée de u.  $l_{0}u_y(x,0)+u(x,0)=f(x)$  
# Types d'EDP  
## EDP premier ordre  
  
- $Pu_x+Qu_y=R$ avec $P, Q, R$ : fonctions de $x, y, u$  
→ [méthode des caractéristiques](m%C3%A9thode%20des%20caract%C3%A9ristiques.md)  
### EDP de transport  
  
- $(cu)_{x}+u_{t}= 0$ avec $c$, fonction de $x$  
→ [méthode des caractéristiques > EDP de transport EDP EDP de transport](m%C3%A9thode%20des%20caract%C3%A9ristiques.md#edp-de-transport-edp-edp-de-transport)  
## EDP seconde ordre  
  
- $Au_{xx}+Bu_{xy}+Cu_{yy}=R$ avec $A, B, C, R$ fonction de $x,y,u$   
**Hyperbolique** $B^{2}-4AC>0$ → [méthode des caractéristiques](m%C3%A9thode%20des%20caract%C3%A9ristiques.md)  
**Parabolique** $B^{2}-4AC=0$ → [méthode de la séparation des variables](m%C3%A9thode%20de%20la%20s%C3%A9paration%20des%20variables.md)  
**Elliptique** $B^{2}-4AC<0$ → [méthode de la séparation des variables](m%C3%A9thode%20de%20la%20s%C3%A9paration%20des%20variables.md)  
## Equation d'onde  
  
- $c^{2}\nabla^{2}u-u_{tt}=0$ - hyperbolique  
→ [méthode des caractéristiques](m%C3%A9thode%20des%20caract%C3%A9ristiques.md)  
## Equation de Laplace  
  
- ${}\nabla^{2}u=0$ - Elliptique  
→ [méthode de la séparation des variables](m%C3%A9thode%20de%20la%20s%C3%A9paration%20des%20variables.md)  
## Equation de diffusion  
  
- ${}\alpha \nabla^{2}u-u_{t}=0$ - Parabolique  
→ [méthode de la séparation des variables](m%C3%A9thode%20de%20la%20s%C3%A9paration%20des%20variables.md)  
  
- *Caractéristiques inutilisables* : dégénérées car parallèles à l’axe des x  
# Résolution  
[méthode des caractéristiques](m%C3%A9thode%20des%20caract%C3%A9ristiques.md)  
[méthode de la séparation des variables](m%C3%A9thode%20de%20la%20s%C3%A9paration%20des%20variables.md)  
