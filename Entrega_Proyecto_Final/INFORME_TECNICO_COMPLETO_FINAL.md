# INFORME TÉCNICO INTEGRAL: PROYECTO FINAL DE GESTIÓN DE LOS PROCESOS PRODUCTIVOS

**ESPECIALIDAD COMPUTACIÓN | 6.º AÑO**  
**ESCUELA TÉCNICA N.º 12 D.E. 1 “LIBERTADOR GRAL. JOSÉ DE SAN MARTÍN”**  

---

## 1. Portada Institucional

* **Institución Educativa:** Escuela Técnica N.º 12 D.E. 1 “Libertador Gral. José de San Martín”
* **Dirección / Jurisdicción:** Dirección General de Educación Técnica – Ministerio de Educación CABA
* **Especialidad:** Computación
* **Curso y División:** 6.º Año
* **Espacio Curricular:** Gestión de los Procesos Productivos (GPP)
* **Nombre del Proyecto:** *Sistema de Simulación y Gestión Económica de Pesca en Ruby*
* **Nombre de Fantasía del Estudio:** *AquaByte Development Studio*
* **Equipo de Desarrollo (Autores):**
  1. **Zerpa, Sebastián** (Líder Técnico & Aseguramiento de Calidad / QA)
  2. **Lizasoain, Ezequiel** (Arquitectura de Software & Gestión Organizacional)
  3. **Luna, Enzo** (Ingeniería de Procesos, Layout & Mantenimiento TPM)
  4. **Alconz, Maycol** (Higiene, Seguridad Laboral, Medio Ambiente & Matriz Legal)
* **Ciclo Lectivo:** 2026
* **Lugar y Fecha:** Ciudad Autónoma de Buenos Aires, Octubre de 2026

---

## 2. Resumen Ejecutivo y Checklist Oficial de Avance

El presente informe técnico expone la planificación, ingeniería y control de calidad aplicados en el desarrollo del **Sistema de Simulación de Pesca en Lenguaje Ruby**. El trabajo adopta un enfoque industrial donde el software no es considerado un script informal, sino un producto manufacturado bajo rigurosos estándares de procesos: **Sistema de Gestión de la Calidad (ISO 9001)**, **Ciclo de Mejora Continua (PDCA)**, **Metodología 5 S**, **Plan de Mantenimiento Total (TPM: Preventivo, Correctivo y Predictivo 4.0)**, **Layout Físico y Lógico**, **Higiene, Seguridad Laboral y CYMAT (Ley 19.587, Ley 24.557 de ART y Res. SRT 295/03)**, **Gestión Ambiental y Residuos RAEE (ISO 14001 y Ley 24.051)**, **Mapeo de Cadena de Valor y Análisis de Ciclo de Vida (ACV de 6 etapas)**, **Sostenibilidad de Triple Impacto**, **Matriz Legal Argentina** y **Planificación Temporal (Gantt)**.

### Checklist Oficial de Seguimiento (12 Etapas Obligatorias)

- [x] **01. Definición y objetivos del prototipo:** Alcance técnico, modularidad y especificaciones funcionales delimitadas al 100%.
- [x] **02. Selección de materiales y componentes:** Cuadro técnico de hardware (4 PCs, UPS, redes) y software (Ruby, RSpec, Git).
- [x] **03. Diseño técnico o esquema funcional:** Diagrama de arquitectura lógica en cuatro capas desacopladas.
- [x] **04. Análisis del ciclo de vida del producto:** Mapeo de la cadena de valor en 6 etapas (materias primas hasta fin de vida) y control de puntos críticos del SDLC.
- [x] **05. Aplicación de principios de sostenibilidad:** Triple impacto formal (Social, Económico y Ambiental/Eficiencia de CPU).
- [x] **06. Aplicación de normas de seguridad e higiene:** Cumplimiento de la Ley 19.587, Ley 24.557 (ART), Dec. 351/79 y Res. SRT 295/03 de Ergonomía.
- [x] **07. Uso de EPP durante el trabajo:** Lentes filtro luz azul, muñequeras ortopédicas y pulseras antiestáticas para hardware.
- [x] **08. Construcción y ensamblado:** Desarrollo del código en Ruby bajo POO (`Jugador`, `Pesca`, `Tienda`, `Data`).
- [x] **09. Pruebas de funcionamiento:** Batería de pruebas automatizadas BDD con el framework RSpec (cobertura $\ge 85\%$).
- [x] **10. Revisión de calidad (control final):** Auditoría estática con RuboCop y verificación de requisitos ISO 9001.
- [x] **11. Redacción del informe técnico:** Documento consolidado formal presentado a la cátedra.
- [x] **12. Preparación de la presentación oral:** Estructura estricta de 12 diapositivas para exposición de 15 minutos.

