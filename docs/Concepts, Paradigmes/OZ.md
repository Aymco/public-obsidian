---  
share: true  
category: Concepts, Paradigmes  
tags:  
  - matière  
created: 2024-05-27  
updated: 2024-05-28  
---  
[Oz (langage) — Wikipédia](https://fr.wikipedia.org/wiki/Oz_(langage))  
# Variables  
``` oz title:"variables"  
local X, Y in  
	X = 6   
end  
declare X = 2 + 8  
```  
&nbsp;  
``` oz title:"Cellules"  
C = {NewCell}  
C := 1  
C := C + 1  
{Browse @C}  
```  
&nbsp;  
``` oz title:Fonctions  
% définition de *fonction* (λx.t)  
declare  
fun {Name X} T end  
proc {Test A} {Browse A + 10} end  
% appel de fonction  
{Name 5}  
% currying  
F = fun {$ X} fun {$ Y} T end end  
```  
&nbsp;  
```oz title:execptions  
try  
	{}  
catch X then {Browse X}   
finally {CloseFile F}  
end  
```  
