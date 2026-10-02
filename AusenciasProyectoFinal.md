# Auditoría y Análisis de Brechas: Proyecto Final de Gestión de los Procesos Productivos

**Especialidad:** Computación | **Curso:** 6.º Año  
**Materia:** Gestión de los Procesos Productivos  
**Proyecto Evaluado:** Sistema / Videojuego de Pesca en Ruby  
**Integrantes:** Sebastián Zerpa, Ezequiel Lizasoain, Enzo Luna, Maycol Alconz  
**Documentos Contrastados:**  
- **Pautas y Reglas de Negocio:** `Proyecto final (Presentación).docx`  
- **Estado Actual del Trabajo:** `Proyecto.docx`  

---

## 1. Resumen Ejecutivo y Diagnóstico Global

- **Grado de Cumplimiento General:** **32% / 100%**
- **Estado de Situación:**  
  El documento `Proyecto.docx` presenta fundamentos conceptuales sólidos y bien orientados al desarrollo de software en lo relativo a **ISO 9001**, **Sostenibilidad (Triple Impacto)** y **Plan de Mantenimiento**. Sin embargo, **carece de más del 65% de las pautas obligatorias** establecidas en `Proyecto final (Presentación).docx`.
- **Principales Carencias Detectadas:**  
  Ausencia total de: Carátula formal, Misión y Visión, Layout (físico y lógico), Metodología 5 S, Sistema de Gestión Ambiental (ISO 14001 formal), Clasificación y Gestión de Residuos (RAEE), Higiene y Seguridad Laboral / EPP, Matriz Legal, Presupuesto/Costos, Diagrama de Gantt y Conclusiones. Asimismo, no se encuentra planificada la estructura de la **Presentación Digital (12 diapositivas)** requerida para la defensa oral de 15 minutos.

---

## 2. Matriz de Calificación y Puntuación por Pauta

A continuación se califica cada pauta exigida por la cátedra (escala de 1 a 10), contrastando el contenido actual frente a los requerimientos formales:

