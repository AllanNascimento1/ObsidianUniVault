Esercizio 1.6
Calcolare per ogni insieme X $X^{\varnothing}=?$ e $\varnothing ^{X}=?$, utilizzare la nozione di funzione.
- $X^{\varnothing}=\{\varnothing\}$ dato che 
$$\varnothing\times X=\varnothing\implies 2^{\varnothing}\implies 2^{\varnothing}=\{\varnothing,\varnothing\}=\{\varnothing\}\implies$$
$$\{f\in\{\varnothing\}|\forall x\in\varnothing,\exists!y\in X\ t.c\ (x,y)\in f\}$$
	Non esiste nessun x che appartenga ad $\varnothing$ di conseguenza le condizioni successive non verranno mai controllate e quindi non hanno un opportunità di essere false.
- Es $X\ne \varnothing$ allora $\varnothing^X=\varnothing$ dato che, come prima, $X\times \varnothing=\varnothing\implies 2^{\varnothing}\implies 2^{\varnothing}=\{\varnothing,\varnothing\}=\{\varnothing\}$ però in questo caso le condizioni cambiano :
$$\{f\in\{\varnothing\}|\forall x\in X,\exists!y\in \varnothing\ t.c\ (x,y)\in f\}$$
	Adesso possiamo scorre gli elementi di X però non esiste nessun y che soddisfa la seconda condizione. Allora $f$ non appartiene ad $\{\varnothing\}$.
	Se $X=\varnothing$ allora cade nel primo caso $\varnothing^{\varnothing}=\{\varnothing\}$

Esercizio 1.10
Siano X,Y,Z tre insiemi e siano $f:X\rightarrow Y$ e $g:Y\rightarrow Z$ due funzioni. Si dimostri le seguenti X affermazioni :
(1) f e g iniettiva $\implies$ $g\circ f$ iniettiva
(2) f e g suriettiva $\implies$ $g\circ f$ suriettiva
	Suppongo $f$ e $g$ sur. e sia $z\in Z$ vale:
	g sur. $\implies$ $\forall z\in Z,\ \exists y\in Y$ tale che $g(y)=z$
	f sur. $\implies$ $\forall y\in Y,\ \exists x\in X$ tale che $f(x)=y$
	$\implies (g\circ f)(x)=g(f(x))=z,\ \forall z\in Z$ 
(3) $f e g bigettiva $\implies$ $g\circ f$ bigettiva

Esercizi 1.11 e 1.12, scovare gli errori correggerli e risolvere
## Esercizi tipo esame
$\Bbb N=\{0,1,2,3,\dots\},\le$ 
Teorema 1 (Principio di induzione "shiftato")
Sia $n\in\Bbb N$ e sia $\{P(n)\}_{n\ge h}$ una famiglia di affermazioni indicizzata su $n\ge h$ supponiamo che valgono :
Ipotesi del teorema
- (Base induttiva) P(h) è vera
- (Passo induttivo) Per ogni $n\ge h$, 
	se $P(n)$ è vera (ipotesi induttiva)
	allora $P(n+1)$ è vera, (passo induttivo)
	ossia $\forall n\ge h, P(n)\implies P(n+1)$ 
Tesi del teorema
- Allora P(n) è vera $\forall n\ge h$ 
	Cioè se riesci a provare che P(n+1) è vera, allora P(n) è sicuramente vera

**Esercizio 1**
Si dimostri per induzione su $n\in\Bbb N$ la seguente uguaglianza :
$$\sum_{k=1}^n\frac{k}{2^k}=2-\frac{n+2}{2^n}\ \forall n\ge 1$$
Soluzione (in forma estesa) : Sia $h:=1$ e, per ogni $n\ge h=1$, consideriamo l'affermazione seguente :
$P(n):=\sum_{k=1}^n\frac{k}{2^k}=2-\frac{n+2}{2^n}$ 

**Base induttiva** :
Dobbiamo verificare la condizione iniziale, cioè in 1.
$P(1)=(\frac{1}{2}=2-\frac{3}{2})\iff(\frac{1}{2}=\frac{1}{2})$  vera, allora la base induttiva è verificata

**Passo induttivo (Completo)** :
(Ipotesi induttiva) Assumiamo che P(n) sia vera per qualunque $n\ge h=1$ ovvero $$P(n)=\left(\sum_{k=1}^n\frac{k}{2^k}=2-\frac{n+2}{2^n}\right)\ \ è\ vera$$ (Passo induttivo) Dobbiamo provare che : $$P(n+1)=\left(\sum_{k=1}^{n+1}\frac{k}{2^k}=2-\frac{(n+1)+2}{2^{n+1}}\right)\ \ è\ vera$$
1° Modo per eseguire il passo induttivo
	$$\sum_{k=1}^{n+1}\frac{k}{2^k}=(\sum_{k=1}^n\frac{k}{2^k})^{ip.\ ind.}+\frac{n+1}{2^{n+1}}=(2-\frac{n+2}{2^n})^{ip.\ ind.}+\frac{n+1}{2^{n+1}}=2-(\frac{n+2}{2^n}-\frac{n+1}{2^{n+1}})$$$$=2-(\frac{2(n+2)-(n+1)}{2^{n+1}})=2-(\frac{n+3}{2^{n+1}})=2-\frac{(n+1)+2}{2^{n+1}}$$
	La proposizione del teorema (passo di induzione) è verificata ovvero il passo induttivo è stato fatto. Dunque, grazie al principio di induzione P(n) è vera $\forall n\ge h=1$.
