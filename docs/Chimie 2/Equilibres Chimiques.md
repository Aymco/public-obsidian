---  
share: true  
category: Chimie 2  
tags:  
  - matière  
created: 2023-11-20  
updated: 2024-01-18  
title: Equilibres Chimiques  
---  
  
[Thermodynamique](Thermodynamique.md) → équilibre :   
  
  
- **fraction molaire** : $x_i:=\frac{n_{i}}{n}$  
  
- **activité** $a_{i}=\gamma_{i}x_{i}$ :   
	- liquide / solide : $a=1$  
	- $\gamma=1$ solution idéale ($=\frac{p_{i}}{p_{i}^o}$)  
		- liquide idéal : (solution très diluée) $a_{i}=\frac{m_{i}}{m^o_{i}}=m_{i}$   
		- solide idéal : $a_{i}=x_{i}$  
	- $\gamma_{i}<1$ ⇒stable  
  
  
- **potentiel chimique** : $\mu_{i}=\mu_{i}^\circ+RT\ln a_{i}$ (grandeur intensive)  
	- $\mu_{i}=\left( \frac{ \partial G }{ \partial n_{i} } \right)_{T,p,n_{i\neq j}}\equiv G_{m,i}$ **énergie libre molaire partielle**  
	- **potentiel pur** : $\mu^A=\mu^{A^o}+RT\ln\frac{p}{p^o}= G^A_{m}$ **énergie libre molaire**  
  
- tout $A$ migre vers l'endroit ou $\mu_{i}$ est le plus faible  
  
  
- Energie libre de *Helmotz*               $A=U-TS$  
  
