---
time: 12.11.2023 15:43
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Variation der Konstanten

>[!mot] Heuristik: Variation der Konstanten bei DGL erster Ordnung
>Affine DGL der Form: 
>$$y'=g(x)y+h(x),\quad y(x_0)=y_0$$
>mit $g,h:I\rightarrow\mathbb{R}$ stetig.
>Sei $G$ Stammfkt. von $g$. Die Partikulärlösung hat folgende Form: $$y(x)=c(x)e^{G(x)}$$wobei $$c(x)=\int^x h(\tilde x)e^{-G(\tilde x)}\dd\tilde x$$

>[!bem] Bemerkung
>$$y''+a_{1}(x)y'+a_{0}(x)y(x)=f(x)\qquad(\star)$$
>Sei $(y_{1},y_{2})$ FS der homogenen Gleichung. Ziel: konstruiere Lösung $y_{p}$ der inhomogenen Gleichung. Schreibe $$y_{p}(x)=c_{1}(x)y_{1}(x)+c_{2}(x)y_{2}(x)$$(Wahl einer vorteilhaften Basis) $$y_{p}'(x)=c_{1}'(x)y_{1}(x)+c_{1}(x)y_{1}'(x)+c_{2}'(x)y_{2}(x)+c_{2}(x)y_{2}'(x)$$
>Ansatz: $$c_{1}'(x)y_{1}(x)+c_{2}'(x)y_{2}(x)=0\qquad(i)$$
>Damit: $$\begin{align*}
&y_{p}'(x)=c_{1}(x)y_{1}'(x)+c_{2}(x)y_{2}'(x)\\[12pt]
&y_{p}''(x)=c_{1}'(x)y_{1}'(x)+c_{1}(x)y_{1}''(x)+c_{2}'(x)y_{2}'(x)+c_{2}(x)y_{2}''(x)
\end{align*}$$
>Einsetzen in $(\star)$ ergibt $$\begin{align*}
&c_{1}(\underbrace{y_{1}''+a_{1}y_{1}'+a_{0}y_{1}}_{=0})+c_{2}(\underbrace{y_{2}''+a_{1}y_{2}'+a_{0}y_{2}}_{=0})+c_{1}'y_{1}'+c_{2}'y_{2}'=f\\[12pt]
\Leftrightarrow\,&c_{1}'y_{1}'+c_{2}'y_{2}'=f\qquad(ii)
\end{align*}$$
>$(i)\land(ii)$ ist [[Lineare Gleichungssysteme|LGS]] für $c_{i}'$.

>[!bem] Bemerkung
>Erinnerung: [[Cramersche Regel]]: $\det A\ne0$, dann für alle $b\in\mathbb{K}^{n}$: $$(A^{-1}b)_{i}=\frac{\det A_{b,i}}{\det A}\quad\text{ mit }A_{b,i}=(A_{1},...,\underbrace{b}_{\text{Stelle }i},...,A_{n})$$
>Hier: $$\begin{pmatrix}y_{1} & y_{2} \\ y_{1}' & y_{2}'\end{pmatrix}\begin{pmatrix}c_{1}' \\ c_{2}'\end{pmatrix}=\begin{pmatrix}0 \\ f\end{pmatrix}$$
>Mit der Wronski-Determinante $W(x)=y_{1}(x)y_{2}'(x)-y_{2}(x)y_{1}'(x)$ folgt $$c_{1}'(x)=-\frac{y_{2}(x)f(x)}{W(x)},\qquad c_{2}'(x)=\frac{y_{1}(x)f(x)}{W(x)}$$

>[!thm] Theorem (Eq. 1.18o)
>Sei $$y^{(n)}+a_{n-1}(x)y^{(n-1)}(x)+...+a_{1}(x)y'(x)+a_{0}(x)y(x)=f(x)\qquad(\star)$$und außerdem $(y_{1},...,y_{n})$ das FS zur homogenen Gleichung.
>Dann: $y_p(x)=\sum_{i=1}^nc_i(x)y_i(x)$ löst $(\star)$, falls $$\begin{pmatrix}y_1(x)&...&y_n(x)\\...&...&...\\y_1^{(n-1)}(x)&...&y_n^{(n-1)}(x)\end{pmatrix}\begin{pmatrix}c_1'(x)\\...\\c_n'(x)\end{pmatrix}=\begin{pmatrix}0\\...\\f(x)\end{pmatrix}$$
>Es folgt $$y_p(x)=\sum_{j=1}^n(-1)^{n+j}y_j(x)\int_{x_0}^x\frac{W(y_1,...,y_{j-1},y_{j+1},...,y_n)}{W(y_1,...,y_n)}f(s)\dd s$$
