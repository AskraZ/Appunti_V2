# Indice
[[#Parte I]]
[[#Parte II]]

# Parte I
# LOGICA PROPOSIZIONALE
la logica proposizionale è strettamente collegata al mondo binario costituito da {0,1}. 
- il vocabolario consiste di un insieme di variabili proposizionali $P$ di solito denotate con $p,q,r$ con eventuale numerazione sottoscritta, ovvero $p_{1},p_{2}.$
- le variabili proposizionali possono assumere solo 2 valori: 1 o 0, rispettivamente Vero e Falso.
le formule più complesse si possono costruire tramite i connettivi logici:
- $\neg \rightarrow$ è la negazione
- $\wedge \rightarrow$ è la congiunzione (e)
- $\vee  \rightarrow$ è la disgiunzione (o)
- $\implies \rightarrow$ è l'implicazione (se ... allora ....)
- $\iff \rightarrow$ è la co-implicazione (se e solo se)

**ESEMPI DI FORMULE**
$\neg P \rightarrow$ non P 
$P \vee Q \rightarrow$ P o Q
$P \wedge Q \rightarrow$ P e Q
$P \implies Q \rightarrow$ se P allora Q
$P \iff Q \rightarrow$ P se e solo se Q
 > $\neg$ ha la precedenza sugli altri connettivi, $\vee$ e $\wedge$ hanno la stessa precedenza

una interpretazione I su $P$ è una funzione  $I:P\rightarrow \{0,1\}$.
date due formule $P_{1}$ e $P_{2}$ e data una interpretazione $I$ che assegna i valori di verità alle variabili:
- $I(\neg P_{1})$ è vera se e solo se $I(P_{1})$ è falsa
- $I(P_{1}\vee P_{2})$ è vera se e solo se almeno una tra $I(P_{1})$ e $I(P_{2})$ è vera
- $I(P_{1}\wedge P_{2})$ è vera se e solo se $I(P_{1})$ e $I(P_{2})$ sono entrambe vere
- $I(P\implies P_{2})$ è vera se $I(P_{1})$ è falsa oppure se $I(P_{2})$ è vera
- $I(P_{1}\iff P_{2})$ è vera se e solo se $I(P_{1}\implies P_{2})$ è vera e $I(P_{2}\implies P_{1})$ è pure vera

![[Screenshot 2025-10-21 213039.png]]

Una formula P si dice ==soddisfacibile== se esiste una interpretazione I delle variabili proposizionali tale che la formula risulti vera.
$$p\vee(q\wedge\neg p)$$
Una formula P si dice ==insoddisfacibile== se per ogni interpretazione I delle variabili proposizionali non esiste nessuna interpretazione tale che la formula sia vera.
$$p\wedge(q\vee \neg p)\wedge(\neg q\wedge \neg p)$$
una formula P si dice tautologia se per ogni interpretazione I delle variabili proposizionali la formula risulterà sempre vera.
![[Screenshot 2025-10-21 224102.png]]

**PROPRIETA' CONNETTIVI LOGICI**
- $p\vee q\equiv q\vee p$ COMMUTATIVITA'
- $p\wedge q\equiv q\wedge p$ COMMUTATIVITA'
- $p\vee(q\vee r)\equiv (p\vee q)\vee r$ ASSOCIATIVITA'
- $p\wedge(q\wedge r)\equiv(p\wedge q)\wedge r$ ASSOCIATIVITA'
*ALTRE EQUIVALENZE LOGICHE*
- $\neg (\neg p)=p$
- $p\implies q\equiv \neg q\implies \neg p$
- $p\implies q\equiv \neg p\vee q$
- $p\iff q\equiv(p\implies q)\wedge(q\implies p)$
- **LEGGI DI DE MORGAN**
  - $\neg(p\vee q)\equiv \neg p\wedge \neg q$
  - $\neg(p\wedge q)\equiv \neg p\vee \neg q$
-  $p\wedge(q\vee r)\equiv(p\vee q)\wedge(p\vee r)$
- $p\vee(q\wedge r)\equiv(p\vee q)\wedge(p\vee r)$
**GIUSTIFICAZIONE LOGICA**
sia $P$ un insieme di proposizioni e P una proposizione.
diciamo che $P$ giustifica P e lo denotiamo con $$P\models P$$
se ogni interpretazione I che soddisfa tutte le formule di $P$ soddisfa anche P.
**ESEMPIO**
sia $P=\{p,p\implies q\}$ allora $P\models q$
dimostriamo che se $P=\{p\vee r,q\vee \neg r\}$ allora $P\models p\vee q$
**CNF**
una formula p è in forma normale congiuntiva (CNF) se è scritta come congiunzione di disgiunzioni, per esempio $$(p\wedge q)\vee(\neg p\wedge \neg r\wedge s)$$
**DNF**
una formula p è in forma normale disgiuntiva (DNF) se è scritta come disgiunzione di congiunzioni, per esempio $$(p\wedge q)\vee(\neg p\wedge \neg r\wedge s)$$
# INSIEMI 
un insieme è univocamente caratterizzato dal suo contenuto, ovvero dagli elementi che gli appartengono.
> **APPARTENENZA**
> se $T$ è un insieme, l'espressione $x\in T$ si legge "x appartiene a T" oppure "x è un elemento di T"

> **NON APPARTENENZA**
> scriveremo invece $x\not\in T$ per negare l'espressione precedente, cioè per affermare che x non appartiene a T

dal momento che un insieme è caratterizzato dal suo contenuto, due insiemi che contengono gli stessi elementi, sono lo stesso insieme.
> **DEFINIZIONE** (Uguaglianza tra Insiemi)
> Due insiemi A e B sono uguali se hanno gli stessi elementi:
> $$A=B\iff(\forall x)(x\in A\iff x\in B)$$

- quando è possibile, si può definire un insieme elencando semplicemente i suoi elementi:
  $\{1,2,3\}=$ l'insieme i cui elementi sono $1,2,3$
>**SINGOLETTO**
>la notazione $\{a\}$ indica l'insieme costituito dal solo elemento a, detto singoletto

>**INSIEME VUOTO**
>con il simbolo $\emptyset$ indicheremo l'insieme vuoto, senza nessun elemento

>**UGUAGLIANZA**
>dalla definizione di uguaglianza  possiamo dedurre che se $A=\{1,2,3\}$ e $B=\{2,1,2,3,1\}$ possiamo definirli uguali perché contengono gli stessi elementi

possiamo definire un insieme anche esplicitando la proprietà che caratterizza i suoi elementi:
$$\{x:\text{la proprietà P è vera per x}\}\equiv\{x:P(x)\}$$ per ogni valore di $x$, $P(x)$ può assumere i valori vero e falso.

**CARDINALITA'**
Ad ogni insieme si può associare un'importante caratterizzazione: la quantità degli elementi che gli appartengono.
>**DEFINIZIONE** (CARDINALITA')
>dato un insieme A, il numero di elementi che lo costituisce è denominato cardinalità dell'insieme ed è denotata con $|A|$.
>se $|A|$ è un numero intero l'insieme si dice finito, altrimenti infinito.

**ESEMPIO**
la cardinalità dell'insieme vuoto è quindi zero, $|\emptyset|=0$ , mentre $|\{1,2,3\}|=3$ e $|\{a\}|=1$.
la cardinalità dell'insieme $|\{x:x\text{ è un numero pari}\}|=+\infty$ 

**INCLUSIONE**
se abbiamo A e B e tutti gli elementi di A sono elementi di B, allora diciamo che A è incluso in B, ovvero che A è un sottoinsieme di B.
>**DEFINIZIONE** (INCLUSIONE)
>A è un sottinsieme di B, denotato con $A\subseteq B$ se $(\forall x)(x\in A\implies x\in B)$
>in questo caso possiamo anche definire B come sovrainsieme di  $B\supseteq A$

**INSIEMI DISCRETI**
> **DEFINIZIONE** (Insieme Discreto)
> Un insieme A si dice discreto se è possibili ordinare i suoi elementi in maniera tale che tra un qualunque elemento ed il successivo non vi siano altri elementi nell'insieme.

## OPERAZIONI TRA INSIEMI
**UNIONE**
l'unione di due insiemi A e B è l'insieme formato da:
$$A\cup B=\{x:x\in A\vee x\in B\}$$
- $A\cup B=B\cup A \rightarrow$ COMMUTATIVITA'
- $A\cup (B\cup C)=(A\cup B)\cup C \rightarrow$ ASSOCIATIVITA'

**INTERSEZIONE**
l'intersezione di due insiemi A e B è l'insieme formato da quegli elementi che appartengono ad entrambi gli insiemi A e B:
$$A\cap B=\{x:x\in A\wedge x\in B$$
- $A\cap B= \emptyset \rightarrow$ insiemi disgiunti 
- $A\cap B=B\cap A \rightarrow$ COMMUTATIVITA'
- $A\cap (B\cap C)=(A\cap B)\cap C \rightarrow$ ASSOCIATIVITA'

**CARDINALITA' DELL'UNIONE**
se A e B sono insiemi finiti allora:
$$|A\cup B|=|A|+|B|-|A\cap B|$$
se sono disgiunti:
$$|A\cup B|=|A|+|B|$$
**ALTRE PROPRIETA'**
- $A\cap A=A$ e $A\cup A=A$
- PROPRIETA' DISTRIBUTIVA 
  - $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$ 
  - $A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$
- PROPRIETA' DI ASSORBIMENTO
  - $A\cap(A\cup B)=A$
  - $A\cap(A\cup B)=A$

**DIFFERENZA DI INSIEMI**
la differenza di due insiemi A e B denotata con $A /B$ è l'insieme:
$$A / B=\{x:x\in A\land x\not\in B\}$$
**CARDINALITA' DELLA DIFFERENZA**
$$|A /B|=|A|-|A\cap B|$$
**INSIEME UNIVERSO**
definiamo un insieme $U$ tale che sia un sovrainsieme di tutti gli insiemi, il complemento di un insieme è l'insieme di tutti gli elementi che non appartengono a quell'insieme.
#### notazione
$U /A=A^{c}\rightarrow$ complemento  di A.

**ESEMPIO**
> se $A=\{1,2,3\}$ e $U=\{1,2,3,\dots,10\}$ 
> $A^{c}=\{4,5,\dots,10\}$

**PROPRIETA'**
- $(A^c)^c=A$
- $(A\cap B)^c=A^c\cup B^c$
- $(A\cup B)^c=A^c\cap B^c$

>**CARDINALITA' DEL COMPLEMENTO**
>se U è finito e $A\subseteq U$ allora $|A^c|=|U|-|A|$

**DIFFERENZA SIMMETRICA**
la differenza simmetrica è l'insieme degli elementi che non appartengono ad entrambi gli insiemi:
$$A\Delta B=(A / B)\cup(B / A)$$
> **ESEMPIO**
> se $A=\{1,2,3\}$ e $B=\{3,4,5\}$
>$A\Delta B=\{1,2,4,5\}$

- COMMUTATIVA
- ASSOCIATIVA

**CARDINALITA' DIFFERENZA SIMMETRICA**
>$|A\Delta B|=|(A / B)\cup(B / A)|=|A / B|+|B / A|=|A|-|A\cap B|+|B|-|B\cap A|=|A|+|B|-2|A\cap B|$


**FAMIGLIE DI INSIEMI**
dato un insieme T, consideriamo un insieme i cui elementi sono tutte le parti o sottoinsiemi di T.
#### notazione
scriveremo questo insieme come $pow(t)$
> **ESEMPIO**
> sia $T=\{1,2,3\}$
> $pow(T)=\{\emptyset,1,2,3,(1,2),(1,3),(2,3),(1,2,3)\}$

gli elementi dell'insieme delle parti sono $2^n$  (n=elementi)

una famiglia di insiemi che ha un numero infinito di elementi è una famiglia infinita.
se invece ha un numero finito di elementi allora è una famiglia finita.
>**ESEMPIO**
>sia $F=\{P,D\}$ dove $P$ è l'insieme dei numeri pari (infinito) e $D$ l'insieme dei numeri dispari (infinito). 
>la famiglia $F$ è una famiglia finita.
>**ESEMPIO**
>sia $F=\{P_{1},P_{2},P_{3},\dots\}$ dove $P_{i}=\{2^{1},\dots,2^n\}$
>la famiglia è infinita ma tutti i suoi elementi sono insiemi finiti.

analogamente, se $F$ è una famiglia qualunque di insiemi, si indica con:
$$\bigcap_{x\in\mathcal{F}} X$$
l'insieme costituito dagli elementi che appartengono a tutti gli insiemi $x\in \mathcal{F}$ e viene detto insieme intersezione della famiglia $\mathcal{F}$ :
$$\bigcap_{x\in\mathcal{F}}X=\{x:\forall X\in\mathcal{F, x\in X}\}$$
sia dato un insieme U ed una operazione definita su uno o più elementi di U.
se l'operazione può essere definita all'interno di U allora diciamo che U è chiuso rispetto a tale operazione.
**ESEMPI**
>sia $U=N$ se consideriamo la somma, N è chiuso rispetto alla somma.
>se consideriamo la sottrazione, N non è chiuso rispetto alla sottrazione.

> $X=\{1,2,3\}$  consideriamo l'operazione $mcm\{1,2,3\}$ , X non è chiuso rispetto a mcm perché $mcm(2,3)=6$

> **DEFINIZIONE** 
> sia $F$ una famiglia di insiemi
> - diciamo che F è chiusa rispetto all'unione se per ogni coppia di insiemi X e Y appartenenti a $F$ anche $X\cup Y$ appartiene a $F$
> - diciamo che F è chiusa rispetto all'intersezione se per ogni coppia di insiemi X e Y appartenenti a $F$ anche $X\cap Y$ appartiene a $F$

#ESEMPI
> Sia $F=\{\{1,2,3\},\{1,2\},\{1,3\}\}$ abbiamo che $F$ è chiuso rispetto all'unione ma non è chiuso rispetto all'intersezione
> perché $\{1,2\}\cap\{1,3\}=\{1\}\not\in F$

sia $F$ una famiglia di insiemi, tutti sottinsiemi di un insieme universo $U$.
quindi, $F\subseteq pow(U)$.
in particolare, per ogni $X\in F$ , $X^{c}= U / X$ è anche un elemento di $pow(U)$.
possiamo allora definire la famiglia "complemento" rispetto ad U, e la denotiamo con $F^{c}$ come segue:
$$F^{c}=\{X^{c}:X\in F\}$$
e notiamo $(F^{c})^{c}=F$ 

> **TEOREMA**
> la famiglia F è chiusa rispetto all'unione (risp. intersezione) $\iff$ la famiglia $F^c$ è chiusa rispetto all'intersezione (risp. unione)
> #DIMOSTRAZIONE
> se $F$ è chiusa rispetto all'unione.
> siano $X,Y\in F^{c}$. esistono allora $A,B\in F$ tali che  $X=A^{c}$ e $Y=B^{c}$ . 


# Parte II
sull'insieme $N$ sono definite due operazioni:
- Somma (+): $N \times N\rightarrow N$ che ad ogni coppia di numeri (n,m) associa il numero $n+m\in N$ 
- Prodotto($\cdot$): $N\times N\rightarrow N$ che ad ogni coppia di numeri (n,m) associa il numero $n\cdot m\in N$
sull'insieme $Z$ sono definite tre operazioni
- Somma e Prodotto: già definite in $N$ 
- Differenza(-): $Z\times Z\rightarrow Z$ che ad ogni coppia di numeri (n,m) associa il numero $n-m\in Z$

>VALORE ASSOLUTO
>il valore assoluto di un intero relativo $n\in Z$ è l'intero $|n|\geq 0$ definito come $$|n|=\begin{cases}
n,  & se \ n\geq 0 \\
-n,  & se \ n\lt 0
\end{cases}$$

**ALCUNE PROPRIETA'**
per ogni $n,m\in Z$ abbiamo:
- $|n|=0 \iff n=0$
- $|n\cdot m|=|n|\cdot|m|$
- $n+|n|\geq 0$ ed in particolare $n+|n|=0 \iff$ $n\leq 0$.

#### DEFINIZIONE ASSIOMATICA $N$
- esiste un numero naturale $0$
- ogni numero naturale $a$ ha un numero naturale successore, denotato come $S(a)$
- non esiste un numero naturale il cui successore è $0$
- numeri naturali distinti hanno successori distinti: se $a\neq b\implies S(a)\neq S(b)$ 
> NOTA 
	avendo definito la funzione + abbiamo che:
	- $S(0)=1$
	- per ogni numero naturale $a,\ S(a)=a+1$
	- infine, dato un numero naturale $n$ ed il suo successore $S(n)$ diciamo che $n$ è il predecessore di $S(n)$ , denotato con $P(S(n))$.
	- Quindi, ogni numero naturale $n$, tranne lo $0$, ha un predecessore che è il numero $n-1$ 

$$
\begin{cases}
a\le a \\ 
a\lt S(a) \\
a\lt b \text{ se esiste } c\in N \text{ tale che } a\lt c \wedge c\lt b
\end{cases}
$$

> ASSIOMA DEL BUON ORDINAMENTO
> se $S$ è un qualunque insieme non vuoto di numeri naturali, allora 
in $S$ esiste un elemento minimo, ovvero esiste $s\in S$ tale che $s\le 
t$ per ogni $t\in S$ 

**PROPRIETA'** ($Z$)
SOMMA  
- $a+b=b+a$
- $a+b+c=a+(b+c)=(a+b)+c$
- $a+0=0+a=a$

PRODOTTO
- $a\cdot b=b\cdot a$ 
- $a\cdot b\cdot c=a\cdot(b\cdot c)=(a\cdot b)\cdot c$
- $a\cdot(b+c)=(a\cdot b)+(a\cdot c)$
- $a\cdot 1=1\cdot a=a$
- $a\cdot 0=0\cdot a=0$

#### PRINCIPIO DI INDUZIONE
- se una proprietà $P$ è posseduta dal numero $0$ e la proprietà $P$ è 
posseduta anche dal successore di ogni numero naturale che possiede la 
proprietà $P$, allora la proprietà $P$ è posseduta da tutti i numeri 
naturali

> **TEOREMA**
> sia $P$ una affermazione riguardante i numeri naturali. se
> (a). $P(0)$ è vera, ed inoltre
> (b). per ogni numero naturale $n$ se $P(n)$ è vera allora è vera anche $P(n+1)$
	
##### DIMOSTRAZIONE 
ragioniamo per assurdo e supponiamo falsa la tesi, ossia supponiamo che 
esista almeno un numero naturale $n$ per cui $P(n)$ è falsa. 
costruiamo l'insieme:

$$S=\{n:n\in N, \text{ e } P(n) \text{ è falsa}\}$$

per la nostra ipotesi di assurdo $S$ non è vuoto. 
Per l'assioma del Buon Ordinamento esiste in $S$ un elemento minimo $s$.
per definizione di $S$, $P(s)$ è falsa.

# PARTE 3
## DISPOSIZIONI E COMBINAZIONI
- Dati due insiemi A e B, con $|A|=k, \ |B|=n$ quante sono le applicazioni di $A$ in $B$?
	- Numero delle disposizioni con Ripetizione di $n$ elementi di classe $k$: denotato con $F_{n,k}$
- Dati due insiemi A e B, con $|A|=k, \ |B|=n$ quante sono le applicazioni iniettive di A in B?
	- Numero delle disposizioni semplici di n elementi di classe k: denotato con $D_{n,k}$
- Dato un insieme B, con $|B|=n$, e preso un intero $k \leq n$, quanti sono i sottinsiemi di B composti di $k$ elementi?
	- Numero delle combinazioni di $n$ elementi di classe $k$: denotato con $C_{n,k}$
- Dato un insieme di $n$ variabili, $\{x_1,x_2,\dots,x_n\}$ e preso un intero $k \leq n$, quanti sono i monomi con coefficiente $1$ di grado k definiti sulle n variabili date?
	- Numero delle combinazioni di n elementi di classe k con ripetizione: denotato con $C^{r}_{n,k}$

---
#### DISPOSIZIONI CON RIPETIZIONE 
Per calcolare $F_{n,k}$ utilizziamo la regola del prodotto: per ognuno 
dei k elementi di $A$ dobbiamo scegliere uno tra gli elementi di $B$ che sono $n$.

$$F_{n,k}=n^{k}$$

###### ESEMPIO 
Quante sono le funzioni booleane definite su un insieme di $k$ variabili booleane?
$f:A\to\{0,1\}$
$F_{2,k}=2^k$

---

Devi impostare il pin dello smartphone, da $n = 4$ numeri e $k=0,1,\dots,9$ 
le possibili combinazioni sono $F_{n,k}=4^{10}$ 

#### DISPOSIZIONI SEMPLICI 
Come prima cosa, notiamo che affinché esista un'applicazione iniettiva 
da A in B, con $|A|=k$ e $|B|=n$ deve essere $n\geq k$.
per calcolare $D_{n,k}$ utilizziamo la regola del prodotto.
Dobbiamo fare $k$ operazioni di scelta tali che:
- La prima operazioni si può fare in $n$ modi
- la seconda operazione si può fare in $n-1$ modi, numero costante
- la $k$-esima operazione si può fare in $n-k+1$ modi, numero costante
allora il numero di scelte totali è:

$$D_{n,k}=n\cdot(n-1)\cdot\dots(n-k+1)=\frac{n!}{(n-k)!}$$

---

Quante squadre di calcio posso formare con un gruppo di 50 studenti?
$n =50$, $k=11$ 

$$\frac{50!}{(50-11)!}=\frac{50!}{39!}=50\cdot49\cdot48\cdot\dots\cdot40=1,5\cdot10^{18}$$

#### PERMUTAZIONI 
Il numero di permutazioni semplici è il numero di disposizioni semplici di classe $n$ 

$$D_{n,n}=n\cdot(n-1)\cdot\dots(n-n+1)=n!$$

---

In una mensola da 5 posti ho 5 libri, in quanti modi posso posizionare i libri?

$$D_{5,5}=5!=120$$

#### COMBINAZIONI
- Consideriamo l'insieme di tutte le $D_{n,k}$ applicazioni iniettive di un insieme A di $k\gt 0$ elementi in un insieme $B$ di $n$ elementi $(k\leq n)$ 

$$f\approx g\iff f(A)=g(A)$$

- Due applicazioni sono equivalenti se hanno la stessa immagine $D_{n,k}=C_{n,k}\cdot k!$ da cui ricaviamo 

$$C_{n,k}=\frac{n\cdot(n-1)\cdot\dots\cdot(n-k+1)}{k!}$$

I valori di $C_{n,k}$ sono detti coefficienti binomiali ed indicati con:

$$\binom{n}{k}$$

dato che: 

$$\binom{n}{k}=\frac{n\cdot(n-1)\cdot\dots\cdot (n-k+1)}{k!}=\frac{n\cdot(n-1)\cdot\dots\cdot (n-k+1)}{k!}\cdot \frac{(n-k)!}{(n-k)!}=\frac{n!}{k!(n-k)!}$$

$$\binom{n}{k}=\frac{n!}{k!(n-k)!}$$

---

In un bancone ci sono 10 gusti di gelato diversi, e ne puoi scegliere 3 differenti.

$$\binom{10}{3}=\frac{10!}{3!(10-3)!}=\frac{10!}{3!\cdot 7!}=\frac{10\cdot 9\cdot 8}{3\cdot 2}=\frac{720}{6}=120$$

---

In una classe ci sono 23 studenti, quante combinazioni di 7 persone sono possibili?

$$\binom{23}{7}=\frac{23!}{7!(23-7)!}=\frac{23!}{7!\cdot 16!}=\frac{23\cdot22\cdot 21\cdot 20\cdot 19\cdot 18\cdot 17}{7!}=\frac{1235591280}{5040}=245157$$

### TEOREMA BINOMIALE (FORMULA DI NEWTON)
Siano $a$ e $b \in \mathbb{R}$, allora 

$$(a+b)^{n}=\sum\limits^{n}_{k=0}a^{n-k}\cdot b^{k}$$

###### DIMOSTRAZIONE 
La potenza $(a+b)^{n}$ è il prodotto di $n$ fattori tutti uguali a $(a+b)$

$$(a+b)\cdot(a+b)\dots\cdot(a+b)$$

otteniamo una somma di monomi tutti di grado $n$ del tipo $a^{n-k}\cdot b^{k}$ con $0\leq k\leq n$
in particolare, i monomi $a^{n}b^{0}=a^{n}$ e $a^{0}b^{n}=b^{n}$ compariranno nella somma una sola volta.

Quante volte compare nella somma $a^{n-1}b$?

tante volte quanti sono i modi di scegliere $n-1$ degli $n$ fattori, da cui scegliere $a$ per sviluppare il prodotto, ovvero $\binom{n}{n-1}=n$.

In generale, il monomio $a^{n-k}b^{k}$ compare tante volte quanti sono i modi di scegliere $n-k$ degli n fattori da cui scegliere $a$ per sviluppare il prodotto, ovvero $\binom{n}{k}$ $\triangle$

[[Teorema Binomiale di Newton - Dimostrazione]]

---

$(a+b)^3$
$a^3b^0=a^{3}\to\binom{3}{0}=\frac{3!}{0!(3!)}=\frac{3!}{3!}=1$
$a^2b^{1}\to\binom{3}{1}=\frac{3!}{1!(2!)}=\frac{6}{2}=3$
$a^1b^2\to\binom{3}{2}=\frac{3!}{2!(1!)}=\frac{6}{2}=3$
$a^0b^3=b^3\to\binom{3}{3}=\frac{3!}{3!(3-3)!}=\frac{6}{6}=1$

$$a^3+3a^2b+3ab^2+b^3$$

---

1. $\sum\limits^{n}_{k=0}\binom{n}{k}=2^{n}$, infatti:

$$2^{n}=(1+1)^{n}=\sum\limits^{n}_{k=0}1^{n-k}\cdot1^{k}=\sum\limits^{n}_{k=0}\binom{n}{k}$$

---
#### COMBINAZIONI CON RIPETIZIONE 
Dato un insieme di $n\gt 1$ variabili, $\{x_{0},x_{1},\dots,x_{n-1}\}$ e preso un intero $k$, i monomi di grado $k$ sono:

$$C^{r}_{n,k}=\binom{n+k-1}{k}$$

###### ESEMPIO 
Dato un insieme di 3 variabili, i monomi di grado 2 sono i seguenti:

$$6=\binom{3+2-1}{2}=\binom{4}{2}=\frac{4!}{2!(4-2)!}=\frac{24}{4}=6$$

---

Dati 5 ragazzi, e dati 23 ghiaccioli uguali, quanti modi diversi di darli abbiamo?

$$\binom{27}{23}=\frac{27!}{23!(4)!}=\frac{421200}{24}=17550$$

## PIGEONHOLE PRINCIPLE
Nella sua forma più semplice, il principio afferma che se dobbiamo fare 
entrare $n+1$ piccioni in una piccionaia che contiene $n$ cassette, 
allora almeno una cassetta deve contenere più di un piccione.
Più in generale, se abbiamo $n=km+1$ ogetti da sistemare in m 
contenitori, allora almeno un contenitore deve contenere $k+1$ oggetti.

---

Immaginiamo di avere il cassetto di un comodino pieno di calzini, neri e blu.
vogliamo prendere al buio, il numero minimo di calzini sufficiente ad 
avere una coppia completa.
Immaginiamo che ogni cassetto sia un colore, se prendiamo 3 calzini ne 
avremo almeno due di un solo colore.
infatti possiamo avere o 3 calzini dello stesso colore o 2 dello stesso 
colore e uno differente.

---
Un essere umano in media ha circa $11000$ capelli in testa, alcuni 
$15000$ e altri $20000$.
Esistono a catania due persone che hanno lo stesso numero di capelli?
- SI:
	- Catania ha più di $300000$ abitanti
	- Dal momento che il numero di abitanti è superiore al numero massimo 
di capelli possibile, allora ci saranno almeno due individui con lo 
stesso numero di capelli

## PROBABILITÀ DISCRETE
La definizione classica della probabilità del verificarsi di un evento A
 è il rapporto tra il numero di casi favoreli $f_A$ ed il numero di casi totali $n$.

$$P(A)=\frac{f_A}{n}$$

> Questa definizione assume che ogni evento ha la stessa probabilità di accadere.

---
###### ESEMPIO
L'evento è "Esce un numero inferiore a $3$" lo spazio dei campioni è 
costituito da tutti i possibili esiti $S=\{1,2,3,4,5,6\}$ e gli esiti 
favorevoli sono $r=\{1,2\}$.

$$\frac{r}{S}=\frac{2}{6}=\frac{1}{3}$$

#### TEORIA DELLA PROBABILITÀ
Assiomi della teoria della probabilità:
- Siano  A e B due eventi qualsiasi $\subset S$
1. $0\leq P(A)\leq 1$ (la probabilità che accada qualcosa è compresa tra
 il non accadere e l'accade certamente).
2. $P(S) = 1$  e $P(\emptyset)=0$ (la probabilità uno di tutti gli 
eventi possibili è 1, mentre la possibilità che accada un evento non 
esistente è 0).
3. $P(A\cup B)=P(A)+P(B)-P(A\cap B)$ (la probabilità che accadano uno 
dei due eventi o entrambi)
	1. se $A\cap B = \emptyset$ significa che entrambi gli eventi non potranno mai 
accadere, quindi $P(A\cup B)=P(A)+P(B)$

---

Il verificarsi di un evento talvolta può cambiare la probabilità che si 
verifichi un altro evento:

$$P(A|B)=\frac{P(A\wedge B)}{P(B)}$$

#### INDIPENDENZA
Lanciamo un dado 3 volte, la probabilità di ottenere $[3,3,3]$ è la 
stessa di ottenere $[2,1,6]$ o $[6,5,1]$.

#### REGOLA DI BAYES 
La probabilità di un evento A, condizionata al verificarsi di un evento B (non nullo) è definita come:
$$P(A|B)=\frac{P(A\wedge B)}{P(B)}=P(A|B)\cdot P(B)=P(A\wedge B)$$
Stesso risultato è $P(B|A):$
$$P(B|A)=\frac{P(B\wedge A)}{P(A)}=P(B|A)\cdot P(A)=P(B\wedge A)$$
Dal momento che $P(A\wedge B)=P(B\wedge A):$
$$P(B|A)=\frac{P(A|B)\cdot P(B)}{P(A)}$$
## TEOREMA DELLA PROBABILITÀ TOTALE
Sia $A$ un evento e siano $B_{1},B_{2}\dots,B_{n}$ eventi mutualmente esclusivi, tali che $P(B_{i})\neq 0$ per ogni $i$ ed inoltre $P(B_{1}\vee B_{2}\vee\dots\vee B_{n}=1)$, ovvero gli eventi sono esaustivi.
Allora:
$$P(A)=P(A|B_{1})P(B_{1})+P(A|B_{2})P(B_{2})+\dots+P(A|B_{n})P(B_{n})=\sum^{n}_{i=1}P(A|B_{i})P(B_{i})$$
###### DIMOSTRAZIONE 
- Gli eventi $B_{1},B_{2},\dots ,B_{n}$ sono esaustivi, quindi almeno uno di loro si deve verificare.
- Quindi se $A$ si verifica, ci sarà un evento $B_{j}$ tale che $B_{j}$ si verifica, dal momento che gli eventi $B_{i }$ sono mutualmente esclusivi abbiamo: $P(A)=P(A\wedge B_{1})+\dots+P(A\wedge B_{n})$
- Dalla definizione di probabilità condizionata abbiamo che $$\forall i \ \ P(A\wedge B_{i})=P(A|B_{i})\cdot P(B_{i})$$$$\triangle$$
---

Supponiamo di dividere un mazzo di 52 carte in due mazzi: $M_{1}$ con 30 carte e $M_{2}$ con le rimanenti 22 carte.
Supponiamo che in $M_{1}$ ci sono 3 assi, e in $M_{2}$ ce n'è solo 1.
Scegliamo un mazzo a caso e da quel mazzo scegliamo una carta a caso.
- Qual'è la probabilità di pescare un asso $P(A)$?
Chiaramente, scegliendo $M_{1}$ abbiamo $P(A|M_{1})=\frac{3}{30}=\frac{1}{10}$
Se scegliamo $M_{2}$ abbiamo $P(A|M_{2})=\frac{1}{22}$.
$P(A)=P(A|M_{1})\cdot P(M_{1})+P(A|M_{2})\cdot P(M_{2})=\frac{1}{10}\cdot \frac{1}{2}+\frac{1}{22}\cdot \frac{1}{2}$
$\frac{1}{20}+\frac{1}{44}=\frac{11+5}{220}=\frac{16}{220}=\frac{8}{110}=\frac{4}{55}$

## PROBLEMI D'URNA
I problemi d'urna sono eventi che possono essere formalizzati come "Estraiamo una o più palline numerate da una o più urne".
Supponiamo di estrarre $k$ palline da un'urna contenente $n$ palline.
nei 4 casi possibili, il numero totale è:
- $D^{r}_{{n,k}}=n^{k}$ ovvero numero delle disposizioni con ripetizione se l'ordine è importante e la pallina viene reinserita dopo ogni estrazione.
- $D_{n,k}=n\cdot (n-1)\cdot \ \dots \ \cdot (n-k+1)$ ovvero numero delle disposizioni semplici, se l'ordine è importante ma la pallina non viene reinserita.
- $C_{n,k}=\binom{n}{k}=\frac{n!}{k!(n-k)!}$ ovvero combinazioni semplici, se l'ordine non è importante e la pallina estratta non viene reinserita.
- $C^{r}_{n,k}=\frac{(n+k-1)!}{k!(n-1)!}$ ovvero numero combinazioni con ripetizione se l'ordine non è importante e la pallina viene reinserita.
# TEORIA DEI GRAFI 
###### DEFINIZIONE GRAFO NON ORIENTATO
Un grafo semplice non orientato, denotato con $G=(V,E)$ consiste di:
- un insieme finito, non vuoto $V={1,2,\dots,m}$ i cui elementi sono chiamati vertici o nodi del grafo
- Un insieme finito $E=\{e_{1},e_{2},\dots,e_{n}\}$, i cui elementi sono sottoinsiemi di $V$ di cardinalità 2, ovvero $e_{k}=\{i,j\}$ con $i,j\in V$, anche detti archi del grafo.
- I due nodi che caratterizzano l'arco sono detti "estremi dell'arco" e si dicono adiacenti.
- Un arco che ha come estremo il nodo $i$ si dice "incidente" ad $i$
- Un vertice che non è l'estremo di alcun arco si dice "isolato".
###### DEFINIZIONE GRAFO ORIENTATO
Un grafo semplice orientato, denotato con $G=(V,E)$ consiste di
- Un insieme finito, non vuoto $V=\{1,2,\dots,m\}$ i  cui elementi sono chiamati nodi del grafo
- Un insieme finito $E=\{e_{1},e_{2},\dots,e_{n}\}$ i cui elementi sono coppie ordinate di elementi di $V$ ovvero $e_{k}=(i,j)$ con $i,j\in V$
- I due nodi toccati da $(i,j)$ sono detti estremi dell'arco e vengono definiti adiacenti.
- Un arco che ha come estremo il nodo $i$, indipendentemente dal verso dell'arco, si dice "incidente" ad $i$.
![[Schermata del 2026-07-13 12-04-54.png]]

### MULTIGRAFI
I grafi orientati e non, che hanno più di arco che collega coppie di nodi sono detti ==multigrafi==.

#### GRADO DI UN NODO
Dato un grafo $G=(V,E)$ il grado di un nodo $v\in V$, denotato con $\delta(v)$ è il numero di archi ad esso incidenti, ossia il numero di vertici ad esso adiacenti $$\delta(v)=|\{e\in E:v\in e\}|$$
Se $G=(V,E)$ è un digrafo definiamo due nozioni diverse di grado di un nodo:$
- grado di ingresso:        $\delta^{-}(v)=|\{e\in E: e=(w,v), \ w \in V\}|$
- grado di uscita:            $\delta^{+}(v)=|\{e\in E: e=(v,w), \ w\in V\}|$
#### HAND-SHAKING THEOREM
Sia $G=(V,E)$ un grafo non orientato, allora la somma dei gradi di ogni vertice è uguale al doppio del numero degli archi: $2|E|$
###### COROLLARIO
Sia $G=(V,E)$ un grafo non orientato, il numero dei vertici di grado dispari è un numero pari.
### GRAFI REGOLARI
- Sia $G=(V,E)$ un grafo non orientato
- Se i vertici del grafo hanno tutti lo stesso grado $r$ allora diciamo che $G$ è regolare di grado $r$
$$|V|=\frac{2|E|}{r}$$
- se $r$ è dispari allora $|V|$ è pari, ovvero un grafo regolare di grado dispari contiene un numero pari di vertici.
### GRAFI COMPLETI
- Sia $G=(V,E)$ un grafo non orientato.
- Diciamo che $G$ è completo se ogni coppia di vertici è connessa da un arco.
- Ne deduciamo allora che se $|V|=n$ il numero di archi del grafo completo è $\binom {n}{2}$ ovvero il numero di tutte le possibili coppie di vertici.
- Un grafo completo con $n$ vertici viene denotato con $K_{n}$
- Inoltre, $\forall n, \ K_{n}$ è un grafo regolare di grado $n-1$
---
### TORNEO
- Sia $G=(V,E)$ un grafo completo, il grafo orientato ottenuto assegnando uno dei due possibili versi ad ogni arco di $G$, si dice Torneo
- L'arco tra ogni coppia è orientato che se fosse vincitore - perdente.
### GRAFI ORIENTATI COMPLETI
La definizione di grafo completo si estende anche ai grafi orientati
- Sia $G=(V,E)$ un grafo orientato, diciamo che $G$ è completo se ogni coppia di vertici è connessa da un arco, ovvero $\forall (i,j)\in E$  e  $(j,i)\in E$
- Ne deduciamo allora che se $|V|=n$ il numero di archi del digrafo completo è $n(n-1)$ ovvero il numero di tutte le possibili coppie ordinate di vertici
### GRAFI BIPARTITI
Sia $G=(V,E)$ un grafo non orientato.
Diciamo che $G$ è bipartito se possiamo partizionare l'insieme dei vertici in 2 insiemi, $V_{1}$ e $V_{2}$ in maniera tale che tutti gli archi di $G$ hanno come estremi un vertice in $V_{1}$ e l'altro vertice $V_{2}$
![[Grafo_bipartito.jpg]]
### GRAFI BIPARTITI COMPLETI
Un grafo bipartito $G=(V,E)$ si dice completo se data la partizione dei vertici $V_{1},V_{2}$ esiste un arco per ogni coppia di vertici $v\in V_{1}$ e $u\in V_{2}$
Un grafo bipartito completo si indica con $K_{n,m}$ dove $n=|V_{1}|$ e $m=|V_{2}|$
![[Schermata del 2026-07-13 13-28-50.png]]
### SOTTOGRAFO
Sia $G=(V,E)$ un grafo non orientato.
Diciamo che $G'=(V',E')$ è un sottografo di $G$ se:
- $V'\subseteq V$
- $E'\subseteq E$ ed inoltre per ogni arco $(u,v)\in E'$ i suoi estremi $u,v$ appartengono entrambi a $V'$
![[Schermata del 2026-07-13 13-32-54.png|399]]
---
Sia $G=(V,E)$ un digrafo.
Diciamo che $G'=(V',E')$ è un sottografo di $G$, anch'esso orientato:
- $V' \subseteq V$
- $E' \subseteq E$ ed inoltre per ogni arco $u,v\in E'$ i suoi estremi $u,v$ appartengono entrambi a $V'$.
### SOTTOGRAFO INDOTTO
Dalla definizione data di sottografo, sia per i grafi orientati che per quelli non orientati, si evince la seguente definizionee di sottografo indotto
- Sia $G=(V,E)$ un grafo (digrafo).
- Sia $V' \subseteq V$.
il sottografo indotto da $V'$ e il sottografo $G=(V',E')$ ottenuto eliminando da $G$ tutti i vertici non appartenenti a $V'$ e tutti gli archi incidenti ad almeno uno dei vertici eliminati.
### ISOMORFISMO TRA GRAFI 
Due grafi, sia entrambi orientati che entrambi non orientati, $G_{1}=(V_{1},E_{1})$ e $G_{2}=(V_{2},E_{2})$ si dicono isomorfi se esiste una applicazione biunivoca $f$ nell'insieme dei vertici $V_{2}$ tale che $(f(u), f(v))$ è un arco di $E_{2} \iff (u,v)$ è un arco di $E_{1}$.
La biiezione $f$ è detta isomorfismo.

---
Consideriamo i due grafi $G_{1}=(V_{1},E_{1})$ e $G_{2}=(V_{2},E_{2})$ così definiti:
- $V_{1}=\{a,b,c,d\}$
- $E_{1}=\{(a,b),(a,d),(b,c),(c,d)\}$
- $V_{2}=\{t,u,v,w\}$
- $E_{2}=\{(t,u),(t,v),(u,v),(u,w),(v,w)\}$
La funzione $f:V_{1}\to V_{2}$ tale che 
$f(a)=t$ | $f(b)=v$ | $(c)=w$ | $f(d)=u$
è un isomorfismo.
![[Schermata del 2026-07-13 17-45-58.png]]
### OMEOMORFISMI
Sia $G=(V,E)$ un grafo non orientato e sia $e=(u,v)$ un arco di $G$.
Una suddivisione dell'arco $e=(u,v)$ è ottenuta introducendo un nuovo vertice $w$ e sostituendo in $G$ l'arco $(u,v)$ con gli archi $e_{1}=(u,w)$ e $e_{2}=(w,v)$

![[Schermata del 2026-07-13 17-49-31.png]]
---
Sia $G=(V,E)$ un grafo orientato e sia $e=(u,v)$ un arco di $G$.
una suddivisione dell'arco orientato $e=(u,v)$ è ottenuta introducendo un nuovo vertice $w$ e sostituendo in $G$ l'arco orientato $(u,v)$ con gli archi orientati $e_{1}=(u,w)$ e $e_{2}=(w,v)$
![[Schermata del 2026-07-13 17-52-13.png]]

---
Due grafi non orientati, $G_{1}=(V_{1}, E_{1})$ e $G_{2}=(V_{2}, E_{2})$ si dicono omeomorfi se attraverso una serie di suddivisioni di archi di $G_{1}$ e $G_{2}$ si possono ottenere due grafi $G'_{1}$ e $G'_{2}$ che sono isomorfi.
![[Schermata del 2026-07-13 17-54-49.png]]

---
Due grafi orientati $G_{1}=(V_{1},E_{1})$ e $G_{2}=(V_{2},E_{2})$ si dicono omeomorfi se attraverso una serie di suddivisioni di archi orientati di $G_{1}$ e $G_{2}$ si sono possono ottenere due grafi $G'_{1}$ e $G'_{2}$ che sono isomorfi.

### PERCORSO
Un percorso (diretto) in un grafo (digrafo) $G=(V,E)$ è una sequenza di nodi $v_{1},\dots,v_{k}$ adiacenti, ossia tali che $\forall i:1\leq i\lt k(v_{i},v_{i+1})$  è un arco del grafo
- il nodo $v_{1}$ è detto nodo origine del percorso ed il nodo $v_{k}$ è detto nodo destinazione.
- i nodi $v_{i}$ con $1\lt i\lt k$ sono detti nodi intermedi del percorso.
- Possiamo definire un percorso anche tramite un sequenza di archi $e_{1},e_{2},\dots,e_{k-1}$ dove 
	per ogni $1\leq j\lt k-1$ gli archi $e_{j}$ e $e_{j+1}$ hanno un vertice in comune
> una qualsiasi sequenza di vertici

### CAMMINO 
Un percorso diretto in un grafo $G$ viene detto cammino se tutti i nodi sono diversi
![[Schermata del 2026-07-13 18-18-20.png]]
### CIRCUITO
Un circuito diretto in un grafo è un percorso chiuso dove $v_{1}=v_{k}$ ed ogni vertice è ripetibile ma non gli archi.
![[Schermata del 2026-07-13 18-20-06.png]]

### CICLO
Un ciclo in un grafo $G$ è un cammino chiuso tale che $v_{1}=v_{k}$ dove tutti i vertici sono diversi.
- Se il grafo è orientato il minimo per formare un ciclo è 2
- Se il grafo non è orientato il minimo è 3
![[Schermata del 2026-07-13 18-23-11.png]]
### GRAFI ACICLICI
un grafo (digrafo) $G=(V,E)$ si dice aciclico se non possiede cicli.
![[Schermata del 2026-07-13 19-49-52.png|435]]
#### VERTICI CONNESSI 
Dato un grafo $G=(V,E)$, diciamo che due vertici $u,v$ sono connessi se esiste un cammino da $u$ a $v$

---
Sia $G=(V,E)$ un grafo e sia $V=V_{1}\cup V_{2}\cup\dots \cup V_{k}$ la partizione indotta dalla relazione di connessione tra i vertici.
Sia $G=(V_{i}, E_{i})$ il sottografo indotto da $V_{i}$ per ogni $i=1,\dots,k$.
Tali sottografi si ==chiamano componenti connesse== di $G$.
![[Schermata del 2026-07-14 11-26-11.png|625]]

---
### GRAFO CONNESSO
Un grafo si dice connesso se ha solo una componente connessa, cioè se dati due vertici qualunque in $V$, i due vertici sono connessi.

---
##### DIGRAFO DEBOLMENTE CONNESSO
Un digrafo $G=(V,E)$ si dice debolmente connesso, se il grafo non orientato ottenuto eliminando da $G$ l'orientamento degli archi è connesso.

---
##### DIGRAFO FORTEMENTE CONNESSO 
Dato un grafo orientato $G=(V,E)$ diciamo che due vertici $u,v$ sono fortemente connessi se esiste un cammino da $u$ a $v$ che un cammino da $v$ a $u$.
### GRAFI K-CONNESSI
Sia dato $G=(V,E)$
il grafo $G$ si dice k-connesso rispetto agli archi se dati due vertici $u,v\in V$ esistono $k$ cammini ad archi disgiunti tra $u,v$
il grafo $G$ si dice k-connesso rispetto ai vertici se dati due vertici $u,v\in V$ esistono $k$ cammini a nodi disgiunti tra $u,v$
## RAPPRESENTAZIONE
#### MATRICE DI ADIACENZA
Sia dato un grafo $G=(V,E)$ con $|V|=n$.
Supponiamo $V=\{1,2,\dots,n\}$.
Costruiamo una matrice $n \times n$:
- $M[i,j]=1$ se $i,j$ sono connessi da un arco
- $M[i,j]=0$ se $i,j$ non sono connessi da un arco 
![[Schermata del 2026-07-14 18-38-17.png]]
#### LISTE DI ADIACENZA 
Dato un grafo $G=(V,E)$ con $|V|=n$ associamo al grafo una lista di array di dimensione $n$ 
> grafo non orientato = $n+2|E|$ valori
> grafo orientato = $2|E|$ valori 

![[Schermata del 2026-07-14 19-40-37.png]]
### CIRCUITO EULERIANO 
Sia $G=(V,E)$ un grafo connesso.
Un circuito euleriano di $G$ è un circuito che passa per ogni arco di $G$ esattamente una ed una sola volta.
Un grafo si dice euleriano, se possiede un circuito euleriano.
![[Schermata del 2026-07-14 19-58-22.png]]
---
Un grafo $G$ è euleriano se e solo se è connesso ed i suoi vertici hanno tutti grado pari.

---
