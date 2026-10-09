# SECCIÓN 2: IDENTIDAD ORGANIZACIONAL, DESCRIPCIÓN DEL PROTOTIPO Y OBJETIVOS

---

## 1. Identidad Organizacional

El proyecto se enmarca bajo la figura organizativa de un estudio independiente de ingeniería de software denominado **AquaByte Development Studio**, conformado por los cuatro desarrolladores del equipo. La cultura corporativa del estudio se apoya en la excelencia técnica, la disciplina operativa y el compromiso ético con el usuario y el ambiente.

### Misión
> Diseñar, construir y mantener soluciones computacionales interactivas y videojuegos de simulación en lenguaje Ruby, aplicando metodologías rigurosas de ingeniería de software, arquitectura orientada a objetos desacoplada, control de calidad continuo y ergonomía en el trabajo, con el propósito de ofrecer a los usuarios una experiencia estable, formativa, fluida y de alto valor de entretenimiento.

### Visión
> Consolidarse como un equipo referente dentro de la Educación Técnico Profesional y la comunidad de software de código abierto en Argentina, demostrando que el desarrollo informático independiente puede articular de manera armónica la calidad industrial bajo normas internacionales (ISO 9001 e ISO 14001), la salud laboral de los desarrolladores y la sostenibilidad integral de triple impacto.

---

## 2. Descripción General del Prototipo

El prototipo desarrollado consiste en un **Simulador Interactivo de Pesca y Gestión Económica** implementado en lenguaje **Ruby (versión 3.x)** para su ejecución en entornos de consola interactiva y terminales compatibles con sistemas operativos POSIX y Windows. 

El sistema recrea la experiencia de un pescador deportivo que debe administrar sus recursos, seleccionar sus aparejos y cebos, interactuar con la fauna ictícola y comercializar sus capturas dentro de un mercado dinámico.

```
       +-------------------------------------------------------+
       |               SISTEMA DE PESCA EN RUBY               |
       +-------------------------------------------------------+
                                  |
         +------------------------+------------------------+
         |                                                 |
         v                                                 v
+------------------+                              +------------------+
| MECÁNICA DE PESCA|                              | ECONOMÍA Y TIENDA|
+------------------+                              +------------------+
| - Picada aleatoria                              | - Venta de peces
| - Evento con Timeout                            | - Compra de cebos
| - Peso y rareza                                 | - Mejora de caña
| - Desgaste de cebo                              | - Balance de saldo
+------------------+                              +------------------+
         |                                                 |
         +------------------------+------------------------+
                                  |
                                  v
                   +-----------------------------+
                   |  INVENTARIO Y PERSISTENCIA  |
                   |      (Carpeta /Data)        |
                   +-----------------------------+
```

### Características Técnicas del Prototipo:
1. **Paradigma y Arquitectura Modular:**
   Estructurado en un modelo de Programación Orientada a Objetos (POO) puro. Las responsabilidades del dominio se distribuyen en clases especializadas con bajo acoplamiento y alta cohesión:
   - `Jugador`: Administra el estado del usuario, nivel de experiencia, saldo monetario acumulado y contenedor de inventario.
   - `Pesca`: Modela la lógica del ecosistema de pesca, cálculo de probabilidades de pique según rareza, factores climáticos simulados y tiempos de reacción.
   - `Tienda`: Gestiona el catálogo de bienes, listas de precios de cebos, cañas de mayor precisión y la transacción comercial de compra/venta de capturas.
   - `Pez`: Modela los atributos biológicos y comerciales de la especie capturada (nombre, peso aleatorio en gramos, coeficiente de rareza y cotización de mercado).
   - `Objeto`: Clase base para insumos, consumibles y equipamiento auxiliar.
2. **Mecánica de Interacción Temporizada (Timing Event):**
   A diferencia de scripts secuenciales estáticos, el sistema implementa captura por eventos dinámicos controlados por el módulo `Timeout` de Ruby (`Timeout::timeout`). El usuario debe responder ante la notificación de "¡El pez mordió el anzuelo!" dentro de una ventana de tiempo aleatoria y crítica. El manejo controlado de excepciones (`Timeout::Error`) previene bloqueos de ejecución o caídas imprevistas del programa.