| # | Pauta / Requisito de la Cátedra | Calificación | Estado | Situación en `Proyecto.docx` | Acciones Requeridas (Agregar / Modificar) |
|---|---|:---:|:---:|---|---|
| **1** | **Estructura y Portada Institucional** | **2 / 10** | 🔴 Crítico | Encabezado simple: *"Proyecto Juego de pesca"*. | Diseñar carátula institucional completa (ET N° 12, materia, curso, integrantes, año), índice y numeración de páginas (3 a 5 pág.). |
| **2** | **Descripción del Prototipo y Objetivos** | **3 / 10** | 🔴 Incompleto | Menciona clases (`Jugador`, `Pesca`, `Tienda`) dentro de ISO 9001. | Redactar descripción funcional del juego, objetivos generales/específicos y justificación técnica del diseño. |
| **3** | **Misión y Visión** | **0 / 10** | ❌ Ausente | No se menciona en el documento. | Redactar la Misión y Visión del equipo/estudio de desarrollo orientado a la calidad y software confiable. |
| **4** | **Materiales, Componentes y Costos** | **1 / 10** | 🔴 Crítico | Solo nombra herramientas sueltas (Ruby, Git, RSpec). | Cuadro técnico de componentes (hardware/software) y tabla de presupuesto con costos estimados (horas-hombre, licencias, servicios). |
| **5** | **Ciclo PDCA (Mejora Continua)** | **6 / 10** | 🟡 Regular | Enfocado únicamente en financiamiento y donaciones. | Reorientar el PDCA hacia el proceso productivo y técnico del software (ej. corrección de fallas críticas y modularización). |
| **6** | **Sistema de Calidad (ISO 9001)** | **8 / 10** | 🟢 Bueno | Desarrollado bajo 5 pilares, pruebas RSpec, QA y refactorización. | Formalizar la Política de Calidad, Objetivos de Calidad con KPIs medibles y un breve mapa/flujo de procesos. |
| **7** | **Metodología 5 S** | **0 / 10** | ❌ Ausente | No se menciona en absoluto. | Aplicar Seiri, Seiton, Seiso, Seiketsu y Shitsuke al entorno de trabajo informático y al repositorio de código en Ruby. |
| **8** | **Layout (Distribución de Planta)** | **0 / 10** | ❌ Ausente | No existe en el documento. | Elaborar plano de Layout físico de la oficina/laboratorio de desarrollo y Layout lógico de arquitectura de software, justificando beneficios. |
| **9** | **Plan de Mantenimiento Total** | **8.5 / 10** | 🟢 Muy Bueno | Preventivo (RuboCop, gems), correctivo (issues, hotfixes) y predictivo (ML y DB). | Muy buen enfoque técnico. Falta tabularlo en un Plan Operativo formal con frecuencias, responsables, herramientas y SLAs. |
| **10** | **Sostenibilidad (Triple Impacto)** | **8 / 10** | 🟢 Bueno | Desarrollado en Social (colaboración), Económico (monetización) y Ambiental (cómputo). | Incorporar métricas cuantificables (reducción de consumo de CPU, tiempo de ejecución y eficiencia de recursos). |
| **11** | **Gestión Ambiental (ISO 14001)** | **1 / 10** | 🔴 Crítico | Solo contiene 2 párrafos sobre eficiencia de procesamiento. | Reestructurar bajo requisitos formales de ISO 14001: Política ambiental, matriz de aspectos/impactos y programas de gestión ambiental. |
| **12** | **Gestión de Residuos (RAEE y consumo)** | **0 / 10** | ❌ Ausente | No se menciona la gestión de residuos. | Detallar clasificación técnica de residuos informáticos (RAEE, consumibles, residuos secos), disposición final y reducción de consumo. |
| **13** | **Seguridad e Higiene Laboral y EPP** | **0 / 10** | ❌ Ausente | No existe en el documento. | Marco normativo (Ley 19.587, Dec. 351/79, Res. SRT 295/03), riesgos ergonómicos, visuales, eléctricos, EPP y señalética. |
| **14** | **Ciclo de Vida del Producto (ACV)** | **2 / 10** | 🔴 Incompleto | Mencionado tangencialmente en mantenimiento. | Diagrama formal de fases del ciclo de vida del software (análisis, diseño, desarrollo, pruebas, despliegue, retiro) y puntos críticos. |
| **15** | **Matriz Legal y Justificación** | **0 / 10** | ❌ Ausente | No existe en el documento. | Matriz con legislación argentina aplicable: Ley 11.723 (Software), Ley 25.326 (Habeas Data), Ley 19.587 (SySO), Ley 24.240 (Consumidor), Licencias. |
| **16** | **Planificación y Diagrama de Gantt** | **0 / 10** | ❌ Ausente | No existe en el documento. | Cronograma en barras de Gantt detallando etapas, tareas, duraciones semanales, dependencias y responsables asignados. |
| **17** | **Conclusiones del Grupo** | **0 / 10** | ❌ Ausente | No existe en el documento. | Reflexión final grupal que integre el aprendizaje técnico (programación en Ruby) con la gestión de procesos industriales y normativas. |
| **18** | **Esquema de Presentación (12 Diapositivas)** | **0 / 10** | ❌ Ausente | No está planificado en el archivo. | Estructurar el contenido slide por slide respetando estrictamente los 12 tópicos exigidos en las pautas. |

---

## 3. Análisis Profundo de Brechas y Propuestas de Contenido

### 3.1. Reajustes sobre lo que ya está escrito

