### Passo 1: L'impostazione del prodotto

**Teoria generale:**

La potenza $(a+b)^n$ rappresenta la moltiplicazione del blocco $(a+b)$ per se stesso $n$ volte:

$$(a+b)^n=(a+b)\cdot(a+b)\cdot\dots\cdot(a+b)$$

**In parallelo ($n=3$):**

Allineiamo esattamente 3 parentesi:

$$(a+b)^3=(a+b)\cdot(a+b)\cdot(a+b)$$

### Passo 2: La regola di moltiplicazione

**Teoria generale:**

Per sviluppare questo prodotto con la proprietà distributiva, siamo obbligati a estrarre esattamente una lettera (scegliere $a$ oppure $b$) da ognuna delle $n$ parentesi, moltiplicando le scelte tra loro.

**In parallelo ($n=3$):**

Dobbiamo fare 3 estrazioni. Un percorso possibile è pescare $a$ dalla prima parentesi, $a$ dalla seconda e $b$ dalla terza.

### Passo 3: La struttura del monomio

**Teoria generale:**

Se decidiamo di estrarre la lettera $b$ per un numero $k$ di volte, siamo matematicamente forzati a estrarre la lettera $a$ dalle parentesi rimanenti, che sono esattamente $n-k$.

Il prodotto di queste lettere sarà sempre un monomio con questa forma fissa:

$$a^{n-k}b^k$$

**In parallelo ($n=3$):**

Fissiamo un numero di estrazioni per la $b$, ad esempio $k=1$.

Se peschiamo la $b$ da 1 parentesi, dalle rimanenti $3-1=2$ parentesi dobbiamo pescare la $a$.

Il monomio che andiamo a generare avrà quindi questa forma:

$$a^{3-1}b^1=a^2b$$

### Passo 4: Il calcolo combinatorio (Il nucleo della dimostrazione)

**Teoria generale:**

Quante volte si forma il monomio $a^{n-k}b^k$? Esattamente tante volte quanti sono i modi per scegliere da quali $k$ parentesi estrarre la $b$, scartando le altre. Questo calcolo corrisponde alle combinazioni semplici di $k$ elementi su $n$ totali, ovvero:

$$\binom{n}{k}$$

**In parallelo ($n=3$ e $k=1$):**

Quante volte si formerà il monomio $a^2b$? Dobbiamo contare in quanti modi possiamo scegliere 1 parentesi (quella della $b$) sulle 3 parentesi totali.

Applichiamo la formula:

$$\binom{3}{1}=\frac{3!}{1!(3-1)!}=\frac{3\cdot2!}{1\cdot2!}=3$$

Verifica logica delle 3 moltiplicazioni che generano $a^2b$:

1. $a\cdot a\cdot b=a^2b$ (scelgo $b$ dalla 3ª parentesi)
    
2. $a\cdot b\cdot a=a^2b$ (scelgo $b$ dalla 2ª parentesi)
    
3. $b\cdot a\cdot a=a^2b$ (scelgo $b$ dalla 1ª parentesi)
    
    Il coefficiente 3 è dimostrato.
    

### Passo 5: La sintesi del Teorema

**Teoria generale:**

Il polinomio finale è la somma di tutti i monomi possibili (da $k=0$ estrazioni di $b$, fino a $k=n$ estrazioni di $b$), ciascuno moltiplicato per il suo coefficiente binomiale $\binom{n}{k}$.

$$(a+b)^n=\sum_{k=0}^{n}\binom{n}{k}a^{n-k}b^k$$

**In parallelo ($n=3$):**

Calcoliamo tutti i casi possibili incrementando $k$ da 0 a 3:

- Se $k=0$: $\binom{3}{0}a^3b^0=1a^3$
    
- Se $k=1$: $\binom{3}{1}a^2b^1=3a^2b$
    
- Se $k=2$: $\binom{3}{2}a^1b^2=3ab^2$
    
- Se $k=3$: $\binom{3}{3}a^0b^3=1b^3$
    

Sommando questi termini, otteniamo esattamente lo sviluppo del cubo di un binomio:

$$(a+b)^3=a^3+3a^2b+3ab^2+b^3$$