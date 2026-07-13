## Rapporto Incrementale
$f:(a,b) \to  \mathbb{R}$ 
$g:[a,c] \to \mathbb{R}$ 
$c\gt b \implies f(a) = g(a)$ 
$f(b)=g(c)$

> incremento di una funzione $f$ 
 $\Delta f=f(b)-f(a)$ 
incremento della variabile $x$
$\Delta x=b-a$

$$\frac{\Delta f}{\Delta x}$$
---

Sia ora $f:(a,b) \to R$, sia $x_{0}\in(a,b)$ 
$\forall x\in(a,b)\ / \ \{x_0\}$
$r(x)=\frac{f(x)-f(x_0)}{x-x_0}=\frac{\Delta f}{\Delta x}$ rapporto incremente di $f$ in $x_0$

---

in modo diverso posso chiamare il generico punto di $(a,b), \ x_{0}+h,$  deve essere 
$a \lt x_{0} + h \lt b\iff a-x_{0}\lt h\lt b-x_0$      $h\neq 0$
ponendo $x = x_{0}+h$ da $r(x)$ si ottiene $R(x)=\frac{f(x_0+h)-f(x_0)}{h}$
$r:(a,b) / \{x_{0}\}\to \mathbb{R}$     $R:(a-x_{0}, b-x_{0}) / \{0\} \to \mathbb{R}$ 

---

dal teorema dei limiti delle funzioni composte si ha $\displaystyle{\lim_{x\to x_{0}}r(x)=\lim_{h\to 0}R(h)}$
### TEOREMA SUL RAPPORTO INCREMENTALE
Una funzione f è **strettamente crescente** in un punto $x_0$​ se e solo se esiste un intorno $I(x_0​,s)$ di raggio $s\gt0$ tale che, per ogni $x$ appartenente all'intorno (con $x\neq x_0​)$, il rapporto incrementale è strettamente positivo:
###### DIMOSTRAZIONE 
$r(x)=\frac{f(x)-f(x_0)}{x-x_0}$ 
se $r(x)\gt0 \ \ \forall x\in I(x_0,s)$ 

