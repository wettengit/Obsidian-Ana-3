---
time: 13.11.2023 11:54
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Stabilität

>[!def] Definition 2.1: Arten von Stabilität
>Sei $D\subset\mathbb{R}^{n+1}$ offen, $f:D\rightarrow\mathbb{R}^{n}$ sei $\mathcal{C}^{1}$, $x_{0}\in\mathbb{R}$. $y_{x_{0},y_{0}}=:y:[x_{0},\infty)\rightarrow\mathbb{R}^{n}$ sei Lsg. von $y'=f(x,y),\quad y(x_{0})=y_{0}$.
>$y$ heißt
>- ($f$-) **stabil** (auf $[x_{0},\infty)$) $$\begin{align*}
&:\Leftrightarrow\forall\varepsilon\gt0:\exists\delta\gt0:\forall z_{0}\in\mathbb{R}^{n}:\\[12pt]
&\left\lVert y_{0}-z_{0}\right\rVert\lt\delta\Rightarrow\left\lVert y_{x_{0},z_{0}}(x)-y(x)\right\rVert\lt\varepsilon\quad\forall x\ge x_{0}
\end{align*}$$
>- ($f$-) **attraktiv** (auf $[x_{0},\infty)$) $$\begin{align*}
&:\Leftrightarrow\exists\delta\gt0:\forall z_{0}\in\mathbb{R}^{n}:\left\lVert y_{0}-z_{0}\right\rVert\lt\delta\Rightarrow\exists y_{x_{0},z_{0}}\text{ auf }I\text{ und }\\[12pt]
&\lim\limits_{x\rightarrow\infty}\left\lVert y(x)-y_{x_{0},z_{0}}(x)\right\rVert=0
\end{align*}$$
>- ($f$-) **asymptotisch stabil** $\Leftrightarrow$ stabil und attraktiv
>- ($f$-) **exponentiell stabil** $$\begin{align*}
&:\Leftrightarrow\exists\delta,L,\omega\gt0:\forall z_{0}\in\mathbb{R}^{n}:\left\lVert y_{0}-z_{0}\right\rVert\lt\delta\Rightarrow\exists y_{x_{0},z_{0}}\text{ auf }I\text{ und }\\[12pt]
&\left\lVert y(x)-y_{x_{0},z_{0}}(x)\right\rVert\le L\left\lVert y_{0}-z_{0}\right\rVert e^{-\omega(x-x_{0})}
\end{align*}$$

>[!bem] Bemerkung 2.2
>1. $y$ exp. stabil $\Rightarrow$ $y$ asymptotisch stabil $\Rightarrow$ $y$ stabil und attraktiv
>2. Für $n=1$: $y$ attraktiv $\Rightarrow$ $y$ stabil aber für $n\gt1$ i.A. falsch
>3. $y$ stabil $\Rightarrow\exists x_{0}\forall x\ge x_{0}:\left\lVert y(x)-y_{x_{0},z_{0}}\right\rVert\lt\varepsilon\text{ für }\left\lVert x_{0}-z_{0}\right\rVert\lt\delta$

>[!exp] Beispiel 2.3
>$$\begin{align*}
&y'=\alpha y&&y(x_{0})=y_{0}\\[12pt]
&\tilde y'=\alpha\tilde y&&\tilde y(x_{0})=\tilde y_{0}
\end{align*}$$
>$\omega:=y-\tilde y$: $\omega'(x)=\alpha\omega\Rightarrow\omega(x)=e^{\alpha x}$ mit $\omega(0)=1=y(0)-\tilde y(0)$
>Also folglich $$\begin{cases}
&\alpha\gt0 & y\text{ exp. stabil}\\[12pt]
&\alpha=0 & y\text{ stabil }(\delta=\varepsilon)\\[12pt]
&\alpha\lt0 & y\text{ ist nicht stabil}
\end{cases}$$

>[!bem] Bemerkung 2.4
>Stabilitätsbegriffe sind bei linearen Systemen unabh. von gewähltem $y$. Moral: Teste an $y\equiv0$

