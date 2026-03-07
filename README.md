# Parcial-sistemas-embebidos-corte-1
Parcial corte 1

# Parte 1

Responda las siguientes preguntas a continuación:

* # ¿Qué son los microcontroladores y los microprocesadores?

los microcontroladores son circuitos integrados programables que contienen todos los componentes en un mismo circuito, pueden contener memorias pequeñas integradas para que cuando se programen no requieran de discos externos de almacenamiento, ademas que son muy usuados para sistemas que no requieran de mucho almacenamiento como procesos de iot, y los microprocesadoresson los dispositivos que realizan la funcion de cpu, en un unico circuito integrado, es capas de almacenar varias cpus. pero no son integrados ya que manejan alto volumen de datos requieren de elementos externos como unidades de almacenamientos para guardar los datos, son requeridos o usuados para computadoras por su gran cantidad de procesamientos a realizar 

* # Defina la arquitectura Von Neumann y la Arquitectura de Harvard además: Exponer sus características, ventajas y diferencias.
   
* Von Neumann
La arquitectura de Von neumann, describe que los almacenamientos estan en una sola memoria
* vemtajas
  Unica memoria para datos y programas.
  Secuencialidad: La CPU procesa una instrucción a la vez
  Es típico de los pc clásicos, sistemas de micro procesados y computadores de propósito general
  
* Harvard
La arquitectura Harvard es un modelo de diseño de computadoras en el que la memoria para instrucciones y la memoria para datos están separadas físicamente, y cada una tiene su propio bus de acceso.
* vemtajas
La memoria de instrucciones es independiente de la memoria de datos.
El procesador puede leer instrucciones y datos al mismo tiempo porque usa dos buses diferentes.

* diferencias
Meroria mientras en von neumann tiene una unica memoria el harvad cuentan con memorias diferentes
Modelo neumann cuenta con unico bus y harvadr tiene buses diferentes

*  Desventajas
Costos operativos
Utilidad en proyectos, no puedo usar una arquitectura neumann donde la capacidad de datos de almacenamiento puede superar la capacidad de memoria. 

* # ¿Qué son los procesadores tipos RISC y tipo CISC?

* RISC
Son procesadores que permiten manejar varias tareas o intrucciones, ademas cuenta con la capacidad de ser versatil al realizar varias intrucciones complejas.

* CISC
Son procesadores que cumplen pocas intrucciones sin afectar el servicio del ordenador, son bastantes faciles de trabajar al tener menor intruccion que cumplir ideal para tareas sencillas o de unica orden

* # ¿Qué es ARM (Advanced RISC Machine)?

Es una familia de arquitecturas de procesadores basada en el diseño RISC, creada para priorizar la eficiencia energética y elrendimiento en dispositivos con recursos limitados.

* # Exponer sus características, ventajas y si es muy usado en la actualidad.?

Menor consumo de energia
Eficiencia rics
Flexibilidad y escabilidad
Soporte y tecnologias avanzadas

* # ¿Cuál es la arquitecura de Arduino? Y ¿qué características tiene?

Arquitectura Harvard
CPU (Unidad Central de Procesamiento)
Memoria
Entradas y salidas
Periféricos integrados D y A

* # ¿Cuál es la arquitectura del pic 16F887 y sus principales características?
  
Arquitectura Harvard
Bus separado para instrucciones y datos
La mayoría de instrucciones se ejecutan en 1 ciclo de instrucción




# parte 2

Plantee una solución paso a paso de las situaciones descritas con loaprendido en clase:

El propósito de los estudiantes de ingeniería de telecomunicaciones decompensar es el planteamiento de una plataforma que permita elreconocimiento de las herramientas que existen en un laboratorio y también alas personas que están en el mismo donde se observe si se movilizan a unavelocidad prudente o si están generando movimientos muy rápidos por medio desistemas embebidos. Formule de manera robusta lo siguiente: 

* ¿Cómo plantearía el desarrollo de una base de datos con imágenes de los diferentes elementos de un laboratorio de telecomunicaciones?

* Desarrollo de una base de datos con imágenes de los elementos del laboratorio
Para que el sistema pueda reconocer herramientas y objetos del laboratorio, primero es necesario crear un conjunto de datos (dataset) de imágenes.

* ¿Cómo crearía un sistema clasificador de elementos con la librería media pipe?

*  ¿Cómo reconocería el sistema la velocidad de las personas en el laboratorio?

*  ¿Cómo haría un despliegue en una plataforma web o móvil?
  
