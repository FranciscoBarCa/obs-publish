   

Conjunto de variables cuyo valor en un **instante concreto** $t_{0}$ que permite calcular **la salida futura** a partir de ese instante si **se conoce la entrada futura** a partir de ese instante. -> [Representación de Estado](Representación%20de%20Estado.md)
/note
![](../assets/Pasted%20image%2020230216221305.png)
En [Representación de Estado](Representación%20de%20Estado.md) el vector de estado representa el conjunto de [Variables de estado](Representación%20de%20Estado.md#Variables%20de%20estado) que se usan para modelar el sistema.

> [!info] Note: #card
> La elección de vector de estado no es **unica**, hay infinitas posibilidades.

# Normas 
## Debe de poder medirse la variable

## Debe de tener el menor ruido posible
[estimador de estado](estimador%20de%20estado.md) en caso de que tengamos mucho ruido
## Entrada no puede ser variable de estado
Ninguna variable del vector $\vec{U}$ puede estar en $\vec{X}$
## Variables linealmente independientes.

## Número de variables de estado
Existen diferentes formas de ver el número de variables de estado necesarias para un sistema.

### Elementos que almacenan energía
Condensadores y bobinas. Vc Ic
Energía potencial. -> xi
> [!info] Note: #card
> Los sistemas estáticos no requieren de variables de estado. Ej circuito resistivo
### Orden del denominador en funciones de transferencia u/y

