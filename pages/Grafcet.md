#Automatizacion 
[Diapos](../assets/AI_Teo_5_Grafcet_2023v1%20(1).pdf)
Se usa para hacer **máquinas de estado**. 
Grafcet es el nombre de la metedologia, no de la programación(SFC).
![[../assets/Grafcet 2023-02-09 09.17.09.excalidraw]]

# Programación
## SFC 
standard Fusion chart -> idioma de IEEE
Graph es un subconjunto de SFC de Siemens.
## Graph
> [!info] Info #card
> FB es equivalente a una clase y cada bloque equivale a una instancia del objeto.
1. Se crea un FB
2. Programar FB
## Elementos fundamentales
### Etapas
![[../assets/Grafcet 2023-02-16 08.04.57.excalidraw]]
#### Etapas activas
La que se está en ese momento
#### Identificador
Frase que describe la situación. Que está haciendo la máquina
Ejemplo: gslowerCamelCase  , gsAbriendo
> [!info] Note: #card
> gs se pone **siempre**. Viene de Grafcet Step

### Transición
![[../assets/Grafcet 2023-02-16 08.11.20.excalidraw]]
#### Lógica
Si se dan las condiciones se va a las siguientes etapas.
**No activa**: No estás en el estado de antes. No estás mirando si se cumple.
**Activa**: Se está mirando su se cumple.
**Ejecuta**: Se cumple y conduce al siguiente estado.
 > [!info] Note: #card
> Además de los típicos de +* y ', tenemos ⏫ y ⏬ flancos de subida y bajada
### Unión
Une una [Etapas](#Etapas) con una [Transición](#Transición).
#### Unión de transición.
=============
Divergencia → Se **activan** varias **etapas** a la vez en paralelo.
Convergencia → Hace falta que  **todas** las etapas anteriores estén **activas** para avanzar a la **transición**
#### Unión simple
1 etapa → 1 Transición. No hay caminos alternativos.
#### Unión de selección
Divergencia → 1 Etapa a múltiples transiciones
Convergencia → Múltiples Transiciones a 1 Etapa
### Acciones

#### Accion continua condicionada
Var toma el valor de la condición. 1 Cumple 0 no (o como sea la lógica)
![](../assets/Pasted%20image%2020230223002647.png)