#### A. Ciclo PDCA (Mejora Continua)
- **Problema detectado:** El PDCA actual se centra en: *"Necesitamos encontrar una forma de obtener fondos económicos para satisfacer el proyecto mediante donaciones"*. La materia es técnica e industrial; el foco debe estar puesto en el **proceso de desarrollo y calidad del software**.
- **Propuesta de modificación:**
  - **Planificar (Plan):** Detectar la alta tasa de fallas en mecánicas clave (bug del equipamiento de la caña de pescar) y la rigidez del código en la tienda (*"la tienda me sacó las ganas de codear"*). Objetivo: reducir defectos a cero en mecánicas base y desacoplar la interfaz de la lógica de negocio en 4 semanas.
  - **Hacer (Do):** Implementar framework de testing automatizado `RSpec`, escribir tests de regresión para las clases `Jugador`, `Pesca` y `Tienda`, y refactorizar el código aplicando patrones orientados a objetos.
  - **Verificar (Check):** Correr la suite de pruebas. Comprobar que la cobertura de pruebas alcance el 85% y que el bug de la caña no se vuelva a manifestar ante nuevas modificaciones.
  - **Actuar (Act):** Establecer como estándar obligatorio que ningún módulo se integre a la rama principal de Git sin pruebas unitarias aprobadas (integración continua).

#### B. Sistema de Gestión de Calidad (ISO 9001)
- **Puntos fuertes actuales:** Muy buen planteamiento de 5 pilares (Gestión de Riesgos, Control Operacional, Información Documentada, Evaluación de Desempeño y Mejora Continua), pruebas con RSpec y control con Git.
- **Qué agregar para completar el estándar:**
  - **Política de Calidad:** Declaración formal donde el equipo se compromete a entregar un software interactivo confiable, mantenible y centrado en la satisfacción del usuario.
  - **Objetivos de Calidad e Indicadores (KPIs):**
    - Cobertura de código con tests $\ge 80\%$.
    - Tiempo de resolución de bugs críticos $< 24\text{ horas}$.
    - Cero fallas en release final de producción.

#### C. Plan de Mantenimiento Total
- **Puntos fuertes actuales:** Se identifican con gran criterio el mantenimiento preventivo (RuboCop, actualización de dependencias, copias de seguridad de `/Data`), correctivo (GitHub Issues, hotfixes) y predictivo (telemetría de fugas de memoria RAM y degradación de base de datos).
- **Qué agregar:** Plasmarlo en una **tabla operativa** con tareas, frecuencias, herramientas y responsables asignados:
  ```text
  | Nivel | Tarea Específica | Frecuencia | Responsable | Herramienta | SLA / Tiempo |
  | Preventivo | Auditoría de código estático | Semanal | Ezequiel L. | RuboCop | 1 hora |
  | Preventivo | Actualización de gemas y parches | Mensual | Sebastián Z. | Bundler Audit | 2 horas |
  | Preventivo | Respaldo de carpeta Data | Diario | Maycol A. | Backup script | 15 minutos |
  | Correctivo | Atención de incidentes críticos | A demanda | Enzo L. | GitHub Issues | < 24 horas |
  | Predictivo | Análisis de consumo de memoria | Quincenal | Sebastián Z. | Profiler / Telemetría | 2 horas |
  ```

---

### 3.2. Contenidos Nuevos Obligatorios a Incorporar

#### A. Identidad Organizacional: Misión y Visión
- **Misión:** Diseñar y desarrollar un software de simulación y entretenimiento en Ruby, aplicando principios de arquitectura modular, buenas prácticas de desarrollo y control de calidad riguroso para asegurar una experiencia de usuario óptima y libre de fallas.
- **Visión:** Consolidarse como un proyecto referente de código abierto en simulaciones computacionales educativas, demostrando que el desarrollo de software puede integrar de manera armónica la calidad industrial, la ergonomía laboral y la sostenibilidad ambiental.