in $]x_0-s,x_{0}[ \begin{cases}r(x)\gt0 \\  x-x_0\lt0\end{cases}\implies f(x)-f(x_0)\lt0$ 

in $]x_{0},x_{0}+s[ \begin{cases}r(x)\gt0 \\  x-x_0\gt0\end{cases}\implies f(x)-f(x_0)\gt0$

viceversa se $f$ è crescente in $x_0$ 
in $]x_{0}-s, x_{0}[ \begin{cases}f(x)-f(x_{0})\lt0 \\  x- x_{0}\lt0\end{cases}\implies r(x)\gt0$

in $]x_{0}, x_{0}+s[ \begin{cases}f(x)-f(x_{0})\gt0 \\  x-x_0\gt0\end{cases}\implies r(x)\gt0$

## CALCOLO DIFFERENZIALE
sia $f:(a,b)\to \mathbb{R}$, sia $x_0\in(a,b)$ 
se $\exists \lim\limits_{x\to x_{0}}\frac{f(x)-f(x_0)}{x-x_0}$ ed è finito, diremo che $f$ è ==derivabile== in $x_0$ e porremo:$$f'(x_0)=\lim\limits_{x \to x_{0}}\frac{f(x)- f(x_{0})}{x-x_{0}}$$
Se $f$ è derivabile in ogni punto di $(a,b)$ si dice che è derivabile in $(a,b)$.
nasce allora la funzione derivata $f':(a,b)\to \mathbb{R}$ 
se $f'$ ammette derivata in $x_0$, tale derivata è chiamata derivata seconda in $x_0$ ($f''$)

> in modo simile si possono avere $f'''(x_{0}),f''''(x_{0}),f^n(x_0)$ 

---

esempi di funzione derivabile:
$f(x)=\delta$
$r(x)=\frac{\delta-\delta}{x-x_{0}}=0 \implies f'(x)=0$
$f(x)=x$
$r(x)=\frac{x-x_{0}}{x-x_{0}}=1\implies f'(x)=1$ 
$f(x)=x^2$
$r(x)=\frac{x^{2}-x_{0}^{2}}{x-x_{0}}= x+x_{0} \to2x_{0} (\lim_{x\to x_{0}}x+x_{0})\implies f'(x)=2x$ 

---

> esempi di funzione non derivabile 

$f(x)=\sqrt{x} \ \ (x_{0}=0)$
$r(x)=\frac{\sqrt{x}-0}{x-0}=\frac{\sqrt{x}}{x}\to \frac{1}{\sqrt{x}}\ \implies \lim_{x\to x_{0}^+}r(x)=+\infty$ 
$f(x)=|x|$  $(x_0=0)$
$r(x)=\frac{|x|-0}{x-0}=\begin{cases}1 & x\gt0 \\  -1 &  x\lt0\end{cases}\implies \not\exists \lim_{x\to 0}r(x)$

##### CRITERIO DI MONOTONIA LOCALE 
se $f'(x) \gt 0\implies f$ è crescente in $x_{0}$.
infatti $f'(x_{0})\gt0 \implies r(x)\gt0$ in un intorno di $x_{0}$.
##### CRITERIO DI MONOTONIA
se $f'(x)\gt0 \ \ \ \forall x \in(a,b) \implies f$ è strettamente crescente in $(a,b)$ (infatti lo è in ogni punto).
###### RELAZIONE TRA DERIVABILITÀ E CONTINUITÀ
sappiamo già che $\sqrt{x}$ e $|x|$ sono continue ma non derivabili, quindi 
$$\text{continuità} \not\implies \text{derivabilità}$$
si ha invece che:
$$\text{derivabilità} \implies \text{continuità}$$
#### TEOREMA 
Se $\exists f'(x_0)$ allora $f$ è continua in $x_0$
###### DIMOSTRAZIONE
$\exists f'(x_{0})\iff \exists p(x)$ polinomio di primo grado tale che $p(x_{0})=f(x_0)$ 

$\lim\limits_{x\to x_{0}}\frac{f(x)-p(x)}{x-x_{0}}$  $(f-p=o(x-x_{0}))$ tende a zero più rapidamente di $x-x_{0}$, quindi $f(x)$ si può approssimare con $p(x)$

$p(x)=f(x_{0})+f'(x_{0})(x-x_{0})$

 $\frac{f(x)-f(x_{0})-f'(x_{0})(x-x_{0})}{x-x_{0}}= \frac{f(x)-f(x_{0})}{x-x_{0}}-\frac{f'(x_{0})(x-x_{0})}{x-x_{0}}=\frac{f(x)-f(x_{0})}{x-x_{0}}-f'(x_{0})$  
 $f'(x)-f'(x)=0$

viceversa se $\exists p(x)=f(x_{0})+o(x-x_{0}):\frac{f(x)-p(x)}{x-x_{0}}$ dobbiamo dimostrare che $\exists f'(x_0)$ 
$r(x)=\frac{f(x)-f(x_{0})}{x-x_{0}}=\frac{f(x)-p(x)+p(x)-f(x_{0})}{x-x_{0}}=\frac{f(x)-p(x)}{x-x_{0}}+\frac{o(x-x_{0})}{x-x_{0}}=a\implies\exists f'(x_{0})=a$

dunque $\exists f'(x_{0}) \iff$ in un intorno di $x_{0} \ f$ si può approssimare con un polinomio di primo grado $p(x)=f(x_{0})+f'(x_{0})(x-x_{0})$

###### INTERPRETAZIONE GEOMETRICA
![[Schermata del 2026-06-22 16-23-35.png]]
$s$ (retta secante) congiunge i punti $(x_{0}, f(x_{0}))$ e $(x_{0}+h, f(x_{0}+h))$
$s: \frac{x-x_{0}}{x_{0}+h-x_{0}}=\frac{y-f(x_{0})}{f(x_{0}+h)-f(x_{0})}\iff y=f(x_{0})+\frac{f(x_{0}+h)-f(x_0)}{h}(x-x_{0})$

per $h\to 0$ si ha: $x_{0}+h\to x_{0}$ e $R(h)\to f'(x_{0})$ quindi la retta $s$ tende alla "posizione limite": $y=f(x_{0})+f'(x_{0})(x-x_{0})$

$t=$ tangente al grafico nel punto di ascissa $x_{0}$
---
se $\displaystyle{\lim_{x\to x_{0}^{-}}r(x)=l\neq\lim_{{x\to x_{0}^{+}}}r(x)=L}$
$x_{0}$ punto angoloso.
$l=f_{-}'(x_{0})$ derivata sinistra
$L=f_{+}'(x_{0})$ derivata destra 
![[Punto_angoloso.png|331]]
e la funziona sarà non derivabile.

---

se $r(x)$ diverge si può dimostrare che il grafico ha tangente verticale.

punto di flesso -\gt una funzione ha tangente verticale se $f''(x)$ cambia segno

punto cuspidale -\gt in una cuspide, la funzione è continua in $x_0$, ma le derivate da destra e da sinistra tendono entrambe a infinito con segni opposti.

---
### REGOLE DI DERIVAZIONE 
Se hai una funzione $f$ derivabile in $x_0$ e una costante reale $h$, la derivata della funzione moltiplicata per la costante è uguale alla costante moltiplicata per la derivata della funzione.
$f(a,b)\in \mathbb{R}$  $x_{0}\in (a,b)$  $\exists f'(x_{0})$
$h\in \mathbb{R}$ ne consegue $g(x)=hf(x)$   si ha $g'(x_{0})=hf'(x_{0})$

---

La derivata di una somma di funzioni derivabili è uguale alla somma delle rispettive derivate.
$f,g:(a,b)\to \mathbb{R}$  $x_{0}\in (a,b)$   $\exists f'(x_{0}), g'(x_{0})$
consegue: $s(x)=f(x)+g(x)$ si ha $s'(x_{0})=f'(x_{0})+g'(x_{0})$

ne segue che posto $c(x)=hf(x)+hg(x)$ si ha $c'(x_{0})=hf'(x_0)+hg'(x_0)$

---

Se una funzione è derivabile in un punto e in quel punto non si annulla (condizione fondamentale per non dividere per zero), allora anche la sua funzione reciproca è derivabile in quel punto.

Sia $f:(a,b)\to \mathbb{R}$   $x_{0}\in (a,b)$  $\exists f'(x_{0})$    $f(x_{0})\neq 0$
possiamo constatare la funzione reciproca $f(x)=\frac{1}{f(x)}$
si ha $f'(x_{0})=-\frac{f'(x_0)}{(f(x_{0}))^2}$ (opposto della derivata prima cambiata di segno fratto $f(x)^2$)

