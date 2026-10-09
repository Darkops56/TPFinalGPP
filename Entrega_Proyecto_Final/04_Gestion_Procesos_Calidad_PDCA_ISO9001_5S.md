# SECCIÓN 4: GESTIÓN DE PROCESOS PRODUCTIVOS, CALIDAD Y MEJORA CONTINUA

---

## 1. Ciclo PDCA (Mejora Continua de Deming aplicada al Software)

De acuerdo con los fundamentos teóricos desarrollados por Walter Shewhart y perfeccionados por W. Edwards Deming presentes en los apuntes de la cátedra, el ciclo **PDCA / PHVA (Planificar - Hacer - Verificar - Actuar)** constituye un método dinámico, iterativo y sin fin para resolver anomalías complejas y optimizar los procesos productivos.

En las etapas preliminares del proyecto, el ciclo PDCA se orientó de forma errónea hacia la obtención de financiamiento por donaciones. En esta versión definitiva, el ciclo ha sido **reorientado formalmente hacia el proceso productivo y técnico del software**, solucionando la causa raíz de la fricción operativa del equipo y los defectos en el código.

```
       +-------------------------------------------------------+
       |             CICLO PDCA - INGENIERÍA DE SOFTWARE       |
       +-------------------------------------------------------+
                     |                                   ^
                     v                                   |
         +-----------------------+           +-----------------------+
         |     1. PLANIFICAR     |           |       4. ACTUAR       |
         | (Plan: Diagnóstico,   |           | (Act: Estandarización,|
         |  KPIs y Objetivos)    |           |  CI en GitHub Actions)|
         +-----------------------+           +-----------------------+
                     |                                   ^
                     v                                   |
         +-----------------------+           +-----------------------+
         |       2. HACER        |           |     3. VERIFICAR      |
         | (Do: RSpec, SOLID y   |---------->| (Check: Métricas QA,  |
         |  Refactorización)     |           |  Cobertura >= 85%)    |
         +-----------------------+           +-----------------------+
```

### A. Etapa 1: Planificar (Plan)
* **Diagnóstico del Problema Técnico:**
  El historial de desarrollo del repositorio registró dos fallas críticas que comprometieron la calidad del producto y la moral del equipo:
  1. *Falla funcional de bloqueo:* El jugador no podía equipar la caña de pescar debido a una inconsistencia de estado en el inventario.
  2. *Alta deuda técnica y fricción de desarrollo:* El módulo de la tienda acumuló un acoplamiento extremo entre la impresión por consola y el cálculo de precios, reflejado en la bitácora: *"la tienda me sacó las ganas de codear"*.
* **Objetivos Cuantificables de la Mejora:**
  - Reducir la tasa de fallas críticas en mecánicas base a **0 incidentes**.
  - Desacoplar la lógica de negocio de la interfaz de consola en 4 semanas.
  - Implementar cobertura de pruebas automatizadas para alcanzar al menos el **85%** del código fuente.
* **Asignación de Recursos y Responsables:**
  - *Herramientas:* Framework `RSpec`, linter `RuboCop` y control de versiones `Git`.
  - *Responsable Principal de Planificación:* Sebastián Zerpa (Líder QA) y Ezequiel Lizasoain (Arquitectura).

### B. Etapa 2: Hacer (Do)
* **Ejecución de la Solución Técnica:**
  - Se estructuró un conjunto de pruebas unitarias automatizadas (`specs`) para verificar el comportamiento de las clases `Jugador`, `Pesca`, `Tienda`, `Pez` y `Objeto`.
  - Se aplicaron principios de diseño orientado a objetos (SOLID), extrayendo la lógica transaccional de compra/venta fuera de los métodos de entrada/salida de la terminal.
  - Se corrigió la asignación de atributos en la clase `Jugador` para asegurar que el método `equipar_herramienta` actualice de forma atómica y persistente el ítem activo.

#### Tabla 2: Registro de Acciones del Plan de Mejora en Desarrollo

