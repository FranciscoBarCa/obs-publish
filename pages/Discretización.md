Existen varios tipos de discretización

# Dinámicas
![](../assets/Pasted%20image%2020230216230750.png)

# Tipos de discretización
## Transformación Invariante
 Suponer que existe un determinado retenedor a Ia entrada.
- [[Zero order hold]]
## Tranformaciones del tipo s = f(z)
- [[Forward euler]]
- [[Backward euler]]
- [[Regla Trapezoidal]]
# Recomendaciones
## Según periodo de muestreo
⏬Ts → las tres discretizaciones funcionan bien
Medio Ts y PI-> [Regla Trapezoidal](Regla%20Trapezoidal.md)
medio Ts y Control PD / PID
-   La derivada en adelanto puede resultar inestable
-   La regla trapezoidal sigue siendo la **más precisa**
-   Con bajo filtrado, la regla trapezoidal puede generar '**ringing**' en el mando
-   Si hay 'ringing', usar la derivada en retraso