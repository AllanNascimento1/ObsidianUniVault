I calcolatori sono un insiemi di circuiti che manipolano la corrente elettrica che viene passata come input, se passa corrente vale 1 altrimenti vale 0.
Per rappresentare sequenze di bit in informazioni utili come lettere, numeri, simboli e ecc si deve stabilire una **codifica** che mappa un informazione a una data sequenza di bit.
## Codifica dei numeri Naturali
La rappresentazione dei numeri deve essere più dinamica rispetto a una normale mappa dato che esistono un numero infinito di numeri, allora usiamo il sistema **Binario** invece del sistema decimale.
Per ridurre il numero di cifre per descrivere numeri grandi esistono anche le basi **Ottale** e, la più spesso utilizzata, **Esadecimale**.
### Conversione tra basi
**Base 2 $\iff$ 16** : Prendi gruppi di 4 bit e li traduci in numeri esadecimali e viceversa.
**Base 2 $\iff$ 8** : Prendi gruppi di 3 bit e li traduci in numeri ottali e viceversa.
**Base 2 $\implies$ 10** : Si moltiplica ogni cifra $c_i$ per $2^i$ dove $i$ è la posizione di $c$.
**Base 10 $\implies$ 2** : Si ripete iterativamente finché x è 0. 
- Si divide il numero decimale per 2
- Il resto viene preso e messo a sinistra del risultato.
- Il quoziente viene assegnato ad x
## Codifica numeri Interi (con segno)
Per codificare numeri negativi abbiamo diverse possibilità:
- Modulo e segno
- Complemento a 1
- Complemento a 2
#### Modulo e segno 
Si usa il bit più a sinistra per determinare il segno, ma può rappresentare solo la metta dei numeri e ha due codifiche per lo zero.
#### Complemento a 1 
Anche questa opzione usa il bit più a sinistra per determinare il segno, ma se il numero è negativo esso viene rappresentato con il complemento a 1 del valore assoluto. Per calcolare il complemento a 1 di un numero inverto ogni bit da 1 a 0 e viceversa. Anche questa opzione ha due codifiche per il 0.
#### Complemento a 2 (Ca2)
Come il complemento a 1 però si calcola il complemento a 2. Per calcolarlo si parte dal bit più a destra e si scorre a sinistra fino che trovi un 1 e a partire dal bit successivo si fa come nel complemento ad 1.
## Codifica numeri reali
Non tutti i numeri reali possono essere rappresentati, come i numeri irrazionali, usando un numero finito di bit e quindi in alcuni casi dobbiamo accontentarci con una approssimazione del numero reale.
Esistono due modi per rappresentarli, **virgola fissa** e **virgola mobile**
#### Virgola Fissa
Un numero reale su k cifre ha $k-f$ cifre dedicate alla parte intera e f cifre alla parte decimale, il numero reale rappresentato in una sequenza di bit si calcola moltiplicandolo per $2^{-f}$ 
Per convertire un numero reale in base 10 alla base binaria converti la parte intera in binario e la metti a sinistra della virgola, anche la parte decimale viene convertita ma moltiplichi per 2 invece di     dividere e prendi la parte intera a posto del resto, il risultato viene messo a destra della virgola.
Questo tipo di codifica ha il grande svantaggio che non può gestire numeri di grandezze diverse contemporaneamente, dato che la virgola è fissa.
#### Virgola Mobile
Questo è il metodo di codifica dei numeri reali più utilizzato nel mondo che è descritto dal standard **IEEE 754**, i numeri reali vengono rappresentati dalla riscrittura $x=M*2^E$ dove M è la mantissa e E è l'esponente. 
![[Pasted image 20260303150714.png]]
Nel standard IEEE 754 un bit è usato per il segno, otto bit per l'esponente (0-255) e gli altri 23 per la mantissa. La mantissa in questo standard è solo la parte decimale della intera mantissa che cambia in base al esponente, questo esponente è solo una parte del esponente totale :
- Se E > 0 allora i numeri sono **normalizzati** (mantissa con parte intera)
	La intera mantissa è 1.M e l'esponente finale è $E-127$
- Se E = 0 allora i numeri sono **denormalizzati** (mantissa senza parte intera)
	La mantissa è 0.M e l'esponente finale è -126
In questo standard esiste anche codifiche a :
- $\pm\infty$ quando l'esponente è 255 e la mantissa è 0, il bit segno indica il segno del infinità
- NaN (Not a Number) esponente 255 e mantissa diversa da 0.
La conversione è un po' complessa, leggi la seguente slide
![[Pasted image 20260304085509.png]]
## Codifica di Testo
Per codificare un testo in sequenza di bit basta implementare una codifica per i caratteri, l'standard più usato per la codifica dei caratteri è **ASCII** che codifica 127 caratteri in 7 bit (in un byte il bit più significativo è default a 0).
Una codifica di 255 caratteri non bastano per tutte le lingue e diversi simboli usati nel mondo, allora esistono altri standard che codificano caratteri usando 2 o 4 byte, ma sono molto meno efficienti.
## Operazioni
### Somma e Sottrazione
##### Numeri Naturali
Come alle elementari, per la somma se vuoi puoi generare il carry nel seguente modo : 
- Parti ponendo un 0 sopra le due cifre più a destra
- Se le cifre sotto sono 1 e 1 allora a sinistra metti un 1, se sono 0 e 0 metti un 0 altrimenti copy il numero attuale.
- Muoviti a sinistra.
##### Complemento a 1
Per la somma/sottrazione basta sommare i due numeri e sommare il risultato al carry più significativo.
Se i due numeri hanno il bit più a sinistra uguale e il risultato ha il bit più significativo diverso allora è andato in overflow.
#### Complemento a 2
Come per il complemento a 1, basta sommare i due numeri (per la sottrazione basta negare il secondo operando) però non c'è bisogno di fare niente al risultato dopa la somma.
Per determinare un overflow basta fare la stessa verifica del complemento a 1.
### Moltiplicazione
La moltiplicazione/divisione per 2 di un numero binario si chiama **Shifting** dato che basta aggiungere un 0 a destra se moltiplichi e togliere la prima cifra a destra se dividi.
Per la moltiplicazione tra numeri naturali fai come alle elementari.
### Matematica Modulare
La matematica modulare è un tipo di aritmetica che lavora con un numero finito di numeri, se un operazione restituisce un valore al di fuori dei limiti del modulo allora il numero risultante "ritorna" al altro stremo come su un orologio, questa operazione è il **resto** della divisione.
La matematica modulare ci serve per descrivere il comportamento delle operazioni in caso di overflow