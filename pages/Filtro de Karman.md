Es un [estimador de estado](estimador%20de%20estado.md) donde la configuración se consigue de forma estadística

# How it works
## 1. Definimos modelo estocástico con ruido
Añadimos un vecotr de ruido blanco a la definicion del vec de estado
![](../assets/Pasted%20image%2020230216123118.png)
> [!info] Note: #card
> ⏫ fiable medida -> ⏬ Wi
> ⏬ fiable (⏫ ruido)-> ⏫wi

El valor absoluto de los valores de Wi no es importante sino la comparación de los valores.

### Lazo cerrado 
![](../assets/Pasted%20image%2020230216123500.png)
### Variables de estado
![](../assets/Pasted%20image%2020230216123829.png)


## 2. Definimos una función de coste que minimiza el tamaño de la matriz de covarianzas del vector de estado
Función de coste: mínima matriz de covarianza del error de estimación de X[k]
