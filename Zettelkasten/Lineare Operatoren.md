---
time: 02.02.2024 16:02
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Lineare Operatoren

>[!def] Definition 4.80: Linearer Operator
>Sei $H$ HR, ${0}\ne D\subset H$. $T:D\rightarrow H$ linear heißt **linearer Operator in $H$**.

>[!exp] Beispiele 4.81, 4.82
>1. $H=L^{2}([a,b])$, $D=\mathcal{C}^{0}([a,b])$. Operatoren mit stetigem Integralkern sind stetig, d.h. für $K:[a,b]^{2}\rightarrow\mathbb{C}$ stetig ist $$(Tf)(x):=\int_{a}^{b}K(x,y)f(y)\dd y\qquad\forall x\in[a,b]\qquad\forall f\in D$$ beschränkt mit $$\left\lVert T\right\rVert\le\sup_{x,y\in[a,b]}|K(x,y)|(b-a)$$
>2. [[Sturm-Liouville-Operatoren]] sind linear, aber im allgemeinen nicht stetig.

>[!thm] Theorem 4.83
>Sei $H$ HR, $D\subset H$ dicht, $T:D\rightarrow H$ beschränkter linearer Operator. Dann gilt $$\#\{\overline{T}\in\text{CL}(H,H):\overline{T}\vert_{D}=T\}=1$$Außerdem $\left\lVert\overline{T}\right\rVert=\left\lVert T\right\rVert$.

>[!def] Definition: Adjungierte
>Sei $H$ HR, $T:H\rightarrow H$ linearer Operator. $T^{*}:H\rightarrow H$ heißt die **Adjungierte** zu $T$ $$:\Leftrightarrow\left\langle Tf,g\right\rangle=\left\langle f,T^{*}g\right\rangle\qquad\forall f,g\in H$$
>Es gilt $(T^{*})^{*}=T$.

>[!def] Definition 4.87: Hermitesch und selbstadjungiert
>Sei $H$ HR, $D\subset H$ dicht, $T:D\rightarrow H$ linearer Operator. $T$ heißt **hermitesch** $$:\Leftrightarrow\left\langle Tf,g\right\rangle=\left\langle f,Tg\right\rangle\qquad\forall f,g\in H$$Falls $D=H$, heißt $T$ **selbstadjungiert**.

>[!thm] Theorem 4.84
>Sei $H$ HR, $T:H\rightarrow H$ beschränkter Operator. Dann existiert eine Adjungierte $T^{*}:H\rightarrow H$ zu $T$, wobei $\left\lVert T\right\rVert=\left\lVert T^{*}\right\rVert$, d.h. $T^{*}$ beschränkt.

>[!def] Definition 4.86: Fourier-Transformation
>Für $f\in L^{1}(\mathbb{R})$ definieren wir die **Fourier-Transformierte** von $f$: $$\hat f:\mathbb{R}\rightarrow\mathbb{C},\quad y\mapsto\frac{1}{2\pi}\int_{\mathbb{R}}f(x)e^{-ixy}\dd x$$
>$\hat f$ ist beschränkt durch $\frac{1}{\sqrt{2\pi}}\left\lVert f\right\rVert_{1}$ und auch stetig.
>Wir definieren die **Fourier-Transformation**, den Operator $T:L^{1}(\mathbb{R})\rightarrow L^{2}(\mathbb{R})$. Dieser ist laut der Plancherel-Gleichung beschränkt, sogar eine Isometrie.
>Sei $$\mathcal{C}_{0}^{\infty}:=\{f\in\mathcal{C}^{\infty}(\mathbb{R},\mathbb{C}):\text{supp }f\text{ kpt}\}\subset L^{1}(\mathbb{R})$$
>Offenbar gilt $\text{cl}(\mathcal{C}_{0}^{\infty})=L^{2}(\mathbb{R})$, somit gibt es eine stetige Erweiterung zu $T$. Außerdem ist die Adjungierte $T^{*}$ zu $T$ definiert durch $$T^{*}g:=\frac{1}{\sqrt{2\pi}}\int_{\mathbb{R}}e^{ixy}g(x)\dd x=\overline{T\overline{g}}\qquad\forall g\in\mathcal{C}_{0}^{\infty}$$
>$T$ ist offenbar unitär.

>[!thm] Theorem 4.90: Toeplitz-Kriterium
>Sei $H$ HR, $T\in\text{CL}(H,H)$. TFAE:
>1. Es existiert eine Inverse $T^{-1}\in\text{CL}(H,H)$ mit $TT^{-1}=\text{id}_{H}$
>2. $\exists d\gt0:\forall x\in H:\left\lVert Tx\right\rVert\ge d\left\lVert x\right\rVert$ und $\ker T^{*}={0}$
