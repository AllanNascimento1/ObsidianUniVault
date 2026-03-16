### Costruzione dei numeri naturali (Assioma di Peano)
**Assioma 2.5** : $0\in\Bbb N$ (esiste un elemento 0, zero)
**Assioma 2.6** : $\exists succ:\Bbb N\rightarrow\Bbb N$ funzione iniettiva (funzione successivo)
**Assioma 2.7** : $succ(\Bbb N)\subset\Bbb N/\{0\}$ ovvero $succ(n)\neq 0\ \ \forall n\in\Bbb N$ 
**Assioma 2.8 (di induzione)** : Sia A un sottoinsieme di $\Bbb N$ supponiamo che A abbia le seguenti proprietà : 
	(1) Base del induzione $0\in A$
	(2) Passo induttivo $\forall n\in N,(n\in A(ipotesi\ induttiva)\implies(passo\ induttivo)\ succ(n)\in A)$ ovvero se un qualche elemento $n\in \Bbb N$ appartiene ad A allora anche $succ(n)$ appartiene ad A.
Questi assiomi descrivono univocamente $\Bbb N$
**NB**: Chiede negli esercizi (assumo sia la verifica) la base del induzione, ipotesi induttiva e passo induttivo
**Proposizione 2.9** : Sia $n\in\Bbb N/\{0\}$ allora $\exists!m\in M$ tale che $succ(m)=n$ ovvero ogni $n\in N/\{0\}$ ammette un unico **predecessore** $m\in\Bbb N\iff succ(\Bbb N)=\Bbb N/\{0\}$ (cioè l'immagine di $succ$ è $\Bbb N/\{0\}$).
Dimostrazione : Se esiste m allora è unico in quanto $succ$ è iniettivo.
	Supponiamo che esista $m\in\Bbb N/\{0\}$ che non ammetta predecessore, definiamo $A:=N/\{m\}\subset\Bbb N$ però osserviamo che $0\in A$ in quanto per ipotesi $m\neq 0$. Sia $n\in A$ consideriamo $succ(n)\neq m\iff succ(n)\in A$ però per l'assioma 2.8 $\implies A=\Bbb N\implies$ m non esiste. 

Corollario 2.9' : La funzione $(\Bbb N,\Bbb N/\{0\},n\mapsto succ(n))$ denotata $succ':\Bbb N\rightarrow\Bbb N/\{0\}$,$succ'(n):=succ(n)\forall n\in\Bbb N$, è una bigezione. In particolare, $\Bbb N$ e $\Bbb N/\{0\}$ sono equipotenti $\iff|\Bbb N|=|\Bbb N/\{0\}|$
## Principio di induzione di prima forma
### Teorema 2.10
Sia $\{P(n)\}_{n\in\Bbb N}$ una famiglia di affermazioni indicizzata su $n\in\Bbb N$ supponiamo che 
	(1) (Base dell'induzione) $P(0)$ è vera.
	(2) (Passo induttivo) $\forall n\in\Bbb N$, $P(n)\implies P(succ(n))$ ovvero se $P(n)$ è vera allora dobbiamo provare che $P(succ(n))$ è vera
![[Pasted image 20260305092330.png]]
**Dimostrazione** : 
	Sia $A:=\{n\in\Bbb N|P(n)\ è\ vera\}$ è vero che $0\in A$ e anche che $succ(n)\in A$ allora $n\in A\iff P(n)\ è\ vera\implies P(succ(n))\ è\ vera\iff succ(n)\in A$ 
### Teorema di Ricorsione (2.11)
Sia X un insieme non vuoto, $h:\Bbb N\times X\rightarrow X$ una funzione (di ricorsione) e $c\in X$ (dato iniziale). Allora esiste un unica $f:\Bbb N\rightarrow X$ funzione tale che:
	(1) $f(0)=c$
	(2) $\forall n\in\Bbb N,f(succ(n))=h(n,f(n))$ 
Non chiede la dimostrazione.
### Struttura algebrica su $\Bbb N$, addizione e moltiplicazione
Sia $m\in\Bbb N$, vogliamo definire formalmente il concetto di "somma a sinistra con m" attraverso la funzione $f:\Bbb N\rightarrow\Bbb N,n\mapsto m+n$ , vogliamo usare il teorema di ricorsione allora poniamo $X:=\Bbb N$, $h:\Bbb N\times\Bbb N\rightarrow\Bbb N$, $(a,b)\mapsto?$ 
**Intuizione**
$$  
\begin{cases}  
f(0)=?\\  
\forall n\in\Bbb N,f(succ(n))=h(n,f(n))
\end{cases}
$$
$$  
\begin{cases}  
f(0)=m+0=m=c\\  
m+(n+1)=(m+n)+1=succ(m+n)
\end{cases}
$$
**Formalmente**
Sia $m,n\in\Bbb N$ e $h:\Bbb N\times\Bbb N\rightarrow\Bbb N$ definito ponendo $h(a,b):=succ(b),\forall(a,b)\in\Bbb N\times\Bbb N$ allora dal teorema ricorsivo $\exists!f:\Bbb N\rightarrow\Bbb N$ tale che :
$$  
\begin{cases}  
f(0)=m\\
\forall n\in\Bbb N,f(succ(n))=h(n,f(n))=succ(f(n))
\end{cases}
$$
	Esempio:
		m=3 , n=2 allora f(2)=h(1,f(1))=h(1,h(0,f(0)))=h(1,h(0,3))=h(1,4)=5
Esercizio:
	Definire via teorema di ricorsione la funzione "moltiplicazione a sinistra con m", $X=\Bbb N$, cioè determinare:
	"$m*0=0$", c=0
	"$m*(succ(n))=h(n,m*n)$"
$$  
\begin{cases}  
f(0)=m*0=0\\  
f(n+1)=m*(n+1)=m*n+m=f(n)+m
\end{cases}
$$
	Allora $h(a,b)=b+m,\forall (a,b)\in\Bbb N\times\Bbb N$ 
$$  
\begin{cases}  
f(0)=0\\  
\forall n\in\Bbb N,f(succ(n))=h(n,f(n))=f(n)+m
\end{cases}
$$
	Esempio:
		m=3 , n=2 allora f(2)=h(1,f(1))=h(1,h(0,f(0)))=h(1,h(0,0))=h(1,3)=6
### Ordinamento parziale e totale di $\Bbb N$
**Parziale**
Definizione 3.6 : Sia X un insieme non vuoto e $R$ una relazione binaria su X (cioè $R\subset X\times X$) diremo che $R$ è un ordinamento parziale di X se valgono le seguenti proprietà:
	(1) $\forall x\in X$ vale che $xRx$ (riflessiva)
		Cioè se vale che la coppia $(x,x)\in R$ 
	(2) $\forall x,y\in X, (xRy)$ e $(yRx)\iff x=y$ (antisimmetrica)
		Se la coppia $(x,y)\in R$ e $x\ne y$ allora la coppia $(y,x)$ non deve appartenere ad $R$.
	(3) $\forall x,y,z\in X,(xRy)$ e $(yRz)\implies xRz$ (transitivo)
		Se $(x,y)\in R$ e $(y,z)\in R$ allora anche $(x,z)$ deve appartenere ad $R$.
**Totale**
Un ordinamento parziale diventa un ordinamento totale se inoltre vale anche la seguente proposizione :
	(4) $\forall x,y\in X,(xRy)$ o $(yRx)$ (tricotomia)
Una coppia $(X,R)$ in cui $R$ è un ordinamento (parziale o totale) si dice un **Insieme Parzialmente/Totalmente Ordinato**.
#### Definizione 3.9 Minore Uguale
Siano $n,m\in\Bbb N$ definiamo il simbolo $\le$ come una relazione binaria su $\Bbb R$ ponendo $n\le m$ se $\exists k\in\Bbb N$ tale che $m=n+k$.
Teorema 3.5 : $(\Bbb N,\le)$ è un insieme totalmente ordinato.
### Insiemi Finiti
Definizione : $n\in\Bbb N/\{0\}$, definiamo $I_n:=\{0,1,2,...,n-1\}$. Ed anche $I_0:=\{\varnothing\}$
Definizione 3.10 : Un insieme X si dice **FINITO** se $\exists n\in\Bbb N$ t.c $X\sim I_n$ (X è un in bigezione con $I_n$). 
Se X non è finito, allora si dice **INFINITO**.
#### Teorema 3.11 (Lemma dei cassetti)
Siano X e Y due insiemi (eventualmente vuoti) e siano $n,m\in\Bbb N$ t.c $n<m$, $X\sim I_n$ e $Y\sim I_m$. Allora non esiste alcuna iniezione (cioè funzione iniettiva) $f:Y\rightarrow X$ 

**Dimostrazione** :
Procediamo per induzione su $n\in\Bbb N$, allora P(n):=("Teorema 3.11") $\forall n\in\Bbb N$

(Base Induttiva) Provare che $P(0)$ non esiste.
Se n=0 $X\sim I_0:=\varnothing$, cioè $X=\varnothing$, dato $m\in\Bbb N$ t.c $m>0$ e dato un insieme $Y\sim I_m$, dobbiamo verificare che non esistono iniezioni $f:Y\rightarrow X=\varnothing$ ($Y\ne\varnothing$ $m\ge 1$). Però se esistesse una tale iniezione f apparterebbe a $\varnothing^Y=\varnothing\implies$ non esistono f $\implies$ non esistono iniezioni.

Se $(n\ge 0,n)^{ipo.\ ind.}(\implies n+1)^{pas.\ ind.}$ Assumiamo che l'asserto P(n) sia verificato per qualche $n\in\Bbb N$ allora dobbiamo provare che $P(n+1)$ è vera.
Sia $n,m\in\Bbb N$ t.c $m>n+1$ e sia X un insieme con $X\sim I_{n+1}$ e sia Y un insieme con $Y\sim I_m$ allora dobbiamo provare che non esiste nessuna iniezione $f:Y\rightarrow X$.
Supponiamo (per assurdo) che esista $f:Y\rightarrow X$ iniettiva allora, poiché $X\sim I_{n+1}$, $\exists g:I_{n+1}\rightarrow X$. Consideriamo $X':=X/\{x_n\}$ e la funzione $g*:I_n\rightarrow X$ è ancora (dove $h\in I_n$) $h\mapsto g(h)$ una biezione $\implies X'\sim I_n$.
Distinguiamo due casi:
	$x_n\notin f(Y)$.
	$x_n\in f(Y)$.
Nel primo caso se osserviamo la funzione $f*:Y\rightarrow X'$ iniettiva $\implies$ m>n+1>n$\implies$m>n$\implies$(per ipotese induttiva) $f*$ non esiste e allora anche $f$ non esiste.
Nel secondo caso dato che $x_n\in f(Y)$ e $f$ è iniettivo$\implies\exists!y\in Y$ t.c $\{Y\}=f^{-1}(x_n)$ definiamo $Y':=Y/\{y\}$ e la funzione $f*:Y'\rightarrow X'$ allora sappiamo che $X\sim I_n$, $Y'\sim I_{m-1}\implies$(per ipotesi induttiva) $f*$ non esiste.
Allora il passo induttivo è stato fatto e per il principio di induzione P(n) è vera $\forall n\in\Bbb N$.
#### Collorario 4.1 (riformulato)
Siano X e Y due insiemi e siano $n,m\in\Bbb N$ t.c $X\sim I_n$ e $Y\sim I_m$. Allora $X\sim Y\iff n=m$.
In particolare, se $n'\in\Bbb N$ t.c $X\sim I_{n'}$, allora $n=n'$.
**Dimostrazione** : 
$\iff$ Se n=m, allora $f:X\rightarrow I_n$ e $g:Y\rightarrow I_m$ dove $I_n=I_m$ e $g^{-1}\circ f:X\rightarrow Y$ allora $X\sim Y$
$\Rightarrow$ Supponiamo che $n\ne m$ a meno di scambiare n con m, possiamo supporre che $n<m:X\sim I_n,Y\sim I_m,n<m,\exists f:Y\rightarrow X$ iniettiva, però grazie al lemma dei cassetti non può esistere f $\implies n=m$
Segue che se X è finito, $\exists!n\in\Bbb N$ t.c insieme cardinato associato $X\sim I_n\implies|X|=I_n$ allora si dice che X ha cardinalità n e si scrive $|X|=n$

**Proposizione 4.4** : Sia X un insieme finito e sia Y un suo sottoinsieme. Allora Y è finito e $|Y|\le|X|$. Inoltre,s e $Y\subsetneq X$ allora $|Y|<|X|$
Dimostrazione : 
Procediamo con induzione. Sia $n:=|X|$ 
(Base del induzione) n=0 allora $|X|=0\iff X\sim I_0\implies X=\varnothing$, Sia $Y=\varnothing\subset X=\varnothing$ allora vale: 
$Y=\varnothing\sim I_0\implies|Y|=0\le|X|=0$ 

$n\ge0, n\implies n+1$ allora assumiamo vero $(|Y|\le|X|$ se $|X|=n)^{ipo.\ ind.}$, allora dimostro che vale l'asserto anche per $|X|=n+1$. 
Sia X un insieme con $|X|=n+1$ e sia Y un sottoinsieme allora definiamo $X':=X/\{x_n\}$ vale $|X'|=n$
Caso 1 : Se $x_n\notin Y$ cioè $Y\subset X'$ allora per ipotesi induttiva $|Y|\le|X'|=n<n+1=|X|$
Caso 2 : Se $x_n\in Y$ allora definiamo $Y':=Y/\{x_n\}\implies Y'\subset X'$ (ipotesi induttiva)$\implies Y'$ è finito e $|Y|<|X'|=n<n+1=|X|$ 

Collorario 4.5: Un insieme finito **non** può essere messo in biggezione con nessuno suo sottoinsieme proprio.
	Oss : $\Bbb N$ non può essere finito dato che la funzione $succ:\Bbb N\rightarrow\Bbb N/\{0\}$ è una biezione