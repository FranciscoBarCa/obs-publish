#Control_Avanzado #control

En un PID normal tenemos el siguiente diagrama:
![image.png](../assets/image_1674733385697_0.png)

El $e$ del denominador genera infinitos polos y empeora mucho la respuesta.
Nuestro objetivo es eliminar este retardo del denominador para así eliminar la horizontalidad del diagrama de Black del lazo abierto
![image.png](../assets/image_1674733498308_0.png)

Para ello se usa el:
# Predictor de Smith

Para arreglar el retardo añadimos al control una capacidad predictiva. En la ducha, si sabemos cómo se comporta nuestra ducha podemos ajustar fácilmente la temp.

Modificamos la planta del control

![image.png](../assets/image_1674733613234_0.png)

Al añadir este nuevo camino eliminamos el retardo de la F de transferencia en lazo cerrado.

![image.png](../assets/image_1674733712295_0.png)

> [!tip] Los gorritos, es decirlas predicciones afectan mucho al resultado.

La suma de los dos caminos u y la entrada de C es P
La P que usamos para la realimentación es una predicción $\hat{P}$

## Error al estimar el retardo.

![image.png](../assets/image_1674735036087_0.png)

## Simulador

> [!danger] HAY QUE  DISEÑAR EL CONTROL CON LA PREDICCIÓN de la planta

[Carpeta Matlab](file://C:/SyncThing/LogSeqNotes/matlab)

> [!tip] Ojo usar el ==tipo== de Control PID que te piden

## Ejemplo
### Planta:

![image.png](../assets/image_1674733993789_0.png)

$P_1 =\frac {1}{0.2s+1}$
$P_2 = -e^{\phi s}$
## Control PID
### Por margen de fase

![image.png](../assets/image_1674734400186_0.png)

Como es muy horizontal, aunque el margen de fase está bien, el margen de ganancia es muy malo y la respuesta es muy mala.
### Por margen de ganancia

[!image.png](../assets/image_1674734549769_0.png)

Mucho mejor pero ==muy== lento.
### Predictor de Smith
Sería igual pero poniendo $P_2=1$
### Comparación

![image.png](../assets/image_1674734807778_0.png)

El MCU es el [[Control Predictivo]]