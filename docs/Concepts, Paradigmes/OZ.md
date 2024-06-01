---  
share: true  
category: Concepts, Paradigmes  
tags:  
  - matière  
created: 2024-05-27  
updated: 2024-05-28  
---  
[Oz (langage) — Wikipédia](https://fr.wikipedia.org/wiki/Oz_(langage))  
[OzCheatSheet](https://github.com/alhassy/OzCheatSheet)  
# Variables  
upp  
```oz title="variables"  
local X, Y in  
	X = 6   
end  
declare X = 2 + 8  
```  
&nbsp;  
```oz title:"List Tupples and Records"  
List = [ 1 2 3 ] = 1|2|3|nim  
circle(1:0 2:1 3:3 4:blue 5:dots) % tupple  
Tupple = jasim('a' 3 neato)  % Tuple of three values  
Record = circle(x:0 y:3 radius:3 color:blue style:dots) % record  
Tupple.2 == Record.y  
```  
&nbsp;  
```oz title="Cellules"  
C = {NewCell}  
C := 1  
C := C + 1  
{Browse @C}  
```  
&nbsp;  
```oz title="Fonctions"  
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
```oz title="execptions"  
try  
	{}  
catch X then {Browse X}   
finally {CloseFile F}  
end  
```  
&nbsp;  
```oz title:concurrence  
fun {Map List F}  
	case List of nil then nil  
	[] H|T then thread {F H} end | {Map T F}  
end  
declare F  
{Browse {Map [1 2] F}} % [_ _]  
F = fun {$ X} X+1 end  % [2 3]  
```  
