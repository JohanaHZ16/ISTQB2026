# ISTQB TAE - Simulacro de Examen

## Instrucciones

| Aspecto | Detalle |
|---------|---------|
| **Preguntas** | 40 preguntas de opcion multiple |
| **Tiempo** | 90 minutos (120 min si no es tu idioma nativo) |
| **Aprobacion** | 65% - Necesitas minimo **26/40** correctas |
| **Estrategia** | ~2 minutos por pregunta. Marca las dificiles y vuelve al final. |

> [!TIP]
> Simula condiciones reales: sin apuntes, cronometro activo, sin interrupciones. Al terminar, revisa tus respuestas con las explicaciones al final.

---

## Seccion A: Introduccion y Objetivos (Preguntas 1-7)

---

### Pregunta 1 (K2)

Cual de las siguientes es una ventaja clave de la automatizacion de pruebas?

- a) Elimina la necesidad de testers manuales en el equipo
- b) Garantiza que el software no tendra defectos
- c) Permite ejecutar pruebas repetitivas de manera consistente y rapida
- d) Reduce el costo total del proyecto a cero

---

### Pregunta 2 (K2)

Cual de las siguientes NO es una limitacion de la automatizacion de pruebas?

- a) Requiere una inversion inicial significativa
- b) No puede reemplazar completamente las pruebas exploratorias
- c) Puede ejecutar pruebas mas rapido que un humano
- d) Los scripts requieren mantenimiento continuo

---

### Pregunta 3 (K2)

Un equipo quiere automatizar pruebas por primera vez. Cual es el factor MAS critico a evaluar antes de comenzar?

- a) El numero de testers disponibles
- b) La testabilidad del sistema bajo prueba (SUT)
- c) El color del logo de la herramienta
- d) La cantidad de lineas de codigo del proyecto

---

### Pregunta 4 (K2)

Cual de las siguientes afirmaciones sobre el ROI de la automatizacion es CORRECTA?

- a) El ROI siempre es positivo desde la primera ejecucion
- b) El ROI mejora con el numero de ejecuciones de las pruebas automatizadas
- c) El ROI no depende del costo de mantenimiento
- d) El ROI es irrelevante para la decision de automatizar

---

### Pregunta 5 (K2)

Que tipo de pruebas se beneficia MAS de la automatizacion?

- a) Pruebas exploratorias
- b) Pruebas de usabilidad
- c) Pruebas de regresion
- d) Pruebas ad-hoc

---

### Pregunta 6 (K2)

Un gerente afirma: "Con la automatizacion, ya no necesitamos testers manuales." Esta afirmacion es:

- a) Correcta, la automatizacion reemplaza todas las pruebas manuales
- b) Incorrecta, las pruebas manuales y automatizadas son complementarias
- c) Correcta, si se automatiza el 100% de las pruebas
- d) Correcta, solo si se usan herramientas de IA

---

### Pregunta 7 (K3)

Un proyecto tiene las siguientes pruebas. Cual es la MEJOR candidata para automatizar?

| Prueba | Frecuencia | Estabilidad del Requisito | Complejidad |
|--------|-----------|--------------------------|-------------|
| A | 1 vez al ano | Baja | Alta |
| B | Cada sprint | Alta | Media |
| C | 1 sola vez | Alta | Baja |
| D | Cada sprint | Baja | Alta |

- a) Prueba A
- b) Prueba B
- c) Prueba C
- d) Prueba D

---

## Seccion B: Preparacion para la Automatizacion (Preguntas 8-14)

---

### Pregunta 8 (K2)

Que significa "controlabilidad" en el contexto de la testabilidad del SUT?

- a) La capacidad de observar los resultados del sistema
- b) La capacidad de establecer el sistema en un estado deseado
- c) La capacidad de controlar el presupuesto del proyecto
- d) La capacidad de controlar al equipo de desarrollo

---

### Pregunta 9 (K2)

Cual es la diferencia entre una tecnica intrusiva y una no intrusiva para mejorar la testabilidad?

- a) Las intrusivas son mas baratas que las no intrusivas
- b) Las intrusivas modifican el SUT, las no intrusivas no lo modifican
- c) Las no intrusivas requieren mas tiempo de implementacion
- d) No hay diferencia, son sinonimos

