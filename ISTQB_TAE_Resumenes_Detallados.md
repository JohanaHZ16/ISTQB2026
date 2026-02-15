# ISTQB TAE - Resumenes Detallados por Capitulo

---

# Capitulo 1: Introduccion y Objetivos de la Automatizacion de Pruebas

## 1.1 Proposito de la Automatizacion

La automatizacion de pruebas es el uso de software para ejecutar pruebas, comparar resultados reales con esperados y generar reportes.

```mermaid
mindmap
  root((Automatizacion de Pruebas))
    Propositos
      Mejorar eficiencia
      Aumentar cobertura
      Reducir tiempo de ejecucion
      Ejecutar pruebas repetitivas
      Pruebas imposibles manualmente
    Beneficios
      Consistencia
      Repetibilidad
      Velocidad
      Reutilizacion
      Feedback rapido
    Limitaciones
      Costo inicial alto
      Mantenimiento continuo
      No reemplaza pruebas manuales
      Requiere habilidades tecnicas
      No encuentra todos los defectos
```

> [!IMPORTANT]
> La automatizacion **NO** reemplaza las pruebas manuales. Las complementa. Siempre habra pruebas que requieran juicio humano, como pruebas exploratorias o de usabilidad.

## 1.2 Factores de Exito

```mermaid
flowchart LR
    A[Factores de Exito] --> B[Arquitectura del TAS]
    A --> C[Testabilidad del SUT]
    A --> D[Estrategia clara]
    A --> E[Habilidades del equipo]
    A --> F[Mantenibilidad]

    B --> B1[Modular y escalable]
    C --> C1[APIs expuestas, hooks de prueba]
    D --> D1[Alcance definido y realista]
    E --> E1[Conocimiento tecnico adecuado]
    F --> F1[Facil de actualizar y extender]
```

> [!TIP]
> Pregunta frecuente de examen: **"Cual es el factor MAS importante para el exito de la automatizacion?"**
> La respuesta suele estar relacionada con la **testabilidad del SUT** y una **arquitectura bien disenada del TAS**.

## 1.3 Cuando Automatizar y Cuando No

| Automatizar | NO Automatizar |
|------------|----------------|
| Pruebas de regresion | Pruebas que se ejecutan una sola vez |
| Pruebas repetitivas | Pruebas exploratorias |
| Pruebas con muchos datos | Pruebas de usabilidad |
| Pruebas de rendimiento | Requisitos que cambian constantemente |
| Pruebas en CI/CD | Pruebas con ROI negativo |

> [!NOTE]
> El **ROI (Return on Investment)** se calcula considerando:
> - Costo de desarrollo del script automatizado
> - Costo de mantenimiento continuo
> - Numero de veces que se ejecutara
> - Costo de ejecutar la misma prueba manualmente
>
> **Formula simplificada**: ROI = (Costo manual x N ejecuciones) - (Costo automatizacion + Costo mantenimiento)

## 1.4 Ventajas y Desventajas

```mermaid
graph TB
    subgraph Ventajas["Ventajas"]
        V1[Ejecucion mas rapida]
        V2[Mayor cobertura]
        V3[Consistencia en resultados]
        V4[Reutilizacion de scripts]
        V5[Ejecucion 24/7]
        V6[Feedback temprano en CI/CD]
    end

    subgraph Desventajas["Desventajas"]
        D1[Inversion inicial alta]
        D2[Mantenimiento constante]
        D3[Falsos positivos/negativos]
        D4[No detecta problemas visuales]
        D5[Requiere personal calificado]
        D6[Dependencia de herramientas]
    end
```

> [!CAUTION]
> Los **falsos positivos** (la prueba falla pero el sistema esta bien) y los **falsos negativos** (la prueba pasa pero hay un defecto) son riesgos criticos de la automatizacion. Reducen la confianza en el TAS.

---

## Preguntas de Repaso - Capitulo 1

> [!QUESTION]
> **P1: Cual de las siguientes NO es una ventaja de la automatizacion de pruebas?**
> a) Ejecucion mas rapida de pruebas de regresion
> b) Eliminacion total de pruebas manuales
> c) Mayor consistencia en la ejecucion
> d) Capacidad de ejecutar pruebas 24/7

> [!SUCCESS]
> **R1:** b) La automatizacion NO elimina las pruebas manuales. Las complementa.

> [!QUESTION]
> **P2: Cual es un prerrequisito importante antes de automatizar pruebas?**
> a) Tener el mayor numero de herramientas posible
> b) Evaluar la testabilidad del SUT
> c) Automatizar todas las pruebas existentes
> d) Eliminar las pruebas manuales primero

> [!SUCCESS]
> **R2:** b) Evaluar la testabilidad del SUT es fundamental antes de iniciar la automatizacion.

---

# Capitulo 2: Preparacion para la Automatizacion de Pruebas

