---  
share: true  
category: Concepts, Paradigmes  
tags:  
  - matière  
created: 2024-05-27  
updated: 2024-06-13  
---  
# Programmation symbolique  
&nbsp;  
  
- **Clause**  liste avec head, tail : `[] H|T`  
  
- **Arbres** :  `<tree T> : := leaf | t(T <tree T> ... <tree T>)`  
	- *Binary* : 2 sous arbres; *ordered* : triée, *balanced* $O(\log n)$  
	- **Lookup** K T : trouve un valeur  
	- **Insert** K W T : peut remplacer une feuille, un noeuds, sous noeuds  
	- **Delete** K T : delete feuille, sous noeuds  
  
- **Liste** `<List T> ::= nil | T ’|’ <List T>`  
	- `List2 = [1 2] = 1 | 2 | nil = (1:1 2:(1:2 2:nil))`  
  
- **Tupple** : `X = state(1 b 2)`, {Label X}, {Width X}  
  
- **procédures** :   
	- def : cree l'env, stocke son code et ses variables  
	- appel : cree nouvel environnement : contextuel (exterieur) + var formelles  
  
- **environnement contextuel**: $E_{c}=\{Z\to z\}{}$  
## Language Kernel  
  
- 1 opération par ligne  
  
- déclaration en locale de toutes les variables.  
  
- *procédures anonymes  
  
- ! fonction inbriquées. (nested)  
  
- **Records** : `state(a:1 2:a b:2)`→ *1 structure de données*  
	- tupple = record  1 - X  
	- liste = record (1:H 2:T)  
	- **atom** record de taille 0  
# Sémantique  
La sémantique d’un language de programmation est l’explication complète de comment celui-ci s’exécute.  
## Language Noyeau (kernel)  
  
- afficher tous les résultats intermédiaires  
  
- fonction → procédure  
```oz  
<s> ::= skip  
| <s>1<s>2  <br>\| local <x> in <s> end|  
| <x>1=<x>2 \| <x>=<v>|  
| if <x> then <s>1 else <s>2 end \| {<x> <y>1,...,<y>n}|  
| case <x> of <p> then <s>1 else <s>2 end|  
<v> ::= <number > \| <procedure > \| <record >   
<number > ::= <int > \| <float >|  
<procedure> ::= proc {$ < x >1,...,< x >n} <s> end  
<record>, <p> ::= <lit> \| <lit>(< f >1:< x >1,...,< f >n:< x >n)|  
```  
  
| type     | oz                     | L. Noyeau                                |  
| -------- | ---------------------- | ---------------------------------------- |  
| fonction | `{oz}fun{Length Xs N}` | `{oz}proc{Length Xs N ?R}`               |  
| Browse   | `{oz}{Browse 10}`      | `{oz}local N in N=10 {Browse N} end`<br> |    
    
## Environnement de la mémoire  
  
- **Environnemnt** $E=\{ X\to x, Y\to y \}{}$  
	- $X,Y{}$ *identifiers* (identificateurs) : valeur dans le programme  
	- $x,y{}$ variables : stocke la valeur  
  
- **mémoire** $\sigma=\{ x=4, y \}{}$  
  
- **environnement contextuel** $E_{c}=\{ A\to a \}{}$ contient   
	- *identificateur libres* : declaré a l'exterieur de l'execution  
  
- valeur proc : (`{oz}proc{$ X Y} Y=X+A end`, $\{ A\to a \}{}$)  
## Machine abstraite  
→ détailler l’exécution sur papier d’un code  
  
- *instruction sémantique* $(\langle s \rangle,E){}$ : instruction noyeau + environnement  
  
- *Pile sémantique* $ST=[(\langle s \rangle,E),\dots,(\langle s \rangle,E)]{}$  
## Execution  
1. $(\langle S_{T} \rangle,E=\emptyset ),\sigma=\emptyset {}$ (env, mem vide )  
2. developper instruction par instruction  
	- declaration de var : ⇒ $(⟨s_{i+1}⟩,E_{i} \cup \{ X\to x \} ),\sigma_{i} \cup \{ x \}{}$  
	- assignation ⇒ $(⟨s_{i+1}⟩,E_{i} ),\sigma_{i} \cup \{ x=v \}{}$  
