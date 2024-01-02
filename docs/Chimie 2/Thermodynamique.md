---  
share: true  
category: Chimie 2  
tags:  
  - matière  
created: 2023-11-02  
updated: 2024-01-02  
---  
  
# Systèmes  
  
- Système **ouvert** : échange de masse et de chaleur  
  
- Système **fermé** : échange de chaleur  
  
- Système **isolé** : !échange   
![Variable, fonction d'état > Variable, fonction d'état](Variable,%20fonction%20d'%C3%A9tat.md#variable-fonction-detat)  
## Détente d'un gaz  
Transformation isotherme réversible ([travail réversible](travail%20r%C3%A9versible.md)) :  
  
- $\delta W=-pdV$  
  
- $W=mR^*T\ln\left( \frac{p_{2}}{p_{1}} \right)$  
## [1er principe thermodynamique - principe d'équivalence](1er%20principe%20thermodynamique%20-%20principe%20d'%C3%A9quivalence.md)  
  
## 2 Eme expérience de Joule  
$\pi_{T}=\left( \frac{ \partial U }{ \partial V } \right)_{T}=0$ pour les gaz parfaits  
## **Enthalpie** $H:=U+pV$  
$p$ constan t : $\delta Q_{p}=dH$  
## Capacité calorifique  
Capacité calorifique à volume constant $C_{V}:=\left( \frac{ \partial U }{ \partial T }  \right)_{V}$  
### Gaz parfait  
comme $U$ est une variable d'état (dépend de $T,V$): $dU=C_{V}dT$  
> [!info]- on considère que $C_{V}$ est constant : $\Delta U=C_{V}\Delta T$  
> en réalite il faudrait faire $\Delta U=\int_{T_{1}}^{T_{2}} C_{V} \, dT$   
#### Capacité calorifique à pression constante  
$C_{p}:=\left( \frac{ \partial H }{ \partial T }  \right)_{p}$ → à pression constante : $dH=C_{p}dT$  
### Gaz quelconque  
$\left( \frac{ \partial U }{ \partial T } \right)_{p}=\pi_{T}\left( \frac{ \partial V }{ \partial T } \right)_{p}+C_{V}$  
### Relation de mayer $C_{P}>C_{V}$  
gaz parfait : $C_{p}-C_{V}=nR=mR^*$  
gaz quelconque : $C_{p}-C_{V}=\alpha \pi_{T}V+\alpha pV$  
$\alpha$ coefficient de dilatation thermique à pression constante : $\alpha=\frac{1}{V}\left( \frac{ \partial V }{ \partial T } \right)_{p}$  
  
# 1 Er principe et systèmes ouverts  
## Conservation de la masse  
$n$ le nombre de frontière ouvertes  
$\frac{dm}{dt}=\sum_{1}^{n}\dot{m}_{i}$  
incompressible : $\frac{dV}{dt}=\sum_{1}^{n}\dot{V}_{i}$  
## Conservation de l'énergie mécanique  
variation énergie cinétique : $\Delta k=w_{i}+w_{e}+w_{d} =\frac{c_{2}^{2}}{2}-\frac{c_{1}^{2}}{2}=[J /kg]$  
  
- $w_{i}$ travaux des forces internes  
	- changement de pression - viscosité du fluide : $w_{i}=\int_{1}^{2} p \, dv-w_{f}$  
  
- $w_{e}$ travaux des forces externes de contact :  
	- travail externe $w_{m}$ et force d'entrée :  $w_{e}=w_{m}-\Delta(pv)$  
  
- $w_{d}$ travaux des forces à distance : $w_{d}=-g\Delta z$  
  
→ $w_{m}=\int_{1}^{2} v \, dp+\Delta k+g\Delta z+w_{f}$  
### Équation de Bernouilli  
travail moteur nul, dissipation par frottement nulles, fluide incompressible :  
$p_{1}+\frac{\rho c_{1}^{2}}{2}+pgz_{1}=p_{2}+\frac{\rho c_{2}^{2}}{2}+pgz_{2}$  
## Premier principe pour les systèmes ouverts  
en prenant en compte l'énergie interne  
$w_{m}=-q+\Delta u+\Delta\left( \frac{c^{2}}{2} \right)+g\Delta z+\Delta(pv)$  
$=-q+\Delta h+\Delta k+g\Delta z$  
→ $\Delta h=\int_{1}^{2} v \, dp+q+w_{f}$  
  
# [Entropie](Entropie.md)  
  
## [cylcles thermodynamiques](cylcles%20thermodynamiques.md)  
  
# Systèmes ouverts  
$w_{m}=\int_{1}^{2} v\, dp+\Delta k+g\Delta z+w_{f}$  
régime permanent : $A_{1}c_{1}=A_{2}c_{2}$ (mm débit)  
pression dynamique : $p_{dyn}=\frac{\rho c^{2}}{2}$  
premier principe : $\Delta h=\int_{1}^{2} v \, dp+q+ww_{f}$  
