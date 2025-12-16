# Definizione per Matrici $2\times 2$
La formula per calcolare il determinante è legata alla inversione di una matrice quadrata e può essere ricavata se fai la moltiplicazione tra due matrici $2\times2$ che risulti nella matrice identica (cioè $AA^{-1}=I_2$).
Infatti troverai che :
$$A^{-1}=\frac{1}{D}
\left[\begin{align*}  
d\quad {-b}\\
{-c}\quad a\\
\end{align*}\right] \quad D=ad-bc$$
Quindi esiste un valore $D=ad-bc$, se $D=0$ allora non esiste una matrice inversa di $A$ dato che la divisione sarebbe impossibile. Dato che per invertire una matrice quadrata $n\times n$ il rango della matrice deve essere uguale ad $n$ allora se $D\neq 0\iff rg(A)=2$.
## Significato Geometrico
In $V^2$ sia $v_1,v_2$ vettori in $\Bbb R^2$ allora $det([v_1\ v_2]) = det\left[\begin{align*}  x_1\quad x_2\\ y_1\quad y_2\\\end{align*}\right]$ è uguale all area con segno del parallelogramma di lati $v_1$ e $v_2$, il segno del determinante dipendente dall'orientazione dei due vettori.
In $V^3$ il determinante di 3 vettori in $\Bbb R^3$ $det[v_1\ v_2\ v_3]$ risulta nel volume con segno del parallelepipedo di lati $v_1,v_2,v_3$, il segno dipende ancora dal orientazione dei vettori.
# Definizione per Matrici quadrate
Sia $A$ una matrice in $M_{n}$ se $n=1$ allora $det(A)=a_{11}$, se $n>1$ allora la matrice viene definita ricorsivamente nel seguente modo :
$$det(A)=\sum_{i=1}^{n}a_{i1}(-1)^{i+1}det(A_{i1})$$
dove $A_{ij}$ è la matrice di ordine n-1 ottenuta da $A$ cancellando la $i$-esima riga e la $j$-esima colonna. Lo scalare $(-1)^{i+j}det(A_{ij})=a_{ij}'$ è detto **Complemento Algebrico** dell elemento $a_{ij}$.
**Fatti Generali** : Se $A$ è triangolare alta allora $det(A)=a_{11}a_{22}...a_{nn}$ cioè la determinante è uguale al prodotto tra gli elementi nella diagonale, in particolare $det(I_n)=1$ e $det(S)=0$ se $S$ è a scalini con rango minore di $n$.
## Proprietà
1) $det(B)=-det(A)$ se $B$ è ottenuto scambiando due righe di $A$.
2) $det(B)=c*det(A)$ se $B$ è ottenuto moltiplicando una riga di $A$ per un scalare $c$.
3) $det(B)=det(A)$ se $B$ è ottenuto sommando un multiplo di una riga di $A$ ad un altra riga di $A$.
4) Se una matrice $A$ ha due righe uguali allora $det(A)=0$
5) Se una riga di $A$ ha tutti zeri allora $det(A)=0$
6) Se $A$ ha ordine $n$ allora $det(kA)=k^ndet(A)$
## Proposizione 1
Possiamo interpretare le proprietà 1,2 e 3 in base alle matrici elementari, cioè che $B=EA$ dove $E$ è una matrice elementare. Questo ci permette di determinare i valore del determinante delle matrici elementari e notiamo l'uguaglianza $det(EA)=det(E)det(A)$, se viene applicata $k$ volte abbiamo :
Sia $A'=(E_k...E_2E_1)A$ con $E_1,...,E_k$ matrici elementari allora $det(A')=det(E_k)...det(E_2)det(E_1)det(A)$.
Se $A'=S$ dove $S$ è a scalini allora se $det(A)\neq 0$ anche $det(S)\neq 0$ e quindi $rg(A)=n$. Quidi vale la seguente proprietà:
7) $det(A)\neq 0\iff rg(A)=n\iff A$ è invertibile.
## Teoremi
**Teorema Di Binet** : Sia $A,B$ matrici di ordine $n$ allora $det(AB)=det(A)det(B)$. Se $A$ è invertibile allora vale anche $det(A^{-1})=1/det(A)$.
**Teorema 2** : Attraverso il teorema di Binet si può anche dimostrare che per ogni matrice quadrata $A$, si ha che $det(A)=det(A^T)$ cioè che le proprietà viste prima valgono anche se applicate alle colonne di $A$.
**Teorema di Laplace** : Sia $A$ una matrice di ordine n allora $det(A)$ può essere calcolato "sviluppando" il determinante secondo una riga o una colonna qualunque.
