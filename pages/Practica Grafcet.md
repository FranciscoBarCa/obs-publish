**¿Cómo se programa una acción continua condicionada en GRAPH? Pon un ejemplo de programación diferente al utilizado en la práctica.**
[Grafcet](Grafcet.md) no permite condicionar directamente las [Acciones](Grafcet.md#Acciones) continuas. Pero podemos trucarlo haciendo que la variable continua se le asigne el valor de otra previamente calculada tal y como se ha hecho en la practica. 
1. Se calcula el valor de la condición y se le aplica a la variable
2. Al salir SN se le asigna un valor ) a la variable.
**Indica qué tipos de variables de un FB se utilizan en la práctica. Pon un ejemplo de cada variable según la práctica e indica por qué se utiliza ese tipo.** ????

- Input: Valores suministrados al FB a la llamada y que <u>no se modifican en FB</u>
- Output: Variables (iArrancar
- Inout (oParado)
- Staticas variables que mantienen su valor entre una llamada a una instancia  
del FB y la siguiente (sParado)
- Temporales variables de tipo temporal (tArrancarOK) (pag9)

**¿Cómo hay que manejar los interruptores del bastidor para probar el test de guías sin conectar la placa Pupitre? ¿Qué posiciones habrá que utilizar: media-alta o media-baja o según entrada? ¿Por qué?** 

Para las entradas <u>Marcha, Paro y Reset</u> se utilizarán los interruptores como si  
fuese un <u>pulsador</u>, es decir se utilizará la posición media-baja y para las  
entradas Abierto y Cerrado se utilizarán los interruptores como si fuese un <u>final  
de carrera</u>, es decir se utilizará la posición media-alta. Porque la posición media  indicará un cero, la posición alta indica un 1 y la baja hace un pulso de un 1.

**Un grupo ha programado el test de dos sistemas de guías para que pare de forma automática por tiempo. Cuando lo comprueban no les funciona el paro automático. Les sigue funcionando el paro manual. ¿Qué les puede estar ocurriendo? ¿Cómo lo pueden comprobar? ¿Cómo lo pueden resolver?** 

En el caso de que solo funcione el caso manual, esto quiere decir que hay algún  
error en los pasos previos de la configuración de la variable timer.
Muy probablemente no ha instanciado el temporizador como multiinstancia
Es decir,  puede haberse olvidado <u>configurar bien el tiempo o</u> puede no haber sustituido
la variable <u>tPararOK</u> en alguna de las transiciones. Para solucionarlo deben  
revisar todas las transiciones y las variables que actúan sobre ellas.

**Describe mediante un diagrama de tiempos el funcionamiento del temporizador TON teniendo en cuenta todas las circunstancias posibles.** 
![[../assets/Practica Grafcet 2023-02-23 00.58.27.excalidraw]]

Al encenderse In se empieza a cargar ET al soltar va a 0.
Si Pt llega a ET -> Q =1


**En una empresa se ha instalado un PLC como los del laboratorio para controlar tres líneas de envasado que son exactamente iguales. ¿Cómo habría que programarlo para que, teniendo un único programa, se consiga que las tres líneas puedan funcionar de forma independiente? Además, si se hace una mejora en el programa, la mejora se aplica a las tres líneas de envasado de forma automática, sin necesidad de realizar cortar y pegar. Explica los pasos principales para realizar la programación en el PLC.** 

Hay que hacer tres segmentos iguales. Cada uno de ellos tendrá un bloque DB  
vinculado al GRAFCET FB. Cualquier modificación en este último se copiará en los  
bloques DB tras actualizarlos en el main.
**¿Por qué en la práctica para programar el test de dos sistemas de guías se programa un FB en vez de 2 FBs sin ningún DB? ¿O por qué no se utiliza directamente 2 DBs sin ningún FB?** 

Porrque un <u>FB es una estructura de programación</u> donde se definen variables de entrada, de  
salida e internas, así como las operaciones a realizar sobre ellas. N<u>o es directamente  
ejecutable,</u> sino que necesita ser instanciado tantas veces como se desee.
Las instancias son las  que son ejecutables y cada instancia debe tener un <u>bloque de datos</u> (DB) para poder guardar  
sus variables y un mismo FB puede instanciarse tantas veces como se quiera para controlar ese  
número de sistemas iguales de manera independiente.
**Indica para qué se utiliza en general la zona de instrucciones permanentes anteriores y la de instrucciones permanentes posteriores de un FB programado en GRAPH. ¿Para qué se utilizan en la práctica si es que se utilizan?** 

¿Por qué las señales relacionadas con la parada manual del test de guías dan la orden cuando toman valor 0? ¿No es contradictorio con procesar la parada dentro del grafcet mediante lógica positiva? Explíquelo.

Explica dos maneras de programar en GRAPH una acción que comienza al arrancar una etapa y acaba al finalizar otra etapa. Entre las dos etapas no hay transición que las una.

Dibuje el esquema del circuito de mando para controlar según la práctica dos sistemas de test de guías con un único PLC. h

¿Cómo se programa en GRAPH que cuando transcurra más de t segundos en una etapa se evolucione a otra etapa de una manera simple? ¿Y si en vez de una etapa es en el conjunto de varias etapas? Justificar que las soluciones utilizadas son simples.

En un FB que se está programando en GRAPH se necesita programar una detección de flanco para la entrada iSubir y no se quiere utilizar las funciones de biblioteca de detección de flanco. ¿Dónde se debería programar dentro del FB? ¿Qué declaraciones de variables habrá que realizar? ¿Qué programa habrá que codificar? 


¿Qué es INIT_SQ? ¿Dónde aparece? ¿Para qué se utiliza? ¿Se podría eliminar? Razona cada respuesta.](<[**¿Cómo se programa una acción continua condicionada en GRAPH? Pon un ejemplo de programación diferente al utilizado en la práctica.**
[Grafcet](Grafcet.md) no permite condicionar directamente las [Acciones](Grafcet.md#Acciones) continuas. Pero podemos trucarlo haciendo que la variable continua se le asigne el valor de otra previamente calculada tal y como se ha hecho en la practica. 
1. Se calcula el valor de la condición y se le aplica a la variable
2. Al salir SN se le asigna un valor ) a la variable.
**Indica qué tipos de variables de un FB se utilizan en la práctica. Pon un ejemplo de cada variable según la práctica e indica por qué se utiliza ese tipo.** ????

- Input: Valores suministrados al FB a la llamada y que %3Cu%3Eno se modifican en FB</u>
- Output: Variables (iArrancar
- Inout (oParado)
- Staticas variables que mantienen su valor entre una llamada a una instancia  
del FB y la siguiente (sParado)
- Temporales variables de tipo temporal (tArrancarOK) (pag9)

**¿Cómo hay que manejar los interruptores del bastidor para probar el test de guías sin conectar la placa Pupitre? ¿Qué posiciones habrá que utilizar: media-alta o media-baja o según entrada? ¿Por qué?** 

Para las entradas <u>Marcha, Paro y Reset</u> se utilizarán los interruptores como si  
fuese un <u>pulsador</u>, es decir se utilizará la posición media-baja y para las  
entradas Abierto y Cerrado se utilizarán los interruptores como si fuese un <u>final  
de carrera</u>, es decir se utilizará la posición media-alta. Porque la posición media  indicará un cero, la posición alta indica un 1 y la baja hace un pulso de un 1.

**Un grupo ha programado el test de dos sistemas de guías para que pare de forma automática por tiempo. Cuando lo comprueban no les funciona el paro automático. Les sigue funcionando el paro manual. ¿Qué les puede estar ocurriendo? ¿Cómo lo pueden comprobar? ¿Cómo lo pueden resolver?** 

En el caso de que solo funcione el caso manual, esto quiere decir que hay algún  
error en los pasos previos de la configuración de la variable timer.
Muy probablemente no ha instanciado el temporizador como multiinstancia
Es decir,  puede haberse olvidado <u>configurar bien el tiempo o</u> puede no haber sustituido
la variable <u>tPararOK</u> en alguna de las transiciones. Para solucionarlo deben  
revisar todas las transiciones y las variables que actúan sobre ellas.

**Describe mediante un diagrama de tiempos el funcionamiento del temporizador TON teniendo en cuenta todas las circunstancias posibles.** 
![[../assets/Practica Grafcet 2023-02-23 00.58.27.excalidraw]]

Al encenderse In se empieza a cargar ET al soltar va a 0.
Si Pt llega a ET -> Q =1


**En una empresa se ha instalado un PLC como los del laboratorio para controlar tres líneas de envasado que son exactamente iguales. ¿Cómo habría que programarlo para que, teniendo un único programa, se consiga que las tres líneas puedan funcionar de forma independiente? Además, si se hace una mejora en el programa, la mejora se aplica a las tres líneas de envasado de forma automática, sin necesidad de realizar cortar y pegar. Explica los pasos principales para realizar la programación en el PLC.** 

Hay que hacer tres segmentos iguales. Cada uno de ellos tendrá un bloque DB  
vinculado al GRAFCET FB. Cualquier modificación en este último se copiará en los  
bloques DB tras actualizarlos en el main.
**¿Por qué en la práctica para programar el test de dos sistemas de guías se programa un FB en vez de 2 FBs sin ningún DB? ¿O por qué no se utiliza directamente 2 DBs sin ningún FB?** 

Porrque un <u>FB es una estructura de programación</u> donde se definen variables de entrada, de  
salida e internas, así como las operaciones a realizar sobre ellas. N<u>o es directamente  
ejecutable,</u> sino que necesita ser instanciado tantas veces como se desee.
Las instancias son las  que son ejecutables y cada instancia debe tener un <u>bloque de datos</u> (DB) para poder guardar  
sus variables y un mismo FB puede instanciarse tantas veces como se quiera para controlar ese  
número de sistemas iguales de manera independiente.
**Indica para qué se utiliza en general la zona de instrucciones permanentes anteriores y la de instrucciones permanentes posteriores de un FB programado en GRAPH. ¿Para qué se utilizan en la práctica si es que se utilizan?** 

¿Por qué las señales relacionadas con la parada manual del test de guías dan la orden cuando toman valor 0? ¿No es contradictorio con procesar la parada dentro del grafcet mediante lógica positiva? Explíquelo.

Explica dos maneras de programar en GRAPH una acción que comienza al arrancar una etapa y acaba al finalizar otra etapa. Entre las dos etapas no hay transición que las una.

Dibuje el esquema del circuito de mando para controlar según la práctica dos sistemas de test de guías con un único PLC. h

¿Cómo se programa en GRAPH que cuando transcurra más de t segundos en una etapa se evolucione a otra etapa de una manera simple? ¿Y si en vez de una etapa es en el conjunto de varias etapas? Justificar que las soluciones utilizadas son simples.

En un FB que se está programando en GRAPH se necesita programar una detección de flanco para la entrada iSubir y no se quiere utilizar las funciones de biblioteca de detección de flanco. ¿Dónde se debería programar dentro del FB? ¿Qué declaraciones de variables habrá que realizar? ¿Qué programa habrá que codificar? 


¿Qué es INIT_SQ? ¿Dónde aparece? ¿Para qué se utiliza? ¿Se podría eliminar? Razona cada respuesta.](<**¿Cómo se programa una acción continua condicionada en GRAPH? Pon un ejemplo de programación diferente al utilizado en la práctica.**
[Grafcet](Grafcet.md) no permite condicionar directamente las [Acciones](Grafcet.md#Acciones) continuas. Pero podemos trucarlo haciendo que la variable continua se le asigne el valor de otra previamente calculada tal y como se ha hecho en la practica. 
1. Se calcula el valor de la condición y se le aplica a la variable
2. Al salir SN se le asigna un valor ) a la variable.
**Indica qué tipos de variables de un FB se utilizan en la práctica. Pon un ejemplo de cada variable según la práctica e indica por qué se utiliza ese tipo.** ????

- Input: Valores suministrados al FB a la llamada y que %3Cu%3Eno se modifican en FB</u>
- Output: Variables (iArrancar
- Inout (oParado)
- Staticas variables que mantienen su valor entre una llamada a una instancia  
del FB y la siguiente (sParado)
- Temporales variables de tipo temporal (tArrancarOK) (pag9)

**¿Cómo hay que manejar los interruptores del bastidor para probar el test de guías sin conectar la placa Pupitre? ¿Qué posiciones habrá que utilizar: media-alta o media-baja o según entrada? ¿Por qué?** 

Para las entradas <u>Marcha, Paro y Reset</u> se utilizarán los interruptores como si  
fuese un <u>pulsador</u>, es decir se utilizará la posición media-baja y para las  
entradas Abierto y Cerrado se utilizarán los interruptores como si fuese un <u>final  
de carrera</u>, es decir se utilizará la posición media-alta. Porque la posición media  indicará un cero, la posición alta indica un 1 y la baja hace un pulso de un 1.

**Un grupo ha programado el test de dos sistemas de guías para que pare de forma automática por tiempo. Cuando lo comprueban no les funciona el paro automático. Les sigue funcionando el paro manual. ¿Qué les puede estar ocurriendo? ¿Cómo lo pueden comprobar? ¿Cómo lo pueden resolver?** 

En el caso de que solo funcione el caso manual, esto quiere decir que hay algún  
error en los pasos previos de la configuración de la variable timer.
Muy probablemente no ha instanciado el temporizador como multiinstancia
Es decir,  puede haberse olvidado <u>configurar bien el tiempo o</u> puede no haber sustituido
la variable <u>tPararOK</u> en alguna de las transiciones. Para solucionarlo deben  
revisar todas las transiciones y las variables que actúan sobre ellas.

**Describe mediante un diagrama de tiempos el funcionamiento del temporizador TON teniendo en cuenta todas las circunstancias posibles.** 
![[../assets/Practica Grafcet 2023-02-23 00.58.27.excalidraw]]

Al encenderse In se empieza a cargar ET al soltar va a 0.
Si Pt llega a ET -> Q =1


**En una empresa se ha instalado un PLC como los del laboratorio para controlar tres líneas de envasado que son exactamente iguales. ¿Cómo habría que programarlo para que, teniendo un único programa, se consiga que las tres líneas puedan funcionar de forma independiente? Además, si se hace una mejora en el programa, la mejora se aplica a las tres líneas de envasado de forma automática, sin necesidad de realizar cortar y pegar. Explica los pasos principales para realizar la programación en el PLC.** 

Hay que hacer tres segmentos iguales. Cada uno de ellos tendrá un bloque DB  
vinculado al GRAFCET FB. Cualquier modificación en este último se copiará en los  
bloques DB tras actualizarlos en el main.
**¿Por qué en la práctica para programar el test de dos sistemas de guías se programa un FB en vez de 2 FBs sin ningún DB? ¿O por qué no se utiliza directamente 2 DBs sin ningún FB?** 

Porrque un <u>FB es una estructura de programación</u> donde se definen variables de entrada, de  
salida e internas, así como las operaciones a realizar sobre ellas. N<u>o es directamente  
ejecutable,</u> sino que necesita ser instanciado tantas veces como se desee.
Las instancias son las  que son ejecutables y cada instancia debe tener un <u>bloque de datos</u> (DB) para poder guardar  
sus variables y un mismo FB puede instanciarse tantas veces como se quiera para controlar ese  
número de sistemas iguales de manera independiente.
**Indica para qué se utiliza en general la zona de instrucciones permanentes anteriores y la de instrucciones permanentes posteriores de un FB programado en GRAPH. ¿Para qué se utilizan en la práctica si es que se utilizan?** 
<u>Instrucciones permanentes anteriores.</u> Son instrucciones que se ejecutan antes de  
ejecutar el grafcet propiamente dicho (cadenas en la terminología Siemens), como, por  
ejemplo, detectar un flanco en una variable.
I<u>nstrucciones permanentes posteriores. </u>Son instrucciones que se ejecutan al terminar  
la ejecución del programa correspondiente a las cadenas. Una utilización puede ser la  
programación de acciones más sofisticadas que las admitidas dentro de una etapa.

**¿Por qué las señales relacionadas con la parada manual del test de guías dan la orden cuando toman valor 0? ¿No es contradictorio con procesar la parada dentro del grafcet mediante lógica positiva? Explíquelo.**
No, es una medida de seguridad, de esta forma, ante cualquier problema con el cableado se realizará una parada de energencia. Por otro lado, no es contradictorio porque a la entrada del FB se niega la variable de paro piparo permitiendo  
implementar lógica positiva dentro del FB con la variable iParar. Esto hace más cómoda la lógica.

**Explica dos maneras de programar en GRAPH una acción que comienza al arrancar una etapa y acaba al finalizar otra etapa. Entre las dos etapas no hay transición que las una.**
1. Realizar una acción permanente al entrar en una etapa y desactivar dicha acción al salir de una segunda etapa.
2. mediante el uso de las instrucciones permanentes utilizando  una estrategia de SET y RESET
**Dibuje el esquema del circuito de mando para controlar según la práctica dos sistemas de test de guías con un único PLC.** 
![[../assets/Practica Grafcet 2023-02-23 01.22.08.excalidraw]]
**¿Cómo se programa en GRAPH que cuando transcurra más de t segundos en una etapa se evolucione a otra etapa de una manera simple? ¿Y si en vez de una etapa es en el conjunto de varias etapas? Justificar que las soluciones utilizadas son simples.**
Transición con gsEstapa.T > 

En el caso de que sean varias etapas, se puede utilizar el bloque TON donde la entrada es el paralelo de la activación de las etapas y la  salida es una variable que permite hacer bypass a dichas etapas cuando pasa el tiempo  marcado.


**En un FB que se está programando en GRAPH se necesita programar una detección de flanco para la entrada iSubir y no se quiere utilizar las funciones de biblioteca de detección de flanco. ¿Dónde se debería programar dentro del FB? ¿Qué declaraciones de variables habrá que realizar? ¿Qué programa habrá que codificar?**

![](../assets/Pasted%20image%2020230223012634.png)


**¿Qué es INIT_SQ? ¿Dónde aparece? ¿Para qué se utiliza? ¿Se podría eliminar? Razona cada respuesta.**  
Es una estrada automática que permite incializar el grafcet cada que hay un flaco positivo en la entrada. INIT Sequence.

La entrada INIT_SQ es una entrada creada automáticamente por TIAPortal que  
permite inicializar el grafcet en la etapa inicial cada vez que hay un flanco positivo  
en esta entrada.  
• Aparece en el FB como un input predeterminado  
• El uso típico de la entrada INIT_SQ es ayudar a resolver problemas llevando el  
grafcet a una etapa totalmente conocida.  
• No se puede eliminar, el programa lo impide, es lo que te permite volver a un  
estado inicia.