---

### Pregunta 10 (K3)

Un equipo evalua herramientas de automatizacion. Cual es el paso MAS importante en el proceso de seleccion?

- a) Elegir la herramienta mas cara del mercado
- b) Seleccionar la herramienta que el gerente prefiere
- c) Realizar un Proof of Concept (PoC) con las herramientas candidatas
- d) Elegir la herramienta mas popular en redes sociales

---

### Pregunta 11 (K2)

En un enfoque Data-Driven, donde se almacenan los datos de prueba?

- a) Dentro del codigo del script de prueba
- b) En archivos externos como CSV, Excel o bases de datos
- c) En la memoria RAM del servidor
- d) En el codigo fuente del SUT

---

### Pregunta 12 (K2)

Cual es la principal ventaja del enfoque Keyword-Driven?

- a) Es el enfoque mas rapido de implementar
- b) No requiere ningun framework
- c) Permite que personas sin conocimientos tecnicos profundos creen casos de prueba
- d) Elimina la necesidad de datos de prueba

---

### Pregunta 13 (K3)

Un SUT tiene una interfaz web inestable cuyos elementos cambian de ID frecuentemente, pero tiene una API REST bien documentada y estable. Cual es la MEJOR estrategia?

- a) Automatizar exclusivamente a traves de la interfaz web
- b) No automatizar hasta que la interfaz web sea estable
- c) Priorizar la automatizacion a nivel de API y minimizar las pruebas de UI
- d) Cambiar el SUT por otro producto

---

### Pregunta 14 (K2)

Que es un "test hook" en el contexto de la testabilidad?

- a) Un defecto encontrado durante las pruebas
- b) Un punto de acceso insertado en el SUT para facilitar las pruebas automatizadas
- c) Un tipo de framework de automatizacion
- d) Una metrica de calidad del software

---

## Seccion C: Arquitectura Generica de Automatizacion - gTAA (Preguntas 15-27)

---

### Pregunta 15 (K2)

Cuantas capas principales tiene la gTAA?

- a) 2
- b) 3
- c) 4
- d) 5

---

### Pregunta 16 (K2)

Cual capa de la gTAA es responsable de interactuar directamente con el SUT?

- a) Capa de generacion de pruebas
- b) Capa de definicion de pruebas
- c) Capa de ejecucion de pruebas
- d) Capa de adaptacion de pruebas

---

### Pregunta 17 (K2)

En la capa de definicion de pruebas, cual es la diferencia entre alto nivel y bajo nivel?

- a) Alto nivel es mas importante que bajo nivel
- b) Alto nivel describe QUE probar; bajo nivel describe COMO probar
- c) Alto nivel es para gerentes; bajo nivel es para desarrolladores
- d) No hay diferencia, son lo mismo

---

### Pregunta 18 (K3)

Un script de Selenium contiene la siguiente linea:
`driver.findElement(By.id("submit-btn")).click();`

A que capa de la gTAA pertenece esta instruccion?

- a) Capa de generacion
- b) Capa de definicion de alto nivel
- c) Capa de ejecucion
- d) Capa de adaptacion

---

### Pregunta 19 (K3)

La siguiente descripcion de prueba dice: "Verificar que un usuario valido puede iniciar sesion exitosamente." A que nivel de la capa de definicion pertenece?

- a) Bajo nivel
- b) Alto nivel
- c) Capa de adaptacion
- d) Capa de ejecucion

---

### Pregunta 20 (K4)

El equipo de desarrollo cambia el ID de un boton de "login-btn" a "sign-in-button" en la interfaz web. Si el TAS esta bien disenado segun la gTAA, que impacto tiene este cambio?

- a) Hay que reescribir todos los scripts de prueba
- b) Solo se debe actualizar la capa de adaptacion
- c) Se deben modificar todas las capas de la gTAA
- d) No tiene ningun impacto, el TAS se adapta automaticamente

---

### Pregunta 21 (K2)

Cual es la funcion principal del motor de ejecucion en la gTAA?

- a) Crear los casos de prueba
- b) Interpretar y ejecutar los scripts de prueba
- c) Interactuar con la interfaz del SUT
- d) Generar los datos de prueba

