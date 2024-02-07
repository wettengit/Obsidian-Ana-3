---
time: 02.02.2024 15:17
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Banachräume

>[!def] Definition: Normen und Banachräume
>Sei $U$ $\mathbb{K}$-[[Vektorräume|Vektorraum]]. $\left\lVert\cdot\right\rVert:U\rightarrow[0,\infty)$ heißt **Norm** $:\Leftrightarrow\forall u,v\in U,\lambda\in\mathbb{K}$ gilt
>1. $\left\lVert u\right\rVert=0\Leftrightarrow u=0$
>2. $\left\lVert\lambda u\right\rVert=|\lambda|\left\lVert u\right\rVert$
>3. $\left\lVert u+v\right\rVert\le\left\lVert u\right\rVert+\left\lVert v\right\rVert$
>
>$(U,\left\lVert\cdot\right\rVert)$ heißt [[Normierte Räume|normierter Raum]], falls vollständig, **Banachraum**.

>[!thm] Theorem 4.41: Algebraische Kriterien für Endlichdimensionalität
>Sei $U$ $\mathbb{K}$-VR. TFAE:
>1. $\dim U\lt\infty$
>2. Jede injektive lineare Abbildung von $U\rightarrow U$ ist surjektiv.
>3. Jede surjektive lineare Abbildung von $U\rightarrow U$ ist injektiv.
>4. Wenn $V\subseteq U$ linearer Unterraum ist und eine bijektive Abbildung von $V\rightarrow U$ existiert, dann $U=V$

>[!thm] Theorem 4.43: Topologische Kriterien für Endlichdimensionalität
>Sei $U$ $\mathbb{K}$-VR. TFAE:
>1. $\dim U\lt\infty$
>2. Alle Normen auf $U$ sind äquivalent
>3. Jede beschränkte Folge in $U$ hat eine konvergente Teilfolge
>4. Jeder lineare Unterraum von $U$ ist abgeschlossen
>5. Jede lineare Abbildung von $U\rightarrow\mathbb{K}$ ist stetig.

>[!def] Definition: $\mathcal{L}^{p}$-Räume und $L^{p}$-Räume
>Sei $I\subset\mathbb{R}$ Intervall. Für $p\in[1,\infty)$ definieren wir $$\mathcal{L}^{p}(I):=\left\{f:I\rightarrow\mathbb{R}:\int_{I}|f(x)|^{p}\dd x\lt\infty\right\}$$
>und $$\left\lVert\cdot\right\rVert^{p}:=\left(\int_{I}|\cdot|^{p}\right)^{\frac{1}{p}}$$
>$\left\lVert\cdot\right\rVert_{p}$ ist eine Pseudonorm auf $\mathcal{L}^{p}(I)$. Wir setzen $$\mathcal{N}(I):=\{f\in\mathcal{L}^{p}(I):\mu(\text{supp }f)=0\}$$
>und definieren $$L^{p}(I):=\mathcal{L}^{p}(I)/\mathcal{N}(I).$$
>Funktionen, die fast überall gleich sind, haben den gleichen Repräsentanten in $L^{p}(I)$. $\left\lVert\cdot\right\rVert_{p}$ ist eine Norm auf $L^{p}(I)$.

>[!thm] Theorem 4.58: Fischer-Riesz
>Sei $p\in[1,\infty)$. Dann ist $(L^{p}(I),\left\lVert\cdot\right\rVert_{p})$ ein Banachraum.

>[!thm] Theorem 4.59: Hölder-Ungleichung
>Seien $p,q\in\mathbb{R}$ **Hölder-konjugiert**, d.h. $\frac{1}{p}+\frac{1}{q}=1$. Man schreibt $q=p^{*}$. Sei $f\in L_{p}(I)$, $g\in L_{q}(I)$. Dann gilt $f\cdot g\in L^{1}(I)$ und $$\left\lVert f\cdot g\right\rVert_{1}\le\left\lVert f\right\rVert_{p}\left\lVert g\right\rVert_{q}$$
