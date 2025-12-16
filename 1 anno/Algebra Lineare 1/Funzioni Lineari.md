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
Sia $T:V\rightarrow V'$ lineare, siano $B=\{u_1,...,u_n\}$ , $C=\{v_1,...,v_m\}$ basi fissate di $V$ e $V'.$ Siano $T_B:V\rightarrow\Bbb K^n$, $T_C:V'\rightarrow \Bbb K^m$ gli isomorfismi ottenuti associando ad ogni vettore le sue coordinate rispetto alla base fissata. Essi determinano univocamente una matrice $A=[a_{ij}]\in M_{m,n}(\Bbb K)$, mediante le relazioni 
$$T(u_j)=a_{1j}v_1+a_{2j}v_2+...+a_{mj}v_m$$
Da questa definizione ci sono alcuni concetti che devono essere rivisti:
La prima è che i vettori di $B$ e $C$ possono appartenere a qualunque spazio vettoriale, cioè $B=\{v_1,v_2,v_3\}\in R^3$ e $C=\{u_1,u_2\}\in R^3$ in questo caso $T:V\rightarrow V'$ dove $V$ è tutto lo spazio $R^3$ mentre $V'$ è un piano nel spazio, quindi $T(x)$ prende vettori nel spazio e li trasforma in vettori nel piano.
Un altro concetto è cosa prende la funzione e cosa restituisce: 
1) La funzione prende vettori appartenenti a $V$ e NON le coordinate di vettori in $V$, esempio: se $B_{2x4}=\{(1,1,1,1),(1,2,3,4)\}$ allora un vettore $w\in B=$$(x,y)_B=xb_1+yb_2$ dove $(x,y)$ è il vettore coordinate e $xb_1+yb_2$ è il vettore stesso, allora è sbagliato scrivere $T((x,y))$ ma è giusto $T((x,y)_B)=T(xb_1+yb_2)$, che si può scrivere come $T(x)=T(T_{B^{-1}}(y))$ dove $x$ è il vettore stesso e $y$ le sue coordinate $T_B(x)=y$. Se $x$ non appartene a $V$ allora  $T_B(x)$ non ha soluzione quindi $T(x)$ non ha senso.
2) 