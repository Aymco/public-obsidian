---  
share: true  
category: Concepts, Paradigmes  
tags:  
  - matière  
created: 2024-05-27  
updated: 2024-06-14  
---  
[Oz (langage) — Wikipédia](https://fr.wikipedia.org/wiki/Oz_(langage))  
[OzCheatSheet](https://github.com/alhassy/OzCheatSheet)  
  
- Dataflow  
# Variables  
upp  
```oz title="variables"  
local X, Y in  
	X = 6   
end  
declare # Creates a link identifier (name) <-> variable(value).   
X = 2 + 8  
```  
&nbsp;  
```oz title:"List Tupples and Records"  
<List T> ::= nil | T ‘|’ <List T>  [EBNF grammar rule]  
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
&nbsp;  
# More (piwy)  
### Functions on lists  
```oz  
fun {Head Xs} Xs.1 end  
fun {Tail Xs} Xs.2 end  
```  
&nbsp;  
```oz title:"Sum of list elements (naïve and with accumulator)"  
fun {Sum L}  
	if L==nil then 0  
	else {Head L} + {Sum {Tail L}}  
end end  
fun {Sum2 L A}  
	if L==nil then A  
	else {Sum2 {Tail L} A+{Head L}}  
end end  
```  
&nbsp;  
```oz title:"Return the nth element of L"  
fun {Nth L N}  
	if N==1 then {Head L}  
	elseif N>1 then {Nth {Tail L} N-1}  
end end  
```  
## Trees  
**Inserting A new key in an ordered binary**  
```oz  
fun {Lookup K T}  
	case T  
	of leaf then notfound  
	[] tree(key:Y value:V T1 T2) andthen K==Y then  
		found(V)  
	[] tree(key:Y value:V T1 T2) andthen K<Y then  
		{Lookup K T1}  
	[] tree(key:Y value:V T1 T2) andthen K>Y then  
		{Lookup K T2}  
	end  
end  
```  
&nbsp;  
```oz  
fun {Insert K W T}  
	case T  
	of leaf then tree(key:K value:W leaf leaf)  
	[] tree(key:Y value:V T1 T2) andthen K==Y then  
		tree(key:K value:W T1 T2)  
	[] tree(key:Y value:V T1 T2) andthen K<Y then  
		tree(key:Y value:V {Insert K W T1} T2)  
	[] tree(key:Y value:V T1 T2) andthen K>Y then  
		tree(key:Y value:V T1 {Insert K W T2})  
	end  
end  
```  
## Tuples  
**Operations on tuples**  
`{Label X}` returns the label of tuple `X` . The label is a constant, called an atom.  
`{Width X}` returns the number of fields.  
**Accessing fields**  
Fields are numbered from `1` up to `{Width X}`.  
`X.N` returns the nth field of tuple `X`:  
**Building a tree**  
&nbsp;  
A tree can be built with tuples:  
&nbsp;  
```oz  
declare  
Y=left(1 2) Z=right(3 4)  
X=mid(Y Z)  
```  
&nbsp;  
**Testing equality**  
&nbsp;  
Equality testing with a number or atom → the number or atom must be the same.  
&nbsp;  
Equality testing of trees → the two trees must have the same root tuples and the same subtrees in corresponding fields. Careful when the tree has a cycle !  
&nbsp;  
### A list is a tuple  
&nbsp;  
The list `H|T` is actually a tuple `‘|’(H T)`. → it is the same thing in the kernel language but for programers comfort there is a syntactic sugar for writing list.  
&nbsp;  
**Syntax of lists as tuples**  
&nbsp;  
```oz  
‘|’(1:5 2: ‘|’(1:6 2: ‘|’(1:7 2:nil))) -> [5, 6, 7]  
```  
&nbsp;  
## Record  
&nbsp;  
> [!INFO]  A record is a generalization of a [tuple](https://www.notion.so/Concepts-paradigms-and-semantics-of-programming-languages-d12fd435d46146b4848caa7daac169c3?pvs=21). Field names can be atoms or any integer. Does not have to start with 1 and does not have to be consecutive. A record also has a label and a width.  
&nbsp;  
&nbsp;  
&nbsp;  
The position of a field is no longer meaningful. Instead, it is the field name that is meaningful  
&nbsp;  
```oz  
X=state(a:1 2:a b:2)  
X.a=1  
```  
&nbsp;  
**Operations on records**  
&nbsp;  
`{Label X}=state` , `{Width X}=3` and `X==state(a:1 b:2 2:a)`.  
&nbsp;  
`{Arity X}` returns a list of field names → [2 a b] (in lexicographic order). Also works for tuples and lists.  
&nbsp;  
A tuple is a record ⇒ The kernel language contains only records.  
&nbsp;  
The record: `X = state(1:a 2:b 3:c)` is the same as the tuple: `X = state(a b c)`  
&nbsp;  
> [!INFO]  The contextual environment of a function / procedure contains all the identifiers that are used inside the function but declared outside of the function.  
&nbsp;  
&nbsp;  
&nbsp;  
> [!INFO]  A free identifier of an instruction is an identifier used inside the instruction that is declared outside the instruction.  
&nbsp;  
&nbsp;  
&nbsp;  
Procedure arguments are not free because the argument defines the identifier  
&nbsp;  
```oz  
local Z in Z=X+Y end   
# Has two free identifiers: {X,Y}  
local Q in  
	proc {Q A} {P A+1} end  
end  
# Has one free identifier: {P}  
# `A` is not free!  
```  
