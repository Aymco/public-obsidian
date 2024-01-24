---  
share: true  
category: MDP  
created: 2023-12-16  
updated: 2024-01-24  
title: Probabilités  
---  
  
[Combinatoires - dénombrements](Combinatoires%20-%20d%C3%A9nombrements.md)  
  
  
- *Axiomes de Kolmogorov*   
	1. $P(A)\in[0,1]$  
	2. $P(\Omega)=1$  
	3. $P(A\cup B)=P(A)+P(B)$ (disjoints)  
  
- proba d'*Union* : $P(A\cup B)=P(A)+P(B)-P(A\cap B)$  
  
- Probabilités *conditionnelles* : $P(A|B)=\frac{P(A\cap B)}{P(B)}$ A sachant(corrigé par)B  
	- $A\perp\!\!\!\perp B\iff P(B|A)=P(B)\iff P(A|B)=P(A)$  
	- *théorème de Bayès* : $P(A|B)=\frac{P(A)}{P(B)}P(B|A)$  
  
- Inférences statistiques : $p$ proba de réussite, $b$ réussites, $n$ épreuves  
	- *succession de Laplace* (*Bayèsienne*) $p\approx \frac{b+1}{n+1}$   
	- raisonnement *Fréquentiste* : $p\approx \frac{b}{n}$  
# Espaces probabilisés  
  
- définition  
	1. *Univers* $\Omega$  
	2. *Tribu* ($\sigma$-algèbre) $\mathcal{A} \{ \Omega \}$ : tous les sous ensembles de $\Omega$  
		- $\bar{a}=\frac{\Omega}{A} \in \mathcal{A}$ , $a_{1}\cup a_{2}\in\mathcal{A}$ fermé para rapport a l'union et compllément  
	1. *Probabilité* $P:\mathcal{A}\to[0,1]$  
  
- *Produit*  $=(\Omega_{1}\times\Omega_{2}, A_{1}\times A_{2}, P(A_{1})P(A_{2}))$ (évenements indé)  
  
- évenements *indépendants* $A\perp\!\!\!\perp B \iff P(A\cap B)=P(A)P(B)$  
  
  
- épreuve de Bernouilli : $\Omega=\{ E,S \}$ échecs, succès  
	- $\mathcal{A}(\Omega)=\{ \emptyset, \{ E \}, \{ S \}, \Omega \}$, $p$ succès  
	- $\times n$ → Schéma de B : $\Omega=\{ E,S \}^n$, $\mathcal{A}(\Omega)$ : proba $p^kq^{n-k}$  
# Variable aléatoire $X$  
  
- $X:\Omega_{1}\to\Omega_{2}$  et inverse : $\forall A\in\Omega_{2}: X^{-1}(A)\in\Omega_{1}$  
  
- proba indépendante de l'espace : $P_{1}(A)=P_{2}(X(A))$  
  
- variables *indépendantes* : $X_{1}^{-1}(A_{1})\perp\!\!\!\perp X_{2}^{-1}(A_{2})$  
  
- variable alé réelles (continues) : ??  
	- nb infini → prends surface  
	- Borel-Lebesgue  
		- produits cartésiens d'intervalles, unions finis/dénombrables et compléments d'E mesurable → *mesurable*  
		- *mesure* $\mu:\mathcal{B}\to \mathbb{R}\cup \infty$: $\mu(A)=\sum \mu(A_{i})$,$P(A)=\frac{\mu(A)}{\mu(\Omega)}$  
  
- **Espérance** : $\mathbb{E}(X)=\int xf(x) \, dx=\sum sP(s)$ avec $s$ valeurs de $X$  
	- linéaire : $\mathbb{E}(aX+bY)=a\mathbb{E}(X)+b\mathbb{E}(Y)$  
	- **Moment d'ordre** $n$ : $m_{n}=\mathbb{E}(X^n)$  
	- *Fonction génératrice des moments* $=E(e^{tX})$  
  
- **Variance** - **écart type** $\sigma$ : $Var(X)=\sigma^{2}(X)=\mathbb{E}(X^{2})-\mathbb{E}(X)^{2}$  
	- **Covariance** : $Cov(X,Y)=\mathbb{E}(XY)-\mathbb{E}(X)\mathbb{E}(Y)$  
		- variables indépendates : $Cov(X,Y)=0$  
	- ⇒$Var(aX+bY)=a^{2}Var(X)+2abCov(X,Y)+b^{2}Var(Y)$  
	- Variance *Conditionnelle* $Var(X|Y=y)=\int (x-\mathbb{E}(Y|X=x))^{2}f(y|x) \, dx$  
	- avec $X|Y$ ⇒  $Var(X)=\mathbb{E}(Var(X|Y))+Var(\mathbb{E}(X|Y))$  
  
