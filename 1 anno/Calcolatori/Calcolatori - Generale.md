## Struttura del corso
![[Pasted image 20260224133848.png]]
Tutte queste informazioni sono disponibili su moddle nella "Parte 1 - Basi -> Lezione 1(Introduzione)"
## Esame
Prova scritta intermedia il 15 aprile e 8 giugno, 6 domande multiple per i due parziali, se accetti i due parziali non devi fare l'esame.
Se i voti sono bassi sarà chiesto un orale obbligatorio.
## Tipi di Calcolatori
I calcolatori sono divisi in 3 macro categorie:
**Calcolatori personali** (desktop o laptop): buone prestazioni, eseguono software di terze parti (architetture aperte).
**Server**: Pensati per eseguire grandi carichi di lavoro.
**Embedded**: Coprono un vasto spettro di applicazioni (mobile, automotive, avionica, gaming), Le applicazioni sono spesso "dedicate" e operano a stretto contatto con l'hardware, requisiti non funzioni essenziali.

L'studio dei calcolatori è utile per ottenere maggiori prestazioni dal hardware, ossia comprendere la gerarchia di memoria e fare un uso efficiente del parallelismo (multi-threading ,GPU ,calcolo distribuito).
## Software di sistema
### Sistema Operativo (SO):
- Gestisce le operazioni di I/O
- Alloca la memoria
- Consente il multitasking
### Compilatore
- Traduce da linguaggio ad altro livello a linguaggio macchina
## Linguaggio Macchina e Assembly
Nei calcolatori l'unità di informazione base è il **bit**, un interruttore che vale 1 se acceso o 0 se spento, il calcolatore è capace di eseguire operazioni su i bit attraverso le porte logiche. Dato che i calcolatori lavorano solo con bit, anche le sequenze di istruzioni che compongono un programma sono espresse in bit.
**Assembly** è un linguaggio mnemonico (che associa ad un verbo un azione) che viene introdotto perché programmare con bit è estremamente difficile, questo linguaggio viene dopo tradotto in stringhe di bit da un traduttore **Assembler**.
Il flusso completo: 
**Ling. ad alto livello** -(compilatore)-> **Assembly** -(assembler)-> **Ling. macchina**
## Componenti del Calcolatore
- Processore
	- Unità di controllo
	- Unità di Elaborazione
- Unità di memoria
- Input e Output

**Componenti Hardware di un PC**: I PC seguono un standard che definisce i suoi componenti hardware ma per questo corso sono importanti:
- **Scheda madre**: piastra su cui sono montati i vari chip, contiene i bus per il trasporto di bit.
- **Memoria Volatile**: RAM
- **Memoria Permanente (o di massa)**: Hard Disk/SSD, CD/DVD e ROMs.
### Processore
Il processore è la parte attiva di ogni calcolatore, è composto da:
- Datapath (Unità di Elaborazione): esegue le operazioni aritmetiche sui dati
- Parte di controllo: indica al datapath, alla memoria e ai IO cosa fare.
- Cache: memoria RAM aggiuntiva per migliorare le prestazioni.
- CPU (core): 
- altri . . .
### Memoria Volatile
La memoria volatile, anche detta memoria principale, si occupa di memorizzare e disporre i dati al calcolatore durante la sua operazione però questi dati vengono persi al spegnimento.
### Memoria Permanente
Questo tipo di memoria si occupa di memorizzare i dati tra esecuzioni diverse e tra spegnimenti del dispositivo, di solito riescono a memorizzare una maggior quantità di dati.
## Astrazioni
Astrazioni permettono di gestire progetti di grande complessità in maniera più semplice, per esempio l'uso del processore avviene tramite un interfaccia che "nasconde" i dettagli delle istruzioni macchina che il processore offre.
Insieme all'interfaccia del sistema operativo, **l'ISA**costituisce l'interfaccia binaria delle applicazioni (Application Binary Interface).

