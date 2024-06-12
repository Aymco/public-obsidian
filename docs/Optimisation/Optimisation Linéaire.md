---  
share: true  
category: Optimisation  
tags:  
  - matière  
created: 2024-06-08  
updated: 2024-06-12  
---  
## Problème d’ opitmisation linéaire  
  
- probleme de minimisation : $\min c^Tx{}$  
	- $f(x)=c^Tx{}$ fonction objectif  
	- $c^T{}$ vecteur des coefficients  
	- $x{}$ **variables de déscision**  
	- **contraintes** : $Ax\geq=\leq b{}$  
  
- forme **géométrique** : $Ax>b{}$ (pour visualiser)  
  
- forme **standart** : $Ax=b:x\geq 0{}$ (pour résoudre)  
  
- ch de forme :   
  
- terme non linéaire : ($|x|{}$) ⇒ ajoute $t{}$  
## Géométrie des polyèdres  
  
- **Demi-espace** $\{ x:a^Tx\leq b \}{}$  
  
- **hyperplan** : $\{ x: a^Tx=b \}{}$  
  
- **Polyèdre** : $\{ x:a_{i}^Tx\geq b_{i} \}{}$ : $\cap{}$ *demi-espaces*   
	- contrainte **li-indé**: $a_{i}{}$ *li-indé*  
	- contrainte **serrée** , **active** : $a_{i}^Tx=b_{i}{}$  
  
- $\mathcal{P}=\{ x\in \mathbb{R}^n:Ax\geq b \}{}$ (polyèdre)   
	- *solution admissible*$\mathbb{S}_{A}$: $x\in \mathcal{P}{}$ et $\exists n{}$ contraintes li-indé actives  
		- *dégénérée* : contraintes serrées $>n{}$  
		- *adjacentes* : partages $n-1{}$ contraintes li-indé serrées  
  
- **th. fondamental** de l'opti li : $\exists{}$cout *optimal fini* et $\exists{}$*sommets* ⇒ $\exists {}$sommet *optimal*  
	- $\exists{}$sommet ⇔ $\not \exists{}$droite $\in \mathcal{P}{}$  
