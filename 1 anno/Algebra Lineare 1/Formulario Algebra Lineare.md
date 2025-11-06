## Vettori Geometrici
#### Vettore ottenuto da due punti
$\vec v=\vec {AB}=(B_1-A_1,B_2-A_2,B_3-A_3) = (v_1,v_2,v_3)$ 
#### Moltiplicazione Scalare
$t*(\vec v)=(t*v_1,t*v_2,t*v_3)$ 
#### Somma / Sottrazione
$\vec v+\vec w=(v_1+w_1,v_2+w_2,v_3+w_3)$ 
$\vec {AB}+\vec{CD}=(B_1-A_1+D_1-C_1,B_2-A_2+D_2-C_2,B_3-A_3+D_3-C_3)$ 

$\vec v-\vec w=\vec v+(-1*\vec w) = (v_1-w_1,v_2-w_2,v_3-w_3)$ 
#### Prodotto Scalare (Euclideo /Forma canonica)
$\vec v*\vec w=v_1*w_1+v_2*w_2+v_3*w_3$ 
Questo è uguale a:
$\vec v*\vec w=|\vec w||\vec v|cos(\alpha)$ 
#### Prodotto Vettoriale
$\vec v\times\vec w=(v_2*w_3+v_3*w_2,v_1*w_3+v_3*w_1,v_1*w_2+v_2*w_1)$ 
#### Distanza tra due punti (Lunghezza di un vettore)
Distanza tra i due punti $A,B$
$$dist(A,B)=\sqrt{(B_1-A_1)^2+(B_2-A_2)^2+(B_3-A_3)^2}$$
Questo significa anche che:
$$Lunghezza(\vec v)=||\vec v||=\sqrt{(v_1)^2+(v_2)^2+(v_3)^2}$$
#### Normalizzazione di un vettore
Normalizzare un vettore significa ottenere un vettore con la stessa direzione ma di lunghezza 1.
$$\vec n=\frac{\vec v}{||\vec v||}$$
#### Proiezione di un vettore sul altro
La proiezione di $\vec w$ sul vettore $\vec v$:
$$pr_{\vec v}(\vec w)=\frac{\vec v*\vec w}{||\vec v||}*\frac{\vec v}{||\vec v||}$$ 
Dato che $\frac{\vec v*\vec w}{||v||}$ è la lunghezza del vettore proietto, mentre $\frac{\vec v}{||\vec v||}$ è il vettore $\vec v$ normalizzato.
## Rette
#### Trovare Eq. Parametrica da un punto e un vettore parallelo
$A=(A_1,A_2,A_3)$  e  $\vec v=(v_1,v_2,v_3)$ 
$$  
r:\left\{\begin{align*}  
x &= A_1 + tv_1\\  
y &= A_2 + tv_2\\
z &= A_3 + tv_3
\end{align*}\right.
$$
#### Trovare Eq. Parametrica da due punti
$A=(A_1,A_2,A_3)$  e  $B=(B_1,B_2,B_3)$ 
calcoli il vettore direzione della retta 
$\vec v=\vec {AB}=(B_1-A_1,B_2-A_2,B_3-A_3)$ 
$$  
r:\left\{\begin{align*}  
x &= A_1 + tv_1\\  
y &= A_2 + tv_2\\
z &= A_3 + tv_3
\end{align*}\right.
$$
#### Equazione Parametrica a Eq. Cartesiana e vice versa
**Eq. Para -> Eq. Cart**
$$  
r:\left\{\begin{align*}  
x &= x_1 + t(\vec v_1)\\  
y &= y_1 + t(\vec v_2)\\
z &= z_1 + t(\vec v_3)
\end{align*}\right.
$$
Dove $\vec v=( (x_2-x_1) , (y_2-y_1) , (z_2-z_1) )$ è il vettore direzionale della retta
Isoli una $t$, quella più facile:
$$  
r:\left\{\begin{align*}  
t &=\frac{1}{\vec v_1}x-\frac{x_1}{\vec v_1}\\  
y &= y_1 + t(\vec v_2)\\
z &= z_1 + t(\vec v_3)
\end{align*}\right.
$$
Sostituiscila dentro le altre equazioni lineari il valore di t:
$$
r:\left\{\begin{align*}
y &= y_1 + (\frac{1}{\vec v_1}x-\frac{x_1}{\vec v_1})(\vec v_2)\\
z &= z_1 + (\frac{1}{\vec v_1}x-\frac{x_1}{\vec v_1})(\vec v_3)
\end{align*}\right.
$$
$$
r:\left\{\begin{align*}
y &= y_1 + (\frac{\vec v_2}{\vec v_1}x-\frac{\vec v_2*x_1}{\vec v_1})\\
z &= z_1 + (\frac{\vec v_3}{\vec v_1}x-\frac{\vec v_3*x_1}{\vec v_1})
\end{align*}\right.
$$
$$
r:\left\{\begin{align*}
\vec v_1y &= \vec v_1y_1 + \vec v_2x-\vec v_2x_1\\
\vec v_1z &= \vec v_1z_1 + \vec v_3x-\vec v_3x_1
\end{align*}\right.
$$
Dopo aver semplificato tutto, otterrai due equazioni lineari che definiscono la retta:
$$
r:\left\{\begin{align*}  
b_1y+a_1x&=d_1\\
c_2z+a_2x&=d_2
\end{align*}\right.
$$
**Eq.Cart -> Eq.Para**
$$
r:\left\{\begin{align*}  
b_1y+a_1x&=d_1\\
c_2z+a_2x&=d_2
\end{align*}\right.
$$
Prendi uno dei componenti, e scambialo con $t$:
$$
r:\left\{\begin{align*}
x&=t\\
b_1y&=d_1-a_1t\\
c_2z&=d_2-a_2t
\end{align*}\right.
$$
Isola le componenti e se necessario sostituisci il valore degli altri componenti nel altra equazioni in modo che riesci a isolare le componenti:
$$
r:\left\{\begin{align*}
x&=t\\
y&=\frac{d_1}{b_1}-\frac{a_1}{b_1}t\\
z&=\frac{d_2}{c_2}-\frac{a_2}{c_2}t
\end{align*}\right.
$$
#### Determinare un punto qualsiasi nella retta
Trovare eq. parametrica della retta. 
sostituire $t$ nel sistema con il valore che vuoi e determina i componenti del punto.
#### Determinare se un punto appartiene ad una retta
Trovare eq. cartesiana, sostituire i componenti del sistema con quelli del punto e vedere se il sistema è vero.
#### Trovare vettore direzionale di una retta
Trovare la equazione parametrica della retta e prendere i coefficienti di $t$.
$\vec v=(a,b,c)$
$$  
r:\left\{\begin{align*}  
x &= A_1 + at\\  
y &= A_2 + bt\\
z &= A_3 + ct
\end{align*}\right.
$$
#### Trovare un vettore ortogonale alla retta (solo in $V^2$)
Trovare la equazione cartesiana della retta e prendere i coefficienti di x,y,z.
$\vec n=(a,b)$
$$  
r:ax+by+c=0
$$
#### Distanza tra un punto e una retta
Dato: $P$ e $r=O+t\vec v$ 
(1) Trovi il piano ortogonale ad $r$ : $\pi:v_1x+v_2y+v_3z+d=0$
(2) Sostituisci P nel equazione di $\pi$ e trovi il valore di $d$.
(3) Fai l'intercessione tra $r$ e $\pi$, per trovare il punto B sulla retta.
$$  
B:\left\{\begin{align*}
&v_1x+v_2y+v_3z+d=0\\
&x=O_1+v_1\\
&y=O_2+v_2\\
&z=O_3+v_3
\end{align*}\right.
$$
(4) Trovi la distanza tra P e B
$$dist(P,B)=\sqrt{(B_1-P_1)^2+(B_2-P_2)^2+(B_3-P_3)^2}$$
#### Distanza tra due rette (Sghembe)
Dato: $r=O_r+t\vec v_r$ e $s=O_s+t\vec v_s$ 
Il modo più facile è:
(1) Trovare il prodotto vettoriale tra $\vec v_r$ e $\vec v_s$ : $\vec v_r\times\vec v_s$ 
(2) Trovare un vettore qualsiasi tra un punto in $r$ e uno in $s$ : $\overrightarrow{O_rO_s}$ 
(3) Calcolare la lunghezza del vettore $\overrightarrow{O_rO_s}$ su $\vec v_r\times\vec v_s$ :
$$||pr_{\vec v_r\times\vec v_s}(\overrightarrow{O_rO_s})||=\frac{\overrightarrow{O_rO_s}*(\vec v_r\times\vec v_s)}{||\vec v_r\times\vec v_s||}$$
## Piani
#### Trovare Eq. Parametrica dato un punto e due vettori
Punto : $A$ 
vettori: $\vec v,\vec w$ 
$$  
\pi:\left\{\begin{align*}  
x &= A_1 + tv_1 + sw_1\\  
y &= A_2 + tv_2 + sw_2\\
z &= A_3 + tv_3 + sw_3
\end{align*}\right.
$$
#### Trovare Eq. Parametrica dato 3 punti
Punti: $A,B,C$

Trovi i due vettori : $\vec {AB}=\vec v$ e $\vec {AC}=\vec w$ 
$$  
\pi:\left\{\begin{align*}  
x &= A_1 + tv_1 + sw_1\\  
y &= A_2 + tv_2 + sw_2\\
z &= A_3 + tv_3 + sw_3
\end{align*}\right.
$$
#### Eq. Para a Eq. Cart e vice versa
**Eq. Para -> Eq. Cart**
$$  
\pi:\left\{\begin{align*}  
x &= A_1 + tv_1 + sw_1\\  
y &= A_2 + tv_2 + sw_2\\
z &= A_3 + tv_3 + sw_3
\end{align*}\right.
$$
Come nelle rette isoli la $t$ e sostituiscila dentro le altre due equazioni.
$$  
\pi:\left\{\begin{align*}  
t&=\frac{x-A_1-sw_1}{v_1}\\  
y &= A_2 + (\frac{x-A_1-sw_1}{v_1})v_2 + sw_2\\
z &= A_3 + (\frac{x-A_1-sw_1}{v_1})v_3 + sw_3
\end{align*}\right.
$$
Dopo dovrai ripetere il processo con la $s$.
$$  
\pi:\left\{\begin{align*}  
s &= \frac{y - A_2}{w_2} - \frac{(x-A_1-sw_1)v_2}{v_1w_2}\\
z &= A_3 + (\frac{x-A_1-sw_1}{v_1})v_3 + (\frac{y - A_2}{w_2} - \frac{(x-A_1-sw_1)v_2}{v_1w_2})w_3
\end{align*}\right.
$$
Se riduci tutti i valori noti otterrai una singola equazione lineare, che è la eq. cartesiana del piano in $V^3$ :
$$ax+by+cz+d=0$$
**Eq. Cart -> Eq. Para**
Sostituisci a $x$ la $t$, e ad $y$ la $s$.
$$  
\pi:\left\{\begin{align*}  
x &= t\\  
y &= s\\
a&t+bs+cz+d=0
\end{align*}\right.
$$
Trovi la z
$$  
\pi:\left\{\begin{align*}  
x &= t\\  
y &= s\\
z &= -\frac{d}{c}-\frac{a}{c}t-\frac{b}{c}s
\end{align*}\right.
$$
#### Determinare un punto qualsiasi nel piano
Trovare eq. parametrica del piano. 
sostituire $t$ e $s$ con i valori che vuoi (Più facile sostituire $t=0$ e $s=0$, che è il punto di origine del' piano) nel sistema e determina i componenti del punto.
#### Determinare se un punto appartiene a un piano
Trovi l'equazione cartesiana del piano e sostituisci i valori dei componenti, se la equazione lineare è vera il punto appartiene al piano, altrimenti no.
#### Distanza di un punto dal piano
Trovare la equazione cartesiana del piano.
$$  
\pi:ax+by+cz+d=0
$$
Usare la formula :
$dist(P,\pi)=\frac{|aP_1+bP_2+cP_3+d|}{\sqrt{a^2+b^2+c^2}}$ 
Cioè il rapporto tra la lunghezza del vettore normale del piano, e il vettore formato del punto P.
#### Trovare vettore ortogonale al piano
Trovare Eq. Cart del piano
$$\pi:ax+by+cz+d=0$$
il vettore ortogonale puo essere ricavato prendendo i coefficienti di $x,y,z$ : $\vec n=(a,b,c)$ 
## Matrici
