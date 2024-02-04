---
time: 21.11.2023 13:39
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Sturm-Liouville-Operatoren

>[!mot] Motivation
>Sei $L$ folgender Diffop: $$L:=a_{0}+a_{1}D+a_{2}D^{2},\qquad a_{i}\in\mathcal{C}^{1}([a,b])$$
>Auf $\mathcal{C}^{0}([a,b])$ definieren wir $$\left\langle f,g\right\rangle=\int_{a}^{b}f(x)g(x)\dd x$$
>Frage: Wann ist $L$ symmetrisch/[[Selbstadjungiert, symmetrisch und hermitesch|selbstadjungiert]]? $$\left\langle Lf,g\right\rangle=\left\langle f,Lg\right\rangle\qquad\forall f,g\in\mathcal{C}^{0}_{0}([a,b])$$
>mit $\mathcal{C}^{0}_{0}([a,b]):=\{u\in\mathcal{C}^{0}([a,b])\vert u(a)=0=u(b)\}$.

>[!def] Definition 3.12: Sturm-Liouville-Operator
>$p,q\in\mathcal{C}^{1}([a,b],\mathbb{R})$, $p(x)\gt0\forall x\in[a,b]$ Dann ist der **Sturm-Liouville-Operator** zu $p,q$ $$L:=q+p'D+pD^{2}=L_{p,q}$$

>[!bem] Bemerkung
>Das ist kein Verlust der Allgemeinheit in den RWP. Außerdem $$Ly=qy+\underbrace{p'y+py''}_{=(py')'}$$

>[!thm] Lemma 3.13
>Seien $p,q\in\mathcal{C}^{1}([a,b],\mathbb{R})$. Sei $L=L_{p,q}=q+p'D+pD^{2}$. Dann $\forall f,g\in\mathcal{C}^{2}([a,b])$:
>1. $$f\cdot(Lg)-g\cdot(Lf)=\left(p\begin{vmatrix}f & g \\ f' & g'\end{vmatrix}\right)'$$
>2. $$\left\langle f,Lg\right\rangle-\left\langle Lf,g\right\rangle=\left.\left(p\begin{vmatrix}f & g \\ f' & g'\end{vmatrix}\right)\right\vert_{a}^{b}$$
>3. $$f,g\in\mathcal{C}^{0}_{0}([a,b])\Rightarrow\left\langle Lf,g\right\rangle=\left\langle f,Lg\right\rangle$$
>4. $$p\in\mathcal{C}^{0}_{0}([a,b])\Rightarrow\left\langle Lf,g\right\rangle=\left\langle f,Lg\right\rangle$$

>[!bew]- Beweis 3.13
>al-ğabr $\square$