## 2.1 Factores del SUT que Afectan la Automatizacion

```mermaid
flowchart TD
    SUT[System Under Test - SUT] --> T[Testabilidad]
    SUT --> I[Interfaces]
    SUT --> A[Arquitectura]
    SUT --> TEC[Tecnologia]

    T --> T1[Observabilidad: Poder ver los resultados]
    T --> T2[Controlabilidad: Poder establecer estados]

    I --> I1[GUI - Interfaz grafica]
    I --> I2[API - Interfaz programatica]
    I --> I3[CLI - Linea de comandos]
    I --> I4[Protocolo - Comunicacion directa]

    A --> A1[Modular: Facil de aislar]
    A --> A2[Monolitica: Dificil de aislar]

    TEC --> TEC1[Web, Mobile, Desktop, Embebido]
```

> [!IMPORTANT]
> **Testabilidad** tiene dos dimensiones clave:
> - **Observabilidad**: Capacidad de observar los resultados del SUT (outputs, logs, estados)
> - **Controlabilidad**: Capacidad de establecer el SUT en un estado deseado (inputs, precondiciones)
>
> Sin buena testabilidad, la automatizacion sera costosa y fragil.

## 2.2 Evaluacion y Seleccion de Herramientas

```mermaid
flowchart LR
    A[Evaluacion de Herramientas] --> B{Criterios}
    B --> C[Compatibilidad con SUT]
    B --> D[Soporte del proveedor]
    B --> E[Costo total de propiedad]
    B --> F[Lenguajes soportados]
    B --> G[Integracion con CI/CD]
    B --> H[Curva de aprendizaje]
    B --> I[Comunidad y documentacion]

    C --> J{Evaluacion}
    D --> J
    E --> J
    F --> J
    G --> J
    H --> J
    I --> J

    J --> K[Proof of Concept - PoC]
    K --> L[Seleccion Final]
```

> [!TIP]
> En el examen, recuerda que la seleccion de herramientas debe basarse en un **Proof of Concept (PoC)** y NO solo en las caracteristicas del marketing del proveedor.

## 2.3 Diseno para Testabilidad

```mermaid
graph TB
    DT[Diseno para Testabilidad] --> H[Test Hooks]
    DT --> API[APIs de prueba]
    DT --> LOG[Logging adecuado]
    DT --> CONFIG[Configuracion externalizada]
    DT --> ID[Identificadores unicos en UI]

    H --> H1["Puntos de acceso insertados
    en el SUT para facilitar pruebas"]

    API --> API1["Interfaces programaticas
    que permiten interaccion directa"]

    ID --> ID1["IDs estables en elementos HTML
    que no cambian entre versiones"]
```

> [!WARNING]
> Las tecnicas de testabilidad pueden ser:
> - **Intrusivas**: Modifican el SUT (agregar hooks, APIs de prueba). Riesgo: pueden introducir defectos.
> - **No intrusivas**: No modifican el SUT (usar interfaces existentes). Mas seguras pero pueden ser mas limitadas.

## 2.4 Enfoques de Automatizacion

```mermaid
graph LR
    subgraph Enfoques["Enfoques de Automatizacion"]
        DD[Data-Driven]
        KD[Keyword-Driven]
        MB[Model-Based]
        SC[Script-Based]
    end

    DD --> DD1["Separa datos de los scripts
    Datos en archivos externos
    Excel, CSV, JSON, DB"]

    KD --> KD1["Usa palabras clave de negocio
    Abstrae acciones tecnicas
    Legible por no-tecnicos"]

    MB --> MB1["Genera pruebas desde modelos
    Diagramas de estado, flujos
    Alta cobertura automatica"]

    SC --> SC1["Scripts lineales de codigo
    Simple pero dificil de mantener
    Poco reutilizable"]
```

> [!NOTE]
> **Comparacion de enfoques:**
>
> | Enfoque | Reutilizacion | Mantenimiento | Habilidades Requeridas |
> |---------|:---:|:---:|:---:|
> | Script-Based | Baja | Dificil | Bajas |
> | Data-Driven | Media | Medio | Medias |
> | Keyword-Driven | Alta | Facil | Medias-Altas |
> | Model-Based | Alta | Medio | Altas |

---

## Preguntas de Repaso - Capitulo 2

> [!QUESTION]
> **P1: Que significa que un SUT tenga buena "controlabilidad"?**
> a) Que se puede observar facilmente su comportamiento
> b) Que se puede establecer en un estado deseado para las pruebas
> c) Que tiene una interfaz grafica intuitiva
> d) Que esta bien documentado

> [!SUCCESS]
> **R1:** b) La controlabilidad se refiere a la capacidad de establecer el SUT en un estado deseado.

> [!QUESTION]
> **P2: En un enfoque keyword-driven, quien puede crear los casos de prueba?**
> a) Solo programadores
> b) Solo testers automatizadores
> c) Personas sin conocimientos tecnicos profundos
> d) Solo el arquitecto de automatizacion

