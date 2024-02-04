---
time: 17.10.2023 13:35
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Grundlegende Begriffe zu Differentialgleichungen

[[P3.3 Analysis III]]

>[!def] Generelles Setting
$m,k\in\mathbb{N}^{*}$, $U$ offen und zsh. in $\mathbb{R}^{m}$, $$V_{n}:=\mathcal{C}^{n}(U,\mathbb{R}^{k}),\qquad W\subset U\times\mathbb{R}^{M}$$
Lösungsraum: $$L_{W}:=\{u\in V_{n}\vert(x,u(x),u'(x),u''(x),...,u^{(n)}(x))\in W\forall x\in U\}$$

>[!exp] Beispiel
>$\Delta u:=\text{tr}(D^{2}u)=\sum\limits_{l=1}^{m}\partial_{l}^{2}u\ge0$. Dementsprechend enthält $W$ alle $u$, die in der vierten Komponente Spur größer $0$ haben.

>[!note] Beobachtung
>Falls $W$ abg. in $U\times\mathbb{R}^{m}$ gibt es $\alpha:U\times\mathbb{R}^{m}\rightarrow\mathbb{R}$ stetig mit $W=\alpha^{-1}(\{0\})$, z.B. $\alpha:=\text{dist}(W,\cdot)$. Falls $\text{int }W=\emptyset$, nennt man $L_{W}$ Lösungsmenge zu Differentialgleichung.

>[!mot] Fokus auf Systeme gewöhlicher DGLs (ODEs/ODE Systems)
>$\text{int }W=\emptyset$, $m=1$. Beispiel: $$u'=(u'')^{2}$$

>[!mot] Fokus auf Gleichungen in Normalform (Auflösen nach höchster Ableitungsordnung)
>Sei $I\subset\mathbb{R}$ Intervall, $N=k\cdot n$, $X\subset\mathbb{R}^{N}$, $f:I\times X\rightarrow\mathbb{R}^{n}$. $$u^{(n)}(t)=f(t,u(t),u'(t),...,u^{(n-1)}(t))\forall t\in I$$
>(Hier: $W=(\text{pr}_{n+1}-f)^{-1}(\{0\})$)
>Sonderfall: $u'(t)=f(t,u(t))$ (1. Ordnung)

>[!exp] Beispiele
>1. $n=1$, $f$ unabh. von 2. Komponente. $$\begin{align*}
&u'(t)=f(t)&&u(t_{0})=u_{0}\\[12pt]
\Rightarrow\quad&u(t)=u_{0}+\int_{t_{0}}^{t}f(s)\dd s\\[12pt]
&L_{\star}=\left\{c+\int_{t_{0}}f(s)\dd s\right\}
\end{align*}$$
>2. $u'=cu\Rightarrow u(t)=Ke^{ct}$ für ein $k\in\mathbb{R}$. Beweis der Eindeutigkeit: $$\frac{u'}{u}=(\ln(u))'\stackrel{!}{=}c$$
>3. $u''=cu$. $$u=\begin{cases}
&c\lt0&&\text{LK von }\sin\&\cos\\ \\
&c\gt0&&\text{LK von }\sinh\&\cosh
\end{cases}$$
>Zurückführen auf System erster Ordnung: $$\begin{pmatrix}u \\ v\end{pmatrix}'=\begin{pmatrix}v \\ cu\end{pmatrix}$$

## Backlinks 
```dataview
TABLE summary AS Zusammenfassung, time AS "Time of Creation"
FROM #mitschrift
WHERE contains(summary, this.file.name)
```