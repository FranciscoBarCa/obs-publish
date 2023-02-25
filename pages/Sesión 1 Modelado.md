#Control_Avanzado
Fernando García-Amorena, Fernando del Pino, Francisco Barragán
  
Hay que modelar dos funciones de transferencia.
## Velocidad de avance de un motor
$$P(s) = \frac{v_{i}(s)\left[ \frac{m}{s} \right]}{u(s) [V]}= \frac{K_{m}}{(1+T_{m}s)(1+T_{f}s)}*e^{- \rho s }$$
Tal que:
- $K_{m}$: Ganancia estática
- $T_{m}$: Constante de tiempo del coche 
- $T_{f}$: Constante de tiempo del filtro. Ya que se filtra la medida de velocidad en un filtro paso bajo. 100ms
- $\rho$: retardo en el mando ~50ms  

Por último el periodo de muestro es de 10ms

## Tensión velocidad lineal
Para sacar el componente de la velocidad de avance se saca la velocidad media entre ambos motores.
$$v(s)=\frac{ v_{izq}+v_{der}}{2}$$
Se puede hacer lo mismo con las tensiones y obtener la tensión común. Se supone que los parámetros de cada motor son iguales por lo que al simplificar queda la misma función de transferencia que para un solo motor.

### Parámetros lineal

$$P(s) = \frac{K_{m}}{(1+T_{m}s)(1+T_{f}s)}= \frac{0.094346}{ (1+0.0601s) (1+0.1s)} $$
$Kp  = 0.094346$
$Tm  = 0.0601$
## Tensión diferencial velocidad angular

Igual que la de avance pero con la difference de vel entre ruedas
$$\omega = \frac{v_{izq}-v_{der}}{R}$$
Donde R es 
### Parámetros giro
$$P(s) = \frac{K_{mg}}{(1+T_{mg}s)(1+T_{f}s)}= \frac{0.85444}{ (1+0.1347s) (1+0.1s)} $$

$K_{mg}= 0.855444$
$T_{mg} = 0.1347$

> [!info] El Tm de la planta de giro es el doble que el de la de avance, por lo que la dinámica será más lenta.
> 

