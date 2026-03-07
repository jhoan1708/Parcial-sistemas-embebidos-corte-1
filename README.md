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

* # ¿Cómo plantearía el desarrollo de una base de datos con imágenes de los diferentes elementos de un laboratorio de telecomunicaciones?

* Desarrollo de una base de datos con imágenes de los elementos del laboratorio
Para que el sistema pueda reconocer herramientas y objetos del laboratorio, primero es necesario crear un conjunto de datos (dataset) de imágenes.

* Paso 1: Identificación de los elementos

Se deben definir los objetos que el sistema reconocerá. Por ejemplo:

Osciloscopio

Multímetro

Fuente de poder

Router

Switch

Cables de red

Protoboard

Antenas

Computadores

* Paso 2: Captura de imágenes

Se deben tomar fotografías reales en el laboratorio.

* Buenas prácticas:

Tomar entre 100 y 300 imágenes por objeto

* Variar:

Ángulos

Iluminación

Distancia

Fondo

* Paso 3: Etiquetado de imágenes

Cada imagen debe estar clasificada por su tipo de objeto.

Herramientas recomendadas:

LabelImg

Roboflow

CVAT

Las etiquetas permiten entrenar el modelo de reconocimiento.

* Paso 4: Preprocesamiento de imágenes

Antes del entrenamiento se realizan:

Redimensionamiento (por ejemplo 224x224)

Normalización

Eliminación de ruido

Con librerías como:

OpenCV

TensorFlow

PyTorch

* # ¿Cómo crearía un sistema clasificador de elementos con la librería media pipe?

* # ¿Cómo reconocería el sistema la velocidad de las personas en el laboratorio?

* Reconocimiento de la velocidad de las personas en el laboratorio, Para detectar si las personas se mueven muy rápido se puede usar MediaPipe Pose.
* Paso 1: Obtener coordenadas del cuerpo, mediaPipe devuelve coordenadas: (x , y , z)

* Paso 2: Calcular desplazamiento, se guarda la posición anterior y la actual.

velocidad = distancia / tiempo. El método consiste en calcular el desplazamiento entre frames.

* Paso 3: Clasificación de movimiento, Se puede definir un umbral.

Ejemplo:

| Velocidad | Clasificación |
| :--- | :--- |
| < 0.02 | Movimiento normal |
| 0.02 - 0.05 | Movimiento rápido |
| > 0.05 | Movimiento peligroso |

* # ¿Cómo haría un despliegue en una plataforma web o móvil?
  
  

## Arquitectura

```mermaid
graph LR
    A[📷 Cámara] --> B{🧠 Sistema de Visión}
    B --> C[🔌 API REST/FastAPI]
    C --> D[🌐 Interfaz Web]

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#bbf,stroke:#333,stroke-width:2px
    style C fill:#dfd,stroke:#333,stroke-width:2px
    style D fill:#ffd,stroke:#333,stroke-width:4px
```

Tecnologías recomendadas:

| Backend | Frontend |
| :--- | :--- |
| Python | HTML |
| Flask | CSS  |
| FastAPI | JavaScript  |

La página puede mostrar:

* Video en tiempo real

* Objetos detectados

* Velocidad de personas

* Alertas

## Arquitectura completa del sistema

```mermaid
graph TD
    %% Definición de los nodos
    A[📷 Cámara del Laboratorio] --> B(🐍 Procesamiento con Python (OpenCV + MediaPipe + IA))
    
    subgraph IA [Cerebro de Inteligencia Artificial]
        B --> B1{🔍 Detección de Objetos}
        B --> B2{👥 Detección de Personas}
        B --> B3{⚡ Cálculo de Velocidad}
    end

    B1 & B2 & B3 --> C[🚀 Servidor FastAPI/Flask]
    
    C --> D[🌐 Plataforma Web]

    %% Estilos de los bloques
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style IA fill:#f0faff,stroke:#007bff,stroke-dasharray: 5 5
    style C fill:#dfd,stroke:#333,stroke-width:2px
    style D fill:#fff9c4,stroke:#fbc02d
    style E fill:#fff9c4,stroke:#fbc02d
```
