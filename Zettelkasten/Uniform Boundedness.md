---
time: 11.01.2024 13:27
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Uniform Boundedness

>[!thm] Theorem U1: Baire'sches Kategorientheorem
>$X\ne\emptyset$ vollst. metr. Raum.
>$$\begin{align*}
&X=\bigcup_{k\in\mathbb{N}}A_{k,\qquad}A_{k}\text{ abg in }X\quad\forall k\in\mathbb{N}\\[12pt]
&\Rightarrow\exists k\in\mathbb{N}:\stackrel{\circ}{A}_{k}:=\text{int}(A_{k},X)\ne\emptyset
\end{align*}$$
>Bem.: Vollst. unverzichtbare Bed.: sonst $X=\mathbb{Q}$, $A_{k}$ einelementig.

>[!thm] Theorem U2: Uniform Boundedness Principle
>$X\ne\emptyset$ vollst. metr. Raum, $Y$ normierter Raum. Sei $$\mathcal{F}\subset\mathcal{C}^{0}(X,Y)\text{ mit }\sup\{\left\lVert f(x)\right\rVert_{Y}:f\in\mathcal{F}\}\lt\infty\quad\forall x\in X$$
>("beschränkte Orbiten") Dann $\exists x_{0}\in X:\exists\varepsilon_{0}\gt0:$ $$\sup\left\{\left\lVert f\vert_{\overline{B}(x_{0},\varepsilon_{0})}\right\rVert_{\infty}:f\in\mathcal{F}\right\}\lt\infty$$

>[!thm] Theorem U3: Banach-Steinhaus-Theorem
>Sei $X$ Banachraum, $Y$ normierter Raum. Sei $$\mathcal{T}\subset\text{CL}(X,Y)\text{ mit }\sup_{T\in\mathcal{T}}\left\lVert Tx\right\rVert_{Y}\lt\infty\quad\forall x\in X$$
>Dann: $\mathcal{T}$ beschränkt in $\text{CL}(X,Y)$ (mit Operatornorm), d.h. $$\sup\{\left\lVert T\right\rVert_{\text{CL}(X,Y)}:T\in\mathcal{T}\}\lt\infty$$

>[!def] Notation U4
>Sei $X$ normierter Raum, $x\in X$, $x\in X'$. $$\left\langle x,x'\right\rangle_{X}:=x'(x)$$
>$X$ Hilbertraum: $$R_{X}:X\xrightarrow{\simeq} X',x\mapsto\left\langle\cdot,x\right\rangle$$
>Dann $$\begin{align*}
&\left\langle x,y\right\rangle_{X}=\left\langle x,R_{X}(y)\right\rangle_{X}\quad\forall x,y\in X\\[12pt]
&\left\langle x,x'\right\rangle_{X}=\left\langle x,R_{X}^{-1}x'\right\rangle_{X}\quad\forall x\in X,x'\in X'
\end{align*}$$

>[!thm] Theorem U5
>Sei $X$ Banachraum, $Y$ normierter Raum. Sei $\mathcal{T}\subset\text{CL}(X,Y)$ mit $\forall x\in X\forall y\in Y':$ $$\sup\{|\left\langle Tx,y'\right\rangle_{Y}|:T\in\mathcal{T}\}\lt\infty$$
>Dann ist $\mathcal{T}$ beschränkt in $\text{CL}(X,Y)$.

>[!def] Definition U6
>Seien $X,Y$ top. Räume, $f:X\rightarrow Y$ heißt offen $$:\Leftrightarrow f(U)\text{ offen }\forall U\subset X\text{ offen}$$

>[!thm] Theorem U7: Open Mapping Theorem
>Seien $X,Y$ Banachräume, $T\in\text{CL}(X,Y)$. Dann: $$T\text{ surjektiv }\Leftrightarrow T\text{ offen}$$

>[!thm] Theorem U8: Inverse Mapping Theorem
>Seien $X,Y$ Banachräume, $T\in\text{CL}(X,Y)$. Dann: $$T\text{ bijektiv }\Leftrightarrow T^{-1}\text{ stetig}$$

>[!thm] Theorem U9: Closed Graph Theorem
>Seien $X,Y$ Banachräume, $T:X\rightarrow Y$ linear. Dann: $$T\subset X\times Y:=\{(x,T(x)):x\in X\}\text{ abgeschlossen }\Leftrightarrow T\text{ stetig}$$

>[!exp] Beispiel U10:
>Adjungierte: $X,Y$ Banachräume, $A:X\rightarrow Y$, $B:Y'\rightarrow X'$ linear. Falls $\forall x\in X:\forall y'\in Y':\left\langle Ax,y'\right\rangle_{Y}=\left\langle x,By'\right\rangle_{X}$, dann $A,B$ stetig. Insbesondere sind selbstadjungierte Operatoren auf Hilberträumen immer stetig.
