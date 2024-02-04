---
time: 07.11.2023 14:12
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Nichtlineare autonome Systeme von Differentialgleichungen

>[!mot] Setting
>Sei $D\subset\mathbb{R}^{n}$ offen. Wir betrachten $$y'=f(y),\qquad f:D\rightarrow\mathbb{R}^{n}\qquad(\star)$$

>[!thm] Theorem 2.11: Linearisierte Stabilität
>Sei $D\subset\mathbb{R}^{n}$ offen, $f:D\rightarrow\mathbb{R}^{n}$ sei $\mathcal{C}^{1}$, $y_{s}\in f^{-1}(\{0\})$. Sei $$J_{f}[y_{s}]:=\left(\frac{\partial f_{i}}{\partial y_{j}}\right)_{i,j=1}^{n}(y_{s})$$
>1. Wenn jedes $\lambda\in\text{spec}(J_{f}[y_{s}])$ erfüllt: $\text{Re }\lambda\lt0\Rightarrow\overline y_{s}:=y_{s}\forall t\in\mathbb{R}$ exponentiell stabil.
>2. Wenn $\exists\lambda\in\text{spec}(J_{f}[y_{s}]):\text{Re }\lambda\gt0\Rightarrow\overline y_{s}$ instabil.

>[!bem] Bemerkung 2.12
>Falls $\text{Re }\lambda\le0\forall\lambda\in\text{spec }A$ und $\exists\lambda\in\text{spec }A:\text{Re }\lambda=0$
>$\Rightarrow$ Wir wissen ohne Kenntnis der Hesseschen an $y_{s}$ i.A. nichts.

>[!bem] Bemerkung 2.13
>$$\begin{align*}
&y_{1}'=-y_{1}+e^{2x}y_{2}\\[12pt]
&y_{2}'=-y_{2}
\end{align*}\qquad(\star)$$
>$0$ ist Lsg. von $(\star)$. Die Lösung des AWP: $$\begin{align*}
&\begin{pmatrix}y_{1}(x) \\ y_{2}(x)\end{pmatrix}=\begin{pmatrix}\left(\xi_{1}-\frac{\xi_{2}}{2}\right)e^{-x}+\frac{\xi_{2}}{2}e^{x} \\ \xi_{2}e^{-x}\end{pmatrix}\qquad\begin{matrix}y_{1}(0)=\xi_{1} \\ y_{2}(0)=\xi_{2}\end{matrix}\\[12pt]
&J_{f}(0)=\begin{pmatrix}-1 & e^{2x}\\
0 & -1\end{pmatrix}\qquad\qquad\text{spec }A=\{-1\}
\end{align*}$$

>[!exp] Beispiel 2.14
>$$\begin{align*}
&x'(t)=(2+x(t))(y(t)-x(t))\\[12pt]
&y'(t)=y(t)(2+x(t)-x^{2}(t))
\end{align*}\qquad(\star)$$
>$(0,0),(-2,0),(-1,-1),(2,2)$ sind Nullstellen der RHS $(\star)$. $$J_{f}(0,0)=\begin{pmatrix}-2  & 2 \\ 0 & \textcolor{red}{2}\end{pmatrix}\qquad\text{Re }\textcolor{red}{\lambda}\gt0\Rightarrow(0,0)\text{ instabil.}$$
>Tatsächlich sind $(-1,-1),(2,2)$ exp. stabil, die anderen beiden instabil.

>[!exp] Beispiel 2.15: Starres mathematisches Pendel
>Sei $l=1$
>$$my''=-mg\sin(y)$$
>Sei $z:=y'$, dann ODS erster Ordnung: $$\boxed{\begin{align*}
&y'=z\\[12pt]
&z'=-g\sin(y)
\end{align*}}$$
>$f(y,z)=(z,-g\sin(y))$ hat Nullstellenmenge $\{(k\pi,0)\vert k\in\mathbb{Z}\}$.
>$$J_{f}\begin{pmatrix}\pi \\ 0\end{pmatrix}=\left.\begin{pmatrix}0 & 1 \\ -g\cos y & 0\end{pmatrix}\right\vert_{y=\pi}=\begin{pmatrix}0 & 1 \\ g & 0\end{pmatrix}\qquad\text{spec}=\{\sqrt{g}\}\Rightarrow(\star)\text{ inst. an}\begin{pmatrix}0 \\ \pi\end{pmatrix}$$
>$\text{spec }J_{f}(0,0)=\{\pm i\sqrt{g}\}\Rightarrow\text{Re }\lambda_{\pm}=0\Rightarrow$ können Satz 2.11 nicht anwenden. Aber: Können Erhaltungsgrößen ausnutzen: Energiebegriffe, **Hamiltonsche Systeme**. Energie: $$E=K+U=mg(-\cos y)+\frac{1}{2}mz^{2}$$
>Wir berechnen $$\frac{d}{dt}E(y(t),z(t))=\nabla E(y(t),z(t))\cdot\begin{pmatrix}y'(t) \\ z'(t)\end{pmatrix}=\begin{pmatrix}mg\sin y(t) & mz(t)\end{pmatrix}\begin{pmatrix}z(t) \\ -g\sin y(t)\end{pmatrix}=0$$

>[!def] Definition 2.16
>Sei $f:D\rightarrow\mathbb{R}^{n}$ lokal Lipschitz. Eine Funktion $E\in\mathcal{C}^{1}(D,\mathbb{R}^{n})$ heißt **erstes Integral** von $y'=f(y)$ $$:\Leftrightarrow\nabla E(y)\cdot f(y)=0\qquad\forall y\in D$$