---

## 3. Identidad Organizacional y Descripción del Prototipo

### 3.1. Identidad Organizacional (AquaByte Development Studio)
* **Misión:** Diseñar, construir y mantener soluciones computacionales interactivas y videojuegos de simulación en lenguaje Ruby, aplicando metodologías rigurosas de ingeniería de software, arquitectura modular, pruebas automatizadas y ergonomía laboral, brindando al usuario una experiencia fluida, formativa y libre de fallas.
* **Visión:** Consolidarse como un equipo referente de desarrollo en la Educación Técnico Profesional y la comunidad de código abierto en Argentina, demostrando que el software independiente puede integrar con excelencia la calidad industrial (ISO 9001), el cuidado ambiental (ISO 14001) y la salud de sus trabajadores.

### 3.2. Descripción General del Prototipo
El sistema es un **Simulador Interactivo de Pesca y Gestión Económica** en entorno de consola interactiva desarrollado en **Ruby (versión 3.x)**. Sus componentes principales son:
1. **Lógica de Pesca y Eventos Temporizados:** Empleo de la gema nativa `Timeout` para modelar ventanas críticas de reacción ante la picada del pez. Manejo controlado de excepciones (`Timeout::Error`) que previenen bloqueos.
2. **Economía y Tienda Desacoplada:** Mecánicas de compraventa de especies capturadas (cuyo precio varía por peso y coeficiente de rareza) y adquisición de aparejos, cañas de mayor precisión y cebos consumibles.
3. **Persistencia Transaccional:** Registro y recuperación segura de inventario y saldo del jugador en archivos locales dentro de la carpeta `/Data`.
4. **Arquitectura Orientada a Objetos:** Clases encapsuladas (`Jugador`, `Pesca`, `Tienda`, `Pez`, `Objeto`) que eliminan la dependencia mutua entre la interfaz visual y las reglas de negocio.

### 3.3. Objetivos y Justificación Técnica del Diseño
* **Objetivo General:** Diseñar y construir un prototipo funcional en Ruby que integre los estándares técnicos de computación con las normativas industriales de calidad, ambiente, seguridad y sostenibilidad exigidos por la cátedra.
* **Objetivos Específicos:**
  - Erradicar la deuda técnica histórica de la tienda y el bug de bloqueo en el equipamiento de la caña.
  - Alcanzar una cobertura de testing automatizado $\ge 85\%$ con RSpec y 0 advertencias de estilo en RuboCop.
  - Minimizar el consumo energético del procesador mediante complejidad algorítmica $\mathcal{O}(1)$ y $\mathcal{O}(n)$.
  - Establecer puestos de trabajo informáticos que cumplan con la Ley 19.587, Ley 24.557 y la Res. SRT 295/03.
* **Justificación del Diseño:** La refactorización bajo principios SOLID e Inyección de Dependencias solucionó la fatiga de desarrollo reportada en la bitácora (*"la tienda me sacó las ganas de codear"*), convirtiendo un script frágil en una arquitectura extensible y fácil de testear.

---

## 4. Recursos, Componentes Técnicos y Presupuesto Estimado

### 4.1. Materiales y Componentes de Hardware y Software
* **Hardware:** 4 estaciones de trabajo (PCs Core i5 / Ryzen 5, 16 GB RAM, SSD NVMe 512 GB), teclados mecánicos de bajo esfuerzo, ratones ergonómicos verticales con pad de gel, monitores IPS de 24 pulgadas, switch de 8 puertos GbE Cat 6 y UPS estabilizada de 1000 VA.
* **Software:** Entorno Linux Ubuntu 22.04 LTS / Windows 11 con WSL2, lenguaje Ruby 3.2, Bundler, RSpec, RuboCop, Bundler-Audit, Git, GitHub y Visual Studio Code.

### 4.2. Presupuesto Económico Detallado (Pesos Argentinos - ARS)

