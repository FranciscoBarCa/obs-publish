#instalciones_electricas

20KV


![[../assets/Cortocircuito 2023-02-10 10.36.32.excalidraw]]
```math
Un = 20 # KV
Scc = 500 # KVA
# linea áerea de 3 cables
# 50mm2 fr ección de cable
# Trafo -> 1000KVA 20KV/400V
# Cortocircuito A = --RED--Linea-- A
Zred_A = pow(Un,2) / Scc
RL= 0.01851*2000m / 55 #
Icc_a = 1 
Pcc_a= 226.9
Zred_B = pow(400,2)/(Pcc_a*pow(10,6)) # impedandia de la red en B --RED--Linea -- Trafo (en base de B)

Ztrafo = 
```

| Lugar | ICC    | Pcc       |
| ----- | ------ | --------- |
| A     | 6.55KA | 226.9 MVA |
| B     |      22.4KA  | 15570 MVA           |
| C     |    10.754 KA     | 7.45 MVA           |
| D      |     6.875 KA   |    5MVA       |
 Nótese la **diferencia entre A y B**
 
> [!info] Info #card
>  $Pcc$ 📉 segun nos acercamos a la carga
>  
>  $Icc$ 📈 segun nos acercamos a la carga

