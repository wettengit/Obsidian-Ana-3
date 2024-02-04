---
time: 28.11.2023 13:45
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Hilberträume und Fourierreihen

>[!exp] Beispiel 4.8: Fourierpolynome
>$f:I:=[-\pi,\pi]\rightarrow\mathbb{R}$ stetig. Suche $a_{0},...,a_{n},b_{1},...,b_{n}$ mit $\left\lVert S_{a,b}-f\right\rVert_{L^{2}(-\pi,\pi)}$ minimal mit $$S_{a,b}(x):=\frac{a_{0}}{2}+\sum\limits_{n=1}^{m}a_{n}\cos(nx)+b_{n}\sin(nx)\qquad\forall x\in I$$
>$S_{a,b}$ ist allg. Form eines sog. trigonometrischen Polynoms von Grad $\le m$ $$U_{m}:=\text{span}\{1,\cos,\sin,\cos(2\cdot),\sin(2\cdot),...,\cos(m\cdot),\sin(m\cdot)\}$$(also trig. Polynome von Grad $\le m$)

>[!thm] Theorem 4.9
>$\forall n,k$: $$\left\langle\cos(n\cdot),\sin(k\cdot)\right\rangle=0,\quad\left\langle\cos(n\cdot),\cos(k\cdot)\right\rangle=\left\langle\sin(n\cdot),\sin(k\cdot)\right\rangle=\begin{cases}
0,&  n\ne k\\[12pt]
\pi,& \text{sonst}
\end{cases}$$

>[!thm] Theorem 4.10
>$u_{n}:[-\pi,\pi]\rightarrow\mathbb{R}$, $$u_{0}(x):=\frac{1}{\sqrt{2\pi}},\quad u_{2n-1}:=\frac{1}{\sqrt{\pi}}\cos(nx),\quad u_{2n}(x):=\frac{1}{\sqrt{\pi}}\sin(nx)$$
>$\{u_{i}\vert i\in\mathbb{N}\}$ sind ONS.

>[!def] Definition 4.11
>$$a_{n}=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\cos(nx)\dd x,\qquad b_{n}:=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\sin(nx)\dd x\qquad(n\in\mathbb{N})$$
>heißen Fourierkoeff. von $f$ und $S_{a,b}$ $m$-tes Fourierpolynom von $f$. Hoffnung: Dies löst obiges Optimierungsproblem.

>[!def] Definition 4.12
>Sei $H$ ein $\mathbb{K}$-VR mit [[Bilinearformen und Sesquilinearformen|Sesquilinearform]] $\left\langle\cdot,\cdot\right\rangle\rightsquigarrow\left\lVert\cdot\right\rVert\rightsquigarrow d(\cdot,\cdot)$. ([[Metrische Räume|Ana II]]) 
>1. Falls $H$ [[Kompakte und zusammenhängende metr. Räume|vollständig]], dann heißt $(H,\left\lVert\cdot\right\rVert)$ ein reeller bzw. komplexer **Hilbertraum**.
>2. Falls $(B,\left\lVert\cdot\right\rVert)$ [[Normierte Räume|normierter]] vollständiger VR ist, dann heißt $(B,\left\lVert\cdot\right\rVert)$ **Banachraum**.
>3. Falls $(F,d)$ metrischer VR (lokalkonvex), vollständig, dann heißt $(F,d)$ **Frechetraum**.

>[!exp] Beispiel 4.13
>- $(\mathbb{R}^{n},\left\lVert\cdot\right\rVert_{2})$ ist HR
>- $(\mathbb{R}^{n},\left\lVert\cdot\right\rVert_{p})$ ist BR für $p\in[1,\infty]$

>[!thm] Theorem 4.14
>Sei $V$ ein VR mit Skalarprodukt, dann:$\left\langle\cdot,\cdot\right\rangle$ stetig.

>[!thm] Theorem 4.15: Projektionssatz
>Sei $H$ ein Hilbertraum. Sei $U\subset H$ abgeschlossen und konvex. Dann: $$\forall f\in H:\exists!f_{0}\in U:\left\lVert f-f_{0}\right\rVert\le\left\lVert f-u\right\rVert\qquad\forall u\in U$$
>($f_{0}=:\text{pr}_{U}^{\perp}(f)$)

>[!thm] Theorem 4.16: Zerlegungssatz
>Sei $H$ HR, $U\subset H$ abgeschlossener lin. Unterrraum ($\Rightarrow$ konvex!). Dann gilt: $$H=U\oplus U^{\perp},\qquad U^{\perp}:=\{v\in H:\left\langle v,u\right\rangle=0\forall u\in U\}$$

>[!thm] Theorem 4.17
>$$(P_{U}^{\perp})^{2}=P_{U}^{\perp},\qquad (P_{U}^{\perp})^{T}=P_{U}^{\perp}$$d.h. $P_{U}^{\perp}$ ist selbstadjungiert.

>[!def] Definition 4.18
>$b:\mathbb{N}\rightarrow H$ heißt ON-Folge $$:\Leftrightarrow\forall n,m\in\mathbb{N}:\left\langle b(n),b(m)\right\rangle=\delta_{nm}$$

