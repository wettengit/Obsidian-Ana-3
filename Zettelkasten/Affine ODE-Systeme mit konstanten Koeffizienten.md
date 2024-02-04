---
time: 12.11.2023 18:10
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Affine ODE-Systeme mit konstanten Koeffizienten

>[!def] Definition: Linearer Differentialoperator
>Sei $V_{k}:=\mathcal{C}^{\infty}(\mathbb{R},\mathbb{R}^{k})$. Ein **allgemeiner lineare Differentialoperator** auf $V_{k}$ ist (für $a\in\mathcal{C}^{\infty}(\mathbb{R},L(\mathbb{R}^{k},\mathbb{R}^{k})$): $$D_{a}:f\mapsto\left(t\mapsto\sum\limits_{j=1}^{n}a_{j}(t)f^{(j)}(t)\right)$$
>$n$ heißt die **Ordnung** des Diffops. $D_{a}\in L(V_{k},V_{k})$ (Ring mit $(+,\circ)$)
>$a$ ist LLZ mit $\left\lVert A(t)\right\rVert_{\text{op}}$. Wollen $\text{Ker }D_{a}$ bestimmen.

>[!mot] Setting
>Spezialfall: $a_{j}$ konstant, $a_{j}=\cdot z$ für ein $z\in\mathcal{C}$, $k=2$, $\mathbb{R}^{2}\simeq\mathbb{C}$. Sei $D:=\frac{d}{dt}$.

>[!thm] Theorem 1.4.1
>$$\Phi:(\text{Pol}(\mathbb{C}),+,\cdot)\rightarrow(L(V_{2},V_{2}),+,\circ),\quad\Phi(a_{0},...,a_{n})(f)=\sum\limits_{k=0}^{n}a_{k}f^{(k)}$$ist ein injektiver Ringhomomorphismus.
>Es gilt außerdem $$\forall P\in\text{Pol}(\mathbb{C}):\forall\lambda\in\mathbb{C}:P(D)e^{\lambda\cdot}=P(\lambda)e^{\lambda\cdot}.$$
>$a\in\text{Pol}(\mathbb{C})\Rightarrow\text{Ker }\Phi(a)=\text{Ker }\Phi(\frac{a}{a_{n}})$, also $\OE$ $a$ **normiert**, also $a_{n}=1$. Falls $a$ außerdem $n$ verschiedene Nullstellen $\lambda_{1},...,\lambda_{n}$ hat, dann ist $$\text{FS}_{\Phi(a)}:=\{e^{\lambda_{k}\cdot}\vert k\in\mathbb{N}_{n}^{*}\}$$
>**Fundamentalsystem** (d.h. Basis des Lösungsraums) von $\Phi(a)$.

>[!def] Definition: Wronski-Determinante
>Sei $(u_{1},...,u_{n})$ ein Tupel von Lösungen von $\Phi(a)=0$ mit $a$ normiert. Dann ist deren **Wronski-Determinante** $$W_{u}(t):=\begin{vmatrix}u_{1}(t) & ... & u_{n}(t) \\ u_{1}'(t) & ... & u_{n}'(t) \\ ... & ... & ... \\ u_{1}^{(n-1)}(t) & ... & u_{n}^{(n-1)}(t)\end{vmatrix}$$

>[!thm] Theorem 1.4.2
>Sei $P=\prod_{j=1}^{r}(x-\lambda_{j})^{k_{j}}$ bel. Polynom. Dann hat $P(D)u=0$ das FS $$\{\varphi_{jm}\vert j\in\mathbb{N}_{r}^{*},m\in\mathbb{N}_{k_{j}-1}\}\text{ mit }\varphi_{jm}(x):=x^{m}e^{\lambda_{j}x}$$

>[!def] Definition: Exponentialabbildung für Matrizen
>Sei $A\in\mathbb{K}^{n\times n}$. $$\exp:M_{n\times n}(\mathbb{K})\circlearrowleft,\quad A\mapsto\exp(A):=\sum\limits_{k=0}^{\infty}\frac{1}{k!}A^{k}$$

>[!thm] Theorem 1.4.3: Eigenschaften der Exponentialabbildung
>$$\begin{align*}
&\text{1) }&&\exp(0)=\mathbb{1}\\[6pt]
&&&(\exp(A))^{-1}=\exp(-A)\\[6pt]
&&&\text{insb. }\exp(\mathbb{K}^{n\times n})\subset\text{GL}(n,\mathbb{K})\\[12pt]
&\text{2) }&&\exp(A+B)=\exp(A)\cdot\exp(B)\text{ falls }[A,B]=0\\[12pt]
&\text{3) }&&\det(\exp(A))=\exp(\text{tr }A)\\[12pt]
&\text{4) }&&\exp(A)=\lim\limits_{n\rightarrow\infty}\left(\mathbb{1}+\frac{1}{n}A\right)^{n}\\[12pt]
&\text{5) }&&\exp(CAC^{-1})=C\exp(A)C^{-1}
\end{align*}$$

