#Control_Avanzado #modelado 
   

 ### Error de seguimiento nulo
 Si hay integrador no hay error -> si viene del infinito de arriba hay un integrador.
 ### Error nulo en perturbaciones
 No podemos decir ya que no sabemos si está en C o P para que sea cero tiene que estar en C.
 ## Diseño por respuesta en frecuencia
 filtrado
 $$C(s) = K_p (\frac{1+Is}{Is})(\frac{1+Ds}{1+fDs})$$
-
 ponderacion de referencia
 $$C(s) = K *(b +Tds +\frac{1}{Ti s})$$
 ### Componente proporcional
 sube  en vertical el diagrama
 mayor marg fase ->menor K | menos rapidez | mayor error (ya que menor K)
 ### Componente integral
 resta fase (retrasa) mueve a la izquierda
 wopi (~0.8 wo)< wo
 Lo usamos para anular error pero el retraso de fase hace la respuesta más lenta (5- 6 grados)
-
 La respuesta inicial suele ser rápida pero al usar  retrasar poco causamos que la acción itegral tarde mucho en estabilizar
 ### C0mponente diferencial
 ### Control PID
-
 $$C(s) = K_p (\frac{1+Is}{Is})(\frac{1+Ds}{1+fDs})$$
 Integral -> Eliminar error de seguimiento
 Diferencial -> compensar velocidad I y mejorar velocidad
 $$φ_0=φ_a +φ_r$$
 ### Conversión de serie a paralelo
 .... estan en los programas
-