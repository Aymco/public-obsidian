---  
share: true  
category: Compléments d'Analyse  
tags:  
  - matière  
created: 2024-01-05  
updated: 2024-06-01  
title: Ensembles et topologies  
---  
  
- **Boule** ouverte $B_{r}(x)=\{ y\in X:d(x,y)<r \}{}$  
  
- $P(\mathbb{N})=Z^N{}$ ensemble des sous ensembles de $\mathbb{N}{}$ (non dénombrable)  
  
- $\mathbb{R}^n{}$ vecteurs de taille n  
  
- $\mathbb{R}^\mathbb{N}{}=\{ f:\mathbb{N}\to \mathbb{R} \}$ (suites)  
  
- Espace $C(I)=\{ f:I\to \mathbb{R}: f \text{ continue} \}{}$  
  
- *Espaces de Lebesgue* : $L^p(a,b)=\left\{  f: \int_{a}^{b}  \lvert f(x)  \rvert_{p}\, dx<\infty  \right\}{}$  
	- Espace :  $l^{p}(\mathbb{N})=\left\{ l_{i}^p\in \mathbb{R}^\mathbb{N}:| | l_{i}^p| |_{p}<\infty  \right\}{}$   
# Ensembles  
  
- $n$ **cardinal** de $A$ : $n=|A|=\#A \in N$ : taille d'un ensemble  
	- $|\emptyset |<|\{ 0,1 \}|<|\mathbb{N}|<|2^\mathbb{N}|=|\mathbb{R}|<|2^{2^\mathbb{R}}|{}$  
  