## Méthode du simplexe  
(forme standart, $n{}$ variables, $m{}$ contraintes $Ax=b{}$ + $n{}$ contraintes $x\geq 0{}$  
  
- soit $m{}$ var. de *base* $x_{B}{}$ et $n-m{}$ var. *hors base* $x_{N}{}$ ($m<n{}$)  
	- $n-m{}$ composantes nulles ($x_{N}{}=0$) → *sommet*  
tableau **simplexe** → peut manipuler les lignes (garder $z{}$ en haut a droite avec coeff 1)  
  
| $c_{B}^T{}$ | $c_{N}^T{}$                | $z$                  |  
| ----------- | -------------------------- | -------------------- |  
| $B{}$       | $N{}$                      | $b{}$                |    
    
→ est **canonique** : $B=I{}$  et $c_{B}^T=0{}$ (⇒ $\tilde{c}=c_{N}^T{}$ *couts réduits*)  
  
- $\exists b_{i}=0{}$ ⇒ sommet *dégénéré*   
  
- sommet *admissible* $b\geq 0{}$, s dual *admissible* $c_{N}{}\geq 0{}$  
  
- *pas dégénéré* ⇔ $x_{B}>0{}$  
  
| $0{}$ | $c_{N}^T-c_{B}^TB^{-1}N{}$ | $z-c_{B}^TB^{-1}b{}$ |  
| ----- | -------------------------- | -------------------- |  
| $I{}$ | $B^{-1}N{}$                | $B^{-1}b{}$          |    
    
(trouver une base $B{}$ : $x_{B}=B^{-1}b\geq 0, x_{N}=0{}$)  
**Pivotage** : répéter :  
1. $c_{N}\geq 0{}$ ⇒ sommet *optimal* FIN  
2. $c_{Ni}{}<0$ et $N_{i}\leq 0{}$ ⇒ solution *non bornée* FIN  
3. choisir $c_{Ni}<0{}$ → rentre dans la base  
	1. $\forall N_{ij}>0{}:q_{j}=\frac{b_{j}}{N_{ij}}{}$  
	2. *pivot* $i:q_{i}=\min q_{j}{}$ → sort de la base  
	3. met à jour le tableau canonique (→ $I{}$ sur nouv. var. de la base)  
## Dualité  
pb de recherche de la *meilleure borne* inférieure valables  
  
- *primal* = dual(dual(primal))  
  
| primal                 | Dual                   |  
| ---------------------- | ---------------------- |  
| min                    | max                    |  
| $a_{i}^Tx=b_{i}{}$     | $y_{i}{}$ libre        |  
| $a_{i}^Tx\geq b_{i}{}$ | $y_{i}\geq 0{}$        |  
| $a_{i}^Tx\leq b_{i}{}$ | $y_{i}\leq 0{}$        |  
| $x_{j}{}$ libre        | $A_{j}^Ty=c_{j}{}$     |  
| $x_{j}\geq 0{}$        | $A_{j}^Ty\leq c_{j}{}$ |  
| $x_{j}\leq 0{}$        | $A_{j}^Ty\geq c_{j}{}$ |    
    
  
- $\min c^Tx:Ax\geq b,x\geq 0\implies$dual: $\max b^Ty:A^Ty\leq c,y\geq 0{}$  
proprietes  
  
- **Dualité faible** : $x{}$, $y{}$ admissiblew : $c^Tx\geq b^Ty{}$  
  
- **Certificat** : solutions : $c^Tx=b^Ty{}$ *optimale*. primal : coût optimal fini ⇔ dual aussi    
	- **Corollaire** : pb non borné ⇒ dual impossible.  
  
- **Dualité forte** : $\exists{}$ sol optimal ⇒ $\exists{}$sol optimale du dual  
  
- *exlusion* : $a_{i}^T{}x\leq b_{i}$ ⇒ $y_{i}∗(a^T_{i} x^*-b_{i} ) = 0{}$  et $x_{i}(A_{i}^Ty_i-c_{i})=0{}$  
**Prediction** :  
  
| var                    | $x^*{}$                        | $y^*{}$                             | base                               | cout optimal $z{}$    |  
| ---------------------- | ------------------------------ | ----------------------------------- | ---------------------------------- | --------------------- |  
| $b+\Delta b{}$         | $x_{B}=B^{-1}(b+\Delta b){}{}$ | =                                   | opti: primal admissible            | $z+y^{*T} \Delta b{}$ |  
| $c+\Delta c{}$         | =                              | $=B^{−1} (c_{B} + \Delta c_{B} ){}$ | opti: dual admissible              | $z+x^{*T} \Delta c{}$ |  
| $c_{k}{}$ et $a_{k}{}$ | =                              | =                                   | opti : $c_{k}-y^{*T}a_{k}\geq 0{}$ | =                     |    
    
## Nombres entiers  
  
- probleme d'opti (mixte) en nombre entiers  
  
- OU : $x_{1}+x_{2}\leq 1{}$; choix d'une contrainte : $a_{i}^Tx-b_{i}\leq My_{i}{}$  
  
- pb *relaxé* : enleve les contraintes entierres  
	- $z_{\text{relaxé}}\geq z{}$  
	- pb impossible ⇒ relaxé impossible  
  
- algo *Branch and Bound* :   
	- soit $z{}$ la borne inférieure, demarre de la relaxation  
	- pt noeuds :  
		- pb imposs ⇒ continue  
		- $z'\leq z{}$ *BOUND* : continue  
		- sol entiere : $z=z'{}$ : continue  
		- sinon *BRANCH* : choisit $x_{i}{}$ → +2 noeuds : $x_{i}\leq ceil(x_{i}){}$ et $x_{i}\geq floor(x_{i}){}$  
	- sol optimal est $z{}$  
&nbsp;  
# Ex  
  
- pb de *flots* : entrees, sorties et capacités entiers ⇒ solution entière  