>[!bem] Bemerkung
>Sei $D=\text{diag}(\lambda_{1},...,\lambda_{n})$. Betrachte $y'=Dy$. Offenbar gilt $$y(t)=\begin{pmatrix}e^{\lambda_{1}t}c_{1} \\ ... \\ e^{\lambda_{n}t}c_{n}\end{pmatrix}=e^{Dt}\cdot c$$
>Sei nun $A$ diagonalisierbar mit $P^{-1}AP=D$ $\Rightarrow\exp(Dt)=P^{-1}\exp(At)P$

>[!thm] Lemma 1.4.4
>Sei $\Psi(t)=e^{Dt}c$ Lösung von $\Psi'=D\Psi$. Dann ist $\varphi=P\Psi$ Lösung von $y'=Ay$.

>[!bem] Bemerkung
>$Pe^{Dx}$ ist FS zu $y'=Ay$.

>[!bem] Bemerkung
>Seien nun $\lambda_{1},...,\lambda_{m}$ mit $\lambda_{j}\ne\lambda_{k}\forall j\ne k$, $1\le m\le n$ die Eigenwerte zur reellen Matrix $A$. Diese lassen sich aufteilen (bei komplexen Eigenwerten, welche konjugiert auftreten, nehmen wir den "oberen") in $$\begin{cases}
&\lambda_{j}\in\mathbb{R} & \forall j=1,...,p\\[12pt]
&\text{Im}(\lambda_{j})\gt0 & \forall j=p+1,...,p+q
\end{cases}$$wobei gilt $p+2q=m$. Seien $\gamma_{j},\alpha_{j}$ die jeweiligen geometrischen und algebraischen Vielfachheiten der $\lambda_{j}$. Sei die [[Jordansche Normalform|Jordan-Basis]] zu $A$ $$\{v_{jk}^{l}\vert j\in\mathbb{N}_{m}^{*},k\in\mathbb{N}_{\gamma_{j}}^{*},l\in\mathbb{N}_{l_{jk}}^{*}\},\qquad\sum\limits_{k=1}^{\gamma_{j}}l_{jk}=\alpha_{j}$$
>Es gilt $$\begin{align*}
&Av_{jk}^{1}=\lambda_{j}v_{jk}^{1}\text{ (Beginn der Jordankette)}\\[12pt]
&Av_{jk}^{l}=\lambda_{j}v_{jk}^{l}+v_{jk}^{(l-1)}\qquad\forall l\in\mathbb{N}_{l_{jk}}\setminus\{0,1\}\text{ falls }l_{jk}\gt1
\end{align*}$$

>[!thm] Theorem 1.4.5
>
>Seien die EV und verallgemeinerten EV zu reellen EW von $A$ reell. Dann ist das FS zu $y'=Ay$: $$\begin{cases}
&e^{\lambda_{j}x}\sum\limits_{r=0}^{l-1}\frac{x^{r}}{r!}v_{jk}^{l-r}, & j\in\mathbb{N}_{p}^{*},k\in\mathbb{N}_{\gamma_{j}}^{*},l\in\mathbb{N}_{l_{jk}}^{*}\\[12pt]
&\underbrace{\text{Re}\left(e^{\lambda_{j}x}\sum\limits_{r=0}^{l-1}\frac{x^{r}}{r!}v_{jk}^{l-r}\right)}_{a},\underbrace{\text{Im}\left(\sum\limits_{r=0}^{l-1}\frac{x^{r}}{r!}v_{jk}^{l-r}\right)}_{b}, & j=p+\mathbb{N}_{q}^{*},k\in\mathbb{N}_{\gamma_{j}}^{*},l\in\mathbb{N}_{l_{jk}}^{*}
\end{cases}$$wobei $$\begin{align*}
&a=e^{\text{Re }\lambda_{j}x}\sum\limits_{r=0}^{l-1}\frac{x^{r}}{r!}(\cos(\text{Im }\lambda_{j}x)\text{Re }v_{jk}^{l-r}-\sin(\text{Im }\lambda_{j}x)\text{Im }v_{jk}^{l-r})\\[12pt]
&b=e^{\text{Re }\lambda_{j}x}\sum\limits_{r=0}^{l-1}\frac{x^{r}}{r!}(\cos(\text{Im }\lambda_{j}x)\text{Im }v_{jk}^{l-r}+\sin(\text{Im }\lambda_{j}x)\text{Re }v_{jk}^{l-r})
\end{align*}$$

