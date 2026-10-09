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

El presente informe técnico expone la planificación, ingeniería y control de calidad aplicados en el desarrollo del **Sistema de Simulación de Pesca en Lenguaje Ruby**. El trabajo adopta un enfoque industrial donde el software no es considerado un script informal, sino un producto manufacturado bajo rigurosos estándares de procesos: **Sistema de Gestión de la Calidad (ISO 9001)**, **Ciclo de Mejora Continua (PDCA)**, **Metodología 5 S**, **Plan de Mantenimiento Total (TPM: Preventivo, Correctivo y Predictivo 4.0)**, **Layout Físico y Lógico**, **Higiene, Seguridad Laboral y Ergonomía (Ley 19.587 y Res. SRT 295/03)**, **Gestión Ambiental y Residuos RAEE (ISO 14001 y Ley 24.051)**, **Análisis de Ciclo de Vida (ACV)**, **Sostenibilidad de Triple Impacto**, **Matriz Legal Argentina** y **Planificación Temporal (Gantt)**.

### Checklist Oficial de Seguimiento (12 Etapas Obligatorias)

- [x] **01. Definición y objetivos del prototipo:** Alcance técnico, modularidad y especificaciones funcionales delimitadas al 100%.
- [x] **02. Selección de materiales y componentes:** Cuadro técnico de hardware (4 PCs, UPS, redes) y software (Ruby, RSpec, Git).
- [x] **03. Diseño técnico o esquema funcional:** Diagrama de arquitectura lógica en cuatro capas desacopladas.
- [x] **04. Análisis del ciclo de vida del producto:** Seis etapas modeladas identificando tres puntos críticos de control.
- [x] **05. Aplicación de principios de sostenibilidad:** Triple impacto formal (Social, Económico y Ambiental/Eficiencia de CPU).
- [x] **06. Aplicación de normas de seguridad e higiene:** Cumplimiento de la Ley 19.587, Dec. 351/79 y Res. SRT 295/03 de Ergonomía.
- [x] **07. Uso de EPP durante el trabajo:** Lentes filtro luz azul, muñequeras ortopédicas y pulseras antiestáticas para hardware.
- [x] **08. Construcción y ensamblado:** Desarrollo del código en Ruby bajo POO (`Jugador`, `Pesca`, `Tienda`, `Data`).
- [x] **09. Pruebas de funcionamiento:** Batería de pruebas automatizadas BDD con el framework RSpec (cobertura $\ge 85\%$).
- [x] **10. Revisión de calidad (control final):** Auditoría estática con RuboCop y verificación de requisitos ISO 9001.
- [x] **11. Redacción del informe técnico:** Documento consolidado formal de 3 a 5+ páginas presentado a la cátedra.
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
  - Establecer puestos de trabajo informáticos que cumplan con los límites de la Res. SRT 295/03.
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

*Punto de Equilibrio:* Comercializando el software de forma independiente a un valor de $ 5.000 ARS por copia, el retorno de inversión se alcanza comercializando 935 licencias, validando la factibilidad comercial del proyecto.

---

## 5. Gestión de Procesos Productivos, Calidad y Mejora Continua

### 5.1. Ciclo PDCA (Mejora Continua de Deming aplicada al Software)
1. **Planificar (Plan):**  
   Se identificó el acoplamiento rígido del módulo `Tienda` y el bug en el método de equipamiento de cañas de la clase `Jugador`. Se fijó el objetivo de erradicar los defectos a 0, desacoplar la interfaz de la lógica de negocio y alcanzar una cobertura de tests $\ge 85\%$ en 4 semanas operativas.
2. **Hacer (Do):**  
   Se implementó el framework `RSpec`, redactando 28 pruebas unitarias. Se refactorizó la clase `Tienda` extrayendo las rutinas de entrada/salida de terminal hacia módulos auxiliares de presentación y aplicando inyección de dependencias. Se corrigió la asignación atómica del estado en `Jugador`.
3. **Verificar (Check):**  
   Se ejecutó la suite de testing obteniendo 100% de éxito (**0 fallas, 0 errores**). La cobertura auditada con `SimpleCov` alcanzó el **88,4%**. Se verificó que el linter `RuboCop` arrojó 0 faltas a la guía de estilo.
4. **Actuar (Act):**  
   Se estandarizó un pipeline de Integración Continua (CI) en GitHub Actions que impide la incorporación de código a la rama `main` sin pasar previamente los tests y el linter. Se documentaron los patrones de diseño en las pautas de arquitectura del equipo.