---

Siano $f,g:(a,b)\to \mathbb{R}$   $x_{0}\in(a,b)$   $\exists f'(x_{0}), g'(x_{0})$   $g(x_{0})\neq 0$
considerato  $q(x)=\frac{f(x)}{g(x)}$   si ha $q'(x_{0})=\frac{f'(x_{0})g(x_{0})-f(x_{0})g'(x_{0})}{(g(x_{0}))^2}$ 

---

Siano 
$f:(\alpha,\beta)\to \mathbb{R}$
$g:(a,b)\to (\alpha, \beta)$
$x_{0}\in (a,b)$
$\exists g'(x_{0}), \exists f'(g(x_{0}))$
considerata la funzione composta $f(x)=f(g(x))$  si ha $f'(x_{0})=f'(g(x_0))g'(x_{0})$
#### FUNZIONE INVERSA 
IP  $f:(a,b)\to R$ strettamente crescente e continua 
considerata $f^{-1}:[\ f(a) , f(b)\ ]\to [a,b]$ sappiamo che è strettamente crescente e continua.
sia $y_{0}\in [\ f(a), f(b) \ ]\implies y_{0}=f(x_{0})$ con $x_{0}\in [a,b]$
 supposto che $\exists f'(x_{0})\neq 0$
 
 TS  $f^{-1}(y_{0})=\frac{1}{f'(x_{0})}$
 
## DERIVATE FUNZIONI ELEMENTARI
1. $f(x)= x\implies f'(x)=0$
2. $f(x)=x^{n}\implies f'(x)=nx^{n-1} \therefore \frac{x^{n}-x_{0}^{n}}{x-x_{0}}=nx^{n-1}$ 
3. $f(x)=x^{-n}=\frac{1}{x^{n}}\implies f'(x)=\frac{-nx^{n-1}}{x^{2n}}=-nx^{-n-1}$ 
4. $f(x)=e^{x}\implies f'(x)=e^{x} \therefore \frac{e^{x}-e^x_{0}}{x-x_{0}}=e^{x_{0}}$
5. $f(x)=\log_{}x\implies f'(x)=\frac{1}{x}$  
6. $f(x)=|x|\implies f'(x)=\frac{|x|}{x}$

sia $f$ derivabile e non nulla, considerato $f(x)=\log_{}|f(x)|$
$f'(x)=\frac{1}{|f(x)|}\equiv \frac{|f(x)|}{x}\equiv \frac{f'(x)}{f(x)}$

$f(x)=x^\alpha$   $\alpha\in R$   $x\gt0$ 

