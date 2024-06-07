---  
share: true  
category: Signaux et Systèmes  
tags:  
  - regrouping  
title: Signaux et systèmes  
created: 2024-02-12  
updated: 2024-06-06  
---  
# Signaux  
  
- delta *Dirac* : $\delta(t)=\{t=0:  \infty  , 0\}$ (t continu)  
	- $f(t)\delta(t-a)=f(a)\delta(t-a){}$  
	- $\int_{-\infty}^{\infty} \delta(t) \, dt=1{}$  
	- $f(t)*\delta(t-a)=f(t-a){}$  
  
- delta *Kronecker* : $\delta[n]=\{n=0:  1  , 0\}$ (t discret $:\mathbb{N}\to \mathbb{R}{}$)   
	- $f[n]\delta[n-a]=f[a]\delta[n-a]{}$  
	- $\sum_{-\infty}^{\infty}\delta[n]=1{}$  
	- $f[n]*\delta[n-a]=f[n-a]{}$  
  
- *pair* / *impair* (comme fct)  
  
- *périodique* : $x(t)=x(t+T){}$  
  
- *déterministe* / *aléatoire* : peut le prédire  
# Transformées de Fourier $\mathcal{F}\{ x \}{}$  
$jw=j2\pi f{}$ et $\Omega=\omega T_{s}{}$  
$T_{s}=\frac{2\pi}{T}{}$ période de discrétisation  
propiétés  
  
- $x\in  \mathbb{R}{}$ → $X \in \mathbb{R}{}$ pair, $\mathfrak{I}{}$ impaire  
  
- $x{}$ pair / impair → $X{}\in$ $\mathbb{R}{}$ et pair / $\mathfrak{I}{}$et impair  
  
- $x,y{}$ non périodiques : $\mathcal{F}\{ x*y \}=XY{}$  et  $\mathcal{F}\{ xy \}=\frac{X*Y}{2\pi}{}$  
  
- $x,y{}$ périodiques : $\mathcal{F}\{ x*y \}=T_{fondamentale}XY{}$  et $\mathcal{F}\{ xy \}=X*Y{}$  
  
- *Relation de Parseval* : $\int_{-\infty}^{\infty} |x(t)|^2 \, dt{}=\frac{1}{2\pi}\int_{-\infty}^{\infty} |X(j\omega)|^2 \, dt$  
## Transformé de Fourier continue - **FT**  
somme des vecteurs de fonction autour d'un cercle en variant la vitesse angulaire  
  
- $x(t)=\frac{1}{2\pi}\int_{-\infty}^{\infty} X(j\omega)e^{j\omega t} \, d\omega{}$  
  
- $X(j\omega)=\int_{-\infty}^{\infty} x(t)e^{-j\omega t} \, dt{}$ ( conv si $\int_{-\infty}^{\infty} |x(t)| \, dt<\infty{}$)  
## Transformé de Fourier temps discret - **DTFT**  
  
- $x[n]=\frac{1}{2\pi}\int_{-\pi}^{\pi} X(e^{j\Omega})e^{j\Omega n} \, d\Omega{}$  
  
- $X(e^{j\Omega})=\sum_{n=-\infty}^{\infty}x[n]e^{-j\Omega n}{}$ (conv si $\sum_{-\infty}^{\infty}|x[n]|<\infty{}$)  
avec $\Omega=\omega T_{s}{}$, $X{}$ période $\frac{2\pi}{T_{s}}{}$  
## Transformée de Fourier discrete - **DFT**  
  
- FT + échantillonnage en fréquentiel  
  
- *echantillonnage* = multiplier par $\sum_{-\infty}^{\infty}\delta(t-nT_{s}){}$ + filtre passe bas ($T_{s}{}$)  
	- $|\omega|>\omega_{max}\implies X(j\omega)=0{}$   
	- *théorème de shannon* :$f_{s}>2f_{max}{}$ ( $\frac{2\pi}{T_{s}}>2\omega_{max}{}$ ⇒ !chevauchement)  
	- $x_{s}{}$ périodique si $T_{s}{}$ multiple de $T{}$  
  
- échantillonnage $\frac{2\pi}{N}$ /N = FS : $X[k]=\frac{X(e^{jk2\pi/N})}{N}{}$  
# Serie de Fourier  
## Séries De Fourier - **FS**  
exponentielle coresspondante aussi de période $T{}$ avec $\omega_{0}=\frac{2\pi}{T}{}$,   
  
