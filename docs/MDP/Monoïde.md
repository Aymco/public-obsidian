---  
share: true  
category: MDP  
created: 2023-10-11  
updated: 2024-01-03  
---  
  
# Définition ==Monoïde==  
  
- ==[Structure algébrique](Structure%20alg%C3%A9brique.md)==  
  
- ==associativité== : $a*(b*c) = (a*b)*c$  
  
- ==neutre== $\exists e: e \in A; \forall a \in A : e*a=a*e=a$  
### Théorème 1 : ==neutre unique== $\exists ! e \in A, \forall a \in A : e*a=a*e=a$  
# Développement  
## Exemple  
  
- $(A^A, \circ)$ l'ensemble des fonction de $A\to A$ et $\circ$ l'opérateur composition  
# Définition : ==Sous monoïde==  
  
- $\forall a,b \in \mathbb{R}, a*b \in \mathbb{R}$  
  
- $1_A \in B, e_A \in B$  
**Théorème** : ==isomorphisme== $(A,*)$ est isomorphe a un sous monoide de $(A^A, \circ)$  
### **définition** : ==Inverse==  
  
- $a$ inverse de $b$ si $a*b=b*a=e$  
**Théorème** : ==inverse unique== : si $\exists a, b \in A, a*b=e$, alors $a$ est unique  