- Ensembles **équipotents** $A \approx B \iff |A|=|B|$ si bijection de $A$ vers $B$   
	- $N\approx Z$ : $n\to \left\{\begin{align} \frac{{n+1}}{2}\quad\quad \frac{-n}{2} \end{align}\right.$  
  
- $A$ est *fini* : $A \approx \{ 1,2,..,n \}$ ($A\approx \mathbb{N}$ → *infini*  )  
  
- Ensemble *infini* : jamais en bijection avec l'ensemble de ses parties  
  
- Ensemble **dénombrable** (*énumérable*) : bijection avec les naturels  
	- $\iff |A|=|\mathbb{N}|{}$  (exemples :  $\mathbb{N}, \mathbb{Z}, \mathbb{Q}{}$, paires et n-upplets)  
	- $\subseteq, \cup, \cap, \bigcup_{\infty \text{ enumérable}} {}$ d'E énumérables ⇒ *enumérable*  
		- $\bigcup_{\infty \text{ non-énumérable}}$ d'E énumérables ⇒ ! *énumérable*  
  
- ensemble **total** : span(ss espace vect engendré) est dense dans $X{}$  
  
- *Majorant* $M:\forall x\in U:x\leq M{}$; *minorant* $m:\forall x\in U:x\geq m{}$  
  
- *supremum* $sup(U){}$, *infinimum* $inf(U){}$  
## Exemples d'ensembles  
  
- ensemble de *fonctions* : $A^B{}:=\{ f:B\to A \}$ et $n^X=\{ 0,n-1 \}^X{}$  
  
- ensemble de *vecteurs* : $\mathbb{R}^3=\mathbb{R}\times \mathbb{R}\times \mathbb{R}{}$  
  
- Ensembles numériques :   
	- $\mathbb{N,Z,Q,R,C}{}$  ($R_{0}=R\setminus \{ 0 \}{}$) ($N = \{ 1,2,\dots \}{}$ ; $N_{0}=N\cup \{ 0 \}$)  
	- *intervalle* $I=[a,b]=\{ x\in R,a\leq x\leq b \}{}$  
## Définitions d'ensembles  
  
- Ensemble **étoilé** en $z_{0}$ : $\forall z\in D$ chemin droit $c:z_{0}\to z$, $c\in D$  
	$\mathcal{A}\in \mathbb{C}$ ouvert, étoilé, $f:\mathcal{A}\to \mathbb{C}$ dérivable : $F(z):=\int_{z_{0}}^{z} f(x) \, dw$  
		⇒$F'(z)=f(z)$  
  
- Ensemble **simplement connexe** : connexe et sans trou  
	$\mathcal{A}\in \mathbb{C}$ ouvert, simplement connexe, $f:\mathcal{A}\to \mathbb{C}$ dérivable  
		⇒$F'(z)=f(z)$  
  
- Ensemble **connexe** : E != réunion 2 ensembles fermés disjoints  
  
- Ensemble **connexe par arcs** : tous les points sont reliés de façon continue  
# Opérateurs topologiques :  
  
- **Union** : $A\cup B=\{ x\in X:x \in A \text{ ou } x \in B \}{}$  
	- $|A \cup B|=|A|+|B| - |A \cap B|$  
  
- **disjonction**, **Intersection** :  $A\cup B=\{ x\in X:x \in A \text{ et } x \in B \}{}$  
  
- **Exclusion** :  $A\setminus B=\{ x\in X:x \in A \text{ et } x \not\in B \}{}$  
&nbsp;  
  
- **sous-ensemble** : $A\subseteq X:\forall x \in A,x\in X{}$  
	- **intérieur** : $\underline{A}=A \setminus \partial A{}$  
		- point *intérieur* : $\exists r>0:B_{r}(x)\subseteq A{}$  
	- **Complémentaire** : $A^*=X \setminus A{}$  
	- **frontière** : $\partial A=\{ x \in  X: \forall r > 0:B_{r}(x) \cap A\not=\emptyset \text{ et } \cap A^{*} \not=\emptyset  \}{}$  
	- **Adhérence** : $\bar{A}=A\cup \partial A{}$ (plus petit fermé contenant A)  
	- **extérieur** : $ext(A)=(\bar{A})^*=\underline{(A^*)}{}$  
	- $A{}$ **ouvert** !p frontieres ⇔ tt p intérieurs   
	- **fermé** $X\setminus A{}$ *ouvert* ; $U=\overline{ U }{}$  
  
- **Composition**: $|A\times B|=|A||B|$  
  
- point *limite* : $\forall r>0: \exists y\neq x: y\in B_{r}(x)\cap A{}$  
  
- point *isolé* : $\exists{}$ voisinage de $x:\mathcal{V}(x)\cap A=\emptyset {}$  
	- $\iff x\not\in \overline{ {A\setminus \{ x \}} }{}$  
# Collections : Ensembles d'Ensembles  
  
- **Collection** : ensemble d'ensemble  
  
- **Topologie** $T{}$ : Collection d'ouverts $O\subseteq X{}$ (ex: $\mathcal{P}(X){}$)  
	1. $X,\emptyset \in T{}$  
	2. $\bigcup_{\alpha} O_{\alpha}{}$; 3. $\bigcap_{\alpha<\infty} O_{\alpha}{}$  → ouvert (intersection $\infty{}$ peut être fermé)  
## Espace Topologique  
  
- $(X,T){}$ **Espace Topologique** : ensemble + topologie  
 - $A{}$ **dense** dans $X{}$ : $\overline{ A }=X{}$  ($\mathbb{Q} {}$ dense $\mathbb{R}{}$)  
	- $\forall x\in X, \exists a \in A\subset X:d(a,x)<\epsilon{}$   
 - $V{}\subset X$ **voisinage** de $x\in X{}$ : $\exists U_{\text{ouvert}} \subseteq V{}$  $:x\in U{}$  
  
- $R{}$ **recouvrement** de $Y{}$: Collection : $Y\subseteq\bigcup_{\alpha}R_{\alpha}{}$  
  
- **Séparé** : 2 points distinct → voisinage distinct ~~(!= séparable)~~  
  
- **Compact** : *séparé* + tout recouvrement ouvert de $T{}$ a un nombre fini de sous recouvrements.  
	- 1. $Im A{}$ continue 2. $B\subseteq A{}$ fermé 3. $\bigcup_{finie}{}$ d'un compact ⇒ compact  
	- *théorème de Heine-Borel* : $\mathbb{R}^{n},\mathbb{C}^n:{}$ *compact* <=> *fermé* + *borné*  
  
- **séquentiellement compact** : toute suite → $\exists{}$ sous suite convergente  
  
- Espace *séparable* : $\exists A\subseteq X{}$  *dense* et *dénombrable*  
