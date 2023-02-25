#Control_Avanzado #modelado
Todas las señales se pueden descomponer en senoidales usando fourirer.
 De esta forma conseguimos el espectro de frecuencias de la señal.

 La frecuencia máxima que se puede tener en una señal es la mitad del periodo de muestro, la frecuencia de muestreo. Las frecuancias de nuestra señal han de estar debajo de esta frecuancia, en la banda base

 Si muestreamos una frecuencia por encima de la banda base crea una frecuencia dentro de la banda base
 $|f-n* f_s|$
 Ej muestreo una señal de 0.6 Hz con una frecuencia de muestro de 1Hz se ve una señal de 0.4 ($|-0.4| Hz$)
-
## Implicaciones
 ruido de 50Hz del sensor dentro de un control de temp con Ts 1Hz
 La frecuencia base es hasta 0.5Hz
 $$|50-n*1Hz|=0$$
 Provoca un error de  regimen permanente en la salida, la cual no se puede filtrar dentro del control PI.
 Ya que realmente no existe esta perturbación estamos empeorando en control.
## Solución: [[Filtro Anti-aliasing]]
