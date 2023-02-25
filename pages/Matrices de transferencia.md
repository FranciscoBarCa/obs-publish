---
aliases: matriz de transferencia
---

$$
\vec{Y}(s)= F(s)\vec{U}(s)
$$
> [!info] Note: #card
> equivalente de la **Planta (P(s))** en sistemas SISO 

Matriz de funciones de transferencia que relacionan entradas con salidas en un [MIMO](Plantas%20MIMO.md)
![|400](../assets/Pasted%20image%2020230216222510.png)
# Representación de estado LTI
Para el modelo de [Representación de Estado](Representación%20de%20Estado.md) se puede sacar la Planta F(s)
Se puede obtener la [Matrices de transferencia](Matrices%20de%20transferencia.md) F(s) apartir de la representación de estado. 
![|400](../assets/Pasted%20image%2020230216222720.png)

> [!info] Note: #card
> No confundir con F(X,U) de [Modelo no lineal](#Modelo%20no%20lineal)

**Por tanto queda**: 	$$F(s) = C(sI-A)^{-1} B$$
> $$
Y(s)= (C(sI-A)^{-1} B ) * U(s)
$$
```
P_tf = tf(P_ss)
 P_tf(i,j) # => función de transferencia Uj =>Yi
```

## Autovalores de la matriz de transferencia

Se pueden ver los autovalores de varias formas
 - Son los autovalores de A
 ```matlab
 eig(A)
```

> [!danger] Very important #card
> Los polos de la matriz de transferencia son los autovalores de A
