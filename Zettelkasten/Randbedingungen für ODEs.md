---
time: 16.11.2023 13:35
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Randbedingungen für ODEs

>[!def] Definition 3.1: Randbedingungen für ODEs zweiter Ordnung
>Sei $x\in[a,b]$, suche $u\in\mathcal{C}^{k}([a,b])$ mit ($a_{0},a_{1},f\in\mathcal{C}^{0}([a,b])$) sodass $$u''(x)+a_{1}(x)u'(x)+a_{0}u(x)=f(x)$$, sodass **Randbedingungen** gelten:
>- **Robin-Randbedingungen**: $$\begin{cases}
\alpha_{0}u(a)+\alpha_{1}u'(a)=\eta_{1}\\
\beta_{0}u(b)+\beta_{1}u'(b)=\eta_{2}
\end{cases}\qquad\eta_{1},\eta_{2},\alpha_{0},\alpha_{1},\beta_{0},\beta_{1}\in\mathbb{R}\text{ mit }(\alpha_{0},\alpha_{1})\ne0\ne(\beta_{0},\beta_{1})$$Spezialfälle: $(\alpha_{1},\beta_{1})=0$ (Dirichlet-RB) und $(\alpha_{0},\beta_{0})=0$ (Neumann-RB)
>- **Periodische Randbedingungen**: $$u(a)=u(b),\qquad u'(a)=u'(b)$$

>[!exp] Beispiele
>1. $u''(x)=1,\quad u'(a)=0=u'(b)\Rightarrow\text{LR}=\emptyset$. $\#\text{LR}=\infty$
>2. $u''(x)=0,\quad u'(a)=0=u'(b)\Rightarrow\text{LR}=\mathbb{R}$ (konstante Fkt.) $\#\text{LR}=\infty$
>3. $u''(x)=0,\quad u(a)=0,\quad u'(b)=0\Rightarrow u=0$ eindeutige Lösung. $\#\text{LR}=1$
>4. $u''(x)+u(x)^{2}=1,\quad u''(a)=0=u'(b)\Rightarrow f(u)=1-u^{2}$ LL. Lös. des AWP existiert und ist eindeutig $\Rightarrow\text{LR}=\{\pm1\},\quad\#\text{LR}=2$

>[!mot] Setting für Theorem 3.2
>Sei $$\begin{align*}
&(Lu)(x):=u''(x)+a_{1}(x)u'(x)+a_{0}u(x),&&x\in[a,b],\quad a_{0},a_{1}\in\mathcal{C}^{0}([a,b])\\[12pt]
&Ru:=C\begin{pmatrix}u(a)\\
u'(a)\end{pmatrix}+D\begin{pmatrix}u(b)\\
u'(b)\end{pmatrix},&&C,D\in\text{Mat}(2\times2,\mathbb{R})
\end{align*}$$
>Suche $\mathcal{C}^{1}$-Lösungen des RWP $Lu=f,Ru=\eta$ für $f\in\mathcal{C}^{0}([a,b])$ und $\eta\in\mathbb{R}^{2}$

>[!thm] Theorem 3.2: Fredholm-Alternative
>Im Setting oben gilt: Entweder (1) oder (2)
>1. RWP $(Lu=f,Ru=\eta)$ hat $\forall\eta\in\mathbb{R}^{2},f\in\mathcal{C}^{0}([a,b])$ eine eindeutige Lösung.
>2. Das assoziierte homogene RWP $Lu=0,Ru=0$ hat eine Lösung (außer Nullösung)

