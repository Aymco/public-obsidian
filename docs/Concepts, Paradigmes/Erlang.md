---  
share: true  
category: Concepts, Paradigmes  
tags:  
  - matière  
created: 2024-05-27  
updated: 2024-05-28  
---  
+rapide : thread et message ⇒ programmation concurentielle  
  
- pas d'assignation → patern matching  
  
- variables *immuables*  
  
- language *fonctionnel* (pas de variables globals, fonctions = valeur)  
  
- struct de données : valeurs sumboliques  
  
- acteur = thread (sa mémoire et peut echanger des messages)  
## Let it crash  
  
- spawn() crash : continue normalement  
  
- spawn_link(Function) crash : exit  
  
- process_flag(trap_exit, true), spawn_link(Function) crash : receive exit msg  
# Code  
```erlang title:"data Types"  
Integers: 1112223344455666777888999000 %of unlimited size  
Floats: 1234.5678, 6.0221415e23  
Strings: "This is a string." (ASCII) %enclosed in double quotes  
Atoms: atom1, 'Atom 2' %Begin with a lowercase, or in single quotes  
Lists: [abc, 123, "pigs in a tree"]  
Tuples: {abc, 123, "pigs in a tree"}  
Binaries: <<0, 255, 128, 128>>, <<"hello">> %n bits is a multiple of 8.  
```  
&nbsp;  
```erlang title:"Operations"  
arithmetic : +X-X; X*Y; X/Y; X div Y; X rem Y;  
comparison : X<Y; X=<Y; X=:=Y; X=/=Y; X>=Y; X>Y; (num : X == Y X /= Y)  
boolean    : not and or andalso orelse  
bitwise    : bnot band bor bxor bsl bsr  
```  
&nbsp;  
```erlang title:"if, case"  
case a of  
	paternN (when GuardN) -> expressionN  
end  
if  
	GuardN -> expressionN  
end  
```  
&nbsp;  
```erlang title:Guards  
abs(Number)   
hd(List)   
node(X)   
size(Tuple)   
element(Integer, Tuple)   
length(List)   
round(Number)   
trunc(Number)   
float(Number)   
node()   
self()   
tl(List)  
```  
&nbsp;  
```erlang title:lists  
[Expression || Generator, GuardOrGenerator, ..., GuardOrGenerator]  
N = [1, 2, 3, 4, 5].   
L = [10 * X + Y || X <- N, Y <- N, X < Y].  
hd(List) -> Element % Returns the first element of the list  
tl(List) -> List % Returns the list minus its first element  
length(List) -> Integer % Returns the length of the list  
List = lists:seq(1, 10).  
lists:all(fun(X) -> X rem 2 =:= 0 end, List). % or any  
[F || {F, C} <- List, C =:= yellow].  
```  
&nbsp;  
```erlang title:"function"  
name(Patterns1) -> Expression_sequence1; ...  
name(PatternsN) -> Expression_sequenceN.  
fun( Patterns1) -> Body1; ...  
	(PatternsN) -> BodyN  
end  
```  
&nbsp;  
```erlang title:recursion  
loop():  
	recuive:  
		something ->   
			take some action,  
			loop();  
	end. % tail recursive (compiler will set a while(true))  
```  
&nbsp;  
```erlang title:"Input - output"  
Line = io:get_line(Prompt).  
Term = io:read(Prompt).  
io:format(StringToPrint)  
io:format(FormatString, ListOfData).  
% FILE input and output  
{ok, Stream} = file:open(FileName, read),  
	Line = io:get_line(Stream, ''), % May return eof file:close(Stream).  
{ok, Stream} = file:open(FileName, write),  
	io:format(Stream, FormatString, ListOfData),   
	file:close(Stream).  
```  
&nbsp;  
```erlang title:messages  
Pid = spawn(Fun) % creer un nouveau processus  
Pid = spawn(Module, Fun, Args)  
Pid ! message % envoyer un msg  
Pid ! {self(), msg} % send its own Pid  
receive  
	patern1 when guard1 -> expr1; ... % guards is optionnal  
end  
```  
&nbsp;  
```erlang title:registering  
register(AnAtom, Pid) % Pid globally accessible “name” AnAtom  
unregister(AnAtom)  
whereis(AnAtom) -> Pid | undefined   
registered() -> [AnAtom :: atom()] % all registered processes  
```  
&nbsp;  
```erlang title:linking  
link(Pid) (unlink(Pid))  
spawn_link(Fun)  
exit(Reason) % terminate and send exit message to linked processes  
exit(Pid, Reason) % just send exit msg to Pid  
```  