>[!thm] Theorem 4.19
>$b_{1},...,b_{n}\in H$, $\left\langle b_{i},b_{j}\right\rangle=0$, dann: $$\left\lVert\sum\limits_{i=1}^{n}b_{i}\right\rVert^{2}=\sum\limits_{i=1}^{n}\left\lVert b_{i}\right\rVert^{2}$$

>[!thm] Theorem 4.20
>Sei $b$ ONF in $H$, $x\in\mathbb{K}^{\mathbb{N}}$, dann $$\sum\limits_{n=1}^{\infty}x_{n}b_{n}\text{ existiert in }H\Leftrightarrow\sum\limits_{n=1}^{\infty}x_{n}^{2}\text{ existiert in }\mathbb{K}$$

>[!thm] Theorem 4.21: Besselsche Ungleichung
>$H$ HR. $b:\mathbb{N}\rightarrow H$ ONF, dann $\forall f\in H$: $$\sum\limits_{n=1}^{\infty}(\left\langle f,b_{n}\right\rangle)^{2}\le\left\lVert f\right\rVert^{2}$$

>[!def] Definition 4.22: Hilbert-Basis
>Eine **Hilbert-Basis** von $H$ ist eine ONF mit $$(\left\langle f,b_{n}\right\rangle=0\quad\forall n\in\mathbb{N}\Rightarrow f=0)\qquad\forall f\in H$$
>($\Leftrightarrow(b(\mathbb{N})^{\perp}=\{0\}$)

>[!thm] Theorem 4.24
>Sei $b$ ONF in $H$. TFAE:
>1. $b$ Hilbert-Basis
>2. $\text{cl}(\text{span }b(\mathbb{N}))=H$ ($b$ keine algebraische Basis)
>3. $\forall f\in H:f=\sum\limits_{n=1}^{\infty}\left\langle f,b_{n}\right\rangle b_{n}$
>4. $\left\langle f,g\right\rangle=\sum\limits_{n\in\mathbb{N}}\left\langle f,b_{n}\right\rangle\left\langle b_{n},g\right\rangle$
>5. "$=$" in Besselscher Ugl.

>[!exp] Beispiel 4.25
>$$l_{2}:=\{x:\mathbb{N}\rightarrow\mathbb{R}\vert\sum\limits_{i=1}^{\infty}x_{i}^{2}\lt\infty\}$$
>Hilbertbasis: $\{\delta_{i}\vert i\in\mathbb{N}\}$, $\forall i\in\mathbb{N}:\delta_{i}(j)=\delta_{ij}\quad\forall j\in\mathbb{N}$.

>[!thm] Theorem 4.27
>In $H=L_{2}([-\pi,\pi])$ betrachten wir $u_{n}:[-\pi,\pi]\rightarrow\mathbb{R}$ mit $$\begin{align*}
&u_{0}(x)=\frac{1}{\sqrt{2\pi}}\qquad u_{2n-1}(x)=\frac{1}{\sqrt{\pi}}\cos(nx)\\[12pt]
&u_{2n}(x)=\frac{1}{\sqrt{\pi}}\sin(nx)
\end{align*}$$
>Dann ist $(u_{n})_{n\in\mathbb{N}}$ eine Hilbert-Basis. Also lässt sich jedes $f\in H$ in eine Reihe entwickeln, $$\begin{align*}
&f(x)=\frac{a_{0}}{2}+\sum\limits_{n=1}^{\infty}(a_{n}\cos(nx)+b_{n}\sin(nx))=\sum\limits_{n=0}^{\infty}\left\langle f,u_{n}\right\rangle u_{n}
\end{align*}$$mit $a_{0}=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\dd x=2\left\langle f,u_{0}\right\rangle u_{0}$.

>[!def] Def.: Von beschränkter Variation
>$f:[-\pi,\pi]\rightarrow\mathbb{R}$ heißt **von beschränkter Variation** falls $\exists M\gt0$, sodass für jede Zerlegung $$-\pi=x_{0}\lt x_{1}\lt...\lt x_{k-1}\lt x_{k}=\pi$$von $[-\pi,\pi]$ gilt: $$\sum\limits_{i=1}^{k}\left\lVert f(x_{i})-f(x_{i-1})\right\rVert\le M$$

>[!thm] Satz 4.28
>Ist $f$ von beschr. Var., periodisch ($f(\pi)=f(-\pi)$) und die Fortsetzung von $f$ auf $\mathbb{R}$ in $x\in\mathbb{R}$ stetig, dann konvergiert die Fourierreihe punktweise gegen $f$ in $x\in\mathbb{R}$.

>[!thm] Satz 4.29
>Ist $f:[-\pi,\pi]\rightarrow\mathbb{R}$ mit $f(\pi)=f(-\pi)$, stetig und stückw. stetig diff'bar, dann konvergiert die Fourierreihe gleichmäßig gegen $f$. ($f\leftrightarrow$ period. Forts. von $f$)

>[!exp] Gegenbeispiel zu 4.28 und 4.29
>$$x\mapsto x\sin\left(\frac{1}{x}\right)$$

>[!exp] Besp. 4.30
>$$f(x)=\begin{cases}
0, & -\pi\le x\lt0 \\
 \\
\pi, & 0\le x\le\pi
\end{cases}$$
>