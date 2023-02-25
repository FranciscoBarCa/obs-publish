Se suele usar el [[Diagrama de Nichols]] y el [Criterio del reverso](Criterios%20de%20estabilidad#Criterio%20del%20reverso) para ver el estable. En caso de cosas raras y problemas, se usa el [Criterio de Nyquist](Criterio%20de%20Nyquist.md).

Se hace usando el [Lazo Abierto](Lazo%20Abierto.md), ya que una buena respuesta en frecuencia en [[lazo abierto]] (G) suele tener una buena repuesta en [[lazo cerrado]] ($\frac{G}{1+G}$)

# Valores clave
## [Margen de fase](Margen%20de%20fase.md)
## [Margen de ganancia](Margen%20de%20ganancia.md)

> [!warning] Importante #card
> Hace falta mirar ambos margenes ya que pueden ser **muy horizontales** y engañar (si cero postivo o cero) o **muy verticales** (polos poco amortiguados)

> [!danger] Very important #card
>En caso de duda/problemas -> usar [[Margen de sensibilidad]]
## [Pulsación de cruce](Pulsación%20de%20cruce.md)
## [Pulsación de oscilación](Pulsación%20de%20oscilación.md)
## [Margen de sensibilidad](Margen%20de%20sensibilidad.md)



# Control PID

## Control P
### Respuesta temporal
🔧 [[Amortiguamiento]]
🧊 [[Rapidez]] impuesta ( aunque tu tranquilo que si ⏫ amort la jodes todo lo que quieras)
🧊  [precisión](Precisión%20en%20regimen%20permanente.md) impuesta
### Respuesta en frecuencia
↕ [Black](Diagrama%20de%20Nichols.md) -> Desplazamos vertical hasta que se consiga el margen de fase deseado. Por tanto, solo podemos los Fm que nos permita la planta(G).
### Criterio de diseño
⏫[Margen de fase](Margen%20de%20fase.md) / [Margen de ganancia](Margen%20de%20ganancia.md) -> ⏫ [[Amortiguamiento]].

## Control PI
📈[precisión](Precisión%20en%20regimen%20permanente.md) -> Error 0 ante escalón(ctes)
G(0) = $\infty$ -> $F(0)=1$ y $F_{d}(0)=0$
### Respuesta temporal
Error 0 de seguimiento

#### Ponderación de referencia
⏫⏫ b -> ⏫⏫ agresivo -> pico inicial de mando le cuesta mucho recuperar -> ⏫ Sobrepaso ⏫ Ts
⏫ b -> ⏫ agresivo el mando con error -> ⏫area del PI -> 
⏬⏬ b -> ⏬ agresivo al error ref -> muy lento u subamortiguado ante escalones

⏫ Ponderación -> ⏫ Velocidad referencia 
⏫ Ponderación ->  ≈ Velocidad perturbación (no ve la ponderación)
### Respuesta en frecuencia
G(0) = $\infty$ -> $F(0)=1$ y $F_{d}(0)=0$
↕ P + ➡[Black](Diagrama%20de%20Nichols.md) -> Retraso de fase
#### Retraso de fase
🐌Respuesta lenta -> respuesta exponencial lenta
**Solución** -> Ponderación
#### Ponderación de referencia
Es de lazo cerrado, así que no se nota en el [Lazo Abierto](Lazo%20Abierto.md)(G) del [Black](Diagrama%20de%20Nichols.md)
### Criterio de diseño: 
📉 [Pulsación de cruce](Pulsación%20de%20cruce.md) /[Pulsación de oscilación](Pulsación%20de%20oscilación.md) (contrarrestamos la lentitud intentando acercar con P)
≈ [Margen de fase](Margen%20de%20fase.md) / [Margen de ganancia](Margen%20de%20ganancia.md) $A_{m} \text{ y } \phi_{m}$
## Control PD
### Respuesta temporal
⏫Rapidez/energico.   ≈ Amortiguamiento o ⏫ Amortiguamiento (plantas poco amortiguadas)

⏫ Ruido de medida en el mando! -> Filtrado para mitigar (f)

Si f -> ⏬ Ganancia a alta frecuencia -> ⏬ Ruido alta frecuencia
### Respuesta en frecuencia
Adelanto de fase
### Criterio de diseño
Adelanto de fase ->⏫ [Pulsación de cruce](Pulsación%20de%20cruce.md) / [Pulsación de oscilación](Pulsación%20de%20oscilación.md)
≈ [Margen de fase](Margen%20de%20fase.md) /[Margen de ganancia](Margen%20de%20ganancia.md)