- **Corrélation** $\rho(X,Y)=\frac{Cov(X,Y)}{\sigma(X)\sigma(Y)}\in[-1,1]$ (0 → indé; 1 → li-dép)  
  
- Inégalité de *Markov* : $P(X\geq a\mathbb{E}(X))\leq \frac{1}{a}$  
  
- Inégalité *Bienaymé-Tchebychev* $P(|X-\mathbb{E}(X)|\geq a\sigma(X))\leq \frac{1}{a^{2}}$  
  
- **Vecteur** de var alé $(X,Y)$ : $F(X,Y)=P(X\geq x, Y\geq y)$  
	- $X\perp\!\!\!\perp Y\implies P({\tiny X{=}x,Y{=}y})=P({\tiny X{=}x})P ({\tiny Y{=}y} )$ ou $f(x,y)=\int f \, dx\cdot\int f \, dy$  
  
- $x$ est **quantile** de $p$ : $x:P(X<x)\leq p\leq P(X)$ ou $F(x)=p$  
  
- **Médiane**  : quantile de $0.5$  
	- $x \in I$ si $X$pas continu  
  
  
- *Densité de probabilité* $f(x)=P(X=x)$ : ($X$ continue) $P(X \in[a,b])=\int_{a}^{b} f(t) \, dt=F(b)-F(A)$  
  
- *Fonction de répartition* : $F(x)=P(x\leq X)=\int_{-\infty}^{x}f(t)  \, dt$  
  
- $Y=h(X)$⇒$f_{y}(x)=\frac{f(x)}{|h'(x)|}$ et $\mathbb{E}_{y}=\int h(x)f(x) \, dx=\sum h(x)P(X=x)$  
# Lois de probabilités  
  
- *Loi géométrique* : $P(X=x)=q^xp$ avec $q$  proba échecs et $x$ nb échecs avant réussite  
	- $\mathbb{E}(X)=\frac{1}{p}$ et $\sigma^{2}=\frac{q}{p^{2}}$  
  
- *Loi Binomiale* : $P(N=k)=B(n,k)p^xq^{n-k}$ avec $n$ épreuves, $x$ réussites ($\{ E,S \}^n\to \{ 0,1,\dots n \}$)  
	- $\mathbb{E}(X)=np$ et $\sigma^{2}=npq$  
	- $p\ll 1$  ⇒ $\approx$ loi de poisson : $\mu=np$   
	- $npq\gg 1$  ⇒ $\approx$ loi normale : $\mu=np$  et $\sigma^{2}=npq$ (e$\mathcal{O}\left( \frac{1}{\sqrt{ n }} \right)$)  
  
- *Loi exponentielle* $f(x)=\lambda e^{-\lambda x}$ et $F(x)=1-e^{\lambda x}$ avec $\lambda$ taux proba/temps  
	- $\mathbb{E}(X)=\frac{1}{\lambda}$ et $\sigma^{2}=\frac{1}{\lambda^{2}}$  
	- $\approx$ loi de poisson : $\lambda=\left[ \frac{p}{t} \right]$, intervalles $n=\frac{T}{\Delta t}$ : $\mu=\lambda T$  
  
- *Loi de Poisson* $P(N=k)=f(k)=\frac{\mu^k}{k!}e^{-\mu}$ avec $n\gg 1,p\ll 1$   
	- $\mathbb{E}(X)=\sigma^{2}=\mu$  
  
- *Loi Normale* $f(x)=\frac{1}{\sigma \sqrt{ 2\pi }}e^{-(x-\mu)^{2}/2\sigma^{2}}=N(\mu,\sigma^{2})$ (loi de Gauss)  
	- *Théorème central limite* : $\forall Z_{n}=\frac{\sum_{i=1}^{n}X_{i}}{n}$ , espérance $\mu$, variance $\frac{\sigma^{2}}{n}$  
		- $n\to \infty$  
		- $\lim_{ n \to \infty }Z_{n}\sim N(\mu , \sigma^{2}/n)$  
		- variable centrée réduite $Z_{n}'=\frac{Z_{n}-\mu}{\sigma /\sqrt{ n }}$ → $Z_{n}'\sim N(0 , 1)$  
		- $P\left( |\frac{\sum X_{i}}{n}-\mu|\geq\epsilon \right)\to 0$  
