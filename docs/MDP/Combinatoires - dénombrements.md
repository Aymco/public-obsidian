---  
share: true  
category: MDP  
tags:  
  - matière  
created: 2023-12-19  
updated: 2024-01-03  
---  
  
# Résumé combinatoires  
| x         | Repetition    | ~~répetition~~ |  
| --------- | ------------- | -------------- |  
| tout      | $Q^{a,b}_{n}=\frac{n!}{a!b!}$ | $P_{n}=n!$        |  
| ordre     | $B^p_{n}=n^p$     | $A^p_{n}=\frac{n!}{(n-p)!}$      |  
| ~~ordre~~ | $D^p_{n}=C^p_{n+p-1}$     | $C^p_{n} = {n \choose p}=\frac{n!}{k!(n-k)!}$      |   
# Développement  
## Combinaisons $C^p_{n}$  
~~repetition~~, ~~ordre~~  
$n \choose k$ $=B(n,k)=C^k_{n}=\frac{n!}{k!(n-k)!}=C^k_{n-1} +C^{k-1}_{n-1}$    
### Binômes de Newton  
$(x+y)^n=\sum_{k=0}^{n}C^k_{n}x^ky^{n-k}$  
## Selection $B^*(n,k)=D^p_{n}$  
repetition, ~~ordre~~  
choisir $p$ eléments parmi $n$ elements   
## Permutations $P_{n}=A^n_{n}$  
~~repetition~~, tout  
bijection entre 2 ensembles ( $n=|A|=|B|$)  
$Bij(n\to n) =P_{n}= n!$   
  
## Arrangement,. Assignations $A^p_{n}$  
! répetitoin, ordre  
  
$Inj(p\to n)$  
## Liste  
ordre, repetition  
$Fct(n\to p)=B^p_{n}=n^p$  
  
## Remplissages  
$p$ vetements dans $n$ tiroirs  
$C^{p-n}_{p-1}$ ??  
$Sur(n\to k)$  
## Dérangements  
permutation avec $f(a)=a$ :on retire les bijection  → $S=F- \cup Fi$  
$d_n=n!\sum_{r=0}^{n}\frac{-1^r}{r!}$  
  
## Partitions  
$n$ enfants → $k$ groupes  
$Par(n\to k)=S(n,k)=Sur(n\to k)$  
nombre de Stirling : $S(n,k) = S(n-1,k-1)+kS(n-1, k)$  
  
## Next level 1D game  
