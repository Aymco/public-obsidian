---  
share: true  
category: Calculabilité  
tags:  
  - regrouping  
title: calculabilité  
created: 2024-02-12  
updated: 2024-06-03  
---  
classifier problème :  calculable, non calculable (en pratique)  
complémentaire : $\bar{A}=X\setminus A{}$  
# Logique propositionnelle  
  
- *proposition* $A{}$  
	- *négation* $!A{}$  
	- *conjonction*(et) $A \wedge B{}$  
	- *disjonction*(ou) $A\vee B{}$  
	- *implication* $A\implies B{}$  
	- *équivalence* $A\iff B{}$  
  
- *FNC* : clause et clause et ..  
  
- *intérprétation* : valeurs → propositions  
	- *modèle*: interpretation →VRAI : ($\exists{}$ modèle → *satisfaisable* (modèle $\in {}$ SAT : E)  
  
- *tautologie* : formule tjrs → VRAI   
	- *conséquence logique* : $p\implies q{}$ tautologie ⇒ $p\models q{}$  
  
- résolution :$A\vee B\text{ et }B!\vee C\implies A\vee C{}$  
	- (model checking)  
# Problemes informatique  
  
- fonction a trouver $\varphi(x){}$ ; avec programme $P{}$; $\varphi(x)=\perp{}$ *indéfinie*  
  
- *fonction* : $\varphi:\mathbb{N}\to \mathbb{N}$  
	- $\varphi{}$ *totale* : $\forall x:\varphi(x)\neq \perp{}$ sinon *partielle*  
	- $\varphi_{m}{}$ *extension* de $\varphi_{n}{}$ : $\forall x:\varphi_{n}(x) \neq \perp{}, \varphi_{m}(x)=\varphi_n(x)$  
	- *fonction universelle* : $\theta(n,x)=\varphi_{n}(x)$  
	- *fonction caracteristique* : $X_{A}{}$ determine si $x \in A {}$  
	- $\exists f{}$ partielle calculable : $\not \exists g{}$ : extension de f totale calculable  
  
- *réduction*  
	- $\chi_{A}{}$ fonction caractéristique (définit si $x\in  A{}$ )   
	- réduction *algorithmique* : $X\leq_{a}Y{}$ : $\exists \chi_{Y}\implies \exists\chi_{X}{}$  (calculabilité)  
		- ⇒ $Y{}$ recursif ⇒ $X{}$ recursif  
		- ⇒$X$ non -recursif ⇒ $Y{}$ non-recursif  
		- $X\leq_{a}\bar{X}{}$   
	- réduction *fonctionnelle*: $X\leq_{f}Y{}\iff\exists{}f$ totale calculable:  $x\in X \iff f(x)\in Y{}$   
		- complexité : $\mathcal{O}_{A}=\mathcal{O}_{f}+\mathcal{O}_{B}{}$   
	- réduction *polynomiale* : $X\leq_{p}Y{}$ : fonctionnelle $O(p){}$  
	- $X\leq_{p}Y\implies X\leq_{f}Y\implies X\leq_{a}Y{}$  
	- $A_{\text{récursif}}\leq_{a,f} B{}$  
	- , $A\leq_{a,f}B{}\iff \bar{A}\leq_{a,f}\bar{B}$  
## Definitions  
  
- *language* : ensemble de mots constitués par $\sum$ (tous mots : $\sum^*{}$)  
	- *mot* : "abc", "01010", $\epsilon{}$ (vide)  
	- *alphabet* $\sum{}$ : ensemble de symboles  
  
- *relation* $R{}$ : $aRb,\langle a,b \rangle\in R,R(a,b){}$ ensemble de paires $\langle a,b \rangle{}$  
# Modèles de Calculabilité  
  
- *Machine de Turing* : complet  
	- *Ruban* suite de case; *tete* écrit / lit la case; *controle* : dirige  
	- $B{}$ : case vide  
	- *puissance* : nb de f : peut calculer; *efficacité* : vitesse de résolution  
	- these de Church-Turing :   
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
    
  
  
- *T-calculable* : $\exists MT: \forall x → f(x){}$  
  
- *T-récursif* , *T-récursivement énumérable* : $\exists MT{}$ ⇒ calculable, récursif, récur. énum  
  
- *automate fini* FA : (sous-catégorie des MT → plus simple)  
	- $\sum{}$ E fini symboles, $s_{0}\in S{}$ E fini d'états et état initial, $A\subset S{}$ état acceptants, $\delta:S\times \sum\to S{}$ f de transition  
	- pas de mémoire, ensemble pas reconnus ex : $a^nb^n{}$  
	- sortie : son état  
	- automates non déterministe ND (NDFA):  
		- → rendre déterministe  
  
- *language de programmation* :   
	- svt complets (=T-complets)  
	- ND : =puissance, ++rapide  
  
- *modèle quantique*  
  
- *modèle humain*  
  
- *automate a Pile* PDA :  
	- ajoute de memoire : $\Gamma{}$ E fini symboles de pile, $\Delta:S\times\sum \times\Gamma\to S\times\Gamma^*{}$  
	- $Z{}$ :pile vide; $A,B / C{}$ :symb ly , somment de la pile / remplacer le somet   
	- $\exists{}$ E recursif  !reconus PDA  
  
- *Fonction récursives*  
  
- *lambda calcul*  
&nbsp;  
  
- propriétés modèle complet :  
	1. *SD* (Solvabilité des Définitions) : f D-calculable ⇒ calculable  
	2. *CD* (Complétude des Définitions) : f calculable ⇒ D-caclulable  
	3. *SA* (Solvabilité Algorithmique) : interpréteur de D : calculable  
	4. *CA* (Complétude Algorithmique) : traduire P(SA) → D  
	5. *U* (Description Universelle)  : interpréteur de D : D-calculable  
	6. *S* (S-m-n affaiblie) : $\exists{}$P : capable de fixer un argument de P'  
![Pasted image 20240601182520.png](Pasted%20image%2020240601182520.png)  
# Calculabilité  
  
- *problemes* : fonctions : $\{ \varphi:\mathbb{N}\to \mathbb{N} \}{}$ (non-dénombrable)  
	- solutions : dénombrable  
	- ⇒ $\exists \varphi{}$ !calculable  
  
- $\varphi_{m}{}$ *calculable* : $\exists n:P_{n}(x)=\varphi_{m}(x){} \quad \forall x$  
&nbsp;  
  
- *ND-programme* : choose(n)  
  
- *ND-récursif* : $\exists{}$ ND-programme : $\{ x \not\in A : 0  ;x\in A:1\cup\dots\}{}$  
  
- *ND-récursivement énumérale* : $\exists{}$ ND-programme : $\{ x \not\in A : \neq 1 \cup \perp  ;x\in A:1\cup\dots\}{}$ ⇔recur enum  
&nbsp;  
exemple :   
  
- $halt(n,x)=\left\{\begin{aligned} 1 &:P_{n}(x)\text{ se termine}\\0 \end{aligned}\right.{}$ → f totale, non-calculable  
  
- $HALT=\{ (n,x):P_{n}(x) \text{ se termine} \}{}$ E: prog se terminent  
  
- $K=\{ n:p_{n}(n)\text{ se termine} \}{}$   
&nbsp;  
&nbsp;  
  
- *algorithme* : ensemble fini d'instruction + calculateur  
	- $f{}$ *calculable* : algo fourni un résultat  
  
- *interpréteur* : $I(n,x)=P_{n}(x){}$ (T-complet ⇒ calculable)  
  
- [Ensembles](Ensembles.md)  
	- ensemble *récusif* : $\exists{}\varphi$ caractéristique calculable  
		- $\iff{}$ ND-récursif (via $\varphi{}$ ND)  
		- $X_{A}{}$ calculable totale $\iff$recur et corecu enumérable$\iff \bar{A}{}$ recur  
		- $A{}$ fini $\implies A{}$ recursif ⇒ $A{}$ énumérable  
	- ensemble *récursivement énumérable* : $\varphi(x)=\perp\implies x \in A{}$  
		- $\iff A=domf{} : f$ totale ou partielle calculable  
		- $\iff A=\mathrm{Im}f:f{}$ total calculable  
		- $\iff \bar{A}{}$  *corérucsivement énumérable*  
&nbsp;  
  
- language **BLOOP** (Bounded loop) : Java, !boucles  
	- ! while, for (var i modifiée) !goto ! f récursives ⇒ totale calculable  
## Théorème de calculabilité  
  
- *Hoare-Allison*  
	- language que des fonction totales: !$I{}$ ⇒ *restrictif* (pas toutes calculables)  
		- interpreteur language != et E f totales non programmables  
	- interpreteur et halt peuvent pas etre dans un meme language  
	- language tt fonction : permettre fonctions non totales  
	- E f totales est pas récusif  
  
- $S_{mn}{}$(*paramétrisation*) : $\exists{}S_{n}^m$ calculable: $\varphi_{k}(.x_{m+n})=\varphi_{S_{n}^m(... x_{m})}(x_{m+1} ... x_{m+n}){}$  
	- transformateur de programme : rentre les argumentss dans un prog  
  
- th. du *point fixe* :$\exists k:\varphi_{k}=\varphi_{f(k)}{}$ avec $P_{k}{}:f$ transformateur  
	- ? : s transfo total calculable : $\exists P_{1},P_{2}:f(P_{1})=P_{2}{};P_{1},P_{2}$ calculent la meme f  
  
- théorème de *RICE* : $A\subset \mathbb{N} ,A\neq \emptyset {}$ recursif ⇒$\exists i\in A, \exists j \not\in A: \varphi_{i}=\varphi_{j}{}$  
	- corollaire : $\forall i\in A, \forall j\not\in {A}:\varphi_{i}\neq\varphi_{j}{}\implies A\in \{ \emptyset , \mathbb{N} \}{}$ ou $A{}$ non recursif  
	- propriété décidable + vérifiée ⇒ $\exists{}$ 2 prog avec et sans propriété : mm f  
	- propriété vérifiée ds certain prog ⇒ non-décidable  
	- $\exists P{}$ determine proprité f ⇒ toute ou aucune f a la propriété  
	- (seulement pour fonctions calculées) (prop liée a la fonction (!programme)  
## Diagonalisation de Cantor  
ensemble d'ensembles infini enumérable ⇒ !enumérable $\mathbb{R}, \mathcal{P}(\mathbb{N}), f:\mathbb{N}\to \{ 0,1 \}{}$  
1. tableau(nombre d'ensembles, elements de l'ensemble)  
2. $diag'_{i,i}=diag_{i,j}?0:1{}$  
	1. ⇒ $diag'_{i}\neq A_{i} :\forall i{}$  CQFD  
&nbsp;  
  
- pb correspondance de *Post* : U,V listes de mots : trouver liste mots identiques   
	- ⇒ non calculable  
  
- *codage* : $c:T\to \mathbb{N}{}$ bijection d'un nouveau type et les naturels  
  
- nombres calculables …  
&nbsp;  
# Complexité d'un programme  
 ![Complexité d'un programme](Complexit%C3%A9%20d'un%20programme.md)  
# Complexité d'un problème  
  
- *EXPTIME* = $\mathcal{O}(2^p){}$ avec p un polynome $=\bigcup_{k\in \mathbb{N} }DTIME(2^{n^k}){}$  
  
- *PSPACE* $\mathcal{O}(p){}$ $=\bigcup_{k\in \mathbb{N}}DSPACE(n^k){}$  
  
- *NP* pro. lemes polynomiaux non-Déterministes  
	- ⇒ E\\X *coNP*   
  
- *P* classe polynomiale : exists algo polynomial (calculable en pratique)  
  
- *PQB*, *BQP* : classe polynomiale quantique bornée : $\exists{}$ algo Q : raison de ⅔  
&nbsp;  
  
- these : $P \subset NP{}$ ($\iff P=NP{}$)  
  
- $p{}$ probleme *difficile* : $\forall P \in C{}$ *réductible* a $p{}$   
  
- *complet* : difficile + $p\in C{}$  
  
- th. de *Cook* : SAT → NP-complet …  
	1. $SAT\in NP{}$  
	2. NP-difficile via $\ll_{p}{}$  
  
- $DTIME(f(n)){}$ : $n\to{}$machine de turing en temps $\mathcal{O}(f(n)){}$  
  
- $DSPACE(f(n)){}$ : $n\to{}$machine de turing en espace $\mathcal{O}(f(n)){}$  
$DTIME\subseteq NTIME\subseteq DSPACE\subseteq NSPACE{}$  
  
- NTIME(f), NSPACE(f) machine non déterministe  
&nbsp;  
&nbsp;  
&nbsp;  
Exemple de problemes  
  
- pb du voyageur(plus court chemin a travers certains points) : NP-complet  
