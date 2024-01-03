---  
share: true  
category: Chimie 2  
tags:  
  - matière  
created: 2023-11-20  
updated: 2024-01-03  
---  
  
[Thermodynamique](Thermodynamique.md) → controle la composition  
  
  
- Energie libre de *Helmotz*     : $A=U-TS$  
  
- Enthalpie/Energie libre de *Gibbs*  $G = H-TS$  
	- $dG = dU + p dV + V dp − T dS − S dT$   
	- $p,T$ cst ⇒ $dG_{p,T} = dH − T dS$   
  
- seul travail $pdV$ ⇒ $dG_{p,T}< 0$ , équilibre $dG_{p,T}=0$  
  
- équilibre *métastable* : nécessite $E_{a}$ → + stable  
## Équations fondamentales d'un système de composition fixée :  
  
  
$$  
\begin{aligned}  
dH&=TdS+Vdp\\  
dA&=-SdT-pdV\\  
dG&=-SdT+Vdp\\  
dU&=Tds-pdV  
\end{aligned}  
  
  
$$  
## Variation de l'enthalpie avec la pression  
  
- $G_{m}(p,T)=G^o_{m}(T)+\int_{p^o}^{p}  V_{m}(p',T)\, dp'$  
  
- gaz parfait ⇒ $=G^o_{m}(T)+RT\ln\left( \frac{p}{p^o} \right)$ (solide + liquide + gaz → gaz)  
  
- solide / liquide  $=G^o_{m}(T)+ V_{m} \Delta p$  
# Potentiel chimique  
  
- **potentiel chimique** : $\mu_{i}$ (grandeur intensive) pour chaque espèce  
	- $\mu_{i}=\left( \frac{ \partial G }{ \partial n_{i} } \right)_{T,p,n_{i\neq j}}\equiv G_{m,i}$ **énergie libre molaire partielle**  
	- **potentiel pur** : $\mu^i=\mu^{i^o}+RT\ln\frac{p}{p^o}= G^A_{m}$ **énergie libre molaire**  
  
- tout $A$ migre vers l'endroit ou $\mu_{i}$ est le plus faible  
  
  
  
- système a composantes multiples $dG=-SdT+Vdp+\sum \mu_{i}dn_{i}$  
# Enthalpie libre standard et affinité chimique  
  
## Enthalpie libre standard  
quotien réactionnel : $Q^o_{r}=\Delta_{r}H^o=\sum_{P}\chi_{P} H^{P^o}-\sum_{R}\chi_{R}H^{R^o}$  
	avec $\chi_{A}$ le coefficient stœchiométrique de $A$  
Energie libre standard de formation avec $G^{A^o}=H^{A^o}-TS^{A^o}$ :   
	$\Delta_{f}G^o=\sum_{P}\chi_{P} G^{P^o}-\sum_{R}\chi_{R}G^{R^o}$  
  
  
- **Entropie standard de réaction** $\Delta_{r}S^o:=\sum v_{i}S_{m}^{i^o}$  
  
- **Enthalpie standard de réaction** $\Delta_{r}H^o:=\sum v_{i}H_{m}^{i^o}$  
  
- **énergie libre standard de réaction** : $\Delta_{r}G^o=\Delta_{r}H^o-T\Delta_{r}S^o$  
  
- **Avancement d'une réaction** :  $d\xi=\frac{dn_{P}}{\chi_{P}}=-\frac{dn_{R}}{\chi_{R}}=[mol]$  
  
- **énergie libre de réaction** : $\Delta_{r}G=\sum v_{i}\mu_{i}$   
	- $\Delta_{r}G<0$ évolution spontanée → $\Delta_{r}G=0$  
  
  
- **Affinité chimique** : $\mathcal{A}:=-\Delta_{r}\mu=-\left( \frac{ \partial G }{ \partial \xi } \right)_{T,p}=\sum_{R}\chi_{R}\mu_{R}-\sum_{P}\chi_{P}\mu_{P}$  
	- $dG=Vdp+SdT-\mathcal{A}d\xi<0$  
	- réaction à l'équilibre : $\mathcal{A}=0$  
  
# Équilibre chimique entre [gaz parfait](gaz%20parfait.md)  
  
- loi de Dalton : $p_{i}=x_{i}p$  
  
- **fraction molaire** : $x_i:=\frac{n_{i}}{n}=\frac{p_{i}}{p}$  
  
- potentiels chimiques : $\mu_{i}=G^{i^o}_{m}+RT\ln \frac{p_{i}}{p^o}$  
  
- affinité chimique$-\mathcal{A}=\Delta_{r}G^\circ+RT\left( \sum_{P}\chi_{P}\ln \frac{p_{P}}{p^o}- \sum_{R}\chi_{R}\ln \frac{p_{R}}{p^o} \right)$  
## Quotient réactionnel $Q=\frac{\prod_{P}\left( a_{P} \right)^{\chi_{P}}}{\prod_{R}\left( a_{R} \right)^{\chi_{R}}}$  
  
- à l'équilibre ⇒ $\Delta_{r}G^o=-RT\ln(K)$ avec  $Q_{eq}=K$  
lien entre les constantes d'équilibres :   
$K_{p}=K_{x}\left( \frac{p}{p^o} \right)^{\Delta\chi}=K_{n}\left( \frac{p}{p^o\sum n_{i}} \right)^{\Delta\chi}$ avec $\Delta\chi=\sum_{P}\chi_{P}-\sum_{R}\chi_{R}$  
  
- *équation de van't Hoff* : $\frac{d(\ln K_{p})}{dT}=\frac{\Delta_{r}H^o}{RT^{2}}$  
	- ⇒ $\ln K_{p,T_{2}}-\ln K_{p, T_{1}}=\frac{\Delta_{r}H^\circ}{R}\left( \frac{1}{T_{2}}-\frac{1}{T_{1}} \right)$  
# Équilibre chimique en solution liquide  
  
- **activité** $a_{i}$ :   
	- mélange idéal ⇒ $a_{i}=\frac{p_{i}}{p^o}$  
	- $a_{i}=\gamma_{i}x_{i}$ avec  $\gamma_{i}<1$ ⇒stable   
	- espèce en solution diluée $a_{A}=\frac{m_{A}}{m^o_{A}}$  
  
- Potentiel chimique :  $\mu_{A}=\mu^{A^\circ}+RT\ln a_{i}$  
  
- $\Delta_{r}G=\Delta_{r}G^o +RT\ln Q$  
## Dissolution  
  
- **produit de solubilité** $K_{s}=\frac{[A^+]_{sat}[B^-]_{sat}}{[AB]}\approx[A^+]_{sat}[B^-]_{sat}$  
  
- **solubilité** $s$ : quantité dissoute $[mol/L]$  
  
- $K_{S}=[A^{y+}]^x_{sat}[B^{x+}]^y_{sat}=(xs)^x(ys)^y$  → $s=^{x+y}\sqrt{\frac{K_{s}}{x^xy^y}  }$  
	- avec réaction : $A_{x}B_{y}(s)\to xA^{y+}+yB^{x-}$  
  
- précipitation (devient solide) $\iff Q_{s}>K_{s}$  
  
- Effet *ions communs* : début : $[A]=c$ ⇒ $K_{s}=(xs+c)^x(ys)^y$  
	- on considère $c \gg xs$ ⇒$Ks\approx c^xy^ys^y$  
  
- *Effet du pH* : $s=\sqrt{ K_{s}(1+K_{b}[H_{3}O^+])}$   