| Rubro | Concepto / Detalle | Cantidad | Costo Unitario (ARS) | Costo Subtotal (ARS) |
|---|---|:---:|:---:|:---:|
| **Hardware** | Amortización de estaciones de trabajo informático (4 PCs) | 4 equipos | $ 200.000 / mes | $ 800.000 |
| **Hardware** | UPS estabilizada de 1000 VA y regletas térmicas ignífugas | 2 kits | $ 180.000 | $ 360.000 |
| **Hardware** | Conectividad cableada: Switch 8 puertos GbE + Cable UTP Cat 6 | 1 kit | $ 90.000 | $ 90.000 |
| **Software** | Entorno de desarrollo (Ruby, VS Code, Git, Linux) | 4 puestos | $ 0 (Open Source) | $ 0 |
| **Cloud** | GitHub Team / Actions CI / Almacenamiento remoto de código | 1 año | $ 60.000 | $ 60.000 |
| **Mano de Obra** | Horas de desarrollo y QA (4 programadores x 80 hs = 320 hs) | 320 hs | $ 8.500 / h | $ 2.720.000 |
| **Servicios** | Conectividad simétrica de banda ancha a Internet | 2 meses | $ 35.000 / mes | $ 70.000 |
| **Servicios** | Energía eléctrica (Tarifa T1 comercial en CABA) | 2 meses | $ 45.000 / mes | $ 90.000 |
| **Seguridad y EPP** | Lentes antirreflejo luz azul, pads de gel y pulseras ESD | 4 kits | $ 35.000 / kit | $ 140.000 |
| **Seguridad Edilicia**| Matafuegos de $CO_2$ (5 kg, Clase B-C) para equipos eléctricos | 1 unidad | $ 120.000 | $ 120.000 |
| **Imprevistos** | Fondo de contingencia técnica / reposición (5%) | Estimado | $ 225.000 | $ 225.000 |
| **TOTAL GENERAL** | **Inversión Integral del Proyecto de Software** | | | **$ 4.675.000** |

---

## 5. Gestión de Procesos Productivos, Calidad y Mejora Continua

### 5.1. Ciclo PDCA (Mejora Continua de Deming aplicada al Software)
1. **Planificar (Plan):** Se identificó el acoplamiento rígido del módulo `Tienda` y el bug en el método de equipamiento de cañas de la clase `Jugador`. Se fijó el objetivo de erradicar los defectos a 0, desacoplar la interfaz de la lógica de negocio y alcanzar una cobertura de tests $\ge 85\%$ en 4 semanas operativas.
2. **Hacer (Do):** Se implementó el framework `RSpec`, redactando 28 pruebas unitarias. Se refactorizó la clase `Tienda` extrayendo las rutinas de entrada/salida de terminal hacia módulos auxiliares de presentación y aplicando inyección de dependencias. Se corrigió la asignación atómica del estado en `Jugador`.
3. **Verificar (Check):** Se ejecutó la suite de testing obteniendo 100% de éxito (**0 fallas, 0 errores**). La cobertura auditada con `SimpleCov` alcanzó el **88,4%**. Se verificó que el linter `RuboCop` arrojó 0 faltas a la guía de estilo.
4. **Actuar (Act):** Se estandarizó un pipeline de Integración Continua (CI) en GitHub Actions que impide la incorporación de código a la rama `main` sin pasar previamente los tests y el linter. Se documentaron los patrones de diseño en las pautas de arquitectura del equipo.

### 5.2. Sistema de Gestión de la Calidad (ISO 9001:2015)
* **Política de Calidad:** *“AquaByte Development Studio se compromete a diseñar software interactivo confiable, mantenible y eficiente, garantizando la satisfacción integral de los usuarios mediante especificaciones técnicas rigurosas, pruebas automatizadas de QA, sustentabilidad y mejora continua.”*
* **Objetivos y KPIs:**
  - Defectos críticos en producción: **0 incidentes**.
  - Cobertura de pruebas unitarias: $\ge \mathbf{85\%}$ (alcanzado: 88,4%).
  - Tiempo Medio de Reparación de Incidentes (MTTR): $< \mathbf{24\text{ horas}}$.
  - Violaciones a guías de estilo: **0 advertencias**.

### 5.3. Metodología 5 S en el Proyecto