>[!bem] Bemerkung Greensche Funktion von $L$
>Wir normieren $L$: Es war $p\gt0$, also $\tilde L:=\frac{1}{p}L=\frac{q}{p}+\frac{p'}{p}D+D^{2}$. Wissen: für $\tilde L$ existiert genau eine Greensche Funktion $\tilde G$. $$\tilde L y=f\Leftrightarrow Ly=pf\Rightarrow G(x,s)=\frac{\tilde G(x,s)}{p(s)}\text{ Greensche Fkt. von }L.$$

>[!thm] Satz 3.14
>Wenn $Ly=0$ und $y(a)=0=y(b)$ nur die Lösung $0$ besitzt, dann gibt es zu $(\star)$ eine Greensche Funktion $G$ mit $G(x,s)=G(s,x)$

>[!bew]- Beweis 3.14
>$G^{l}(x,s)=\frac{v_{1}(x)v_{2}(s)}{p(s)W(s)},\quad G^{r}(x,s)=\frac{v_{1}(s)v_{2}(x)}{p(s)w(s)}$. $W(x)=v_{1}v_{2}'-v_{1}'v_{2}$. $(p\cdot W)'=v_{1}\underbrace{(Lv_{2})}_{=0}-v_{2}\underbrace{(Lv_{1})}_{=0}=0$
>$\rightsquigarrow p\cdot W$ konstant.: $(x,s)\in D^{l}\rightsquigarrow(s,x)\in D^{r}$ $$\forall x,s\in[a,b],x \lt s:G(x,s)=G^{l}(x,s)=\frac{v_{1}(x)v_{2}(s)}{p(s)W(s)}=G^{r}(s,x)=G(x,s)\qquad\square$$

>[!def] Definition 3.15: Dirichlet-Eigenwertprobleme
>$\lambda\in\mathbb{R}$ heißt **Dirichlet-Eigenwert** (DEW) zu $L$ $$:\Leftrightarrow\exists u\in\mathcal{C}^{2}([a,b])\cap\mathcal{C}_{0}^{0}([a,b]),\quad u\ne0:\qquad\boxed{Lu\textcolor{red}{+}\lambda u=0}$$
>$u$ heißt dann auch **Dirichlet-Eigenfunktion** (DEF)

>[!bem] Bemerkung 3.16
>Nach Def. hat hom. RWP zu $L$ eine Lösung $\Leftrightarrow0$ Dirichlet-EW von $L$.

>[!thm] Satz 3.17
>Wenn $P$ ein $L^{2}$-symmetrischer Operator auf $\mathcal{C}^{0}([a,b])$, $\lambda_{1}\ne\lambda_{2}$ DEW mit DEF $u_{1},u_{2}$. Dann $\left\langle u_{1},u_{2}\right\rangle=0$.

>[!bew]- Beweis 3.17
>$u_{1},u_{2}\vert_{\partial I}=0\Rightarrow\left\langle Pu_{1},u_{2}\right\rangle=\left\langle u_{1},Pu_{2}\right\rangle$ $$\begin{align*}
&-\lambda_{1}\left\langle u_{1},u_{2}\right\rangle=\left\langle-\lambda_{1}u_{1},u_{2}\right\rangle=\left\langle u_{1},Lu_{2}\right\rangle=\left\langle u_{1},-\lambda_{2}u_{2}\right\rangle=-\lambda_{2}\left\langle u_{1},u_{2}\right\rangle
&\Rightarrow\underbrace{(-\lambda_{1}+\lambda_{2})}_{\ne0}\left\langle u_{1},u_{2}\right\rangle=0&&\square
\end{align*}$$

>[!thm] Satz 3.18
>Sei $0$ nicht DEW des Sturm-Liouville-Operators $L$. Sei $G$ Green'sche Funktion von $L$, dann $$Lu+\lambda u=0\Leftrightarrow\int_{a}^{b}G(x,s)u(s)\dd s=-\frac{1}{\lambda}u(x)$$

>[!bew]- Beweis 3.18
>$$Lu=f\Leftrightarrow\int_{a}^{b}G(x,s)\underbrace{f(s)}_{=-\lambda u(s)}\dd s=u(x)\qquad\square$$

>[!thm] Satz 3.19
>$L_{p,q}=q+p'D+pD^{2}\text{ mit }q\le0\lt p$. Sei $\lambda$ DEW von $L_{p,q}$. Dann gilt $\lambda\gt0$. $\sigma_{\text{Dir}}(L)\subset\mathbb{R}^{+}$.

>[!bew]- Beweis 3.19
>Sei $Lu=-\lambda u$. $$\begin{align*}
\lambda\left\lVert u\right\rVert^{2}&=\left\langle\lambda u,u\right\rangle=-\left\langle Lu,u\right\rangle\\[12pt]
&=-\int_{a}^{b}(qu+\textcolor{Aquamarine}{(pu')'u})\dd x=-\int_{a}^{b}q(x)u^{2}(x)\dd x-\textcolor{Aquamarine}{R}\\[12pt]
R&=\int_{a}^{b}(pu')'u\dd x=\underbrace{pu'u\vert_{a}^{b}}_{=0}-\int_{a}^{b}\underbrace{p}_{\ge0}\underbrace{u'\cdot u'}_{\ge0}\dd x\lt0&&\square
\end{align*}$$

>[!thm] Satz 3.20
>Sei $\lambda\in\sigma_{\text{Dir}}(L)$. Die Eigenfkt. zu $\lambda$ bilden einen endlich-dim. Teilraum von $\mathcal{C}^0_0([a,b])$ mit Dimension $\text{GV}(\lambda)$. Ordnet man $\sigma_{\text{Dir}}$ in eine Folge in $\mathbb{R}$, dann gilt $$\lim\limits_{n\rightarrow\infty}\lambda_{n}=\infty$$