> [!SUCCESS]
> **R2:** c) El enfoque keyword-driven usa palabras clave de negocio, lo que permite que personas sin conocimientos tecnicos profundos participen en la creacion de casos de prueba.

---

# Capitulo 3: La Arquitectura Generica de Automatizacion de Pruebas (gTAA)

> [!IMPORTANT]
> Este es el **capitulo mas importante** del examen. La gTAA es el modelo central que debes dominar. Muchas preguntas K3 y K4 se basan en este capitulo.

## 3.1 Vision General de la gTAA

```mermaid
graph TB
    subgraph gTAA["Arquitectura Generica de Automatizacion de Pruebas (gTAA)"]
        subgraph TG["Capa de Generacion de Pruebas"]
            TG1[Generacion Manual]
            TG2[Generacion Automatica]
        end

        subgraph TD["Capa de Definicion de Pruebas"]
            TD1[Definicion de Alto Nivel]
            TD2[Definicion de Bajo Nivel]
        end

        subgraph TE["Capa de Ejecucion de Pruebas"]
            TE1[Motor de Ejecucion]
            TE2[Gestion de Configuracion]
            TE3[Reporte de Resultados]
        end

        subgraph TA["Capa de Adaptacion de Pruebas"]
            TA1[Adaptadores de Interfaz]
            TA2[Interaccion con el SUT]
        end
    end

    TG --> TD
    TD --> TE
    TE --> TA
    TA --> SUT[Sistema Bajo Prueba - SUT]

    subgraph PM["Gestion del Proyecto de Pruebas"]
        PM1[Planificacion]
        PM2[Seguimiento]
        PM3[Control]
    end

    PM -.-> gTAA
```

## 3.2 Capa de Generacion de Pruebas

```mermaid
flowchart TD
    GEN[Capa de Generacion] --> MAN[Generacion Manual]
    GEN --> AUTO[Generacion Automatica]

    MAN --> MAN1["El tester disena los
    casos de prueba manualmente"]
    MAN --> MAN2["Basado en requisitos,
    especificaciones, experiencia"]

    AUTO --> AUTO1["Generacion a partir de modelos
    (Model-Based Testing)"]
    AUTO --> AUTO2["Generacion a partir de
    datos y combinaciones"]
    AUTO --> AUTO3["Captura y reproduccion
    (Record & Playback)"]

    style GEN fill:#4a90d9,color:#fff
```

> [!NOTE]
> **Captura y Reproduccion (Record & Playback)**:
> - Util para crear scripts iniciales rapidamente
> - **Desventaja**: Los scripts generados son fragiles, dificiles de mantener y poco reutilizables
> - Se recomienda como punto de partida, NO como estrategia principal

## 3.3 Capa de Definicion de Pruebas

```mermaid
flowchart TD
    DEF[Capa de Definicion] --> HI[Definicion de Alto Nivel]
    DEF --> LO[Definicion de Bajo Nivel]

    HI --> HI1["Describe QUE probar"]
    HI --> HI2["Lenguaje de negocio"]
    HI --> HI3["Keywords / BDD / Given-When-Then"]
    HI --> HI4["Independiente de la implementacion"]

    LO --> LO1["Describe COMO probar"]
    LO --> LO2["Scripts ejecutables"]
    LO --> LO3["Incluye datos concretos"]
    LO --> LO4["Dependiente de la herramienta"]

    HI -->|"Se traduce a"| LO

    style DEF fill:#27ae60,color:#fff
```

> [!TIP]
> Diferencia clave para el examen:
> - **Alto nivel** = QUE probar (independiente de herramienta)
> - **Bajo nivel** = COMO probar (dependiente de herramienta)
>
> Ejemplo:
> - Alto nivel: "Verificar que el usuario puede iniciar sesion con credenciales validas"
> - Bajo nivel: `driver.findElement(By.id("username")).sendKeys("admin")`

## 3.4 Capa de Ejecucion de Pruebas

```mermaid
flowchart TD
    EXEC[Capa de Ejecucion] --> MOTOR[Motor de Ejecucion]
    EXEC --> CONFIG[Gestion de Configuracion]
    EXEC --> REPORT[Reporte de Resultados]
    EXEC --> SCHED[Programacion y Secuenciacion]

    MOTOR --> M1["Interpreta los scripts de prueba"]
    MOTOR --> M2["Controla el flujo de ejecucion"]
    MOTOR --> M3["Manejo de excepciones"]

    CONFIG --> C1["Entornos de ejecucion"]
    CONFIG --> C2["Parametros de configuracion"]
    CONFIG --> C3["Datos de prueba"]

    REPORT --> R1["Logs de ejecucion"]
    REPORT --> R2["Resultados Pass/Fail"]
    REPORT --> R3["Capturas de pantalla"]
    REPORT --> R4["Metricas de ejecucion"]

    SCHED --> S1["Orden de ejecucion"]
    SCHED --> S2["Ejecucion paralela"]
    SCHED --> S3["Reintentos automaticos"]

    style EXEC fill:#e67e22,color:#fff
```

