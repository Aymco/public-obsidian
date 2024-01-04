---  
share: true  
category: MDP  
created: 2023-12-16  
updated: 2024-01-04  
---  
  
[Combinatoires - dénombrements](Combinatoires%20-%20d%C3%A9nombrements.md)  
# Espaces probabilisés  
  
- définition   
	1. *Univers* $\Omega$  
	2. *Tribu* $A \{ \Omega \}$  
		- $\bar{a}=\frac{\Omega}{A} \in A$  
	1. *Probabilité* $P(a)$  
  
- *Axiomes de Kolmogorov*   
	1. $P(A)\in[0,1]$  
	2. $P(\Omega)=1$  
	3. $P(A\cup B)=P(A)+P(B)$ (disjoints)  
  
- *Produit*  $=(\Omega_{1}\times\Omega_{2}, A_{1}\times A_{2}, P(A_{1})P(A_{2}))$  
  
- espaces *indépendants* $A\perp\!\!\!\perp B$ ⇒ $P(A\cap B)=P(A)P(B)$  
# Variable aléatoire $X$  
  
- $X:\Omega_{1}\to\Omega_{2}$  et inverse : $\forall A\in\Omega_{2}: X^{-1}(A)\in\Omega_{1}$  
  
- proba indépendante de l'espace : $P_{1}(A)=P_{2}(X(A))$  
  
- variables *indépendantes* : $X_{1}^{-1}(A_{1})\perp\!\!\!\perp X_{2}^{-1}(A_{2})$  
  
- **Espérance** : $\mathbb{E}(X)=\int P(s) \, ds=\sum sP(s)$ avec $s$ les valeurs de $X$   
	- **Moment d'ordre** $n$ : $m_{n}=\mathbb{E}(X^n)$  
  
- **Variance** - **écart type** $\sigma$ : $var(X)=\sigma^{2}(X)=\mathbb{E}(X^{2})-\mathbb{E}(X)^{2}$  
	- **Covariance** : $Cov(X,Y)=\mathbb{E}(XY)-\mathbb{E}(X)\mathbb{E}(Y)$  
	- ⇒ $Var(aX+bY)=a^{2}Var(X)+2abCov(X,Y)+b^{2}Var(Y)$  
	- Variance *Conditionnelle* $Var(X|Y=y)=\int (x-\mathbb{E}(Y|X=x))^{2}f(y|x) \, dx$  
	- avec $X|Y$ ⇒  $Var(X)=\mathbb{E}(Var(X|Y))+Var(\mathbb{E}(X|Y))$  
  
- **Corrélation** $\rho(X,Y)=\frac{Cov(X,Y)}{\sigma(X)\sigma(Y)}\in[-1,1]$ (0 → indé; 1 → li-dép)  
  
- *Bienaymé-Tchebychev* $P(|X-\mathbb{E}(X)|\geq a)\leq \frac{Var(X)}{a^{2}}$  
## Fonctions de représentation  
  
- *Densité de probabilité* $f(x)=P(X=x)$ : $P(X \in[a,b])=\int_{a}^{b} f(t) \, dt=F(b)-F(A)$  
  
- *Fonction de répartition* : $F(x)=P(X\leq x)=\int_{-\infty}^{x}f(t)  \, dt$  
# Lois de probabilités  
  
- *Loi géométrique* : $P(X=x)=q^xp$ avec $q$  proba échecs et $x$ nb échecs avant réussite  
	- $\mathbb{E}(X)=\frac{1}{p}$ et $\sigma^{2}=\frac{q}{p^{2}}$  
  
- *Loi Binomiale* : $P(X=x)=C_{n}^k\,p^x(1-p)^{n-x}$ avec $n$ épreuves, $x$ réussites  
	- $\mathbb{E}(X)=np$ et $\sigma^{2}=npq$  
  
  
- *Loi exponentielle* $f(x)=\lambda e^{-\lambda x}$ et $F(x)=1-e^{\lambda x}$ avec $\lambda$ taux proba/temps  
	- $\mathbb{E}(X)=\frac{1}{\lambda}$ et $\sigma^{2}=\frac{1}{\lambda^{2}}$  
  
- *Loi de Poisson* $f(x)=\frac{\mu^x}{x!}e^{-\mu}$ $\approx$ loi Binomiale $n\gg 0,p\ll 0$   
	- $\mathbb{E}(X)=\sigma^{2}=\mu$  
  
- *Loi Normale* $f(x)=\frac{1}{\sigma \sqrt{ 2\pi }}e^{-(x-\mu)^{2}/2\sigma}=N(\mu,\sigma)$ [loi normale - loi de Gauss](loi%20normale%20-%20loi%20de%20Gauss.md)  
	- *Théorème central limite* : $\forall Z_{n}=\sum_{i=0}^{n}X_{i}$  
		- $\lim_{ n \to \infty } P(Z_{n}=z)=f(z)$  
# Probabilités conditionnelles  
  
- $P(A|B)=\frac{P(A\cap B)}{P(B)}$ A sachant (corrigé par) B  
  
- *théorème de Bayès* : $P(A|B)=\frac{P(A)}{P(B)}P(B|A)$  
## Inférences statistiques  
  
- trouver la proba à partir d'observations  
  
- $p$ proba de réussite, $b$ réussites, $n$ épreuves  
  
- m *Bayèsienne* : *succession de Laplace* $p\approx \frac{b+1}{n+1}$   
  
- m *Fréquentiste* : $p\approx \frac{b}{n}$  
