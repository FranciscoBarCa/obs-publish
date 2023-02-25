---
aliases: estimador del vector de estado, estimación de estado
---

# How it works
   La medida directa del estado puede requerir de un **número excesivo de sensores**
   ⏫ Sensores → ⏫ Coste ⏬ Fiabilidad(se rompen)
   
## Estimación de estado en lazo abierto
No se miden/comparan las salidas → No sabemos cómo de bien estamos haciendo → simulador para sacar las salidas
**Simulador** en tiempo discreto de la representación de estado de la planta que utiliza como entradas los mandos calculados por el control y, en algunos casos, las perturbaciones conocidas.
## Estimadores de estado en lazo cerrado u observadores
![Observadores de estado](Observadores%20de%20estado.md)

# Usos
[[Observador de Luenberger]]
[[Filtro de Karman]]