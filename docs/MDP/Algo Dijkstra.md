---  
share: true  
category: MDP  
created: 2023-09-20  
updated: 2024-01-04  
---  
  
  
- $d(i)$ *cout min* d'un chemin en passent par les noeuds déja visités  
  
- $Ns$ ensemble des *noeuds visités*  
  
- $v$ le noeuds ajouté (le plus proche parmi les invisités)  
  
- loop :   
	- $v$ : element minimise d(v)  
	- $Ns$ := NS U {v}  
  
 $\mathcal{O}(|N^2|)$  
