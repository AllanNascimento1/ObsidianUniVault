Prof : Claudio Agostinelli
Libro : Probabilità e Statistica Ross
	https://z-library.sk/book/d5R08g8ARp/probabilit%C3%A0-e-statistica-per-lingegneria-e-le-scienze.html
Sito : datascience.maths.unitn.it/~claudio/teaching/ps/2025/index.html
	user : PS2025
	pass : Glivenko2025?
Esercizi teorici per casa ogni settimana.
Gli esercizi per casa saranno gli stessi del esame intermedio e del esame finale, però con i numeri cambiati.
Le prove sono composte da :
	10 domande a risposta multipla
	4 esercizi
	Durano 120 minuti
#### Programma/Indice
Probabilità 70%
	Introduzione
	Assiomi della Probabilità
	Probabilità condizionata e Indipendenza Stocastica
	Variabili aleatorie
	Teoremi limite (Grandi Numeri)
Statistica Inferenziale di tipo parametrico 30%
	Strumento verosimiglianza
		Stime puntuale
		Stime Intervallare
		Verifica delle ipotesi (forse)
		Modello lineare (forse)
## Lezione 1
La probabilità soggettiva è il tipo di probabilità dove i dati iniziali del problema e la probabilità da calcolare non sono ben definiti, questo tipo di probabilità non sarà trattato in questo corso.

**Definizione : Esperimento Aleatorio (o Casuale)**
Un Esperimento si dice Aleatorio (o Casuale) per un certo individuo, in un certo istante, se l'individuo non è ancora in grado di indicare con sicurezza il risultato (indipendentemente se l'esperimento è già avvenuto oppure no).

**Definizione : Esito (o Evento Elementare)**
Un evento elementare è un possibile risultato del nostro esperimento aleatorio. Gli eventi elementari sono tra loro **incompatibili**, cioè se l'esperimento risulta uno non può succedere nessun altro esito.
Gli eventi elementari possono essere scritti nei seguenti modi : 
	Se lancio un dado a 6 facce allora gli eventi possono essere : 
	- $A_1=\{1\}=$"1"={"esce il numero 1"}={"esce la faccia con l'etichetta 1"}
	- $A_2=${"esce un numero pari"}={2,4,6}
	- Ecc...
Come visto sopra gli eventi elementari sono insiemi composti per elenco o per descrizione 

**Definizione : Spazio Campionario ($\Omega$)**
Un spazio campionario è la collezione di tutti gli eventi elementari di un esperimento, gli elementi di $\Omega$ sono :
- A due a due incompatibili.
- Sono esaustivi, cioè l'esperimento non può risultare un esito al di fuori di $\Omega$.
	Esempio : 
		Estraiamo una pallina da una scatola con 3 palline (rossa, verde, bianca), i nostri eventi elementari sono : 
		Verde={"pallina verde"}, Bianca={"pallina Bianca"}, Rossa={"pallina rossa"} 
		Allora $\Omega=\{V,B,R\}$
		Ma se definiamo l'evento elementare come: Palline={"uscita una palina"} allora $\Omega_P=\{Palline\}$ 
		Si noti che in Palline ci sono anche gli eventi Verde, Bianca e Rossa allora l'unione tra $\Omega$ e $\Omega_P$ non è un spazio campionario dato che gli eventi elementari non sono incompatibili (può uscire sia una pallina sia un colore).

**Ripasso Diagramma di Venn**
![[Pasted image 20260310101308.png]]
$A\cup B$ unione, $A\cap B$ intercessione , $A^c$ complemento di A

**Esperimenti più complessi**
Gli eventi elementari possono essere insiemi formati da più elementi (cioè coppie) e esistono diversi modi per descrivere l'spazio campionario di questi esperimenti : 
Esempio : 
Lancio due dadi a 6 facce, gli eventi elementari saranno coppie (i,j) allora
- Posso elencare tutte le coppie $\Omega=\{(1,1),(2,1),(3,1),\dots,(1,2),(1,3),(1,4),\dots\}$ 
- Posso anche definire $\Omega=\Omega_A\times\Omega_B$ dove $\Omega_A=\{1,2,3,4,5,6\}$ e $\Omega_B=\{1,2,3,4,5,6\}$

