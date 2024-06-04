---  
share: true  
category: Calculabilité  
tags:  
  - regrouping  
title: calculabilité  
created: 2024-02-12  
updated: 2024-06-04  
---  
  
- complémentaire : $\bar{A}=X\setminus A{}$  
  
- **language** : ensemble de mots constitués par $\Sigma$ (tous mots : $\Sigma^*{}$)  
	- *non-trivial* : opérations de base peuvent etre effectuées  
	- **mot** : "abc", "01010", $\epsilon{}$ (vide)  
	- **alphabet** $\Sigma{}$ : ensemble de symboles  
  
- *codage* : $c:T\to \mathbb{N}{}$ bijection d'un nouveau type et les naturels  
  
- **relation** $R{}$ : $aRb,\langle a,b \rangle\in R,R(a,b){}$ ensemble de paires $\langle a,b \rangle{}$  
# Logique propositionnelle  
  
- **proposition** $A{}$  
	- *négation* $!A,\neg A{}$  
	- *conjonction*(et) $A \wedge B{}$  
	- *disjonction*(ou) $A\vee B{}$  
	- *implication* $A\implies B{}$  
	- *équivalence* $A\iff B{}$  
  
- **FNC** : clause et clause et ..  
  
- **intérprétation** : valeurs → propositions  
  
- **modèle**: *interpretation* →VRAI : ($\exists{}$ *modèle* ⇔ form *satisfaisable* ⇔form$\in {}$**SAT**)  
  
- **tautologie** : formule tjrs → VRAI   
	- *conséquence logique* : $p\implies q{}$ *tautologie* ⇔ $p\models q{}$ (affirmation)  
  
- résolution : $A\vee B\text{ et }B!\vee C\implies A\vee C{}$  
  
- (model checking)  
# Problemes informatique  
  
- **programme** $P{}$ avec sa fonction $\varphi(x){}$  
  
- *fonction* : $\varphi:\mathbb{N}\to \mathbb{N}$       ($\varphi(x)=\perp{}$ *indéfinie*)  
	- $\varphi{}$ **totale** : $\forall x:\varphi(x)\neq \perp{}$ sinon *. artielle*  
	- $\varphi_{m}{}$ **extension** de $\varphi_{n}{}$ : $\forall x:\varphi_{n}(x) \neq \perp{}, \varphi_{m}(x)=\varphi_n(x)$  
	- *fonction* **universelle** : $\theta(n,x)=\varphi_{n}(x)$  
	- *fonction* **caractéristique** : $\chi_{A}{}$ determine si $x \in A {}$  
	- $\exists f{}$ partielle calculable : $\not \exists g{}$ : extension de f totale calculable  
## Réduction  
  
- réduction **algorithmique** : $X\leq_{a}Y{}$ : $\exists \chi_{Y}\implies \exists\chi_{X}{}$  (calculabilité)  
	- ⇒ $Y{}$ recursif ⇒ $X{}$ recursif  
	- ⇒$X$ non -recursif ⇒ $Y{}$ non-recursif  
	- $X\leq_{a}\bar{X}{}$   
  
- réduction **fonctionnelle**: $X\leq_{f}Y{}\iff\exists{}f$ totale calculable:  $x\in X \iff f(x)\in Y{}$   
	- complexité : $\mathcal{O}_{A}=\mathcal{O}_{f}+\mathcal{O}_{B}{}$   
  
- réduction **polynomiale** : $X\leq_{p}Y{}$ : fonctionnelle $O(p){}$  
  
- $X\leq_{p}Y\implies X\leq_{f}Y\implies X\leq_{a}Y{}$  
  
- $A_{\text{récursif}}\leq_{a,f} B{}$  
  
- , $A\leq_{a,f}B{}\iff \bar{A}\leq_{a,f}\bar{B}$  
# Modèles de Calculabilité  
  
- **Machine de Turing** : complet  
	- *Ruban* suite de case; *tete* écrit / lit la case; *controle* : dirige  
	- $B{}$ : case vide  
	- **puissance** : nb de f : peut calculer; **efficacité** : vitesse de résolution  
	- *these de Church-Turing* :   
		1. ?? : il n'existe pas de modèle plus puissant  
		2. ?? : f calculable ⇒ T-calculable  
		3. VRAI : tt def de calculabilité équivalentes  
	- *Oracle* : 3 états : $oracle_{ask,ues,no}{}$ : demande si $x\in  A{}$ : oui, non  
  
| machine                  |            puissance            | efficacité |  
| ------------------------ | :-----------------------------: | :--------: |  
| ruban semi-infini        |                =                |     -      |  
| ruban multiple           |                =                |   +(^2)    |  
| plusieures têtes         |                =                |     =      |  
| mouvements élargis       |                =                | +linéaire  |  
| non-déterministe ND(NDT) |                =                |   ++expo   |  
| à oracle                 | =(+ si oracle sur non-récursif) |            |    
    
  
  
