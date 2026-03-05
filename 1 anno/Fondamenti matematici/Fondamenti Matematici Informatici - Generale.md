### Referenze
https://pignatelli.maths.unitn.it
- Dispensa
- Esami : Matematica discreta 2 (adesso chiamato FMI)
### Argomenti
- Aritmetica modulare e crittografia RSA
	- 11 Teoremi?
- Cenni di teoria dei grafi
# Cenni teoria degli insiemi
Per questo corso ci serve solo i concetti primitivi di **Elemento** e **Insieme** e la nozione di appartenenza, che può essere messa a fondamento della teoria degli insiemi.
#### Insiemi
Con questi concetti primitivi possiamo dare una definizione a cosa è un insieme, un insieme è una collezione di elementi cui ha la **Proprietà Fondamentale** di poter sempre stabilire senza ambiguità se qualche cosa è un suo elemento oppure no.

Consideriamo:
$A=\{x|x\notin x\}$
Supponiamo che A sia un insieme:
	Allora A sarebbe l'insieme di tutti gli elementi x tale che x non appartenga all'insieme x.
	Poiché A è un insieme devo poter stabilire se A visto come elemento appartiene ad A visto come insieme per capire se A è un insieme.
	Vale: $A\in A\implies A\notin A$  però è Falso.  se $A\notin A\implies A\in A$ anche questo è falso. Allora A non può essere un insieme.
### Simboli
- $\in$ e $\notin$ : 
Scriviamo $x\in A$ che significa che x è un elemento del insieme A, la negazione si scrive $x\notin A$ e significa che x non appartiene al insieme A.
Es: $A=\{1,2,3\}\iff 1\in A, 2\in A, 3\in A$ 
- $\iff$ : La doppia freccia $\iff$ vuol dire "se e solo se" oppure "equivalente".
- | : "|" vuol dire "tale che".
- $\implies$ :
Vuol dire implicazione, un altro modo di scrivere è A o (non B) supponendo $A\implies B$
Oss : Se A è sempre falso allora l'implicazione è sempre vera, esempio: se $P(x)$ è una qualsiasi proprietà allora vale sempre $\forall x\ \ x\in\varnothing\implies P(x)$.
- $\exists$ e $\exists !$ : Esiste e esiste un unico.
- $:=$ è definita come.

$O(A)=\{\varnothing,\{1\},\{2\},\{3\},\{1,2\},\{1,3\},\{2,3\},A\}\implies A\in O(A)$ 
$O(A)=2^A$ 
#### Assioma 1.1 Estensionalità
l'insieme A e B, sono $A=B \iff (\forall x:x\in A\iff x\in B)$.
##### Definizione 1.5: 
Siano X e Y due insiemi supponiamo $X\subset Y$ oppure $Y\supset X$ (dove $\subset$ vuol dire "contenuto") se $(\forall x\in X \implies x\in Y)$.
#### Assioma 1.6 Separazione
Sia X un insieme Supponiamo che ad ogni elemento x di X sia associato a una affermazione P(X) che può essere vero a falsa, Allora:
$\{x|x\in X, P(x)$ è vera$\}$ è un insieme.
Osservazione: L'insieme il cui elementi sono tutti gli insiemi non esiste. Se esistese varebbe la seguente ugualianza: $\{x|x\in x\}$ 
## Operazioni tra insiemi
Siano X e Y insiemi:
	$X\cup Y = \{x|x\in X\ o\ x\in Y\}$ Unione
	$X\cap Y=\{x|x\in X\ e\ x\in Y\}$ Intercessione
	$X$ \ $Y=\{x|x\in X\ e\ x\notin Y\}$ sottrazione, anche detto complementare di Y in X
	$X\times Y=\{(x,y)|x\in X,y\in Y\}$ prodotto, tutte le coppie ordinate degli elementi di X e Y.
		La virgola vuol dire "e"
		$\varnothing \times X=\varnothing=X\times \varnothing$