> [!WARNING]
> El motor de ejecucion debe manejar **excepciones** adecuadamente. Si un paso falla, debe:
> 1. Registrar el fallo con detalle suficiente
> 2. Tomar evidencia (screenshots, logs)
> 3. Decidir si continuar con el siguiente paso o abortar
> 4. Restaurar el estado del SUT si es necesario (teardown/cleanup)

## 3.5 Capa de Adaptacion de Pruebas

```mermaid
flowchart TD
    ADAPT[Capa de Adaptacion] --> GUI[Adaptador GUI]
    ADAPT --> APIT[Adaptador API]
    ADAPT --> CLI[Adaptador CLI]
    ADAPT --> PROT[Adaptador de Protocolo]

    GUI --> GUI1["Interactua con elementos
    visuales del SUT"]
    GUI --> GUI2["Selenium, Appium, Cypress"]

    APIT --> API1["Llamadas HTTP/REST/SOAP"]
    APIT --> API2["REST Assured, Postman"]

    CLI --> CLI1["Comandos de terminal"]
    CLI --> CLI2["Scripts de shell"]

    PROT --> PROT1["TCP/IP, MQTT, etc."]
    PROT --> PROT2["Comunicacion de bajo nivel"]

    GUI --> SUT[SUT]
    APIT --> SUT
    CLI --> SUT
    PROT --> SUT

    style ADAPT fill:#8e44ad,color:#fff
```

> [!IMPORTANT]
> La capa de adaptacion es la **unica capa que interactua directamente con el SUT**. Actua como un "traductor" entre el TAS y el SUT. Si el SUT cambia (por ejemplo, un boton cambia de ID), solo esta capa deberia necesitar modificacion.

## 3.6 Flujo Completo de la gTAA

```mermaid
sequenceDiagram
    participant TG as Generacion
    participant TD as Definicion
    participant TE as Ejecucion
    participant TA as Adaptacion
    participant SUT as SUT

    TG->>TD: Crea casos de prueba (alto nivel)
    TD->>TD: Traduce a scripts (bajo nivel)
    TD->>TE: Envia scripts al motor
    TE->>TE: Configura entorno
    TE->>TA: Envia comandos
    TA->>SUT: Interactua con el sistema
    SUT-->>TA: Respuesta del sistema
    TA-->>TE: Resultado de la interaccion
    TE->>TE: Compara resultado real vs esperado
    TE-->>TE: Genera reporte Pass/Fail
```

## 3.7 Patron de Diseno: Page Object Model

```mermaid
classDiagram
    class BasePage {
        +WebDriver driver
        +waitForElement()
        +click()
        +type()
        +getText()
    }

    class LoginPage {
        -usernameField
        -passwordField
        -loginButton
        +enterUsername(user)
        +enterPassword(pass)
        +clickLogin()
        +login(user, pass)
    }

    class HomePage {
        -welcomeMessage
        -logoutButton
        +getWelcomeText()
        +clickLogout()
        +isLoggedIn()
    }

    class LoginTest {
        +testValidLogin()
        +testInvalidLogin()
        +testEmptyFields()
    }

    BasePage <|-- LoginPage
    BasePage <|-- HomePage
    LoginTest --> LoginPage
    LoginTest --> HomePage
```

> [!TIP]
> El **Page Object Model (POM)** es un patron de diseno fundamental:
> - Cada pagina del SUT tiene una clase correspondiente
> - Los elementos de la pagina son atributos de la clase
> - Las acciones sobre la pagina son metodos de la clase
> - Los tests usan los page objects, NO interactuan directamente con los elementos
>
> **Beneficio**: Si cambia la UI, solo cambias el Page Object, no todos los tests.

---

## Preguntas de Repaso - Capitulo 3

> [!QUESTION]
> **P1: Cual capa de la gTAA interactua directamente con el SUT?**
> a) Capa de generacion
> b) Capa de definicion
> c) Capa de ejecucion
> d) Capa de adaptacion

> [!SUCCESS]
> **R1:** d) La capa de adaptacion es la unica que interactua directamente con el SUT.

> [!QUESTION]
> **P2: En la gTAA, donde se define "QUE probar" vs "COMO probar"?**
> a) En la capa de generacion (QUE) y ejecucion (COMO)
> b) En la capa de definicion: alto nivel (QUE) y bajo nivel (COMO)
> c) En la capa de adaptacion (QUE) y generacion (COMO)
> d) En la capa de ejecucion (QUE) y adaptacion (COMO)

