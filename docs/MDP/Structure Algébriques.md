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
	- *Table de Cayley* : représentation matricielle de $*$ entre chaque el  
  
- *Sous structure algébrique* $(B,*)$  $B \subseteq A$ :  $b_{1}*b_{2}, 1_{A}\in B$  
  
- *Inverse* (*unique*) $a$ inverse de $b$ si $a*b=e$  
# Monoïde  
1. Structure algébrique  
2. *associativité* : $a*(b*c) = (a*b)*c$  
3. *neutre* (*unique*) $\exists e: e \in A; \forall a \in A : e*a=a*e=a$  
  
  
- *Sous monoïde* $B$ : $\forall a,b \in \mathbb{R}, a*b \in \mathbb{R}$ 2. neutre $1_A \in B, e_A \in B$  
  
- Théorème : *isomorphisme* $(A,*)$ est isomorphe a un sous monoïde de $(A^A, \circ)$  
  
# Groupe $(G,*)$  
1. definition : Monoïde,  tous ses éléments *possèdent un inverse*  
  
- $a,b,c \in G \Rightarrow  a*c=b*c \Rightarrow a=b$  
  
- $ab=e \iff a^{-1}=b\iff b^{-1}=a$  
  
- $G$ **commutatif** (Abélien) : $a*b=b*a$  
  
- **Sous groupe** $H$ : sous structure, $\forall x \in H, x^{-1} \in H$  
	- $Z_{n}=0,1,\dots, n-1$ addition modulo : isomorphe à $Z/nZ$    
	- sous groupe fini $H$ : sous ensemble fini, non-vide et stable   
  
- *théorème de Lagrange* $G$ fini, $H$ sous groupe ⇒ $|H|=m$ divise $|G|=n$  
## Classe latérale (coset)  
1. de $a\in G$ modulo $H$ : $aH = \{ax|x \in H\}$ ensembles  (*! groupe*)  
  
- nombre limité de classe latérales : $6H = H$  
  
- (*Somme* : $x \in bH, x \in aH <=> b^{-1}*a  \in H$ → $1H + 2H = 3H$)  
  
- partition de $G$ : ensemble des CL distinctes : $1H+2H+\dots=G$  
  
- Théorème *bijection* $f:H\to aH$  avec $f(x)=ax$: $[a]=aH$→ mm nb d'éléments  
  
- **Groupes Quotient** $G /H$ : classes latérales de G mod H : $[a][b]=[ab]$  
## Groupes cycliques  
  
- soit $G$ fini et $g\in G$, sous groupe $\langle g \rangle =\{ g, g^2, g^3, \dots \}$  
  
- $G$ cyclique : $\exists g:\langle g \rangle=G$ (ordre $n$) ($\exists m:g^m=\epsilon$)  
	- ⇒unique sous groupe $H$ ordre $m$ divisant $n$  
  
- *théorème d'Euler-Fermat* : $G$ ordre fini ⇒ $g^n=\epsilon$  
# Anneaux $(A, +, *)$  
1. $(A,+)$ groupe commutatif (neutre : $0_{A}$)  
2. $(A,**)$ un Monoïde (neutre : $1_{A}$)  
3. $*$ se distribue sur $+$ à droite et a gauche :  
  
  
- si $*$ est *commutatif* → Anneau commutatif  
  
- $0_{A}$ est *absorbant*: $a*0_{A}=0_{A}$  
  
- $1_{A}=0_{A}$ → $A=\{ 0 \}$  
  
- *incompatibilité anneau-groupe*:  
	- si $a*0_{A}=0_{A}$ alors  $a*0_{A}=1_{A}$ est impossible  
  
- *Corps* : Anneau : $(A\setminus \{0_{A}  \})$ est groupe (commutatif comme le groupe)  
	- $\mathbb{Z}_{n}$ avec nb premier → corps $(Z_{n}, +\,mod, *\,mod)$  
  
# Applications  
  
- *Logarithme discret* $x=\log_{g}(h)$ avec $g,h\in G$ et $g^x=h$  
	- dans $\mathbb{Z}_{p}^*$ → complexe  
  
- *Protocole de Diffie-Hellman* :  
	- groupe $(Z_{n}, \cdot \mod p)$ avec $p$ un nombre premier car ($a*b\neq 0$)  
	1. clé privée $x,y$  
	2. échange $g^x, g^y$  
	3. peut calculer $g^{x+y}=(g^x)^y$   
  
### Stockage de données : Solomon-Reed  
  
- Anneau polynomial : $A[X]$ : $\forall a \in A,  \sum a_{i}X^i=p(X) \in A[X]$  
  
- $F_{n}$ anneau sous-jacent, $q$ taille alphabet, $k$ nb de mot, $n$ nb de mot enregistrés  
  
- $code :(F_{q})^k\to(F_{q})^n$ (voir devoir)  
