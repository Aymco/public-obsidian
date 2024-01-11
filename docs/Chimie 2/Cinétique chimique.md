---  
share: true  
category: Chimie 2  
tags:  
  - matière  
created: 2023-12-26  
updated: 2024-01-11  
title: Cinétique chimique  
---  
  
décrit la *vitesse* de réaction (tend vers équilibre(→thermo))  
  
soit la réaction : $\chi_{A}A+\chi_{ b}B\to \chi_{m}M+\chi_{n}N$  
  
- **Avancement d'une réaction** :  $d\xi=\frac{dn_{P}}{\chi_{P}}=-\frac{dn_{R}}{\chi_{R}}=[mol]$  
  
- **vitesse de réaction** : $r=\frac{1}{V}\frac{ d\xi(t) }{ dt }=\left[ \frac{mol}{L\cdot s} \right]$  
	- volume cst ⇒ $r=\frac{1}{\chi_{i}} \frac{d[mol/L]}{dt}$  
	- taux de production $P_{i}(t)=\frac{[j]}{[f]_{f}}$ / conversion $C_{i}(t)=1-\frac{[j]}{[j]_{f}}$  
  
- **vitesse d'apparition** produit et réactifs: $R_{A}=|\frac{1}{V} \frac{dn_{A}}{dt}|=\frac{\chi_{A}}{V} \frac{d\xi}{dt}=\chi_{A}r$  
  
  
- $r=k[A]^\alpha[B]^\beta\dots[M]^\mu[N]^\eta$ avec   
  
- constante de vitesse $k$   
  
- *ordre partiels* : $\alpha,\beta, \mu,\eta$ (svt : produit $0$, réactif $\alpha>0$; $<0$⇒ inhibition)  
  
- *ordre global* : $\alpha+\beta+\dots$   
  
- ordre 1 : réaction monomoléculaire $A=P$ : $k=[1/s]$  
	- $r=k[A]=-\frac{d[A]}{dt}$ ⇒ EDO exponentielle  
  
- ordre 2 : réaction bimoléculaire $2A=P$ ⇒ $k=[L /mol\cdot s]$  
	- $r=k[A]^{2}=-\frac{1}{2} \frac{d[A]}{dt}$ ⇒ EDO inverse : $[A]=\frac{[A]_{0}}{1+2[A]_{0}kt}$  
  
- pseudo ordre 0 : $A=P\implies r=k\implies[A]=[A]_{0}-kt$   
	- (réactif >> pdv vitesse :$[A]\gg[B]\implies[A] = [A]_{0}$)  
## Influence de la température sur la vitesse  
  
- *Loi d'Arrhénius* : $k=Ae^{-E_{a}/RT}$  (Collision élastique sinon)  
  
- $E_{a}$ l'énergie d'activation par mol barrière  
  
- Théorie des *collisions* (phase gazeuse) :    
	- réaction si $E_{cin}>E_{a}$ ⇒$e^{-E_{a}/RT}$ mol * $A$(facteur de frequence !tt reaction)  
  
- Théorie du *complexe activé* : Transition State Theory (TST)  
	- Collision ⇒ déforme molécules ⇒ Energie cinétique → Energie potentielle    
	- ⇒ $ABC^\#$édifice transitoire : complexe activé ($E_{p}+$ avec liaisons transitoires)  
![Pasted image 20240103145607.png](Pasted%20image%2020240103145607.png)  
  
- *Catalyseur* : fournit nouveau chemin réactionnel avec $E_{a}'<E_{a}$⇒ + mol passent  
  
- Réaction radicales en chaine :   
	- Initialisation : formation des radicaux (=intermédiaires réactionnels)  
	- propagation : action des radicaux sur réactifs (conservation des radicaux)  
	- Terminaison : destruction des radicaux  
  
- Quasi-stationnarité des radicaux: v apparition = v disparition  
