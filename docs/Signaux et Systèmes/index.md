---  
share: true  
category: Signaux et Systèmes  
tags:  
  - regrouping  
title: Signaux et systèmes  
created: 2024-02-12  
updated: 2024-06-17  
---  
pas complet …  
&nbsp;  
  
- **Convolution** : $x*y=\sum_{k}^{\infty} x[k]y[n-k]{}$  
	- $x(t)*h(t)=\int_{-oo}^\infty x(\tau)h(t-\tau) \, d\tau{}$  
# Signaux  
  
- *pair* / *impair* : → somme de s pair et impair : $x(t)=x_{p}(t)+x_{i}(t){}$ :   
  
- *périodique* : $x(t)=x(t+T){}$ avec $\omega=\frac{2\pi}{T}{}$  (discret : $x[n+N]{}$ et $\Omega=\frac{2\pi}{N}{}$)  
  
- *déterministe* / *aléatoire* : peut le prédire  
  
- *Energie* : $E=\int_{-\infty}^{\infty} x^{2}(t) \, dt{}$  
  
- *Puissance* : $P=\lim_{ T \to \infty } \frac{1}{T}\int_{-T /2}^{T/2} x^{2}(t) \, dt{}$  
  
| Si. élémentaires | Continu $x(t){}$                              | Discret $x[n]{}$                       |  
| ---------------- | --------------------------------------------- | -------------------------------------- |  
| **impulsion**    | delta *Dirac*                                 | delta *Kronecker*                      |  
| def              | $\delta(t)=\{t=0:  \infty  , 0\}$             | $\delta[n]=\{n=0:  1  , 0\}$           |  
| multiplication   | $f(t)\delta(t-a)=f(a)\delta(t-a){}$           | $f[n]\delta[n-a]=f[a]\delta[n-a]{}$    |  
| intégration      | $\int_{-\infty}^{\infty} \delta(t) \, dt=1{}$ | $\sum_{-\infty}^{\infty}\delta[n]=1{}$ |  
| convolution      | $f(t)*\delta(t-a)=f(t-a){}$                   | $f[n]*\delta[n-a]=f[n-a]{}$            |  
| **Echelon**      | $u(t-a)=\{ 1:t\geq a, 0 \}{}$                 | $u[n-a]=\{ 1:n\geq a,0 \}{}$           |  
| → delta          | $\delta(t)=\frac{ d }{ dt }u(t){}$            | $\delta[n]=u[n]-u[n-1]{}$              |  
| **Rampe**        | $r(t-a)=\{ t:t\geq a, 0 \}{}$                 | $r(n-a)=\{ n:t\geq a ,0\}{}$           |  
| → echelon        | $r(t)=tu(t){}$                                | $r[n]=n u(n){}$                        |    
    
→ somme d'impulsion : $x(t)=\int_{-\infty}^{\infty} x(s)\delta(t-s) \, ds{}$  
# Systemes $\mathcal{H}\{ x(t) \}=y(t){}:signal\to signal$  
  
- Systeme **LIT**: *Linéaire a temps invariant*(LTi) :    
	- *invariance temporelle* : sortie ne varie pas si entrée retardé  
		- $\mathcal{H}\{ x \}[n]=y[n]\implies \mathcal{H}\{ x \}[n-a]=y[n-a]{}$  
	- *linéaire* : $\mathcal{H}\{ax+by\}=a\mathcal{H}\{ x \}+b\mathcal{H}\{ y \}$   
&nbsp;  
  
- *sans mémoire* : $y(t)=cx(t)\implies h[n]=c\delta[n]{}$  
  
- *causal* : depend pas des valeurs futures : $h[n]=0\quad\forall n<0{}$   
  
- *inversible* : $\exists h^{-1}:h^{-1}*h=\delta{}$  
&nbsp;  
  
- **réponse indicielle** : $s(t):=h(t)*u(t){}$ →  $h(t)=\frac{ds(t)}{dt}{}$   
  
- *interconnection* :$H_{1}\{ H_{2}\{  \} \}:h_{1}(t)+h_{2}(t){}$et $H_{1}\{  \}+H_{2}\{  \}:h_{1}(t)*h_{2}(t){}$  
&nbsp;  
representation S LIT  
  
- **reponse impulsinnelle** : $h(t)=H\{ \delta(t) \}{}$  → $y[k]=x[k]*h[k]{}$  
  
- **Schéma Bloc** : …  
  
- **eq diff entrée sortie** : …  
  
- **repr. d'état** : …  
# [Transformées](Transform%C3%A9es.md)  
&nbsp;  
# Fonction de transfert  
  
- **fonction de tansfert** : $H(z)=\sum_{-\infty}^{\infty}h[k]z^{-n}{}$  
	- image de $x[n]\to X(z)\to Y(z)=X(z)H(z)\to y(n){}$  
	- $G(z)=\mathcal{L}\{ g(s) \}{}$  
  