#### B. Descripción General del Prototipo y Objetivos
- **Descripción:** Minijuego de simulación de pesca por consola/interfaz ligera desarrollado en lenguaje Ruby, estructurado en arquitectura orientada a objetos (clases `Jugador`, `Pesca`, `Tienda`, `Pez`, `Objeto`). Permite al usuario interactuar con eventos temporizados de captura, gestión de inventario, economía interna de compra/venta de cebos e ítems, y persistencia de progreso en archivos de datos.
- **Objetivo General:** Desarrollar un prototipo funcional de software que integre los estándares técnicos de computación con las normativas industriales de calidad, ambiente y seguridad laboral.
- **Objetivos Específicos:**
  - Implementar lógica desacoplada y validada mediante tests automatizados en RSpec.
  - Minimizar el consumo de recursos computacionales (eficiencia de CPU y memoria).
  - Diseñar un sistema mantenible, escalable y documentado bajo control de versiones Git.

#### C. Presupuesto y Costos Estimados
Tabla económica para justificar la viabilidad del proyecto:

| Rubro | Concepto | Cantidad | Costo Unitario (ARS) | Costo Total (ARS) |
|---|---|:---:|:---:|:---:|
| **Hardware** | Estaciones de desarrollo (amortización PCs) | 4 equipos | $ 800.000 | $ 3.200.000 |
| **Software** | Entorno de desarrollo (Ruby, VS Code, Git) | 4 licencias | $ 0 (Open Source) | $ 0 |
| **Infraestructura** | Repositorio GitHub Team / CI / Hosting | 1 año | $ 50.000 | $ 50.000 |
| **Mano de Obra (RRHH)** | Horas de desarrollo (4 integrantes x 80 hs) | 320 hs | $ 7.500 / h | $ 2.400.000 |
| **Servicios e Insumos** | Conectividad a Internet y suministro eléctrico | 3 meses | $ 90.000 / mes | $ 270.000 |
| **Seguridad y Ergonomía** | Filtros de pantalla, regletas térmicas, EPP | Kit grupal | $ 80.000 | $ 80.000 |
| **TOTAL ESTIMADO** | | | | **$ 6.000.000** |

#### D. Metodología 5 S aplicada al Proyecto
1. **Seiri (Clasificar / Despejar):**
   - *Físico:* Eliminar cables en desuso, periféricos defectuosos y documentación en papel obsoleta en el laboratorio.
   - *Software:* Purgar código muerto, librerías no utilizadas y ramas huérfanas en Git.
2. **Seiton (Ordenar):**
   - *Físico:* Disponer periféricos, cables canalizados y puestos de trabajo rotulados.
   - *Software:* Organización estricta de carpetas (`/Classes`, `/LogicaJuego`, `/Data`, `/Spec`) y nombres consistentes de variables y métodos.
3. **Seiso (Limpiar):**
   - *Físico:* Limpieza periódica de gabinetes, filtros de ventilación, teclados y monitores.
   - *Software:* Ejecución de linters (`rubocop -a`) para formateo automático y sanitización de archivos de datos.
4. **Seiketsu (Estandarizar):**
   - *Físico:* Protocolo de orden al inicio y cierre de cada jornada de desarrollo.
   - *Software:* Adopción de la Guía de Estilos oficial de Ruby y plantillas estandarizadas para Pull Requests y Commits.
5. **Shitsuke (Disciplina / Sostener):**
   - *Físico y Software:* Revisiones cruzadas periódicas entre compañeros (Code Reviews), respeto por las normas de higiene y auditorías internas continuas.

#### E. Layout (Distribución del Espacio de Trabajo)
- **Layout Físico (Puesto de Trabajo y Laboratorio):**
  - Diagrama de planta que ubique los 4 puestos de trabajo respetando distancias ergonómicas.
  - Distribución funcional: Área de codificación y desarrollo colaborativo, mesa central de reuniones y puesta en común (Scrum/Kanban), puesto de pruebas y servidor local, y área de descanso visual.
  - **Beneficios:** Favorece la comunicación directa entre desarrolladores, reduce fatiga visual y postural, elimina obstáculos en rutas de evacuación y optimiza la ventilación del equipamiento informático.
