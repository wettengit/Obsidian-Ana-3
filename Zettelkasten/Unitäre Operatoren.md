---
time: 04.02.2024 00:19
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Unitäre Operatoren

>[!def] Definition 4.91: Unitäre Operatoren
>Sei $U:H\rightarrow H$ linearer Operator. $U$ heißt unitär $:\Leftrightarrow U$ isometrisch und surjektiv, d.h. $$\begin{align*}
&\text{1) }\qquad \left\lVert Ux\right\rVert=\left\lVert x\right\rVert\forall x\in H\Leftrightarrow\left\langle Ux,Uy\right\rangle=\left\langle x,y\right\rangle\forall x,y\in H\\[12pt]
&\text{2) }\qquad U(H)=H
\end{align*}$$

>[!bem] Bemerkung 4.92
>Ist $U$ unitär, dann ist $U$ aufgrund der Isometrie auch injektiv. Daher existiert eine Inverse $U^{-1}$ (welche offenbar auch unitär ist)
>$$U(H):=\{u\in\text{CL}(H,H):u\text{ unitär}\}$$ist eine Gruppe mit $\circ$.

>[!thm] Theorem 4.93
>Sei $U\in\text{CL}(H,H)$. Dann gilt $$U\text{ unitär}\Leftrightarrow UU^{*}=U^{*}U=\text{id}_{H}$$

