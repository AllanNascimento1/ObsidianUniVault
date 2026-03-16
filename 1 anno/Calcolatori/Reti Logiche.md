Le reti logiche sono circuiti che trasformano alcuni valori logici in ingresso in altri valori logici in uscita.
Sono di due tipi :
- Combinatorie : Non hanno memoria, l'uscita dipende solo dal input
- Sequenziali : Hanno memoria, l'output dipende dal stato interno del circuito
### Combinatorie
Una delle maniere per rappresentare una rete logica combinatoria è quella della tabella di verità che elenca tutti gli output possibili in base ai bit in ingresso.
Dato che questa rappresentazione diventa infattibile se hai troppi bit allora esiste anche gli operatori del algebra di Boole che possono descrivere qualsiasi tabella di verità.
Alcuni dei circuiti combinatori più usati in calcolatori moderni sono :
- **Decoder** : I decoder hanno un uscita per ogni combinazione possibile degli input che si attivano quando riceve la combinazione corretta.
- **Multiplex** : Circuito con diversi input e un singolo output, attraverso degli input aggiuntivi di controllo questo circuito determina quale degli input passa.
### Sequenziali
Le reti logiche di tipo sequenziali sono spesso necessarie nei calcolatori per la loro capacità di memorizzare informazioni, questi circuiti sono ottenuti attraverso una **"reazione"** cioè reindirizzare le uscite alle entrate in modo da creare un anello.
Per memorizzare un singolo bit si usa un **Latch D** o **Flip-Flop**, questi circuiti rimediano al problema di un **Stato Indecidibile** (quando è impossibile conoscere l'output con certezza) attraverso un input **Clock** e una tabella di verità che non ha un stato indecidibile.
#### Problema di temporizzazione
Diversi circuiti sequenziali possono non funzionare come si spera quando si cambia il suo input, dato che per periodi di tempo molto piccoli la rete logica può ricevere una sequenza che cambia il suo stato interno prima di ricevere l'input aspettato cambiando cosi il suo output.
Per questo motivo tutti i calcolatori moderni hanno un clock interno (un segnale periodico) che viene messo come ingresso di abilitazione, cioè forza gli input a zero se il segnale clock è a zero.
## Algebra di Boole
Le operazioni basi sono AND $A\cdot B$ , OR $A+B$ e NOT $\bar A$. Le regole basi sono:
	Identità : A+0=A , $A\cdot 1=A$
	Zero e uno : A+1=1, $A\cdot 0=0$ 
	Regola dell'inversa : $A+\bar A=1$, $A\cdot\bar A=0$
	Regola commutativa : $A+B=B+A$ , $A\cdot B=B\cdot A$ 
	Regola associativa : $A+(B+C)=(A+B)+C$ , $A\cdot(B\cdot C)=(A\cdot B)\cdot C$ 
	Regola distributiva : $A\cdot(B+C)=(A\cdot B)(A\cdot C)$ , $A+(B\cdot C)=(A+B)(A+C)$
Esistono anche le 2 **Regole De Morgan**
	$\overline{A\cdot B}=\bar A+\bar B$  e $\overline{A+B}=\bar A\cdot\bar B$ 

Per trasformare una tabella di verità in un espressione booleana basta guardare quali combinazioni di input genera l'output 1, per ogni combinazione trovata usi degli AND sugli input per ottenere 1, dopo sommi attraverso OR tutti i prodotti ottenuti.
![[Pasted image 20260310142305.png]]
Questa espressione è chiamata Forma Canonica