- **Layout Lógico (Arquitectura del Software):**
  - Diagrama de bloques que refleje la separación entre la interfaz de usuario por consola, la lógica de juego y la capa de persistencia (`Data`).

#### F. Sistema de Gestión Ambiental (ISO 14001) y Residuos (RAEE)
- **Política Ambiental:** Compromiso del equipo en optimizar el consumo energético y gestionar adecuadamente los residuos generados durante el ciclo de desarrollo.
- **Matriz de Aspectos e Impactos Ambientales:**
  - *Consumo de energía eléctrica (PCs/Servidores):* Agotamiento de recursos no renovables y emisiones indirectas de CO₂. *Medida de control:* Configuración de perfiles de suspensión, apagado total al finalizar la jornada y optimización algorítmica para reducir ciclos de CPU.
  - *Generación de RAEE (Residuos de Aparatos Eléctricos y Electrónicos):* Contaminación potencial por metales pesados (plomo, cadmio, estaño). *Medida de control:* Disposición diferenciada de componentes dañados en Puntos Verdes o centros de reciclaje autorizados (Ley 24.051 y normativas locales de RAEE).
- **Tipos de Residuos:**
  - *RAEE / Peligrosos:* Placas madre, fuentes de alimentación averiadas, cables cortados, periféricos rotos.
  - *Secos Reciclables:* Cajas de cartón de componentes, embalajes y papel de oficina.
  - *Basura Digital:* Archivos duplicados, logs infinitos y copias obsoletas que incrementan la demanda de almacenamiento en la nube.

#### G. Higiene y Seguridad Laboral / EPP
- **Marco Legal:** Ley Nacional N.° 19.587 de Higiene y Seguridad en el Trabajo, Decreto Reglamentario 351/79 y Resolución SRT 295/03 (específica de Ergonomía).
- **Riesgos Laborales en Computación y Medidas Preventivas:**
  - *Riesgo Ergonómico:* Dolores posturales, contracturas cervicales y síndrome del túnel carpiano por digitación prolongada. *Medidas:* Sillas regulables con soporte lumbar, teclados y mouses ergonómicos con pad de gel, y pausas activas obligatorias de 5 a 10 minutos cada una hora.
  - *Riesgo Visual:* Fatiga ocular y resequedad por exposición continua a pantallas (PVD). *Medidas:* Regla 20-20-20 (mirar a 6 metros durante 20 segundos cada 20 minutos), iluminación artificial homogénea (500 lux) y pantallas con filtro antirreflejo.
  - *Riesgo Eléctrico:* Posibilidad de cortocircuitos o electrocución por conexiones defectuosas. *Medidas:* Uso de canaletas ignífugas, disyuntores diferenciales, termomagnéticas y verificación de jabalina de puesta a tierra.
  - *Riesgo Psicosocial:* Estrés y síndrome de agotamiento (burnout) ante bloqueos lógicos. *Medidas:* Planificación realista de tareas y rotación de módulos complejos.
- **Elementos de Protección Personal (EPP):**
  - Lentes ergonómicos con filtro de luz azul.
  - Muñequeras ortopédicas de compresión elástica.
  - Calzado dieléctrico con suela aislante de goma y pulsera antiestática (para tareas de mantenimiento y ensamble de hardware).
- **Pictogramas y Señalética Requerida:**
  - Cartel de *"Riesgo Eléctrico"* sobre tableros y bastidores.
  - Cartel de señalización de *"Matafuegos Clase C"* (gases limpios o CO₂ para fuegos de origen eléctrico sin dañar los componentes electrónicos).
  - Vías de evacuación y botiquín de primeros auxilios señalizados según Norma IRAM 10.005.

