#Automatizacion 
# Diagrama de contactos
## Entradas
Leen cada entrada cada $Ts$
> [!info] Info #card
> El diagrama representa el estado sin pulsar. Al pulsar se "juntan" las placas

—||— → 1 cierra circuito
—|/|— → 1 abre circuito

> [!warning] Importante #card
> No tiene que ver con el tipo de switch que hay conectado fuera, sino que como se interpreta el 1

### Serie
—||—||— AND
### Paralelo
—||—
—||— OR
## Salidas
—( )—
Escriben en la salida cada $Ts$
### Bobinas con funciones adicionales
#### Set
—(S)— 
1 → Pone a 1 la salida
0 → No hace nada
#### Reset
—(R)— 
1 →Pone a 0 la salida
0 → No hace nada

### Orden de paro.

> [!warning] Todas las órdenes de paro tienen que estar en un contacto normalmente cerrado.  Si una rata se come el cable es como si hubiésemos pulsado el interruptor.
>  --|/|--(R)-- (externamente hay conectado un NC)

## Funciones
> [!warning] Importante #card
> Es recomendable poner solo una fución por linea. 

> [!danger] Very important #card
> No se ejecutan todas en paralelo, sino secuencialmente.

 En el peor de los casos, si cuelga el sistema, salta el WatchDog para obligar a escribir en $T_{s}$.