### 5.2. Sistema de Gestión de la Calidad (ISO 9001:2015)
* **Política de Calidad:** *“AquaByte Development Studio se compromete a diseñar software interactivo confiable, mantenible y eficiente, garantizando la satisfacción integral de los usuarios mediante especificaciones técnicas rigurosas, pruebas automatizadas de QA, sustentabilidad y mejora continua.”*
* **Objetivos y KPIs:**
  - Defectos críticos en producción: **0 incidentes**.
  - Cobertura de pruebas unitarias: $\ge \mathbf{85\%}$ (alcanzado: 88,4%).
  - Tiempo Medio de Reparación de Incidentes (MTTR): $< \mathbf{24\text{ horas}}$.
  - Violaciones a guías de estilo: **0 advertencias**.
* **Los 5 Pilares de Calidad en Ruby:**
  1. *Gestión de Riesgos:* Control preventivo de timeouts de pesca y validación estricta de inventario.
  2. *Control Operacional:* Modularidad estricta en clases (`Jugador`, `Pesca`, `Tienda`, `Pez`, `Objeto`).
  3. *Información Documentada:* Trazabilidad mediante Git, commits atómicos y manual técnico README.
  4. *Evaluación del Desempeño:* Batería de pruebas automatizadas con RSpec.
  5. *Mejora Continua:* Code reviews cruzados entre pares para detección temprana de deuda técnica.

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

Basándonos en la guía de Mantenimiento para la Industria 4.0, se implementó un plan estructurado en tres niveles tácticos:

### Tabla de Plan Operativo de Mantenimiento

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

## 8. Higiene, Seguridad, Medio Ambiente y Residuos (HSE)

### 8.1. Higiene y Seguridad Laboral (Ley 19.587 y Res. SRT 295/03)
* **Riesgo Ergonómico (Túnel Carpiano):** Mitigado con ratones ergonómicos verticales con almohadillas de gel, teclados de bajo esfuerzo y pausas activas obligatorias (10 minutos de estiramiento por cada 60 minutos de trabajo continuo).
* **Riesgo Visual (Pantallas PVD):** Iluminación homogénea a 500 lux, paneles mate antirreflejo y regla 20-20-20.
* **Riesgo Eléctrico:** Cableado canalizado en zócalos ignífugos, disyuntor diferencial de 30 mA, puesta a tierra certificada y matafuegos de $CO_2$ para no dañar componentes informáticos.
* **EPP Informáticos:** Lentes con filtro de luz azul, muñequeras ortopédicas y pulseras antiestáticas para el ensamble de PCs.

### 8.2. Gestión Ambiental (ISO 14001:2015) y Clasificación de Residuos
* **Política Ambiental:** Compromiso de uso racional de la energía y disposición responsable de desechos electrónicos.
* **Aspectos e Impactos:** Control del consumo energético de PCs (perfiles eco, apagado total al cierre) y reducción de la huella térmica.
* **Clasificación de Residuos:**
  1. *RAEE (Ley 24.051):* Placas quemadas, fuentes y cables dañados; segregados en cajas plásticas y entregados a **Puntos Verdes de CABA**.
  2. *Residuos Secos:* Cartones y embalajes de componentes entregados a cooperativas de reciclaje.
  3. *Basura Digital:* Depuración mensual de logs redundantes y ramas abandonadas en servidores para ahorrar almacenamiento cloud.

---

## 9. Ciclo de Vida del Software (ACV) y Sostenibilidad de Triple Impacto

### 9.1. Fases del ACV y Puntos Críticos
1. *Concepción y Requerimientos:* Delimitación de historias de usuario.
2. *Diseño y Arquitectura:* **Punto Crítico 1:** Fricción por acoplamiento de la tienda $\rightarrow$ Resuelto con patrones SOLID.
3. *Construcción y Codificación:* Programación en Ruby bajo la guía de estilo.
4. *Aseguramiento de Calidad (QA):* **Punto Crítico 2:** Regresiones en mecánicas base (bug de caña) $\rightarrow$ Resuelto con suite de RSpec en CI.
5. *Despliegue y Operación:* **Punto Crítico 3:** Pérdida de partidas en `/Data` $\rightarrow$ Resuelto con guardado atómico y backups diarios.
6. *Mantenimiento y Fin de Vida:* Sanitización limpia de datos y procesos.

### 9.2. Sostenibilidad: Modelo de Triple Impacto
* **Pilar Social:** Cuidado de la salud laboral del equipo (ergonomía y clima cooperativo sin burnout) y liberación del código como software libre para beneficio educativo de la ET N.º 12.
* **Pilar Económico:** Modelo ético sin mecánicas adictivas de azar (*pay-to-win*), basado en financiamiento sustentable y transparente.
* **Pilar Ambiental:** Código ultraliviano con menos del 2% de uso de CPU, operable en hardware de más de 10 años, combatiendo la obsolescencia programada.

