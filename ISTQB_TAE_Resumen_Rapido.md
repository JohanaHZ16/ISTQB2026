# ISTQB TAE - Resumen Rapido (Cheat Sheet)

> [!TIP]
> Repasa este documento el dia antes del examen. Contiene lo esencial de cada capitulo en formato compacto.

---

## Datos del Examen

| | |
|---|---|
| **40 preguntas** | Opcion multiple |
| **90 min** | 120 min si no es tu idioma nativo |
| **65%** | 26/40 para aprobar |
| **K2-K3-K4** | Comprension, Aplicacion, Analisis |

---

## Cap 1: Introduccion

```mermaid
flowchart LR
    AUTO[Automatizacion] --> SI[Automatizar]
    AUTO --> NO[NO Automatizar]

    SI --> S1[Regresion]
    SI --> S2[Repetitivas]
    SI --> S3[Alto volumen de datos]
    SI --> S4[CI/CD]

    NO --> N1[Exploratorias]
    NO --> N2[Usabilidad]
    NO --> N3[Una sola vez]
    NO --> N4[ROI negativo]
```

> [!IMPORTANT]
> - Automatizacion **complementa**, NO reemplaza pruebas manuales
> - ROI mejora con cada ejecucion adicional
> - Factores de exito: testabilidad del SUT + arquitectura del TAS + habilidades del equipo

---

## Cap 2: Preparacion

```mermaid
flowchart TD
    TEST[Testabilidad] --> OBS[Observabilidad: ver resultados]
    TEST --> CTRL[Controlabilidad: establecer estados]

    ENF[Enfoques] --> SC[Script-Based: lineal, fragil]
    ENF --> DD[Data-Driven: datos externos]
    ENF --> KD[Keyword-Driven: palabras clave de negocio]
    ENF --> MB[Model-Based: genera desde modelos]

    TEC[Tecnicas] --> INT[Intrusiva: modifica SUT]
    TEC --> NINT[No intrusiva: no modifica SUT]
```

> [!IMPORTANT]
> - Seleccion de herramientas = **PoC** (Proof of Concept), no por marketing
> - **Test hook** = punto de acceso intrusivo en el SUT
> - **Keyword-Driven** permite participacion de no-tecnicos

---

## Cap 3: gTAA (EL MAS IMPORTANTE)

```mermaid
flowchart TB
    subgraph gTAA
        G["1. GENERACION
        Crea casos de prueba
        (manual o automatica)"]

        D["2. DEFINICION
        Alto nivel: QUE probar
        Bajo nivel: COMO probar"]

        E["3. EJECUCION
        Motor, config, reportes
        Compara real vs esperado"]

        A["4. ADAPTACION
        Unica que toca el SUT
        Adaptadores: GUI/API/CLI"]
    end

    G --> D --> E --> A --> SUT[SUT]
```

> [!WARNING]
> **Reglas clave para el examen:**
> - Solo la **capa de adaptacion** toca el SUT
> - Si cambia la UI → solo cambia la **capa de adaptacion**
> - Alto nivel = QUE (negocio) | Bajo nivel = COMO (tecnico)
> - **Record & Playback**: rapido pero fragil, NO es estrategia a largo plazo

### Page Object Model (POM)

> [!IMPORTANT]
> - 1 Page Object = 1 pagina/componente del SUT
> - Encapsula **elementos** (localizadores) y **acciones** (metodos)
> - Si cambia la UI → solo cambia el Page Object, NO los tests
> - Reduce drasticamente el costo de mantenimiento

---

## Cap 4: Riesgos

```mermaid
flowchart LR
    R[Riesgos] --> TEC[Tecnicos: scripts fragiles, herramienta incompatible]
    R --> PROC[Proceso: falta habilidades, expectativas irrealistas]
    R --> SUTR[SUT: UI inestable, baja testabilidad]

    M[Mitigacion] --> PIloto[Despliegue gradual]
    M --> SEP[Separacion de capas]
    M --> MANT[Planificar mantenimiento]
```

> [!IMPORTANT]
> - **Falso positivo** = falla la prueba pero el SUT esta bien (reduce confianza)
> - **Falso negativo** = pasa la prueba pero hay defecto (MAS peligroso)
> - **Principal causa de fracaso** = mantenimiento no planificado
> - Despliegue: **Piloto → Expansion → Optimizacion**

### 4 Tipos de Mantenimiento

| Tipo | Cuando |
|------|--------|
| **Correctivo** | Defecto en el TAS |
| **Adaptativo** | Cambia el SUT o entorno |
| **Perfectivo** | Mejorar rendimiento/estructura |
| **Preventivo** | Refactorizar proactivamente |

---

## Cap 5: Metricas

```mermaid
graph TB
    subgraph Piramide["Piramide de Pruebas"]
        UI["UI Tests
        POCOS - lentos - caros"]
        API_T["API / Integration
        MODERADOS"]
        UNIT["Unit Tests
        MUCHOS - rapidos - baratos"]
    end

    UI --> API_T --> UNIT

    style UI fill:#e74c3c,color:#fff
    style API_T fill:#f39c12,color:#fff
    style UNIT fill:#27ae60,color:#fff
```

> [!IMPORTANT]
> - **Piramide**: muchas unitarias, pocas UI
> - **Cono de helado** (anti-patron): muchas UI, pocas unitarias
> - **Trazabilidad bidireccional**: Requisito ↔ Prueba
> - 95% pass rate ≠ buena cobertura (puede haber areas no cubiertas)

### Metricas Clave

| Del TAS | Del SUT |
|---------|---------|
| # scripts automatizados | Defectos encontrados |
| Tiempo de ejecucion | Cobertura de codigo |
| Tasa pass/fail | Cobertura de requisitos |
| Costo mantenimiento/script | Densidad de defectos |

---

## Cap 6: Transicion

```mermaid
flowchart LR
    P[Prioridad de Automatizacion] --> P1["1ro: Smoke tests"]
    P1 --> P2["2do: Regresion"]
    P2 --> P3["3ro: Casos de borde"]
    P3 --> P4["4to: Expansion continua"]
```

> [!IMPORTANT]
> - Transicion **gradual e incremental**, nunca todo de golpe
> - **TAE** = disena, desarrolla y mantiene scripts y framework
> - Mejora continua con ciclo **PDCA** (Plan-Do-Check-Act)
> - **Modelo de madurez**: Inicial → Gestionado → Definido → Medido → Optimizado

---

## Formula de Supervivencia para el Examen

```mermaid
flowchart TD
    P[Leer pregunta 2 veces] --> D[Descartar opciones absurdas]
    D --> A{Quedan 2 opciones?}
    A -->|Si| B[Buscar palabra clave que las diferencia]
    A -->|No| C[Elegir la mas alineada con el syllabus]
    B --> E[Responder]
    C --> E
    E --> F{Seguro?}
    F -->|Si| G[Siguiente pregunta]
    F -->|No| H[Marcar y volver al final]
```

> [!CAUTION]
> **Trampas comunes en el examen:**
> - Palabras como "siempre", "nunca", "todos", "ninguno" → generalmente son **FALSAS**
> - "La automatizacion elimina/reemplaza X" → generalmente es **FALSO**
> - Si dos opciones parecen correctas → busca la que menciona un concepto del syllabus
> - Las respuestas mas largas y especificas suelen ser las correctas

> [!TIP]
> **Distribucion de tiempo:**
> - Preguntas K2: ~1.5 min cada una
> - Preguntas K3: ~2 min cada una
> - Preguntas K4: ~3 min cada una
> - Reserva 10 min al final para revisar las marcadas
