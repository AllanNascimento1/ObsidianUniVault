Il linguaggio assembly è un linguaggio intermedio tra i linguaggi di programmazione (Java, C++, ML e ecc) e il linguaggio macchina (sequenza di bit), Il compilatore di assembly si chiama **Assembler** ed è l'ultimo passaggio che il compilatore fa prima di ottenere un programma in linguaggio macchina.
Ogni istruzione assembly (tranne alcune poche eccezioni) corrisponde a una istruzione a linguaggio macchina.
Ogni dispositivo ha una architettura della CPU diversa e di conseguenza una **Instruction Set Architecture (ISA)** diversa, l'ISA di un dispositivo definisce :
- L'insieme delle istruzioni riconosciute dalla CPU 
- Il linguaggio assembly specifico a quel tipo di architettura 
- I registri della CPU.
Le due ISA che rappresentano i due estremi sono **CISC** e **RISC**:
- **RISC (Reduced Instruction Set Computer)** : Semplifica l'implementazione del hardware, però offre meno flessibilità e performance ai programmi.
- **CISC (Complex Instruction Set Computer)** : Offre istruzioni più complesse e flessibili al linguaggio assembly (e di conseguenza ottimizza i linguaggi ad alto livello) al costo di un maggiore costo e complessità al livello hardware.
Esiste anche altre architetture come :
- ARM (Advanced RISC Macchine) : Un architettura intermedia tra RISC e CISC.
### Istruzioni assembly
La CPU esegue un istruzione in 3 passaggi:
- Fetch : Prende l'istruzione nel area di memoria indicata dai registri "program counter"(PC) o "instruction pointer"(IP).
- Decode : ???
- Execute : Esegue l'istruzione che può essere una somma, salto, accesso alla memoria e ecc.
Le istruzioni assembly consistono in operazioni aritmetiche/logiche, modifiche/accesso ai registri e alla memoria e controllo del flusso di istruzioni (con salti e altri).

**Operazioni Aritmetiche/Logiche**
Tipicamente le operazioni aritmetiche/logiche hanno due operandi ed una destinazione, gli operandi e destinazione possono essere nei registri o nella memoria in base al ISA del dispositivo, queste due implementazioni rispecchiano le architetture RISC e CISC rispettivamente.
Architetture RISC : 

**Istruzioni di Movimento Memoria**
Le istruzioni di accesso/modifica della memoria hanno bisogno del area di memoria che l'istruzione vuole manipolare, questa area di memoria può essere ottenuta in diversi modi : 
- Assoluto : Indirizzo di memoria costante 
- Indiretto : indirizzo di memoria contenuto in un registro 
- indirizzo di memoria ottenuto attraverso operazioni nel valore di un registro
Architetture RISC
	load <destination\> , <memory location\>
	store <memory location\> , <destination\>

**Istruzioni di Controllo Flusso Istruzioni**
### Registri
I registri sono le aree di memoria immediatamente accessibili dalla CPU, sono usati per ogni operazione che la CPU può effettuare e sono aree di memoria molto piccole (di solito 32 registri con 64 bit ciascuno).
I registri sono determinati dal ISA e di conseguenza i registri cambiano da macchina a macchina, comunque questi sono alcuni dei registri :
- FLAG (non tutte ISA) : registro usato per memorizzare tutti i diversi flag usati nelle istruzioni condizionali.
- Program Counter : 
- Instruction Pointer : 

**Application Binary Interface**
L'ABI è un insieme di convenzioni software che spiegano come usare i registri, le ABI sono usate dai compilatori in modo da permettere un programma di funzionare in diversi tipi di ISA. Le ABI sono utili anche per capire errori di compilazione, dato che descrivono come verrà tradotta una istruzione dal compilatore.