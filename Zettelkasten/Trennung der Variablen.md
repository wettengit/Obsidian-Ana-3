---
time: 19.10.2023 13:46
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Trennung der Variablen

>[!mot] Heuristik: Trennung der Variablen
>Sei $f(x,y)=g(x)\cdot h(y)$, sei $h(y)\ne0$. Die entsprechende [[Systeme gewöhnlicher Differentialgleichungen|DGL]] hat die Form $$y'(x)=g(x)h(y)$$
>Unter Nutzung der Leibniz-Notation lässt sich das mehr oder weniger schummelnd umformen zu
>$$\begin{align*}
&\frac{1}{h(y)}\dd y=g(x)\dd x\\[12pt]
&\int_{u_{0}}^{\cdot}\frac{1}{h(y)}\dd y=\int_{t_{0}}^{\cdot}g(x)\dd x
\end{align*}$$
>Sei $H$ Stammfunktion von $\frac{1}{h}$, $G$ Stammfkt. von $g$: $H'(u_{0})\ne0\Rightarrow$ [[Parametrisierungen und Auflösen von Gleichungen|lokal existiert Inverse]] von $H$: $$\varphi(x)=H^{-1}(G(x))$$(lokal, solange $G(x)\in H(\mathbb{R})$) Es gilt $H(\varphi(x))=G(x)$, dementsprechend $H'(\varphi(x))\cdot\varphi'(x)=G'(x)=g(x)$, also $$\varphi'(x)=g(x)h(\varphi(x))$$Also ist $\varphi$ eine Lösung der DGL.

>[!exp] Beispiel 1.3.2
>$$\begin{align*}
&y'(x)=\frac{1}{x}y(x),x\gt0\\[12pt]
&\frac{1}{y}\dd y=\frac{1}{x}\dd x\\[12pt]
&\ln(y)=\ln(x)+C\\[12pt]
&y=\pm\underbrace{e^{C}}_{\tilde C}x
\end{align*}$$

>[!exp] Beispiel 1.3.4
>$x'(t)=\sin(x(t)),\quad x(0)=1,\quad(t,x)\in\mathbb{R}\times(0,\pi)$. $f(t,x)=1\cdot\sin x\Rightarrow$ lok. LB $\checkmark\Rightarrow\exists!$ Lösung lokal.
>$$\begin{align*}
&\int_{1}^{x}\frac{\dd\chi}{\sin\chi}=\int_{1}^{t}\dd\tau+x(0)=t-1+\underbrace{C}=t
\end{align*}$$
>Linke Seite ist nicht mehr durch elementare Fkt. ausdrückbar.
>Asymptotik: $$\lim_{x\rightarrow\pi}\int_{0}^{x}\frac{\dd\chi}{\sin\chi}=\infty$$
>Also max. Lsg. auf ganz $\mathbb{R}$, $$\lim_{t\rightarrow\infty}x(t)=\pi,\qquad\lim_{t\rightarrow-\infty}x(t)=0.$$
