---
time: 12.11.2023 16:10
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# ODE-Koordinatentransformationen

>[!thm] Theorem 1.5.1
>Sei $J\subset\mathbb{R}$ Intervall, $X\subset\mathbb{R}^{n}$ offen, $f:J\times X\rightarrow\mathbb{R}^{n}$ stetig. $D_{2}f$ stetig $\Rightarrow$ LLZ in zweiter Komponente. Sei $Y\subset\mathbb{R}^{n}$, $\phi:J\times Y\rightarrow X$ stetig und dif'bar. $D_{2}\phi\in\text{GL}(n,\mathbb{R})$. Sei $I\subset J$ Intervall, $y:I\rightarrow Y$ löse $$\begin{align*}
&y'(t)=(D_{2}\phi(t,y(t)))^{-1}(f(t,\phi(t,y(t)))-D_{1}\phi(t,y(t)))\\[12pt]
\Leftrightarrow\,&f(t,\phi(t,y(t)))=D_{1}\phi(t,y(t))+D_{2}\phi(t,y(t))y'(t)=\frac{d}{dt}\phi(t,y(t))
\end{align*}$$
>Dann gilt: $x:I\rightarrow X,x(t)=\phi(t,y(t))\forall t\in I$ löst $x'(t)=f(t,x(t))$.

>[!exp] Beispiel 1.5.2
>$X=Y=J=(0;\infty)$. Sei $f:J\times J\rightarrow\mathbb{R}$ homogen vom Grad $0$, d.h. $f(\lambda t,\lambda x)=f(t,x)\quad\forall\lambda,t,x\in J$. Sei $\phi:J\times J\rightarrow X,\phi(t,y)=ty\forall(t,y)\in J\times J$, dann transformiert sich $$x'(t)=f(t,x(t)),\quad x(t_{0})=x_{0}$$zu $$y'(t)=\frac{1}{t}(f(t,y(t))-y(t)),\quad y(t_{0})=\frac{x_{0}}{t_{0}}$$

>[!exp] Beispiel 1.5.3: $\text{SO}(n)$-Symmetrie
>$I=\mathbb{R}$, $X=\mathbb{R}^{2}$, $Y=(0,\infty)\times\mathbb{R}$. Sei $f:\mathbb{R}^{2}\rightarrow\mathbb{R}^{2}$ diff'bar und $\text{SO}(2)$-invariant: $$f(S_{\theta}x)=S_{\theta}f(x)\forall x\in\mathbb{R}^{2}\forall\theta\in\mathbb{R},\qquad S_{\theta}=\begin{pmatrix}\cos\theta & -\sin\theta \\ \sin\theta & \cos\theta\end{pmatrix}$$
>d.h. "$f=f(r)$", also $\exists g,h:\mathbb{R}\rightarrow\mathbb{R}$ in $\mathbb{R}\setminus\{0\}$ $\mathcal{C}^{1}$, sodass $$f(x)=g(\underbrace{x_{1}^{2}+x_{2}^{2}}_{r^{2}(t)})x+h(x_{1}^{2}+x_{2}^{2})ix\qquad\forall x\in\mathbb{R}^{2}$$
>Die Transformation ist gegeben durch Polarkoordinaten: $$\phi(r,\theta)=\begin{pmatrix}r\cos\theta \\ r\sin\theta\end{pmatrix}$$und entkoppelt das System: $$\begin{align*}
&r'(t)=g(r^{2}(t))r(t)&&(1)\\[12pt]
&\theta'(t))=h(r^{2}(t))&&(2)
\end{align*}$$
>Löse $(1)\rightsquigarrow(2)$.