- **diagramme de bode** : graphe (echelle log): $\omega\to 20\log_{10}(|H(j\omega)|){}$  
	- CONSTRUCTION :  $H=K \frac{\left( \frac{j\omega}{\omega_{0}} \right)\left( \frac{j\omega}{\omega_{1}} +1\right)\left( \frac{j\omega}{\omega_{2}}^{2}+2\xi \frac{j\omega}{\omega_{2}}+1\right)}{\left( \frac{j\omega}{\omega_{3}} \right)\left( \frac{j\omega}{\omega_{4}} +1\right)\left( \frac{j\omega}{\omega_{5}}^{2}+2\xi \frac{j\omega}{\omega_{5}}+1\right)}{}$  
	- → $20\log(jw)\to {}$ pente 20db / décade  
	- $\log(j\omega+1)\to 0 : \omega\leq 1  {}$   
  
| terme                                                                | amplitude                                                                                                                                                                                    | Phase                                                                                                                                             |  
| -------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |  
| $K{}$                                                                | $20\log_{10}(K){}$                                                                                                                                                                           | $0: K>0; \pm \pi:K<0{}$                                                                                                                           |  
| $\frac{j\omega}{\omega_{i}}{}$                                       | $20\log\left( \frac{\omega}{\omega_{0}} \right){}$                                                                                                                                           | $\frac{\pi}{2}{}$                                                                                                                                 |  
| $\frac{j\omega}{\omega_{i}}+1$                                       | $\left\{\begin{aligned} 0 :\omega\ll\omega_{i}\\ 20\log \sqrt{ 2 } \approx 3 : \omega=\omega_{i}\\20\log\left( \frac{\omega}{\omega_{i}} \right):\omega\gg\omega_{i} \end{aligned}\right.{}$ | $\left\{\begin{aligned} 0 &:\omega\ll\omega_{i}\\ \frac{\pi}{4} &: \omega=\omega_{i}\\ \frac{\pi}{2}&:\omega\gg\omega_{i} \end{aligned}\right.{}$ |  
| $\frac{j\omega}{\omega_{i}}^{2}+2\xi \frac{j\omega}{\omega_{i}}+1{}$ | $\left\{\begin{aligned} 0 :\omega\ll\omega_{i}\\ 20\log  (2\xi ) \approx 3 : \omega=\omega_{i}\\40\log\left( \frac{\omega}{\omega_{i}} \right):\omega\gg\omega_{i} \end{aligned}\right.{}$   | $\left\{\begin{aligned} 0 &:\omega\ll\omega_{i}\\ \frac{\pi}{2} &: \omega=\omega_{i}\\ \pi&:\omega\gg\omega_{i} \end{aligned}\right.{}$           |    
    
  
- **Schéma-bloc** :entrée $x{}$, sortie $y{}$, états internes $q_{i}{}$  
	- $\forall i:I_{i}=0{}$  
	- etat : $q'(t)=Aq(t)+Bx(t){}$ et $y(t)=Cq(t)+Dx(t){}$  
	- fct de transfert : $H(s)=\frac{Y(s)}{X(s)}=C(sI-A)^{-1}B+D{}$  
		- $C(sI-A)^{-1}=\frac{Ccof(zI-A)B}{\det(zI-A)}{}$  
  
- ch de var interne : $Tq=\tilde{q}=TAT^{-1}\tilde{q}+TBx{}$ et $y=CT^{-1}\tilde{q}+Dx{}$  
&nbsp;  
# Commandabilité  
  
- $x^*{}$ *atteignable* : $\exists T:x[T]=x^*{}$ avec $x[0]=0{}$   
  
- soit $y[n]=cx[n]{}$ et $x[n+1]=Ax[n]+bu[n]{}$  
	- *matrice de commandabilité* : $\mathcal{C}(A,b)=(A^{d-1}b \dots Ab \; b){}$   
	- *matrice d'observabilité* : $\mathcal{O}(A,c)=(c \dots cA^{n-1}){}$   
  
- systeme **commandable** : tt etat atteignable ( $\forall x^*{}$ )   
	- $\iff C {}$ de rang plein $\iff \det(C)\neq 0{}$  
  
- $\bar{q}{}$ *accessible* : $q(0)=0, \exists T:q(T)=\bar{q}{}$  
  
- *non-observable* :$\forall T>0:x(t)=0\quad\forall t\in [0,T]$ ⇒ $y(t)=0 \quad\forall t\in [0,T] {}$  
	- S *observable* (aucun état non-observable) :   
		- observation finie de la sortie → determine état initial  
	- *entirement observable* : $\mathcal{O}{}$ de plein rang  
	- ker de $\mathcal{O}(A,C)=(C \dots CA^{n-1}){}$   
# Stabilité  
  
- *BIBO Stable*(Bounded input B. output) : entrée bornée ⇒ sortie bornée  
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
