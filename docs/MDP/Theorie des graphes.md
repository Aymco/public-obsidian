---  
share: true  
category: MDP  
created: 2023-09-20  
updated: 2024-01-04  
---  
  
[MDP](MDP.md)  
# Graphes  
$G(N,R)$ :  triple($N$ Noeuds, $R$ aretes, $I$ relation Incidence $N-R$)  
  
- **ordre** $|N|$ : nombre de $N$  
  
- boucle : arête d'un noeud sur lui même  
  
- **degré** de $N$ : nombre d’arêtes   
  
- **Parcours** suite alternée de $N$ et $R$ : $P:=(i_{0}, \alpha_{1},i_{1} \dots)$  
	- de longueur $k$ (ouvert / fermé)  
  
- **Cycle** : $N\neq$  sauf $i_{0}=i_{k}$  
  
- **Piste** : parcours avec $R\neq$  
	- **Circuit** : Piste fermée  
  
- **Eulérienne** : passe par tous les $R$  
  
- **Hamiltonien** : passe par tous $N$  
  
## Types de graphes:  
  
- graphe **simple** : ! liaisons doubles, ! boucles  
  
- graphe **connexe** : tous $N$ relié  
  
- **arbre** : connexe,  !cycle, $|R|=|N|-1$, 1 seul chemin pour$N$  
	- arbre **sous-tangent** : graphe ou on à sélectionné des $R$ qui forment un arbre  
	- [Algo Kruskal](Algo%20Kruskal.md)  
  
- graphe **orienté** (pondéré)  
  
- graphe **isomorphe** : $G(N,R),G'(N',R')$ isomorphes : bijection $N\to N'$  
  
- *Théorème d'Euler* : Piste Eulérienne <=> max 2 noeuds de degré impair (connexe)  
  
  
- [Algo Dijkstra](Algo%20Dijkstra.md)  
  
- [Bellman-Ford](Bellman-Ford.md) : fonctionne avec des poids négatifs  
  
  
- représentation *matricielle* :   
	- matrice d'adjacence : $A=(N,S)$ : $|N|\times |N|$  
	  
