---  
share: true  
category: MDP  
created: 2023-09-20  
updated: 2024-01-04  
---  
  
[MDP](MDP.md)  
  
# Graphes  
$G(N,R)$ :  ($N$ Noeuds, $R$ aretes, $I$ relation Incidence)  
  
- **ordre** : nombre de $N$  
  
- **degré** d'un noeud : nombre d’arêtes   
  
- **Parcours** de longueur k (nombre d arêtes ).  (ouvert / fermé)  
  
- **Cycle** : 1er = dernier $N$  
  
- **Piste** : parcours avec tt elements distincts  
	- **Eulérienne** : passe par tous les $R$  
	- **Hamiltonien** : passe par tous $N$  
  
## Types de graphes:  
  
- graphe **simple** : !liaisons doubles, !boucles  
  
- graphe **connexe** : tous relié  
  
- **arbre** : connexe + !cycle  
  
- arbre **sous-tangent** : graphe ou on à sélectionné des $R$ qui forment un arbre  
  
- graphe **orienté**  
  
- graphe **isomorphe** : $G_{1} \to G_{2}$  
### Théorème d'Euler  
Piste Eulérienne <=> max 2 noeuds de degré impair  
## Algorithmes  
  
- [Algo Dijkstra](Algo%20Dijkstra.md)  
  
- [Bellman-Ford](Bellman-Ford.md) : fonctionne avec des poids négatifs  
  
- [Algo Kruskal](Algo%20Kruskal.md)  
# Structures Algébriques  
![Structure algébrique > Définition structure algébrique $(A,*)$](Structure%20alg%C3%A9brique.md#definition-structure-algebrique-dollaradollar)  
  
![Monoïde > définition **Monoïde**](Mono%C3%AFde.md#definition-monoide)  
  
![Monoïde > définition **Sous monoïde**](Mono%C3%AFde.md#definition-sous-monoide)  
  
![Groupes (structure algébrique) > définition groupe $(G,*)$](Groupes%20(structure%20alg%C3%A9brique).md#definition-groupe-dollargdollar)  
  
![Anneaux (structure algébrique) > Anneaux Définition $(A, +, *)$](Anneaux%20(structure%20alg%C3%A9brique).md#anneaux-definition-dollara-dollar)  
  
## Applications  
### Encodage  
groupe $(Z_{n}, \cdot \mod p)$ avec $p$ un nombre premier car ($a*b\neq 0$)  
  
→ groupe $<g>$ : facile a calculer $g^x$ mais $\log g^x$ compliqué  
→ $g^x*g^y=g^{x+y}$  
  
Protocole de Diffie-Hellman :  
1. clé privée $x,y$  
2. on envoie $g^x$  
3. peut calculer $g^{x+y}$   
attaque : man in the middle  
### Stockage de données : Solomon-Reed  
Anneau polynomial : $A[X]$ : $\forall a \in A,  \sum a_{i}X^i=p(X) \in A[X]$  
$F_{n}$ anneau sous-jacent, $q$ taille alphabet, $k$ nb de mot, $n$ nb de mot enregistrés  
$code :(F_{q})^k\to(F_{q})^n$  
  
# Dénombrement  
## Equipotence $A \approx B$  
$\iff$ $\exists$ **bijection** entre $A$ et $B$ (mm nb éléments)  
$A$ est **fini** / infini : $A \approx \{ 1,2,..,n \}$  
	cardinal de $A$ : $n=|A|=\#A \in N$  
$A \approx N$ → ensemble infini **indénombrable**  
### $N\approx Z$ : $n\to \left\{\begin{align} \frac{{n+1}}{2}\\ \frac{-n}{2} \end{align}\right.$  
### $N \approx Q$  
Démo  
#todo   
### $N \approx R$  
Démo  
#todo   
  
## Dénombrement [Combinatoires - dénombrements](Combinatoires%20-%20d%C3%A9nombrements.md)  
  
$f(x)=1 : |A|=\sum_{a\in A}^{}f(a)$  
**Unions** d'ensembles : $|A \cup B|=|A|+|B| - |A \cap B|$  
(existe une formule générale)  
**Composition**: $|A\times B|=|A||B|$  
  
![Combinatoires - dénombrements > Résumé combinatoires](Combinatoires%20-%20d%C3%A9nombrements.md#resume-combinatoires)  
   
## Dénombrer avec des génératrices  
![Fonction génératrice > Fonction génératrice définition](Fonction%20g%C3%A9n%C3%A9ratrice.md#fonction-generatrice-definition)  
  
$n$ éléments dans $N$ cases avec $A_{i}$ les valeurs acceptées pour la case $i$  
$f(x)=\prod_{i=1}^N \sum_{j\in A_{i}}x^j$ → réponses $f_{n}$  
#todo   
### Astuces  
  
- $\sum_{i=0}^{\infty}x^i=\frac{1}{1-x}$ et $\lim_{ x \to 1 }$  
  
- $\sum_{i=0}^{\infty}(i+1)x^i=\frac{1}{(1-x)^{2}}$  
  
- $\sum_{i=0}^{\infty}(i+1-a)x^i=\frac{x^a}{(1-x)^{2}}$  
  
### Équations de récurrences $\alpha v_{n+2}+\beta v_{n+1}+\gamma v_{n}=\dots$  
#todo   
  
## Fonctions de hachage  
$H:\{ 0,1 \}^*\to \{ 0,1 \}^n$ taille $?\to n$  
collision si 2 entrées donnent la même valeure  
### Blockchains  
Chaque bloque est le hash du block précédent et d'une donnée  
le block $h_{i}$ peut nous donner toutes les info précédentes  
graine $s$ : nombres aléatoire $a_{n}=H(s,n)$  