2° Modo per eseguire il passo induttivo$$P(n+1)=\left(\sum_{k=1}^{n+1}\frac{k}{2^k}=2-\frac{(n+1)+2}{2^{n+1}}\right)=\left((\sum_{k=1}^n\frac{k}{2^k})^{ip.\ ind.}+\frac{n+1}{2^{n+1}}=2-\frac{(n+1)+2}{2^{n+1}}\right)$$$$=\left((2-\frac{n+2}{2^n})^{ip.\ ind.}+\frac{n+1}{2^{n+1}}=2-\frac{n+3}{2^{n+1}}\right)=\left(\frac{-2n-4+n+1}{2^{n+1}}=\frac{-n-3}{2^{n+1}}\right)$$$$=\left(\frac{-n-3}{2^{n+1}}=\frac{-n-3}{2^{n+1}}\right)$$
	L'ultima uguaglianza è evidentemente soddisfatta quindi anche la prima è vera, cioè P(n+1) è vera. Dunque il passo induttivo è stato fatto si può quindi applicare il Teorema di induzione.
**Soluzione compatta**
	Si dimostri per induzione su $n\in\Bbb N$ ciò che segue : 
	$$\sum_{k=1}^n\frac{k}{2^k}=2-\frac{n+2}{2^n}\ \forall n\ge 1$$
	Vale :
	$\frac{1}{2^1}=\frac12$ 
	$2-\frac{1+2}{2^1}=2-\frac32=\frac{4-3}{2}=\frac12$ 
	Dato che $$\sum_{k=1}^1\frac{k}{2^k}=\frac12=2-\frac{1+2}{2^1}$$allora la **base del induzione** è verificata.
	Paso induttivo : $(n\ge 1,n)^{ipo.\ ind.}(\implies n+1)^{pas.\ ind.}$ 
	Assumiamo che $\forall n\ge 1$ $$\sum_{k=1}^n\frac{k}{2^k}=2-\frac{n+2}{2^n}\ \ sia\ vera$$Dobbiamo dimostrare che $$\sum_{k=1}^{n+1}\frac{k}{2^k}=2-\frac{(n+1)+2}{2^{n+1}}$$Da qua puoi dimostrarlo con il primo o secondo metodo.

**Esercizio 2**
$$\sum_{k=1}^n6k^2=n(n+1)(2n+1)\ \ \ \forall n\ge 2$$
(Base Induttiva) $$\sum_{k=1}^26k^2=(6+(6*4)=2(2+1)(4+1))=(24+6=2*3*5)=(30=30)$$Dunque la base del induzione è verificata
(Ipotesi Induttiva) $n\ge 2, n$ (Paso Induttivo) $\implies n+1$ 
	Dobbiamo dimostrare che:$$\sum_{k=1}^{n+1}6k^2=(n+1)((n+1)+1)(2(n+1)+1)$$
- Usiamo il primo modo :$$\sum_{k=1}^{n+1}6k^2=(\sum_{k=1}^{n}6k^2)^{ipo.\ ind.}+6(n+1)^2=[n(n+1)(2n+1)]^{ipo.\ ind.}+6(n+1)^2$$$$=(n+1)[n(2n+1)+6(n+1)]=(n+1)[2n^2+n+6n+6]=(n+1)(2n^2+7n+6)$$
	Invece di calcolare la radice del polinomio verifico che vale : 
		$2n^2+7n+6=((n+1)+1)(2(n+1)+1)$
		$\iff2n^2+7n+6=(n+2)(2n+2+1)\iff2n^2+7n+6=(n+2)(2n+3)$
		$\iff2n^2+7n+6=2n^2+3n+4n+6\iff2n^2+7n+6=2n^2+7n+6$   
	Allora vale che $(n+1)(2n^2+7n+6)=(n+1)((n+1)+1)(2(n+1)+1)$ e quindi il passo induttivo è verificato e per il teorema di induzione P(n) è vera $\forall n\ge 2$.
- Con il secondo modo :$$(\sum_{k=1}^{n}6k^2)^{ipo.\ ind.}+6(n+1)^2=(n+1)(n+2)(2n+2+1)$$
	$\iff(n(n+1)(2n+1))^{ipo.\ ind.}+6(n+1)^2=(n+1)(n+2)(2n+3)$$\iff(n+1)(n(2n+1)+6(n+1))=(n+1)(2n^2+3n+4n+6)$$\iff(n+1)(2n^2+n+6n+6)=(n+1)(2n^2+7n+6)$$\iff(n+1)(2n^2+7n+6)=(n+1)(2n^2+7n+6)$
	Il passo induttivo è verificato, allora per il teorema di induzione P(n) è vera $\forall n\ge 2$.