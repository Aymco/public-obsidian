---  
share: true  
category: Physique 3  
tags:  
  - matière  
created: 2023-12-23  
updated: 2024-01-02  
---  
  
  
- électromagnétique   
  
- sonores   
  
rayonnement électromagnétique = champ électromagnétique rayonné  
	source : charge accélérée  
# Antenne Modélisation  
champ de polarisation *circulaire* : 2 linéaires $\perp$ et déphasés  
## Dipôle oscillant  
de charge $q$ dont la position de + est : $z_{p}(t)=z_{0}\sin(\omega t) \hat{z}$, $\vec{r}$ particule → $P$   
$a_{\perp}$ composante de $a$ perpendiculaire à $\vec{r}$  
  
- rayonnement EM isotrope, propa sphérique, $i=\frac{1}{4\pi r^{2}}$  
  
- Onde arrivant sur $P$ au tps $t$ dépend du rayonnement au temps : $t'=t-\frac{\vec{|r|}}{c}$  
  
- champ électrique perçu : $\vec{E}=-\frac{\mu q}{4\pi r}a_{\perp}t'$   
	avec $c$ vitesse de la lumière dans le milieu (incorrect mais approxime correctement)  
énergie transportée : $P_{moy}=\frac{\mu_{0}^{2}}{12\pi}\sqrt{ \frac{\epsilon_{0}}{\mu_{0}} }\omega^4p_{0}^{2}$  
## Micro antenne  
taille $h\ll \lambda$ : déphasage nul  
courant alternatif : $I(t)=I_{0}\cos(\omega t)$  
$I(t)=\frac{dq}{dt}\iff I_{0}dz=\omega z_{0}dq$ en utilisant $z(t)=z_{0}\sin(\omega t) \hat{z}$  
on intègre : $hI_{0}=\omega z_{0}\Delta q=\omega p_{0}$  
→ $E_{\theta}=-\frac{1}{2}\sqrt{ \frac{\mu_{0}}{\epsilon_{0}} }I_{0}{\frac{h\sin(\theta)}{\lambda r}\sin(\omega t-kr)}$ en approximant $r$  
énergie transportée : $P_{moy}=\frac{\pi}{3}\sqrt{ \frac{\epsilon_{0}}{\mu_{0}} }\left( \frac{h}{\lambda} \right)^{2}I_{0}$  
## Macro antenne  
$dE_{\theta}=-\frac{1}{2}\sqrt{ \frac{\mu_{0}}{\epsilon_{0}} }I_{0}{\frac{dz\sin(\theta)}{\lambda r}\sin(\omega t-k(r-z\cos(\theta)))}$ d micro ondes  
→ complexes → intègre $\int_{-h}^{h}  \, dz$  
→ isole imaginaires: $E_{\theta}=-\frac{I_{0}}{2\pi r}\sqrt{ \frac{\mu_{0}}{\epsilon_{0}} }\tan(\theta)\sin(\omega t-kr)\sin(kh\cos\theta)$  
énergie transportée : $P_{moy}=\frac{1}{4\pi}\sqrt{ \frac{\epsilon_{0}}{\mu_{0}} }I_{0}^{2}\int_{0}^{\pi} \frac{\sin^3\theta}{\cos ^{2}\theta}\sin^2(kh\cos\theta) \, d\theta$  