| Fecha | Tarea Realizada | Tiempo Invertido | Responsable | Resultado / Observaciones |
|:---:|---|:---:|:---:|---|
| **Semana 1** | Aislamiento y reproducción del bug de caña mediante tests | 8 hs | S. Zerpa | Se escribió test en `spec/jugador_spec.rb` que fallaba sistemáticamente (*Red*). |
| **Semana 2** | Refactorización de la clase `Tienda` (desacoplamiento consola) | 14 hs | E. Lizasoain | Se separaron métodos de cálculo económico de la interfaz (*Green*). |
| **Semana 3** | Incorporación de tests de regresión para transacciones y pesca | 10 hs | S. Zerpa | Suite de pruebas ampliada a 28 casos unitarios. |
| **Semana 4** | Integración del linter `RuboCop` para cumplimiento de estilos | 6 hs | E. Luna | Se corrigieron 52 advertencias de estilo y complejidad ciclomática. |

### C. Etapa 3: Verificar (Check)
* **Evaluación de Resultados Cuantitativos:**
  - **Pruebas de Regresión:** La suite de `RSpec` ejecutó el 100% de los tests con resultado exitoso (**0 fallos, 0 errores**).
  - **Cobertura de Código:** Medida con la gema `SimpleCov`, la cobertura alcanzó el **88,4%**, superando la meta fijada del 85%.
  - **Tolerancia a Fallos:** Se verificó que ante entradas inválidas del usuario o tiempo agotado en eventos de captura (`Timeout::Error`), el sistema maneja la excepción sin cierres forzados.
  - **Clima de Trabajo:** Se eliminó la fricción de desarrollo reportada, facilitando la colaboración fluida entre los cuatro integrantes.

### D. Etapa 4: Actuar (Act)
* **Estandarización y Prevención de Recidivas:**
  - Se estableció como **regla de ingeniería fija** que ninguna modificación de código puede fusionarse a la rama principal (`main`) sin haber superado previamente la suite de pruebas unitarias y la validación de estilo con `RuboCop`.
  - Se implementó un flujo de Integración Continua (CI) en GitHub Actions que ejecuta los tests de manera obligatoria ante cada *Pull Request*.
  - Las lecciones aprendidas se documentaron en las pautas internas de arquitectura del equipo para futuros módulos.

---

## 2. Sistema de Gestión de la Calidad (ISO 9001:2015)

Tomando como base la norma internacional **ISO 9001:2015** provista en los apuntes, el proyecto implementa un Sistema de Gestión de la Calidad (SGC) formal adaptado a los procesos de desarrollo de software.

### A. Política de Calidad de AquaByte Development Studio
> *“En AquaByte Development Studio nos comprometemos a diseñar y producir software interactivo confiable, mantenible y eficiente, garantizando la satisfacción integral de nuestros usuarios mediante el cumplimiento riguroso de especificaciones técnicas, la adopción de pruebas de aseguramiento de calidad (QA), el desarrollo sustentable y la mejora continua de nuestros procesos productivos.”*  
> **Firma:** Equipo de Dirección Técnica (Zerpa, Lizasoain, Luna, Alconz).

### B. Objetivos de Calidad e Indicadores Clave de Desempeño (KPIs)
Para garantizar el control del SGC según el Capítulo 6 de la norma ISO 9001:2015, se fijaron los siguientes objetivos medibles:

| Objetivo de Calidad | Indicador de Medición (KPI) | Meta Establecida | Frecuencia de Control |
|---|---|:---:|:---:|
| **1. Fiabilidad Funcional** | Densidad de defectos críticos en release final | **0 defectos críticos** | Por cada versión liberada |
| **2. Cobertura de Pruebas** | Porcentaje de líneas de código cubiertas por tests RSpec | $\ge \mathbf{85\%}$ | Semanal (vía CI) |
| **3. Tiempo de Respuesta a Bugs** | Tiempo Medio de Reparación (MTTR) en incidentes de código | $< \mathbf{24\text{ horas}}$ | Mensual |
| **4. Conformidad de Código** | Número de violaciones a la guía de estilo RuboCop | **0 advertencias** | En cada Pull Request |
| **5. Satisfacción del Usuario** | Tasa de retención y aprobación en pruebas de usabilidad | $\ge \mathbf{90\%}$ | En cada ciclo de pruebas |

### C. Los 5 Pilares de Calidad aplicados al Código en Ruby
1. **Gestión de Riesgos (Enfoque Preventivo):**  
   Control preventivo de excepciones de concurrencia y temporización (`Timeout::Error`) durante la simulación de pique, validando previamente el inventario de cebos y el estado del jugador para imposibilitar transacciones corruptas.
