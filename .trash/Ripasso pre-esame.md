# COMPITO 18-06-24
##### T1 (TEOREMA LIMITE SUCCESSIONI MONOTONE)
Sia $a_{n}$ una successione di numeri reali.
Se $a_{n}$ è monotona, allora essa ammette sempre limite, nello specifico:
- se è crescente, il limite coinciderà con il suo estremo superiore $\sup_{}a_n$, se è anche limitata superiormente, il limite sarà un reale L, altrimenti sarà $+\infty$
- se è decrescente, il limite coinciderà con l'estremo inferiore $\inf a_n$, se limitata inferiormente sarà L altrimenti $-\infty$
###### DIMOSTRAZIONE 
Assumiamo per ipotesi che $a_n$ sia crescente e che sia limitata superiormente.
Chiamiamo $L$ l'estremo superioredell'insieme dei valori della successione:
$L=\sup_{}a_n$
l'obbiettivo è dimostrare che $\lim\limits_{n\to \infty}a_n=L$ , applicando la definizione di limite:
$\forall \epsilon>0,\  \exists\overline{n}:|a_{n}-L|<\epsilon \ \ \forall n>\overline{n}$

$a_{n}\leq L  \ \ \ \forall n$
$\epsilon >0  \ \ \ \exists\overline{n}:a_\overline{n}>L-\epsilon$
la successione è crescente, quindi: $a_{n}\geq a_\overline{n}$
$\forall n>\overline{n}\implies L-\epsilon<a_\overline{n}\leq a_{n} < L <L+\epsilon$

$$|a_{n}-L|<\epsilon \ \ \ \ \ \forall n>\overline{n}$$
##### T2 
Sia $a_{n}$ una successione limitata, dire quale delle seguenti affermazioni è errata:
- a) se $a_{n}$ è convergente allora è monotona 
- b) se $a_{n}$ è monotona allora è convergente

a) è falsa:
$a_{n}=\frac{(-1)^{n}}{n}$
1. è limitata tra $-1$ e $\frac{1}{2}$
2. per a $n\to \infty$ converge a $0$
3. non è monotona, $f(1)=-1, f(2)=\frac{1}{2}, f(3)=-\frac{1}{3}$
##### ES2
$\begin{cases}a_{n}+1=\sqrt{2+a_n}-1 \\  a_{0}=2\end{cases}$
dire se $a_{n}$ ammette limite.

$L=\sqrt{2+L}-1$
$L+1=\sqrt{2+L}$
$(L+1)^{2}=2+L$
$L^2+2L+1=2+L$
$L^2+L-1=0$
$L_{1,2}=\frac{-1(+-)\sqrt{1-4(1)(-1)}}{2}=\frac{-1(+-)\sqrt{5}}{2}$

$\sqrt{2+a_{n}}-1\leq a_{n}$
$\sqrt{2+a_{n}}\leq a_{n}+1$
$2+a_{n}\leq a_{n}^2+2a_{n}+1$
$a_{n}^{2}+a_{n}-1\leq 0$

$a_{n}\geq \frac{\sqrt{5}-1}{2}$
$\lim_{n\to \infty}a_{n}=\frac{\sqrt{5}-1}{2}$

# COMPITO 13-06-25
##### T1 (TEOREMA ESISTENZA ZERI)
Sia $f:[a,b]\to R$ una funzione 
se f è una funzione continua in un intervallo chiuso e limitato $[a,b]$, e se assume valori di segno opposto agli estremi dell'intervallo (cioé $f(a)\cdot f(b)<0$) allora esiste almeno un punto $c\in(a,b)$ tale che $f(c)=0$

