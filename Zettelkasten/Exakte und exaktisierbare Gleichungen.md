---
time: 19.10.2023 14:21
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Exakte und exaktisierbare Gleichungen

>[!mot] Setting
>Seien $I,I'\subset\mathbb{R}$ Intervalle. Sei $y'=f(x,y),\quad y(x_{0})=y_{0}$ AWP und das lasse sich schreiben als $$P(x,y)\dd x+Q(x,y)\dd y=0,\quad y(x_{0})=y_{0}\qquad(\star)$$
>mit stetigen Funktionen $P,Q:I\times I'\rightarrow\mathbb{R}$. Außerdem gelte $Q(x,y)\ne0\forall(x,y)\in I\times I'$

>[!def] Definition: Exaktheit
>Unter obigen Voraussetzungen ist $P(x,y)\dd xQ(x,y)\dd y=\dd\varphi(x,y)$ ein totales Differential einer Funktion $\varphi:I\times I'\rightarrow\mathbb{R}$, genau dann wenn $P,Q$ in einem einfach zsh. Gebiet $\mathcal{C}^{1}$ sind und gilt $$\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}=0$$
>In diesem Fall lässt sich $(\star)$ als $d\varphi(x,y)=0$ schreiben und heißt **exakt**. $\{(x,y(x))\vert x\in I\}\subset I\times I'$ ist dann eine Niveaulinie von $\varphi$.

>[!bem] Bestimmung der Lösung
>Falls $(\star)$ exakt ist, lässt sich $\varphi$ per Kurvenintegral berechnen: $$\varphi(x,y)=\varphi(x_{0},y_{0})+\int_{x_{0}}^{x}P(\tilde x,y_{0})\dd\tilde x+\int_{y_{0}}^{y}Q(x_{0},\tilde y)\dd\tilde y$$
>Die Bedingung $$\varphi(x,y)=C\in\mathbb{R}$$lässt sich dann nach $y$ auflösen.

>[!bem] Exaktisierung
>Eine Funktion $\mu(x,y)$ ist ein **integriender Faktor** für die DGL $(\star)$, wenn daraus durch Multiplikation mit $\mu$ ein totales Differential wird, d.h. wenn gilt $$\mu P\dd x+\mu Q\dd y=\dd\varphi$$
>Setzt man in die Integrabilitätsbedingung ein, ergibt sich $$\mu\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)=Q\frac{\partial\mu}{\partial x}-\frac{\partial\mu}{\partial y}$$
>$\mu$ kann in bestimmten Fällen nur von $x$ bzw. $y$ abh. sein, dann erhält man eine [[Trennung der Variablen|separierbare DGL]] für $\mu(x)$/$\mu(y)$:
>$$\begin{align}&\frac{1}{Q}\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)\text{ unabh. von }y\Rightarrow\mu'(x)=\frac{\mu(x)}{Q}\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)\\[12pt]&\frac{1}{P}\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)\text{ unabh. von }x\Rightarrow\mu'(y)=-\frac{\mu(y)}{P}\left(\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}\right)\end{align}$$
