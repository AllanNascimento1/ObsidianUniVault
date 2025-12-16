# Definite da Matrici
Grazie alla definizione che abbiamo dato all prodotto matriciale possiamo associare a ogni matrice $A$ (tipo m,n) una funzione $T_A(x)$ con dominio $K^n$ (Insieme della variabile indipendente "x") e codominio $K^m$ (Insieme di arrivo, non necessariamente tutti i vettori del codominio sono raggiungibili da $T_A$).
$$T_A(x)=Ax,\forall x\in K^n$$
Come nelle funzioni che abbiamo visto nelle basi, la variabile $x$ è la $n$-upla che indica le coordinate di un vettore, che nel caso della base canonica le coordinate di un vettore **sono** le sue componenti, allora possiamo dire che la funzione $T_A$ trasforma vettori nella base canonica in vettori definiti dal insieme generatore formato dai vettori colonna di $A$. Ad esempio
$$
A=
\left[\begin{align*}  
2\quad {0}\quad 1\\
0\quad 1\quad 3\\
\end{align*}\right]
\Rightarrow T_A(x_1,x_2,x_3)=(2x_1+x_3,x_2+3x_3)
$$
Questa funzione associa vettori nel spazio a vettori nel piano, i vettori che formano l'immagine di $T_A$ vengono ottenuti dalla combinazione lineare dei tre vettori colona di $A$, cioè $A^1=(2,0)$, $A^2=(0,1)$, $A^3=(1,3)$  
## Proprietà
Una funzione lineare rispetta le proprietà dei oggetti lineari, cioè :
$$T_A(a_1v_1+a_2v_2)=a_1T_A(v_1)+a_2T_A(v_2)$$
La composizione di due funzioni è uguale al prodotto tra le matrici:
$$T_A(T_B(x))=A(Bx)=(AB)x=T_{AB}$$
L'inversa di una funzione $T_A$ è uguale a $T_{A^{-1}}=T_A^{-1}$ 
# Tra due spazi vettoriali
### Definizione 1
Siano $V$ e $V'$ due spazi vettoriali sul campo $\Bbb K$ allora una funzione $T:V\rightarrow V'$ è detta funzione lineare (o operatore, trasformazione, applicazione lineare) se :
$$T(a_1v_1+a_2v_2)=a_1T(v_1)+a_2T(v_2)\quad \forall a_1,a_2\in \Bbb K,v_1,v_2\in V$$
In questa funzione lo spazio $V$ è il dominio e $V'$ è il codominio, mentre l'immagine è il sottoinsieme del codominio raggiungibile dalla funzione :
$$Im(T)=\{v'\in V'\ |\ v'=T(v)\}$$
**Osservazioni su funzioni definite da matrici**: 
1) La dimensione del imagine di una funzione è $dim(Im(T_A))=rg(A)$
2) Il sistema lineare $Ax=b\Rightarrow T_A(x)=b$ cioè il sistema ha soluzione solo se $b\in Im(T_A)$ 
### Definizione 2
Sia $T:V\rightarrow V'$ lineare. Il nucleo/kernel di $T$. indicato con $N(T)$ o $Ker(T)$ è l'insieme controimmagine (sottoinsieme del dominio) del vettore nullo : 
$$N(T)=\{v\in V\ |\ T(v)=0\}$$
Cioè il nucleo di $T$ è un sottospazio del dominio che viene trasformato nel vettore nullo dalla funzione lineare $T$.
**Osservazioni su funzioni definite da matrici**: 
1) Si nota che il nucleo ha dimensione $n-rg(A)$, allora :
$$dim(N(T_A))+dim(Im(T_A))=(n-rg(A))+rg(A)=n$$
## Proposizione 1
Se $T:V\rightarrow V'$ è lineare, allora $N(T)$ è un sottospazio di $V$ e $Im(T)$ è un sottospazio di $V'$.
## Proposizione 2
Una funzione $T$ è iniettiva se e solo se $N(T)=\{0\}$. E' suriettiva se e solo se $Im(T)=V'$.
# Matrici associate a funzioni lineari
Sia $T:V\rightarrow V'$ lineare una funzione già definita e siano $B=\{u_1,...,u_n\}$ e $C=\{v_1,...,v_m\}$ basi fissate di $V$ e $V'.$ Siano $T_B:V\rightarrow\Bbb K^n$ e $T_C:V'\rightarrow \Bbb K^m$ gli isomorfismi ottenuti associando ad ogni vettore le sue coordinate rispetto alla base fissata. Essi determinano univocamente una matrice $A=[a_{ij}]\in M_{m,n}(\Bbb K)$, mediante le relazioni.
$$T(u_j)=a_{1j}v_1+a_{2j}v_2+...+a_{mj}v_m$$
Da questa definizione ci sono alcuni concetti fondamentali :
#### Cosa sono $V$ e $V'$ ?
$V$ e $V'$ sono spazi vettoriali qualunque, dove $V$ è il dominio della funzione e $V'$ il codominio, non l'immagine. Per le funzioni lineari è importante notare che i vettori in $V$ e $V'$ possono "vivere" in altri spazi vettoriali facendo in modo che la funzione $T:V\rightarrow V'$ prenda vettori di $V$ che hanno più componenti di quello che si aspetta e che ritorni vettori di $V'$ con la stessa caratteristica. 