>[!exp] Beispiel 2.17
>$y'=-y,z'=-z$ $(\star)$. Lösung: $\begin{pmatrix}y \\ z\end{pmatrix}(t)=\begin{pmatrix}y_{0} \\ z_{0}\end{pmatrix}e^{-t}$. Sei $E:\mathbb{R}^{2}\rightarrow\mathbb{R}$ ein erstes Integral wie oben. $$E(y_{0},z_{0})=E(y_{0}e^{-t},z_{0}e^{-t})\xrightarrow[\,t_{\infty}\,]{}E(0)\Rightarrow E\text{ const.}$$
>"Es gibt kein nicht-triviales erstes Integral von $(\star)$." Konstanten sind immer erste Integrale, sagen aber nichts über das System aus.

>[!exp] Beispiel 2.20: 2D Hamiltonsches System
>Physikalisch: $y(t)$ Ortskoordinate, $z(t)$ Impulskoordinate
>$$\begin{align*}
&y'=\frac{\partial }{\partial z}H(y,z)\\[12pt]
&z'=-\frac{\partial }{\partial y}H(y,z)
\end{align*}$$
>z.B. Pendel: $H=E$

>[!exp] Beispiel 2.21: Räuber-Rate
>Seien $\alpha,\beta,\gamma,\delta\in(0,\infty)$.
>$$\begin{align*}
&y'=y(\alpha-\beta z)\\[12pt]
&z'=z(\delta y-\gamma)
\end{align*}$$
>Sagen wir, $$\begin{align*}
&y(\alpha-\beta z)=\partial_{z}H\\[12pt]
&z(\delta y-\gamma)=\partial_{y}H
\end{align*}\text{ für ein }H$$
>$\Rightarrow H\in\mathcal{C}^{\infty}$, [[Gradient, Jacobi-Matrix und Hessematrix|Clairault-Schwarz]] gilt offenbar nicht, also finde ich kein $H$. Trotzdem: $$E(y,z)=\alpha\ln(|z|)-\beta z+\gamma\ln(|y|)-\delta y$$ist erhaltenes 1. Integral auf $\mathbb{R}^{+}\times\mathbb{R}^{+}$ (und auch auf anderen Quadranten) auf $\mathbb{R}^{+}\times\mathbb{R}^{+}$ gibt es Transformation zu einem Ham. System.

>[!exp] Was ist ein Hamiltonsches System auf einer [[Mannigfaltigkeiten|Mannigfaltigkeit]] ($M\subset\mathbb{R}^{n}$ offen)? (nicht klausurrelevant)
>Ein Hamiltonsches System ist offenbar nichts anderes der **Fluss** (System folgt Vektorfeld $\partial_{t}u=V(u)$) eines **symplektischen Gradienten** $V=s\text{grad}(H)$, $H:M\rightarrow\mathbb{R}$. Also nicht $\left\langle\text{grad }H,W\right\rangle=\dd H\cdot W$, sondern $\omega(s\text{grad }H,W)=\dd H\cdot W$ mit $\omega$ **symplektische Form**, z.B. $\omega(x,y)=\left\langle ix,y\right\rangle$ in $\mathbb{R}^{2}\simeq\mathbb{C}$ (vertauscht sozusagen Orts- und Impulskoordinaten mit Vorzeichenwechsel). Bilinearform symmetrisch, Symplektische Form antisymmetrisch.

>[!def] Definition 2.23: Ljapunow-Funktion
>Sei $D\subset\mathbb{R}^{n}$ offen, $f:D\rightarrow\mathbb{R}^{n}$ lokal Lipschitz, $y_s\in f^{-1}(\{0\})$, $\bar y_{s}(t)\equiv y_{s}$ stationäre Lsg. Sei $y_{s}\in U\subset D$ offen und $V\in\mathcal{C}^{1}(U,\mathbb{R})$. $V$ heißt
>1. (schwache) **Ljapunow-Funktion** an $y_{s}$ $$:\Leftrightarrow\nabla V(y)\cdot f(y)\le0\quad\forall y\in U$$
>2. **starke Ljapunow-Funktion** an $y_{s}$ $$:\Leftrightarrow\nabla V(y)\cdot f(y)\lt0\quad\forall y\in U\setminus\{y_{s}\}$$

>[!bem] Bemerkung 2.24
>1. (starke) LF fallen (streng) monoton längs Lösungen
>2. Erste Integrale sind schwache LF.

>[!exp] Beispiel 2.25: Mathematisches Pendel
>Jede Lösung liegt in einer Niveaumenge $N_{a}:=E^{-1}(\{a\})$ von $E$, $\Rightarrow E$ ist auch LF

>[!thm] Theorem 2.26
>Sei $f:D\rightarrow\mathbb{R}^{n}$ lokal Lipschitz, $y_{s}\in f^{-1}(\{0\})$, $\overline y_{s}:t\mapsto y_{s}\forall t\in\mathbb{R}$. Sei $V:U\rightarrow\mathbb{R}$. $V$ (starke) LF von $y'=f(y)$ an $y_{s}$.
>Falls $$V(y_{s})\lt V(y)\quad\forall y\in U\setminus\{y_{s}\}$$, dann ist $\overline y_{s}$ (asymptotisch) stabil.

>[!bem] Bemerkung 2.27
>Nochmal zur Stabilität der Ruhelage $(0,0)$ beim math. Pendel. $E(y,z)=\frac{z^{2}}{2}-g\cos(y)$ ist schwache LF (1. Int.). $$E(0,0)=-g\lt E(y,z)\forall(y,z)\in(-2\pi,2\pi)\times\mathbb{R}$$
>Also ist $(0,0)$ stabil, aber nicht asymptotisch stabil.