>[!bew]- Beweis 3.2
>$\{u_{1},u_{2}\}$ FS für $Lu=0$. Dann $\forall u,u_{p}$ mit $Lu_{p}=f$: $$\exists c_{1},c_{2}\in\mathbb{R}:u(x)=u_{p}(x)+c_{1}u_{1}(x)+c_{2}u_{2}(x)\quad\forall x\in[a,b]$$
>(denn $\tilde u:=u-u_{p}$ löst $L\tilde u=0$).
>RWP lösen durch geeignete Wahl der $c_{i}$: $$\eta=Ru=Ru_{p}+\underbrace{\left[C\begin{pmatrix}u_{1}(a) & u_{2}(a) \\ u_{1}'(a) & u_{2}'(a)\end{pmatrix}+D\begin{pmatrix}u_{1}(b) & u_{2}(b) \\ u_{1}'(b) & u_{2}'(b)\end{pmatrix}\right]}_{=:M}\begin{pmatrix}c_{1} \\ c_{2}\end{pmatrix}$$
>Grundfrage: $M$ [[Invertierung von Matrizen|invertierbar]]? Sei LR des HRWP $\{0\}$. $u_{p}=0\qquad0=\eta=R\cdot0+M\begin{pmatrix}c_{1} & c_{2}\end{pmatrix}=M\begin{pmatrix}c_{1} \\ c_{2}\end{pmatrix}$ hat nur Lösung $\begin{pmatrix}c_{1} \\ c_{2}\end{pmatrix}=0\Rightarrow M$ invertierbar. $\forall\eta\in\mathbb{R}^{2}:\forall u_{p}\in\text{RWP}:\eta=Ru_{p}+M\begin{pmatrix}c_{1} \\ c_{2}\end{pmatrix}$ hat genau eine Lösung. $\square$

>[!bem] Bemerkung
>$\#\text{LR}\in\{0,1,\infty\}\Rightarrow$ Bsp. (4) konnte kein lineares Robin-RWP sein.

>[!exp] Beispiel 3.4: $\#\text{LR}=0$
>$y''+y=0\quad y(0)=1\textcolor{red}{=c_{1}},y(\pi)=1=\textcolor{red}{-c_{1}}\Rightarrow y(x)=c_{1}\cos(x)+c_{2}\sin(x)\Rightarrow\text{LR}=\emptyset$

>[!exp] Beispiel 3.3: $\#\text{LR}=1$
>$y''+y=0,\quad a=0,b=\frac{\pi}{2},\quad y(0)=1,\quad y\left(\frac{\pi}{2}\right)=1\Rightarrow y(x)=\cos(x)+\sin(x)$

>[!exp] Beispiel 3.5: $\#\text{LR}=\infty$
>$y''+y=0,\quad a=0,b=\pi\quad y(0)=1,y(\pi)=-1\Rightarrow\text{LR}=\cos+\mathbb{R}\sin$.

>[!mot] Setting
>Sei Randbed.: $$Ru=\begin{pmatrix}\eta_{1} \\ \eta_{2}\end{pmatrix},\qquad\begin{cases}
R_{1}(u)=\alpha_{1}u(a)+\alpha_{2}u'(a)=\eta_{1} \\
R_{2}(u)=\beta_{1}u(a)+\beta_{2}u'(a)=\eta_{2}
\end{cases}$$
>Annahme: HRWP $Lu=0=Ru$ hat nur Lösung $0$, d.h. nach oben: $$\det M=\det\left(C\begin{pmatrix}u_{1}(a) & u_{2}(a) \\ u_{1}'(a) & u_{2}'(a)\end{pmatrix}+D\begin{pmatrix}u_{1}(b) & u_{2}(b) \\ u_{1}'(b) & u_{2}'(b)\end{pmatrix}\right)\ne0$$ für ein FS $u=(u_{1},u_{2})$ von $Lu=0,\quad C=\begin{pmatrix}\alpha_{1} & \alpha_{2} \\ 0 & 0\end{pmatrix},\quad D=\begin{pmatrix}0 & 0 \\ \beta_{1} & \beta_{2}\end{pmatrix}$.
>$$\begin{align*}
&\det\begin{pmatrix}\alpha_{1}u_{1}(a)+\alpha_{2}u_{1}'(a) & \alpha_{1}u_{2}(a)+\alpha_{2}u_{2}'(a)\\
\beta_{1}u_{1}(a)+\beta_{2}u_{1}'(a) & \beta_{1}u_{2}(a)+\beta_{2}u_{2}'(a)\end{pmatrix}=\det\begin{pmatrix}R_{1}u_{1} & R_{1}u_{2}\\
R_{2}u_{1} & R_{2}u_{2}\end{pmatrix}\ne0&&(\star)
\end{align*}$$
>Passe zunächst FS an RB an:

>[!thm] Lemma 3.6
>Für jedes FS $u$ von $Lu=0$ gilt, falls $(\star)$ gilt, dass $(v_{1},v_{2})$ mit $$\left.\begin{cases}
v_{1}=c_{11}u_{1}+c_{12}u_{2} \\
v_{2}=c_{21}u_{1}+c_{22}u_{2}
\end{cases}\quad\right\vert\quad\begin{cases}
c_{11}=R_{1}u_{2} & c_{12}=-R_{1}u_{1} \\
c_{21}=R_{2}u_{2} & c_{22}=-R_{2}u_{1}
\end{cases}$$ein FS von $Lu=0$ mit $R_{1}v_{1}=0=R_{2}v_{2}$.

