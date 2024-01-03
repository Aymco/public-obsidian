---  
share: true  
category: Chimie 2  
tags:  
  - matière  
created: 2023-11-20  
updated: 2024-01-03  
---  
  
[Thermodynamique](Thermodynamique.md) → controle la composition  
Energie libre de Helmotz     : $A=U-TS$  
Enthalpie/Energie libre de Gibbs  $G = H-TS$  
$dG = dU + p dV + V dp − T dS − S dT$  
transformation isotherme et isobare :   
	$dG\leq \delta W+pdV$  
## Équations fondamentales d'un système de composition fixée :  
  
  
$$  
\begin{align}  
dH&=TdS+Vdp\\  
dA&=-SdT-pdV\\  
dG&=-SdT+Vdp\\  
dU&=Tds-pdV  
\end{align}  
  
  
$$  
## Variation de l'enthalpie avec la pression  
$G_{m}(p,T)=G^o_{m}(T)+\int_{p^o}^{p}  V_{m}(p',T)\, dp'$  
gaz parfait : $=G^o_{m}(T)+RT\ln\left( \frac{p}{p^o} \right)$  
solide / liquide : $=G^o_{m}(T)+ V_{m} \Delta p$  
solide/liquide + gaz : considère que le gaz : $\approx RT\ln \frac{p}{p^o}$  
# Potentiel chimique  
composition change :  
**potentiel chimique** : $\mu_{i}$ (grandeur intensive)  
$\mu_{i}:=\left( \frac{ \partial G }{ \partial n_{i} } \right)_{T,p,n_{i\neq j}}=\left( \frac{ \partial U }{ \partial n_{i} } \right)_{S,v,n_{i\neq j}}=\left( \frac{ \partial H }{ \partial n_{i} } \right)_{S,p,n_{i\neq j}}=\left( \frac{ \partial A }{ \partial n_{i} } \right)_{T,V,n_{i\neq j}}$  
équation fondamentale de G : $dG=-SdT+Vdp+\sum \mu_{i}dn_{i}$  
forme pure : $G^A_{m}:=\mu^A$  
gaz parfait pur : $\mu^A=G^{A^o}_{m}+RT\ln\left( \frac{p}{p^o} \right)$  
**fraction molaire** de $A$ : $x_A:=\frac{n_{A}}{\sum n_{i}}$  
tout $A$ migre vers l'endroit ou son potentiel chimique est le plus faible  
# Enthalpie libre standard et affinité chimique  
  
## Enthalpie libre standard  
$Q^o_{r}=\Delta_{r}H^o=\sum_{P}\chi_{P} H^{P^o}-\sum_{R}\chi_{R}H^{R^o}$  
avec $\chi_{A}$ le coefficient stœchiométrique de $A$  
enthalpie libre de Gibbs standard de formation avec $G^{A^o}=H^{A^o}-TS^{A^o}$ :   
$\Delta_{f}G^o=\sum_{P}\chi_{P} G^{P^o}-\sum_{R}\chi_{R}G^{R^o}$  
enthalpie libre de Gibbs standard de réaction : $\Delta_{r}G^o=\Delta_{r}H^o-T\Delta_{r}S^o$  
**Avancement d'une réaction** :  $d\xi=\frac{dn_{P}}{\chi_{P}}=-\frac{dn_{R}}{\chi_{R}}=[mol]$  
## Affinité chimique $\mathcal{A}$  
$\mathcal{A}=-\left( \frac{ \partial G }{ \partial \xi } \right)_{T,p}=\sum_{R}\chi_{R}\mu_{R}-\sum_{P}\chi_{P}\mu_{P}=-\Delta_{r}\mu$  
$dG=Vdp+SdT-\mathcal{A}d\xi<0$  
réaction à l'équilibre : $\mathcal{A}=0$  
  
# Équilibre chimie entre [gaz parfait](gaz%20parfait.md)  
loi de Dalton : $p_{i}=x_{i}p$  
potentiels chimiques : $\mu_{i}=G^{i^o}_{m}+RT\ln \frac{p_{i}}{p^o}$  
affinité chimique : $-\mathcal{A}=\Delta_{r}G^o+RT\left( \sum_{P}\chi_{P}\ln \frac{p_{P}}{p^o}- \sum_{R}\chi_{R}\ln \frac{p_{R}}{p^o} \right)$  
## Quotient réactionnel  
$Q_{p}=\frac{\prod_{P}\left( \frac{p_{P}}{p^o} \right)^{\chi_{P}}}{\prod_{R}\left( \frac{p_{R}}{p^o} \right)^{\chi_{R}}}$ (indice p : calculé depuis pressions partielles)  
à l'équilibre : $Q_{p}=K_{p}$ → $\Delta_{r}G^o=-RT\ln(K_{p})$  
lien entre les constantes d'équilibres :   
$K_{p}=K_{x}\left( \frac{p}{p^o} \right)^{\Delta\chi}=K_{n}\left( \frac{p}{p^o\sum n_{i}} \right)^{\Delta\chi}$ avec $\Delta\chi=\sum_{P}\chi_{P}-\sum_{R}\chi_{R}$  
### Évolution avec la température  
équation de van't Hoff : $\frac{d(\ln K_{p})}{dT}=\frac{\Delta_{r}H^o}{RT^{2}}$  
  
# Équilibre chimique en solution liquide  
Potentiel chimique : $\mu_{A}=\mu^{A^o}+RT\ln a_{A}$  
avec $a_{A}$ l'activité de $A$ ( gaz parfait : $a_{A}=\frac{p_{A}}{p^o}$)  
→ espèce en solution diluée $a_{A}=\frac{m_{A}}{m^o_{A}}$  
**produit de solubilité** $K_{s}=\frac{[A^+]_{sat}[B^-]_{sat}}{[AB]}\approx[A^+]_{sat}[B^-]_{sat}$  
**solubilité** $s$ : quantité dissoute $[mol/L]$  
réaction : $A_{x}B_{y}(s)\to xA^{y+}+yB^{x-}$  
$K_{S}=[A^{y+}]^x_{sat}[B^{x+}]^y_{sat}=(xs)^x(ys)^y$  → $s=^{x+y}\sqrt{\frac{K_{s}}{x^xy^y}  }$  
précipitation (devient solide) $\iff Q_{s}>K_{s}$  
## Effet ions communs  
début : $[A]=c$  
$K_{s}=[A^{y+}]^x_{sat}[B^{x+}]^y_{sat}=(xs+c)^x(ys)^y$  
on considère $c \gg xs$ →$Ks\approx c^xy^ys^y$  
## Effet du pH  
  
# Réaction d'oxydo-réduction - rédox  
**degré d'oxydation**  :   
  
- $0$ : élément pu  
  
- charge de l'ion monomatomique  
  
- $1$ Alcalin  
  
- $-1$ Fluor  
  
- $2$ Alcalino-terreux + Zn, Cd  
  
- $1$ hydrogène lié à un non-métal  
  
- $-1$ hydrogène lia à un métal  
  
- $-2$ oxygène (sauf les peroxydes →$-1$)  
oxydation : perte d’électrons, degré augmente  
réduction : gain d'électrons,  degré diminue  
oxydant    : accepte des électrons, se réduit  
réducteur : donne des électrons,  s'oxyde  
  
# Piles électrochimiques  
oxydation : anode  
réduction : cathode  
fourni de l'énergie : dessine anode - cathode  