---

## 10. Marco Regulatorio y Matriz Legal en la República Argentina

| Norma Legal | Denominación Oficial | Aplicación al Proyecto | Modo de Cumplimiento en el Software |
|---|---|---|---|
| **Ley 11.723** | Régimen Legal de la Propiedad Intelectual | Protección jurídica del código fuente en Ruby. | Autoría formal del equipo y adopción de la Licencia de Código Abierto MIT. |
| **Ley 25.326** | Ley de Protección de Datos Personales | Privacidad en perfiles de usuario y partidas. | Almacenamiento local descentralizado; no se recopilan datos sensibles ni telemetría. |
| **Ley 19.587 / Res. 295/03** | Higiene y Seguridad Laboral / Ergonomía | Condiciones psicofísicas en el laboratorio. | Puestos ergonómicos, pausas activas, iluminación de 500 lux y canaletas ignífugas. |
| **Ley 24.051 / Ley 25.675** | Residuos Peligrosos y Ley General del Ambiente | Gestión de rezagos electrónicos de hardware. | Prohibición de descarte domiciliario; acopio y entrega de RAEE en Puntos Verdes CABA. |
| **Ley 24.240** | Ley de Defensa del Consumidor | Transparencia ante los usuarios. | Reglas de juego claras, juego gratuito y donaciones explícitamente voluntarias. |
| **Licencia MIT** | Licencia de Software Permisiva | Términos de uso público del repositorio. | Cláusula de exención de garantía y libertad de modificación sin fines maliciosos. |

---

## 11. Planificación Temporal (Diagrama de Gantt)

El proyecto se desarrolló en **seis semanas de trabajo**, acumulando **320 horas técnicas de ingeniería** distribuidas entre los cuatro integrantes:

```
+----------------------------------------------------+----+----+----+----+----+----+
| Tarea / Actividad del Proyecto                     | S1 | S2 | S3 | S4 | S5 | S6 |
+----------------------------------------------------+----+----+----+----+----+----+
| 1. Requerimientos y Definición del Prototipo       | ██ |    |    |    |    |    |
| 2. Arquitectura de Clases y POO en Ruby            |    | ██ |    |    |    |    |
| 3. Mecánica de Pesca, Timing Event e Inventario    |    | ██ | ██ |    |    |    |
| 4. Desarrollo de Tienda y Refactorización SOLID    |    |    | ██ | ██ |    |    |
| 5. Suite de Pruebas Automatizadas con RSpec (QA)   |    |    |    | ██ | ██ |    |
| 6. Implementación 5S y Plan de Mantenimiento (TPM) |    |    |    |    | ██ |    |
| 7. Gestión Ambiental, Layout Físico y SySO (HSE)   |    |    |    |    | ██ |    |
| 8. Informe Técnico Final y Presentación (12 Slides)|    |    |    |    |    | ██ |
+----------------------------------------------------+----+----+----+----+----+----+
```

* **Sebastián Zerpa:** QA, RSpec, Ciclo PDCA, Objetivos ISO 9001 e integración general.
* **Ezequiel Lizasoain:** Refactorización de Tienda, Misión/Visión, Metodología 5S y Presupuesto.
* **Enzo Luna:** Mantenimiento Total TPM, Layout Físico/Lógico y Ciclo de Vida ACV.
* **Maycol Alconz:** Mecánica de Pesca, Higiene y Seguridad Laboral, Residuos RAEE e ISO 14001, Matriz Legal.

---

## 12. Conclusiones Generales del Grupo

El desarrollo del presente Proyecto Final demostró de manera contundente que **el software debe ser concebido y gestionado como un proceso productivo industrial**. 

La aplicación articulada de normas de calidad (ISO 9001), el ciclo de mejora continua (PDCA), la disciplina de las 5S, el mantenimiento productivo total (TPM) y la adecuación a las leyes laborales (Ley 19.587) y ambientales (ISO 14001, RAEE) permitió transformar un código informal, vulnerable y fuente de fricción técnica, en un producto informático robusto, escalable, ético y comercialmente viable.

El equipo de trabajo integrado por **Sebastián Zerpa, Ezequiel Lizasoain, Enzo Luna y Maycol Alconz** concluye satisfactoriamente las etapas del proyecto, consolidando las competencias profesionales técnicas y de gestión adquiridas durante su trayectoria en la **Escuela Técnica N.º 12**.
