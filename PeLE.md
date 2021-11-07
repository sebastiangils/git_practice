# Tarea PeLE
**Ejemplo 1.64** 
 Para el ejemplo anterior, si se sabe que el Sr. Rodríguez fue nombrado gerente de una sucursal de su empresa ¿cuál es la probabilidad de que la empresa haya abierto una sucursal en Montevideo?  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Es claro de la regla de Bayes que:

$$
\begin{align*}
    P(A \mid G) &=\frac{P(A)P(G\mid A)}{P(G)} \\
    &= \frac{0.4 \times 0.8}{0.38} \\  
    &= 0.84211. \blacktriangle 
\end{align*}
$$

**Ejemplo 1.65** La cuarta parte de una pobación está vacunada contra una enfermedad contagiosa. En el trascurso de una epidemia debida a tal enfermedad, se observa que de cada cinco enfermos sólo uno está enfermo. Se quiere calcular la probabilidad de que un no vacunado esté enfermo.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Sean:  
V :=  "La persona está vacunada"  
E :=  "La persona está enferma"  
De acuerdo a la información suministrada se tiene que:  
$$
\begin{align*}
    P ( V\mid E ) &= \frac{1}{5} \\  
    P ( E\mid V ) &= \frac{1}{12}\\  
    P (V) &= \frac{1}{4}.  
\end{align*}
$$

Por lo tanto,  

$$
\begin{align*}
    x :&= P(E \mid V^c)  \\
    &= \frac{P(V^c \mid E)P(E)}{P(V^c)} \\
    &= \frac {\frac{4}{5} (\frac{1}{12}.\frac{1}{4} + \frac{3}{4}x)}{\frac{3}{4}}\\
\end{align*}
$$
de donde se obtiene  
$$x = \frac{1}{9} .\  \blacktriangle$$ 


**Definición 1.66 (distribución a priori y a posteriori)**  
Sea $A_1,A_2$,... una partición finita o numerable de $\Omega$ con $P(A_i)$ > 0 para
todo $i$. Si $B$ es un elemento de $\mathfrak{F}$ con $ P(B) > 0$ , entonces $(P(A_n))_n$ se llama
distribución "a priori", esto es, antes de que suceda $B$, y $(P(A_n \mid B))_n$  se
llama distribución "a posteriori", es decir, después de que sucede $B$.  
  

**Ejemplo 1.67** En una ciudad se llevan a cabo pruebas para detectar cierta
enfermedad. Supóngase que el 1% de las personas sanas son registradas como enfermas, que el 0.1% de la población está realmente enferma y que el
90% de los enfermos son reportados como tales. Se desea calcular la probabilidad de que una persona, seleccionada al azar y reportada como enferma,
esté realmente enferma.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Si se definen los eventos:    
$E := $ "La persona realmente está enferma"  
$T := $ "la persona es reportada como enferma"  

entonces de la información suministrada se sabe que:  
$$
\begin{align*} 
    P(E) &= 0.001 \\
    P(T\mid E^c) &= 0.001 \\  
    P(T \mid E) &= 0.9  
\end{align*}
$$

Por lo tanto, 

$$
\begin{align*}  
    P(E \mid T) &= \frac {P(T\mid E) P(E)}{P(T\mid E^c)P(E^c) + P(T \mid E)P(E)} \\  

    &= \frac {0.9 \times 0.001}{0.01 \times 0.999+0.9 \times 0.001} \\

    &=8.2645 \times 10^{-2} \approx 0.083   
\end{align*}
$$
En este caso:  
$$
\begin{align*}  
\text{Distribución a priori} &= (0.001,0.999)  \\
\text{Distribución a posteriori} &= (0.083,0.917).  \blacktriangle  
\end{align*}
$$
Algunas veces la ocurrencia de un evento $B$ no afecta la probabilidad de
ocurrencia de un evento $A$,esto es,  
$$
\begin{align}
P(A \mid B) = P(A)
\end{align}
$$  
En este caso se dice que el evento $A$ es "independiente" del evento $B$. La
"definición" dada en (1) tiene como inconveniente que sólo es válida si
$P(B) > 0$. Para evitar esta dependencia de la probabilidad del evento $B$, se
asume como definición de independencia la siguiente:  
**Definición 1.68 (eventos independientes)** Dos eventos $A$ y $B$ son independientes, si y sólo si,   
$$P(A \cap B) = P(A) P(B) $$  
En caso contrario se dice que los eventos son dependientes.  
**Ejemplo 1.69** Supóngase que se lanza un dado corriente dos veces consecutivas. Sean:  
$A := $"la suma de los resultados obtenidos es un número par"  
$B := $"el resultado del segundo lanzamiento es par"  
En este caso:  
$$P(A) = P(B) = \frac{1}{2}$$  
Y ademas, $P(A \cap B) = \frac{1}{4}$. Por lo tanto, los eventos son independientes. $\blacktriangle$  


**Ejemplo 1. 70** Se carga un dado de manera que la probabilidad de obtener
un número par es igual ag. Sean A y B como en el ejemplo anterior. En
este caso se tiene que:  

$$
\begin{align*}
    P(A) &= \frac{13}{25} \\ 
    P(B) &= \frac{2}{5} \\
    P(A \cap B) &= \frac{4}{25} \\  
\end{align*}
$$ 
por lo tanto, $A$ y $B$ no son independientes.  $\blacktriangle$  

**Nota 1.71** Un error, que a menudo se comente, es asegurar que los eventos son independientes si son mutuamente excluyentes. Observe que esto
no es cierto. Por ejemplo, si se lanza una moneda corriente una vez y se
consideran los eventos:  
$A := $"el resultado obtenido es cara"  
$B :=$ "el resultado obtenido es sello"   
entonces, es claro que, $A$ y $B$ son mutuamente excluyentes. Sin embargo no
son independientes, pues  
$$0= P(A \cap B)  \not = \frac{1}{4} = P(A)P(B).$$  

**Teorema 1. 72** Sean $A$ y $B$ eventos independientes. Entonces: 

1. $A$ y $B^c$ son independientes (y por simetría $A^c$ y $B$ son independientes).  
1.  $A^c$ y $B^c$ son independientes.  


**Demostración.**  

1.  
$$
\begin{align*}
P(A) &= P(A \cap B^c) + P(A \cap B) \\  
&= P(A \cap B^c) + P(A)P(B)  
\end{align*}
$$    

por lo tanto,  

$$P(A \cap B^c) = P(A)[1 - P(B)] = P(A)P(B^c)$$  

2.  
$$
\begin{align*}
P(A^c \cap B^c) &= 1 - P(A \cup B) \\  
&= 1 - P(A) - P(B) + P(A \cap B) \\  
&= 1 - P(A) - P(B) - P(A)P(B) \\
&= [1- P(A)][1 - P(B)] \\
&= P(A^c)P(B^c) \\  
\end{align*}
$$  
$\blacksquare $   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; En muchos casos se requiere analizar la independencia de dos o más
eventos, por ello es necesario generalizar el concepto de independencia dado.  
**Definición 1. 73 (familia independiente)** Una familia $\{A_i : i \in I\}$ de
eventos se dice independiente si:  
$$ P(\bigcap_{i \in J} A_i ) = \prod_{i \in J} P(A_i)  $$   
para todo subconjunto finito $J$ de $I$. 