2. **Control Operacional y Arquitectura Modular:**  
   División de responsabilidades en clases coherentes (`Jugador`, `Pesca`, `Tienda`, `Pez`, `Objeto`). Las reglas de cálculo de valores (peso $\times$ rareza) se encapsulan y protegen de mutaciones arbitrarias.
3. **Información Documentada (Capítulo 7.5 ISO 9001):**  
   Trazabilidad completa mediante commits atómicos y descriptivos en Git, documentación de clases y métodos con convención YARD, y manuales de instalación en el archivo `README.md`.
4. **Evaluación del Desempeño (Capítulo 9 ISO 9001):**  
   Verificación sistemática mediante suites de testing BDD con RSpec, simulando escenarios extremos de inventario lleno, saldo monetario insuficiente y timeouts de captura.
5. **Mejora Continua (Capítulo 10 ISO 9001):**  
   Auditorías internas entre pares (*Code Reviews* cruzados) antes de cada entrega de etapa, transformando las anomalías detectadas en oportunidades de refactorización.

---

## 3. Metodología 5 S aplicada al Proyecto

Conforme a la *“Guía para la implementación del programa 5S”* del INTI y el documento de *“Metodología 5S en la Educación Técnico Profesional”* del Ministerio de Educación de CABA incluidos en los apuntes, la metodología se implementó de forma dual: en el **entorno físico del laboratorio escolar** y en el **entorno digital del repositorio de software**.

```
       +-------------------------------------------------------------+
       |               METODOLOGÍA 5 S EN COMPUTACIÓN                |
       +-------------------------------------------------------------+
         |
         +--> 1. SEIRI (Clasificar): Purgar cables rotos / Código muerto
         |
         +--> 2. SEITON (Ordenar): Puestos rotulados / Carpetas /Classes y /Spec
         |
         +--> 3. SEISO (Limpiar): Mantenimiento de gabinetes / RuboCop -a
         |
         +--> 4. SEIKETSU (Estandarizar): Protocolo de taller / Ruby Style Guide
         |
         +--> 5. SHITSUKE (Disciplina): Auditorías periódicas / Code Reviews cruzados
```

### Tabla 3: Matriz de Aplicación de las 5 S en el Proyecto

| Etapa 5 S | Aplicación en Entorno Físico (Laboratorio / Taller) | Aplicación en Entorno Digital (Software y Repositorio) |
|---|---|---|
| **1. Seiri**  <br>*(Clasificar / Despejar)* | Se retiraron cables periféricos defectuosos, componentes dañados y manuales en papel desactualizados, liberando espacio en los bancos de trabajo. | Se eliminaron bloques de código muerto, gemas no utilizadas en el `Gemfile`, variables sin referencia y ramas obsoletas en el repositorio Git. |
| **2. Seiton** <br>*(Ordenar)* | Se canalizaron los cables bajo zócalos ignífugos; se asignaron gavetas rotuladas para periféricos y herramientas de mantenimiento de hardware. | Se estructuró el árbol de directorios de forma estricta: `/Classes`, `/LogicaJuego`, `/Data`, `/Spec`, adoptando la convención snake_case para archivos y CamelCase para clases. |
| **3. Seiso**  <br>*(Limpiar)* | Se programó la limpieza quincenal con aire comprimido en ventiladores de gabinetes, pantallas y teclados para evitar fallas térmicas. | Se sanitizaron los archivos de datos en `/Data` y se aplicó formateo automático con `rubocop -a` para erradicar espacios innecesarios y malas indentaciones. |
| **4. Seiketsu** <br>*(Estandarizar)* | Se colocaron carteles de verificación y listas de chequeo al inicio y fin de la jornada técnica en el laboratorio de la escuela. | Se oficializó el uso del Ruby Style Guide y se redactaron plantillas unificadas para la apertura de *Pull Requests* y reporte de *Issues*. |
| **5. Shitsuke** <br>*(Disciplina / Hábito)* | Se fijó el hábito ineludible de ordenar la estación de trabajo y verificar el apagado de equipos antes de retirarse. | Se institucionalizó la práctica obligatoria de *Code Review* cruzado entre compañeros y el pase obligatorio de la suite RSpec antes de fusionar código. |
