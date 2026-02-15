# ISTQB TAE - Flashcards de Estudio

> [!TIP]
> **Como usar estas flashcards:**
> - Lee solo la pregunta (frente de la tarjeta)
> - Intenta responder mentalmente
> - Despliega la respuesta para verificar
> - Marca las que fallas para repasarlas despues

---

## Categoria 1: Conceptos Fundamentales

---

### Flashcard 1
**Que es la automatizacion de pruebas?**

<details>
<summary>Ver respuesta</summary>

El uso de software especializado para ejecutar pruebas, comparar resultados reales con los esperados y generar reportes, reduciendo la intervencion manual.
</details>

---

### Flashcard 2
**Que significa SUT?**

<details>
<summary>Ver respuesta</summary>

**System Under Test** (Sistema Bajo Prueba). Es el sistema o aplicacion que esta siendo probado.
</details>

---

### Flashcard 3
**Que significa TAS?**

<details>
<summary>Ver respuesta</summary>

**Test Automation Solution** (Solucion de Automatizacion de Pruebas). Es el conjunto completo de herramientas, scripts, framework y procesos utilizados para automatizar pruebas.
</details>

---

### Flashcard 4
**Que significa TAF?**

<details>
<summary>Ver respuesta</summary>

**Test Automation Framework** (Framework de Automatizacion de Pruebas). Es la estructura base que proporciona las funcionalidades reutilizables para crear y ejecutar pruebas automatizadas.
</details>

---

### Flashcard 5
**Que significa gTAA?**

<details>
<summary>Ver respuesta</summary>

**Generic Test Automation Architecture** (Arquitectura Generica de Automatizacion de Pruebas). Es el modelo de referencia que define la estructura del TAS en capas.
</details>

---

### Flashcard 6
**Que significa ROI en automatizacion?**

<details>
<summary>Ver respuesta</summary>

**Return on Investment** (Retorno de Inversion). Mide si el beneficio de automatizar supera el costo de desarrollar y mantener los scripts. Mejora con cada ejecucion adicional.
</details>

---

### Flashcard 7
**Cual es la diferencia entre verificacion y validacion?**

<details>
<summary>Ver respuesta</summary>

- **Verificacion**: Estamos construyendo el producto correctamente? (cumple especificaciones)
- **Validacion**: Estamos construyendo el producto correcto? (cumple necesidades del usuario)
</details>

---

## Categoria 2: Testabilidad

---

### Flashcard 8
**Cuales son las dos dimensiones de la testabilidad?**

<details>
<summary>Ver respuesta</summary>

1. **Observabilidad**: Capacidad de observar los resultados, estados y comportamiento del SUT
2. **Controlabilidad**: Capacidad de establecer el SUT en un estado deseado (precondiciones, inputs)
</details>

---

### Flashcard 9
**Que es una tecnica intrusiva de testabilidad?**

<details>
<summary>Ver respuesta</summary>

Una tecnica que **modifica el SUT** para facilitar las pruebas. Ejemplos: agregar test hooks, APIs de prueba, logging adicional. Riesgo: puede introducir defectos en el SUT.
</details>

---

### Flashcard 10
**Que es una tecnica no intrusiva?**

<details>
<summary>Ver respuesta</summary>

Una tecnica que **NO modifica el SUT**. Usa interfaces existentes (GUI, API, CLI) tal como estan. Es mas segura pero puede ser mas limitada.
</details>

---

### Flashcard 11
**Que es un test hook?**

<details>
<summary>Ver respuesta</summary>

Un punto de acceso insertado intencionalmente en el SUT para facilitar las pruebas automatizadas. Es una tecnica **intrusiva**. Ejemplo: un endpoint especial que permite resetear la base de datos.
</details>

---

## Categoria 3: Enfoques de Automatizacion

---

### Flashcard 12
**Que es el enfoque Data-Driven?**

<details>
<summary>Ver respuesta</summary>

Un enfoque donde los **datos de prueba se separan de los scripts** y se almacenan en fuentes externas (CSV, Excel, JSON, DB). El mismo script se ejecuta multiples veces con diferentes conjuntos de datos.
</details>