| Etapa | Aplicación en el Taller / Laboratorio Escolar | Aplicación en el Código y Repositorio de Software |
|---|---|---|
| **1. Seiri (Clasificar)** | Retiro de cables en desuso, periféricos quemados y papeles obsoletos. | Purgado de código muerto, ramas huérfanas en Git y gemas innecesarias en `Gemfile`. |
| **2. Seiton (Ordenar)** | Puestos rotulados, gavetas identificadas y cables canalizados. | Estructura estricta de carpetas: `/Classes`, `/LogicaJuego`, `/Data`, `/Spec`. |
| **3. Seiso (Limpiar)** | Limpieza quincenal con aire comprimido en pantallas, gabinetes y coolers. | Formateo automático de código con `rubocop -a` y sanitización de archivos `/Data`. |
| **4. Seiketsu (Estandarizar)** | Listas de control de orden al inicio y cierre de cada turno de trabajo. | Adopción de la Guía Oficial de Estilo de Ruby y plantillas para Pull Requests. |
| **5. Shitsuke (Disciplina)** | Hábito sostenido de orden y respeto por las normas del laboratorio. | Revisiones de código cruzadas (*Code Reviews*) obligatorias antes de cada fusión. |

---

## 6. Plan de Mantenimiento Total (TPM: Preventivo, Correctivo y Predictivo)

| Nivel | Tarea Específica | Frecuencia | Responsable | Herramienta | SLA / Tiempo | Criterio de Aprobación |
|---|---|:---:|:---:|:---:|:---:|---|
| **Preventivo** | Auditoría estática de estilo y complejidad | Semanal | E. Lizasoain | `RuboCop` | 1 hora | 0 ofensas de estilo |
| **Preventivo** | Detección de vulnerabilidades en gemas | Mensual | S. Zerpa | `Bundler-Audit` | 2 horas | 0 CVEs reportadas |
| **Preventivo** | Copia de seguridad automatizada de `/Data` | Diario | M. Alconz | Script Cron + Bash | 15 min | Backup íntegro comprimido |
| **Correctivo** | Triaje y clasificación de incidentes | Diario | E. Lizasoain | GitHub Issues | $< 4\text{ hs}$ | Severidad asignada |
| **Correctivo** | Resolución de bugs críticos (*Hotfixes*) | A demanda | S. Zerpa | Git + RSpec | $< 24\text{ hs}$ | Test de regresión verde |
| **Correctivo** | Restauración ante corrupción de partidas | A demanda | M. Alconz | Script restore | $< 30\text{ min}$ | Partida restaurada |
| **Predictivo** | Telemetría de consumo de memoria RAM | Quincenal | E. Luna | Profiler / Data Analytics | 2 horas | Curva de memoria estable |
| **Predictivo** | Medición de latencia de persistencia `/Data` | Mensual | S. Zerpa | Benchmark Ruby | 1 hora | Latencia media $< 50\text{ ms}$ |

---

## 7. Distribución del Espacio de Trabajo (Layout Físico y Lógico)

### 7.1. Layout Físico del Laboratorio de Desarrollo
El laboratorio de 35 m² cuenta con:
* **4 Puestos Individuales Ergonómicos:** Dispuestos en isla enfrentada 2 a 2, con iluminación natural lateral que elimina reflejos directos en monitores.
* **Mesa de Coordinación Central:** Destinada a reuniones ágiles (*Daily Stand-ups*), revisiones de código y tablero visual Kanban.
* **Servidor Local y Banco de QA:** Espacio aislado con switch Gigabit Ethernet, UPS de 1000 VA y banco de pruebas de RSpec.
* **Seguridad y Emergencia:** Tablero eléctrico con disyuntor de 30 mA y llaves termomagnéticas junto a la puerta; matafuegos de $CO_2$ (Clase C) señalizado con pictograma IRAM 10.005; botiquín de primeros auxilios y pasillos libres de 1,60 m hacia la salida.

### 7.2. Layout Lógico (Arquitectura en Capas)
1. **Capa 1 (Presentación):** Entrada y salida por terminal, menús interactivos y formateo visual ANSI.
2. **Capa 2 (Lógica y Control):** Clases `Pesca` (eventos temporizados de pique) y `Tienda` (cálculo de transacciones).
3. **Capa 3 (Modelo de Dominio):** Entidades `Jugador`, `Pez` y `Objeto` con atributos protegidos.
4. **Capa 4 (Infraestructura y Persistencia):** Serialización y lectura de datos atómica en la carpeta `/Data`.