#### H. Ciclo de Vida del Producto (ACV) y Puntos Críticos
Etapas del ciclo de vida del software:
1. **Concepción y Requerimientos:** Detección de la necesidad y delimitación del alcance.
2. **Diseño y Arquitectura:** Definición de clases, diagramas de flujo y patrones de diseño.
3. **Desarrollo y Ensamble:** Codificación en lenguaje Ruby. (*Punto Crítico:* riesgo de deuda técnica y acoplamiento excesivo en el módulo Tienda).
4. **Verificación y Pruebas (QA):** Validación mediante pruebas automáticas con RSpec. (*Punto Crítico:* regresiones funcionales que rompan mecánicas ya existentes).
5. **Distribución y Operación:** Publicación de releases en GitHub y ejecución por parte del usuario final.
6. **Mantenimiento y Fin de Vida:** Parches correctivos, migración o eliminación segura de datos sin dejar procesos huérfanos en servidores.

#### I. Matriz Legal
Tabla de cumplimiento normativo en Argentina:

| Norma / Ley | Denominación Oficial | Aplicación al Proyecto | Modo de Cumplimiento |
|---|---|---|---|
| **Ley 11.723** | Régimen Legal de la Propiedad Intelectual | Protección de la propiedad intelectual sobre el código fuente en Ruby y mecánicas del juego. | Licenciamiento formal (ej. Licencia MIT) y registro de autoría en el repositorio. |
| **Ley 25.326** | Protección de los Datos Personales (Habeas Data) | Regulación sobre perfiles de usuario, registros de juego y donaciones. | Almacenamiento seguro, principio de finalidad y no cesión de datos a terceros. |
| **Ley 19.587 y Res. SRT 295/03** | Higiene y Seguridad Laboral / Ergonomía | Condiciones físicas y ambientales en las estaciones de trabajo de los desarrolladores. | Puestos ergonómicos, pausas activas y verificación eléctrica periódica. |
| **Ley 25.675 y Ley 24.051** | Ley General del Ambiente / Residuos Peligrosos y RAEE | Tratamiento y disposición de los desechos electrónicos del equipo de desarrollo. | Reciclaje y entrega de rezagos electrónicos en puntos verdes habilitados. |
| **Ley 24.240** | Defensa del Consumidor | Transparencia ante los usuarios en sistemas de compras dentro del juego o donaciones. | Términos y condiciones claros, evitando publicidad o cobros engañosos. |

#### J. Diagrama de Gantt (Planificación Temporal)
Planificación del proyecto en 6 semanas de trabajo:

| Tarea / Etapa del Proyecto | Responsable Principal | Sem 1 | Sem 2 | Sem 3 | Sem 4 | Sem 5 | Sem 6 |
|---|---|:---:|:---:|:---:|:---:|:---:|:---:|
| 1. Definición de requerimientos y prototipo | Equipo completo | █ | | | | | |
| 2. Arquitectura de clases y POO en Ruby | Sebastián Zerpa | | █ | | | | |
| 3. Mecánicas de juego (Pesca e Inventario) | Maycol Alconz | | █ | █ | | | |
| 4. Desarrollo de Tienda y Refactorización | Ezequiel Lizasoain | | | █ | █ | | |
| 5. Suite de pruebas automatizadas (RSpec) | Sebastián Zerpa | | | | █ | █ | |
| 6. Implementación 5S y Plan de Mantenimiento | Enzo Luna | | | | | █ | |
| 7. Gestión ambiental, Layout y SySO | Maycol Alconz | | | | | █ | |
| 8. Informe técnico final y Presentación | Equipo completo | | | | | | █ |

