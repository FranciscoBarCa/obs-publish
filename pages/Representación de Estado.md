#Control_Avanzado #control
 
La representación de estado tiene las sistemas MIMO.
Usado en 
## Variables:
### Entradas
$\vec{U}$ → mandos que se va a usar
### Salidas
$\vec{Y}$ → variables que se van a controlar
### Variables de estado
$\vec{X}$  → Variables auxiliares que se **miden** 
		[[Vector de estado]]
		Malas medidas -> [estimador de estado](estimador%20de%20estado.md)
# Modelos
 En general: Un sistema dinámico se puede modelar apartir de un **instante en concreto** si se sabe el valor del [Vector de estado](Vector%20de%20estado.md) en dicho instante y sabemos los mandos futuros que se le van a aplicar a dicho sistema![[../assets/Representación de Estado 2023-02-16 20.20.45.excalidraw|700]]
 

## Modelo no lineal
![[../assets/Representación de Estado 2023-02-16 22.07.03.excalidraw]]
No se suele usar, en su lugar, se realiza un [Linealizado en punto de operación](Linealizado%20en%20punto%20de%20operación.md) o se usa un [Control Predictivo](Control%20Predictivo.md)
## Modelo lineal LTI
> [!info] Note: #card
> Será el que se use la mayoría de las veces, ya sea porque el sistema es LTI, o porque se está aplicando [Linealizado en punto de operación](Linealizado%20en%20punto%20de%20operación.md)

![[../assets/Representación de Estado 2023-02-16 22.08.34.excalidraw|700]]


### Matriz de transferencia F
Se puede obtener la [Matrices de transferencia](Matrices%20de%20transferencia.md) F(s) apartir de la representación de estado. 
![Matrices de transferencia](Matrices%20de%20transferencia.md)
# Discretización
Para la [[Discretización]] de una representación de estado se suele usar un [ZOH](Zero%20order%20hold.md)
![[../assets/Representación de Estado 2023-02-17 14.37.44.excalidraw]]
El modelo discretuzado usa las matrices Ad Bd Cd Y Dd.
![[../assets/Representación de Estado 2023-02-17 14.42.52.excalidraw]]
> [!warning] Note: #card
> **No confundir las matrices discretas** con las A B C D de [Modelo lineal LTI](#Modelo%20lineal%20LTI)

## MATLAB

``` matlab
Pss_d=c2d(Pss,ts);
Ad=Pss_d.a;
Bd=Pss_d.b;
```
[[Estimador de estado]]