**Regole di De Morgan**
- $(A\cup B)^c=A^c\cap B^c$ 
- $(A\cap B)^c=A^c\cup B^c$ 
- $(A^c)^c=A$ 
Supponiamo $A_1,A_2,\dots,A_n\subseteq\Omega$ 
$$(\bigcup_{i=1}^nA_i)^c=\bigcap_{i=1}^nA_i^c$$
$$(\bigcap_{i=1}^nA_i)^c=\bigcup_{i=1}^nA_i^c$$
Una successione numerabile di insiemi
$$(A_i)_{i=1}^{+\infty}$$
Definizione Insieme delle parti : Insieme potenza è la collezione di tutti i sottoinsiemi di $\Omega$. la denotiamo $P(\Omega)$.
- Indichiamo la cardinalità di $\Omega$ : #$\Omega$ 
- Se $\Omega$ è finito allora $\#P(\Omega)=2^{\#\Omega}$ 
### Probabilità Assiomatica
Dato un spazio campionario $\Omega$ e il suo insieme potenza $P(\Omega)$ la probabilità è una applicazione
$P_r:P(\Omega)\rightarrow\Bbb R^+$ che deve soddisfare le seguenti proprietà : 
1) (non negatività) se $A\in P(\Omega)$ allora $Pr(A)\ge 0$
2) (normalizzazione) $Pr(\Omega) = 1$
3) ($\sigma$ additività) se $(A_i)_{i=1}^{+\infty}$ tale che $A_i\in P(\Omega)\ \ \forall i\in\Bbb N$ è a due incompatibile $A_i\cap A_j=\varnothing$   $\forall i,j\ \ i\neq j$ allora $Pr(\bigcup_{i=1}^{+\infty}A_i)=\sum_{i=1}^{+\infty}Pr(A_i)$
	3') (additività) se $(A_i)_{i=1}^n$ tale che $A_i\cap A_j=\varnothing$  $\forall i,j\ \ i\neq j$ allora $Pr(\bigcup_{i=1}^nA_i)=\sum_{i=1}^{n}Pr(A_i)$ 

Esempio : 
$\Omega=\{1,2,3,4,5,6\}$ assumiamo che $Pr(\{1\})=Pr(\{2\})=\dots=Pr(\{6\})=p$.
$1=^{(2)}Pr(\Omega)=Pr(\{1,2,3,4,5,6\})=Pr(\{1\}\cup\{2\}\cup\dots\cup\{6\})=Pr(\bigcup_{i=1}^{6}\{i\})=^{(3)}6p$ 
$\implies p=\frac16$ 
$Pr(\{1,2\})=Pr(\{1\}\cup\{2\})=^{(3)}Pr(\{1\})+Pr(\{2\})=\frac16+\frac16=\frac13$ 
$Pr(\{\pi\})=$ non lo so, non è definita.

Regola 1:
Se A è un evento con $Pr(A)$ allora $Pr(A^c)=1-Pr(A)$ , $\Omega=A\cup A^c$ , $\varnothing=A\cap A^c$ 
2) $Pr(\Omega)=1$
3) $Pr(\Omega)=Pr(A\cup A^c)=^{(3)}Pr(A)+Pr(A^c)=1$ allora $Pr(A^c)=1-Pr(A)$ 

Regola 2:
Se A e B sono due eventi (compatibili) allora : $Pr(A\cup B)=Pr(A)+Pr(B)-Pr(A\cap B)$
- $A\cup B=A\cup(B\cap A^c)$ 
- $A\cap(B\cap A^c)=\varnothing$ 
- $B=(A\cap B)\cup(A^c\cap B)$ 
$Pr(A\cup B) = Pr(A\cup(B\cap A^c))=^{(B)}Pr(A)+Pr(B\cap A^c)$
$Pr(B)=Pr((A\cap B)\cup(A^c\cap B))=^{(3)}Pr(A\cap B)+Pr(A^c\cap B)$
$Pr(A\cup B)-Pr(B)=Pr(A)-Pr(A\cap B)$ 