$f(x)=x^{\alpha e^{\alpha \log x}\implies}f'(x)=e^{\alpha \log_{} x} = \alpha \frac{1}{x}=x^{\alpha }\alpha\frac{1}{x}=\alpha x^{\alpha-1}$ 

$x^{\alpha}\cdot \alpha x^{-1}=\alpha x^{\alpha - 1}$ 

---

$f(x)=\sin x$    $R(h)=\frac{\sin(x_0+h)-\sin(x_{0})}{h}=\frac{\sin x_{0}\cdot \cos h+\cos x_{0}\cdot \sin h-\sin x_{0}}{h}=\sin x_{0}\frac{\cos h-1}{h}+\cos x_{0}\frac{\sin h}{h}\to \cos x_{0}$

$f(x)=\cos x\implies f'(x)=-\sin x$
$f(x)=\tan x=\frac{\sin x}{\cos x}\implies f'(x)=\frac{\cos^{2}x+\sin^{2}x}{cos^{2}x}=1+\tan^{2}x$ 

---

$f:(a,b)\to R$  $x_{0}\in(a,b)$ 
$f'(x_{0})=\lim\limits_{x\to x_{0}}\frac{f(x)-f(x_{0})}{x-x_{0}}=\lim\limits_{h\to 0}\frac{f(x_{0}+h)-f(x_{0})}{h}$

$f_{-}'(x_{0})=\lim\limits_{x\to x_{0}^-}r(x)$  derivata sinistra
$f_{+}'(x_{0})=\lim\limits_{x\to x_{0}^{+}}r(x)$  derivata destra 

