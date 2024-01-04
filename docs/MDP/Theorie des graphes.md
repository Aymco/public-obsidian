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