#### K. Checklist de Avance Obligatorio
Registrar formalmente en el informe el checklist de las 12 etapas:
- [x] Definición y objetivos del prototipo
- [x] Selección de materiales y componentes
- [x] Diseño técnico o esquema funcional
- [x] Análisis del ciclo de vida del producto
- [x] Aplicación de principios de sostenibilidad
- [x] Aplicación de normas de seguridad e higiene
- [x] Uso de EPP durante el trabajo
- [x] Construcción y ensamblado
- [x] Pruebas de funcionamiento
- [x] Revisión de calidad (control final)
- [x] Redacción del informe técnico
- [x] Preparación de la presentación oral

#### L. Conclusiones del Grupo
Redactar una síntesis reflexiva destacando cómo la integración de normas de calidad (ISO 9001), gestión ambiental (ISO 14001, RAEE), ergonomía laboral (Ley 19.587) y metodologías ágiles/5S transformaron un simple script de pesca en Ruby en un producto de software profesional, confiable, sustentable y viable para su lanzamiento.

---

## 4. Estructura Final Recomendada para el Informe Técnico (Word de 3 a 5 Páginas)

Para confeccionar el archivo final definitivo en Microsoft Word respetando todas las pautas, se recomienda estructurar las secciones de la siguiente forma:

1. **PORTADA INSTITUCIONAL**  
   (Escuela, Curso, Especialidad, Asignatura, Título, Integrantes, Fecha).
2. **RESUMEN EJECUTIVO Y CHECKLIST DE SEGUIMIENTO**
3. **IDENTIDAD ORGANIZACIONAL Y DESCRIPCIÓN DEL PROTOTIPO**  
   - 3.1. Descripción General del Prototipo  
   - 3.2. Objetivos y Justificación del Diseño  
   - 3.3. Misión y Visión  
4. **RECURSOS, COMPONENTES Y COSTOS ESTIMADOS**  
   - 4.1. Materiales y Componentes (Hardware y Software)  
   - 4.2. Presupuesto y Estimación de Costos  
5. **GESTIÓN DE PROCESOS PRODUCTIVOS Y CALIDAD**  
   - 5.1. Ciclo PDCA aplicado a la Mejora Continua del Software  
   - 5.2. Sistema de Gestión de la Calidad (ISO 9001: Política, 5 Pilares, Pruebas RSpec)  
   - 5.3. Metodología 5 S en el Proyecto  
6. **PLAN DE MANTENIMIENTO TOTAL**  
   - 6.1. Mantenimiento Preventivo, Correctivo y Predictivo (Tabla Operativa)  
7. **DISTRIBUCIÓN Y ORGANIZACIÓN DEL ESPACIO (LAYOUT)**  
   - 7.1. Layout Físico de Estaciones de Desarrollo  
   - 7.2. Beneficios Productivos y Ergonómicos del Layout  
8. **HIGIENE, SEGURIDAD Y MEDIO AMBIENTE (HSE)**  
   - 8.1. Higiene y Seguridad Laboral (Riesgos informáticos, EPP y Señalética)  
   - 8.2. Sistema de Gestión Ambiental (ISO 14001 y Matriz de Aspectos)  
   - 8.3. Gestión de Residuos (RAEE y Consumo Racional)  
   - 8.4. Ciclo de Vida del Producto (ACV y Puntos Críticos)  
   - 8.5. Sostenibilidad (Triple Impacto: Económico, Social y Ambiental)  
9. **MARCO REGULATORIO (MATRIZ LEGAL)**  
10. **PLANIFICACIÓN TEMPORAL (DIAGRAMA DE GANTT)**  
11. **CONCLUSIONES DEL GRUPO**  

---

## 5. Estructura para la Presentación Digital (12 Diapositivas en Canva o PowerPoint)

La cátedra especifica un formato estricto de **12 diapositivas**, con conceptos breves, esquemas visuales claros y logos institucionales:

- **Diapositiva 1 - Portada:**  
  Nombre del proyecto (*Sistema de Pesca en Ruby*), integrantes (Sebastián Zerpa, Ezequiel Lizasoain, Enzo Luna, Maycol Alconz), curso (6.° Año Computación), Escuela Técnica N.° 12 y captura o esquema del prototipo.