Regola 3:
Se $A\subseteq B$ allora $Pr(A)\leq Pr(B)$
- $B=(A\cap B)\cup(A^c\cap B)=A\cup(A^c\cap B)$ 
- $Pr(B)=Pr(A\cup(A^c\cap B))=^{(3)}Pr(A)+Pr(A^c\cap B)\geq^{(2)}Pr(A)$ poiché $Pr(A^c\cap B)\geq 0$.
	Nota : $A\in P(\Omega)$ allora $A\subseteq\Omega$ , se si applica la regola 3 allora $Pr(A)\leq Pr(\Omega)=^{(2)}1$ 

Regola 4 (Disuguaglianza di Bonferroni): Non la facciamo.
### Probabilità dove $\Omega$ è numerabile
Costituzione di una probabilità quando $\Omega$ è numerabile (quantità non finita di elementi), cioè quando devo ripetere l'esperimento finché esce il risultato desiderato.
$\Omega=(\omega_i)_{i=1}^{+\infty}$ dove $\omega_i$ sono gli eventi elementari.
$P(\Omega)$, ad ogni $\omega_i\in P(\Omega)$ assegno un peso $p(\omega_i)$  $\forall i\in\Bbb N$ 
(i) $p(\omega_i)\geq 0$ 
(ii) $\sum_{i=1}^{+\infty}p(\omega_i)=1$ la $Pr(A)=Pr(\bigcup_{\omega_i\in A}\omega_i)=^{(3)}\sum_{\omega\in A}Pr(\omega_i)$ 
##### Ipotesi di equiprobabilità
Assumiamo adesso di considerare una funzione $p(\omega_i)=p$ 
$\Omega=\bigcup_{i=1}^{+\infty}\{\omega_i\}$
$1=^{(2)}Pr(\Omega)=Pr(\bigcup_{i=1}^{+\infty}\{\omega_i\})=^{(3)}\sum_{i=1}^{+\infty}Pr(\{\omega_i\})=\sum_{i=1}^{+\infty}p(\omega_i)$  
- Se $p=0$ allora $\implies0\neq 1$
- Se $p>0$ allora $\implies +\infty\neq 1$ 
	Allora se $\omega$ è numerabile la $Pr(\omega_i)$ non può essere equiprobabile

Esempio : **RIGUARDARSI LE SERIE GEOMETRICHE**
$\Omega=\{0,1,2,\dots\}$ 
$P_r(\{n\})=\frac1{2^{n+1}}$   $\forall n\in\Omega$ 
Devo verificare che la somma di tutte le $P_r$ sia 1 e che nessuna probabilità sia negativa.
$P_r(\Omega)=P(\bigcup\{n\})=^{(3)}\sum^\infty_{n=0}P_r(\{n\})=\sum^\infty_{n=0}\frac1{2^{n+1}}$
$\sum^\infty_{n=0}q^n=\frac1{1-q}$ se $0<q<1$ 
Calcolare la probabilità che {n è un numero pari}={0,2,4,6,...}=$\{0\}\cup\{2\}\cup\{4\}\cup\dots$ 
L'evento complementare è {n è dispari}={1,3,5,7,...}
	$P_r(\{disp\})=P_n(\bigcup\{n\})=^{(3)}\sum Pr(\{n\})=\sum_{n=1}^\infty(\frac14)=\frac13$ ???
	$P_r(\{pari\})=1-P_r(\{disp\})=1-\frac13=\frac23$ 

Definizione : Data una famiglia di spazi campionari $\{\Omega_i\}_{i\in I}$ con l'insieme I di cardinalita finita definiamo $\Omega=\times_{i\in I}\Omega_i$ spazio campionario prodotto 
$P_i=P(\Omega_i)$ 
$P=P(\Omega)=\oplus_{i\in I} P(\Omega_i)$ Probabilità di numeri prodotto