---

### Pregunta 22 (K3)

En el Page Object Model (POM), que representa una clase Page Object?

- a) Un caso de prueba completo
- b) Una pagina o componente del SUT con sus elementos y acciones
- c) El motor de ejecucion del framework
- d) Una base de datos de resultados

---

### Pregunta 23 (K4)

Un equipo tiene 200 scripts de prueba de UI. Tras una actualizacion del SUT, 150 scripts fallan porque los localizadores de elementos cambiaron. Cual patron de diseno habria reducido el esfuerzo de mantenimiento?

- a) Singleton Pattern
- b) Factory Pattern
- c) Page Object Model
- d) Observer Pattern

---

### Pregunta 24 (K3)

Cual de las siguientes es una responsabilidad de la capa de ejecucion?

- a) Definir los pasos de prueba en lenguaje de negocio
- b) Gestionar la configuracion del entorno y generar reportes de resultados
- c) Traducir los comandos a acciones sobre el SUT
- d) Disenar los casos de prueba

---

### Pregunta 25 (K4)

Un TAS tiene los siguientes problemas: los scripts de prueba contienen directamente los localizadores de elementos, los datos de prueba estan hardcodeados en los scripts, y no hay separacion entre la logica de negocio y la interaccion con la UI. Que principio de la gTAA se esta violando?

- a) El principio de ejecucion rapida
- b) El principio de separacion de capas y responsabilidades
- c) El principio de cobertura maxima
- d) El principio de documentacion exhaustiva

---

### Pregunta 26 (K2)

Que tecnica de automatizacion captura las acciones del usuario sobre el SUT para generar scripts automaticamente?

- a) Model-Based Testing
- b) Keyword-Driven Testing
- c) Record and Playback (Captura y Reproduccion)
- d) Data-Driven Testing

---

### Pregunta 27 (K3)

Cual es la principal desventaja de Record and Playback como estrategia de automatizacion a largo plazo?

- a) Es demasiado rapido de implementar
- b) Los scripts generados son fragiles, dificiles de mantener y poco reutilizables
- c) No puede interactuar con interfaces graficas
- d) Requiere conocimientos avanzados de programacion

---

## Seccion D: Riesgos y Contingencias (Preguntas 28-32)

---

### Pregunta 28 (K3)

Cual de los siguientes es un riesgo TECNICO de la automatizacion de pruebas?

- a) Falta de apoyo de la gerencia
- b) Fragilidad de los scripts ante cambios en el SUT
- c) Falta de presupuesto
- d) Resistencia del equipo al cambio

---

### Pregunta 29 (K3)

Un equipo experimenta que el 40% de los scripts automatizados fallan despues de cada release, pero los fallos no son defectos reales del SUT. Cual es el termino correcto para estos fallos?

- a) Falsos negativos
- b) Falsos positivos
- c) Defectos criticos
- d) Errores de regresion

---

### Pregunta 30 (K3)

Cual es la estrategia recomendada para desplegar un TAS por primera vez en una organizacion?

- a) Automatizar todas las pruebas de una sola vez
- b) Comenzar con un piloto pequeno, validar y luego expandir gradualmente
- c) Comprar la herramienta mas costosa y esperar resultados inmediatos
- d) Automatizar solo las pruebas que nunca fallan

---

### Pregunta 31 (K4)

Un proyecto de automatizacion tiene un ano de antiguedad. El equipo reporta que gastan mas tiempo manteniendo los scripts existentes que creando nuevos. Cual es la causa raiz MAS probable?

- a) El equipo no tiene suficientes miembros
- b) La arquitectura del TAS no tiene buena separacion de capas
- c) Las herramientas son demasiado modernas
- d) Se ejecutan demasiadas pruebas

---

### Pregunta 32 (K2)

Cual tipo de mantenimiento del TAS se realiza cuando el SUT cambia y los scripts deben actualizarse para seguir funcionando?

- a) Mantenimiento correctivo
- b) Mantenimiento adaptativo
- c) Mantenimiento perfectivo
- d) Mantenimiento preventivo

---

## Seccion E: Reportes y Metricas (Preguntas 33-37)

---

### Pregunta 33 (K2)

