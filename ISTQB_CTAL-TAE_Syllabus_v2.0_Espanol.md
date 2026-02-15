# Tester Certificado Nivel Avanzado - Ingenieria de Automatizacion de Pruebas (CTAL-TAE)

## Syllabus Version 2.0

**International Software Testing Qualifications Board**

---

## Aviso de Derechos de Autor

Aviso de Derechos de Autor (c) International Software Testing Qualifications Board (en adelante denominado ISTQB(R))

ISTQB(R) es una marca registrada del International Software Testing Qualifications Board.

Copyright (c) 2024 los autores del syllabus de Ingenieria de Automatizacion de Pruebas v2.0: Andrew Pollner (Presidente), Peter Foldhazi, Patrick Quilter, Gergely Agnecz, Laszlo Szikszai.

Copyright (c) 2016 los autores Andrew Pollner (Presidente), Bryan Bakker, Armin Born, Mark Fewster, Jani Haukinen, Raluca Popescu, Ina Schieferdecker.

Todos los derechos reservados. Los autores transfieren los derechos de autor al ISTQB(R). Los autores (como titulares actuales de los derechos de autor) y el ISTQB(R) (como futuro titular de los derechos de autor) han acordado las siguientes condiciones de uso:

- Se pueden copiar extractos de este documento para uso no comercial si se reconoce la fuente.
- Cualquier Proveedor de Formacion Acreditado puede usar este syllabus como base para un curso de formacion si se reconoce a los autores y al ISTQB(R) como fuente y propietarios de los derechos de autor.
- Cualquier individuo o grupo puede usar este syllabus como base para articulos y libros, si se reconoce a los autores y al ISTQB(R) como fuente.
- Cualquier otro uso de este syllabus esta prohibido sin obtener primero la aprobacion por escrito del ISTQB(R).

---

## Historial de Revisiones

| Version | Fecha | Observaciones |
|---------|-------|---------------|
| Syllabus 2016 | 2016/10/21 | Publicacion GA de CTAL-TAE |
| Syllabus v2.0 | 2024/05/03 | Publicacion GA de CTAL-TAE v2.0 |

---

## Tabla de Contenidos

