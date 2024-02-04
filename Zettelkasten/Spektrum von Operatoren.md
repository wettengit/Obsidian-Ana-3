---
time: 25.01.2024 13:50
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Spektrum von Operatoren

>[!thm] Theorem 4.100: Satz von Banach
>Sei $B$ BR, $T\in\text{CL}(B,B)$ bijektiv. Dann ist $T^{-1}\in\text{CL}(B,B)$.

>[!thm] Lemma 4.102
>Sei $T\in\text{CL}(B,B)$ mit $\left\lVert T\right\rVert\lt1$. Dann ist $\text{id}-T$ beschränkt invertierbar und $$\left\lVert(\text{id}-T)^{-1}\right\rVert\le\frac{1}{1-\left\lVert T\right\rVert}$$

>[!thm] Theorem 4.103
>Sei $S\in\text{CL}(B,B)$ beschränkt invertierbar und $T\in\text{CL}(B,B)$. Sei $$\left\lVert S-T\right\rVert\lt\frac{1}{\left\lVert S^{-1}\right\rVert}.$$Dann ist auch $T$ beschränkt invertierbar.

>[!def] Definition 4.104: Spektrum von Operatoren
>Sei $B$ BR und $T\in\text{CL}(B,B)$. Sei $\mathbb{1}:=\text{id}_{B}$. 
>1. Das **Spektrum** von $T$ ist $$\sigma(T):=\{\lambda\in\mathbb{C}:T-\lambda\mathbb{1}\text{ nicht bijektiv}\}$$
>2. Das **Punktspektrum** von $T$ ist $$\sigma_{p}(T):=\{\lambda\in\mathbb{C}:T-\lambda\mathbb{1}\text{ nicht injektiv}\}$$
>3. Das **kontinuierliche Spektrum** von $T$ ist $$\sigma_{c}(T):=\{\lambda\in\sigma(T)\setminus\sigma_{p}(T):\overline{(T-\lambda\mathbb{1})(B)}=B\}$$
>4. Das **Restspektrum** von $T$ ist $$\sigma_{r}(T):=\sigma(T)\setminus\sigma_{p}(T)\setminus\sigma_{c}(T)$$
>
>$\lambda\in\sigma(T)$ heißt **Spektralwert** und $(T-\lambda\mathbb{1})^{-1}$ für $\lambda\not\in\sigma(T)$ die Resolvente von $T$ an der Stelle $\lambda$.

>[!bem] Bemerkung 4.105
>1. $$\sigma_{p}(T)={\lambda\in\mathbb{C}:\exists x\in B\setminus\{0\}:T x=\lambda x}$$
>2. Für $\lambda\in\sigma_{c}(T)$ ist $T-\lambda\mathbb{1}$ injektiv mit dichtem Bild $T(B)\ne B$.
>3. Es gilt $\forall T\in\text{CL}(B,B)$: $$\sigma(T)=\sigma_{p}(T)\sqcup\sigma_{c}(T)\sqcup\sigma_{r}(T)$$

>[!thm] Theorem 4.106
>Sei $T\in\text{CL}(B,B)$. Dann ist $\sigma(T)$ kompakt in $\mathbb{C}$. Es gilt $$\sigma(T)\subset B(0,\left\lVert T\right\rVert)$$

>[!thm] Theorem 4.110
>Sei $B$ endlichdim. BR und $T\in\text{CL}(B,B)$. Dann ist $$\sigma(T)=\sigma_{p}(T)\quad\text{ bzw. }\quad\sigma_{c}(T)=\emptyset=\sigma_{r}(T)$$

