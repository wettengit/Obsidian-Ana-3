---
time: 02.02.2024 15:43
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Beschränkte lineare Transformationen

>[!def] Definition 4.64: Operatornorm und beschränkte Operatoren
>Seien $V,W$ normierte Räume, $A:V\rightarrow W$ linear. Wir definieren die **Operatornorm** $$\left\lVert A\right\rVert:=\sup_{f\in V\setminus{0}}\frac{\left\lVert Af\right\rVert}{\left\lVert f\right\rVert}=\sup_{g\in V,\left\lVert g\right\rVert=1}\left\lVert Ag\right\rVert$$
>$A$ heißt **beschränkt** $$:\Leftrightarrow\left\lVert A\right\rVert\lt\infty$$

>[!exp] Beispiel 4.65
>$$\begin{align*}
&\text{1)}\qquad\left\lVert\text{id}\right\rVert=1\\[12pt]
&\text{2)}\qquad\left\lVert A\right\rVert=0\Leftrightarrow A=0\\[12pt]
&\text{3)}\qquad\mathcal{P}\text{ Projektion}\Rightarrow\left\lVert\mathcal{P}\right\rVert=1\lor\mathcal{P}=0
\end{align*}$$

>[!thm] Theorem 4.67
>Seien $V,W$ normierte Räume und $A:V\rightarrow W$ linear. Dann gilt $$A\text{ stetig}\Leftrightarrow A\text{ beschränkt}$$

>[!thm] Theorem 4.71
>$V,W$ normierte Räume. Sei $V$ endlichdim. Dann ist $V$ ein Banachraum und jede lineare Abbildung $A:V\rightarrow W$ ist stetig.

>[!def] Definition 4.73: Dualraum
>Sei $\mathcal{H}$ $\mathbb{K}$-HR. Der Dualraum zu $\mathcal{H}$ ist $$\mathcal{H}^{*}:=\{A:\mathcal{H}\rightarrow\mathbb{K}\vert A\text{ linear und stetig}\}$$  $A\in\mathcal{H}^{*}$ heißt stetiges, lineares Funktional.

>[!thm] Theorem 4.75: Darstellungssatz/Riesz-Fréchet
>Sei $\mathcal{H}$ $\mathbb{K}$-HR und $A$ beschränktes lineares Funktional. Dann gilt $$\exists!g\in\mathcal{H}:Af=\left\langle g,f\right\rangle\qquad\forall f\in\mathcal{H}$$
>Man nennt $g$ erzeugendes Element von $A$, ferner gilt $\left\lVert A\right\rVert=\left\lVert g\right\rVert$.

>[!bem] Bemerkung 4.78
>$$\begin{align*}
&\text{1) }\qquad(L^{p})^{*}\simeq L^{p^{*}}\\[12pt]
&\text{2) }\qquad(L^{p})^{*}\simeq L^{p}\Leftrightarrow p=2
\end{align*}$$
>Hilberträume sind reflexiv, d.h. $(\mathcal{H}^{\star})^{\star}\simeq\mathcal{H}$, sogar selbstdual.
