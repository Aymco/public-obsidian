---  
share: true  
category: Compléments d'Analyse  
tags:  
  - matière  
created: 2024-06-01  
updated: 2024-06-05  
---  
voir [distance, norme, produit scalaire](distance,%20norme,%20produit%20scalaire.md)    
  
- [Algèbre linéaire > Espace vectoriel $X{} subseteq mathbb{R} n$](Alg%C3%A8bre%20lin%C3%A9aire.md#Espace%20vectoriel%20$X{}%20subseteq%20mathbb{R}%20n$)   
les espaces sont des [Ensembles](Ensembles.md)  
# Espace Topologique  
  
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
# Espace métrique  
  
- **Espace métrique** :$(X,d){}$ : Ensemble, distance (aussi espace topologique)  
	- (que 2 cond dist: *pseudo-métrique*)  
	- $X{}$ **Complet** : tt suite de cauchy converge vers $x^*{}$ ($\mathbb{R},\mathbb{C}, l^p, l^\infty,\not \mathbb{Q}{}$)  
		- $\exists i:X\to \overline{ X }{}$ complet : $d(x,y)=\bar{d}(i(x),i(y)){}$ et $\overline{ i(X) }={}\bar{X}{}$  
	- *compact* ⇔ *séquentiellement Compact* ⇔ *Complet* + *séparable*  
	- compact ⇒ fermé  
	- *fermé* ⇔ *séquentiellement fermé*  
	- *connexe* : seuls ouverts+fermé : $\emptyset,X {}$  
	- *connexe par arcs* : $\exists\gamma_{\text{continue}}:\gamma(0)=x, \gamma(1)=y\quad\forall x,y\in X{}$  
	- (espace *convexe* : norme *convexe*)  
	- th. *point fixe* : *complet* + $f{}$ *contractante* ⇒$\exists{}$ unique point fixe:$f(x)=x{}$  
	- th. *valeures extremes* (bornes atteintes): $(X,d){}$ *compact*,$f{}$continue ⇒ min, max  
  
- **Espace Normé** : $(X, | | \cdot| |){}$  espace vectoriel  
	- $X{}$ *séparable* $\iff{}\exists$ famille de $X{}$ totale  
  
- **Espace de Banach** $\mathfrak{B}$ : *Normé* + *Complet* (ex: $\mathbb{R}^n, l^p(\mathbb{N}),l^\infty(\mathbb{N}){}$)  
	- critère de *Weierstrass* : $f{}$ conv ponctuellement ⇒ conv uniformément  
  
- Espace **préhilbertiens** : $(X, \langle \cdot,\cdot \rangle){}$ espace vectoriel  
  
- Espace de **Hilbert** $\mathfrak{H}{}$ : *préhilbertiens* + *Complet*      (⇒ $\mathfrak{B}{}$)   
