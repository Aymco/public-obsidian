---  
tags:  
  - matière  
created: 2023-12-22  
updated: 2023-12-30  
---  
  
onde originale : onde incidente $\vec{k}_{1}$, angle incidence $\theta_{1}$  
![[../../Excalidraw/shéma réfraction|shéma réfraction]]  
## Réflexion  
angle **réfléchi** $\theta_{r}=\theta_{1}$  
## Réfraction  
  
- Conservation composantes tangentielles à l’interface de 2 milieux  
angle **réfracté** $\theta_{2}$  **loi de Snell-Descartes** :   
$$  
n_1 sin(\theta_1)=n_2 sin(\theta_2)  
$$  
Indice de réfraction $n = \sqrt{ \epsilon_{r}\mu_{r} }$   
	($n_{eau}=1,0008$, $n_{vide}=1$, $n_{verre}=1,4-1,7$)  
## **Angle critique** $\theta_{c}$ : $\sin\theta_{c}=\frac{n_{1}}{n_{2}}$  
$\theta_{1}>\theta_{c}$ → ! réfraction   
## Lois de Fresnel  
champ électrique de l'onde incidente : $E_{1}=E_{\parallel}+E_{\perp}$  
avec $E_{\parallel},E_{\perp} \perp \vec{k}_{1}$ et $E_{\parallel}$ compris dans le plan d'incidence($H=E\sqrt{ \frac{\epsilon}{\mu} } (\vec{k}\times \vec{E})$)  
$$  
\begin{align}  
\vec{E}_{r\parallel}=\frac{{Z_{2}\cos(\theta_{2})-Z_{1}\cos(\theta_{1})}}{{Z_{2}\cos(\theta_{2})+Z_{1}\cos(\theta_{1})}}\vec{E}_{1\parallel}\\  
\vec{E}_{r\perp}=\frac{{Z_{2}\cos(\theta_{1})-Z_{1}\cos(\theta_{2})}}{{Z_{2}\cos(\theta_{1})+Z_{1}\cos(\theta_{2})}}\vec{E}_{1\perp}\\  
\vec{E}_{2\parallel}=\frac{{2Z_{2}\cos(\theta_{1})}}{{Z_{2}\cos(\theta_{2})+Z_{1}\cos(\theta_{1})}}\vec{E}_{1\parallel}\\  
\vec{E}_{2\perp}=\frac{{2Z_{2}\cos(\theta_{1})}}{{Z_{2}\cos(\theta_{1})+Z_{1}\cos(\theta_{2})}}\vec{E}_{1\perp}  
\end{align}  
$$  
## **Angle De Brewster**  
l’angle pour lequel la reflexion de l’onde polarisée $\parallel$ au plan d’incidence s’annule  
  
- rayon réfléchi est perpendiculaire au rayon réfracté $\tan(\theta_1)= \frac{n_2}{n_{1}}$  
## [[../spécifiques/Ondes mécaniques|Ondes mécaniques]] Ex  
  
- la masse d'une corde change au delà  d'un certain point  
  
- onde sonore qui arrive dans un nuage de gaz plus lourd  
  
# Interférences **constructive** / **destructrice**  
sources de meme fréquence  
### Sources de meme phase  
2 sources $E_{P}=A\cos(kr_{1}-\omega t)+A\cos(kr_{2}-\omega t)$ $=2A\cos\left( {\frac{\phi}{2}}  \right)\cos\left( \frac{k(r_{1}+r_{2})}{2}-\omega t \right)$  
**déphasage angulaire** $\phi=2\pi {\frac{r_{1}-r_{2}}{\lambda}}$  
  
- 1er terme : forme **hyperbolique**  
  
- 2eme terme : forme **elliptique**  
  
- L’amplitude est modulée spatialement par $\cos\left( \frac{\phi}{2} \right)$  
  
- $\phi$ → interférences constructives / destructives   
  
- Intensité : $I = 4A^{2}\cos^{2}\left( \frac{\phi}{2} \right)$  
  
- Lignes nodales : $I = 0$  
  
- Lignes ventrales/anti-nodales : $I = 4A^{2}$  
  
- Utilité : diriger énergie vers certaines régions de l’espace $\lambda$  
## Sources déphasées de $\phi'$  
déphasage total : $\phi(P)=\underbrace{ 2\pi \frac{(r_{2}-r_{1})}{\lambda} }_{ \phi  \text{ "naturel"} }+\phi'$  
## Cas : duo de fentes  
approximation de Fraunhofer :$r_{1}-r_{2}=d\sin(\theta)$ avec $d$ la distance entre les fentes  
	⇒ $\phi=\frac{2\pi d}{\lambda}\sin(\theta_{1})$   
$\phi=\frac{2\pi d}{\lambda}(\sin(\theta_{1})+\sin(\alpha))$ avec $\alpha$ l'angle du point $P$  
	→ maximiser/minimiser pour trouver les points  
## Réseau de fentes  
on remplace le cos par une exponentielle :   
$E_{P}(t)=\sum_{p=1}^{N}A\cos(kr_{i}-\omega t)=\sum_{p=1}^{N}Ae^{kr_{i}-\omega t}$  
#todo   
# Diffraction  
fente approximée par $N$ fentes idéales : [[./ondes#principe de Huygens|ondes > principe de Huygens]]  
l'épaisseur de la fente : $a=Nd$, amplitude d'une source  $A_{i}=\frac{A}{N}$  
en prenant $N\to \infty$ : intensité : $I(P)=I_{0} \frac{\sin^{2}\left( \frac{a\pi \sin(\theta)}{\lambda} \right)}{\left( \frac{\pi a\sin(\theta)}{\lambda} \right)^{2}}$  
*principe de Banbinet* : meme figure de diffraction pour objet et trou de mm taille  
## Instrument d'optique  
résolution : dist/angle min pour différentier 2 points : $\theta_{i}>\theta_{1}$ :  
  
- fente rectangulaire : $\Delta \sin(\theta_{i})=\frac{\lambda}{a}$  
  
- fente circulaire : $\Delta \sin(\theta_{i})=\frac{1,22\lambda}{a}$  
# Effet doppler  
$$  
f_o=\frac{{v-v_o}}{{v-v_{s}}}f_{s}  
$$  
$o$ : observateur, $s$ : source, $v$ vitesse de propagation de l'onde  
vitesse dans le sens $s\to o$  
## Cas relativiste : $v_{s} \to c$  
$f_{o}=\sqrt{ \frac{{c+v_{s}}}{c-v_{s}}} f_{s}$  