- [0. Introduccion](#0-introduccion)
- [1. Introduccion y Objetivos de la Automatizacion de Pruebas](#1-introduccion-y-objetivos-de-la-automatizacion-de-pruebas--45-minutos-k2)
- [2. Preparacion para la Automatizacion de Pruebas](#2-preparacion-para-la-automatizacion-de-pruebas--180-minutos-k4)
- [3. Arquitectura de Automatizacion de Pruebas](#3-arquitectura-de-automatizacion-de-pruebas--210-minutos-k3)
- [4. Implementacion de la Automatizacion de Pruebas](#4-implementacion-de-la-automatizacion-de-pruebas--150-minutos-k4)
- [5. Estrategias de Implementacion y Despliegue](#5-estrategias-de-implementacion-y-despliegue-para-la-automatizacion-de-pruebas--90-minutos-k3)
- [6. Reportes y Metricas de Automatizacion de Pruebas](#6-reportes-y-metricas-de-automatizacion-de-pruebas--150-minutos-k4)
- [7. Verificacion de la Solucion de Automatizacion de Pruebas](#7-verificacion-de-la-solucion-de-automatizacion-de-pruebas--135-minutos-k3)
- [8. Mejora Continua](#8-mejora-continua--210-minutos-k4)
- [9. Referencias](#9-referencias)
- [10. Apendice A](#10-apendice-a--objetivos-de-aprendizajenivel-cognitivo-de-conocimiento)
- [11. Apendice B](#11-apendice-b--matriz-de-trazabilidad)
- [12. Apendice C](#12-apendice-c--notas-de-la-version)
- [13. Apendice D](#13-apendice-d--terminos-especificos-del-dominio)
- [14. Indice](#14-indice)

---

## Reconocimientos

Este documento fue publicado formalmente por la Asamblea General del ISTQB(R) el 3 de mayo de 2024.

Fue producido por el Grupo de Trabajo de Automatizacion de Pruebas del Grupo de Trabajo Especialista del International Software Testing Qualifications Board: Graham Bath (Presidente del Grupo de Trabajo Especialista), Andrew Pollner (Vicepresidente del Grupo de Trabajo Especialista y Presidente del Grupo de Trabajo de Automatizacion de Pruebas), Peter Foldhazi, Patrick Quilter, Gergely Agnecz, Laszlo Szikszai.

Los revisores del Grupo de Trabajo de Automatizacion de Pruebas incluyeron: Armin Beer, Armin Born, Geza Bujdoso, Renzo Cerquozzi, Jan Giesen, Arnika Hryszko, Kari Kakkonen, Gary Mogyorodi, Chris van Bael, Carsten Weise, Marc-Florian Wendland.

Revisor Tecnico: Gary Mogyorodi

---

## 0. Introduccion

### 0.1 Proposito de este Syllabus

Este syllabus constituye la base para la Cualificacion Internacional de Pruebas de Software para la cualificacion de Ingenieria de Automatizacion de Pruebas de Nivel Avanzado (CTAL-TAE). El ISTQB(R) proporciona este syllabus de la siguiente manera:

1. A los organismos miembros, para traducirlo a su idioma local y acreditar proveedores de formacion. Los organismos miembros pueden adaptar el syllabus a las necesidades de su idioma particular y modificar las referencias para adaptarlas a sus publicaciones locales.
2. A los organismos de certificacion, para derivar preguntas de examen en su idioma local adaptadas a los objetivos de aprendizaje de este syllabus.
3. A los proveedores de formacion, para producir material didactico y determinar metodos de ensenanza apropiados.
4. A los candidatos a la certificacion, para prepararse para el examen de certificacion (ya sea como parte de un curso de formacion o de forma independiente).
5. A la comunidad internacional de ingenieria de software y sistemas, para avanzar en la profesion de pruebas de software y sistemas, y como base para libros y articulos.

### 0.2 La Ingenieria de Automatizacion de Pruebas en las Pruebas de Software

La cualificacion de Ingenieria de Automatizacion de Pruebas esta dirigida a cualquier persona involucrada en pruebas de software y automatizacion de pruebas. Esto incluye personas en roles como testers, analistas de pruebas, ingenieros de automatizacion de pruebas, consultores de pruebas, arquitectos de pruebas, gestores de pruebas y desarrolladores de software. Esta cualificacion tambien es apropiada para cualquier persona que desee una comprension basica de la automatizacion de pruebas, como gerentes de proyecto, gerentes de calidad, gerentes de desarrollo de software, analistas de negocio, directores de TI y consultores de gestion.

El syllabus de Ingenieria de Automatizacion de Pruebas esta dirigido al ingeniero de pruebas que busca implementar o mejorar la automatizacion de pruebas. Define metodos y practicas que pueden soportar una solucion sostenible. Otras directrices y modelos de referencia relacionados con las soluciones de automatizacion de pruebas son estandares de ingenieria de software para los ciclos de vida de desarrollo de software seleccionados, tecnologias de programacion y estandares de formato. Este syllabus no ensena ingenieria de software. Sin embargo, se espera que un ingeniero de automatizacion de pruebas tenga habilidades, experiencia y pericia en ingenieria de software.

Ademas, un ingeniero de automatizacion de pruebas necesita estar al tanto de los estandares y mejores practicas de programacion y documentacion de la industria para utilizarlos al desarrollar una solucion de automatizacion de pruebas. Estas practicas pueden aumentar la mantenibilidad, confiabilidad y seguridad de la solucion de automatizacion de pruebas. Tales estandares se basan tipicamente en caracteristicas de calidad.

### 0.3 Trayectoria Profesional para Testers e Ingenieros de Automatizacion de Pruebas

El esquema del ISTQB(R) proporciona soporte para profesionales de pruebas en todas las etapas de sus carreras, ofreciendo tanto amplitud como profundidad de conocimiento. Las personas que obtienen la certificacion ISTQB(R) de Ingenieria de Automatizacion de Pruebas tambien pueden estar interesadas en la cualificacion de Estrategia de Automatizacion de Pruebas (CT-TAS).

Las personas que obtienen la certificacion ISTQB(R) Tester Certificado en Ingenieria de Automatizacion de Pruebas tambien pueden estar interesadas en los Niveles Avanzados Principales (Analista de Pruebas, Analista Tecnico de Pruebas y Gestor de Pruebas) y posteriormente en el Nivel Experto (Gestion de Pruebas o Mejora del Proceso de Pruebas). Cualquier persona que busque desarrollar habilidades en practicas de pruebas en un entorno Agil podria considerar las certificaciones de Tester Tecnico Agil o Liderazgo de Pruebas Agil a Escala. El flujo de Especialista ofrece una inmersion profunda en areas que tienen enfoques y actividades de pruebas especificos, por ejemplo, en Estrategia de Automatizacion de Pruebas, Pruebas de Rendimiento, Pruebas de Seguridad, Pruebas de IA y Pruebas de Aplicaciones Moviles, o donde se requiere conocimiento especifico del dominio (por ejemplo, Pruebas de Software Automotriz o Pruebas de Videojuegos).

### 0.4 Resultados de Negocio

Esta seccion enumera los Resultados de Negocio esperados de un candidato que ha obtenido la certificacion de Ingenieria de Automatizacion de Pruebas.

Un candidato que ha obtenido la certificacion de Ingenieria de Automatizacion de Pruebas puede...

| Codigo | Resultado de Negocio |
|--------|---------------------|
| TAE-B01 | Describir el proposito de la automatizacion de pruebas |
| TAE-B02 | Comprender la automatizacion de pruebas a traves del ciclo de vida del desarrollo de software |
| TAE-B03 | Comprender la configuracion de una infraestructura para habilitar la automatizacion de pruebas |
| TAE-B04 | Aprender el proceso de evaluacion para seleccionar las herramientas y estrategias adecuadas |
| TAE-B05 | Comprender los conceptos de diseno para construir soluciones de automatizacion de pruebas modulares y escalables |
| TAE-B06 | Seleccionar un enfoque, incluyendo un piloto, para planificar el despliegue de la automatizacion de pruebas dentro del ciclo de vida del desarrollo de software |
| TAE-B07 | Disenar y desarrollar soluciones de automatizacion de pruebas (nuevas o modificadas) que satisfagan las necesidades tecnicas |
| TAE-B08 | Considerar el alcance y enfoque de la automatizacion de pruebas y el mantenimiento del testware |
| TAE-B09 | Comprender como se integran las pruebas automatizadas dentro de los pipelines CI/CD |
| TAE-B10 | Comprender como recopilar, analizar y reportar datos de automatizacion de pruebas para informar a las partes interesadas |
| TAE-B11 | Verificar la infraestructura de automatizacion de pruebas |
| TAE-B12 | Definir oportunidades de mejora continua para la automatizacion de pruebas |

### 0.5 Objetivos de Aprendizaje Examinables y Nivel Cognitivo de Conocimiento

Los objetivos de aprendizaje apoyan los resultados de negocio y se utilizan para crear los examenes de Tester Certificado en Ingenieria de Automatizacion de Pruebas.

En general, todos los contenidos de este syllabus son examinables en los niveles K2, K3 y K4, excepto la Introduccion y los Apendices. Es decir, al candidato se le puede pedir que reconozca, recuerde o rememore una palabra clave o concepto mencionado en cualquiera de los ocho capitulos. Los niveles especificos de los objetivos de aprendizaje se muestran al inicio de cada capitulo y se clasifican de la siguiente manera:

- **K2**: Comprender
- **K3**: Aplicar
- **K4**: Analizar

Se proporcionan mas detalles y ejemplos de objetivos de aprendizaje en el Apendice A.

Todos los terminos listados como palabras clave justo debajo de los encabezados de capitulo deben ser recordados, incluso si no se mencionan explicitamente en los objetivos de aprendizaje.

### 0.6 El Examen del Certificado de Ingenieria de Automatizacion de Pruebas

El examen del Certificado de Ingenieria de Automatizacion de Pruebas se basara en este syllabus. Las respuestas a las preguntas del examen pueden requerir el uso de material basado en mas de una seccion de este syllabus. Todas las secciones del syllabus son examinables, excepto la Introduccion y los Apendices. Los estandares y libros se incluyen como referencias, pero su contenido no es examinable, mas alla de lo que se resume en el propio syllabus de dichos estandares y libros.

El criterio de entrada para presentar el examen de Ingenieria de Automatizacion de Pruebas es que los candidatos tengan interes en pruebas de software y automatizacion de pruebas. Sin embargo, se recomienda encarecidamente que los candidatos tambien:

- Tengan al menos una experiencia minima en desarrollo de software y pruebas de software, como seis meses de experiencia como ingeniero de pruebas de software o como desarrollador de software.
- Tomen un curso que haya sido acreditado segun los estandares del ISTQB (por uno de los organismos miembros reconocidos por el ISTQB).

> **Nota sobre Requisito de Entrada**: El certificado de Nivel Basico (Foundation Level) del ISTQB(R) debe obtenerse antes de presentar el examen de certificacion de Ingenieria de Automatizacion de Pruebas del ISTQB(R).

### 0.7 Acreditacion

Un Organismo Miembro del ISTQB(R) puede acreditar a proveedores de formacion cuyo material de curso siga este syllabus. Los proveedores de formacion deben obtener las directrices de acreditacion del Organismo Miembro o entidad que realice la acreditacion. Un curso acreditado se reconoce como conforme a este syllabus y se le permite tener un examen del ISTQB(R) como parte del curso.

Las directrices de acreditacion para este syllabus siguen las Directrices Generales de Acreditacion publicadas por el Grupo de Trabajo de Gestion de Procesos y Cumplimiento.

### 0.8 Manejo de Estandares

Hay estandares referenciados en el syllabus de Ingenieria de Automatizacion de Pruebas (por ejemplo, IEEE e ISO). El proposito de estas referencias es proporcionar un marco (como en las referencias a ISO 25010 respecto a las caracteristicas de calidad) o proporcionar una fuente de informacion adicional si el lector lo desea. El syllabus utiliza los documentos estandar como referencia. Los documentos de estandares no estan destinados para examinacion. Consulte el Capitulo 9 Referencias para mas informacion sobre Estandares.

### 0.9 Manteniendose Actualizado

La industria del software cambia rapidamente. Para lidiar con estos cambios y proporcionar a las partes interesadas acceso a informacion relevante y actual, los grupos de trabajo del ISTQB han creado enlaces en el sitio web www.istqb.org, que refieren a documentos de soporte y cambios en los estandares. Esta informacion no es examinable bajo el syllabus de Ingenieria de Automatizacion de Pruebas.

### 0.10 Nivel de Detalle

El nivel de detalle en este syllabus permite cursos y examenes consistentes a nivel internacional. Para lograr este objetivo, el syllabus consiste en:

- Objetivos instruccionales generales que describen la intencion del Especialista en Ingenieria de Automatizacion de Pruebas
- Una lista de terminos que los estudiantes deben ser capaces de recordar
- Objetivos de aprendizaje para cada area de conocimiento, describiendo el resultado cognitivo de aprendizaje a alcanzar
- Una descripcion de los conceptos clave, incluyendo referencias a fuentes como literatura aceptada o estandares

El contenido del syllabus no es una descripcion de toda el area de conocimiento de las pruebas de software; refleja el nivel de detalle a cubrir en los cursos de formacion en Ingenieria de Automatizacion de Pruebas. Se centra en conceptos y tecnicas de prueba que pueden aplicarse a todos los proyectos de software, incluyendo aquellos que siguen metodos Agiles. Este syllabus no contiene ningun objetivo de aprendizaje especifico relacionado con pruebas Agiles, pero si discute como estos conceptos se aplican en proyectos Agiles y otros tipos de proyectos.

### 0.11 Como esta Organizado este Syllabus

Hay ocho capitulos con contenido examinable. El encabezado de nivel superior para cada capitulo especifica el tiempo para el capitulo; no se proporciona temporalizacion por debajo del nivel de capitulo. Para cursos de formacion acreditados, el syllabus requiere un minimo de 21 horas de instruccion, distribuidas en los ocho capitulos de la siguiente manera:

- **Capitulo 1: 45 minutos** - Introduccion y Objetivos de la Automatizacion de Pruebas
  - El tester aprende sobre los beneficios de la automatizacion de pruebas y sus limitaciones
  - Se cubre la automatizacion de pruebas dentro de diferentes modelos de ciclo de vida del desarrollo de software
  - El tester aprende como la arquitectura de un sistema bajo prueba (SUT) impacta la idoneidad de las herramientas de prueba

- **Capitulo 2: 180 minutos** - Preparacion para la Automatizacion de Pruebas
  - Se cubre el diseno para la testabilidad del SUT a traves de la observabilidad, controlabilidad y una arquitectura claramente definida
  - El tester aprende sobre la automatizacion de pruebas en diferentes entornos
  - Se cubren los factores requeridos para evaluar una solucion de automatizacion de pruebas apropiada
  - El tester aprendera sobre las consideraciones tecnicas necesarias para desarrollar recomendaciones sobre automatizacion de pruebas

- **Capitulo 3: 210 minutos** - Arquitectura de Automatizacion de Pruebas
  - Se cubre la arquitectura de automatizacion de pruebas y sus componentes que conducen a una solucion de automatizacion de pruebas
  - El tester aprendera sobre las capas y su aplicacion en un framework de automatizacion de pruebas
  - Se cubriran multiples enfoques para usar herramientas de automatizacion de pruebas
  - El tester aprendera como los principios de diseno y patrones de diseno pueden aplicarse a la automatizacion de pruebas

- **Capitulo 4: 150 minutos** - Implementacion de la Automatizacion de Pruebas
  - Se cubrira como planificar y desplegar efectivamente un proyecto piloto de automatizacion de pruebas
  - El tester aprendera sobre los riesgos de despliegue y las estrategias de mitigacion
  - Se cubriran los factores que mejoran la mantenibilidad del codigo de automatizacion de pruebas

- **Capitulo 5: 90 minutos** - Estrategias de Implementacion y Despliegue para la Automatizacion de Pruebas
  - El tester aprendera sobre los pipelines CI/CD y la ejecucion automatizada de pruebas a traves de los niveles de prueba
  - Se cubrira la gestion de configuracion para los componentes de la automatizacion de pruebas
  - El tester aprendera sobre las dependencias aplicadas a las pruebas de API y de contrato

- **Capitulo 6: 150 minutos** - Reportes y Metricas de Automatizacion de Pruebas
  - El tester aprendera sobre donde se pueden recopilar datos del SUT y la automatizacion de pruebas para analisis y reportes
  - Se cubrira el analisis de datos de los reportes del SUT y la automatizacion de pruebas para descubrir causas de fallos
  - Se cubrira el uso de reportes de pruebas y dashboards para informar a las partes interesadas

- **Capitulo 7: 135 minutos** - Verificacion de la Solucion de Automatizacion de Pruebas
  - El tester aprendera como examinar y verificar la operacion correcta de los componentes y el entorno de automatizacion de pruebas
  - Se cubrira la garantia de que los scripts y suites de prueba se ejecutan correctamente
  - El tester comprendera cuando realizar analisis de causa raiz
  - Se cubriran tecnicas para analizar el codigo de automatizacion de pruebas en cuanto a calidad

- **Capitulo 8: 210 minutos** - Mejora Continua
  - Se cubriran areas adicionales de analisis de datos para la mejora de casos de prueba
  - El tester aprendera formas de hacer mejoras y actualizaciones a una solucion de automatizacion de pruebas y sus componentes
  - Se cubrira la identificacion de formas de consolidar y optimizar la automatizacion de pruebas
  - El tester aprendera como las herramientas de automatizacion de pruebas pueden asistir con las necesidades de soporte y configuracion de pruebas

---

## 1. Introduccion y Objetivos de la Automatizacion de Pruebas – 45 minutos (K2)

**Palabras clave**: sistema bajo prueba, automatizacion de pruebas, ingeniero de automatizacion de pruebas

### Objetivos de Aprendizaje para el Capitulo 1:

**1.1 Proposito de la Automatizacion de Pruebas**
- TAE-1.1.1 (K2) Explicar las ventajas y desventajas de la automatizacion de pruebas

**1.2 Automatizacion de Pruebas en el Ciclo de Vida del Desarrollo de Software**
- TAE-1.2.1 (K2) Explicar como se aplica la automatizacion de pruebas en los diferentes modelos del ciclo de vida del desarrollo de software
- TAE-1.2.2 (K2) Seleccionar herramientas de automatizacion de pruebas adecuadas para un sistema bajo prueba dado

---

### 1.1 Proposito de la Automatizacion de Pruebas

#### 1.1.1 Explicar las Ventajas y Desventajas de la Automatizacion de Pruebas

La automatizacion de pruebas, que incluye la ejecucion automatizada de pruebas y los reportes de pruebas, consiste en una o mas de las siguientes actividades:

- Usar herramientas de software especificas para controlar y configurar suites de prueba para la ejecucion de pruebas
- Ejecutar pruebas de manera automatizada
- Comparar los resultados reales con los resultados esperados

La automatizacion de pruebas proporciona caracteristicas y capacidades significativas que pueden interactuar con un sistema bajo prueba (SUT). La automatizacion de pruebas puede cubrir un area amplia de software. Las soluciones cubren muchos tipos de software (por ejemplo, SUT con interfaz de usuario (UI), SUT sin UI, aplicaciones moviles, protocolos de red y conexiones).

**La automatizacion de pruebas tiene muchas ventajas:**

- Permite ejecutar mas pruebas por compilacion en comparacion con las pruebas manuales
- Proporciona la capacidad de crear y ejecutar pruebas que no pueden ejecutarse manualmente (por ejemplo, respuesta en tiempo real, pruebas remotas y pruebas en paralelo)
- Permite pruebas mas complejas que las pruebas manuales
- Se ejecuta mas rapido que las pruebas manuales
- Esta menos sujeta a error humano
- Es mas efectiva y eficiente en el uso de recursos de prueba
- Proporciona retroalimentacion mas rapida sobre la calidad del SUT
- Ayuda a mejorar la confiabilidad del sistema (por ejemplo, disponibilidad y recuperabilidad)
- Mejora la consistencia de la ejecucion de pruebas a traves de los ciclos de prueba

**Sin embargo, la automatizacion de pruebas tiene desventajas potenciales incluyendo:**

- Costos adicionales para el proyecto ya que puede ser necesario contratar un ingeniero de automatizacion de pruebas (TAE), comprar nuevo hardware y establecer capacitacion
- Requerimiento de inversion inicial para configurar una solucion de automatizacion de pruebas
- Tiempo para desarrollar y mantener una solucion de automatizacion de pruebas
- Requerimiento de objetivos claros de automatizacion de pruebas para asegurar el exito
- Rigidez de las pruebas y menor adaptabilidad a cambios en el SUT
- Introduccion de defectos adicionales por la automatizacion de pruebas

**Hay limitaciones de la automatizacion de pruebas que deben tenerse en cuenta:**

- No todas las pruebas manuales pueden automatizarse
- Solo se verifica lo que las pruebas automatizadas estan programadas para hacer
- La automatizacion de pruebas solo puede verificar resultados interpretables por maquina, lo que significa que algunas caracteristicas de calidad pueden no ser testeables con automatizacion
- La automatizacion de pruebas solo puede verificar resultados de pruebas que pueden ser verificados por un oraculo de pruebas automatizado

---

### 1.2 Automatizacion de Pruebas en el Ciclo de Vida del Desarrollo de Software

#### 1.2.1 Explicar Como se Aplica la Automatizacion de Pruebas en los Diferentes Modelos del Ciclo de Vida del Desarrollo de Software

**Cascada (Waterfall)**

El modelo en cascada es un modelo de SDLC que es tanto lineal como secuencial. Este modelo tiene fases distintas (es decir, requisitos, diseno, implementacion, verificacion y mantenimiento) y cada fase tipicamente concluye con documentacion que debe ser aprobada. La implementacion de la automatizacion de pruebas tipicamente ocurre en paralelo o despues de la fase de implementacion. Las ejecuciones de prueba usualmente tienen lugar durante la fase de verificacion debido a que los componentes de software no estan listos para pruebas hasta entonces.

**Modelo en V (V-model)**

El modelo en V es un modelo de SDLC donde un proceso se ejecuta de manera secuencial. A medida que un proyecto se define desde requisitos de alto nivel hasta requisitos de bajo nivel, se definen actividades correspondientes de prueba e integracion para validar esos requisitos. De aqui se derivan los niveles de prueba tradicionales: componente, integracion de componentes, sistema, integracion de sistema y aceptacion como se describe en la Seccion 2.2 del CTFL. Proporcionar un framework de automatizacion de pruebas (TAF) para cada nivel de prueba es posible y recomendado.

**Desarrollo de software Agil**

En el desarrollo de software Agil, hay innumerables posibilidades para la automatizacion de pruebas. A diferencia del modelo en cascada o el modelo en V, en el metodo de desarrollo de software Agil, los TAEs y los representantes de negocio pueden decidir sobre la hoja de ruta, los plazos y la entrega planificada de pruebas. En este metodo, hay mejores practicas como revisiones de codigo, programacion en pares y ejecucion frecuente de pruebas automatizadas. Eliminar silos (es decir, asegurar que los desarrolladores, testers y otras partes interesadas trabajen juntos) permite a los equipos cubrir todos los niveles de prueba con la cantidad y profundidad apropiada de automatizacion de pruebas, logrando un objetivo llamado automatizacion dentro del sprint (in-sprint automation). Se encuentran mas detalles en el Syllabus ISTQB CT-TAS, Seccion 3.2.

#### 1.2.2 Seleccionar Herramientas de Automatizacion de Pruebas Adecuadas para un Sistema Bajo Prueba Dado

Para identificar las herramientas de prueba mas adecuadas para un proyecto dado, primero se debe analizar el SUT. Los TAEs necesitan identificar los requisitos del proyecto que pueden usarse como linea base para la seleccion de herramientas.

Dado que se utilizan diferentes caracteristicas de herramientas de automatizacion de pruebas para software de UI y, por ejemplo, servicios web, es importante comprender lo que el proyecto quiere lograr a lo largo del tiempo. No hay limite en el numero de herramientas y caracteristicas de automatizacion de pruebas que se pueden usar o seleccionar, pero los costos siempre deben ser considerados. Usar una herramienta comercial lista para usar o implementar una solucion personalizada basada en tecnologia de codigo abierto puede ser un proceso complejo.

El siguiente tema a evaluar es la composicion y experiencia del equipo en automatizacion de pruebas. En el caso donde los testers tienen poca o ninguna experiencia en programacion, usar una solucion de bajo codigo (low-code) o sin codigo (no-code) puede ser una opcion viable.

Para testers tecnicos con conocimiento de programacion, puede ser util seleccionar herramientas cuyo lenguaje coincida con el del SUT. Esto proporciona ventajas que incluyen la capacidad de trabajar con desarrolladores en la depuracion de defectos de automatizacion de pruebas de manera mas eficiente y la capacitacion cruzada de miembros entre equipos.

---

## 2. Preparacion para la Automatizacion de Pruebas – 180 minutos (K4)

**Palabras clave**: pruebas de API, pruebas de GUI, testabilidad

### Objetivos de Aprendizaje para el Capitulo 2:

**2.1 Comprender la Configuracion de una Infraestructura para Habilitar la Automatizacion de Pruebas**
- TAE-2.1.1 (K2) Describir las necesidades de configuracion de una infraestructura que habilite la implementacion de la automatizacion de pruebas
- TAE-2.1.2 (K2) Explicar como se aprovecha la automatizacion de pruebas dentro de diferentes entornos

**2.2 Proceso de Evaluacion para Seleccionar las Herramientas y Estrategias Adecuadas**
- TAE-2.2.1 (K4) Analizar un sistema bajo prueba para determinar la solucion de automatizacion de pruebas apropiada
- TAE-2.2.2 (K4) Ilustrar los hallazgos tecnicos de una evaluacion de herramientas

---

### 2.1 Comprender la Configuracion de una Infraestructura para Habilitar la Automatizacion de Pruebas

#### 2.1.1 Describir las Necesidades de Configuracion de una Infraestructura que Habilite la Implementacion de la Automatizacion de Pruebas

La testabilidad del SUT (es decir, la disponibilidad de interfaces de software que soporten las pruebas, por ejemplo, para habilitar el control y la observabilidad del SUT) debe disenarse e implementarse en paralelo con el diseno e implementacion de las otras caracteristicas del SUT. Este trabajo es generalmente realizado por un arquitecto de software ya que la testabilidad es un requisito no funcional del sistema, a menudo con la participacion de un TAE para identificar las areas especificas donde se pueden hacer mejoras.

Para una mejor testabilidad del SUT hay diferentes soluciones que se pueden utilizar y que tienen diferentes necesidades de configuracion, por ejemplo:

- **Identificadores de accesibilidad**: Los diferentes frameworks de desarrollo pueden generar estos identificadores automaticamente o los desarrolladores pueden establecerlos manualmente
- **Variables de entorno del sistema**: Ciertos parametros de la aplicacion pueden cambiarse para facilitar las pruebas a traves de la administracion
- **Variables de despliegue**: Similares a las variables del sistema pero pueden establecerse antes de iniciar el despliegue

Disenar para la testabilidad de un SUT consiste en los siguientes aspectos:

- **Observabilidad**: El SUT necesita proporcionar interfaces que den vision del SUT. Los casos de prueba pueden entonces usar estas interfaces para determinar si los resultados reales son iguales a los resultados esperados.
- **Controlabilidad**: El SUT necesita proporcionar interfaces que puedan usarse para realizar acciones sobre el SUT. Esto puede ser elementos de UI, llamadas a funciones, elementos de comunicacion (por ejemplo, protocolos TCP/IP y USB), o senales electronicas para interruptores fisicos o logicos en las diferentes variables de entorno.
- **Transparencia de la arquitectura**: La documentacion de una arquitectura necesita proporcionar componentes e interfaces claros y comprensibles que den observabilidad y controlabilidad en todos los niveles de prueba y fomenten la calidad.

#### 2.1.2 Explicar Como se Aprovecha la Automatizacion de Pruebas dentro de Diferentes Entornos

Diferentes tipos de pruebas automatizadas pueden ejecutarse en diferentes entornos. Estos entornos pueden diferir entre proyectos y metodologias, y la mayoria de los proyectos tienen uno o mas entornos para utilizar en las pruebas. Desde un punto de vista tecnico, estos entornos pueden crearse a partir de contenedores, software de virtualizacion y otros enfoques.

Un conjunto de posibles entornos a considerar incluye los siguientes:

**Entorno de desarrollo local**

Un entorno de desarrollo local es donde el software se crea inicialmente y los componentes se prueban con automatizacion para verificar la idoneidad funcional. Varios tipos de pruebas pueden ocurrir en el entorno de desarrollo local incluyendo pruebas de componentes, pruebas de GUI y pruebas de interfaz de programacion de aplicaciones (API). Tambien es importante notar que al usar un entorno de desarrollo integrado (IDE) en la computadora dada, se pueden realizar pruebas de caja blanca para identificar problemas de codificacion y calidad lo mas pronto posible.

**Entorno de compilacion (Build)**

Su proposito principal es compilar el software y ejecutar pruebas que verifican la correccion de la compilacion resultante en un ecosistema DevOps. Este entorno puede ser un entorno de desarrollo local o un agente de integracion continua/entrega continua (CI/CD) donde se pueden realizar pruebas de bajo nivel (es decir, pruebas de componentes y pruebas de integracion de componentes) y analisis estatico sin despliegue real a otros entornos.

**Entorno de integracion**

Despues de realizar pruebas de bajo nivel y analisis estatico, la siguiente etapa es un entorno de integracion del sistema. Aqui, esta presente un candidato a release del SUT que esta completamente integrado con otros sistemas que pueden probarse. En este entorno se puede ejecutar una suite de pruebas completamente automatizada, ya sea pruebas de UI o pruebas de API. En este entorno no hay pruebas de caja blanca, solo pruebas de caja negra (es decir, integracion de sistema y/o pruebas de aceptacion). Es importante notar que este es el primer entorno donde la monitorizacion debe estar presente para ver que sucede en segundo plano durante el uso del SUT para permitir una investigacion eficiente de defectos/fallos.

**Entorno de preproduccion**

Un entorno de preproduccion se usa principalmente para evaluar caracteristicas de calidad no funcionales (por ejemplo, eficiencia del rendimiento). Aunque las pruebas no funcionales pueden realizarse en cualquier entorno, hay un enfoque extra en preproduccion porque se asemeja a produccion lo mas posible. A menudo, las pruebas de aceptacion del usuario pueden ser realizadas por las partes interesadas del negocio para verificar el producto final y es posible ejecutar la suite de pruebas automatizadas existente aqui tambien, si es necesario. Este entorno tambien esta monitorizado.

**Entorno de produccion/operacional**

Un entorno de produccion puede usarse para evaluar caracteristicas de calidad funcionales y no funcionales en tiempo real mientras los usuarios interactuan con un sistema desplegado, con monitorizacion y ciertas mejores practicas que habilitan las pruebas en produccion (por ejemplo, despliegue canario, despliegue blue/green y pruebas A/B).

---

### 2.2 Proceso de Evaluacion para Seleccionar las Herramientas y Estrategias Adecuadas

#### 2.2.1 Analizar un Sistema Bajo Prueba para Determinar la Solucion de Automatizacion de Pruebas Apropiada

Cada SUT puede ser diferente uno de otro, pero hay varios factores y caracteristicas que pueden analizarse para tener una solucion de automatizacion de pruebas (TAS) exitosa. Durante la investigacion de un SUT, los TAEs necesitan reunir requisitos considerando su alcance y capacidades dadas. Diferentes tipos de aplicaciones (por ejemplo, servicio web, movil y web) necesitan diferentes tipos de automatizacion de pruebas desde un punto de vista tecnico. La investigacion se puede hacer - y se recomienda - en colaboracion con otras partes interesadas (por ejemplo, testers manuales, partes interesadas del negocio y analistas de negocio) para identificar tantos riesgos y sus mitigaciones como sea posible para tener una solucion de automatizacion de pruebas beneficiosa para el futuro.

Los requisitos para un enfoque y arquitectura de automatizacion de pruebas deben considerar lo siguiente:

- Que actividades del proceso de prueba deben automatizarse (por ejemplo, gestion de pruebas, diseno de pruebas, generacion de pruebas y ejecucion de pruebas)
- Que niveles de prueba deben soportarse
- Que tipos de prueba deben soportarse
- Que roles y conjuntos de habilidades de prueba deben soportarse
- Que productos de software, lineas de productos y familias deben soportarse (por ejemplo, para definir el alcance y vida util del TAS implementado)
- Que tipo de SUTs necesitan ser compatibles con el TAS
- Disponibilidad de datos de prueba y su calidad
- Posibles metodos y formas de emular casos inalcanzables (por ejemplo, aplicaciones de terceros involucradas)

#### 2.2.2 Ilustrar los Hallazgos Tecnicos de una Evaluacion de Herramientas

Despues de que el SUT se analiza y los requisitos se han recopilado de todas las partes interesadas, es probable que haya herramientas de automatizacion de pruebas que cumplan estos requisitos que puedan considerarse. Puede que no exista una sola herramienta que se ajuste a todos los requisitos identificados, y las partes interesadas deben reconocer esta posibilidad.

Es util capturar los hallazgos sobre las posibles herramientas y reflexionar sobre los diversos requisitos directos e indirectos en una tabla de comparacion. El objetivo de la tabla de comparacion es permitir a las partes interesadas ver las diferencias entre las herramientas basadas en requisitos especificos. La tabla de comparacion lista las herramientas en las columnas y los requisitos en las filas. Las celdas contienen informacion sobre las propiedades de cada herramienta respecto a cada requisito y sobre las prioridades.

En general, las herramientas de automatizacion de pruebas deben evaluarse para determinar si se ajustan a los requisitos identificados en la seccion anterior (2.2.1). Los requisitos a considerar al evaluar y comparar las herramientas incluyen:

- El lenguaje/tecnologia de la herramienta y las herramientas del IDE
- La capacidad de configurar una herramienta, si soporta diferentes entornos de prueba, configuraciones de ejecucion y usa valores de configuracion dinamicos o estaticos
- La capacidad de gestionar datos de prueba dentro de la herramienta. La gestion de datos de prueba podria integrarse con un repositorio central para control de versiones
- Para diferentes tipos de prueba, puede ser necesario seleccionar diferentes herramientas de automatizacion de pruebas
- La capacidad de proporcionar funcionalidad de reportes. Esto es importante para alinearse con los requisitos de reportes de prueba del proyecto
- La capacidad de integrarse con otras herramientas usadas en el proyecto o la organizacion, como CI/CD, seguimiento de tareas, gestion de pruebas, reportes u otras herramientas
- La capacidad de expandir la arquitectura general de pruebas y evaluar la escalabilidad, mantenibilidad, modificabilidad, compatibilidad y confiabilidad de las herramientas

Esta tabla de comparacion es una buena fuente para determinar una herramienta o conjunto de herramientas propuesto para usar en la automatizacion de pruebas del SUT.

El proceso puede variar en cuanto a como se toma la decision sobre que herramienta(s) se usaran, pero la propuesta debe demostrarse a las partes interesadas apropiadas para su aprobacion.

---

## 3. Arquitectura de Automatizacion de Pruebas – 210 minutos (K3)

**Palabras clave**: desarrollo guiado por comportamiento, captura/reproduccion, pruebas guiadas por datos, arquitectura generica de automatizacion de pruebas, pruebas guiadas por palabras clave, scripting lineal, pruebas basadas en modelos, scripting estructurado, capa de adaptacion de pruebas, framework de automatizacion de pruebas, solucion de automatizacion de pruebas, arnes de pruebas, script de prueba, testware, paso de prueba, desarrollo guiado por pruebas

### Objetivos de Aprendizaje para el Capitulo 3:

**3.1 Conceptos de Diseno Aprovechados en la Automatizacion de Pruebas**
- TAE-3.1.1 (K2) Explicar las capacidades principales en una arquitectura de automatizacion de pruebas
- TAE-3.1.2 (K2) Explicar como disenar una solucion de automatizacion de pruebas
- TAE-3.1.3 (K3) Aplicar el uso de capas en los frameworks de automatizacion de pruebas
- TAE-3.1.4 (K3) Aplicar diferentes enfoques para automatizar casos de prueba
- TAE-3.1.5 (K3) Aplicar principios de diseno y patrones de diseno en la automatizacion de pruebas

---

### 3.1 Conceptos de Diseno Aprovechados en la Automatizacion de Pruebas

#### 3.1.1 Explicar las Capacidades Principales en una Arquitectura de Automatizacion de Pruebas

**Arquitectura Generica de Automatizacion de Pruebas (gTAA)**

La gTAA es un concepto de diseno de alto nivel que proporciona una vista abstracta de la comunicacion entre la automatizacion de pruebas y los sistemas a los que esta conectada, es decir, el SUT, la gestion de proyectos, la gestion de pruebas y la gestion de configuracion (ver figura 1). Tambien proporciona las capacidades que son necesarias cubrir al disenar una arquitectura de automatizacion de pruebas (TAA).

Las interfaces de la gTAA describen lo siguiente:

- La **interfaz del SUT** describe la conexion entre el SUT y el TAF (ver seccion 3.1.3 respecto al framework de automatizacion de pruebas)
- La **interfaz de gestion de proyectos** describe el progreso del desarrollo de la automatizacion de pruebas
- La **interfaz de gestion de pruebas** describe el mapeo de las definiciones de casos de prueba y los casos de prueba automatizados
- La **interfaz de gestion de configuracion** describe los pipelines CI/CD, los entornos y el testware

**Capacidades proporcionadas por herramientas y librerias de automatizacion de pruebas**

Las capacidades principales de automatizacion de pruebas deben identificarse y seleccionarse de las herramientas disponibles segun sea necesario para un proyecto dado:

- **Generacion de pruebas**: Soporta el diseno automatizado de casos de prueba basado en un modelo de prueba. Las herramientas de pruebas basadas en modelos pueden aprovecharse en el proceso de generacion (ver el Syllabus ISTQB CT-MBT). La generacion de pruebas es una capacidad opcional.

- **Definicion de pruebas**: Soporta la definicion e implementacion de casos de prueba y/o suites de prueba, que opcionalmente pueden derivarse de un modelo de prueba. Separa la definicion de la prueba del SUT y/o de las herramientas de prueba. Contiene los medios para definir pruebas de alto nivel y bajo nivel, que se manejan en los componentes de datos de prueba, casos de prueba y libreria de pruebas o combinaciones de estos.

- **Ejecucion de pruebas**: Soporta la ejecucion de pruebas y el registro de pruebas. Proporciona una herramienta de ejecucion de pruebas para ejecutar las pruebas seleccionadas automaticamente, y un componente de registro y reporte de pruebas.

- **Adaptacion de pruebas**: Proporciona la funcionalidad necesaria para adaptar las pruebas automatizadas a los diversos componentes o interfaces del SUT. Proporciona diferentes adaptadores para conectar con el SUT a traves de APIs, protocolos y servicios.

#### 3.1.2 Explicar Como Disenar una Solucion de Automatizacion de Pruebas

Una Solucion de Automatizacion de Pruebas (TAS) se define por una comprension de los requisitos funcionales, no funcionales y tecnicos del SUT, las herramientas existentes o requeridas que son necesarias para implementar una solucion. Un TAS se implementa con herramientas comerciales o de codigo abierto y puede necesitar adaptadores adicionales especificos del SUT.

La TAA define el diseno tecnico para el TAS general. Debe abordar:

- Seleccionar herramientas de automatizacion de pruebas y librerias especificas de las herramientas
- Desarrollar plugins y/o componentes
- Identificar requisitos de conectividad e interfaces (por ejemplo, firewalls, bases de datos, URLs/conexiones, mocks/stubs, colas de mensajes y protocolos)
- Conectar con las herramientas de gestion de pruebas y gestion de defectos
- Utilizar un sistema de control de versiones y repositorios

#### 3.1.3 Aplicar el Uso de Capas en los Frameworks de Automatizacion de Pruebas

**Framework de Automatizacion de Pruebas (TAF)**

El TAF es la base de un TAS. A menudo incluye un arnes de pruebas (test harness), tambien conocido como ejecutor de pruebas (test runner), y librerias de pruebas, scripts de prueba y suites de prueba.

**Capas del TAF**

Las capas del TAF definen un limite distinto de clases que tienen propositos similares como casos de prueba, reportes de prueba, registro de prueba, encriptacion y arneses de prueba. Al introducir una capa para cada proposito individual, el diseno puede volverse complicado. Por lo tanto, se recomienda mantener bajo el numero de capas del TAF.

**Scripts de prueba**

Su proposito es proporcionar un repositorio de casos de prueba del SUT y anotaciones de suites de prueba. Llama a los servicios de la capa de logica de negocio que puede involucrar pasos de prueba, flujos de usuario o llamadas API. Sin embargo, no deben hacerse llamadas directas a las librerias principales desde los scripts de prueba.

**Logica de negocio**

Todas las librerias dependientes del SUT se almacenan en esta capa. Estas librerias heredaran los archivos de clase de las librerias principales o usaran las fachadas proporcionadas por ellas (ver seccion 3.1.5 respecto a herencia y fachadas). La capa de logica de negocio se usa para configurar el TAF para ejecutar contra el SUT y las configuraciones adicionales.

**Librerias principales (Core libraries)**

Todas las librerias que son independientes de cualquier SUT se almacenan en esta capa. Estas librerias principales pueden reutilizarse en cualquier tipo de proyecto que comparta la misma pila de desarrollo.

**Escalando la automatizacion de pruebas**

El ejemplo (figura 3) muestra como las librerias principales proporcionan una base reutilizable para multiples TAFs. En el Proyecto #1 hay dos TAFs construidos sobre las librerias principales, y un proyecto separado aprovecha las librerias principales ya existentes para construir su TAF para probar la App #3. Un TAE construye los TAFs para el Proyecto #1, mientras que un segundo TAE construye el TAF para el Proyecto #2.

#### 3.1.4 Aplicar Diferentes Enfoques para Automatizar Casos de Prueba

Hay varios enfoques de desarrollo que los equipos pueden elegir para producir casos de prueba automatizados. Estos pueden incluir lenguajes de scripting interactivos o lenguajes de programacion compilados. Los diferentes enfoques proporcionan diferentes beneficios de automatizacion y pueden aprovecharse en diferentes circunstancias. Aunque el desarrollo guiado por pruebas (TDD) y el desarrollo guiado por comportamiento (BDD) son metodologias de desarrollo, si se siguen correctamente, resultan en el desarrollo de casos de prueba automatizados.

**Captura/reproduccion (Capture/playback)**

La captura/reproduccion es un enfoque que captura las interacciones con el SUT mientras se realiza manualmente una secuencia de acciones. Estas herramientas producen scripts de prueba durante la captura, y dependiendo de la herramienta usada, el codigo de automatizacion de pruebas puede ser modificable. Las herramientas que no exponen codigo a veces se denominan automatizacion de pruebas sin codigo (no-code), mientras que las herramientas que exponen codigo se denominan automatizacion de pruebas de bajo codigo (low-code).

| | Pros | Contras |
|---|------|---------|
| | Inicialmente facil de configurar y usar | Dificil de mantener, escalar y evolucionar |
| | | El SUT necesita estar disponible mientras se captura un caso de prueba |
| | | Solo factible para un alcance pequeno y un SUT que raramente cambia |
| | | La ejecucion capturada del SUT depende altamente de la version del SUT desde la cual se tomo la captura |
| | | Grabar cada caso de prueba individual en lugar de reutilizar bloques existentes consume tiempo |

**Scripting lineal**

El scripting lineal es una actividad de programacion que no requiere librerias de prueba personalizadas hechas por un TAE y se usa para escribir y ejecutar los scripts de prueba. Un TAE puede aprovechar cualquier script de prueba grabado por una herramienta de captura/reproduccion, que luego puede modificarse.

| | Pros | Contras |
|---|------|---------|
| | Facil de configurar y comenzar a escribir scripts | Dificil de mantener, escalar y evolucionar |
| | Los scripts pueden modificarse mas facilmente comparado con captura/reproduccion | El SUT necesita estar disponible mientras se captura un caso de prueba |
| | | Solo factible para un alcance pequeno y un SUT que raramente cambia |
| | | Se necesita algun conocimiento de programacion comparado con captura/reproduccion |

**Scripting estructurado**

Se introducen librerias de prueba con elementos reutilizables, pasos de prueba y/o flujos de usuario. El conocimiento de programacion es necesario para la creacion y mantenimiento de scripts de prueba en este enfoque.

| | Pros | Contras |
|---|------|---------|
| | Facil de mantener, escalar, portar, adaptar y evolucionar | El conocimiento de programacion es necesario |
| | La logica de negocio puede separarse de los scripts de prueba | La inversion inicial en el desarrollo del TAF y la definicion del testware consume tiempo |

**Desarrollo guiado por pruebas (TDD)**

Los casos de prueba se definen como parte del proceso de desarrollo antes de que se implemente una nueva caracteristica del SUT. El enfoque TDD es prueba, codigo y refactorizacion, o tambien conocido como rojo, verde y refactorizacion. Un desarrollador identifica y crea un caso de prueba que fallara (rojo). Luego desarrolla la funcionalidad que satisfara el caso de prueba (verde). El codigo luego se refactoriza para optimizarlo y cumplir con los principios de codigo limpio. El proceso continua con la siguiente prueba y el siguiente incremento de funcionalidad.

| | Pros | Contras |
|---|------|---------|
| | Simplifica el desarrollo de casos de prueba a nivel de componente | Inicialmente toma mas tiempo acostumbrarse a TDD |
| | Mejora la calidad y estructura del codigo | No seguir TDD correctamente puede resultar en falsa confianza en la calidad del codigo |
| | Mejora la testabilidad | |
| | Facilita lograr una cobertura de codigo deseada | |
| | Reduce la propagacion de defectos a niveles de prueba superiores | |
| | Mejora la comunicacion entre desarrolladores, representantes de negocio y testers | |
| | Las historias de usuario que no se verifican usando pruebas de GUI y API pueden lograr rapidamente los criterios de salida siguiendo TDD | |

**Pruebas guiadas por datos (Data-driven testing - DDT)**

Las pruebas guiadas por datos se basan en el enfoque de scripting estructurado. Los scripts de prueba se proporcionan con datos de prueba (por ejemplo, archivos .csv, archivos .xlsx y volcados de base de datos). Esto permite ejecutar los mismos scripts de prueba multiples veces con diferentes datos de prueba.

| | Pros | Contras |
|---|------|---------|
| | Permite la expansion rapida y facil de casos de prueba a traves de fuentes de datos | Puede ser necesaria una gestion adecuada de datos de prueba |
| | El costo de agregar nuevas pruebas automatizadas puede reducirse significativamente | |
| | Los analistas de pruebas pueden especificar pruebas automatizadas poblando uno o mas archivos de datos de prueba que describen las pruebas, dandoles mas libertad con menos dependencia de los analistas tecnicos de pruebas | |

**Pruebas guiadas por palabras clave (Keyword-driven testing - KDT)**

Los casos de prueba de KDT son una lista o tabla de pasos de prueba derivados de palabras clave y los datos de prueba sobre los que operan las palabras clave. Las palabras clave se definen desde la perspectiva del usuario. Esta tecnica a menudo se construye sobre DDT.

| | Pros | Contras |
|---|------|---------|
| | Los analistas de pruebas y analistas de negocio pueden involucrarse en la creacion de casos de prueba automatizados siguiendo el enfoque KDT | Implementar y mantener las palabras clave es una tarea compleja que los TAEs necesitan cubrir, lo cual puede volverse desafiante cuando el alcance crece |
| | KDT tambien puede usarse para pruebas manuales independientemente de la automatizacion de pruebas (ver el Estandar ISO/IEC/IEEE 29119-5 respecto a Pruebas Guiadas por Palabras Clave) | Crea un esfuerzo enorme para sistemas mas pequenos |

**Desarrollo Guiado por Comportamiento (BDD)**

BDD aprovecha un formato de lenguaje natural (es decir, dado, cuando y entonces / given, when, then) para formular criterios de aceptacion que pueden usarse como casos de prueba automatizados y almacenarse en archivos de caracteristicas (feature files). Una herramienta BDD puede entonces entender el lenguaje y ejecutar los casos de prueba.

| | Pros | Contras |
|---|------|---------|
| | Mejora la comunicacion entre desarrolladores, representantes de negocio y testers | Los casos de prueba adicionales, tipicamente condiciones de prueba negativas y casos limite, aun necesitan ser definidos por el equipo |
| | Los escenarios BDD automatizados actuan como casos de prueba y aseguran la cobertura de especificaciones | Muchos equipos confunden BDD con solo una forma de escribir casos de prueba en lenguaje natural, sin involucrar a los representantes de negocio y desarrolladores |
| | BDD puede aprovecharse para producir multiples tipos de prueba en diferentes niveles de la piramide de pruebas | Implementar y mantener los pasos de prueba en lenguaje natural es una tarea compleja para los TAEs |
| | | Los pasos de prueba excesivamente complejos convertiran la depuracion en una actividad dificil y costosa |

#### 3.1.5 Aplicar Principios de Diseno y Patrones de Diseno en la Automatizacion de Pruebas

La automatizacion de pruebas es una actividad de desarrollo de software. Por lo tanto, los principios de diseno y patrones de diseno son tan importantes para un TAE como para un desarrollador de software.

**Principios de programacion orientada a objetos**

Hay cuatro principios principales de programacion orientada a objetos: encapsulamiento, abstraccion, herencia y polimorfismo.

**Principios SOLID**

Es un acronimo de responsabilidad unica (Single responsibility), abierto-cerrado (Open-closed), sustitucion de Liskov (Liskov substitution), segregacion de interfaces (Interface segregation) e inversion de dependencias (Dependency inversion). Estos principios mejoran la legibilidad, mantenibilidad y escalabilidad del codigo.

**Patrones de diseno**

De los muchos patrones de diseno, tres son los mas importantes para los TAEs:

- El **patron fachada (facade)** oculta los detalles de implementacion para exponer solo lo que los testers necesitan crear en los casos de prueba
- El **patron singleton** se usa a menudo para asegurar que solo hay un driver que se comunica con el SUT

En el **modelo de objeto de pagina (page object model)**, se crea un archivo de clase y se refiere como un modelo de pagina. Siempre que la estructura del SUT cambie, el TAE solo tendra que hacer actualizaciones en un lugar, el localizador dentro de un modelo de pagina, en lugar de actualizar los localizadores en cada caso de prueba.

El **patron de modelo de flujo (flow model pattern)** es una expansion del modelo de objeto de pagina. Introduce una fachada adicional sobre los modelos de objeto de pagina, que almacena todas las acciones del usuario que interactuan con los objetos de pagina. Al introducir un diseno de doble fachada, el patron de modelo de flujo proporciona una abstraccion y mantenibilidad mejoradas ya que los pasos de prueba pueden reutilizarse en multiples scripts de prueba.

---

## 4. Implementacion de la Automatizacion de Pruebas – 150 minutos (K4)

**Palabras clave**: riesgo, fixture de prueba

### Objetivos de Aprendizaje para el Capitulo 4:

**4.1 Desarrollo de la Automatizacion de Pruebas**
- TAE-4.1.1 (K3) Aplicar directrices que soporten actividades efectivas de piloto y despliegue de automatizacion de pruebas

**4.2 Riesgos Asociados al Desarrollo de la Automatizacion de Pruebas**
- TAE-4.2.1 (K4) Analizar riesgos de despliegue y planificar estrategias de mitigacion para la automatizacion de pruebas

**4.3 Mantenibilidad de la Solucion de Automatizacion de Pruebas**
- TAE-4.3.1 (K2) Explicar que factores soportan y afectan la mantenibilidad de la solucion de automatizacion de pruebas

---

### 4.1 Desarrollo de la Automatizacion de Pruebas

#### 4.1.1 Aplicar Directrices que Soporten Actividades Efectivas de Piloto y Despliegue de Automatizacion de Pruebas

Es importante definir el alcance de validacion para un piloto de automatizacion de pruebas. Un proyecto piloto no toma mucho tiempo en realizarse, pero el resultado puede tener un impacto significativo en la direccion que toma el proyecto. Basado en la informacion recopilada sobre el SUT y los requisitos del proyecto, se debe evaluar lo siguiente para establecer directrices que optimicen los esfuerzos de automatizacion de pruebas:

- Lenguaje(s) de programacion que se usaran
- Herramientas comerciales/de codigo abierto adecuadas
- Niveles de prueba a cubrir
- Casos de prueba seleccionados
- Enfoque de desarrollo de casos de prueba

Basado en los puntos anteriores, los TAEs pueden definir un enfoque inicial a seguir. Basado en los requisitos, se pueden crear varios prototipos iniciales diferentes para mostrar los pros y contras de los diferentes enfoques. A partir de ahi, los TAEs pueden decidir que camino seguir.

Definir cronogramas es una parte importante para cumplir los plazos y asegurar el exito del piloto. Una recomendacion comun es verificar periodicamente el progreso del proyecto piloto para identificar cualquier riesgo y mitigarlo.

Durante el piloto, tambien se recomienda intentar integrar la solucion y el codigo ya implementado en el CI/CD. Esto puede exponer problemas tempranamente, ya sea en el SUT, el TAS o en la integracion general de diferentes herramientas dentro de la organizacion.

A medida que crece el numero de casos de prueba, los TAEs pueden pensar en cambiar la configuracion inicial de CI/CD para ejecutar las pruebas de diferentes maneras y en diferentes momentos.

Ademas, durante el proyecto piloto, es necesario evaluar otros aspectos no tecnicos, tales como:

- El conocimiento y experiencia de los miembros del equipo
- La estructura del equipo
- Las reglas de licenciamiento y organizacion
- El tipo de pruebas planificadas y los niveles de prueba objetivo a cubrir durante la automatizacion de casos de prueba

Una vez que el proyecto piloto esta completo, el esfuerzo debe evaluarse por los TAEs y los gestores de pruebas para evaluar el exito o fracaso y tomar una decision apropiada.

### 4.2 Riesgos Asociados al Desarrollo de la Automatizacion de Pruebas

#### 4.2.1 Analizar Riesgos de Despliegue y Planificar Estrategias de Mitigacion para la Automatizacion de Pruebas

La interfaz del TAF con el SUT necesita considerarse como parte del diseno arquitectonico. Luego se pueden seleccionar las herramientas de empaquetado, registro de pruebas y arnes de pruebas.

Durante la implementacion del piloto, la expansion y el mantenimiento del codigo de automatizacion de pruebas necesitan considerarse. Estos son factores cruciales de la fase de evaluacion del piloto y pueden afectar seriamente la decision final.

Se pueden identificar diferentes riesgos de despliegue a partir del piloto:

- Aperturas de firewall
- Utilizacion de recursos (por ejemplo, CPU y RAM)

Se debe preparar para riesgos de despliegue como problemas de firewall, utilizacion de recursos, conexion y confiabilidad de red. Estos no estan estrictamente conectados a la automatizacion de pruebas, pero los TAEs necesitan asegurar que todas las condiciones se cumplan para proporcionar puertas de calidad confiables y beneficiosas en su proceso de desarrollo.

Usar dispositivos reales para la automatizacion de pruebas moviles proporciona un ejemplo. Los dispositivos moviles deben estar encendidos, tener suficiente bateria para funcionar durante la prueba, estar conectados a una red y tener acceso al SUT.

Los riesgos tecnicos de despliegue pueden incluir:

**Empaquetado (Packaging)**

El empaquetado debe considerarse ya que el control de versiones de la automatizacion de pruebas es tan importante como para el SUT. El testware puede necesitar subirse a un repositorio para compartirlo en toda la organizacion, ya sea en las instalaciones o en la nube.

**Registro (Logging)**

El registro de pruebas da la mayor parte de la informacion sobre los resultados de las pruebas. Hay varios niveles de registro de pruebas y todos son utiles en la automatizacion de pruebas por varias razones:

- **Fatal**: Este nivel se usa para registrar eventos de error que pueden llevar a abortar la ejecucion de la prueba
- **Error**: Este nivel se usa cuando una condicion o interaccion falla y por lo tanto tambien falla el caso de prueba
- **Warn (Advertencia)**: Este nivel se usa cuando ocurre una condicion/accion inesperada pero no rompe el flujo del caso de prueba
- **Info**: Este nivel se usa para mostrar informacion basica sobre un caso de prueba y lo que sucede durante la ejecucion de la prueba
- **Debug**: Este nivel se usa para almacenar detalles especificos de ejecucion que generalmente no se requieren para los registros basicos, pero son utiles durante la investigacion de un fallo de prueba
- **Trace**: Este nivel es similar a Debug pero tiene aun mas informacion

**Estructuracion de pruebas (Test Structuring)**

La parte mas importante del TAS es el arnes de pruebas y los fixtures de prueba incluidos en el, elementos que deben estar disponibles para que las pruebas se ejecuten. Los fixtures de prueba proporcionan libertad para controlar un entorno de prueba y los datos de prueba. Las precondiciones y postcondiciones pueden definirse para la ejecucion de pruebas y los casos de prueba pueden agruparse en suites de prueba de varias maneras. Estos aspectos tambien son importantes para evaluar durante un proyecto piloto. Ademas, los fixtures de prueba permiten la creacion de pruebas automatizadas que son repetibles y atomicas.

**Actualizacion (Updating)**

Uno de los riesgos tecnicos mas comunes son las actualizaciones automaticas en los arneses de prueba (por ejemplo, agentes) y los cambios de version en los dispositivos. Estos riesgos pueden mitigarse teniendo fuentes de alimentacion adecuadas, conexiones de red apropiadas y planes de configuracion de dispositivos apropiados.

### 4.3 Mantenibilidad de la Solucion de Automatizacion de Pruebas

#### 4.3.1 Explicar que Factores Soportan y Afectan la Mantenibilidad de la Solucion de Automatizacion de Pruebas

La mantenibilidad esta altamente afectada por los estandares de programacion y las expectativas de los TAEs entre si.

Una regla de oro es intentar seguir los principios de codigo limpio de Robert C. Martin ("Clean Code: A Handbook of Agile Software Craftsmanship", 2008).

Brevemente, los principios de codigo limpio enfatizan los siguientes puntos:

- Usar una convencion de nombres comun para las clases, metodos y variables con nombres significativos
- Usar una estructura de proyecto logica y comun
- Evitar el hardcoding
- Evitar demasiados parametros de entrada para los metodos
- Evitar metodos largos y complejos
- Usar registro (logging)
- Usar patrones de diseno donde sean beneficiosos y requeridos
- Enfocarse en la testabilidad

Las convenciones de nombres son muy utiles para identificar el objetivo de una variable dada. Tener nombres de variables comprensibles como "loginButton", "resetPasswordButton" ayuda a los TAEs a entender que componente usar.

El hardcoding es el proceso de incrustar valores en el software sin la capacidad de cambiarlos directamente. Puede evitarse usando pruebas guiadas por datos, de modo que los datos de prueba provienen de una fuente comun que puede mantenerse mas facilmente. El hardcoding reduce el tiempo de desarrollo, pero no se recomienda usarlo ya que los datos pueden cambiar frecuentemente, lo cual puede consumir tiempo en mantenimiento. Usar constantes para aquellas variables que no se espera que cambien frecuentemente tambien es aconsejable. Al hacerlo, las fuentes y lugares que necesitan mantenerse pueden reducirse.

Aprovechar los patrones de diseno tambien es altamente recomendado. Los patrones de diseno, como se describen en la seccion 3.1.5, permiten implementar un codigo de automatizacion de pruebas estructurado y adecuadamente mantenible, siempre que los patrones de diseno se usen correctamente.

Para asegurar la alta calidad del codigo de automatizacion de pruebas, se recomienda hacer uso de analizadores estaticos. Los formateadores de codigo como los comumente usados en los IDEs mejoraran la legibilidad del codigo de automatizacion de pruebas.

Aparte de los principios de codigo limpio, se recomienda usar una estructura y estrategia de ramas acordada en el control de versiones. Usar diferentes ramas para caracteristicas, releases y correcciones de defectos es util para entender el contenido de las ramas.

---

## 5. Estrategias de Implementacion y Despliegue para la Automatizacion de Pruebas – 90 minutos (K3)

**Palabras clave**: pruebas de contrato

### Objetivos de Aprendizaje para el Capitulo 5:

**5.1 Integracion en Pipelines CI/CD**
- TAE-5.1.1 (K3) Aplicar la automatizacion de pruebas en diferentes niveles de prueba dentro de los pipelines
- TAE-5.1.2 (K2) Explicar la gestion de configuracion para el testware
- TAE-5.1.3 (K2) Explicar las dependencias de la automatizacion de pruebas para una infraestructura de API

---

### 5.1 Integracion en Pipelines CI/CD

#### 5.1.1 Aplicar la Automatizacion de Pruebas en Diferentes Niveles de Prueba dentro de los Pipelines

Uno de los principales beneficios de la automatizacion de pruebas es que las pruebas implementadas pueden ejecutarse sin supervision, haciendolas candidatas ideales para ejecutar dentro de los pipelines. Esto puede lograrse a traves de pipelines CI/CD o el pipeline usado para ejecutar las pruebas regularmente.

Los niveles de prueba usualmente se integran de la siguiente manera:

- Las **pruebas de configuracion** para TAF/TAS, durante la compilacion, pueden considerarse como una subespecie de pruebas de componentes. Estas pruebas se ejecutan durante la compilacion de un proyecto de automatizacion de pruebas (TAF/TAS) y verifican que todas las rutas a los archivos usados en los scripts de prueba son correctas, que los archivos realmente existen y estan ubicados en las rutas especificadas.

- Las **pruebas de componentes** son parte del paso de compilacion del pipeline, ya que se ejecutan en los componentes individuales (por ejemplo, clases de libreria y componentes web). Actuan como puertas de calidad para el pipeline, siendo una parte crucial de un pipeline de integracion continua.

- Las **pruebas de integracion de componentes** pueden ser parte del pipeline de integracion continua si son pruebas de componentes de bajo nivel o del SUT. En tales casos, estas pruebas y las pruebas de componentes se ejecutan juntas.

- Las **pruebas de sistema** a menudo pueden integrarse en un pipeline de despliegue continuo, donde actuan como la ultima puerta de calidad del SUT entregado.

- Las **pruebas de integracion de sistema** entre diferentes componentes del sistema son a menudo parte de un pipeline de entrega continua como puertas de calidad. Estas pruebas de integracion de sistema aseguran que los componentes del sistema desarrollados por separado funcionen juntos.

Muchos sistemas modernos de integracion continua diferencian entre las fases de compilacion y despliegue de los pipelines de entrega continua. En estos casos, las pruebas de componentes y las pruebas de integracion de componentes son parte de la primera fase de compilacion. Cuando esta primera fase es exitosa (es decir, compilacion y prueba juntas), los componentes/SUT se despliegan.

En el caso de pruebas de integracion de sistema, pruebas de sistema y pruebas de aceptacion, hay dos enfoques principales para integrarlas en tales pipelines:

1. Los casos de prueba se ejecutan como parte de la fase de despliegue despues del despliegue de componentes. Esto puede ser beneficioso, ya que basandose en los resultados de las pruebas, el despliegue puede fallar y tambien revertirse. Sin embargo, en este caso, si las pruebas necesitan re-ejecutarse, se necesita hacer un redespliegue.

2. Los casos de prueba se ejecutan como un pipeline separado, disparado por el despliegue exitoso. Esto puede ser beneficioso si se espera que diferentes suites de prueba y varios codigos de automatizacion de pruebas se ejecuten en cada despliegue. En este caso, las pruebas no actuan como una puerta de calidad. Por lo tanto, requiere otras acciones, usualmente manuales, para revertir un despliegue no exitoso.

Los pipelines tambien pueden usarse para otros propositos de automatizacion de pruebas, tales como:

- **Ejecutar diferentes suites de prueba periodicamente**: Una suite de pruebas de regresion puede ejecutarse cada noche (es decir, la regresion nocturna), especialmente para suites de prueba de ejecucion prolongada, para que el equipo tenga una imagen clara de la calidad del SUT por la manana.
- **Ejecutar pruebas no funcionales**: Ya sea como parte de un pipeline de despliegue continuo o por separado, para monitorizar periodicamente ciertas caracteristicas de calidad no funcionales del sistema como la eficiencia del rendimiento.

#### 5.1.2 Explicar la Gestion de Configuracion para el Testware

La gestion de configuracion es una parte integral de la automatizacion de pruebas, ya que la automatizacion a menudo se ejecuta en multiples entornos de prueba y versiones del SUT.

La gestion de configuracion en la automatizacion de pruebas incluye:

**Configuracion del entorno de prueba**

Cada entorno de prueba usado en el pipeline de desarrollo puede tener diferentes configuraciones, como varias URLs o credenciales. La configuracion del entorno de prueba usualmente se almacena con el testware. Sin embargo, en el caso de la automatizacion de pruebas usada en multiples proyectos o multiples TAFs para el mismo proyecto, la configuracion del entorno de prueba puede ser parte de la libreria principal comun o de un repositorio compartido.

**Datos de prueba**

Los datos de prueba tambien pueden ser especificos para el entorno de prueba o para la release y el conjunto de caracteristicas del SUT. Al igual que con la configuracion del entorno de prueba, los datos de prueba usualmente se almacenan con TAFs mas pequenos, pero tambien pueden usarse sistemas de gestion de datos de prueba.

**Suites de prueba/casos de prueba**

Una practica comun es configurar diferentes suites de prueba de los casos de prueba, basadas en su proposito, como pruebas de humo o pruebas de regresion. Estas suites de prueba a menudo se ejecutan en niveles de prueba separados, aprovechando diferentes pipelines y entornos de prueba.

Cada release del SUT determina un conjunto de caracteristicas que incluye casos de prueba y suites de prueba que evaluan la calidad de la release dada. Hay diferentes opciones en el testware para manejar esto:

- Un **feature toggle** puede definirse por cada release o entorno de prueba. Hay casos de prueba y suites de prueba para probar cada caracteristica. El feature toggle puede usarse en el testware para identificar que suites de prueba ejecutar en una release/entorno de prueba dado.

- El testware tambien puede **liberarse con el SUT** usando la misma version de release. De esta forma, hay una coincidencia exacta entre la version del SUT y el testware que puede probarlo. Tal release usualmente se implementa usando un sistema de gestion de configuracion con tags o ramas.

#### 5.1.3 Explicar las Dependencias de la Automatizacion de Pruebas para una Infraestructura de API

Al realizar la automatizacion de pruebas de API, es crucial tener la siguiente informacion sobre las dependencias para construir una estrategia adecuada:

- **Conexiones de API**: Comprender la logica de negocio que puede probarse automaticamente y la relacion entre las APIs
- **Documentacion de API**: Sirve como linea base para la automatizacion de pruebas con toda la informacion relevante (por ejemplo, parametros, encabezados y tipos distintos de objetos de solicitud-respuesta)

Las pruebas de API integradas y automatizadas pueden ser realizadas por los desarrolladores o los TAEs. Sin embargo, con el desplazamiento a la izquierda (shift left) se recomienda soportar y dividir las pruebas entre diferentes niveles. En el Syllabus ISTQB CTFL, se mencionan las pruebas de integracion de componentes y las pruebas de integracion de sistema, que pueden extenderse con una mejor practica llamada pruebas de contrato.

**Pruebas de contrato (Contract testing)**

Las pruebas de contrato son un tipo de prueba de integracion que verifica que los servicios pueden comunicarse entre si y que los datos compartidos entre los servicios son consistentes con un conjunto especificado de reglas. Usar pruebas de contrato proporciona compatibilidad entre dos sistemas separados (por ejemplo, dos microservicios) para comunicarse uno con otro. Va mas alla de la validacion de esquema, requiriendo que ambas partes lleguen a un consenso sobre el conjunto permitido de interacciones mientras se permite la evolucion a lo largo del tiempo. Captura las interacciones que se intercambian entre cada servicio, almacenandolas en un contrato, que luego puede usarse para verificar que ambas partes se adhieren a el. Una de las principales ventajas de este tipo de prueba es que los defectos que ocurren de los servicios subyacentes pueden encontrarse antes en el SDLC y la fuente de estos defectos puede identificarse mas facilmente.

En el **enfoque impulsado por el consumidor** de las pruebas de contrato, el consumidor establece su expectativa determinando como el proveedor debe responder a las solicitudes provenientes de este consumidor. En el **enfoque impulsado por el proveedor** de las pruebas de contrato, el proveedor crea el contrato, que muestra como operan sus servicios.

---

## 6. Reportes y Metricas de Automatizacion de Pruebas – 150 minutos (K4)

**Palabras clave**: medicion, metrica, registro de prueba, reporte de progreso de prueba, paso de prueba

### Objetivos de Aprendizaje para el Capitulo 6:

**6.1 Recopilacion, Analisis y Reportes de Datos de Automatizacion de Pruebas**
- TAE-6.1.1 (K3) Aplicar metodos de recopilacion de datos de la solucion de automatizacion de pruebas y el sistema bajo prueba
- TAE-6.1.2 (K4) Analizar datos de la solucion de automatizacion de pruebas y el sistema bajo prueba para comprender mejor los resultados
- TAE-6.1.3 (K2) Explicar como se construye y publica un reporte de progreso de pruebas

---

### 6.1 Recopilacion, Analisis y Reportes de Datos de Automatizacion de Pruebas

#### 6.1.1 Aplicar Metodos de Recopilacion de Datos de la Solucion de Automatizacion de Pruebas y el Sistema Bajo Prueba

Los datos pueden recopilarse de las siguientes fuentes:

- **Registros del SUT**: Web/UI movil, APIs, Aplicaciones, Servidores web, Servidores de base de datos
- **Registros del TAF** para proporcionar un rastro de auditoria
- **Registros de compilacion**
- **Registros de despliegue**
- **Registros de produccion** para monitorizar datos en produccion:
  - Monitorizacion de rendimiento en produccion para realizar analisis de tendencias
  - Registros de pruebas de eficiencia de rendimiento en un entorno de pruebas de rendimiento (por ejemplo, pruebas de carga, estres y spike)
- **Capturas de pantalla y grabaciones de pantalla** (nativas de la herramienta de automatizacion o de terceros)

Dado que un TAS tiene testware automatizado en su nucleo, el testware automatizado puede mejorarse para registrar informacion sobre su uso. Las mejoras del testware realizadas al testware subyacente pueden ser usadas por todos los scripts de prueba automatizados de nivel superior. Por ejemplo, mejorar el testware subyacente para registrar el tiempo de inicio y fin de la ejecucion de pruebas puede aplicarse a todas las pruebas.

**Caracteristicas de la automatizacion de pruebas que soportan la medicion y generacion de reportes de prueba**

Los lenguajes de scripting de muchas herramientas de prueba soportan la medicion y los reportes a traves de facilidades que pueden usarse para registrar informacion antes, durante y despues de la ejecucion de pruebas individuales y suites de prueba completas.

Los reportes de prueba en cada una de una serie de ejecuciones de prueba necesitan tener una caracteristica de analisis para considerar los resultados de prueba de las ejecuciones anteriores para poder destacar tendencias, como cambios en la tasa de exito de las pruebas.

La automatizacion de pruebas tipicamente requiere automatizar tanto la ejecucion de la prueba como la verificacion de la prueba, esta ultima se logra comparando elementos especificos de los resultados reales con los resultados esperados. Esta comparacion se hace mejor con una herramienta de prueba usando aserciones. El nivel de informacion que se reporta como resultado de esta comparacion debe considerarse. Es importante que el estado de la prueba se determine correctamente (es decir, aprobada o fallida). En el caso de estado fallido, se requerira mas informacion sobre la causa del fallo (por ejemplo, capturas de pantalla).

**Registro de pruebas (Test logging)**

Los registros de prueba son una fuente que se usa frecuentemente para analizar posibles defectos dentro del TAS y el SUT.

**Registro del TAS:**

El contexto determina si el TAF o la ejecucion de pruebas es responsable de registrar informacion que debe incluir lo siguiente:

- Que caso de prueba esta actualmente en ejecucion, incluyendo tiempo de inicio y fin
- El estado de la ejecucion de pruebas: aprobado, fallido o fallo del TAS. El estado a veces puede ser inconcluso y es importante que la organizacion defina definiciones claras y consistentes. Un fallo del TAS se aplica a situaciones donde el defecto no esta en el SUT
- Detalles de bajo nivel del registro de pruebas (por ejemplo, registrar pasos de prueba significativos) incluyendo informacion de tiempo
- Informacion dinamica sobre el SUT (por ejemplo, fugas de memoria) que el caso de prueba pudo identificar con la ayuda de herramientas de terceros
- En el caso de pruebas de confiabilidad o pruebas de estres donde se realizan numerosos ciclos de prueba, debe registrarse un contador
- Cuando los casos de prueba tienen elementos aleatorios, deben registrarse los numeros/opciones aleatorios
- Todas las acciones que realiza un caso de prueba deben registrarse de tal manera que los registros puedan reproducirse para re-ejecutar la prueba con los mismos pasos y el mismo tiempo
- Las capturas de pantalla pueden guardarse durante la ejecucion de pruebas para uso posterior durante el analisis de causa raiz
- Siempre que una suite de pruebas inicie un fallo, el TAS debe asegurarse de que toda la informacion necesaria para analizar el defecto este disponible/almacenada
- El uso de color puede ayudar a distinguir diferentes tipos de informacion de registro de pruebas (por ejemplo, defectos en rojo y progreso en verde)

**Registro del SUT:**

La correlacion de los resultados de automatizacion de pruebas con los registros del SUT ayuda a identificar la causa raiz de defectos en el SUT y el TAS:

- Cuando se identifica un defecto en el SUT, toda la informacion necesaria para analizar el defecto debe registrarse, incluyendo marcas de fecha y hora, ubicacion de la fuente del defecto y mensajes de error
- Al inicio de un sistema, la informacion de configuracion debe registrarse en un archivo
- Usando automatizacion de pruebas, los registros del SUT pueden ser facilmente buscables. Un fallo identificado en el registro de pruebas por el TAS debe ser facilmente identificable en el registro del SUT, y viceversa

**Integracion con otras herramientas de terceros**

Cuando la informacion de la ejecucion de casos de prueba automatizados se usa en otras herramientas para seguimiento y reportes, es posible proporcionar la informacion en un formato adecuado para herramientas de terceros.

**Visualizacion de resultados de pruebas**

Los resultados de pruebas pueden hacerse visibles usando graficos. Considere usar iconos de colores como semaforos para indicar el estado general de la ejecucion/automatizacion de pruebas para que se puedan tomar decisiones basadas en la informacion reportada.

#### 6.1.2 Analizar Datos de la Solucion de Automatizacion de Pruebas y el Sistema Bajo Prueba para Comprender Mejor los Resultados de Pruebas

Despues de la ejecucion de pruebas, es importante analizar los resultados de pruebas para identificar posibles fallo(s) tanto en el SUT como en el TAS. Para tal analisis, los datos recopilados del TAS son primarios y los datos recopilados del SUT son secundarios.

- Analizar los datos del entorno de prueba para soportar el dimensionamiento adecuado de la automatizacion de pruebas (por ejemplo, en la nube)
- Comparar resultados de pruebas de ejecuciones anteriores
- Determinar como usar los registros web para monitorizar el uso del software

Los fallos de ejecucion de pruebas necesitan analizarse, ya que hay problemas potenciales:

1. Verificar si el mismo fallo ocurrio en las ejecuciones de prueba anteriores. Esto podria ser un defecto conocido ya sea en el SUT o el TAS
2. Si el defecto no es conocido, identificar el caso de prueba y que esta probando
3. Encontrar en que paso de prueba del caso de prueba ocurrio el fallo
4. Analizar la informacion del registro de pruebas sobre el estado del SUT y si coincide con los resultados esperados
5. Si el estado del SUT no es lo esperado, registrar un defecto en el sistema de gestion de defectos

Si el SUT implementa registros de auditoria para interacciones de usuario (es decir, sesiones de UI o llamadas API), ayuda a analizar los resultados de pruebas. Usualmente hay un ID unico anadido a la interaccion con el mismo ID para cada llamada e integracion subsiguiente en el sistema. Este ID unico usualmente se llama **ID de correlacion** o **ID de traza**. Esto puede ser registrado por el TAS para ayudar a analizar los resultados de pruebas.

#### 6.1.3 Explicar Como se Construye y Publica un Reporte de Progreso de Pruebas

Los registros de prueba dan informacion detallada sobre los pasos de prueba, acciones a tomar y respuestas esperadas de un caso de prueba y/o suite de prueba. Sin embargo, los registros de prueba solos no pueden proporcionar una buena vision general de los resultados de prueba. Para esto, es necesario tener funcionalidad de reportes de prueba. Despues de la ejecucion de una suite de prueba, debe crearse y publicarse un reporte de progreso de pruebas conciso. Se puede usar un generador de reportes para esto.

**Contenido de un reporte de progreso de pruebas**

El reporte de progreso de pruebas debe contener los resultados de pruebas, informacion del SUT y documentacion del entorno de pruebas en un formato apropiado para cada una de las partes interesadas.

Es necesario saber que pruebas han fallado y las razones del fallo. Para facilitar la resolucion de problemas, es importante conocer el historial de ejecucion de pruebas y quien lo reporto.

**Publicacion de los reportes de pruebas**

El reporte de pruebas debe publicarse a todas las partes interesadas relevantes. Puede subirse a un sitio web, en la nube o en las instalaciones, enviarse a una lista de correo o subirse a otra herramienta como una herramienta de gestion de pruebas.

Las partes interesadas a reportar incluyen:

- **Partes interesadas de gestion**: Roles tipicos: arquitecto de solucion o empresarial, gerente de proyecto/entrega, gerente de programa, gestor de pruebas o director de pruebas
- **Partes interesadas operacionales**: Roles tipicos: propietario/gerente de producto, representante de negocio o analista de negocio
- **Partes interesadas tecnicas**: Roles tipicos: lider de equipo, scrum master, administrador web, desarrollador/administrador de base de datos, lider de pruebas, TAE, tester o desarrollador

Los reportes de pruebas pueden variar en contenido o detalle dependiendo de los destinatarios. Mientras que las partes interesadas tecnicas pueden estar mas interesadas en detalles de bajo nivel, la gerencia se enfocara en tendencias.

**Creacion de dashboards**

Las herramientas modernas de reportes proporcionan varias opciones de reportes a traves de dashboards, graficos coloridos, colecciones detalladas de registros y analisis automatizado de registros de pruebas. Estas herramientas soportan la agregacion de datos de fuentes como registros de ejecucion de pipelines, herramientas de gestion de proyectos y repositorios de codigo.

**Analisis de registros de prueba con Inteligencia Artificial/aprendizaje automatico**

En anos recientes, algunas herramientas de automatizacion de pruebas incluyen o se basan en algoritmos de aprendizaje automatico (ML). El analisis automatizado de grandes cantidades de datos en registros de prueba ayuda al TAE a reducir el tiempo dedicado a encontrar localizadores rotos, analizar la razon de los fallos de prueba y agrupar defectos comunes para los reportes de prueba.

---

## 7. Verificacion de la Solucion de Automatizacion de Pruebas – 135 minutos (K3)

**Palabras clave**: analisis estatico

### Objetivos de Aprendizaje para el Capitulo 7:

**7.1 Verificacion de la Infraestructura de Automatizacion de Pruebas**
- TAE-7.1.1 (K3) Planificar la verificacion del entorno de automatizacion de pruebas incluyendo la configuracion de herramientas de prueba
- TAE-7.1.2 (K2) Explicar el comportamiento correcto para un script de prueba automatizado y/o suite de prueba dados
- TAE-7.1.3 (K2) Identificar donde la automatizacion de pruebas produce resultados inesperados
- TAE-7.1.4 (K2) Explicar como el analisis estatico puede ayudar a la calidad del codigo de automatizacion de pruebas

---

### 7.1 Verificacion de la Infraestructura de Automatizacion de Pruebas

#### 7.1.1 Planificar la Verificacion del Entorno de Automatizacion de Pruebas Incluyendo la Configuracion de Herramientas de Prueba

Si el entorno de automatizacion de pruebas y todos los demas componentes del TAS funcionan como se espera aun requiere verificacion. Estas verificaciones se hacen, por ejemplo, antes de iniciar la automatizacion de pruebas.

**Instalacion, configuracion y personalizacion de herramientas de prueba**

El TAS esta compuesto por muchos componentes. Cada uno de estos necesita ser confiable para asegurar un rendimiento repetible y confiable. En el nucleo del TAS estan los componentes ejecutables, las librerias de funciones correspondientes y los archivos de datos y configuracion de soporte. El proceso de configurar un TAS puede variar desde el uso de scripts de instalacion automatizados hasta la colocacion manual de archivos en las carpetas correspondientes.

La instalacion automatizada o la copia desde un repositorio tiene ventajas. Puede garantizar que las pruebas en diferentes SUTs se han realizado con la misma version y configuracion del TAS.

**Repetibilidad en la configuracion/desmontaje del entorno de prueba**

Un TAS se implementara en una variedad de sistemas, servidores y para soportar pipelines CI/CD. Para asegurar que el TAS funcione correctamente en cada entorno de prueba, es necesario tener un enfoque sistematico para cargar y descargar el TAS de cualquier entorno de prueba dado.

**Conectividad con sistemas/interfaces internos y externos**

Una vez que un TAS esta instalado en un entorno de SUT dado, y antes de usar el SUT, se debe administrar un conjunto de verificaciones o precondiciones para asegurar que la conectividad a sistemas internos, sistemas externos e interfaces estan disponibles.

**Pruebas de componentes del TAF**

Al igual que cualquier proyecto de desarrollo de software, los componentes del TAF necesitan ser probados y verificados individualmente. Esto puede incluir pruebas funcionales y no funcionales (por ejemplo, eficiencia de rendimiento y utilizacion de recursos).

#### 7.1.2 Explicar el Comportamiento Correcto para un Script de Prueba Automatizado y/o Suite de Prueba Dados

Las suites de prueba automatizadas necesitan ser probadas para completitud, consistencia y comportamiento correcto. Se pueden aplicar diferentes tipos de verificaciones para asegurar que la suite de prueba automatizada esta disponible en cualquier momento dado o para determinar que es apta para el uso.

Pasos que pueden tomarse para verificar la suite de prueba automatizada incluyen:

- **Verificar la composicion de la suite de prueba**: Verificar la completitud (por ejemplo, todos los casos de prueba tienen resultados esperados y los datos de prueba estan presentes) y la version correcta del TAF y el SUT

- **Verificar nuevas pruebas que se enfocan en nuevas caracteristicas del TAF**: La primera vez que se usa una nueva caracteristica del TAF en casos de prueba, debe verificarse y monitorizarse de cerca

- **Considerar la repetibilidad de las pruebas**: Al repetir pruebas, los resultados siempre deben ser los mismos. Los casos de prueba que no dan un resultado confiable (por ejemplo, debido a condiciones de carrera) deben moverse de la suite activa y analizarse por separado

- **Considerar la intrusividad de las herramientas de prueba automatizadas**: El TAS a menudo estara estrechamente acoplado con el SUT. Un alto nivel de intrusion puede mostrar fallos durante las pruebas que no son evidentes en produccion

#### 7.1.3 Identificar Donde la Automatizacion de Pruebas Produce Resultados Inesperados

Cuando un script de prueba falla o pasa inesperadamente, se debe realizar un analisis de causa raiz. Esto incluira inspeccionar registros de prueba, datos de rendimiento, configuracion y desmontaje del script de prueba.

Tambien es util ejecutar algunas pruebas aisladas. Los fallos intermitentes son mas dificiles de analizar. El defecto puede estar en el caso de prueba, el SUT, el TAF, el hardware o la red. Monitorizar los recursos del sistema puede dar pistas sobre la causa raiz.

Verificar si todas las aserciones estan en su lugar. Las aserciones faltantes pueden resultar en resultados de prueba inconclusos.

#### 7.1.4 Explicar Como el Analisis Estatico Puede Ayudar a la Calidad del Codigo de Automatizacion de Pruebas

El analisis estatico de codigo puede ayudar a encontrar vulnerabilidades y defectos en el codigo del programa. Esto puede incluir el SUT o el TAF.

Los escaneos automatizados pueden inspeccionar el codigo para mitigar riesgos. Esto proporciona una revision del SUT en busca de defectos y asegura que los estandares de calidad de codigo se cumplan y apliquen. Esto tambien puede considerarse una tecnica proactiva de deteccion de defectos, y juega un papel significativo en las implementaciones de DevSecOps (es decir, DevOps con enfasis en Seguridad). Estos escaneos ocurren temprano en el SDLC a traves de pipelines para proporcionar a los equipos de desarrollo retroalimentacion inmediata.

La salida respecto a defectos usualmente se categoriza como critica, alta, media o baja severidad para que los equipos de desarrollo tengan la capacidad de priorizar que defectos eligen corregir.

Como las herramientas de automatizacion de pruebas usan lenguajes de programacion, hay un riesgo de que se introduzca codigo de automatizacion de pruebas inadecuado al SDLC. Como ejemplo simple, una practica comun al automatizar pruebas es tener un nombre de usuario y contrasena. Es concebible que un TAE pueda incluir incorrectamente la contrasena en texto plano dentro de uno o muchos scripts de prueba.

Las herramientas de analisis estatico pueden beneficiar el codigo de automatizacion de pruebas. Pueden usarse para analizar el codigo de automatizacion de pruebas en busca de violaciones de seguridad como una contrasena en texto plano dentro del codigo.

---

## 8. Mejora Continua – 210 minutos (K4)

**Palabras clave**: validacion de esquema, histograma de prueba

### Objetivos de Aprendizaje para el Capitulo 8:

**8.1 Oportunidades de Mejora Continua para la Automatizacion de Pruebas**
- TAE-8.1.1 (K3) Descubrir oportunidades para mejorar los casos de prueba a traves de la recopilacion y analisis de datos
- TAE-8.1.2 (K4) Analizar los aspectos tecnicos de una solucion de automatizacion de pruebas desplegada y proporcionar recomendaciones para la mejora
- TAE-8.1.3 (K3) Reestructurar el testware automatizado para alinearse con las actualizaciones del sistema bajo prueba
- TAE-8.1.4 (K2) Resumir oportunidades para el uso de herramientas de automatizacion de pruebas

---

### 8.1 Oportunidades de Mejora Continua para la Automatizacion de Pruebas

#### 8.1.1 Descubrir Oportunidades para Mejorar los Casos de Prueba a Traves de la Recopilacion y Analisis de Datos

La recopilacion y analisis de datos pueden mejorarse al considerar varios tipos de datos con los enfoques descritos a continuacion.

**Histograma de prueba**

Un reporte visual de datos de prueba representado como un histograma de prueba proporciona areas de mejora potenciales respecto a las tendencias de datos de casos de prueba. Los TAEs pueden decidir sobre posibles areas de mejora ya que muchas herramientas de CI/CD y reportes de prueba tienen la capacidad de mostrar diferentes resultados de prueba y sus respectivos datos de prueba. El histograma de prueba tambien permite a los TAEs identificar y seleccionar aquellos casos de prueba que son fragiles y refactorizarlos con mejoras adicionales o repensando la implementacion real.

**Inteligencia Artificial**

Otra oportunidad reciente es utilizar la Inteligencia Artificial (IA) para soportar las pruebas y la automatizacion de pruebas. Por ejemplo, en casos de prueba de UI, los datos tambien incluyen valores de localizadores de UI que pueden tratarse como entradas. Herramientas recientes de vanguardia muestran la capacidad de detectar si un localizador dado ha cambiado del que se usaba. Basandose en ML y reconocimiento de imagenes, pueden identificar los nuevos selectores y usar un algoritmo de auto-reparacion (self-healing) para arreglar el caso de prueba e incluir los localizadores cambiados en el reporte de prueba.

**Validacion de esquema**

La validacion de esquema puede aplicarse en el analisis de datos de API (por ejemplo, propiedades derivadas de endpoints objetivo) y analisis de base de datos (por ejemplo, reglas de validacion para campos de software, como tipos de datos permitidos y rangos de valores). Con la validacion de esquema, el TAS es capaz de verificar si una respuesta coincide con la especificacion de negocio real.

Ejemplo: una API tiene seis elementos de respuesta obligatorios que deben ser cadenas en la respuesta. Con herramientas de validacion de esquema no es necesario escribir aserciones individuales para verificar si estos tipos son cadenas y sus valores no son nulos. La validacion de esquema manejara estas verificaciones, haciendo el codigo de automatizacion de pruebas implementado mucho mas corto y aumentando la eficiencia de deteccion de defectos en el servicio backend.

#### 8.1.2 Analizar los Aspectos Tecnicos de una Solucion de Automatizacion de Pruebas Desplegada y Proporcionar Recomendaciones para la Mejora

Ademas de las tareas de mantenimiento continuo necesarias para mantener el TAS sincronizado con el SUT, hay muchas oportunidades para mejorar el TAS. Estas mejoras pueden hacerse para lograr una variedad de beneficios incluyendo mayor eficiencia, mejor facilidad de uso, capacidades adicionales y soporte mejorado para las pruebas.

Areas especificas de un TAS que pueden considerarse para mejora incluyen:

**Scripting**

Las tecnicas de scripting varian desde el scripting lineal hasta el enfoque de pruebas guiadas por datos y hasta el enfoque mas sofisticado de pruebas guiadas por palabras clave. Puede ser apropiado actualizar la tecnica actual de scripting del TAS para todas las nuevas pruebas automatizadas.

Otra area de mejora del TAS para scripts de prueba puede enfocarse en su implementacion:

- Evaluar la superposicion de scripts/casos/pasos de prueba para consolidar pruebas automatizadas. Los casos de prueba que contienen secuencias de acciones similares no deben implementar estos pasos de prueba multiples veces. Estos pasos deben convertirse en una funcion y anadirse a una libreria para que puedan reutilizarse
- Establecer un proceso de recuperacion de fallos para el TAS y el SUT
- Evaluar los mecanismos de espera para asegurar que se use el mejor tipo:
  - **Esperas hardcodeadas** (es decir, esperar un cierto numero de milisegundos): pueden ser causa raiz de muchos defectos de automatizacion
  - **Espera dinamica por sondeo (polling)**: verificar que un cierto cambio de estado o accion ha tenido lugar, es mucho mas flexible y eficiente. Recordar incluir un mecanismo de timeout
  - **Suscripcion al mecanismo de eventos del SUT**: Mucho mas confiable que las otras dos opciones, pero el lenguaje de scripting necesita soportar la suscripcion a eventos y el SUT necesita ofrecer estos eventos al TAS

**Ejecucion de pruebas**

Cuando una suite de pruebas de regresion automatizada no termina porque la ejecucion toma demasiado tiempo, puede ser necesario probar concurrentemente en diferentes entornos de prueba. En el caso de CI/CD, una buena practica es ejecutar trabajos por lotes en paralelo para optimizar el tiempo de ejecucion de pruebas.

**Verificacion**

Antes de crear nuevas funciones de verificacion, adoptar un conjunto de metodos de verificacion estandar para uso de todas las pruebas automatizadas. Esto evitara la re-implementacion de acciones de verificacion en multiples pruebas.

**TAA**

Puede ser necesario cambiar la TAA para soportar mejoras de la testabilidad del SUT. Estos cambios pueden hacerse en la arquitectura del SUT y/o en la TAA del TAS.

**TAF**

A menudo hay nuevas versiones de las librerias principales usadas en un TAF. A veces son actualizaciones importantes y la ultima version no puede referenciarse inmediatamente en la lista de dependencias del TAF ya que romperia las pruebas. Por lo tanto, es mejor primero realizar un piloto y un analisis de impacto.

**Configuracion y desmontaje (Setup y teardown)**

Las acciones y configuraciones que se repiten antes o despues de cada script o suite de prueba deben moverse a metodos de configuracion o desmontaje. De esta manera, cualquier cambio puede actualizarse en un solo lugar.

**Documentacion**

Esto cubre todas las formas de documentacion desde la documentacion de automatizacion de pruebas, documentacion de usuario para el TAS y los reportes y registros de pruebas producidos por el TAS.

**Caracteristicas del TAS**

Anadir caracteristicas y funciones del TAS como reportes de prueba detallados, registros de prueba e integracion con otros sistemas. Solo anadir nuevas caracteristicas que se usaran. Anadir caracteristicas no usadas solo aumenta la complejidad y disminuye la confiabilidad y mantenibilidad.

**Actualizaciones y mejoras del TAF**

Al actualizar o mejorar a nuevas versiones del TAF, pueden estar disponibles nuevas funciones que pueden usarse por los casos de prueba o pueden corregirse fallos. El riesgo es que actualizar el TAF podria tener un impacto adverso en los casos de prueba existentes. Probar la ultima version de la herramienta de prueba ejecutando pruebas de muestra antes de desplegar la nueva version.

#### 8.1.3 Reestructurar el Testware Automatizado para Alinearse con las Actualizaciones del Sistema Bajo Prueba

Seguir un conjunto dado de cambios a un SUT existente requerira actualizaciones al TAS incluyendo el TAF y las librerias de componentes. Cualquier cambio, no importa cuan trivial, puede tener un impacto adverso de amplio alcance en la confiabilidad y rendimiento del TAS.

**Identificar cambios en los componentes del entorno de prueba**

Evaluar que cambios y mejoras necesitan hacerse. Los cambios deben hacerse incrementalmente, con una mentalidad de producto minimo viable, para que el impacto en el TAS pueda medirse a traves de una ejecucion limitada de scripts de prueba. Una ejecucion de regresion completa es el ultimo paso para verificar que el cambio no afecto adversamente los scripts de prueba automatizados.

**Aumentar la eficiencia y efectividad de las librerias de funciones principales del TAS**

A medida que un TAS madura, se descubren nuevas formas de realizar tareas de manera mas eficiente. Estas nuevas tecnicas necesitan incorporarse en las librerias de funciones principales.

**Consolidar multiples funciones que actuan sobre el mismo tipo de control**

Los TAEs pueden usar varias funciones que pueden consolidarse en menos funciones, logrando los mismos resultados y minimizando el mantenimiento.

**Refactorizar la TAA para acomodar cambios en el SUT**

A traves del ciclo de vida de un TAS, se necesitaran hacer cambios para acomodar cambios en el SUT. Se debe tener cuidado al extender las caracteristicas para que no se implementen de manera acoplada, sino que se analicen y cambien en la TAA.

**Convenciones de nombres y estandarizacion**

A medida que se introducen cambios, las convenciones de nombres para el nuevo codigo y las librerias de funciones necesitan ser consistentes con los estandares previamente definidos.

**Evaluacion de scripts de prueba existentes para revision/eliminacion**

El proceso de cambio y mejora tambien incluye una evaluacion de los scripts de prueba existentes, su uso y valor continuado. Apuntar a las pruebas que se ejecutan con poca frecuencia o no se ejecutan en absoluto para eliminacion reducira la complejidad del TAS.

#### 8.1.4 Resumir Oportunidades para el Uso de Herramientas de Automatizacion de Pruebas

Aparte de las pruebas reales, la automatizacion de pruebas puede ayudar en actividades no especificas de prueba tales como:

**Configuracion y control de entorno**

Ciertos scripts de prueba (por ejemplo, creacion de datos de prueba) pueden aprovecharse en un metodo de configuracion para crear diferentes datos de prueba en un nuevo entorno de prueba. Los scripts de prueba pueden tener control sobre la configuracion de la infraestructura de prueba y pueden aprovecharse en la limpieza posterior al proceso.

**Envejecimiento de datos (Data aging)**

La automatizacion de pruebas puede usarse para manipular los datos de prueba en el entorno de prueba. Por ejemplo, en bases de datos, los campos de fecha pueden verificarse y controlarse para mantenerlos actualizados desde una perspectiva anual.

**Generacion de capturas de pantalla y video**

La mayoria de las herramientas modernas de automatizacion de pruebas de UI tienen una capacidad integrada para crear capturas de pantalla o videos en ciertas condiciones y almacenarlos. Con estas herramientas de prueba, los equipos pueden soportar al negocio en la creacion de capturas de pantalla y videos de uso real para documentacion de releases de software o propositos de marketing.

---

## 9. Referencias

### Estandares

Los estandares para la automatizacion de pruebas incluyen pero no se limitan a:

- **ATML (Automatic Test Markup Language)** por IEEE
- **IEEE Std 1636.1**: Resultados de Pruebas
- **ISO/IEC/IEEE 29119-5 (2016)**: Ingenieria de Software y Sistemas - Pruebas de Software - Parte 5: Pruebas Guiadas por Palabras Clave
- **ISO/IEC 30130:2016 (E)**: Ingenieria de Software - Capacidades de herramientas de prueba de software
- **TTCN-3** (Testing and Test Control Notation) por ETSI e ITU
- **UTP** (UML Testing Profile) por OMG

### Documentos ISTQB(R)

| Identificador | Referencia |
|---------------|-----------|
| ISTQB-AL-TTA | Syllabus de Analista Tecnico de Pruebas de Nivel Avanzado, Version 4.0, Junio 2021 |
| ISTQB-FL | Syllabus de Nivel Basico, Version 4.0, Abril 2023 |
| ISTQB-MBT | Syllabus de Pruebas Basadas en Modelos, Version 1.0, Octubre 2015 |
| ISTQB-PT | Syllabus de Pruebas de Rendimiento, Diciembre 2018 |
| ISTQB-SEC | Syllabus de Tester de Seguridad, Version 1.0, Marzo 2016 |
| ISTQB-TAS | Syllabus de Estrategia de Automatizacion de Pruebas, Febrero 2024 |
| ISTQB-Glossary | Glosario de Terminos del ISTQB |

### Libros

- Paul Baker et al., "Model-Driven Testing: Using the UML Testing Profile", Springer 2008
- Efriede Dustin et al., "Implementing Automated Software Testing", Addison-Wesley, 2009
- Efriede Dustin et al., "Automated Software Testing", Addison-Wesley, 1999
- Mark Fewster, Dorothy Graham, "Experiences of Test Automation", Addison-Wesley, 2012
- Mark Fewster, Dorothy Graham, "Software Test Automation", ACM Press Books, 1999
- Robert C Martin, "Clean Code: A Handbook of Agile Software Craftsmanship", 2008
- Manikandan Sambamurthy, "Test Automation Engineering Handbook", Enero 2023

---

## 10. Apendice A – Objetivos de Aprendizaje/Nivel Cognitivo de Conocimiento

### Nivel 2: Comprender (K2)

El candidato puede seleccionar las razones o explicaciones para declaraciones relacionadas con el tema, y puede resumir, comparar, clasificar y dar ejemplos del concepto de pruebas.

**Verbos de accion**: Clasificar, comparar, diferenciar, distinguir, explicar, dar ejemplos, interpretar, resumir

### Nivel 3: Aplicar (K3)

El candidato puede llevar a cabo un procedimiento cuando se enfrenta a una tarea familiar o seleccionar el procedimiento correcto y aplicarlo a un contexto dado.

**Verbos de accion**: Aplicar, implementar, preparar, usar

### Nivel 4: Analizar (K4)

El candidato puede separar la informacion relacionada con un procedimiento o tecnica en sus partes constituyentes para una mejor comprension y puede distinguir entre hechos e inferencias. Una aplicacion tipica es analizar un documento, software o situacion de proyecto y proponer acciones apropiadas para resolver un problema o tarea.

**Verbos de accion**: Analizar, deconstruir, delinear, priorizar, seleccionar

---

## 11. Apendice B – Matriz de Trazabilidad

La matriz de trazabilidad entre los Resultados de Negocio y los Objetivos de Aprendizaje del Especialista en Ingenieria de Automatizacion de Pruebas se encuentra disponible en el documento original del syllabus.

---

## 12. Apendice C – Notas de la Version

Consulte el documento original del syllabus para las notas detalladas de la version.

---

## 13. Apendice D – Terminos Especificos del Dominio

Consulte el glosario oficial del ISTQB para los terminos especificos del dominio de automatizacion de pruebas.

---

## 14. Indice

Consulte el documento original del syllabus para el indice completo.

---

*Traduccion al espanol del documento original: ISTQB Certified Tester Advanced Level - Test Automation Engineering Syllabus v2.0 (2024/05/03)*

*Este documento es una traduccion no oficial con fines educativos. Para la version oficial, consulte www.istqb.org*
