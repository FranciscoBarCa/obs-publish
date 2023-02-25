
Entradas: Mandos calculados Perturbaciones conocidas y **medidas de las salidas**
Medida de las salidas -> Termino corrector para estimador de estado en lazo abierto
En lazo cerrado → polos del control y polos de la estimación (es decir, la planta) ⇾ reducir la sensibilidad de la estimación a los errores de modelado de la planta.
> [!info] Note: #card
> Los estimadores de lazo cerrado pueden estimar todo el vector de estado (observadores de orden completo) o sólo una parte de él (observadores de orden reducido).

El sistema de control realimenta el estado estimado en lugar del estado medido.
> [!warning] Importante #card
> 


Añadimos la matriz de ganancias Gd para poder cambiar los **polos del observador**
![](../assets/Pasted%20image%2020230216122407.png)

> [!info] Note: #card
> Donde ponemos los polos
> ![[../assets/estimador de estado 2023-02-16 12.25.28.excalidraw]]