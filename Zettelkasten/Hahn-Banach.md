---
time: 16.01.2024 13:19
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Hahn-Banach

>[!thm] Theorem H1: Hahn-Banach
>Sei $X$ ein $\mathbb{R}$-VR mit:
>1. $p:X\rightarrow\mathbb{R}$ sublinear: $$\forall x,y\in X:\forall\alpha\in[0,\infty):\begin{cases}
p(x+y)\le p(x)+p(y)\ \\
p(\alpha x)=\alpha p(x)
\end{cases}$$
>2. $Y\subset X$ lin. UR, $f:Y\rightarrow\mathbb{R}$ linear
>3. $f(x)\le p(x)\forall x\in Y$
>
>Dann gibt es $F:X\rightarrow\mathbb{R}$ linear mit $$F\vert_{Y}=f\text{ und }F(x)\le p(x)\forall x\in X$$

>[!thm] Zorn's Lemma
>Sei $(N,\le)\ne\emptyset$ partiell geordnete Menge mit: Jede totalgeordnete Teilmenge $Y\subset N$ hat eine obere Schranke: $$\exists n\in N:n\ge y\quad\forall y\in Y$$
>Dann enthält $N$ ein maximales Element. $$\exists n^{*}\in N:n^{*}\ge n\quad\forall n\in N$$
>Bem.: Zorns Lemma $\Leftrightarrow$ [[Fraenkel- und Auswahl-Axiome|Auswahlaxiom]].

>[!thm] Theorem H2: Hahn-Banach für $\text{CL}(X)$
>Sei $X$ ein normierter $\mathbb{K}$-VR und $Y\subset X$ linearer Unterraum (mit induzierter Norm). $$\forall y'\in Y':\exists x'\in X':x'\vert_{Y}=y'\land\left\lVert x'\right\rVert=\left\lVert y'\right\rVert$$

>[!thm] Theorem H3:
>Sei $X$ normierter Raum, sei $Y\subset X$ abgeschlossener linearer Unterraum. Sei $x_{0}\in X\setminus Y$. Dann $\exists x'\in X':$ $$x'=0\text{ auf }Y,\left\lVert x'\right\rVert_{X'}=1,\quad x'(x_{0})=\text{dist}(x_{0},Y):=\inf\{\left\lVert x_{0}-y\right\rVert:y\in Y\}$$

>[!thm] Theorem H4:
>Sei $X$ normierter Raum, sei $x_{0}\in X$:
>1. Für $$x_{0}\ne0:\exists x_{0}'\in X':\left\lVert x_{0}'\right\rVert_{X'}=1\text{ und }x_{0}'(x_{0})=\left\lVert x_{0}\right\rVert_{X'}(\ne0)$$
>2. Falls $x'(x_{0})=0\quad\forall x'\in X'$: $x_{0}=0$
>3. $(\text{ev}_{x_{0}}:x'\mapsto x'(x_{0}))\in\text{CL}(X',\mathbb{K})=X''$ mit $\left\lVert\text{ev}_{x_{0}}\right\rVert_{X''}=\left\lVert x_{0}\right\rVert_{X}$
