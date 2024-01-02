---  
share: true  
category: Chimie 2  
tags:  
  - matière  
created: 2023-11-01  
updated: 2024-01-02  
---  
  
#todo   
# Transformations  
### Recap - transformations  
|     transformation     | cst |                rel                | $W$              | $Q$                       |  
|:----------------------:| --- |:---------------------------------:| ---------------- |:------------------------- |  
|       isotherme        | $T$ |             $d(pV)=0$             | $=-pdV$          | $=-W$                     |  
|        isobare         | $p$ | ${T_{2}}/{T_{1}}={V_{2}}/{V_{1}}$ | $=-p\Delta V$    | $=\Delta H=C_{p}\Delta T$ |  
|        isochore        | $V$ | ${T_{2}}/{T_{1}}={p_{2}}/{p_{1}}$ | $0$              | $=\Delta U=C_{v}\Delta T$ |  
| Adiabatique reversible | $S$ |         $d(pV^\gamma)=0$          | $=C_{v}\Delta T$ | $0$                       |  
## Isotherme  
$$  
\begin{align}  
dH=C_{p}dT=0\\  
dU=C_{v}dT=0\\  
dH=d(U+pV) \implies 0=d(pV)   
\end{align}  
$$  
$$  
\begin{align}  
\Delta U= \Delta Q + \Delta W=0\\  
Q=\int p \, dV =\int -V \, dp   
\end{align}  
$$  
## Isochore, isobare  
  
$$  
dq=c_{v}dT=c_{p}dT  
$$  
## Adiabatique  
$\delta q=0$  
$$  
\begin{align}  
d(pV^\gamma)=0\\  
\end{align}  
$$  
$\gamma=1+\frac{R^*}{cv}=\frac{C_{p}}{C_{V}}$  
$\gamma_{gp}=\frac{ddl+2}{ddl}$  
  
# Cycles  
$\oint du=0$  
Cycle moteur : $\oint dw>0$  
cycle récepteur : $\oint dw <0$  
**Rendement** : $\eta=\frac{{Q_{fourni}-Q_{\mathrm{Re}jeté}}}{Q_{fourni}}$  
### Coefficient de performance  
$COP_{froid}=|\frac{q_{f}}{w_{m,t}}|$  
$COP_{chaud}=|\frac{q_{c}}{w_{m,t}}|$  
## Cycle de carnot  
1. Compression isotherme  
2. Compression adiabatique  
3. détente isotherme  
4. détente adiabatique  
### Machine motrice  
$\eta=1-\frac{T_{2}}{T_{1}}$  
### Machine frigorifique  
$COP=\frac{1}{{\frac{T_{1}}{T_{2}}-1}}$  
### Machine - pompe à chaleur  
$COP=\frac{1}{1-\frac{T_{1}}{T_{2}}}$  
  
## Diagramme de cycle  
### (p,V)  
isochore , isobare → lignes  
travail : surface fermé par le cycle $w_{T}=-\oint pdv$  
### (s,T)  
adiabatique, isotherme  
chaleur totale perçue $q_{t}=\oint Tds$  
### Aires equivalentes  
$0=q+w$ car cycle  
les aires sont égales  
