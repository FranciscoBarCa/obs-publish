#Control_Avanzado 
# Formato Serie
$$C(s)=K_{p}*\frac{(1+I*s)}{I*s}*\frac{(1+D*s)}{1+f*D*s}$$

# PI margen de ganancia
![](../assets/Pasted%20image%2020230207112427.png)
# PI margen de fase
	![](../assets/Pasted%20image%2020230207112739.png)

Para una respuesta parecida, el control ajustado por ganancia tiene menor sensibilidad y será más estable.
# PID
![](../assets/Pasted%20image%2020230207114440.png)

![](../assets/Pasted%20image%2020230207123954.png)


# PID con predictor de Smith
[Control PID con proyector de Smith](Control%20PID%20con%20proyector%20de%20Smith.md)
El predictor de Smith del modelo tiene un limitador que empeora la salida respecto a la simulación. Lo que satura es la **pendiente**
![](../assets/Pasted%20image%2020230207124720.png)