- $x\left( t\right)=\sum_{k=-\infty}^{\infty}X[k]e^{ek\omega_{0}t}{}$  
  
- $X[k]=\frac{1}{T}\int_{0}^{T} x(t)e^{-jk\omega_{0}t} \, dt{}$  
  
- divise par $T{}$ ($T\to \infty{}$ : FS=FT/T)  
  
- FS *répétition de deltas* : $x(t)=\sum_{-\infty}^{\infty}\delta(t-nT){}$⇒ $X[k]=\frac{1}{T}{}$⇒ $x(t)=\frac{1}{T}\sum_{-\infty}^{\infty}e^{2\pi jkt/T}{}$⇒$X(jw)=\frac{2\pi}{T}\sum_{-\infty}^{\infty}\delta\left( \omega-\frac{2\pi k}{T} \right){}$  
## Séries De Fourier Temps discret - **DTFS**  
  
- $x\left[ n\right]=\sum_{k=0}^{N-1}X[k]e^{ek\Omega_{0}n}{}$  
  
- $X[k]=\frac{1}{N}\sum_{n=0}^{N-1} x[n]e^{-jk\Omega_{0}n} {}$  
$x[n]{}$ de période $N{}$  
## Fast Fourier Transform - **FFT algo**  
  
- DTFS : $x[0:N-1]\to X[0:N-1]{}$ : $X[k]=\sum x[n]e^{-jk\Omega_{0}n} {}$  puis $/N{}$  
  
- *zéro padding* : ajouter $N-L{}$ zéro → augmenter la précision ($N{}$ puissance de 2)  
# Transformée de Laplace $\mathcal{L}\{ \}{}$  
  
- généralisation de FT : $s=\sigma+j\omega{}$  
  
- $X(s)=\int_{-\infty}^{\infty} x(\tau)e^{-s\tau} \, d\tau{}$   
  
- $x(t)=\frac{1}{2\pi}\int_{-\infty}^{\infty} X(\sigma+j\omega)e^{(\sigma+j\omega)t} \, d\omega{}$  
  
- existe TL pour des signaux sans FT  
  
- a une région de convergence *ROC*: $\int_{-\infty}^{\infty} |x(t)|e^{-\sigma t} \, <\infty{}$  
  
- **Unitlatérale** : $X_{u}(s)=\int_{0^-}^{\infty} x(\tau e^{-s\tau}) \, d\tau{}$  
	- #TODO  
# Transformée en $\mathcal{Z}{}$  
generalisation DFT  
  
- $X(z)=\sum_{-\infty}^{\infty}x[k]z^{-k}{}$  
  
- $x[n]=\frac{1}{2\pi}\int_{-\pi}^{\pi} X(\mathrm{re}^{j\omega}) (\mathrm{re}^{j\omega})^n\, d\omega=\frac{1}{2\pi j}\oint X(z)z^{n-1}\,dz{}$  
  
- *ROC* : $\sum_{-\infty}^{\infty}|x[n]r^{-n}|<\infty{}$  
  
- propiétés :  
	- #TODO  
  