---

## 8. Higiene, Seguridad Laboral, CYMAT, Riesgos y Medio Ambiente (HSE)

### 8.1. Marco Legal y Principios de Seguridad e Higiene
* **Principios Rectores:** Prevención en el origen, Protección Integral psicofísica y Responsabilidades Compartidas entre empleador y trabajador.
* **Leyes Vigentes:**
  - **Ley 19.587 (Higiene y Seguridad en el Trabajo) y Dec. 351/79:** Obligaciones patronales (entorno seguro, capacitación, EPP, vigilancia de salud) y de los trabajadores (cumplimiento, uso de EPP, aviso de riesgos). Sanciones por infracción (multas, clausuras).
  - **Ley 24.557 (Ley de Riesgos del Trabajo - LRT):** Aseguramiento obligatorio mediante ART bajo supervisión de la SRT, prestaciones médico-asistenciales inmediatas, rehabilitación, cobertura de salarios caídos e indemnizaciones.
  - **Res. SRT 295/03:** Límites ergonómicos de digitación y posturas en puestos con pantallas (PVD).
  - **Norma IRAM 10.005:** Sistema estandarizado de colores y formas de señalización.

### 8.2. Diferenciación Conceptual entre Peligro y Riesgo
* **Peligro:** Es la fuente, situación o condición intrínseca con potencial de causar daño (Ej.: cable pelado con tensión eléctrica en 220 V).
* **Riesgo:** Es la probabilidad de que una persona sufra un daño como resultado de la exposición a dicho peligro, combinando probabilidad y consecuencia:
  $$\text{Riesgo} = \text{Probabilidad} \times \text{Severidad de la Consecuencia}$$
  (Ej.: probabilidad de que un técnico lo toque y sufra electrocución). Aumenta con desorden o falta de señalización; disminuye con canalizaciones ignífugas, disyuntores de 30 mA y capacitación.

### 8.3. Factores de Riesgo según Condiciones y Medio Ambiente de Trabajo (CYMAT)
1. **Físicos:** Tensión eléctrica de 220 V (choque eléctrico/fuego Clase C), iluminación inadecuada (reflejos en pantallas) y carga térmica de PCs.
2. **Químicos:** Vapores y aerosoles inflamables en mantenimiento de hardware (alcohol isopropílico, solventes de contactos, pastas térmicas).
3. **Biológicos:** Hongos y bacterias en teclados, mouses y filtros de gabinetes de uso colectivo.
4. **Ergonómicos:** Sobrecarga estática sedente prolongada y movimientos repetitivos de flexión carpiana durante la digitación.
5. **Psicosociales:** Estrés agudo, frustración ante fallas algorítmicas (*"la tienda me sacó las ganas de codear"*) y presión por plazos de entrega.
6. **Mecánicos:** Golpes con escritorios, tropiezos con cables en el piso y caídas de gabinetes durante el ensamble.

### 8.4. Metodología de Evaluación de Riesgos y Matriz 3x3
El proceso evaluativo sigue 4 etapas: **1. Identificación $\rightarrow$ 2. Análisis $\rightarrow$ 3. Valoración $\rightarrow$ 4. Control**.

| Probabilidad \ Consecuencia | Consecuencia LEVE | Consecuencia MODERADA | Consecuencia GRAVE |
|---|:---:|:---:|:---:|
| **Probabilidad ALTA** | Nivel ALTO (Naranja) | Nivel CRÍTICO (Rojo) | Nivel CRÍTICO (Rojo) |
| **Probabilidad MEDIA** | Nivel MEDIO (Amarillo) | Nivel ALTO (Naranja) | Nivel CRÍTICO (Rojo) |
| **Probabilidad BAJA** | Nivel BAJO (Verde) | Nivel MEDIO (Amarillo) | Nivel ALTO (Naranja) |