- **Diapositiva 2 - Ciclo PDCA:**  
  Esquema del ciclo Planificar-Hacer-Verificar-Actuar aplicado a la calidad y resolución de fallas en mecánicas de juego.
- **Diapositiva 3 - Seguridad e Higiene:**  
  Riesgos en el puesto informático (ergonómicos y eléctricos), EPP utilizados (lentes filtro azul, pulseras antiestáticas) y señalética (matafuegos Clase C, riesgo eléctrico).
- **Diapositiva 4 - Ciclo de Vida del Producto:**  
  Diagrama de las 6 etapas del software e identificación de los puntos críticos (refactorización de la tienda y pruebas de regresión).
- **Diapositiva 5 - Gestión Ambiental (Residuos):**  
  Clasificación de residuos generados por el proyecto, tratamiento de RAEE (e-waste) y acciones para reducir el consumo eléctrico y papel.
- **Diapositiva 6 - Normas ISO 14001:**  
  Requisitos de la norma aplicados al desarrollo de software (política ambiental, eficiencia energética y servidores de bajo impacto).
- **Diapositiva 7 - Metodología 5 S:**  
  Aplicación de Seiri, Seiton, Seiso, Seiketsu y Shitsuke en puestos de trabajo físicos y en la organización del repositorio de código.
- **Diapositiva 8 - Mantenimiento Preventivo:**  
  Tabla resumen con tareas preventivas (RuboCop, actualización de gemas, backups), correctivas (issues) y predictivas (telemetría de memoria).
- **Diapositiva 9 - Normas ISO 9001 (Sistema de Calidad):**  
  Los 5 pilares de calidad en Ruby, framework de tests RSpec y control de versiones en Git para la satisfacción del usuario.
- **Diapositiva 10 - Sostenibilidad:**  
  Análisis del Triple Impacto: Social (colaboración comunitaria), Económico (modelo de donaciones/tienda) y Ambiental (código eficiente).
- **Diapositiva 11 - Layout:**  
  Esquema gráfico del layout del laboratorio de trabajo y justificación de los beneficios ergonómicos y productivos para el equipo.
- **Diapositiva 12 - Matriz Legal y Conclusiones:**  
  Tabla sintética de leyes (Ley 11.723, 25.326, 19.587, 24.240) y reflexión final sobre la integración técnica y de gestión.

---

## 6. Plan de Acción y Distribución de Tareas del Equipo

Para completar el trabajo de manera ágil entre los 4 integrantes:

1. **Sebastián Zerpa:**  
   - Confeccionar la Portada Institucional y maquetar el documento Word.  
   - Ajustar el Ciclo PDCA hacia el proceso técnico.  
   - Redactar los Objetivos de Calidad y KPIs de la norma ISO 9001.
2. **Ezequiel Lizasoain:**  
   - Redactar la Misión y Visión del proyecto.  
   - Desarrollar la Metodología 5 S aplicada al código y puesto de trabajo.  
   - Confeccionar la tabla de Materiales, Componentes y Costos Estimados.
3. **Enzo Luna:**  
   - Elaborar los esquemas del Layout Físico y Lógico.  
   - Diagramar el Ciclo de Vida del Producto (ACV) y sus puntos críticos.  
   - Diseñar el cronograma en el Diagrama de Gantt.
4. **Maycol Alconz:**  
   - Redactar la sección de Higiene y Seguridad Laboral, EPP y señalética.  
   - Desarrollar la norma ISO 14001 y la clasificación de Residuos (RAEE).  
   - Confeccionar la Matriz Legal completa.
5. **Conjunto (Todos):**  
   - Redactar las Conclusiones del Grupo.  
   - Diseñar las 12 diapositivas en Canva o PowerPoint y ensayar la presentación oral de 15 minutos asegurando la participación activa de los cuatro integrantes.