> [!SUCCESS]
> **R2:** b) La capa de definicion tiene dos niveles: alto nivel (QUE probar) y bajo nivel (COMO probar).

> [!QUESTION]
> **P3: Si un boton en la interfaz del SUT cambia su ID, cual capa de la gTAA debe modificarse?**
> a) Capa de generacion
> b) Capa de definicion
> c) Capa de ejecucion
> d) Capa de adaptacion

> [!SUCCESS]
> **R3:** d) Solo la capa de adaptacion debe cambiar, ya que es la que interactua con los elementos del SUT.

> [!QUESTION]
> **P4: Cual es la principal ventaja del Page Object Model?**
> a) Hace los tests mas rapidos de ejecutar
> b) Centraliza la interaccion con la UI para reducir el impacto de cambios
> c) Elimina la necesidad de la capa de adaptacion
> d) Permite ejecutar tests sin navegador

> [!SUCCESS]
> **R4:** b) El POM centraliza la interaccion con la UI, de modo que un cambio en la interfaz solo requiere actualizar el Page Object correspondiente.

---

# Capitulo 4: Riesgos y Contingencias de Despliegue

## 4.1 Tipos de Riesgos

```mermaid
mindmap
  root((Riesgos del TAS))
    Riesgos Tecnicos
      Herramienta incompatible
      Fragilidad de los scripts
      Entornos inestables
      Datos de prueba inconsistentes
      Integracion deficiente
    Riesgos de Proceso
      Falta de habilidades
      Resistencia al cambio
      Expectativas irrealistas
      Falta de mantenimiento
      Scope creep
    Riesgos del SUT
      Cambios frecuentes en la UI
      Falta de testabilidad
      Interfaces inestables
      Versiones incompatibles
      Dependencias externas
```

## 4.2 Gestion de Riesgos

```mermaid
flowchart TD
    A[Identificar Riesgos] --> B[Evaluar Probabilidad e Impacto]
    B --> C[Priorizar Riesgos]
    C --> D{Estrategia de Mitigacion}

    D --> E[Evitar: Eliminar la causa]
    D --> F[Mitigar: Reducir probabilidad o impacto]
    D --> G[Transferir: Delegar a terceros]
    D --> H[Aceptar: Asumir el riesgo]

    E --> I[Monitorear y Revisar]
    F --> I
    G --> I
    H --> I

    I --> A
```

> [!WARNING]
> **Riesgos mas comunes y sus mitigaciones:**
>
> | Riesgo | Mitigacion |
> |--------|-----------|
> | Scripts fragiles | Usar patrones de diseno robustos (POM), waits explicitos |
> | Cambios frecuentes en UI | Aislar la interaccion en la capa de adaptacion |
> | Datos de prueba inconsistentes | Gestionar datos de prueba independientemente |
> | Falta de habilidades | Capacitacion continua del equipo |
> | Entornos inestables | Entornos dedicados para automatizacion |

## 4.3 Estrategia de Despliegue

```mermaid
flowchart LR
    subgraph Fase1["Fase 1: Piloto"]
        P1[Seleccionar subset pequeno]
        P2[Validar herramienta]
        P3[Establecer metricas base]
    end

    subgraph Fase2["Fase 2: Expansion"]
        E1[Ampliar cobertura gradualmente]
        E2[Refinar framework]
        E3[Capacitar al equipo]
    end

    subgraph Fase3["Fase 3: Optimizacion"]
        O1[Integrar con CI/CD]
        O2[Monitorear metricas]
        O3[Mejora continua]
    end

    Fase1 --> Fase2 --> Fase3
```

> [!TIP]
> El despliegue debe ser **gradual e incremental**. Nunca intentes automatizar todo de una vez. Un piloto exitoso da confianza y permite ajustar la estrategia antes de escalar.

## 4.4 Mantenimiento del TAS

```mermaid
flowchart TD
    MAINT[Mantenimiento del TAS] --> TIPOS{Tipos de Mantenimiento}

    TIPOS --> CORRECT[Correctivo]
    TIPOS --> ADAPT[Adaptativo]
    TIPOS --> PERF[Perfectivo]
    TIPOS --> PREVENT[Preventivo]

    CORRECT --> C1["Corregir scripts que fallan
    por defectos en el TAS"]

    ADAPT --> A1["Adaptar scripts cuando
    cambia el SUT o entorno"]

    PERF --> P1["Mejorar rendimiento,
    legibilidad, estructura"]

    PREVENT --> PR1["Refactorizar para evitar
    problemas futuros"]
```

> [!CAUTION]
> El **costo de mantenimiento** es la principal razon por la que los proyectos de automatizacion fracasan. Planifica y presupuesta el mantenimiento desde el inicio del proyecto.

---

## Preguntas de Repaso - Capitulo 4