Segun la piramide de automatizacion de pruebas, que tipo de pruebas debe ser el MAS numeroso?

- a) Pruebas de interfaz de usuario (UI)
- b) Pruebas de integracion / API
- c) Pruebas unitarias
- d) Pruebas de rendimiento

---

### Pregunta 34 (K2)

Que es el "anti-patron del cono de helado" en automatizacion?

- a) Tener demasiadas pruebas unitarias
- b) Una piramide invertida con muchas pruebas UI y pocas unitarias
- c) No tener framework de automatizacion
- d) Ejecutar pruebas solo en un navegador

---

### Pregunta 35 (K2)

Cual de las siguientes es una metrica del TAS (no del SUT)?

- a) Numero de defectos en produccion
- b) Tiempo promedio de ejecucion del suite de pruebas automatizadas
- c) Cobertura de codigo del SUT
- d) Numero de requisitos funcionales

---

### Pregunta 36 (K3)

Un reporte de automatizacion muestra que el suite de pruebas tiene una tasa de exito del 95%. Sin embargo, los defectos en produccion han aumentado. Cual es la explicacion MAS probable?

- a) La automatizacion esta funcionando perfectamente
- b) Las pruebas automatizadas no cubren las areas donde estan los defectos (baja cobertura efectiva)
- c) El 95% de exito significa que el software esta casi perfecto
- d) Los defectos en produccion no tienen relacion con las pruebas

---

### Pregunta 37 (K2)

Que significa trazabilidad bidireccional en el contexto de la automatizacion?

- a) Poder ejecutar pruebas en dos direcciones
- b) Poder rastrear desde un requisito hasta las pruebas que lo cubren, y viceversa
- c) Tener dos reportes diferentes por cada ejecucion
- d) Ejecutar pruebas en dos entornos diferentes

---

## Seccion F: Transicion Manual a Automatizado (Preguntas 38-40)

---

### Pregunta 38 (K4)

Un equipo tiene los siguientes tipos de pruebas manuales. Cual deberia automatizar PRIMERO?

| Tipo | Frecuencia | Valor de Negocio | Estabilidad | Esfuerzo de Automatizacion |
|------|-----------|-----------------|-------------|---------------------------|
| Smoke tests | Cada build | Critico | Alta | Bajo |
| Pruebas de edge cases | Mensual | Medio | Media | Alto |
| Pruebas de regresion | Cada sprint | Alto | Alta | Medio |
| Pruebas exploratorias | Semanal | Alto | Baja | Muy Alto |

- a) Pruebas de edge cases
- b) Smoke tests
- c) Pruebas exploratorias
- d) Pruebas de regresion

---

### Pregunta 39 (K3)

Cual es la responsabilidad PRINCIPAL del Test Automation Engineer (TAE)?

- a) Aprobar las releases del producto
- b) Disenar, desarrollar y mantener los scripts y el framework de automatizacion
- c) Gestionar el presupuesto del proyecto
- d) Escribir los requisitos de negocio

---

### Pregunta 40 (K4)

Un equipo esta en el Nivel 2 (Gestionado) del modelo de madurez de automatizacion. Tienen un framework basico y algunos scripts estables. Cual es el paso MAS apropiado para avanzar al Nivel 3 (Definido)?

- a) Implementar inteligencia artificial en todas las pruebas
- b) Establecer patrones de diseno, un framework maduro e integrar con CI/CD
- c) Eliminar todas las pruebas manuales
- d) Contratar mas testers manuales

---

# Hoja de Respuestas

> [!WARNING]
> No mires las respuestas hasta haber completado todo el simulacro. Cronometra tu tiempo y anota tus respuestas antes de verificar.

---

<details>
<summary><strong>Click aqui para ver las respuestas</strong></summary>

## Respuestas y Explicaciones

---

### Seccion A: Introduccion y Objetivos

> [!SUCCESS]
> **Pregunta 1: c)** Permite ejecutar pruebas repetitivas de manera consistente y rapida.
> La automatizacion no elimina testers (a), no garantiza cero defectos (b), ni reduce costos a cero (d).

> [!SUCCESS]
> **Pregunta 2: c)** Ejecutar pruebas mas rapido es una VENTAJA, no una limitacion. Las demas opciones si son limitaciones reales.

