---
time: 13.11.2023 13:02
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Autonome ODE-Systeme

>[!mot] Setting
>Sei $D\subset\mathbb{R}^{n}$ offen. Wir betrachten $$y'=f(y),\qquad f:D\rightarrow\mathbb{R}^{n}\qquad(\star)$$

>[!bem] Bemerkung 2.6
>Die Translationsinvarianz von $F$ überträgt sich auf die Lösungen: Mit $y$ ist auch $y\circ\text{Tr}$ Lösung.

>[!def] Definition 2.7
>Eine konstante Lösung $y\equiv c$ von $(\star)$ heißt stationär. (dann $f(c)=0$). Nun sei die DGL auch linear: $$(\star)\begin{cases}
&y'=Ay\\[12pt]
&y(0)=y_{0}
\end{cases}$$

>[!def] Definition: Spektrum, Halbeinfach
>Das Spektrum einer Matrix $A\in\mathbb{R}^{n\times n}$ ist die Menge ihrer Eigenwerte: $$\text{spec }A:=\{\lambda\in\mathbb{C}\vert\exists v\in\mathbb{R}^{n}:Av=\lambda v\}$$
>$\lambda\in\text{spec}(A)$ heißt **halbeinfach** $$:\Leftrightarrow\text{GV}(\lambda)=\text{AV}(\lambda)$$

>[!thm] Theorem 2.8
>1. System $(\star)$ (d.h. jede Lösung) [[Stabilität|stabil]] $\Leftrightarrow\text{Re}(\lambda)\le0\forall\lambda\in\text{spec}(A)$ und falls $\exists\lambda\in\text{spec}(A):\text{Re}(\lambda)=0$, dann $\lambda$ halbeinfach.
>2. $(\star)$ asymptotisch stabil $\Leftrightarrow$ $(\star)$ exponentiell stabil $\Leftrightarrow\text{Re}(\lambda)\lt0\forall\lambda\in\text{spec}(A)$. Mit $s:=\max\{\text{Re}(\lambda)\vert\lambda\in\text{spec}(A)\}\lt0$ gilt: $$\left\lVert e^{Ax}y_{0}\right\rVert\le M_{\omega}\left\lVert y_{0}\right\rVert e^{-\omega x}\qquad\forall\omega\in(s,0)$$
>   Falls $\forall\lambda\in\text{spec}(A):\text{Re}(\lambda)=s\Rightarrow\lambda\text{ halbeinfach}$, dann $\exists M:\lVert\underbrace{e^{Ax}y_{0}}_{y(t)}\rVert\le M\left\lVert y_{0}\right\rVert\cdot e^{sx}$
>   3. $(\star)$ instabil, falls $$\exists\lambda\in\text{spec }A:\text{Re}(\lambda)\gt0\lor(\text{Re}(\lambda)=0\land\lambda\text{ halbeinfach})$$

>[!exp] Beispiel 2.9
>$$\begin{align*}
&x_{1}'=-x_{1}\\[12pt]
&x_{2}'=x_{1}-2x_{2}
\end{align*}\qquad(\star)$$
>$\rightsquigarrow$ $0$ ist Lsg. von $(\star)$ $\Leftrightarrow\begin{pmatrix}x_{1} \\ x_{2}\end{pmatrix}=A\begin{pmatrix}x_{1} \\ x_{2}\end{pmatrix}$ mit $A=\begin{pmatrix}-1  & 0 \\ 1 & -2\end{pmatrix}$.
>$\rightsquigarrow$ EW. $\lambda_{1}=-1$, $\lambda_{2}=-2$, ER $\mathbb{R}v_{i}$ mit $v_{1}=\begin{pmatrix}1 \\ 1\end{pmatrix},\quad v_{2}=\begin{pmatrix}0 \\ 1\end{pmatrix}$.
>$\text{Re}\lambda_{i}\lt0\forall i\Leftrightarrow(\star)$ exponentiell stabil, $\omega=-1$ wählbar.
>Allg. Lsg.: $$x(t)=c_{1}e^{-t}\begin{pmatrix}1 \\ 1\end{pmatrix}+c_{2}e^{-2t}\begin{pmatrix}0 \\ 1\end{pmatrix}\text{ für }c_{i}\in\mathbb{R}$$

>[!exp] [[Nichtlineare autonome Systeme von Differentialgleichungen]]