- **Unilatérale** : $X_{u}(z)=\sum_{0}^{\infty}x[n]s^{-n}{}$  
&nbsp;  
# Propriétés  
|    propiétés continue     |              eq (continu)               |            $\mathcal{F}{}$            |                   $\mathcal{L}{}$                   |              $\mathcal{L}{}$ ROC               |  
| :-----------------------: | :-------------------------------------: | :-----------------------------------: | :-------------------------------------------------: | :--------------------------------------------: |  
|        *linéarité*        |                $ax+by{}$                |             $aX()+bY(){}$             |                   $aX(s)+bY(s){}$                   |         $R_{1}\cap R_{2}\subseteq R{}$         |  
|    *décalage temporel*    |             $x(t-t_{0}){}$              |   $e^{-j\omega t_{0}}X(j\omega){}$    |                 $e^{-st_{0}}X(s){}$                 |                     $R{}$                      |  
|    *décalage temporel*    |           $X(j(\omega-v)) {}$           |            $e^{jvt}x(t){}$            |                 $e^{s_{0}t}x(t){}$                  |        $R=R_{1}+\mathfrak{R}(s_{0}){}$         |  
| *ch echelle en temporel*  |                $x(at){}$                | $\frac{1}{\mid a\mid}X(j\omega /a){}$ | $\frac{1}{\mid a\mid}X\left( \frac{s}{a} \right){}$ |                  $R=aR_{1}{}$                  |  
|       *convolution*       |                 $x*y{}$                 |     $XY{}$($\cdot T{}$si périod )     |                       $XY{}$                        |         $R_{1}\cap R_{2}\subseteq R{}$         |  
|                           |                 $xy{}$                  |       $X*Y{}$($/2\pi{}$!périod)       |                                                     |                                                |  
|    *diff en temporel*     |        $\frac{ dx(t) }{ dt }{}$         |        $j\omega X(j\omega){}$         |                      $sX(s){}$                      |              $R_{1}\subseteq R{}$              |  
|   *diff en fréquentiel*   |   $\frac{ dX(j\omega) }{ d\omega }{}$   |              $jtx(t){}$               |                     $-tx(t){}$                      |                     $R{}$                      |  
| *intégration en temporel* | $\int_{-\infty}^{t} x(\tau) \, d\tau{}$ |                                       |                 $\frac{X(s)}{s}{}$                  | $R=$$R_{1}\cap \{  \mathfrak{R\{ s \}>0} \}{}$ |    
    
  
# Systemes $\mathcal{H}\{ x(t) \}=y(t){}$  
  
- Systeme **LTI**(LIT): *Linéaire a temps invariant* :    
	- *invariance temporelle* : sortie ne varie pas si entrée retardé  
	- *linéaire* : $\mathcal{H}(ax+by)=a\mathcal{H}(x)+b\mathcal{H}(y){}$   
  
- *sans mémoire* : $y(t)=cx(t)\implies h[n]=c\delta[n]{}$  
  
- *causal* : depend pas des valeurs futures : $h[n]=0\quad\forall n<0{}$   
  
- *inversible* : $\exists h^{-1}:h^{-1}*h=\delta{}$  
  
- **reponse impulsinnelle** : $h(t)=H\{ \delta(t) \}{}$  → $y[k]=x[k]*h[k]{}$  
  
- **réponse indicielle** : $s(t):=h(t)*u(t){}$ → $h(t)=\frac{ds(t)}{dt}{}$ ($S(z)=H(z)U(z){}$)  
  
- **Convolution** : $x*y=\sum_{k}^{\infty} x[n]y[k-n]{}$  
  
- *interconnection* :$H_{1}\{ H_{2}\{  \} \}:h_{1}(t)+h_{2}(t){}$et $H_{1}\{  \}+H_{2}\{  \}:h_{1}(t)*h_{2}(t){}$  
# Fonction de transfert  
  
- fonction de tansfert : $H(z)=\sum_{-\infty}^{\infty}h[k]z^{-n}{}$  
	- image de $x[n]\to X(z)\to Y(z)=X(z)H(z)\to y(n){}$  
  
- diagramme de bode : graphe $\omega\to 20\log(|H(j\omega)|){}$  
	- CONSTRUCTION :  $H=K \frac{\left( \frac{j\omega}{\omega_{0}} \right)\left( \frac{j\omega}{\omega_{1}} +1\right)\left( \frac{j\omega}{\omega_{2}}^{2}+2\xi \frac{j\omega}{\omega_{2}}+1\right)}{\left( \frac{j\omega}{\omega_{3}} \right)\left( \frac{j\omega}{\omega_{4}} +1\right)\left( \frac{j\omega}{\omega_{5}}^{2}+2\xi \frac{j\omega}{\omega_{5}}+1\right)}{}$  
  