>[!bem] Bemerkung
>Ohne $(\star)$ gibt es ein solches FS nicht. s.o. $u''+u=0,\quad u(0)=u(\pi)=0$

>[!mot]- Herleitung Green'sche Funktion
>Erinnerung: [[Variation der Konstanten]]:
>Sei $\phi(x)$ FS von $Lu=0$. Eine Lösung der Gleichung $Lu=f$ ist 1. Komp. von $$\begin{align*}
y(x)&=\int_{0}^{x}\phi(x)\phi(s)^{-1}\begin{pmatrix}0 \\ f(s)\end{pmatrix}\dd s\\[6pt]
&=\int_{0}^{x}\begin{pmatrix}v_{1}(x) & v_{2}(x) \\ v_{1}'(x) & v_{2}'(x)\end{pmatrix}\frac{1}{v_{1}(s)v_{2}'(s)-v_{1}'(s)v_{2}(s)}\begin{pmatrix}v_{2}'(s) & -v_{2}(s) \\ -v_{1}'(s) & v_{1}(s)\end{pmatrix}\begin{pmatrix}0 \\ f(s)\end{pmatrix}\dd s\\[12pt]
y_{1}(x)&=\int_{0}^{x}\frac{v_{2}(x)v_{1}(s)-v_{1}(x)v_{2}(s)}{W(s)}f(s)\dd s\\[12pt]
&=\int_{0}^{x}\frac{v_{2}(x)v_{1}(s)}{W(s)}f(s)\dd s-\int_{0}^{x}\frac{v_{1}(x)v_{2}(s)}{W(s)}f(s)\dd s
\end{align*}$$
>$\tilde y:x\mapsto\left(\int_{0}^{1}\frac{v_{2}(s)}{W(s)}f(s)\dd s\right)v_{1}(x)$ löst $L\cdot=0$. $L\cdot=f$ wird auch gelöst von $y_{p}:=y_{1}+\tilde y$ mit$$y_p(x)=\int_{0}^{x}\frac{v_{2}(x)v_{1}(s)}{W(s)}f(s)\dd s+\int_{x}^{1}\frac{v_{1}(x)v_{2}(s)}{W(s)}f(s)\dd s=\int_{0}^{1}G(x,s)f(s)\dd s$$
>mit $$G(x,s):=\begin{cases}
\frac{v_{2}(x)v_{1}(s)}{W(s)}, & x\le s \\
\frac{v_{1}(x)v_{2}(s)}{W(s)}, & x\ge s
\end{cases}$$
>$y_{p}$ löst $Lu=f$ und auch RWP: $$\begin{align*}
R_{1}y_{p}&=\alpha_{1}y_{p}(0)+\alpha_{2}y_{p}'(0)\\[12pt]
&=\alpha_{1}\int_{0}^{1}\frac{v_{1}(0)v_{2}(s)}{W(s)}f(s)\dd s+\\[6pt]
&\qquad\qquad+\alpha_{2}\left(\frac{v_{2}(0)v_{1}(0)}{W(0)}f(0)-\frac{v_{1}(0)v_{2}(0)}{W(0)}f(0)+\int_{0}^{1}\frac{v_{1}'(0)v_{2}(s)}{W(s)}f(s)\dd s\right)\\[12pt]
&=\underbrace{(\alpha_{1}(0)+\alpha_{2}v_{1}'(0))}_{R_{1}v_{1}=0}\int_{0}^{1}\frac{v_{2}(s)}{W(s)}f(s)\dd s=0
\end{align*}$$

>[!def] Definition 3.7: Green'sche Funktion
>Wir nennen $G:[0,1]^{2}\rightarrow\mathbb{R}$ eine **Green'sche Funktion** für das RWP $\{L\cdot=f\vert f\in\mathcal{C}^{0}([0,1])\},\quad R\cdot=\eta$, wenn $G$ folgende Eigenschaften erfüllt:
>1. $G$ stetig auf $[0,1]^{2}$, $G$ auf $D^{\pm}:=\{(x,y)\in[0,1)^{2}\vert\pm x\le\pm y\}$ jeweils zweimal stetig partiell nach $x$ diff'bar.
>2. $G_{x}^{+}(x,x)-G_{x}^{-}(x,x)=1\Rightarrow G\vert_{\{x\}\times\mathbb{R}},G\vert_{\mathbb{R}\times\{y\}}$ nicht $\mathcal{C}^{1}$.
>3. $\forall(x,s)\in[0,1]^{2}:LG(\cdot,s)=0$ für $s\ne x$ (da $\{v_{1},v_{2}\}$ FS) keine klassische Lösung wegen des Sprungs!
>4. $R_{1}G(\cdot,s)=R_{2}G(\cdot,s)=0\quad\forall s\in(0,1)$

>[!thm] Theorem 3.8
>Falls $G$ eine Green'sche Funktion zu RWP, dann $\forall f\in\mathcal{C}^{0}([0,1])$: $$y:x\mapsto\int_{0}^{1}G(x,s)f(s)\dd s\quad\forall x\in[0,1]$$ ist die eindeutige Lösung von (RWP), und $G$ eindeutig.

>[!bew]- Beweis 3.8
>Seien $G_{1},G_{2}$ Green'sche Funktionen zu (RWP), sei $f\in\mathcal{C}^{0}([a,b])$. $$\begin{align*}
&\int_{0}^{1}G_{1}(x,s)f(s)\dd s=\int_{0}^{1}G_{2}(x,s)f(s)\dd s\\[12pt]
\Leftrightarrow\,&\int_{0}^{1}(G_{1}(x,s)-G_{2}(x,s))f(s)\dd s=0a
\end{align*}$$
>$f:s\mapsto G_{1}(x_{0},s)-G_{2}(x_{0},s)\forall s\in[0,1)$ ist $\in\mathcal{C}^{0}([0,1])$. $$\begin{align*}
&\Rightarrow\,\int_{0}^{1}(G_{1}(x,s)-G_{2}(x,s))(G_{1}(x_{0},s)-G_{2}(x_{0},s))\dd s=0\quad\forall x\in[0,1]\\[12pt]
\xRightarrow{x=x_{0}}\,&\int(G_{1}(x_{0},s)-G_{2}(x_{0},s))^{2}\dd s=0\Rightarrow G_{1}(x_{0},s)=G_{2}(x_{0},s)\quad\forall s\in[0,1]
\end{align*}$$
>$x_{0}$ bel. $\Rightarrow$ $G$ eindeutig. $\square$

>[!bem] Merksatz
>Die Green'sche Funktion eines Diffops $P$ ist der **Integralkern** von $P^{-1}$. 
>**Integralkern**: $A:\mathcal{C}^{0}(I)\rightarrow\mathcal{C}^{0}(I)$. $A$ hat Integralkern $\varphi:\Leftrightarrow(Av)(s)=\int_{I\times I}\varphi(s,t)v(t)\dd t$

>[!bsp] Beispiel 3.10
>$u''(x)=f(x)$, $u(0)=u(1)=0$. FS $(u_{1},u_{2})=(1,x\mapsto x)$ der homogenen DGL $u''=0$. $$A:=\begin{pmatrix}R_{1}u_{1} & R_{1}u_{2} \\ R_{2}u_{1} & R_{2}u_{2}\end{pmatrix}=\begin{pmatrix}u_{1}(0) & u_{2}(0) \\ u_{1}(1) & u_{2}(1)\end{pmatrix}=\begin{pmatrix}1 & 0 \\ 1 & 1\end{pmatrix}$$invertierbar. Da $(u_{1},u_{2})$ FS hat das homogene RWP nur triviale Lösung, nach Fredholm ist das RWP eindeutig lösbar. Neues FS $v=A^{-1}u\{x\mapsto-x,x\mapsto x-1\}$. $W(x)=-1$. Dann $R_{1}v_{1}=0=R_{2}v_{2}$ $\rightsquigarrow\exists$ Greensche Funktion. $$G(x,s)=\begin{cases}
\frac{s(x-1)}{1}, & s\le x\\ \\
\frac{x(s-1)}{1}, & s\ge x
\end{cases}\qquad\forall(x,s)\in[0,1]^{2}$$
>$(\star)$ hat also genau die Lösung $$y(x)=\int_{0}^{1}G(x,s)\cdot f(x)\dd x.$$

>[!info] [[Sturm-Liouville-Operatoren]]