---

### Flashcard 13
**Que es el enfoque Keyword-Driven?**

<details>
<summary>Ver respuesta</summary>

Un enfoque que usa **palabras clave de negocio** (keywords) para representar acciones. Ejemplo: "Login", "AgregarAlCarrito", "VerificarSaldo". Permite que personas no tecnicas creen casos de prueba.
</details>

---

### Flashcard 14
**Que es Model-Based Testing?**

<details>
<summary>Ver respuesta</summary>

Un enfoque que **genera casos de prueba automaticamente** a partir de modelos del sistema (diagramas de estado, flujos, arboles de decision). Ofrece alta cobertura pero requiere habilidades avanzadas.
</details>

---

### Flashcard 15
**Que es Record and Playback?**

<details>
<summary>Ver respuesta</summary>

Una tecnica que **captura las acciones del usuario** sobre la interfaz del SUT y las convierte en scripts reproducibles. Util para prototipos rapidos, pero los scripts generados son **fragiles y poco mantenibles**.
</details>

---

### Flashcard 16
**Que es el enfoque Script-Based (lineal)?**

<details>
<summary>Ver respuesta</summary>

Scripts de codigo escritos linealmente paso a paso. Simple de crear pero **dificil de mantener** y con **baja reutilizacion**. No se recomienda como estrategia principal a largo plazo.
</details>

---

## Categoria 4: Arquitectura gTAA

---

### Flashcard 17
**Cuales son las 4 capas de la gTAA?**

<details>
<summary>Ver respuesta</summary>

1. **Generacion de pruebas**: Crear/disenar casos de prueba
2. **Definicion de pruebas**: Definir QUE y COMO probar (alto y bajo nivel)
3. **Ejecucion de pruebas**: Motor que ejecuta, configura y reporta
4. **Adaptacion de pruebas**: Interaccion directa con el SUT
</details>

---

### Flashcard 18
**Que hace la capa de generacion de pruebas?**

<details>
<summary>Ver respuesta</summary>

Crea y disena los casos de prueba. Puede ser **manual** (el tester los disena) o **automatica** (generados a partir de modelos, captura, o algoritmos).
</details>

---

### Flashcard 19
**Que hace la capa de definicion de pruebas?**

<details>
<summary>Ver respuesta</summary>

Define las pruebas en dos niveles:
- **Alto nivel**: QUE probar (lenguaje de negocio, independiente de herramienta)
- **Bajo nivel**: COMO probar (scripts ejecutables, dependiente de herramienta)
</details>

---

### Flashcard 20
**Que hace la capa de ejecucion de pruebas?**

<details>
<summary>Ver respuesta</summary>

- Interpreta y ejecuta los scripts de prueba (motor de ejecucion)
- Gestiona la configuracion del entorno
- Compara resultados reales vs esperados
- Genera reportes y logs
- Maneja excepciones durante la ejecucion
</details>

---

### Flashcard 21
**Que hace la capa de adaptacion de pruebas?**

<details>
<summary>Ver respuesta</summary>

Es la **unica capa que interactua directamente con el SUT**. Contiene adaptadores de interfaz (GUI, API, CLI, protocolo) que traducen los comandos del TAS en acciones sobre el SUT.
</details>

---

### Flashcard 22
**Si cambia un elemento de la UI del SUT, que capa se modifica?**

<details>
<summary>Ver respuesta</summary>

Solo la **capa de adaptacion**. Si la gTAA esta bien implementada, las demas capas no necesitan cambiar. Este es el principio de **separacion de responsabilidades**.
</details>

---

### Flashcard 23
**Que es el Page Object Model (POM)?**

<details>
<summary>Ver respuesta</summary>

Un patron de diseno donde cada pagina/componente del SUT tiene una clase que encapsula:
- Los **elementos** de la pagina (localizadores)
- Las **acciones** posibles (metodos)

Los tests usan los Page Objects en lugar de interactuar directamente con la UI. Reduce el impacto de cambios en la interfaz.
</details>

---

