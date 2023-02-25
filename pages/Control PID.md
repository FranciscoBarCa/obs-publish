#Control_Avanzado #control
- Fácilmente ajustable y robusto
 Solo se puede sistemas SISO una entrada una salida.

### Problemas
 Actua mal ante retardos en el lazo. -> Hace falta ajustar con diseños muy lentos para evitar
 Doble integrador(común para actuar posición con fuerza) -> Hay que
 Polos poco amortiguados(circuitos eléctricos con mucha reactiva muelles con bajas fricciones viscosas)
 Sistemas inestable (equilibrista)
### Soluciones a los problemas
#### Soluciones basadas en PID
- Retardos -> [[Control PID con proyector de Smith]]
- Doble integrador / bajo amortiguamiento -> [[Control PID en cascada]]
- Multivariable -> PID multivariable
#### Usar controles NO PID
- [regulador por realimentación de estado](Control%20por%20realimentación%20de%20estado.md)
- [[Control Predictivo]]
## Respuesta
Todas las funciones de transferencia tienen los mismos polos en lazo cerrado (1+CP) Difieren en los ceros
## Diferencial

## Diseño
 Diseñamos buscando que el sistema no sea inestable (usamos margenes de [[Estabilidad]] )