---  
share: true  
category: Concepts, Paradigmes  
tags:  
  - matière  
created: 2024-05-28  
updated: 2024-05-28  
---  
# Paradigmes en général  
=manière de programmer  
  
- *programmation impérative* : déroulement du programme  
	- *orienté objet*  
	- programmation *structurée  
	- Programmation *procédurale*  
  
- *programmation déclarative* : résultat du programme  
	- programmation *fonctionnelle*  
	- programmation *logique*  
Languages noyeau des paradigmes : (svt 1 conept qui differe)  
![Pasted image 20240528155806.png](Pasted%20image%2020240528155806.png)  
&nbsp;  
# Programmation Fonctionnelle  
&nbsp;  
  
- *programmation déclarative*  
  
- permet :   
	- *Invariant prog*, symbolic prog  
	- high order prog, data abstraction  
	- concurrent prog  
  
- *Single-assignement variable*  - variable *immuables* (identificateur muable)  
  
- *recursion* :   
```oz title:recursion  
for(s,i,transform) =   
	if(i>0) then for(transform(s), i-1, transform)  
	else s  
	end  
```  
  
- *accumulateur* : *tail-recursive*   
```oz title:  
accFac(n,acc) =   
	if(n>1) then fac(n-1, a*1)  
	else 1 end  
```  