Definizione: Probabilità Prodotto
$A_i\in P(\Omega_i)$  $i\in I$ 
$A=\prod_{i\in I}A_i\in P(\Omega)$ 
$P_r(A)=P_r(\prod_{i=I}A_i)=\prod_{i\in I}P_i(A_i)$ 

Esempio: Lancio di due monete allora : 
$\Omega=\{(T,T),(T,C),(C,T),(C,C)\}$ 
altrimenti posso definire $\Omega=\times_{i=1}^2\Omega_i=\Omega_1\times\Omega_2$ dove $\Omega_1=\{T,C\}$ e $\Omega_2=\{T,C\}$ 
altrimenti se $P_1=P(\Omega_1)$ e $P_2=P(\Omega_2)$ allora $P=\oplus_{i=1}^2P_i=P(\Omega)$ $$  
Pr_1(\omega_1)=\begin{cases}  
\frac12\ se\ \omega_1=T\\  
\frac12\ se\ \omega_1=C
\end{cases}
$$$$  
Pr_2(\omega_2)=\begin{cases}  
\frac12\ se\ \omega_2=T\\  
\frac12\ se\ \omega_2=C
\end{cases}
$$
allora : $Pr((T,T))=Pr_1(T)*Pr_2(T)=\frac14$ 
$Pr((\omega_1,\omega_2))=Pr_1(\omega_1)*Pr_2(\omega_2)$ 

Esercizio 1 : Se uno spazio campionario $\Omega$ ci sono due sottoinsiemi $A,B\subseteq\Omega$ 
$Pr(A^c)=0,3$ , $Pr(B)=0,4$ , $Pr(A\cap B^c)=0,5$ come definisco $\Omega$ ?
Possiamo provare $Pr(A)=1-Pr(A^c)=0,7$ e $Pr(B^c)=1-Pr(B)=0,6$ 
	Definisco $\Omega_A=\{A,A^c\}$ e $\Omega_B=\{B,B^c\}$ allora 
	$\Omega=\Omega_A\times\Omega_B=\{(A,B),(A^c,B),(A,B^c),(A^c,B^c)\}=$
	$\{A\cap B,A^c\cap B,A\cap B^c,A^c\cap B^c\}$ 
	NB: A e B non definiscono l'intero $\Omega$ dato che $Pr(A\cup B)=Pr(B)+Pr(A\cap B^c)=0,9\neq1\neq Pr(\Omega)$ e secondo la regola 3 $Pr(A\cup B)<Pr(\Omega)\implies A\cup B\subset\Omega$ 
Se proviamo a definire la probabilità prodotto $Pr(A\cap B^c)=0,7*0,6$ però $0,7*0,6\neq 0,5$ allora la probabilità prodotto non definisce **questo** esperimento (può essere utile se ridefiniamo l'esperimento).

Esercizio 2 : Mezza di carte (52 carte) e ne estraiamo una in maniera casuale
$\Omega=\{1,2,3,\dots,52\}$ 
Fiori = $1,\dots,13$
Picche =$14,\dots, /$
Cuori = $\dots$
Quadri = $\dots, 52$
Qual è la probabilità di estrarre una figura qualsiasi o una carta di fiori $A_1=${"figura"}
$A_2=${"fiori"}
$Pr(A_1)=Pr(\{11,12,13,\dots\})=^{(3)}Pr(\{11\})+Pr(\{12\})+\dots=\frac1{52}*12=\frac{\#A_1}{\#\Omega}$
$Pr(A_2)=\frac{\#A_2}{\#\Omega}=\frac{13}{52}$
$Pr(A_1\cap A_2)=Pr(\{11,12,13\})=\frac3{52}$ 
$Pr(A_1\cup A_2)=Pr(A_1)+Pr(A_2)-Pr(A_1\cap A_2)=\frac{12}{52}+\frac{13}{52}-\frac{3}{52}=\frac{22}{52}$  