| terme                                                                | amplitude                                                                                                                                                                                    | Phase                                                                                                                                             |  
| -------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |  
| $K{}$                                                                | $20\log_{10}(K){}$                                                                                                                                                                           | $0: K>0; \pm \pi:K<0{}$                                                                                                                           |  
| $\frac{j\omega}{\omega_{i}}{}$                                       | $20\log\left( \frac{\omega}{\omega_{0}} \right){}$                                                                                                                                           | $\frac{\pi}{2}{}$                                                                                                                                 |  
| $\frac{j\omega}{\omega_{i}}+1$                                       | $\left\{\begin{aligned} 0 :\omega\ll\omega_{0}\\ 20\log \sqrt{ 2 } \approx 3 : \omega=\omega_{0}\\20\log\left( \frac{\omega}{\omega_{0}} \right):\omega\gg\omega_{0} \end{aligned}\right.{}$ | $\left\{\begin{aligned} 0 &:\omega\ll\omega_{0}\\ \frac{\pi}{4} &: \omega=\omega_{0}\\ \frac{\pi}{2}&:\omega\gg\omega_{0} \end{aligned}\right.{}$ |  
| $\frac{j\omega}{\omega_{i}}^{2}+2\xi \frac{j\omega}{\omega_{i}}+1{}$ | $\left\{\begin{aligned} 0 :\omega\ll\omega_{0}\\ 20\log  (2\xi ) \approx 3 : \omega=\omega_{0}\\40\log\left( \frac{\omega}{\omega_{0}} \right):\omega\gg\omega_{0} \end{aligned}\right.{}$   | $\left\{\begin{aligned} 0 &:\omega\ll\omega_{0}\\ \frac{\pi}{2} &: \omega=\omega_{0}\\ \pi&:\omega\gg\omega_{0} \end{aligned}\right.{}$           |    
    
  
- **Schéma-bloc** :entrée $x{}$, sortie $y{}$, états internes $q_{i}{}$  
	- $\forall i:I_{i}=0{}$  
	- etat : $q'(t)=Aq(t)+Bx(t){}$ et $y(t)=Cq(t)+Dx(t){}$  
	- fct de transfert : $H(s)=\frac{Y(s)}{X(s)}=C(sI-A)^{-1}B+D{}$  
		- $C(sI-A)^{-1}=\frac{Ccof(zI-A)B}{\det(zI-A)}{}$  
  
- ch de var interne : $Tq=\tilde{q}=TAT^{-1}\tilde{q}+TBx{}$ et $y=CT^{-1}\tilde{q}+Dx{}$  
&nbsp;  
# Commandabilité  
  
- $q(0)=q_{0}{}$ *commandable* : $\exists T:q(T)=0{}$   
	- $\forall q_{i}{}$ →completement commandable , ker de (engendré par les colonnes)  
		- *matrice de commandabilité* : $\mathcal{C}(A,B)=(B \dots A^{n-1}B){}$   
  
- $\bar{q}{}$ *accessible* : $q(0)=0, \exists T:q(T)=\bar{q}{}$  
  
- *non-observable* :$\forall T>0:x(t)=0\quad\forall t\in [0,T]$ ⇒ $y(t)=0 \quad\forall t\in [0,T] {}$  
	- S *complètement observable* (aucun état non-observable) : ker de  
		- $\mathcal{O}(A,C)=(C \dots CA^{n-1}){}$  
# Stabilité  
  
- *BIBO Stable*(bounded input b. output) :   
	- $|x[n]|\leq M_{x}<\infty \;\;\forall n{}$ ⇒ $|y[n]|\leq M_{y}<\infty \;\;\forall n{}$  
	- $\iff LTI:\sum_{-\infty}^{\infty}|h[k]|<\infty{}$  
	- #TODO  
  
- *Stabilité interne* : $(\bar{q},\bar{x}){}$ point *équilibre* : $A\bar{q}+B\bar{x}=0{}$  
	- *stable* : + bruit ⇒ reste dans une marge  
	- *attractif* : +bruit ⇒ tasser a 0  
		- *asymptotiquement stable* : stable + attractif ($\forall i:\mathfrak{R}\{ \lambda _{i} \}<0,|\lambda_{i}|<1{}$)  
	- *systeme stable* : tt equilibre stables  
	- $\forall i:\mathfrak{R}\{ \lambda _{i} \}>0,|\lambda_{i}|>1{}$ ⇒ instable  
	- $\forall i:\mathfrak{R}\{ \lambda _{i} \}\leq0,|\lambda_{i}|\leq1{}$ :  
		- $\forall i : |\lambda_{i}|=1\implies m_{g}(\lambda_{i})=m_{a}(\lambda_{i}){}$ ⇒ marginalement stable  
		- $\exists i : |\lambda_{i}|=1\implies m_{g}(\lambda_{i})=m_{a}(\lambda_{i}){}$ ⇒ instable  
		- #TODO  
