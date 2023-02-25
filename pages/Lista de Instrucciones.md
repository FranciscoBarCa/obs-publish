#Automatizacion 

# RLO
Variable donde se guarda el resultado de cada instrucción.
Al empezar un programa o tras **asignar una salida, la siguiente instrucción inicializa el RLO.**
# Ejemplo
| Instrucción | Significado     |
| ----------- | --------------- |
| A/O SJ1     | RLO=SJ1         |
| A SJ2       | RLO=SJ2 AND RLO |
| ON SJ3      | RLO SJ3' OR RLO |
| = PF        | PF = RLO        |
|             |                 |
f= SJI*SJ2+SJ3'
