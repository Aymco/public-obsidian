---  
share: true  
category: MDP  
tags:  
  - matière  
created: 2024-01-04  
updated: 2024-01-04  
---  
  
# Structures Algébriques $(A,*)$ ou $(A,T)$  
1. $A$ : un ensemble  
2. $*$ : un opérateur stable     $A*A\to A$  
	- *opérateur stable* : produit de 2 termes dans $A$ est dans $A$  
Exemples : $(\mathbb{R}, x)$, (C, t, x) $(S(A), 0)$   → permuter une liste,  $(P(A), )$    : ensemble des parties de A  
  
- *Sous structure algébrique* $(B,*)$ : $\forall a,b \in B, a*b\in B$  
# Monoïde  
1. Structure algébrique  
2. *associativité* : $a*(b*c) = (a*b)*c$  
3. *neutre* $\exists e: e \in A; \forall a \in A : e*a=a*e=a$  
Exemple : $(A^A, \circ)$ l'ensemble des fonction de $A\to A$ et $\circ$ l'opérateur composition  
  
- Théorème 1 : *neutre unique* $\exists ! e \in A, \forall a \in A : e*a=a*e=a$  
# Sous monoïde $B$  
  
- Définition :   
	1. $\forall a,b \in \mathbb{R}, a*b \in \mathbb{R}$  
	2. neutre $1_A \in B, e_A \in B$  
  
- Théorème : *isomorphisme* $(A,*)$ est isomorphe a un sous monoïde de $(A^A, \circ)$  
  
- définition : *Inverse* : $a$ inverse de $b$ si $a*b=b*a=e$  
	- Théorème : *inverse unique* : si $\exists a, b \in A, a*b=e$, alors $a$ est unique  
# Groupe $(G,*)$  
1. definition : Monoïde, tous ses éléments *possèdent un inverse*  
  
- $a,b,c \in G \Rightarrow  a*c=b*c \Rightarrow a=b$  
  
- $ab=e \iff a^{-1}=b\iff b^{-1}=a$  
  
- $G$ **commutatif** / **Abélien** : $a*b=b*a$  
## Sous groupe $H$  
1. $\forall x,y \in H, x*y \in H$  
2. $1_G \in H$  
3. $\forall x \in H, x^{-1} \in H$  
## Groupes cycliques  
1. sous-groupe engendré  
  
- loi : puissance : $a^n=\underbrace{ a*a*\dots }_{ n }$ ⇒ $<g> =\{ g, g^2, g^3, \dots \}$  
  
- Structure algébrique  
# Classe latérale (CL) ( coset) de $a$ modulo $H$  
1. $a\in G,   aH = \{ax|x \in H\}$  
  
- $1H, 2H, ..$ : ensembles  (*! groupe* : pas de neutre)  
  
- nombre limité de classe latérales : $6H = H$  
  
  
- *Somme* : $x \in bH, x \in aH <=> b^{-1}*a  \in H$  
	- $1H + 2H = 3H$  
  
- $1H+2H+\dots=G$  
  
- Théorème *bijection* entre $H$ et $aH$ → mm nb d'éléments  
# Anneaux $(A, +, *)$  
1. $(A,+)$ est commutatif (neutre : $0_{A}$)  
2. $(A,**)$ un Monoïde (neutre : $1_{A}$)  
3. $*$ se distribue sur $+$ à droite et a gauche :  
	- droite  $x*(y+z)=x*y+x*z$  
	- gauche $(y+z)*x=y*x+z*x$  
4. si $*$ est *commutatif* → Anneau commutatif  
  
- $0_{A}$ est *absorbant*: $a*0_{A}=0_{A}$  
  
- $1_{A}=0_{A}$ → $A=\{ 0 \}$  
  
- *incompatibilité anneau-groupe*:  
	- si $a*0_{A}=0_{A}$ alors  $a*0_{A}=1_{A}$ est impossible  
## Corps  
  
- $(A\setminus \{0_{A}  \})$ est un groupe  
  
- corps premiers : $(Z_{n}, +\mod, *\mod)$  
# Applications  
### Encodage  
groupe $(Z_{n}, \cdot \mod p)$ avec $p$ un nombre premier car ($a*b\neq 0$)  
  
→ groupe $<g>$ : facile a calculer $g^x$ mais $\log g^x$ compliqué  
→ $g^x*g^y=g^{x+y}$  
  
Protocole de Diffie-Hellman :  
1. clé privée $x,y$  
2. on envoie $g^x$  
3. peut calculer $g^{x+y}$   
attaque man in the middle  
### Stockage de données : Solomon-Reed  
Anneau polynomial : $A[X]$ : $\forall a \in A,  \sum a_{i}X^i=p(X) \in A[X]$  
$F_{n}$ anneau sous-jacent, $q$ taille alphabet, $k$ nb de mot, $n$ nb de mot enregistrés  
$code :(F_{q})^k\to(F_{q})^n$  
