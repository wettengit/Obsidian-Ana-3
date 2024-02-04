---
time: 04.02.2024 00:21
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Selbstadjungierte kompakte Operatoren

>[!thm] Lemma 4.121
>Sei $H$ HR und $T\in\text{CL}(H,H)$ selbstadjungiert. Dann ist $$\left\lVert T\right\rVert=\sup_{x\in H,\left\lVert x\right\rVert=1}|\left\langle Tx,x\right\rangle|$$

>[!thm] Theorem 4.122
>Sei $H$ HR und $T\in\text{CL}(H,H)$ selbstadjungiert. Sei $c\gt0$ mit $$|\left\langle Tx,x\right\rangle|\le c\left\lVert x\right\rVert^{2}.$$
>Dann ist $\left\lVert T\right\rVert\le c$.

>[!thm] Theorem 4.123
>Sei $H$ HR und $T\in K(H)$ selbstadjungiert. Dann ist $\left\lVert T\right\rVert$ oder $-\left\lVert T\right\rVert$ ein Eigenwert von $T$.

>[!thm] Theorem 4.124: Spektralsatz
>Sei $H$ HR und $T\in K(H)\setminus\{0\}$ selbstadjungiert. Dann gilt
>1. **Entweder** $T$ hat endlich viele EW: $$\left\lVert T\right\rVert=|\lambda_{1}|\ge|\lambda_{2}|\ge...\ge|\lambda_{N}|,\qquad N\in\mathbb{N}$$
>2. **Oder** $T$ hat abzählbar unendlich viele EW $\lambda_{n}\ne0$. Dann ist $$\lim_{n\rightarrow\infty}\lambda_{n}=0.$$
>
>Es gibt ein ONS aus EV $(u_{1},...,u_{n})$ bzw. $(u_{n})_{n}$ mit $$\forall x\in H:x=\sum\limits_{n=1}^{N}\left\langle x,u_{n}\right\rangle u_{n}+x_{0}\text{ bzw. }x=\sum\limits_{n=1}^{\infty}\left\langle x,u_{n}\right\rangle u_{n}+x_{0}$$wobei $x_{0}\in\ker T=\text{span}(u_{1},...)^{\perp}$ und $$T x=\sum\limits_{n=1}^{N}\lambda_{n}\left\langle x,u_{n}\right\rangle u_{n}\quad\text{bzw. }\quad T x=\sum\limits_{n=1}^{\infty}\lambda_{n}\left\langle x,u_{n}\right\rangle u_{n}$$
>Ist $\ker T=\{0\}$, ist $(u_{n})_{n}$ eine Hilbertbasis zu $H$.

>[!thm] Korollar 4.125
>Für $T\in\text{CL}(H,H)$ s.a. ist $$\sigma(T)\subset\mathbb{R}$$

>[!thm] Korollar 4.126
>Sei $T\in\text{CL}(H,H)$ kompakt und selbstadjungiert. Sei $0\not\in\sigma_{p}(T)$. Sei außerdem $\#\sigma_{p}(T)=\infty$. Dann ist $0\in\sigma_{c}(T)$.

