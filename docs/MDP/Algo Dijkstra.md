---  
share: true  
category: MDP  
created: 2023-09-20  
updated: 2024-01-03  
---  
  
## Dijkstra  
d(i) cout min d'un chemin en passent par les noeds déja visités  
Ns ensemble des points visités  
v le noeuds ajouté (le plus proche parmi les invisités)  
  
loop  
	v : element minimise d(v)  
	Ns := NS U {v}  
  
ordre quadratique O(|N$^2$|)  
  
[CP](CP.md)  
[algo](algo.md)  
