---  
share: true  
category: Physique 3  
tags:  
  - matière  
created: 2023-12-23  
updated: 2024-01-13  
title: Fonction d'onde de Schrödinger  
---  
  
  
- **Fonction d'onde** $\psi$ distribution spatiale de la particule  
  
- *Densité de probabilité* : $|\psi|^{2}$  ($|z|^{2}=\bar{z}\cdot z$)  
voir aussi [puits et barrières de potentiel](puits%20et%20barri%C3%A8res%20de%20potentiel.md)  
# Equation de Schrödinger  
  
- $\left( -\frac{\hbar^{2}\nabla^{2}}{2m}+V  \right)\psi=i\hbar \psi_{t}$ avec $V=V(x,y,t)$  
  
- souvent E défini : $\psi=\psi_{1}(\vec{r})e^{-iEt/\hbar}$ et $| \psi|^{2}=|\psi_{1}(\vec{r})|^{2}$  
  
- particule stationnaire : (el gravite autour du noyau)  
	- ⇒ eq Indépendante du temps : $\left( -\frac{\hbar^{2}\nabla^{2}}{2m}+V  \right)\psi_{1}(\vec{r})=E\psi_{1}(\vec{r})$  
  
  
- particule *non-localisée* $\psi_{1}(\vec{r})=C_{k}e^{i\vec{k}\cdot \vec{r}}$ et $\psi_{2}(t)=C_{E}e^{-iEt/\hbar}$  
  
- particule *localisée* $\psi_{1}(\vec{r})=\int_{-\infty}^{\infty}$ au dessus, pareil  
  
  
- *superposition quantique* : système à 2+ état → combili : $\psi=\sum_{i}^{}\alpha_{i}\psi_{i}$  
	- paradoxe du chat de Schrodinger : proba ½ d'une situation → dans les 2  
## Solution particule libre  
  
- potentiel nul (!Forces → énergie interne cst → $U=0$)  
  
- $\psi=C(k)e^{i(kx-\bar{n}k^{2}t/2m)}$ avec $C(k)$ le pic   
  
- pour un certain $k$ on a $\Delta p=0$ et $\Delta x=\infty$  
  
- Energie $E=\hbar w_{0}$, impulsion $p=\hbar k_{0}$  
  
- Solution particule libre *localisée* (paquet d'ondes):  
	- $\psi=\int_{-\infty}^{\infty} C(k)e^{i(kx-\bar{n}k^{2}t/2m)} \, dk$  
*incertitude d'Heisenberg* : $\Delta x\Delta p\geq \frac{\hbar}{2}$et $\Delta E\Delta t\geq \frac{\hbar}{2}$  
  
# Oscillateur quantique  
$k$ constante de raideur (voir [Oscillateurs harmoniques](Oscillateurs%20harmoniques.md))  
  
- **niveaux d'Energie** : $E_{n}=\left( n+\frac{1}{2} \right) \hbar \omega$ avec $\omega=\sqrt{ \frac{k}{m} }$   
  
Solution pour le niveau d'énergie le plus bas : fonction d’Hermite :  
$\psi=Ce^{-\sqrt{ mk }x^{2}/2\hbar}$ ([Fonction d'onde de Schrödinger](Fonction%20d'onde%20de%20Schr%C3%B6dinger.md))  