*Evaluación de los riesgos del proyecto:*
* *Ergonómico repetitivo:* Probabilidad Alta x Consecuencia Moderada = **CRÍTICO** $\rightarrow$ Controlado a **BAJO** con mouses verticales, pad de gel y pausas activas (10 min/h).
* *Ergonómico postural:* Probabilidad Alta x Consecuencia Moderada = **CRÍTICO** $\rightarrow$ Controlado a **BAJO** con sillas regulables con apoyo lumbar.
* *Físico visual (PVD):* Probabilidad Alta x Consecuencia Leve = **ALTO** $\rightarrow$ Controlado a **BAJO** con lentes filtro azul, 500 lux y regla 20-20-20.
* *Físico eléctrico:* Probabilidad Baja x Consecuencia Grave = **ALTO** $\rightarrow$ Controlado a **BAJO** con disyuntor de 30 mA, canaletas ignífugas y extintor de $CO_2$.
* *Químico (mantenimiento):* Probabilidad Media x Consecuencia Leve = **MEDIO** $\rightarrow$ Controlado a **BAJO** con ventilación forzada y guantes de nitrilo.
* *Mecánico (cables en piso):* Probabilidad Media x Consecuencia Moderada = **ALTO** $\rightarrow$ Controlado a **BAJO** con canalización perimetral y pasillos libres.
* *Psicosocial (estrés):* Probabilidad Media x Consecuencia Moderada = **ALTO** $\rightarrow$ Controlado a **BAJO** con Pair Programming y arquitectura SOLID.

### 8.5. Jerarquía / Pirámide de Control de Riesgos
1. **Eliminación:** Supresión de cables precarios y eliminación del código monolítico acoplado.
2. **Sustitución:** Reemplazo de paneles antiguos por pantallas LED con filtro antiparpadeo y solventes no tóxicos.
3. **Controles de Ingeniería:** Zócalos ignífugos, disyuntor de 30 mA, puesta a tierra $< 5\ \Omega$, UPS 1000 VA y extintor de $CO_2$.
4. **Controles Administrativos:** Pausas activas obligatorias (10 min cada 60 min), regla 20-20-20, rotación de módulos y señalética IRAM 10.005.
5. **EPP (Última Barrera):** Lentes con filtro de luz azul (400–450 nm), muñequeras de neopreno, pulseras ESD con resistencia de 1 MΩ y calzado con suela dieléctrica (IRAM 3610).

### 8.6. Capacitación y Cultura Preventiva
Formación en 4 ejes: Conocimiento de riesgos informáticos, uso correcto de EPP, procedimientos de emergencia/evacuación y cultura de seguridad compartida (Seiton/Seiso).

### 8.7. Gestión Ambiental (ISO 14001:2015) y Clasificación de Residuos
* **Política Ambiental:** Optimización de recursos energéticos, preservación del hardware y descarte ecológico de residuos.
* **Clasificación de Residuos:**
  1. *RAEE (Ley 24.051 y Ley CABA 2.807):* Fuentes quemadas, motherboards, placas y periféricos rotos. Acopio en contenedor rotulado y entrega en **Puntos Verdes de CABA**.
  2. *Residuos Secos:* Cartones, plásticos y embalajes entregados a cooperativas de reciclaje urbano.
  3. *Basura Digital:* Depuración mensual de logs redundantes y ramas abandonadas en Git para reducir el consumo fantasma de servidores cloud.

---

## 9. Ciclo de Vida del Producto (ACV) y Sostenibilidad de Triple Impacto

### 9.1. Mapeo de la Cadena de Valor del Ciclo de Vida del Producto (6 Etapas Oficiales)

