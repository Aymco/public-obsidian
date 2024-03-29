---  
share: true  
category: Chimie 2  
tags:  
  - matière  
created: 2023-11-02  
updated: 2024-01-17  
title: Thermodynamique  
---  
  
  
- [Gaz Parfait](Gaz%20Parfait.md)  
  
- [Variable, fonction d'état](Variable,%20fonction%20d'%C3%A9tat.md)  
  
  
- Système **ouvert** : échange de masse et de chaleur  
  
- Système **fermé** : échange de chaleur  
  
- Système **isolé** : !échange   
# Systèmes Fermé  
  
  
- [Entropie](Entropie.md)  
  
- [cylcles thermodynamiques](cylcles%20thermodynamiques.md)  
## 1er Principe thermodynamique - principe d'équivalence  
**Energie interne** :  $\Delta U=Q+W$ (variable d'état)  
	**chaleur** $Q$ (du point de vue du système ) équivalent au **travail** $W$   
  
- $\delta W=-pdV$ (cas réversible : transformation lente, $p_{interne} = p_{externe}$)  
	- (⇒ $W=mR^*T\ln\left( \frac{V_{1}}{V_{2}} \right)=mR^*T\ln\left( \frac{p_{2}}{p_{1}} \right)$)  
  
- **Enthalpie** $H:=U+pV$  
	- $dH=\delta Q_{p}$ ($p$ constant)  
  
  
## Capacité calorifique  
**Capacité calorifique** ($V$ cst) $C_{V}:=\left( \frac{ \partial U }{ \partial T }  \right)_{V}=\frac{ddl}{2}R$  
  
- Gaz quelconque ⇒ $dU=C_{V}dT+\pi_{T}dV$   
	- $V$ cst / Gaz parfait ⇒ $dU=C_{V}dT$ ⇒ $\Delta U=C_{V}\Delta T$  
		- (on considère  $C_{V}(T)$ cst)  
**Capacité calorifique** ($p$ cst) : $C_{p}:=\left( \frac{ \partial H }{ \partial T }  \right)_{p}$  ⇒. $dH=C_{p}dT$  
  
*Relation de mayer* $C_{P}>C_{V}$ : $C_{p}-C_{V}=\alpha V(\pi_{T}-p)$   
  
- avec $\alpha$ coeff de *dilatation thermique* à $p$ cst : $\alpha=\frac{1}{V}\left( \frac{ \partial V }{ \partial T } \right)_{p}$  
  
- gaz parfait : $C_{p}-C_{V}=mR^*$  
  
coefficient *Joules Thompson* $\mu_{T}=\left( \frac{\delta T}{\delta P} \right)_{H}$   et $\pi_{T}=\left( \frac{ \partial U }{ \partial V } \right)_{T}$   
  
- gaz **quelconques** $\mu_{T}, \pi_{T} \not = 0$  
  
- gaz **idéaux** (GP) $\mu_{T} = \pi_{T}=0$  
  
  
**degrés de liberté** :  
  
- Gaz monoatomiques : $ddl=3$  
  
- Gaz polyatomiques : $ddl=(\lambda _{translation}+\lambda_{rotation}+2\lambda_{vibration})$  
	- $\lambda_{translation}=3$ , $\lambda_{rotation}=2$ à température ambiante    
	- $\lambda_{vibration}=1$ : $T\to$ dissociation($E_{c-vib}=E_{p-vib}=\frac{R}{2}$)  
  
# Systèmes ouverts  
soit $n$ le nombre de frontière ouvertes  
  
- Conservation de la masse $\frac{dm}{dt}=\sum_{1}^{n}\dot{m}_{i}$  
  
- incompressible : $\frac{dV}{dt}=\sum_{1}^{n}\dot{V}_{i}$  
  
- **pression dynamique** : $p_{dyn}=\frac{\rho c^{2}}{2}$  
## Conservation de l'énergie mécanique  
  
- $w_{i}$ travaux des forces *internes*  
	- changement de pression - viscosité du fluide : $w_{i}=\int_{1}^{2} p \, dv-w_{f}$  
  
- $w_{e}$ travaux des forces *externes* de contact : $w_{e}=w_{m}-\Delta(pv)$  
	- avec $w_{m}$ travail externe et force d'entrée  
  
- $w_{d}$ travaux des forces *à distance* - énergie potentielle : $w_{d}=g\Delta z$  
Bilan énergie : $\Delta k+g \Delta z=w_{i}+w_{e} =[J /kg]$  
	⇒ $w_{m}=\int_{1}^{2} v \, dp+\Delta k+g\Delta z+w_{f}$  ($w_{m}>0$ : $W$ reçu par le fluide)  
*Équation de Bernouilli* : $p_{1}+\frac{\rho c_{1}^{2}}{2}+pgz_{1}=p_{2}+\frac{\rho c_{2}^{2}}{2}+pgz_{2}$ travail moteur nul, dissipation par frottement nulles, fluide incompressible  
Bilan Energie mécanique et interne $w_{m}=-q+\Delta h+\Delta k+g\Delta z$ avec $\Delta u+\Delta k+g\Delta z=w_{e}+q$  
	⇒ $\Delta h=\int_{1}^{2} v \, dp+q+w_{f}$ (Premier principe)  