## Categoria 5: Riesgos y Mantenimiento

---

### Flashcard 24
**Que es un falso positivo en automatizacion?**

<details>
<summary>Ver respuesta</summary>

Cuando la prueba **reporta un fallo** pero el SUT **esta funcionando correctamente**. Causas comunes: scripts fragiles, datos inconsistentes, entornos inestables, tiempos de espera insuficientes.
</details>

---

### Flashcard 25
**Que es un falso negativo en automatizacion?**

<details>
<summary>Ver respuesta</summary>

Cuando la prueba **pasa exitosamente** pero el SUT **tiene un defecto real**. Es mas peligroso que un falso positivo porque genera falsa confianza. Causa comun: verificaciones insuficientes o incorrectas.
</details>

---

### Flashcard 26
**Cuales son los 4 tipos de mantenimiento del TAS?**

<details>
<summary>Ver respuesta</summary>

1. **Correctivo**: Corregir defectos en los scripts del TAS
2. **Adaptativo**: Adaptar scripts cuando cambia el SUT o entorno
3. **Perfectivo**: Mejorar rendimiento, legibilidad o estructura
4. **Preventivo**: Refactorizar para evitar problemas futuros
</details>

---

### Flashcard 27
**Cual es la principal causa de fracaso en proyectos de automatizacion?**

<details>
<summary>Ver respuesta</summary>

El **costo de mantenimiento no planificado**. Los scripts requieren actualizacion continua cuando cambia el SUT, los datos o el entorno. Sin presupuesto para mantenimiento, el TAS se degrada rapidamente.
</details>

---

### Flashcard 28
**Que estrategia de despliegue se recomienda para un TAS?**

<details>
<summary>Ver respuesta</summary>

**Gradual e incremental** en 3 fases:
1. **Piloto**: Subset pequeno, validar herramienta y enfoque
2. **Expansion**: Ampliar cobertura, refinar framework, capacitar equipo
3. **Optimizacion**: Integrar con CI/CD, monitorear metricas, mejora continua
</details>

---

## Categoria 6: Metricas y Reportes

---

### Flashcard 29
**Que dice la piramide de automatizacion de pruebas?**

<details>
<summary>Ver respuesta</summary>

- **Base (mas grande)**: Pruebas unitarias - rapidas, baratas, estables
- **Medio**: Pruebas de integracion/API - velocidad y costo moderados
- **Cima (mas pequena)**: Pruebas de UI - lentas, caras, fragiles

Se deben tener MAS pruebas unitarias y MENOS de UI.
</details>

---

### Flashcard 30
**Que es el anti-patron del cono de helado?**

<details>
<summary>Ver respuesta</summary>

Una piramide **invertida** donde hay muchas pruebas de UI y pocas unitarias. Es un anti-patron porque:
- Las pruebas de UI son lentas, caras y fragiles
- El suite tarda mucho en ejecutarse
- El mantenimiento es costoso
- El feedback es lento
</details>

---

### Flashcard 31
**Que es la trazabilidad bidireccional?**

<details>
<summary>Ver respuesta</summary>

La capacidad de rastrear en ambas direcciones:
- **Requisito → Prueba**: Que pruebas cubren este requisito?
- **Prueba → Requisito**: Que requisito valida esta prueba?

Permite identificar requisitos sin cobertura y justificar el valor de la automatizacion.
</details>

---

### Flashcard 32
**Nombra 3 metricas del TAS y 3 del SUT.**

<details>
<summary>Ver respuesta</summary>

**Metricas del TAS:**
1. Numero de scripts automatizados
2. Tiempo de ejecucion del suite
3. Tasa de pass/fail de los scripts

**Metricas del SUT:**
1. Defectos encontrados por automatizacion
2. Cobertura de codigo
3. Cobertura de requisitos
</details>

---

## Categoria 7: Transicion y Roles

---

### Flashcard 33
**Que criterios se usan para decidir que pruebas automatizar?**

<details>
<summary>Ver respuesta</summary>