#### DERIVATE PER STUDIO DI FUNZIONE 
Ricordiamo che data $f:(a,b)\to R$ 
- $f$ cresce strettamente in $(a,b)$ se $x\lt y\implies f(x)\lt f(y)$
- f cresce strettamente in $x_{0}\in(a,b)$ se $\exists r\gt0:\begin{cases}]x_{0}-r, x_{0}[ \ f(x)\lt f(x_{0}) \\  ]x_{0}, x_{0}+r[ \ f(x)\gt f(x_{0})\end{cases}$
- $x_{0}\in (a,b)$ è un punto di min (o max) per $f$ se $\exists r\gt0:\forall x\in I(x_{0}, r): f(x)\geq (\leq) f(x_{0})$
## TEOREMA DI FERMAT
sia $f:(a,b)\to R$ , sia $x_{0}\in\ ]a,b[$  punto di max o min relativo e supponiamo che $\exists f'(x_{0})$ allora $f'(x_{0})=0$

$\gt$ il teorema fornisce una condizione necessaria per l'esistenza di punti di estremo relativo all'interno dell'intervallo.
$\gt$ la condizione non è sufficiente ma necessaria.

###### DIMOSTRAZIONE
$x_{0}\in ]a,b[$
$\exists f'(x_{0})\implies f_{-}'(x_{0})=f_{+}'(x_{0})$ 

$\begin{cases}f_{-}'(x_{0})=\lim\limits_{x\to x_{0}^{-}}\frac{f(x)-f(x_{0})}{x-x_{0}}\leq 0 \\  f_{+}'(x_{0})=\lim\limits_{x\to x_{0}^{+}}\frac{f(x)-f(x_{0})}{x-x_{0}} \geq 0\end{cases}\implies f_{-}'(x_{0})=f_{+}'(x_{0})=0$

sia $x_{0}\in ]a,b[: f'(x_{0})=0$ , $x_{0}$ è detto ==punto stazionario==
## TEOREMA DI ROLLE
IP  $f:[a,b]\to R$ continua
$f$ derivabile in $]a,b[$
$f(a)=f(b)$ 

TS  $\exists c\in]a,b[:f'(c)=0$
###### DIMOSTRAZIONE 
per il teorema di weierstrass:
$\exists x_{1}, x_{2} \in [a,b]:$
$f(x_1)=\min_{[a,b]}f$
$f(x_{2})=\max_{[a,b]}f$
$\gt$ se uno di essi è interno, ad es $x_{1}\in]a,b[$ si ha $f(x_{1})=0$ per il teorema di fermat.
$\gt$ se $x_{1}=a$ e $x_{2}=b$ o viceversa $\iff \min_{}f=\max_{}f\implies$ $f$ è costante $\implies f'(x)=0   \ \ \ \forall x\in[a,b]$

## TEOREMA DI LAGRANGE
IP  $f:[a,b]\to R$  continua 
$f$ derivabile in $]a,b[$ 

TS  $\exists c\in\ ]a,b[: \frac{f(b)-f(a)}{b-a}=f'(c)$

###### DIMOSTRAZIONE 
$g(x)=(f(b)-f(a))x-(b-a)f(x)$
$g$ è continua in $[a,b]$ e derivabile in $]a,b[$, vediamo se $g(a)=g(b)$

$g(a)=f(b)a-f(a)a-bf(a)+af(a)$
$g(b)=f(b)b-f(a)b-bf(b)+af(b)=g(a)$
quindi per il teorema di rolle $\exists c\in ]a,b[:g'(c)=0$

si ha $g'(x)=f(b)-f(a)-(b-a)f'(x)$
$g'(c)=0\implies f(b)-f(a)=(b-a)f'(c)\implies TS$

##### CRITERI DI MONOTONIA 
$f:(a,b)\to \mathbb{R}$ derivabile 
1. $f'(x_{0})\geq 0$    $\forall x\in(a,b)\to$ $f$ crescente in $(a,b)$
	se $x\lt y$ per il teorema di lagrange $\exists c\in(a,b)\implies f$ strettamente crescente in $(a,b)$
2. (stretta monotonia) $f'(x)\gt0 \ \ \forall x\in(a,b)\implies f$ strettamente crescente in $(a,b)$
	però per $f(x)=x^3$ la condizione non è verificata
3. (stretta monotonia generale)
	CNS affinché $f$ sia strettamente crescente in $(a,b)$: $f'(x)\geq 0 \ \ \ \forall x\in(a,b)$
	 $\not\exists(c,d)\subseteq(a,b): f'(x)=0 \ \ \ \forall x\in(c,d)$
#### TEOREMA SULLE FUNZIONI CON DERIVATA NULLA
IP $f:(a,b)\to R$
$f'(x)=0$   $\forall x \in (a,b)$
TS $f$ è continua in $(a,b)$
###### DIMOSTRAZIONE 
scelto $x_{0}\in(a,b)$, dimostriamo che $f(x)=f(x_{0}) \ \ \ \forall x\in(a,b)$
sia dato $x$, ad esempio $x\gt x_{0}$ e applichiamo il teorema di lagrange nell'intervallo $[x_{0},x]$ .
$\exists c\in ]x_{0}, x[: f(x)-f(x_{0})=f'(c)(x-x_{0})=0$
#### TEOREMA DI PROLUNGAMENTO DELLA DERIVATA 
IP   $f:(a,b)\to R$   $c\in(a,b)$
$f$ derivabile in $(a,b) / \{c\}$
$f$ continua in $c$
$\exists \lim\limits_{x\to c}f'(x)=l \ \ \ \ (l\in R\vee l=+\infty)$

TS $\lim\limits_{x\to c}\frac{f(x)-f(c)}{x-c}=l$

#### STUDIO DEI PUNTI STAZIONARI#
$f:(a,b)\in R  \ \ \ \ \ c\in]a,b[ \ \ \ \ \ f'(c)=0$ (punto stazionario)
per il teorema di fermat, $c$ potrebbe essere un punto di estremo relativo.
per sapere se lo è occorre trovare $r\gt0$ : in $I(c,r) \ \ f(x)$ è sempre $(\leq) \vee (\geq) f(c)$

---

Supponiamo che $f$ sia derivabile in $(a,b)$, studiamo il segno di $f'$
![[Schermata del 2026-06-23 13-18-51.png]]
allora $c$ è un punto di estremo relativo.

infatti, se $f'(x) \lt0$ per $x \lt c$, $f'(x)\gt0$ per $x\gt c$ allora:
a sinistra di $c$, $f$ è decrescente $\implies f(x)\gt f(c)$

$\begin{cases}\text{a sinistra di } c, f \text{ è decrescente} \implies f(x)\gt f(c) \\ \text{a destra di } c, f\text{ è crescente}\implies f(x)\gt f(c)\end{cases}\implies c$ punto di minimo relativo

## TEOREMA DI DE L'HOPITAL
IP  $f,g:(a,b) / \{x_{0}\}\to R$  derivabile
$\lim\limits_{x\to x_{0}}f(x)=\lim\limits_{x\to x_{0}}g(x)=0   (+\infty/-\infty )$ 
$g^{t}(x)\neq 0 \ \ \ \ \forall x\in(a,b) / {c}$
$\exists \lim\limits_{x\to x_{0}}\frac{f'(x)}{g'(x)}=l$