- **automate fini** FA : (sous-catégorie des MT → plus simple)  
	- $\Sigma{}$ E fini symboles, $s_{0}\in S{}$ E fini d'états et état initial, $A\subset S{}$ état acceptants, $\delta:S\times \Sigma\to S{}$ f de transition  
	- !mémoire, ensembles pas reconnus ex : $a^nb^n{}$  
	- sortie : son état  
	- automates non déterministe ND (NDFA):  
		- → rendre déterministe  
  
- **automate a Pile - PDA** :  
	- ajoute de memoire : $\Gamma{}$ E fini symboles de pile, $\Delta:S\times\Sigma \times\Gamma\to S\times\Gamma^*{}$  
	- $Z{}$ :pile vide; $A,B / C{}$ :symb ly , somment de la pile / remplacer le somet   
	- $\exists{}$ E recursif  !reconus PDA  
  
- *language de programmation* (svt complets)  
	- ND : =puissance, ++rapide  
  
- *modèle quantique*  
  
- *modèle humain*  
  
- *Fonction récursives*  
  
- *lambda calcul*  
  
- propriétés **modèle complet** :  
	1. **SA** (Solvabilité Algorithmique) : interpréteur de D : calculable  
	2. ⇒ **SD** (Solvabilité des Définitions) : f D-calculable ⇒ calculable  
	3. **CA** (Complétude Algorithmique) : $\forall p \in {}$mod(SA)⇒ $\exists P \in D:\varphi_{P}=\varphi_{p}{}$  
	4. ⇒ **CD** (Complétude des Définitions) : f calculable ⇒ D-caclulable  
	5. **U** (Description Universelle)  : interpréteur de D : D-calculable  
	6. **S** (S-m-n affaiblie) : $\exists{}$P : capable de fixer un argument de P'  
![Pasted image 20240601182520.png](Pasted%20image%2020240601182520.png)  
# Calculabilité  
  
- **problemes** : fonctions : $\{ \varphi:\mathbb{N}\to \mathbb{N} \}{}$ (non-dénombrable)  
	- solutions : dénombrable (⇒ $\exists \varphi{}$ !calculable)  
  
- **algorithme** : ensemble fini d'instruction + calculateur  
	- $\varphi_{m}{}{}$ **calculable** : $\exists P_{n}=\varphi_{m}{}{}$ algo fourni un résultat  
  
- **interpréteur** : $I(n,x)=P_{n}(x){}$ (T-complet ⇒ calculable)  
  
- [Ensembles](Ensembles.md)  
	- ensemble (**ND-**)**récusif** : $\exists{}\varphi$ caractéristique calculable (Non deterministe)  
		- $X_{A}{}$ calculable totale $\iff$recur et corecu enumérable$\iff \bar{A}{}$ recur  
		- $A{}$ fini $\implies A{}$ recursif ⇒ $A{}$ énumérable  
	- ensemble (**ND-**)**récursivement énumérable** : $\varphi(x)=\perp\implies x \in A{}$  
		- $\iff A=domf{} : f$ totale ou partielle calculable  
		- $\iff A=\mathrm{Im}f:f{}$ total calculable  
		- $\iff \bar{A}{}$  **corérucsivement énumérable**  
## Théorème de calculabilité  
  
- **Diagonalisation de Cantor** : tableau infini ($s_{i},s_{i,j}{}$)  
	1. $diag'_{i,i}=diag_{i,j}?0:1{}$ ⇒ $diag'_{i}\neq A_{i} :\forall i{}$  CQFD  
	 - collection de $E_{\infty,\text{énumérable}}{}$ ⇒ !enumérable $\mathbb{R}, \mathcal{P}(\mathbb{N}), f:\mathbb{N}\to \{ 0,1 \}{}$  
  
- th. de **Hoare-Allison** : language $D{}$ (*non-trivial*): $f{}$ totale(⇒ calculable) (ex: **BLOOP** : Java, !boucles)(CA,SA)   
	- $diag(n)=inter(n,n){}$→$d'(n)=diag(n)+1{}$calculable⇒paradoxe(car$\in \mathbb{N}{}$)⇒ interpreteur ! calculable $\not \in D{}$   
		- ⇒ *restrictif*   
		- ⇒ $\exists f$ totale $\not\in D{}$  
	- interpreteur + halt $\not\in D{}$ (non-trivial)  
	- $\forall f{}$ total est calculable dans D ⇒ $\exists f{}$ !totale calculable dans D  
  
- $S_{mn}{}$(**paramétrisation**) : $\exists{}S_{n}^m$*calculable*: $\varphi_{k}(.x_{m+n})=\varphi_{S_{n}^m(... x_{m})}(x_{m+1} ... x_{m+n}){}$  
	- *transformateur de programme* : rentre les arguments→prog (*totale calculable*)  
  