## Unioni e Intercessione arbitraria
Sia I un insieme non vuoto (detto l'insieme degli indici) per ogni $i\in I$, sia X un insieme. Siano $\{X_i\}_{i\in I}$ è una famiglia di insiemi parametrizzata da I.
## Relazioni e Funzioni
#### Definizione 1.9
Siano X e Y due insiemi. Un sottoinsieme R del prodotto cartesiano $X\times Y$ si dice relazione tra X e Y. Se $x\in X$, $y\in Y$ tale che $(x,y)\in R$, allora so scrive $xRy$ e si dice che x è in R relazione con y.
![[Pasted image 20260226085247.png]]
$(x,y)\in R\iff xRy$
#### Definizione 1.10
Siano X eY due insiemi e sia $f\subset X\times Y$ una relazione, tra X e Y, diciamo che $f$ è una **funzione da X in Y** (oppure applicazione, mappa) se $\forall x\in X,\exists !y\in Y : (x,y)\in f\ oppure\ xfy$  

Se f soddisfa quest'ultima condizione ovvero è una finzione di X in Y, allora verrà indicata con $f:X\rightarrow Y$.
Riassumendo : una funzione è il dato di $(X,Y,f)$ dove X è il dominio di $f$ e Y è il codominio di $f$.
### Funzione come legge
Siano X e Y insiemi non vuoti allora una funzione $f_{legge} : X\rightarrow Y$ è una legge (intesa come nozione primitiva) che ad ogni $x\in X$ associa un solo elemento $y\in Y$. 
Questa nozione esiste perché la definizione "associa" non è rigida come la nozione insiemistica, creando la differenza tra di loro, però le dimostrazioni sono molto più veloci e intuitive rispetto a quelle create dalla nozione insiemistica.
![[Pasted image 20260226091224.png]]
#### Equivalenza tra la nozione insiemistica e "come legge" di funzione
Siano X e Y due insiemi non vuoti e sia $f:X\rightarrow Y$ una funzione, cioè $f\subset X\times Y$ tale che $\forall x\in X,\ \exists !y\in Y$ | $(x,y)\in f$, allora puoi vedere questa funzione "come legge" se dal grafico insiemistico disegni i punti dentro x e li associ a y
Osservazione Personale : Per quello che ho capito la nozione insiemistica è quella con l'asse Y e X mentre la nozione come legge sono gli insiemi con le freccette tra elementi di x e di y. 

Supponiamo sia data una funzione come legge $f_{legge}:X\rightarrow Y$ possiamo verificare che sia uguale a una funzione insiemistica se per ogni x si disegni una retta parallela al asse Y che tocca solo un elemento y? Quello che otterrai alla fine è il $Grafico(f_{legge})$

**Da qui in avanti useremo il concetto di funzione come legge**
#### Definizione di insieme delle Parti 
Siano X e Y due insiemi (eventualmente vuoti) allora definiamo l'insieme $Y^X$ come l'insiemi i cui da $X\boh Y$.
**Osservazione**: Sia A un insieme allora indichiamo con simbolo $2^A$ oppure $O(A)$. l'insieme i cui elementi sono tutti i sottoinsiemi di A. $O(A)$ è detto insieme delle **Parti di A**.
Es : $A=\{1,2\}$ allora $2^A=\{\varnothing,\{1\},\{2\},A\}$ 

Vale: 
$$y^x=\{f\in 2^{X\times Y}|\forall x\in X,\exists !y\in Y\ t.c\ (x,y)\in f\}$$

#### Esercizio
Calcolare per ogni insieme X $X^{\varnothing}=?$ e $\varnothing ^{X}=?$, utilizzare la nozione di funzione.
- $X^{\varnothing}=1$ dato che 
$$\varnothing\times X=\varnothing\implies 2^{\varnothing}\implies 2^{\varnothing}=\{\varnothing,\varnothing\}=\{\varnothing\}\implies$$
$$\{f\in\{\varnothing\}|\forall x\in\varnothing,\exists!y\in X\ t.c\ (x,y)\in f\}$$
	Non esiste nessun x che appartenga ad $\varnothing$ di conseguenza le condizioni successive non verranno mai verificate e quindi non hanno un opportunità di essere false.
- $\varnothing^X$ = 0 dato che, come prima, $X\times \varnothing=\varnothing\implies 2^{\varnothing}\implies 2^{\varnothing}=\{\varnothing,\varnothing\}=\{\varnothing\}$ però in questo caso le condizioni cambiano :
$$\{f\in\{\varnothing\}|\forall x\in X,\exists!y\in \varnothing\ t.c\ (x,y)\in f\}$$
	Adesso possiamo scorre gli elementi di X però non esiste nessun y che soddisfa la seconda condizione. Allora $f$ non appartiene ad $\{\varnothing\}$. 

Esempio 1.12 : Sia X un insieme non vuoto. La funzione identità di X, indicata con $id_X : X\rightarrow X$, è determinata ponendo : $id_X(x)=x\ \forall x\in X$
#### Definizione 1.15 Composizione tra funzioni
Siano X, Y e Z tre insiemi non vuoti consideriamo $f:X\rightarrow Y$ e $g:Y\rightarrow Z$ allora definiamo la funzione $g\circ f:X\rightarrow Z$ ponendo $(g\circ f)(x):=g(f(x))\ \ \forall x\in X$, questa funzione è chiamata "f composto g" anche se viene scritta $g\circ f$.

La definizione insiemistica usa la nozione di "spazio" dove la funzione composta è vista come intercessione delle funzioni $f$ definita nel piano XY, e della funzione $g$ definita nel piano YZ. Questa definizione è molto più complessa di quella appena vista e non verrà trattata in questo corso.
#### Definizione Immagine e Controimmagine
Sia $f:X\rightarrow Y$ una funzione tra insiemi non vuoti e A un sottoinsieme di X, definiamo l'immagine di A tramite $f$ come segue : 
$$f(A):=\{\forall y\in Y|\exists a\in A, y=f(a)\}=\{f(a)\in Y|a\in A\}$$
Se $A=X$ allora $f(x)$ si dice anche immagine di $f$.

Dato B un sottoinsieme di Y, definiamo la controimmagine $f^{-1}(B)$ di B tramite $f$ ponendo $f^{-1}(B):=\{x\in X|f(x)\in B\}$
Se $B=\{b\}$, allora $f^{-1}(\{b\})=\{x\in X|f(x)=b\}$, si puo scrivere $f^{-1}(\{b\})=f^{-1}(b)$ e si chiama **Fibra di f sopra b**.
Il concetto di fibra è molto importante, per esempio quando ci chiedevano : 
Risolvere l'equazione $x^2=1$ è sotto inteso che $x\in \Bbb R\iff f:\Bbb R\rightarrow \Bbb R,f(x):=x^2\ \ \forall x\in \Bbb R$
$\{x\in \Bbb R|x^2=1\}=\{x\in \Bbb R|f(x)=1\}=f^{-1}(1)=1$ 
#### Definizione Iniettiva e Suriettiva 3/3/2026
Una funzione $f:X\rightarrow Y$ è
- Iniettiva se, per ogni $x,x'\in X$ con $x\neq x'$, allora $f(x)\neq f(x')$ ovvero le fibre di f sono o vuote o singoletti.
- Suriettiva se $f(x)=Y$ ovvero $\forall y\in Y, \exists x\in X\ t.c\ f(x)=y$ ovvero tutte le sue fibre sono non vuote.
- Bigettiva se è iniettiva e suriettiva.
#### Esempi
Sia $\Bbb R$ = "insieme dei numeri reali" e $\Bbb R^+=\{x\in\Bbb R |x\geq 0\}$ consideriamo :
$f_1=\Bbb R\rightarrow\Bbb R,f_1(x)=x^2$, questa funzione non è iniettiva o suriettiva.
$f_2=\Bbb R\rightarrow\Bbb R^+,f_2(x)=x^2$, questa funzione non è iniettiva ma è suriettiva.
$f_3=\Bbb R^+\rightarrow\Bbb R^+,f_3(x)=x^2$ questa funzione è sia iniettiva sia suriettiva, allora è bigettiva.
![[Pasted image 20260303105232.png]]
### Proposizione 1.21
Sia $f:X\rightarrow Y$ una bigettiva tra insiemi non vuoti. Allora esiste un unica funzione $g:Y\rightarrow X$ tale che $g\circ f=id_x\iff g(f(x))=x=id_x\ \ \forall x\in X$ vale anche $f\circ g=id_y$
La funzione $g:Y\rightarrow X$ si dice inversa di $f$ e si indica con $f^{-1}:Y\rightarrow X$
Dimostrazione : Sia $y\in Y$ poichè $f$ è bigettiva allora $f^{-1}(y)=\{x\in X|f(x)=y\}=\{x_y\}$ adesso definiamo $g:Y\rightarrow X$ ponendo $g(Y):=x_y\ \ \forall y\in Y$ 
Vale $(f\circ g)(y)=f(g(y))=f(x_y)=y$
$g\circ f=id_x$? Sia $x_0\in X$ allora per definizione $f(x_0)=f(x)\iff x_0=x$$\iff (g\circ f)(x_0)=(g\circ f)(x)$
#### Esercizi
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
#### Def 3.1 Insiemi equipotenti (Cenni)
Siano X e Y due insiemi (anche vuoti) diciamo che X è equipotente a Y, scrivendo $X\sim Y$, se esiste una bigettiva $f:X\rightarrow Y$, cioè se hanno lo stesso numero di elementi.
Proposizione : Dati X,Y e Z tre insiemi valgono:
	(1) $X\sim X$, l'identità basta come dimostrazione 
	(2) $X\sim Y\implies Y\sim X$, se esiste la bigettiva da X a Y allora la sua inversa è lda Y a X.
	(3) $X\sim Y$ e $Y\sim Z\implies X\sim Z$
### Insieme Cardinale
Per capire cosa è un insieme cardinale ci serve il concetto di **classe**, in specifico la classe di tutti gli insiemi. In tale classe si può effettuare un operazione di estrazione (denotata da "|X|") che per ogni insieme nella classe restituisce un insieme rappresentante, questo insieme rappresentante (chiamato **cardinale**) è sempre equipotente al insieme input. Per esempio : $|\varnothing|=\varnothing$, $|\{a\}|=|\{b\}|=|\{£\}|=|\{8\}|=\dots=\{0\}$, $|\{a,b\}|=\dots=\{0,1\}$ e ecc
Dalla costruzione segue che
- Ogni insieme X è equipotente al suo insieme cardinale $X\sim |X|$
- Due insiemi cardinali distinti non sono mai equipotenti.
#### Teorema 2.6
Siano X e Y due insiemi vale la seguente equivalenza: $X\sim Y\iff|X|=|Y|$ 
**Dimostrazione** : non ho scritto
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
#### Intuizione
$$  
\begin{cases}  
f(0)&=?\\  
\forall n\in&\Bbb N,f(succ(n))=h(n,f(n))
\end{cases}
$$
$$  
\begin{cases}  
f(0)&=m+0=m=c\\  
m+&(n+1)=(m+n)+1=succ(m+n)
\end{cases}
$$
Riassumendo:
	$X:=\Bbb N,h:\Bbb N\times\Bbb N$ definiamo ponendo $h(a,b):=succ(b),\forall(a,b)\in\Bbb N\times\Bbb N$ 
	$c=m$ 
	$\implies$teorema ricorsivo$\implies\exists!f:\Bbb N\rightarrow\Bbb N$ tale che :
$$  
\begin{cases}  
f(0)=m\\  
\forall n\in\Bbb N,f(succ(n))=h(n,f(n))=succ(f(n))
\end{cases}
$$
Esercizio:
Definire via teorema di ricorsione la funzione "moltiplicazione a sinistra con m", $X=\Bbb N$, cioè determinare:
	"$m*0=0$", c=?
	"$m*(succ(n))=h(n,m*n)$"

#### Ordinamento totale di $\Bbb N$
Definizione 3.6 : Sia X un insieme non vuoto ossia $R\subset X\times X$ diremo che $Ru'$ un ordinamento parziale di X se :
	(1) $xRx\ \forall x\in X$ (riflessiva)
	(2) $\forall x,y\in X, (xRy)$ e $(yRx)\iff x=y$ (simetrica)
	(3) $\forall x,y,z\in X,(xRy)$ e $(yRz)\implies xRz$ (transitivo)
Se in aggiunta vale la proposizione 
	(4) $\forall x,y\in X,(xRy)$ o $(yRx)$ (tricot?)
	R si dice ordine totale di x la coppia $(X,R)$ se R è un ordine parziale (totale) di X.
Definizione 3.3 : Siano $n,m\in\Bbb N$ definiamo $\le\ \subset\Bbb N\times\Bbb N$ ponendo $n\le m$ se $\exists k\in\Bbb N$ tale che $m=n+k$.
Teorema 3.5 : $(\Bbb N,\le)$ è totalmente ordinato.