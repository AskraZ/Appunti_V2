[[Ripasso pre-esame]]
[[Derivate]]
# Funzioni
Siano $A$ e $B$ due insiemi non vuoti.
$$f:A\to B$$
$A$ è detto Dominio della funzione
$B$ è detto Codominio della funzione

$f:A\to B$ si dice:
- Suriettiva: $\mathrm{Im}(f)=B \ \ \ \forall y\in B, \ \exists x\in A:f(x)=y$
- Iniettiva: $\forall x_{1},x_{2}\in A |x_{1}\neq x_{2}|\implies f(x_{1})\neq f(x_{2})$
- Dispari: $\forall x\in R\implies f(-x)=-f(x)$
- Pari: $\forall x\in R\implies f(-x)=f(x)$

### DEFINIZIONE (FUNZIONE LIMITATA)
$f:A\subseteq R\to R$
$f$ si dice limitata inferiormente se è limitata inferiormente la sua immagine.
Si chiama estremo inferiore di $f$ in $A$ e si indica con $\inf \ f(A)$

---
$f$ si dice limitata superiormente se è limitata superiormente la sua immagine.
Si chiama estremo superiore di $f$ in $A$ e si indica con $sup \ f(A)$

---
Sia $f:A\subseteq R\to R$ 
Sia $f$ limitata inferiormente

$l=inf \ f(A)\iff\begin{cases}l\leq f(x)\ \ \ \ \ \forall x \in A\\ \forall \epsilon>0 \ \  \ \  \ \ \ \ \exists x' \in A: f(x')<l+\epsilon \end{cases}$

Sia $f$ limitata superiormente

$L=sup \ f(A)\iff\begin{cases}L\geq f(x) \ \ \ \ \forall x\in A \\ \forall \epsilon>0 \ \ \ \ \ \ \ \ \ \exists x'' \in A:f(x'')>L-\epsilon\end{cases}$

---
 Sia $f:A\subseteq R\to R$ 
 Si dice che $f$ ha minimo in $A$ se $\exists  min \ f  (a)$, ovvero se $\exists x'\in A:f(x')\leq f(x) \ \ \ \ \forall x\in A$

# Successioni
Una successione viene indicata con $$\{x_{1},x_{2},\dots,x_{n},\dots\} \  \text{oppure} \ \{x_n\}_{n\in N}$$
### DEFINIZIONE (CRESCENTE E DECRESCENTE)
Una successione $\{x_{n}\}$ è detta crescente se per ogni $n \lt m$, con $n,m\in N$, si ha $x_{n}\lt x_{m}$ ;
Una successione $\{x_{n}\}$ è detta decrescente se per ogni $n\lt m$, con $n,m \in N$, si ha $x_{n}\gt x_{m}$ ;
non crescente $\to$ $x_{n}\geq x_{m}$
non decrescente $\to$ $x_{n}\leq x_{m}$
> SE VALE UNA DI QUESTE PROPRIETA' LA FUNZIONE È DETTA MONOTONA

### DEFINIZIONE (SUCCESSIONE LIMITATA)
Sia $\{a_{n}\}$ una successione, si dice che $\{a_n \}$ è limitata inferiormente se $\exists h\in R: \ h\leq a_{n}, \ \ \ \ \ \forall n \in N$
Si dice che $\{a_{n}\}$ è limitata superiormente se $\exists k\in R:$ $k \geq a_{n}$,    $\forall n\in N$  
##### ESEMPI
$x^2-10$ è limitata inferiormente:
![[Screenshot 2026-04-24 130117.png|400]]
$\frac{1}{n}$ è limitata superiormente e inferiormente:
![[Screenshot 2026-04-24 125725.png|409]]

Una successione limitata superiormente ed inferiormente si dice Limitata.
### DEFINIZIONE (DIVERGENZA E CONVERGENZA)
Sia $\{a_n\}$ una successione numerica, si dice che $\{a_{n}\}$ diverge a $-\infty$ e scriviamo che $\exists \lim_{ n \to \infty }{a_{n}}=-\infty$ se $\forall k\gt 0 \ \ \exists \psi\in N$ (dipendente da k): $\forall n\gt \psi$ risulta $a_{n}\lt -k$

---
$a_{n}$ diverge a $-\infty$ se preso un qualunque numero $k$ maggiore di $0$, esiste un indice di soglia $\psi$ tale che tutti i punti di $a_n$ con $n\gt \psi$ risulta che i valori di $a_{n}$ saranno minori di $-k$
![[unnamed.png|517]]

---
Sia $\{a_n\}$ una successione numerica, si dice che $\{a_{n}\}$ diverge a $+\infty$ e scriviamo che $\exists \lim_{ n \to \infty }{a_{n}}=+\infty$ se $\forall k\gt 0 \ \ \exists \psi\in N$ (dipendente da k): $\forall n\gt \psi$ risulta $a_{n}\gt k$
![[unnamed (1).png|517]]

---
Sia $\{a_n\}$ una successione numerica, si dice che $\{a_{n}\}$ converga a $l\in R$ e scriviamo che $$\exists \ \lim_{ n \to \infty }{a_{n}=l}$$ se $\forall \epsilon>0 \ \ \ \exists \psi\in N$ (dipendente da $\epsilon$) tale che $\forall n\in N, n>\psi$ risulta:
$|a_{n}-l|\lt \epsilon$ 
$-\epsilon \lt a_n-l\lt \epsilon$
$l-\epsilon \lt a_{n}\lt \epsilon + l$
![[Screenshot 2026-04-24 142036.png]]
### DEFINIZIONE (REGOLARE)
Una successione $a_{n}$ si dice regolare se converge a $+\infty$ o diverge a $-\infty$
Se $a_{n}$ non è regolare allora si dice oscillante.
## TEOREMA DELL'UNICITA' DEL LIMITE
Sia $a_{n}$ una successione regolare, allora il suo limite è unico.
##### DIMOSTRAZIONE
supponiamo per assurdo che $\exists \lim_{ n \to \infty }a_{n}=l$ e $\exists \lim_{ n \to \infty }a_{n}=m$ con $l\neq m$.
supponiamo $l\gt m$, $\epsilon=\frac{l-m}{2}\gt 0$ 

---
Per  $\exists \lim_{ n \to \infty }a_{n}=l$:
$\exists \psi'\in N:\forall n\gt \psi' \ \ \ \ l-\epsilon\lt a_{n}\lt \epsilon+l \ \ \ \ \epsilon=\frac{l-m}{2}$

$\frac{l+m}{2}=l-\frac{l-m}{2}\lt a_{n}\lt l+\frac{l-m}{2} = \frac{3l-m}{2}$

Per  $\exists \lim_{ n \to \infty }a_{n}=m$:
$\exists \psi''\in N:\forall n\gt \psi'' \ \ \ \ m-\epsilon\lt a_{n}\lt \epsilon+m \ \ \ \ \epsilon=\frac{l-m}{2}$

$\frac{3m+l}{2}=\frac{l+m}{2}\lt a_{n} \lt \frac{l+m}{2} = \frac{m-l}{2}$

# Limiti
Sia $a\in R$ 
$$\lim_{n\to \infty}n^a=\begin{cases}+\infty \ \ \ se \ a\gt 0 \\ 1 \ \ \ \ \ \ \ \ se \  a =0 \\ 0 \ \ \ \ \ \ \ \ se\ a \lt 0\end{cases}$$


---