> [!QUESTION]
> **P1: Cual es la estrategia recomendada para desplegar la automatizacion de pruebas?**
> a) Automatizar todo de una sola vez para maximizar el ROI
> b) Un enfoque gradual e incremental comenzando con un piloto
> c) Esperar hasta que el SUT este completamente estable
> d) Comenzar por las pruebas mas complejas para demostrar valor

> [!SUCCESS]
> **R1:** b) El enfoque gradual e incremental permite validar la estrategia y ajustar antes de escalar.

> [!QUESTION]
> **P2: Cual es la principal causa de fracaso en proyectos de automatizacion?**
> a) Seleccion incorrecta de herramientas
> b) Falta de presupuesto inicial
> c) Costo de mantenimiento no planificado
> d) Falta de apoyo de la gerencia

> [!SUCCESS]
> **R2:** c) El costo de mantenimiento no planificado es la principal causa de fracaso. Los scripts requieren actualizacion continua.

---

# Capitulo 5: Reportes y Metricas de Automatizacion de Pruebas

## 5.1 Tipos de Metricas

```mermaid
mindmap
  root((Metricas))
    Metricas del TAS
      Numero de scripts automatizados
      Tiempo de ejecucion del suite
      Tasa de scripts que pasan vs fallan
      Cobertura de automatizacion
      Tiempo de creacion de scripts
      Costo de mantenimiento por script
    Metricas del SUT
      Defectos encontrados por automatizacion
      Cobertura de codigo
      Cobertura de requisitos
      Densidad de defectos
    Metricas de Eficiencia
      ROI de la automatizacion
      Ahorro de tiempo vs manual
      Frecuencia de ejecucion
      Tiempo de feedback
```

## 5.2 Piramide de Automatizacion de Pruebas

```mermaid
graph TB
    subgraph Piramide["Piramide de Automatizacion"]
        UI["UI Tests
        (Pocos - Lentos - Costosos)"]

        API_T["API / Integration Tests
        (Moderados - Velocidad media)"]

        UNIT["Unit Tests
        (Muchos - Rapidos - Baratos)"]
    end

    UI --> API_T --> UNIT

    style UI fill:#e74c3c,color:#fff
    style API_T fill:#f39c12,color:#fff
    style UNIT fill:#27ae60,color:#fff
```

> [!IMPORTANT]
> La **piramide de pruebas** indica que:
> - La **base** (unit tests) debe ser la mas grande: son rapidos, baratos y estables
> - El **medio** (API/integracion) debe ser moderado
> - La **cima** (UI) debe ser la mas pequena: son lentos, caros y fragiles
>
> **Anti-patron**: El "cono de helado" invierte la piramide con muchas pruebas UI y pocas unitarias.

## 5.3 Dashboard y Reportes

```mermaid
flowchart TD
    EXEC[Ejecucion de Pruebas] --> RAW[Datos Crudos]
    RAW --> PROC[Procesamiento]

    PROC --> DASH[Dashboard]
    PROC --> REP[Reportes]
    PROC --> ALERT[Alertas]

    DASH --> D1[Estado actual de pruebas]
    DASH --> D2[Tendencias historicas]
    DASH --> D3[Cobertura visual]

    REP --> R1[Resumen ejecutivo]
    REP --> R2[Detalle tecnico]
    REP --> R3[Trazabilidad con requisitos]

    ALERT --> A1[Fallos criticos]
    ALERT --> A2[Degradacion de rendimiento]
    ALERT --> A3[Umbral de calidad no alcanzado]
```

> [!NOTE]
> Un buen reporte de automatizacion debe incluir:
> - **Resumen**: Pass/Fail totales, porcentaje de exito
> - **Tendencias**: Comparacion con ejecuciones anteriores
> - **Detalles de fallos**: Logs, screenshots, pasos para reproducir
> - **Trazabilidad**: Mapeo con requisitos y casos de prueba
> - **Metricas de eficiencia**: Tiempo total, tiempo promedio por test

## 5.4 Logging y Trazabilidad

```mermaid
flowchart LR
    REQ[Requisito] --> TC[Caso de Prueba]
    TC --> SCRIPT[Script Automatizado]
    SCRIPT --> RESULT[Resultado]
    RESULT --> DEFECT[Defecto - si falla]

    REQ -.->|Trazabilidad Completa| DEFECT
```

> [!TIP]
> La **trazabilidad bidireccional** permite:
> - Desde un requisito, saber que pruebas automatizadas lo cubren
> - Desde un defecto, saber que requisito se ve afectado
> - Identificar requisitos sin cobertura automatizada
> - Justificar el valor de la automatizacion ante stakeholders

---

## Preguntas de Repaso - Capitulo 5

> [!QUESTION]
> **P1: Segun la piramide de automatizacion, que tipo de pruebas deberian ser las mas numerosas?**
> a) Pruebas de UI
> b) Pruebas de integracion
> c) Pruebas unitarias
> d) Pruebas de rendimiento