**Esempio**: se $B=\{v_1,v_2,v_3\}\in R^5$ e $C=\{u_1,u_2\}\in R^3$ in questo caso $T:V\rightarrow V'$ dove $V$ è un spazio in $R^5$ mentre $V'$ è un piano nel spazio, allora $T(x)$ è un vettore $v'=(x_1,x_2,x_3)\in V'\in \Bbb R^3$ che prende come $x$ un vettore $v=(x_1,x_2,x_3,x_4,x_5)\in V\in \Bbb R^5$. 
Si può vedere che $n=3$ (numero vettori in $B$) è diverso da 5 (numero componenti di $v\in V$) e analogamente $m=2\neq 3$, $n$ e $m$ sono invece i numeri di componenti nelle **Coordinate** di $v$ e $v'$ ottenute dagli isomorfismi $T_B:V\rightarrow\Bbb K^n$ e $T_C:V'\rightarrow \Bbb K^m$.
#### Cosa è $T:V\rightarrow V'$ ?
Per trovare la matrice $A$ della funzione $T:V\rightarrow V'$ si deve già conoscere $T(b_1),T(b_2),...,T(b_n)$ dove $b_1,...,b_n\in B$, cioè è necessario sapere "come" vengono trasformati i vettori in $B$ a vettori in $V'.$ 
Se invece sono definiti gli isomorfismi  $T_B:V\rightarrow\Bbb K^n$ e $T_C:V'\rightarrow \Bbb K^m$ come nella definizione sopra, allora per trovare la matrice $A$ si può usare anche usare $T:K^n\rightarrow K^m$ che lavora con le coordinate di vettori $v$ e $v'$, cioè prende coordinate di $v\in V$ e le trasforma in coordinate di $v'\in V'$.
#### Cosa prende come incognita $T$ ?
La funzione $T:V\rightarrow V'$ prende vettori appartenenti a $V$ e NON le coordinate di vettori in $V$.
**Esempio**: se $B=\{(1,1,1,1),(1,2,3,4)\}$ allora un vettore $v=$$(x,y)_B=xb_1+yb_2$ dove $(x,y)$ è il vettore coordinate e $(x,y)_B=(xb_1+yb_2)$ è il vettore stesso (che "vive" in un piano in $\Bbb R^4$), allora è sbagliato scrivere $T((x,y))$ cioè che l'incognita della funzione è il vettore coordinate di $v\in V$, ma è giusto scrivere $T((x,y)_B)=T(xb_1+yb_2)=T(v)$ cioè il vettore $v\in V$ stesso.
Se si vuole vedere l'incognita della funzione come le coordinate del vettore $v$ allora si può scrivere $T(x)=T(T_{B^{-1}}(y))$ dove $x\in V$ e $y\in \Bbb R^2$, ricorda che l'isomorfismo $T_B(x)=y$ dove $T_B:V\rightarrow \Bbb R^2$. 
Osservazione: Se $x$ non appartene a $V$ allora l'isomorfismo $T_B(x)$ non ha soluzione quindi la funzione $T(x)$ non ha senso .
## Come si costruisce la matrice $A$
La matrice $A\in M_{mn}(\Bbb K)$ è costruita prendendo come le $n$ colonne i vettori $T_C(T(b_j))$ per $j=1,...,n$. Cioè le colonne di $A$ sono le coordinate dei $n$ vettori immagini dei vettori della base $B$, questo perché si può vedere $T_C(T(b_j))=T_C(T(T_B^{-1}(e_j)))$ dove $e_j$ sono le colonne di $I_n$ base di $K^n$.
### Definizione 3
La matrice $A$ costruita in questo modo è detta matrice associata a $T$ rispetto alle basi $B$ e $C$, e indicata col simbolo $M_B^C(T)$. Se $V=V'$ e $B=C$ allora si scrive $M_B(T)$.
Se $V=K^n$,$V=K^m$ e si scelgono le basi canoniche nei due spazi allora si scrive $M(T)$. Si noti che vale sempre: $M(T_A)=A$.
### Proposizione 3
Sia $T:V\rightarrow V'$ con base $B$ di $V$ e $C$ di $V'$ e sia $A=M_B^C(T)$. Si consideri $v\in V$ e sia $x$ il vettore colonna delle coordinate $x_1,...,x_n$ di $v$ rispetto alla base $B$ allora l'immagine $T(v)$ ha vettore delle coordinate rispetto alla base $C$ date dal prodotto matriciale $Ax$. 
Cioè $Ax=T_C(T(v))$ dove il vettore coordinate $x$ può essere calcolato attraverso $v$ : $x=T_B(v)$ e il vettore stesso $v$ può essere calcolato attraverso le coordinate : $v=T_B^{-1}(x)=x_1b_1+...+x_nb_n$.
### Proposizione 4
Sia $A=M_B^C(T)$. Valgono le seguenti proprietà:
$$T_C(Im(T))=Im(T_A),\ \ T_B(N(T))=N(T_A)$$
Dove $T:K^n\rightarrow K^m$ cioè la funzione che trasforma le coordinate dei vettori in $V$ a coordinate di vettori in $V'$.