> [!SUCCESS]
> **Pregunta 3: b)** La testabilidad del SUT es el factor mas critico. Sin buena testabilidad, la automatizacion sera costosa y fragil.

> [!SUCCESS]
> **Pregunta 4: b)** El ROI mejora con cada ejecucion adicional, ya que el costo de desarrollo se amortiza. No es positivo desde el inicio (a) y si depende del mantenimiento (c).

> [!SUCCESS]
> **Pregunta 5: c)** Las pruebas de regresion son repetitivas, frecuentes y predecibles, ideales para automatizar. Las exploratorias (a), de usabilidad (b) y ad-hoc (d) requieren juicio humano.

> [!SUCCESS]
> **Pregunta 6: b)** Las pruebas manuales y automatizadas son complementarias. Siempre habra pruebas que requieran juicio humano.

> [!SUCCESS]
> **Pregunta 7: b)** La Prueba B tiene alta frecuencia (cada sprint), alta estabilidad y complejidad media. Es la mejor candidata. C se ejecuta una sola vez, A y D tienen requisitos inestables.

---

### Seccion B: Preparacion para la Automatizacion

> [!SUCCESS]
> **Pregunta 8: b)** Controlabilidad = capacidad de establecer el sistema en un estado deseado. Observabilidad (a) es la otra dimension de testabilidad.

> [!SUCCESS]
> **Pregunta 9: b)** Las tecnicas intrusivas modifican el SUT (agregar hooks, APIs de prueba). Las no intrusivas usan interfaces existentes sin modificar el SUT.

> [!SUCCESS]
> **Pregunta 10: c)** El Proof of Concept valida que la herramienta funciona en el contexto real del proyecto. No se debe elegir por precio (a), preferencia (b) o popularidad (d).

> [!SUCCESS]
> **Pregunta 11: b)** En Data-Driven, los datos se separan de los scripts y se almacenan en fuentes externas (CSV, Excel, DB).

> [!SUCCESS]
> **Pregunta 12: c)** El enfoque Keyword-Driven usa palabras clave de negocio, permitiendo que personas sin conocimientos tecnicos profundos participen.

> [!SUCCESS]
> **Pregunta 13: c)** Si la API es estable y la UI es fragil, priorizar la automatizacion a nivel de API maximiza la estabilidad y el ROI.

> [!SUCCESS]
> **Pregunta 14: b)** Un test hook es un punto de acceso insertado en el SUT especificamente para facilitar las pruebas automatizadas. Es una tecnica intrusiva.

---

### Seccion C: Arquitectura Generica de Automatizacion - gTAA

> [!SUCCESS]
> **Pregunta 15: c)** La gTAA tiene 4 capas: Generacion, Definicion, Ejecucion y Adaptacion.

> [!SUCCESS]
> **Pregunta 16: d)** La capa de adaptacion es la unica que interactua directamente con el SUT a traves de adaptadores de interfaz.

> [!SUCCESS]
> **Pregunta 17: b)** Alto nivel = QUE probar (lenguaje de negocio, independiente de herramienta). Bajo nivel = COMO probar (scripts ejecutables, dependiente de herramienta).

> [!SUCCESS]
> **Pregunta 18: d)** La instruccion interactua directamente con un elemento del SUT (busca y hace click en un boton). Esto pertenece a la capa de adaptacion.

> [!SUCCESS]
> **Pregunta 19: b)** Es una descripcion en lenguaje de negocio que dice QUE verificar sin especificar COMO. Es alto nivel.

> [!SUCCESS]
> **Pregunta 20: b)** En una gTAA bien disenada, los cambios en la interfaz del SUT solo afectan la capa de adaptacion. Las demas capas no necesitan cambiar.

> [!SUCCESS]
> **Pregunta 21: b)** El motor de ejecucion interpreta los scripts, controla el flujo de ejecucion y maneja excepciones.

> [!SUCCESS]
> **Pregunta 22: b)** Un Page Object representa una pagina o componente del SUT, encapsulando sus elementos y las acciones posibles.

> [!SUCCESS]
> **Pregunta 23: c)** El Page Object Model centraliza los localizadores en un solo lugar. Si cambian, solo se actualiza el Page Object, no los 200 scripts.