- Enthalpie/Energie libre de *Gibbs*  $G = H-TS$  
	- $dG = dU + p dV + V dp − T dS − S dT$   
	- $p,T$ cst ⇒ $dG_{p,T} = dH − T dS$   
	- équilibre ⇒ $dG_{p,T}=0$  
	- Variation selon $p$ : $G_{m}(p,T)=G^o_{m}(T)+\int_{p^o}^{p}  V_{m}(p',T)\, dp'$  
		- gaz parfait ⇒ $=G^o_{m}(T)+RT\ln\left( \frac{p}{p^o} \right)$ (solide + liquide + gaz → gaz)  
		- solide / liquide  $\approx G^o_{m}(T)$  
  
  
  
- seul travail $pdV$ ⇒ $dG_{p,T}< 0$   
  
- équilibre *métastable* : nécessite $E_{a}$ → + stable  
## Équations fondamentales  
(composition fixée, pas de réactoin) :  
  
- $dU=TdS-pdV$ , $U(S,V)$  
  
- $dH=TdS+Vdp$, $H(S,p)$  
  
- $dA=-SdT-pdV$,   $A(T,V)$  
  
- $dG=-SdT+Vdp$ ,  $G(T, p)$  
système a composantes multiples  
  
- $dG=-SdT+Vdp+\sum \mu_{i}dn_{i}$  
  
  
# Separation  
Energie libre standard de formation $\Delta_{f}G^o=\sum_{P}\chi_{P} G^{P^o}-\sum_{R}\chi_{R}G^{R^o}$  
	avec $G^{A^o}=H^{A^o}-TS^{A^o}$   
  
  
- **Avancement d'une réaction** :  $d\xi=\frac{dn_{P}}{\chi_{P}}=-\frac{dn_{R}}{\chi_{R}}=[mol]$  
  
- **énergie libre de réaction** : $\Delta_{r}G=\sum \chi_{i}\mu_{i}=\Delta _rG^\circ+RT\ln Q$   
	- **énergie libre standard de réaction** : $\Delta_{r}G^o=\Delta_{r}H^o-T\Delta_{r}S^o$  
		- $\Delta_{r}G^\circ=\sum\chi_{i}\Delta_{f}G^{i^\circ}_{m}$  
		- energie libre standart de *formation* $\Delta_{f}G^{i^\circ}_{m}=\Delta_{f}H^{i^\circ}_{m}-T\Delta_{f}S^{i^\circ}_{m}$  
	- $\Delta_{r}G=\Delta_{r}G^\circ+RT\ln\mathcal{Q}$  
	- $\Delta_{r}G<0$ évolution spontanée   
	- → équilibre : $\Delta_{r}G=0$ et $\Delta_{r}G^\circ=-RT\ln K$  
  
  
- **Entropie standard de réaction** $\Delta_{r}S^\circ:=\sum \chi_{i}S_{m}^{i^\circ}$   
  
- **Enthalpie standard de réaction** $\Delta_{r}H^\circ:=\sum \chi_{i}H_{m}^{i^\circ}$   
	- $\Delta_{r}H^\circ=\sum\chi_{i}\Delta_{f}H^{i^\circ}_{m}$   
	- Enthalpie standart de *formation* ($\Delta_{f}H^\circ_{298K}=0=\Delta_{f}G^\circ_{298K}$)  
  
- **Quotient réactionnel** $\mathcal{Q}=\frac{\prod_{P}\left( a_{P} \right)^{\chi_{P}}}{\prod_{R}\left( a_{R} \right)^{\chi_{R}}}$  
	- $\mathcal{Q}^\circ_{r}=\Delta_{r}H^\circ=\sum_{P}\chi_{P} H^{P^o}-\sum_{R}\chi_{R}H^{R^o}$  
  
- **constante d'équilibre** : $K:=\mathcal{Q}_{eq}$  
	- liens : $K_{p}=K_{x}\left( \frac{p}{p^o} \right)^{\Delta\chi}=K_{n}\left( \frac{p}{p^o\sum n_{i}} \right)^{\Delta\chi}$   
		avec $\Delta\chi=\sum_{P}\chi_{P}-\sum_{R}\chi_{R}$  
  
- *équation de van't Hoff* : $\frac{d\ln K}{dT}=\frac{\Delta_{r}H^o}{RT^{2}}$  
	- ⇒$\Delta_{r}H$cst - indé de $T$ ⇒ $\ln K_{T_{2}}-\ln K_{T_{1}}=-\frac{\Delta_{r}H^\circ}{R}\left( \frac{1}{T_{2}}-\frac{1}{T_{1}} \right)$  
  
  
  
- **Affinité chimique** : $\mathcal{A}:=-\Delta_{r}\mu=-\left( \frac{ \partial G }{ \partial \xi } \right)_{T,p}=\sum_{R}\chi_{R}\mu_{R}-\sum_{P}\chi_{P}\mu_{P}$  
	- $dG=Vdp+SdT-\mathcal{A}d\xi<0$  
	- réaction à l'équilibre : $\mathcal{A}=0$  
  
# Équilibre chimique entre [Gaz Parfait](Gaz%20Parfait.md)  
  
- mélange idéal : $\mu_{i}=G^{i^\circ}_{m}+RT\ln \frac{p_{i}}{p^\circ}$  
  
- pur : $\mu^A=G^{A^\circ}_{m}+RT\ln \frac{p}{p^\circ}$  
  
- affinité chimique $-\mathcal{A}=\Delta_{r}G^\circ+RT\left( \sum_{P}\chi_{P}\ln \frac{p_{P}}{p^o}- \sum_{R}\chi_{R}\ln \frac{p_{R}}{p^o} \right)$  
# Équilibre chimique en solution liquide  
  
- (Potentiel chimique :  $\mu_{A}=\mu^{A^\circ}+RT\ln a_{i}$)  
  
## Dissolution  
  
- **produit de solubilité** $K_{s}=\frac{[A^+]_{sat}[B^-]_{sat}}{[AB]}\approx[A^+]_{sat}[B^-]_{sat}$  
  
- **solubilité** $s$ : quantité dissoute $[mol/L]$  
  
- $K_{S}=[A^{y+}]^x_{sat}[B^{x+}]^y_{sat}=(xs)^x(ys)^y$  → $s=^{x+y}\sqrt{\frac{K_{s}}{x^xy^y}  }$  
	- avec réaction : $A_{x}B_{y}(s)\to xA^{y+}+yB^{x-}$  
  
- précipitation (devient solide) $\iff Q_{s}>K_{s}$  
  
- Effet *ions communs* : début : $[A]=c$ ⇒ $K_{s}=(xs+c)^x(ys)^y$  
	- on considère $c \gg xs$ ⇒$Ks\approx c^xy^ys^y$  
  
- *Effet du pH* : $s=\sqrt{ K_{s}(1+K_{b}[H_{3}O^+])}$   