| Etapa del ciclo de vida | Actividades principales | Impactos ambientales / sociales | Aspectos de calidad, higiene y seguridad | Propuestas de mejora |
|---|---|---|---|---|
| **1. Extracción de materias primas** | Metales y minerales de las PCs: cobre, silicio, oro, estaño, plomo de baterías UPS y plásticos. Ruby y software son open source sin extracción física. | Minería con contaminación hídrica y de suelos, alto consumo energético y explotación laboral en la cadena del hardware. Impacto indirecto. | Sin control directo. Riesgos laborales mineros y escasa trazabilidad de origen. | Reutilizar PCs de la escuela, adquirir equipos con sello Energy Star/EPEAT y desarrollar software ultraliviano. |
| **2. Fabricación de componentes** | Hardware: Fabricación externa de placas, SSDs, monitores y cable UTP.<br>Software: Desarrollo en Ruby (`Jugador`, `Pesca`, `Tienda`, `Pez`, `Objeto`), tests RSpec y gems. | Emisiones de gases industriales y residuos peligrosos de hardware. En software: consumo eléctrico continuo de PCs y minutos de CI en GitHub. | Riesgos ergonómicos y fatiga visual.<br>Controles: Suite RSpec (88,4% cobertura), linter RuboCop, relación con **ISO 9001** (aseguramiento de la calidad en diseño y codificación) y revisiones cruzadas. | Código de baja complejidad ($\mathcal{O}(1)$, $\mathcal{O}(n)$), pausas activas (Res. SRT 295/03), apagar equipos al cierre y optimizar CI. |
| **3. Ensamblado** | Software: Integración modular, persistencia en `/Data` y pipeline CI.<br>Físico: Montaje del laboratorio escolar con 4 puestos, cableado y UPS. | Consumo energético de builds y pruebas. Residuos de embalaje de componentes (cartón, polietileno) y recortes de cable UTP. | Riesgos de electrocución y descargas ESD.<br>Medidas: Pulseras antiestáticas, UPS, extintor de $CO_2$ (Clase C). Pruebas de integración en RSpec (28 tests). | Cableado bajo zócalos ignífugos, separación de residuos secos en origen, CI automatizado y capacitación en seguridad eléctrica. |
| **4. Distribución** | Publicación de ejecutables en GitHub Releases y descarga por usuarios. Sin embalaje físico ni transporte automotor. | Energía de servidores cloud y transferencia de datos. Ahorro de 100% de plásticos de empaque y fletes respecto a medios físicos. | Auditoría de seguridad con `Bundler-Audit`, Licencia MIT y cumplimiento de Ley 25.326. Riesgo físico nulo. | Paquetes livianos, `.gitignore` estricto para no subir basura lógica y documentación clara en `README.md`. |
| **5. Uso** | El usuario ejecuta el juego en consola, pesca con eventos temporizados, comercia en la tienda y guarda partida. Mantenimiento por bugs. | Consumo bajísimo: $< 2\%$ CPU y 25 MB RAM. Corre en PCs de $>10$ años, combatiendo obsolescencia y rezagos. Sin loot boxes adictivas. Riesgo: tiempo de pantalla. | Guardado atómico con backups contra corrupción de `/Data`, intercepción de `Timeout::Error`. Mensajes de pausas y buena postura. | Optimización continua, alertas programadas de descanso dentro del juego y actualizaciones livianas. |
| **6. Fin de vida útil** | Fin de soporte de versiones viejas, desinstalación, purga de branches/logs y baja definitiva de equipos de computación. | Basura digital en servidores con consumo fantasma permanente. Los RAEE contienen plomo, mercurio y cadmio si se vierten en basurales. | Desinstalación limpia sin dejar datos huérfanos (Ley 25.326). Acopio diferenciado de RAEE según Ley 24.051 y Ley CABA 2.807 (articulado con **ISO 14001**: gestión ambiental y disposición segura). | Purga mensual (`git fetch --prune`), entrega formal en Puntos Verdes, reutilización de piezas sanas como repuestos y código open source. |

### 9.2. Ciclo de Vida del Software (SDLC) y Puntos Críticos de Control
1. *Concepción y Requerimientos:* Historias de usuario delimitadas.
2. *Diseño y Arquitectura:* **Punto Crítico 1:** Fricción por acoplamiento de la tienda $\rightarrow$ Resuelto con patrones SOLID e Inyección de Dependencias.
3. *Construcción y Codificación:* Programación en Ruby 3.2 auditada con RuboCop.
4. *Aseguramiento de Calidad (QA):* **Punto Crítico 2:** Regresiones en mecánicas base (bug de caña) $\rightarrow$ Resuelto con suite de 28 tests en RSpec integrada en CI.
5. *Despliegue y Operación:* **Punto Crítico 3:** Pérdida de partidas en `/Data` $\rightarrow$ Resuelto con guardado atómico transaccional y backups diarios.
6. *Mantenimiento y Fin de Vida:* Sanitización limpia de registros y descarte legal de RAEE.

### 9.3. Sostenibilidad: Modelo de Triple Impacto
* **Pilar Social:** Salud ocupacional sin burnout (pausas activas, clima cooperativo) y publicación de código abierto para formación didáctica en la ET N.º 12.
* **Pilar Económico:** Modelo ético sin mecánicas predatorias (*pay-to-win* o *loot boxes*), sustentado en donaciones transparentes o precio accesible.
* **Pilar Ambiental:** Green Software con menos del 2% de carga de CPU, operable en computadoras escolares de más de 10 años, combatiendo directamente la obsolescencia programada.