> [!SUCCESS]
> **R1:** c) Las pruebas unitarias forman la base de la piramide y deben ser las mas numerosas.

> [!QUESTION]
> **P2: Que es el "anti-patron del cono de helado" en automatizacion?**
> a) Tener demasiadas pruebas unitarias
> b) Invertir la piramide con muchas pruebas UI y pocas unitarias
> c) No tener pruebas de integracion
> d) Ejecutar pruebas sin reportes

> [!SUCCESS]
> **R2:** b) El cono de helado es una piramide invertida donde la mayoria de las pruebas son de UI, lo cual es costoso, fragil y lento.

---

# Capitulo 6: Transicion de Pruebas Manuales a Automatizadas

## 6.1 Criterios para Seleccionar Pruebas a Automatizar

```mermaid
flowchart TD
    SELECT[Seleccion de Pruebas para Automatizar] --> CRIT{Criterios de Evaluacion}

    CRIT --> FREQ[Frecuencia de Ejecucion]
    CRIT --> CRIT2[Criticidad del Negocio]
    CRIT --> COMP[Complejidad Tecnica]
    CRIT --> STAB[Estabilidad del Requisito]
    CRIT --> DATA[Volumen de Datos]

    FREQ --> |Alta frecuencia| HIGH[Alta Prioridad para Automatizar]
    CRIT2 --> |Alta criticidad| HIGH
    DATA --> |Gran volumen| HIGH

    COMP --> |Muy complejo| LOW[Baja Prioridad]
    STAB --> |Requisito inestable| LOW

    HIGH --> AUTO[Automatizar]
    LOW --> MANUAL[Mantener Manual]
```

> [!IMPORTANT]
> **Regla de oro para decidir que automatizar:**
>
> Automatiza pruebas que son:
> 1. **Repetitivas**: Se ejecutan frecuentemente
> 2. **Estables**: Los requisitos no cambian cada semana
> 3. **De alto volumen**: Requieren muchos datos o combinaciones
> 4. **Criticas**: Cubren funcionalidades core del negocio
> 5. **Tediosas**: Propensas a error humano por monotonia

## 6.2 Estrategia de Transicion

```mermaid
flowchart TD
    START[Inicio de Transicion] --> EVAL[Evaluar Suite de Pruebas Actual]
    EVAL --> CLASS[Clasificar Pruebas]

    CLASS --> A[Candidatas a Automatizar]
    CLASS --> B[Mantener Manuales]
    CLASS --> C[Eliminar - Obsoletas]

    A --> PRIOR[Priorizar por Valor]
    PRIOR --> SPRINT1[Sprint 1: Pruebas de humo criticas]
    SPRINT1 --> SPRINT2[Sprint 2: Regresion principal]
    SPRINT2 --> SPRINT3[Sprint 3: Casos de borde]
    SPRINT3 --> SPRINT4[Sprint N: Expansion continua]

    SPRINT4 --> REVIEW[Revision y Ajuste]
    REVIEW --> PRIOR
```

## 6.3 Modelo de Madurez de Automatizacion

```mermaid
graph BT
    L1["Nivel 1: Inicial
    - Sin automatizacion formal
    - Scripts ad-hoc
    - Sin framework"]

    L2["Nivel 2: Gestionado
    - Framework basico
    - Algunos scripts estables
    - Proceso definido"]

    L3["Nivel 3: Definido
    - Framework maduro
    - Patrones de diseno
    - Integracion con CI"]

    L4["Nivel 4: Medido
    - Metricas establecidas
    - ROI demostrable
    - Optimizacion continua"]

    L5["Nivel 5: Optimizado
    - Automatizacion inteligente
    - Self-healing tests
    - AI-assisted testing"]

    L1 --> L2 --> L3 --> L4 --> L5

    style L1 fill:#e74c3c,color:#fff
    style L2 fill:#e67e22,color:#fff
    style L3 fill:#f1c40f,color:#000
    style L4 fill:#2ecc71,color:#fff
    style L5 fill:#3498db,color:#fff
```

## 6.4 Roles y Responsabilidades

```mermaid
flowchart LR
    subgraph Roles["Roles en Automatizacion"]
        TAE_R["TAE
        Test Automation Engineer"]
        TM["Test Manager"]
        TA_ARCH["Test Automation
        Architect"]
        DEV["Developer"]
        BA["Business Analyst"]
    end

    TAE_R --> R1["Disena, desarrolla y
    mantiene scripts"]
    TM --> R2["Planifica y gestiona
    la estrategia"]
    TA_ARCH --> R3["Define la arquitectura
    y framework"]
    DEV --> R4["Colabora en testabilidad
    del SUT"]
    BA --> R5["Define criterios de
    aceptacion automatizables"]
```