## Sémantique des cellules  
  
- cellule = identifiant + contenu  
  
- *single-assignement store* : $\sigma_{1}=\{ x=4,y=\xi,z \}{}$  
  
- *multiple-assignement store* : $\sigma_{2}=\{ y:z \}{}$  
	- mémoire complete: $s=s_{1}\cup s_{2}{}$  
## Sémantique des Threads  
  
- intr = `thread< s >end`  
  
- multi ensemble stack sémantique : $MST{}$  
  
- execution : $(MST_{1},\sigma_{1})\to(MST_{2},\sigma_{2})\to\dots{}$  
	- *interleaving semantics* chaque step $\to{}$ execute 1 étape d'un thread  
	- *True concurency semantics* : +1 thread a chaque étape  
# Symbolic Programming  
  
- `<List T> : := nil | T ’|’ <List T>` (notation *EBNF*) (`'|'` : suite doit etre définie)  
  
- tupples, reccords  
# Lambda Calcul  
pseudo-langage de programmation : fonction qui prend un seul argument.   
C’est la base du paradigme fonctionnel.  
fonctions *anonymes*, argument *unique*   
  
- 2 instructions :   
	- abstraction, fonction :  $\lambda x.y{}$ = `{oz}fun{$ X} Y end`   
	- application : $xy=x(y){}$=`{oz}{F1 F2}`  
  
- variable *libre* (*liée*) : pas attachée a un *binder* $\lambda x{}$ ($λx.(yx){}:y$ libre )  
  
- *currying* : $\lambda xy.(x+y)=\lambda x.(\lambda y.(x+y)){}$  
  
- *entiers* : $n ≜ λfx.(f^n(x)){}$ (abstractions)  
  
- *booléens* $true ≜ λab.a$ et $false ≜ λab.b{}$  
	- $NOT(p) ≜ λp.p \;FALSE\quad TRUE{}$  
	- $OR(p, q) ≜ λpq(ppq){}$  
	- $AN D(p, q) ≜ λpq(qpq){}$  
	- $IF\_THEN\_ELSE(p,a,b) ≜ λpab(pab){}$  
  
- *Pairs* …  
  
- *opérateurs élémentaires* …  
  
- SUCC, PLUS, MUL, POW  
  
- *Y -Combinator* : $Y ≜ λg.(λx.g(x\;x))(λx.g(x\;x)){}$  
	$Yg=(\lambda x.g(x\;x))(\lambda x.g(x\;x))=g((\lambda x.g(x\;x))(\lambda x.g(x\;x)))=g(Yg){}$  
## Réductions  
  
- $\alpha{}$ Renaming : $\lambda x.x \implies \lambda y.y{}$  
  
- $\beta{}$ réduction : $(λx.x)(y)\implies y{}$  
  
- $\eta{}$ réduction : $λy.(λz.p)y\implies λz.p{}$  
	- *applicative order* : arguments puis fonctions  
	- *normal order* : fonction puis arguments si néscéssaire  
&nbsp;  
# Abstraction de Données  
→ programmation orientée objet  
  
- *Encapsulation* : cacher parties du codes ⇒ sécurité  
  
| 4 *abstraction de données*    |         etat         |                        sans état                         |  
| ----------------------------- | :------------------: | :------------------------------------------------------: |  
| valeurs et opérateurs liée    |       *Objet*        |         *Objet fonctionnel* (renvoie nouv objet)         |  
| Valeurs et opétateurs séparés | *ADTS* (struct en C) | *ADT* : Abstract Data Type (justes fonctions (entiers )) |    
    
# Programmation concurrentielle  
  
- **Thread** : séquentiel, indépendant, (interleaving semantics), comm  
  
- *Scheduler* (ordonnanceur) : reparti l'usage au proccesseur (selon priorité)  
  
- ordre d'éxécution :   
	- ordre d'éxecution *total* : ordre possible : tt le code  
	- ordre d'éxecution *partiel* : constant (Y=0 puis Z=Y+1)  
	- ordre d'éxecution *effectif* : total observé  
  
- *Non-déterminisme* : meme arguments → réponse différente  