- th. du **point fixe** :$\exists k:\varphi_{k}=\varphi_{f(k)}{}$ avec $P_{k}{}:f$ transformateur *total calculable*  
	1. $h(u,v)=\left\{\begin{aligned} \varphi_{\varphi_{u}(u)}(v) \\ \perp:\varphi_{u}(u)=\perp \end{aligned}\right.{}=\varphi_{S(u)}(v)$ *calculable* ($S_{mn}{}$: totale calculable)  
	3. $g(u)=f(S(u)){}$ *total calculable* ⇒ $\exists r:\varphi _{r} (u) = g(u) = f(S(u)){}$   
	5. ⇒ $h(r, v) = \varphi _{S(r)}(v){}$ et 6. $h(r,v) = \varphi_{\varphi_{r}(r)}(v){} = \varphi _{f(S(r))}(v){}$  
	7. ⇒$\varphi_{S(r)}(v) = \varphi_{f(S(r))}(v){}$ CQFD  
  
- th. de **RICE** : $A\subset \mathbb{N} ,A\neq \emptyset {}$ *recursif* ⇒$\exists i\in A, \exists j \not\in A: \varphi_{i}=\varphi_{j}{}$  
	- corollaire : $\forall i\in A, \forall j\not\in {A}:\varphi_{i}\neq\varphi_{j}{}\implies A\in \{ \emptyset , \mathbb{N} \}{}$ ou $A{}$ *non recursif*  
		1. Démo : $\chi_{A}{}$ : ($\varphi_{k}=\perp{}$, $k\in \bar{A}{}$ ) : $\varphi_{int}\neq \varphi_{ext}{}$  
		2. $halt(n,x):P_{j}(z)=P_{n}(x), P_{m}(z){}$ : $j\in A?\;1,0{}$   
		3. ⇒ $\in A{}$ !calculable ⇒ *non récursif*  
	- propriété *décidable* + *vérifiée* ⇒ $\exists{}$ 2 prog avec et sans propriété : mm f  
	- $\exists P:{}$propriété *vérifiée* ⇒ prop *non-décidable*  
	- $E{}=\{  f: proprité \}$ *récursif* ⇒ $E\subset \{ X,\emptyset  \}{}$   
	- (propriétés liée → fonctions calculées)  
 ![Complexité d'un programme > Complexité d'un programme](Complexit%C3%A9%20d'un%20programme.md#Complexité%20d'un%20programme)  
# Complexité d'un problème  
  
- **N**TIME, **N**… m. *non déterministe* (**D**… déterministe)  
  
- ..**TIME**$(f(n)){}$ : $n\to{}$machine de turing en *temps* $\mathcal{O}(f(n)){}$  
  
- ..**SPACE**$(f(n)){}$ : $n\to{}$machine de turing en *espace* $\mathcal{O}(f(n)){}$   
	- ⇒ $DTIME\subseteq NTIME\subseteq DSPACE\subseteq NSPACE\subseteq DTIME(2^{f(n)}){}$  
  
- **P**.. classe polynomiale : exists algo polynomial (calculable en pratique)  
  
- **NP**.. non-Déterministes polynomiaux ⇒ E\\X **coNP**   
  
- **EXPTIME** = $\mathcal{O}(2^p){}$ avec p un polynome $=\bigcup_{k\in \mathbb{N} }DTIME(2^{n^k}){}$  
  
- **PSPACE** $\mathcal{O}(p){}$ $=\bigcup_{k\in \mathbb{N}}DSPACE(n^k){}$  
  
- **PQB**, **BQP** : classe polynomiale quantique bornée : $\exists{}$ algo Q : raison de ⅔  
&nbsp;  
  
- $p{}$ pb **difficile** : $\forall P \in C{}$ *réductible* a $p{}$   
  
- $p{}$ (T-)**complet** : difficile + $p\in C{}$  
  
- these??  : $P = NP{}$ ($\iff P\subset NP{}$)    
  
- th. de **Cook** : $SAT\in {}$*NP-COMPLET*  ⇒($SAT\in P\implies P=NP{}$)  
	1. $SAT\in {}$*NP* : algo fixe les variables logiques : $\mathcal{O}(n\log n){}$  
	2. *NP-difficile* $\forall B\in NP : B\leq_{p}SAT{}$ : $B{}$ → transforme en porposition  
&nbsp;  
## Exemple de problemes  
  
- pb du voyageur(plus court chemin a travers certains points) : NP-complet  
  
- pb correspondance de *Post* : U,V listes de mots : trouver liste mots identiques   
	- ⇒ non calculable  
### Ensembles  
  
- $halt(n,x)=\left\{\begin{aligned} 1 &:P_{n}(x)\text{ se termine}\\0 \end{aligned}\right.{}$ → *totale*, *non-calculable* :  
	1. $diag(n)=\{ halt(n,n)=0\;?\;\;1,\perp \}{}=P_{d}$   
	2. $diag(d){}$ termine ⇒ =0 ⇒ !termine ⇒ =1 ⇒ paradoxe ⇒ halt !calculable  
  
- $HALT=\{ (n,x):P_{n}(x) \text{ se termine} \}{}$  
  
- $K=\{ n:p_{n}(n)\text{ se termine} \}{}$   
## A voir  
&nbsp;  