> [!SUCCESS]
> **Pregunta 24: b)** La capa de ejecucion gestiona la configuracion, ejecuta los scripts y genera reportes de resultados.

> [!SUCCESS]
> **Pregunta 25: b)** Se viola el principio de separacion de capas: datos, logica de negocio y localizadores deberian estar en capas separadas.

> [!SUCCESS]
> **Pregunta 26: c)** Record and Playback captura las acciones del usuario sobre la interfaz y las convierte en scripts automaticos.

> [!SUCCESS]
> **Pregunta 27: b)** Los scripts de R&P son lineales, fragiles ante cambios en la UI, dificiles de mantener y poco reutilizables.

---

### Seccion D: Riesgos y Contingencias

> [!SUCCESS]
> **Pregunta 28: b)** La fragilidad de scripts es un riesgo tecnico. Los demas (a, c, d) son riesgos organizacionales o de proceso.

> [!SUCCESS]
> **Pregunta 29: b)** Falsos positivos = la prueba reporta un fallo que no es un defecto real del SUT. Pueden ser causados por scripts fragiles, datos inconsistentes o entornos inestables.

> [!SUCCESS]
> **Pregunta 30: b)** El enfoque gradual (piloto, validar, expandir) es la estrategia recomendada. Reduce riesgos y permite ajustar la estrategia.

> [!SUCCESS]
> **Pregunta 31: b)** Sin buena separacion de capas, cualquier cambio en el SUT impacta multiples scripts, generando un alto costo de mantenimiento.

> [!SUCCESS]
> **Pregunta 32: b)** Mantenimiento adaptativo = adaptar los scripts cuando cambia el SUT o el entorno. Correctivo = corregir defectos del TAS. Perfectivo = mejorar rendimiento/estructura. Preventivo = refactorizar para evitar problemas futuros.

---

### Seccion E: Reportes y Metricas

> [!SUCCESS]
> **Pregunta 33: c)** Las pruebas unitarias forman la base de la piramide: son rapidas, baratas y estables.

> [!SUCCESS]
> **Pregunta 34: b)** El cono de helado es una piramide invertida: muchas pruebas UI (lentas, caras, fragiles) y pocas unitarias.

> [!SUCCESS]
> **Pregunta 35: b)** El tiempo de ejecucion del suite es una metrica del TAS. Las demas son metricas del SUT o del proyecto.

> [!SUCCESS]
> **Pregunta 36: b)** Un 95% de exito no significa buena cobertura. Si las pruebas no cubren las areas problematicas, los defectos pasan a produccion.

> [!SUCCESS]
> **Pregunta 37: b)** Trazabilidad bidireccional = desde requisito hacia pruebas y desde pruebas hacia requisito. Permite identificar requisitos sin cobertura.

---

### Seccion F: Transicion Manual a Automatizado

> [!SUCCESS]
> **Pregunta 38: b)** Los smoke tests tienen: frecuencia maxima (cada build), valor critico, alta estabilidad y bajo esfuerzo. Son la prioridad #1.

> [!SUCCESS]
> **Pregunta 39: b)** El TAE disena, desarrolla y mantiene los scripts y el framework de automatizacion. Es su responsabilidad principal.

> [!SUCCESS]
> **Pregunta 40: b)** Para pasar de Nivel 2 a 3 se necesitan patrones de diseno establecidos, un framework maduro e integracion con CI/CD.

---

## Tabla de Resultados

| Rango | Calificacion | Estado |
|-------|-------------|--------|
| 36-40 | Excelente | Listo para el examen |
| 30-35 | Muy bien | Repasa las areas debiles |
| 26-29 | Aprobado justo | Necesitas mas practica |
| 20-25 | Cerca | Refuerza capitulos 3 y 2 |
| 0-19 | Insuficiente | Vuelve a estudiar el syllabus completo |

> [!TIP]
> Si obtuviste menos de 26, enfocate en:
> 1. **Capitulo 3 (gTAA)**: Es el que mas peso tiene
> 2. Las preguntas **K4 (analisis)**: Practica aplicar conceptos a escenarios
> 3. Revisa el glosario de terminos para evitar confusiones

</details>
