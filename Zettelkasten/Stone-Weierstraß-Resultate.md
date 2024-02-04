---
time: 30.11.2023 13:34
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Stone-Weierstraß-Resultate

>[!bem] Erinnerung
>Konvergenz in $d_{\text{sup}}\Leftrightarrow$ gleichgr. Konvergenz. $X,Y$ metr. Räume, $Y$ vollst. $\Rightarrow(\mathcal{C}^{0}(X,Y),d_{\text{sup}})$ vollst. $\mathbb{K}\in\{\mathbb{R},\mathbb{C}\}$, $\text{Pol}([a,b],\mathbb{K})=\{p:[a,b]\ni t\mapsto p(t)\in\mathbb{K}\vert p\in\mathbb{K}[x]\}\subset\mathcal{C}^{\infty}([a,b],\mathbb{K})$

>[!thm] Lemma 3.25 (Weierstraß)
>$$\text{cl}(\text{Pol}([a,b],\mathbb{K}))=\mathcal{C}^{0}([a,b],\mathbb{K})$$bzgl. der $d_{\text{sup}}$.

>[!def] Definition: Algebra
>[[Vektorräume|Vektorraum]]+[[Ringe|Ring]] mit $+,\cdot$, $\exists$ Unteralgebren (Untervektorraum abgeschlossen unter $\cdot$). ? Bsp.: $X$ Menge, $Y$ Algebra $Y^{X}=\text{Abb}(X,Y)$ punktweise $+,\cdot$.

>[!thm] Theorem 3.26
>Sei $X$ [[Kompakte und zusammenhängende metr. Räume|kpt. metr. Raum.]] $\mathcal{C}^{0}(X,\mathbb{K})$ ist Algebra. Sei $R\subset\mathcal{C}^{0}(X,\mathbb{K})$ Unteralgebra von $\mathcal{C}^{0}$ dann $\overline R^{d_{\sup}}$ ist Unteralgebra.

>[!thm] Theorem 3.27
>Sei $X$ kpt. metr. Raum, $R\subset\mathcal{C}^{0}(X,\mathbb{R})$ unitäre Unteralgebra (d.h. mit Einselement, also die konstanten Funktionen sind $\in R$). Seien $f,g\in R$. Dann $|f|,\max(f,g),\min(f,g)\in\text{cl}(R)$.

>[!thm] Theorem 3.28: Stone-Weierstraß
>Sei $X$ kpt. [[Topological spaces|top. Raum]], $R\subset\mathcal{C}^{0}(X,\mathbb{K})$ unitäre Unteralgebra. Annahme: $\forall x,y\in X:x\ne y\Rightarrow\exists f\in R:f(x)\ne f(y)$ ("$R$ trennt Punkte"). Dann $$\boxed{\text{cl}(R)=\mathcal{C}^{0}(X,\mathbb{K})}$$

>[!thm] Theorem 3.29: Stone-Weierstraß+✨
>$X$ kpt, sei $R\subset\mathcal{C}^{0}(\mathbb{K})$ eine Unteralgebra, dann: $$\text{cl}(R)=\mathcal{C}^{0}(\mathbb{K})\textcolor{Aquamarine}{\Leftrightarrow} V_{R}(x)\ne R\quad\forall x\in X\textcolor{Aquamarine}{\Leftrightarrow}V_{R}(x)\ne V_{R}(y)\quad\forall x,y\in X\text{ mit }x\ne y$$

>[!bem] Bemerkung
>$$\mathcal{C}^{0}_{2\pi-\text{p}}:=\{f\in\mathcal{C}^{0}(\mathbb{R},\mathbb{K})\vert f\,2\pi-\text{periodisch}\}\simeq\mathcal{C}^{0}(\mathbb{S}^{1},\mathbb{K})$$
>(isomorph als Algebra). Außerdem $\left\lVert\cdot\right\rVert_{\infty}$ wohldef. auf $\mathcal{C}^{0}_{2\pi-\text{p}}(\mathbb{R})$.

>[!def] Definition 3.30
>$f:\mathbb{R}\rightarrow\mathbb{K}$, $$\mathbb{K}=\begin{cases}
\mathbb{R}\\\mathbb{C}
\end{cases}$$ heißt **reelles/komplexes trigonometrisches Polynom** $$\begin{align*}
&:\Leftrightarrow\begin{cases}
\exists m\in\mathbb{N}^{*}:\exists a_{0},a_{1},...,a_{m},b_{1},...,b_{m}\in\mathbb{R} \\
\exists m,M\in\mathbb{N}:\exists c_{-m},...,c_{M}\in\mathbb{C}
\end{cases}:\\[12pt]
&\qquad\begin{cases}
f(t)=a_{0}+\sum\limits_{k=1}^{m}a_{k}\cos(kt)+b_{k}\sin(kt)&\forall t\in R \\
f(t)=\sum\limits_{k=-m}^{M}c_{k}e^{ikt}&\forall t\in R
\end{cases}
\end{align*}$$
>Der Raum der trigonometrischen Polynome über $\mathbb{K}$ (von $\mathbb{R}$ nach $\mathbb{K}$) heißt $$\text{TPol}_{\mathbb{K}}(\mathbb{R})$$

>[!thm] Theorem 3.31
>Sei $f\in\mathcal{C}^{0}_{2\pi-\text{p}}(\mathbb{R},\mathbb{K})$, dann existiert eine Folge $n\mapsto g_{n}\in\text{TPol}_{\mathbb{K}}(\mathbb{R})$ mit $$\boxed{g_{n}\xrightarrow[\,n_{\infty}\,]{d_{\sup}}f}$$
>Die Trigonometrischen Polynome sind also dicht in den $2\pi$-periodischen Funktionen.

>[!thm] Theorem 3.22
>$$\boxed{\text{TPol}_{\mathbb{K}}(\mathbb{R})\subset L^{2}([0,2\pi])}$$
>Die trigonometrischen Funktionen bilden also eine Hilbertbasis von $L^{2}([0,2\pi])$!