1. **Frecuencia de ejecucion** (alta = automatizar)
2. **Criticidad del negocio** (alta = automatizar)
3. **Estabilidad del requisito** (estable = automatizar)
4. **Volumen de datos** (alto = automatizar)
5. **Complejidad tecnica** (muy alta = evaluar cuidadosamente)
</details>

---

### Flashcard 34
**Que pruebas NO se deben automatizar?**

<details>
<summary>Ver respuesta</summary>

- Pruebas **exploratorias** (requieren juicio humano)
- Pruebas de **usabilidad** (requieren percepcion humana)
- Pruebas **ad-hoc** (no tienen guion fijo)
- Pruebas que se ejecutan **una sola vez**
- Pruebas con requisitos **muy inestables**
- Pruebas con **ROI negativo**
</details>

---

### Flashcard 35
**En que orden se recomienda automatizar durante la transicion?**

<details>
<summary>Ver respuesta</summary>

1. **Smoke tests criticos** (primero - alto valor, baja complejidad)
2. **Pruebas de regresion principales** (segundo - alta frecuencia)
3. **Casos de borde y expansion** (tercero - cobertura adicional)
4. **Expansion continua** (iterativo - mejora continua)
</details>

---

### Flashcard 36
**Cuales son las responsabilidades del TAE?**

<details>
<summary>Ver respuesta</summary>

- Disenar y desarrollar scripts de prueba automatizados
- Mantener y actualizar el framework de automatizacion
- Analizar fallos (distinguir defectos del SUT vs del TAS)
- Colaborar con desarrolladores para mejorar testabilidad
- Generar reportes y metricas de automatizacion
- Seleccionar y evaluar herramientas
</details>

---

### Flashcard 37
**Cuales son los 5 niveles del modelo de madurez de automatizacion?**

<details>
<summary>Ver respuesta</summary>

1. **Inicial**: Sin automatizacion formal, scripts ad-hoc
2. **Gestionado**: Framework basico, algunos scripts estables
3. **Definido**: Framework maduro, patrones de diseno, integracion CI
4. **Medido**: Metricas establecidas, ROI demostrable
5. **Optimizado**: Automatizacion inteligente, self-healing, AI-assisted
</details>

---

## Categoria 8: Conceptos Rapidos

---

### Flashcard 38
**CI/CD en el contexto de automatizacion?**

<details>
<summary>Ver respuesta</summary>

- **CI (Continuous Integration)**: Integracion continua del codigo con ejecucion automatica de pruebas en cada commit
- **CD (Continuous Delivery)**: Entrega continua del software hasta produccion

La automatizacion de pruebas es fundamental para CI/CD: proporciona feedback rapido y confiable.
</details>

---

### Flashcard 39
**Que es un wait explicito vs implicito en automatizacion web?**

<details>
<summary>Ver respuesta</summary>

- **Implicito**: Tiempo fijo de espera para TODOS los elementos (ej: siempre espera 10s)
- **Explicito**: Espera CONDICIONADA para un elemento especifico (ej: espera hasta que el boton sea clickeable, maximo 10s)

Los **explicitos son preferibles** porque son mas precisos y eficientes.
</details>

---

### Flashcard 40
**Que diferencia hay entre framework y herramienta?**

<details>
<summary>Ver respuesta</summary>

- **Herramienta**: Software especifico que ejecuta una funcion (ej: Selenium = interaccion con navegador)
- **Framework**: Estructura completa que organiza herramientas, librerias, patrones y convenciones para crear un TAS robusto (ej: un framework que usa Selenium + TestNG + POM + reportes)

El framework es el "esqueleto", las herramientas son los "organos".
</details>

---

> [!IMPORTANT]
> **Metodo de repaso recomendado:**
> - **Dia 1**: Todas las flashcards. Marca las que fallas.
> - **Dia 2**: Solo las que fallaste + 10 aleatorias.
> - **Dia 3**: Repite el ciclo. Elimina las que ya dominas.
> - **Dia 4+**: Solo las dificiles hasta que las domines todas.
>
> Este metodo se basa en la **repeticion espaciada**, cientificamente probada para mejorar la retencion.