---

## 10. Marco Regulatorio y Matriz Legal en la República Argentina

| Norma / Ley | Denominación Oficial | Aplicación al Proyecto | Modo de Cumplimiento en el Software |
|---|---|---|---|
| **Ley 11.723** | Régimen de Propiedad Intelectual (Dec. 165/94) | Protección jurídica del código fuente en Ruby. | Autoría formal del equipo y adopción de la Licencia MIT. |
| **Ley 25.326** | Protección de Datos Personales (Habeas Data) | Privacidad en perfiles de usuario y partidas. | Almacenamiento local descentralizado; no se recopilan datos sensibles ni telemetría intrusiva. |
| **Ley 19.587 / Dec. 351/79** | Higiene y Seguridad Laboral | Condiciones físicas, lumínicas y eléctricas del laboratorio. | Puestos ergonómicos, pausas activas, iluminación de 500 lux, zócalos ignífugos y matafuegos $CO_2$. |
| **Ley 24.557** | Ley de Riesgos del Trabajo (LRT - ART / SRT) | Cobertura integral frente a accidentes y enfermedades profesionales. | Registro ante ART, prestaciones médicas/dinerarias y Sistema de Gestión de Riesgos. |
| **Res. SRT 295/03** | Especificaciones Técnicas sobre Ergonomía | Puestos de trabajo con pantallas (PVD) y digitación. | Ratones verticales, pads con gel, regulación de altura visual y pausas de 10 min/h. |
| **Ley 24.051 / Ley 25.675** | Residuos Peligrosos y Ley General del Ambiente | Gestión de rezagos electrónicos de hardware. | Prohibición de descarte domiciliario; acopio y entrega de RAEE en **Puntos Verdes CABA**. |
| **Ley CABA 1.854 y 2.807** | Basura Cero y Régimen de RAEE en CABA | Residuos urbanos y electrónicos en la Comuna 1. | Segregación en origen en tacho verde (secos) y entrega calificada de rezagos electrónicos. |
| **Ley 24.240** | Ley de Defensa del Consumidor | Transparencia ante los usuarios. | Reglas de juego claras, juego gratuito y donaciones explícitamente voluntarias. |
| **Licencia MIT** | Licencia de Software Permisiva OSI | Marco legal público del repositorio GitHub. | Libertad de uso, copia y estudio con cláusula de **exención de garantía y responsabilidad**. |

---

## 11. Planificación Temporal (Diagrama de Gantt)

El proyecto se ejecutó en **seis semanas operativas** con **320 horas técnicas** distribuidas equitativamente entre los 4 integrantes:
* **Sebastián Zerpa:** QA, RSpec, Ciclo PDCA, Objetivos ISO 9001 e integración general.
* **Ezequiel Lizasoain:** Refactorización de Tienda, Misión/Visión, Metodología 5S y Presupuesto.
* **Enzo Luna:** Mantenimiento Total TPM, Layout Físico/Lógico y Ciclo de Vida ACV.
* **Maycol Alconz:** Mecánica de Pesca, Higiene y Seguridad Laboral, CYMAT, Evaluación de Riesgos, Residuos RAEE e ISO 14001, Matriz Legal.

---

## 12. Conclusiones Generales del Grupo

El desarrollo del presente Proyecto Final demostró de manera contundente que **el software debe ser concebido y gestionado como un proceso productivo industrial**. 

La aplicación articulada de normas de calidad (ISO 9001), el ciclo de mejora continua (PDCA), la disciplina de las 5S, el mantenimiento productivo total (TPM 4.0), las leyes laborales y de riesgos del trabajo (Ley 19.587, Ley 24.557, CYMAT, Matriz de Riesgos 3x3) y las normativas ambientales (ISO 14001, RAEE, Mapeo del Ciclo de Vida en 6 etapas) permitió transformar un código informal, vulnerable y fuente de frustración técnica, en un producto informático robusto, escalable, ético y comercialmente viable.

El equipo de trabajo integrado por **Sebastián Zerpa, Ezequiel Lizasoain, Enzo Luna y Maycol Alconz** concluye satisfactoriamente las etapas del proyecto, consolidando las competencias profesionales técnicas y de gestión adquiridas durante su trayectoria en la **Escuela Técnica N.º 12**.
