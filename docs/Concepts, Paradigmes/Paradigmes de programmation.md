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
  
- *accumulateur* : *tail-recursive* (moins de stack)  
```oz title:  
accFac(n,acc) =   
	if(n>1) then fac(n-1, a*1)  
	else 1 end  
Fac(n) = accFac(n,1)  
```  
  
- *Invariant Programming* : $n!\cdot a=x{}\to n!=1,a=x$   
  
- *programmation d'ordre supérieur* :*ordre* d'une fonction :   
	- ordre 1 : input,output !fonction  
	- ordre N+1: input,output fonctions ordre N  
	- *genericity* : ex: Map  
	- *instantiation* : retourne une fonction  
	- *compose* f°g  
	- *FoldL* : `{oz}fun{FoldL List Fun Acc}` applique `{oz}{Fun Head Acc}` sur tt List  
	- *encapsulation* : `{oz}fun{Zero} 0 end`  
	- *delayed execution* : `{oz}proc{} if {Cond} then {exe} end end`  
## Language noyeau  
&nbsp;  
# Programmation orientée objet  
JAVA  
# Programmation en flot de données déterministe  
  
- ajout de la concurrence  
  
- dataflow execution :   
	- attend → X libre ⇒ executer  
  
- producteur consommateur  
  
- client-serveur : *non-déterminisme* : décision faite hos portée du programme  
	- ⇒flot de donnée déterministe X cassé  
  
- AVEC des ports   
	- …  
  
- …  
&nbsp;  
  
- Programmation concurrentielle :  
	- *flot de données déterministe* : limitation non déterministes  
	- *flot de données déterministe avec de ports* : meilleur compromis  
	- *message passing* (multi agent actor) : Complet mais complique (Erlang)  
&nbsp;  
# Programmation multi agents  
  
- *Sieve of eratosthenes* : retourne nb premiers :   
	- chaque agent retire les multiples d'un nombre  
  
- *Digital logic simulation* :   
# Message-passing concurrency (multi agent)  
#TODO   