3. **Persistencia de Datos y Trazabilidad:**
   El progreso de la partida, el balance económico y el inventario del usuario se serializan y guardan de forma persistente en archivos de texto estructurados dentro del directorio local `/Data`. Se contemplan rutinas de validación para prevenir la corrupción de datos ante cierres inesperados.
4. **Entorno de Ejecución Ligero:**
   El software no requiere interfaces gráficas pesadas ni motores de renderizado con alto consumo de cómputo, lo que le permite funcionar de forma fluida en equipos con recursos limitados (PCs educativas o servidores headless), optimizando el ciclo de vida del hardware.

---

## 3. Objetivos y Justificación Técnica del Diseño

### Objetivo General
> Desarrollar y validar un prototipo funcional de software interactivo en Ruby que integre los estándares técnicos de la especialidad Computación con los lineamientos de la materia Gestión de los Procesos Productivos: control de calidad (ISO 9001), mejora continua (PDCA), orden y limpieza (5S), mantenimiento integral (TPM), layout ergonómico, gestión ambiental (ISO 14001, RAEE), seguridad laboral (Ley 19.587) y cumplimiento legal argentino.

### Objetivos Específicos
1. **Calidad y Fiabilidad del Software:**
   - Erradicar defectos en tiempo de ejecución en mecánicas críticas mediante un diseño orientado a objetos con interfaces claras.
   - Alcanzar y sostener una cobertura de pruebas automatizadas superior al **85%** utilizando el framework `RSpec`.
   - Garantizar cero advertencias de estilo y vulnerabilidades mediante auditoría estática con la gema `RuboCop`.
2. **Eficiencia y Sostenibilidad Computacional:**
   - Diseñar rutinas algorítmicas de baja complejidad temporal $\mathcal{O}(1)$ y $\mathcal{O}(n)$ en las transacciones de compra/venta e inventario, reduciendo la carga de CPU y la huella energética indirecta del hardware.
   - Establecer un procedimiento de serialización eficiente en la carpeta `/Data` que minimice las operaciones de entrada/salida (I/O) en disco.
3. **Mantenibilidad y Escalabilidad del Proceso:**
   - Documentar la arquitectura del software y estandarizar el repositorio de control de versiones con Git, facilitando la incorporación colaborativa de nuevos desarrolladores.
   - Diseñar un Plan de Mantenimiento Total que combine tareas calendarizadas preventivas, respuesta ágil a incidentes correctivos y monitoreo predictivo de degradación de recursos.
4. **Seguridad y Ergonomía del Entorno de Trabajo:**
   - Modelar una estación de trabajo que respete los límites ergonómicos de la Res. SRT 295/03, mitigando los riesgos de síndrome del túnel carpiano, fatiga visual postural y estrés térmico/eléctrico en el laboratorio.

### Justificación Técnica del Diseño
La elección de **Ruby** como lenguaje central se fundamenta en su expresividad sintáctica, su rigurosa implementación del paradigma orientado a objetos (donde todo elemento es un objeto) y su robusto ecosistema de gemas profesionales para aseguramiento de calidad (`RSpec` para pruebas unitarias/comportamiento y `RuboCop` para linteo). 

Históricamente, el proyecto experimentó dificultades de diseño: el acoplamiento excesivo en el módulo de la tienda y la ocurrencia de bugs críticos como la imposibilidad de equipar la caña de pescar generaban fricción técnica y desmotivación en el equipo (*"la tienda me sacó las ganas de codear"*). 

La justificación técnica de la refactorización actual radica en aplicar **patrones de diseño de software** (como Inyección de Dependencias y Principio de Responsabilidad Única - SOLID), transformando un código vulnerable en una solución mantenible, testeable y preparada para escalar comercialmente.
