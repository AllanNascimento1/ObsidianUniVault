## Vettori Geometrici
Nel algebra lineare i punti sono rappresentati nel [insieme](Ana%20Mat%20Generale.md#Teoria%20degli%20insiemi) $\Bbb R^2$ (Piano) o $\Bbb R^3$ (Spazio), che sono l'insiemi formati dal [prodotto cartesiano](Ana%20Mat%20Generale.md#Prodotto%20Cartesiano) di $\Bbb R\times\Bbb R$ per il piano e $\Bbb R\times\Bbb R\times\Bbb R$ per l'spazio, questi punti possono essere identificati mediante l'introduzione di un sistema di coordinate cartesiane. 
Questi punti sono scritti $P(x,y)$ nel piano e $P(x,y,z)$ nel spazio.

La prima definizione di vettore geometrico è per ogni coppia $A = (x_A,y_A)$ , $B = (x_B,y_B)$ nel piano, il vettore geometrico $\vec {AB}$ è l'elemento di $\Bbb R^2$ aventi componenti $(x_B - x_A,y_B-y_A)$ , la stessa identica cosa vale per $\Bbb R^3$. 
I vettori ottenuti da $\vec {AB}=(x_B - x_A,y_B-y_A)$  si chiamano **vettori applicati** (dato che hanno l'origine in $O$) e sono quelli utilizzati da tutte le operazioni che vedremmo più avanti.

Graficamente ciò significa che il vettore $\vec {AB}$ è una freccia che parte dal punto di origine $O(0,0,0)$ e arriva al punto $(x_B - x_A,y_B-y_A)$ che pero, se questa freccia viene spostata in modo tale che il suo punto di origine sia il punto $A$ essa punterà a $B$ .
![[Pasted image 20250913194011.png]]
Osservazione : Il vettore $\vec {AB}$ in figura può anche essere visto come il punto $C$ , dato che entrambi hanno gli stessi componenti $(x,y,z)$ , quindi puoi immaginare questa operazione come spostando i due punti finché il punto $A$ sia nel origine e prendendo il nuovo valore di $B$ per il vettore.
### Operazioni
Negli insiemi del piano e spazio si possono introdurre due operazioni
#### Somma di vettori geometrici
La somma di due vettori geometrici $\vec V$ e $\vec W$ risulta nel vettore geometrico $\vec V+\vec W=(x_V+x_W,y_V+v_W)$ . 
Se invece di avere i vettori $\vec V$ e $\vec W$ hai solo i punti che lo formano $A,B$ e $C,D$ dovrai ottenere i componenti dei tuoi vettori ricordando la formula $\vec {AB}=(x_B - x_A,y_B-y_A)$ , quindi la formula per intero sarebbe $\vec {AB}+\vec {CD}=(x_B-x_A+x_D-x_C,y_B-y_A+y_D-y_C)$

Geometricamente questo processo è come prendere i due vettori applicati $\vec V$ e $\vec W$ (che partono da $O(0,0)$ ) e spostare uno di essi nella punta del altro, successivamente si prende il vettore che parte dal origine e arriva alla punta del secondo vettore.
![[Pasted image 20250913201641.png]]
##### Proprietà fondamentali
Associativa : 
	$(\vec {AB}+\vec {BC})+\vec {CD}$ = $\vec {AB}+(\vec {BC}+\vec {CD})$ $\forall$ $A,B,C,D$.
	$(\vec V+\vec W)+\vec R$ = $\vec V+(\vec W+\vec R)$
Esistenza del elemento neutro : 
	esiste un vettore nullo $\vec O$ dove $\vec {AA}$ = $\vec O$ qualunque sia il punto $A$. 
	L'elemento neutro ha la proprietà : $\vec {AB}+\vec O$ = $\vec O + \vec {AB}$ = $\vec AB$.
	In pratica questa proprietà dice che esiste il vettore $\vec O=(0,0,0)$.
Vettore opposto : 
	per ogni $A,B$ esiste un vettore opposto $-\vec {AB}=\vec {BA}$ tale che $\vec {AB}+\vec BA$ = $\vec {BA}+\vec {AB}$ = $\vec O$.
	Il vettore opposto si può anche ottenere $-\vec V=-1*\vec V$.
Commutativa : 
	$\vec {AB}+\vec {CD}=\vec {CD}+\vec{AB}$ per ogni $A,B,C,D$.
#### Moltiplicazione Scalare
La moltiplicazione scalare è il prodotto tra un numero reale $t$ e un vettore geometrico $\vec {AB}$ (che come sempre è un vettore applicato) aventi componenti $(tx_B-tx_A,ty_B-ty_A)$. La stessa cosa vale per l'spazio.
Geometricamente questo significa che $t\vec {AB}$ forma il vettore $\vec {AB'}$, che avrà lunghezza $|\vec {AB'}| = t\times|\vec {AB}|$, la direzione del nuovo vettore cambia in base al valore di $t$ :  
	Se $t>0$ , il punto $B'$ sarà sulla semiretta $AB$. 
	![[Pasted image 20250914103527.png]]
	Esiste anche il caso dove $t>0$ e $t<1$ in cui il punto $B'$ sarà sulla semiretta $AB$ ma formerà un vettore di lunghezza minore rispetto ad $\vec {AB}$.
	![[Pasted image 20250914104339.png]]
	Se $t<0$ il punto $B'$ sarà sulla semiretta opposta ad $\vec {AB}$ .
	![[Pasted image 20250914105433.png]]
NB: I vettori $AB$ e $AB'$ sono vettori applicati, quindi nelle immagini partono dal origine $O(0,0,0)$.
## Rette
Grazie alla moltiplicazione scalare, una retta $r$ può essere rappresentata da due punti $P_1(x_1,y_1)$ e $P_2(x_2,y_2)$, dato che ogni altro punto $P$ della retta $r$ verifica la condizione $\vec {P_1P} = t\vec {P_1P_2}$ possiamo trovare le componenti del punto $P(x,y)$ $\in r$ attraverso la [forma parametrica](Equazioni%20Parametriche.md) della retta $r$.
$$  
\left\{\begin{align*}  
x &= x_1 + t(x_2-x_1)\\  
y &= y_1 + t(y_2-y_1)
\end{align*}\right.
$$
Geometricamente questa equazione è come prendere il vettore applicato di $\vec {P_1P_2}$ e scalarlo per $t$, questo crea un nuovo vettore $\vec {P_1P}$ che se spostato al punto di origine della retta, ossia $P_1$, risulterà nel punto $P$.
![[Pasted image 20250916094036.png]]

Se eliminiamo il parametro $t$ dalla equazione possiamo ottenere un [equazione cartesiana](Equazioni%20Cartesiane.md) della retta.
$$ax+by=c$$
	Svolgimento, considerando $\vec V(x_V,y_V) = (x_1-x_2 , y_1-y_2)$ :
$$
\left\{\begin{align*}  
x &= x_1 + tx_V\\  
y &= y_1 + ty_V 
\end{align*}\right.
$$
$$
\left\{\begin{align*}  
t &= \frac{x - x_1}{x_V}\\  
y &= y_1 + (\frac{x - x_1}{x_V})y_V 
\end{align*}\right.
$$
$$\frac{y -y_1}{y_V} = \frac{x - x_1}{x_V} $$
$$\frac{y}{y_V}-\frac{y_1}{y_V} = \frac{x}{x_V}-\frac{x_1}{x_V}$$
$$\frac{y}{y_V}-\frac{x}{x_V} = \frac{y_1}{y_V}-\frac {x_1}{x_V}$$
$$\frac{x_V*y-y_V*x}{y_V*x_V} = \frac{y_1*x_V-x_1*y_V}{y_V*x_V}$$
$$x_V*y-y_V*x = y_1*x_V-x_1*y_V$$
$$ax+by=c$$
la differenza tra queste due equazioni è che la forma parametrica è in funzione di t, cioè si può trovare $P(x,y)$ a partire di $t$ o $t$ a partire di un punto $P$ sulla retta. Mentre l'equazione cartesiana funziona attraverso $x$ e $y$.

Nel spazio le rette hanno un equazioni parametrica per ogni suo componente $(x,y,z)$.
$$  
\left\{\begin{align*}  
x - x_1 &= t(x_2-x_1)\\  
y - y_1 &= t(y_2-y_1)\\
z - z_1 &= t(z_2-z_1)
\end{align*}\right.
$$
Di conseguenza le rette nello spazio sono composte anche da due equazioni cartesiane nella forma.
$$\begin{align*}  
by+ax&=d\\
cz+ax&=d
\end{align*}$$
NB: le due equazioni cartesiane dipendono da quale eq. parametrica hai ottenuto $t$, nel caso sopra $t$ è stato preso dalla eq. parametrica di $x$.
## Piani e Combinazione Lineare
Piani nel algebra lineare sono spesso chiamati con il $\pi$. Il piano può essere descritto da 3 punti $P_1,P_2,P_3$ nello spazio. Un punto $P$ appartiene a $\pi$ se $\vec {P_1P}$ = $s\vec {P_1P_2}+t\vec {P_1P_3}$ (questa operazione si chiama **Combinazione Lineare** di $\vec {P_1P_2}$ e $\vec {P_1P_3}$ ). 
La combinazione lineare funziona perché qualsiasi punto $P$ del piano può essere identificato attraverso la somma di due vettori moltiplicati per l'scalare $t$ e $s$, se essi non sono proporzionali (cioè giacciano sulla stessa retta). 
![[Pasted image 20250919082812.png]]

## Lunghezze e Prodotto Scalare 
Il prodotto Scalare ha due espressioni che risultano nel stesso valore, se guardi il quaderno (o la scheda su moodle) vedrai la dimostrazione della loro uguaglianza:
$\vec v*\vec w = v_1w_1+v_2w_2$ 
$\vec v*\vec w=|\vec v||\vec w|cos(\alpha)$ 
La seconda espressione può essere vista geometricamente come l'area del rettangolo formato dalla base uguale al vettore $\vec v$ e altezza uguale al vettore creato dalla proiezione di $|\vec v|cos(\alpha)$ su $\vec w$.
![[Pasted image 20250919152015.png]]
Un'altra caratteristica del prodotto scalare è che può essere usato per determinare se due rette sono ortogonali, dato che se l'angolo tra di loro è di 90° il $cos(\alpha)$ risulterà 0 è di conseguenza anche il risultato del prodotto sarà 0. 
### Alcune applicazioni del Prodotto Scalare
#### **(1)** Trovare rette ortogonali
Attraverso il prodotto scalare possiamo anche trovare facilmente dei vettori ortogonali ad rette nel piano, e a piani nel spazio, troviamo vettori ortogonali ai piani attraverso la loro equazione cartesiana. 
**Rette in $V^2$**
Dato una retta nel piano di equazione $ax+by=c$ possiamo sostituire ai componenti i valore di due punti $P_1$ , $P_2$ nella retta per ottenere il sistema:
$$
\left\{\begin{align*}  
ax_1+by_1=c\\
ax_2+by_2=c
\end{align*}\right.
$$
Se adesso gli uguagliamo otterremo
$$a(x_2-x_1)+b(y_2-y_1)=0$$
Questa formula è identica a quella del prodotto scalare $v_x*w_x+v_y*w_y$ se $\vec w=(x_2-x_1,y_2-y_1)$, quindi questo significa che $a$ ed $b$ sono i componenti di un altro vettore ortogonale alla nostra retta.
$\vec n=(a,b)\Rightarrow\vec n*\vec {P_1P_2}=0$

**Piani in $V^3$**
Se applichiamo questo concetto nel spazio, dovremmo considerare un piano di equazione $ax+by+cz=d$ .
Quindi il vettore $\vec n=(a,b,c)$ sarà un vettore ortogonale al piano, questo vettore prende il nome di **normale**.
#### **(2)** Trovare l'area formata dal parallelogramma di due vettori
Per iniziare l'area di un parallelogramma si ottiene con $A=b*h$ dove $b$ è la base e $h$ l'altezza, quindi la base del nostro parallelogramma sarà la lunghezza di uno dei vettori $|\vec w|$ e la altezza può essere trovata con la proiezione del $sin(\alpha)$ moltiplicato per la ipotenusa $|\vec v|$, quindi l'area sarà $A=|\vec w||\vec v|sin(\alpha)$.
Possiamo semplificare l'equazione grazie al prodotto scalare e alla fine otterremo:
$A^2=|\vec v|^2|\vec w|^2-(\vec v*\vec w)^2$ 
che in $V^2$ può essere scritto come:
$A=|v_1*w_2-v_2*w_1|$ 
## Aree e Prodotto Vettoriale
Per calcolare l'area del parallelogramma nel spazio, possiamo sempre utilizzare la formula che abbiamo appena trovato ma dato che i vettori hanno una componente in più nel spazio, l'equazione diventa:
$A^2=(v_2w_3-v_3w_2)^2+(v_3w_1-v_1w_3)^2+(v_1w_2-v_2w_1)^2$
Questa operazione prende il nome di **Prodotto Vettoriale**.
$\vec v\times\vec w=(v_2w_3-v_3w_2$ , $v_3w_1-v_1w_3$ , $v_1w_2-v_2w_1)$

Come puoi vedere il prodotto vettoriale ritorna un altro vettore (**NB: Solamente in $V^3$** ), questo vettore ha come lunghezza l'area del parallelogramma dei due vettori originali, questo è perché il calcolo della lunghezza di un vettore è :
$|\vec v|^2=v_1^2+v_2^2+v_3^2$ 
Questo vettore ha anche la caratteristica che è ortogonale a $\vec v$ e $\vec w$. Perche? Boh

Alcune proprietà importanti:
(1) Se $\vec v$ e $\vec w$ sono proporzionali $\vec v\times\vec w=\vec O$, dato che l'angolo è di 0°
(2) Il verso del prodotto vettoriale è determinato dalla regola della mano destra, vedendolo come un orologio il vettore punterà verso di noi se partendo dalle 12:00 vediamo $\vec w$ (il secondo operatore) per primo altrimenti punterà lontano da noi.
### Alcune applicazioni del prodotto vettoriale
##### **(1)** Trovare il Volume del parallelepipedo di 3 vettori
Possiamo trovare il volume del parallelepipedo formato da 3 vettori attraverso il prodotto misto :
$$V=\vec u*(\vec v\times\vec w)$$
Questo perché come ho detto prima, il prodotto scalare è uguale al **area** formata dalla proiezione di un vettore (in questo caso $\vec u$) sul altro vettore (in questo caso $\vec v\times\vec w$), questa proiezione è equivale alla altezza del parallelepipedo, per la lunghezza del altro vettore ($\vec v\times\vec w$).
Quindi abbiamo la proiezione di $\vec u$ sul vettore $\vec v\times\vec w$ , ossia l'altezza, moltiplicato per la lunghezza di $\vec v\times\vec w$ , che dato le proprietà del prodotto vettoriale è proprio la area del parallelogramma formato da $\vec v$ e $\vec w$.
![[Pasted image 20251001080656.png]]
## Calcolo distanze in $V^3$ 
#### Distanza tra due punti
Per calcolare la distanza tra due punti $A$ e $B$ possiamo usare la formula di Pitagora.
$$dist(A,B)=\sqrt{(x_A-x_B)^2+(y_A-y_B)^2+(z_A-z_B)^2}$$
### Distanza tra un punto e una retta
Calcolare la distanza tra un punto $A$ e una retta $r$ è un po' più complesso e ci sono alcune maniere per farlo.
Quindi avremmo il punto $A$
$$A=(x_A,y_A,z_A)$$
E l'equazione in forma cartesiana della retta $r$, che dovremmo scrivere in forma parametrica:
$$r:\left\{\begin{align*}  
\pi_1:ax+by+cz+d=0\\
\pi_2:ax+by+cz+d=0
\end{align*}\right.$$

**(1) Trovando il piano ortogonale**
Una maniera è quella di trovare un piano $\pi$ ortogonalew a $r$ e contenente il punto $A$.
Trovare il piano ortog
## Gruppi
Per iniziare ricordiamoci gli insiemi numerici:
$\Bbb N = \{0,1,2,3,...\}$ naturali
$\Bbb Z = \{0,\pm1,\pm2,\pm3,...\}$ interi
$\Bbb Q = \{\frac pq|p\in\Bbb Z, q\in\Bbb Z, q\neq0\}$ razionali, insieme delle frazioni
$\Bbb R =$ numeri reali
In questi insiemi possiamo eseguire alcune operazioni che hanno alcune proprietà diverse in base al insieme.

Per esempio nel insieme dei naturali la somma è un operazione che deve soddisfare una condizione, altrimenti l'equazione può risultare un numero negativo, che non è presente nei $\Bbb N$.
$x+a=b$   $\in\Bbb N$ se $b>a$ 
La somma nel insieme degli interi non deve soddisfare nessuna condizione.
$x+a=b$   $\in\Bbb Z$   $\forall a\in\Bbb Z$  $\forall b\in\Bbb Z$ 
Ma la moltiplicazione nei $\Bbb Z$ invece, deve soddisfare una condizione che non è presente nel insieme dei razionali.

Quindi:
L'insieme dei interi esiste per l'operazione della sottrazione
I razionali per la divisione
I reali per le radici positive
I complessi per le radice con segno
Oss: Queste operazioni sono le inverse delle operazioni normali, e quindi sono categorizzate come la stessa operazione, sottrazione = somma. 
### Definizione Gruppo
Adesso possiamo dare una Definizione ai gruppi:
Un gruppo è un insieme G in cui è definita un operazione $*$ tale che
$*:G,G\to G$
$(a,b) \mapsto a*b$  
(prende in input 2 elementi di G e risulta in un altro elemento di G )
Questa operazione deve soddisfare queste 3 proprietà:
(1) Associativa $(a*b)*c=a*(b*c)$ 
(2) Esiste un elemento neutro $l\in G:a*l=l*a=a$ 
(3) Elementi simmetrici tale che $\forall a\in G$ $\exists$ $a'\in G:a*a'=a'*a=l$ 

Usiamo la seguente notazione per definire quale operazione in quale insieme vogliamo considerare $(\Bbb Z,+)$ , cioè la somma negli interi.
Esempi:
$(\Bbb Z,+)$ è un gruppo commutativo (a+b=b+a)
$(\Bbb N,+)$ non è un gruppo perché non soddisfa la seconda e terza condizione.

$(\Bbb N,\times)$ soddisfa la prima e seconda condizione ma non la terza.
$(\Bbb Q,\times)$ non è un gruppo, non soddisfa la terza condizione dato che **NON esiste** un elemento simmetrico a 0 tale che $0*n'=l$ cioè 1.
$(\Bbb Q^*=\Bbb Q/\{0\},\times)$ è un gruppo commutativo.

## Campi
I campi sono degli insiemi $\Bbb K$ che contengono gruppi commutativi per la somma e moltiplicazione (escludendo il 0).
(1) $(\Bbb K,+)$ è gruppo commutativo
(2) $(\Bbb K^*=\Bbb K/\{0\},\times)$ è gruppo commutativo
(3) Vale la proprietà distributiva, cioè $((a+b)\times c=ac+bc)$ 
## Spazi di n-uple
Gli insiemi che abbiamo usato per rappresentare i punti, cioè i prodotti cartesiani di $\Bbb R\times\Bbb R=\Bbb R^2$  e  $\Bbb R\times\Bbb R\times\Bbb R=\Bbb R^3$ possono essere generalizzate in qualsiasi insieme che soddisfa le condizioni per essere un **campo**.
$\Bbb R^n$ è detto spazio delle n-uple di numeri reali, dette anche vettori numerici a n componenti.
Un e-nupla è scritta $a=(a_1,a_2,...,a_n)$ dove $a\in\Bbb R^n$ 
### Operazioni
#### Somma
Per definire l'insieme delle n-uple $\Bbb R^n$ come un gruppo commutativo dobbiamo introdurre la somma nelle n-uple.
Dato $a=(a_1,a_2,...,a_n)$ e $b=(b_1,b_2,...,b_n)$
$$a+b=(a_1+b_1,a_2+b_2,...a_n+b_n)$$
L'elemento neutro sarà $O=(0,0,...,0)$ e $-a=(-a_1,-a_2,...,-a_n)$ 
#### Moltiplicazione per scalare
$$ka=(ka_1,ka_2,...,ka_n)$$
Dove $O=0*a$ l'elemento neutro è 1 e $(-1)a=-a$
## Matrici
Una matrice è una tabella rettangolare (quindi anche quadrata) di $m$ righe e $n$ colonne che appartiene al insieme $M_{m,n}(\Bbb R)$, l'insieme dei reali di $m\times n$.
$$A=\left[\begin{align*}  
a_{11}\quad a_{12}\quad &... \quad a_{1n}\\
a_{21}\quad a_{22}\quad &...\quad a_{2n}\\
...\quad ...\quad &...\quad ...\\
a_{m1}\quad a_{m2}\quad &...\quad a_{mn}
\end{align*}\right]$$
Per non scrivere tutte questo si userà la notazione $A=[a_{ij}]$. 
Delle matrici possono essere **Vettori Colonna** se sono di tipo (1,n), cioè se hanno una sola riga e possono essere identificati con la n-upla, o dei **Vettori Riga** se sono di tipo (m,1).
Se invece una matrice ha m=n essa è una **Matrice Quadrata** e appartiene al insieme $M_n(\Bbb R)$.
### Operazioni
#### Somma
Dato le matrici A e B
$$A+B=[a_{ij}+b_{ij}]$$
Elemento neutro: $O=[0_{ij}]$
$-A=[-a_{ij}]$ 
$A+(B+C)=(A+B)+C$ 
Quindi $(M_{n,m}(\Bbb R),+)$ è commutativo.
#### Moltiplicazione per scalare
Dato la matrice $A$ e l'scalare $k$
$$kA=[k*a_{ij}]$$
Elemento neutro è 1
$(-1)*A=-A=[-a_{ij}]$ 
$k(hA)=(kh)A$ 
$k(A+B)=kA+kB$
$(k_1+k_2)A=k_1A+k_2A$ 
Questo gruppo è commutativo
#### Moltiplicazione tra Matrici
La moltiplicazione tra matrici può avvenire solo tra **Matrici Conformabili**, cioè se la matrice a sinistra A ha lo stesso numero di colonne(n) dell numero di righe(m) della matrice a destra B.
Dato $A=[a_{ij}],(m,n)$ e $B=[b_{jk}](n,l)$ 
$$AB=C=[c_{ik}],(m,l)$$
$$c_{ij}=\sum_{h=1}^na_{ih+b_{hk}}=a_{i1}b_{1k}+a_{i2}b_{2k}+...+a_{in}b_{nk}$$
Quindi in pratica la cella $c_{ik}$ di C è uguale al **Prodotto Scalare** tra il **vettore colonna** di B in posizione k e il **vettore riga** di A in $i$.
L'elemento neutro è $I_n$ di tipo (n,n) dove $i_{ij}=0$ per $i\neq j$, $i_{ij}=1$ per $i=j$  tale che $AI_n=A=I_nA$  
$(AB)C=A(BC)$
$A(B+C)=AB+AC$
$k(AB)=(kA)B=A(kB)$
Questo gruppo NON è commutativo ($AB\neq BA$)
##### Inversione di Matrici
L'inversa di una matrice esiste solo se la matrice è quadrata.
L'inversa di $A$ è $A^{-1}$ tale che $A^{-1}A=I_n$ . 
Non tutte le matrici quadrate hanno una inversa. 
Il prodotto tra due matrici invertibili è se stesso invertibile, quindi si può definire l'insieme delle matrici invertibili $GL_n(\Bbb R)$ $(n\times n)$, questo insieme forma un gruppo non commutativo con l'inversione di matrici.
##### Potenza di Matrici
Una matrice può essere elevata solo se è quadrata.
Sia $k\geq 0$,  se k=0 $A^k=I_n$ 
se k>0
$$A^k=A*A*\ ...*A \quad (k\; volte)$$

$A^iA^j=A^{i+j}=A^jA^i$ 
##### Trasposizione di Matrice
La matrice trasposta di $A=[a_{ij}]$ (m,n), è la matrice $A^T=[a_{ji}]$ (n,m), cioè prendendo le colonne della matrice come righe.
Una matrice è **Simmetrica** quando la matrice è quadrata e $A=A^T$ 

$(AB)^T=B^TA^T$ 
### Sistemi lineari in forma matriciale
Grazie alla peculiare definizione della moltiplicazione matriciale possiamo descrivere un sistema di equazioni lineare come:
$$Ax=b$$
Dove A è la matrici dei **Coefficienti** delle incognite, x è un vettore colonna con le **Incognite** e b è un vettore colonna con i **Termini Noti**.
### Alcune Applicazioni delle Matrici
#### Teoria dei grafi
Un grafo $G$ è formato da un insieme di vertici $V$ e una lista di lati $E$, dove per lato si intende una coppia non ordinata (cioè $l_1(v_1,v_2)$=$l_2(v_2,v_1)$) di vertici.
Se i lati sono una coppia ordinata di vertici, il grafo si dice **Orientato**.
I grafi possono anche essere descritto da una matrice chiamata **Matrice di Adiacenza** $A=[a_{ij}]$ (n,n), dove ogni cella corrisponde al numero di lati che iniziano dal vertice $v_i$ e finiscono al vertice $v_j$, di conseguenza se il grafo non è orientato la matrice di adiacenza sarà simmetrica.
Una proprietà importante dei grafi sono i **Camini**, cioè una successione di lati che congiunge un vertice a un altro, la **Lunghezza** di un camino è il numero di lati nel camino.
##### Teorema
Sia $A$ la matrice di adiacenza a un grafo $G$, l'elemento in posizione $(i,j)$ della matrice $A^s$ è uguale al numero di camini di lunghezza $s$ con inizio in $v_i$ e fine in $v_j$.
Questo teorema ci dice che per trovare tutti i camini nel grafo $G$ di lunghezza $n$ possiamo semplicemente mettere la nostra matrice a potenza $n$. Quindi se vogliamo trovare tutti i camini di lunghezza 2 possiamo fare: $A^2=A*A$.
### Combinazioni lineari
La combinazione lineare delle matrici $A_1,...,A_k$ è una matrice:
$$c_1A_1+c_2A_2+...+c_kA_k|c_1,...,c_k\in\Bbb R$$
In particolare si può definire un sistema lineare di forma $Ax=b$ come la combinazione lineare delle colonne $A_1,A_2,...$ per gli elementi di $x=(x_1,x_2,...)$