> [!NOTE]
> El **TAE (Test Automation Engineer)** es el rol central. Sus responsabilidades incluyen:
> - Disenar y desarrollar scripts de prueba automatizados
> - Mantener y actualizar el framework de automatizacion
> - Analizar fallos y distinguir entre defectos del SUT y del TAS
> - Colaborar con desarrolladores para mejorar la testabilidad
> - Generar reportes y metricas de automatizacion

## 6.5 Mejora Continua del TAS

```mermaid
flowchart TD
    subgraph PDCA["Ciclo PDCA para Automatizacion"]
        PLAN[Plan: Identificar mejoras]
        DO[Do: Implementar cambios]
        CHECK[Check: Medir resultados]
        ACT[Act: Estandarizar o ajustar]
    end

    PLAN --> DO --> CHECK --> ACT --> PLAN
```

> [!TIP]
> **Areas clave de mejora continua:**
> - **Rendimiento**: Reducir el tiempo total de ejecucion del suite
> - **Estabilidad**: Reducir falsos positivos y scripts fragiles
> - **Cobertura**: Aumentar el porcentaje de pruebas automatizadas
> - **Mantenibilidad**: Refactorizar codigo para mayor claridad
> - **Integracion**: Mejorar la integracion con el pipeline CI/CD

---

## Preguntas de Repaso - Capitulo 6

> [!QUESTION]
> **P1: Cual de las siguientes pruebas es la PEOR candidata para automatizacion?**
> a) Prueba de regresion ejecutada en cada sprint
> b) Prueba exploratoria ad-hoc
> c) Prueba de humo con datos predecibles
> d) Prueba de rendimiento bajo carga

> [!SUCCESS]
> **R1:** b) Las pruebas exploratorias requieren juicio humano, creatividad y no siguen un guion fijo, por lo que no son buenas candidatas para automatizacion.

> [!QUESTION]
> **P2: En que orden se recomienda automatizar las pruebas durante la transicion?**
> a) Todas al mismo tiempo para ahorrar esfuerzo
> b) Primero las mas complejas para demostrar capacidad
> c) Primero pruebas de humo criticas, luego regresion, luego expansion
> d) Primero las pruebas que fallan mas frecuentemente

> [!SUCCESS]
> **R2:** c) Se recomienda un enfoque gradual comenzando por pruebas de humo criticas, luego regresion principal y finalmente expansion a otros tipos.

> [!QUESTION]
> **P3: Cual es la responsabilidad PRINCIPAL del Test Automation Engineer?**
> a) Definir la estrategia de pruebas del proyecto
> b) Disenar, desarrollar y mantener los scripts automatizados
> c) Aprobar las releases del producto
> d) Gestionar el presupuesto de pruebas

> [!SUCCESS]
> **R3:** b) El TAE es responsable de disenar, desarrollar y mantener los scripts y el framework de automatizacion.

---

# Resumen Visual Completo

```mermaid
graph TB
    subgraph CAP1["Cap 1: Introduccion"]
        C1[Proposito y objetivos]
        C1B[Ventajas y limitaciones]
        C1C[Factores de exito]
    end

    subgraph CAP2["Cap 2: Preparacion"]
        C2[Testabilidad del SUT]
        C2B[Seleccion de herramientas]
        C2C[Enfoques de automatizacion]
    end

    subgraph CAP3["Cap 3: gTAA"]
        C3[Generacion - Definicion]
        C3B[Ejecucion - Adaptacion]
        C3C[Page Object Model]
    end

    subgraph CAP4["Cap 4: Riesgos"]
        C4[Riesgos tecnicos y proceso]
        C4B[Estrategia de despliegue]
        C4C[Mantenimiento del TAS]
    end

    subgraph CAP5["Cap 5: Metricas"]
        C5[Metricas del TAS y SUT]
        C5B[Piramide de pruebas]
        C5C[Reportes y trazabilidad]
    end

    subgraph CAP6["Cap 6: Transicion"]
        C6[Criterios de seleccion]
        C6B[Estrategia incremental]
        C6C[Mejora continua]
    end

    CAP1 --> CAP2 --> CAP3 --> CAP4 --> CAP5 --> CAP6

    style CAP3 fill:#e74c3c,color:#fff
```

> [!IMPORTANT]
> **Prioridades de estudio para el examen:**
> 1. **Capitulo 3 (gTAA)** - El mas importante y con mayor peso en el examen
> 2. **Capitulo 2 (Preparacion)** - Testabilidad y enfoques son temas frecuentes
> 3. **Capitulo 6 (Transicion)** - Preguntas practicas de analisis (K4)
> 4. **Capitulo 4 (Riesgos)** - Preguntas de aplicacion (K3)
> 5. **Capitulo 5 (Metricas)** - Preguntas de comprension (K2)
> 6. **Capitulo 1 (Introduccion)** - Preguntas basicas (K2)

---

*Este documento es una guia de estudio detallada. Se recomienda complementar con el syllabus oficial de ISTQB y examenes de practica.*
