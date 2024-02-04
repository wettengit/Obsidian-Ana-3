---
time: 09.01.2024 13:36
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Kompakte Operatoren und schwache Konvergenz

>[!def] Def.
>$X$, $Y$ BR.
>$$CL(X,Y):=\{f\in\text{Abb}(X,Y)\vert f\text{ stetig, linear}\}$$

>[!def] Def. 4.95
>Sei $B$ $\mathbb{C}$-BR. $u:\mathbb{N}\rightarrow B$ heißt **schwach-konvergent** $$:\Leftrightarrow f\circ u\text{ konvergent }\forall f\in\text{CL}(B,\mathbb{C})=B^{*}$$
>(schwächer als Konvergenz)

>[!bem] Bemerkung
>Falls $B$ Hilbertraum, dann $u:\mathbb{N}\rightarrow B$ schwach-konvergent $$\Leftrightarrow\left\langle v,u(n)\right\rangle\xrightarrow[\,n_{\infty}\,]{}\left\langle v,u_{\infty}\right\rangle\forall v\in B$$
>(Darstellungssatz Fréchet-Riesz)
>Wir bezeichnen für $f\circ u\xrightarrow[\,n_{\infty}\,]{}f(u_{\infty})\forall f\in B$: $$u_{n}\xrightharpoonup[n_{\infty}]{}u_{\infty}$$

>[!bem] Behauptung
>Falls $u:\mathbb{N}\rightarrow H$ HR, $u(n)\in B(0,r)\forall n\in\mathbb{N}$ und $u(n)\xrightharpoonup[\,n_{\infty}\,]{}u_{\infty}\in H$. Dann $u_{\infty}\in\overline{B}(0,r)$.

>[!exp] Beispiel 4.97
>$$l_{2}:=\left\{x:\mathbb{N}\rightarrow\mathbb{C}:\sum\limits_{n=1}^{\infty}|x_{n}|^{2}\lt\infty\right\}$$
>mit SP $$\left\langle x,y\right\rangle:=\sum\limits_{n=1}^{\infty}\overline{x_{n}}y_{n}$$
>$X:\mathbb{N}\rightarrow l_{2}$ beschränkt, $$\exists c\gt0:\left\lVert X(n)\right\rVert\le c\quad\forall n\in\mathbb{N}$$
>$X$ konvergiert in $l_{2}$ schwach gegen $x^{*}$ $$\Leftrightarrow\forall k\in\mathbb{N}:\left\langle X(n),\delta_{k}\right\rangle\xrightarrow[\,n_{\infty}\,]{}x^{*}_{k}$$
>z.B. $X(n)=\delta_{n}\xrightharpoonup[\,n_{\infty}\,]{}0$.

>[!thm] Satz 4.98: Schwacher Bolzano-Weierstraß
>Jede beschränkte Folge in einem HR $H$ enthält eine schwach konvergente Teilfolge.

>[!def] Def. 4.111
>Seien $B,B'$ Banachräume, $T\in\text{CL}(B,B')$ heißt kompakt $$:\Leftrightarrow\forall r\gt0:\forall x:\mathbb{N}\rightarrow B(0,r):n\mapsto(T\circ x)(n)\text{ hat konv. TF}$$
>Wollen also: Bild von beschränkten Teilmengen ist präkompakt (unter Abschluss kpt)
>Wir definieren $$K(B):=\{T\in\text{CL}(B,B):T\text{ kpt}\}$$

>[!thm] Thm. 4.112
>$T:B\rightarrow B$ ist kpt $\Rightarrow\overline{T(B(0,1))}$ kpt.

>[!exp] Beispiel 4.113
>Sei $l_{2}$ wie oben, aber $\mathbb{C}\rightsquigarrow\mathbb{K}$. $T=\mathbb{1}_{l_{2}}$ ist nicht kpt: $B(0,1)$ enthält Folge $n\mapsto\delta_{n}$ ohne konv. TF

>[!exp] Beispiel/Satz 4.114
>$K:[a,b]\times[a,b]\rightarrow\mathbb{C}$ stetig. $$T:L^{2}([a,b])\rightarrow L^{2}([a,b]):f\mapsto\int_{a}^{b}K(\cdot,s)f(s)\dd s$$
>kompakt.

>[!thm] Lemma 4.115
>Sei $H$ HR, $T\in K(H)$ und $$E_\lambda:=\ker(T-\lambda\mathbb{1})$$der Eigenraum zu $\lambda$. Dann gilt für $\lambda\ne0$: $\dim E_{\lambda}\lt\infty$.

>[!thm] Theorem 4.117
>Sei $H$ $\mathbb{C}$-HR und $T\in K(H)$. Sei $\varepsilon\gt0$. Dann gibt es endlich viele linear unabh. EV zu EW $\lambda\in\sigma_{p}(T)$ mit $|\lambda|\lt\varepsilon$.

