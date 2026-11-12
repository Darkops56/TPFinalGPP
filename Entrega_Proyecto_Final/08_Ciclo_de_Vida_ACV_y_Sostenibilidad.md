# SECCIÓN 8: ANÁLISIS DE CICLO DE VIDA DEL PRODUCTO (ACV), PUNTOS CRÍTICOS Y SOSTENIBILIDAD

---

## 1. Mapeo de la Cadena de Valor y Ciclo de Vida del Producto Tecnológico

En concordancia con los apuntes de la cátedra (*"Actividad de Indagación: Mapeo de la Cadena de Valor de un Producto Tecnológico"* y *"Ciclo de Vida (Proyecto)"*), el Análisis de Ciclo de Vida (ACV) y el Mapeo de la Cadena de Valor evalúan exhaustivamente todas las fases por las que transita un producto técnico desde la extracción de materias primas hasta su descarte o reciclaje final.

Aun tratándose de un producto de software programado en Ruby, el sistema interactúa de manera indisociable con la infraestructura física de hardware (estaciones de trabajo, servidores, redes y componentes electrónicos). Por ello, el análisis articula tanto la dimensión física de los equipos como la lógica del código, cubriendo las **seis etapas del ciclo de vida** e integrando referencias a los sistemas de gestión de calidad (ISO 9001) y gestión ambiental (ISO 14001):

### Tabla 6A: Mapeo del Ciclo de Vida del Producto (Cadena de Valor Integral)

| Etapa del ciclo de vida | Actividades principales | Impactos ambientales / sociales | Aspectos de calidad, higiene y seguridad | Propuestas de mejora |
|---|---|---|---|---|
| **1. Extracción de materias primas** | Obtención de los metales y materiales de los equipos que usamos: cobre, silicio, oro, estaño, plomo (baterías de las UPS) y plásticos.<br><br>Ruby y las herramientas son open source, así que no requieren extracción física directa. | Minería con contaminación de agua y suelo, alto consumo de energía y explotación laboral en la cadena del hardware.<br><br>Es un impacto indirecto, porque usamos equipos ya existentes. | No controlamos esta etapa directamente. Hay riesgos laborales en minería y poca trazabilidad de materiales. | Reutilizar PCs existentes o reacondicionados de la escuela, preferir equipos con certificaciones ambientales (Energy Star, EPEAT) y hacer software liviano que no obligue a comprar hardware nuevo. |
| **2. Fabricación de componentes** | **Hardware:** Terceros fabrican placas madre, SSDs, monitores y cable UTP.<br><br>**Software:** Desarrollo de las clases (`Jugador`, `Pesca`, `Tienda`, `Pez`, `Objeto`), pruebas en RSpec y uso de gems. | **Hardware:** Emisiones y residuos peligrosos.<br><br>**Software:** Consumo eléctrico continuo de las PCs y de los minutos de CI en GitHub Actions (centros de datos). | Riesgos ergonómicos y visuales por horas de pantalla continuas.<br><br>Controles: RSpec (cobertura 88,4%), linter RuboCop, relación con **ISO 9001** (aseguramiento de la calidad en diseño y codificación) y revisiones de código cruzadas. | Código eficiente, pausas activas obligatorias, ergonomía según Res. SRT 295/03, apagar equipos al terminar la jornada y optimizar los minutos de CI. |
| **3. Ensamblado** | **Software:** Integración de las clases, persistencia en `/Data` y pipeline de CI.<br><br>**Físicamente:** Montaje del laboratorio con 4 puestos, cableado y conexión de UPS estabilizada. | Consumo energético de builds y pruebas.<br><br>Residuos de embalaje del hardware (cajas de cartón, polietileno) y recortes de cable UTP. | Riesgos eléctricos y de descarga estática (ESD): pulseras ESD, UPS y extintor de $CO_2$ Clase C.<br><br>Pruebas automatizadas de integración y regresión (28 tests). | Cableado canalizado en zócalos ignífugos, separación de residuos en origen, CI automatizado y capacitación obligatoria en seguridad eléctrica. |
| **4. Distribución** | Publicación en *GitHub Releases* y descarga directa por parte de los usuarios.<br><br>No hay embalaje físico ni transporte automotor. | Energía de servidores cloud y transferencia de datos por la red.<br><br>Frente al software en caja o soporte físico, ahorramos el 100% de embalajes y huella de transporte. | Revisión de dependencias con `Bundler-Audit`, licencia MIT permisiva y protección de datos (Ley 25.326).<br><br>El riesgo físico del usuario en esta etapa es nulo. | Paquete liviano, `.gitignore` estricto para no subir archivos basura al repositorio y documentación técnica clara en `README.md`. |
| **5. Uso** | El jugador ejecuta el juego en terminal, pesca con eventos temporizados, gestiona inventario y guarda la partida en `/Data`.<br><br>Mantenimiento: corrección ágil de errores reportados. | Impacto energético muy bajo: menos de 2% de CPU y 25 MB de RAM.<br><br>Funciona en PCs de más de 10 años, lo que evita recambios y residuos. Sin mecánicas predatorias (*loot boxes*). Riesgo social: tiempo de pantalla. | Guardado atómico con backups diarios para evitar partidas corruptas, y `Timeout::Error` manejado limpiamente sin caídas bruscas.<br><br>Recomendación de pausas y buena postura en consola. | Seguir optimizando algoritmos, sumar avisos de descanso en el juego y hacer actualizaciones livianas. |
| **6. Fin de vida útil** | Fin del soporte de versiones antiguas, desinstalación, purga de ramas y logs, y eventual baja de equipos informáticos escolares. | Basura digital que ocupa servidores cloud (consumo fantasma de energía).<br><br>Los RAEE contienen plomo, cadmio y mercurio si se descartan inadecuadamente. | Desinstalación limpia, sin dejar datos huérfanos ni procesos residuales.<br><br>Caja rotulada para RAEE según Ley 24.051 y Ley CABA 2.807 (articulada con **ISO 14001**: gestión ambiental y disposición segura de residuos). | Purga mensual de repositorios (`git fetch --prune`), entrega en Puntos Verdes, reutilización de piezas como repuestos pedagógicos y dejar el código abierto para que siga siendo útil. |

---

## 2. Ciclo de Vida del Software (SDLC) y Puntos Críticos de Control

De forma complementaria al análisis integral de la cadena de valor, la ingeniería del producto analiza las fases técnicas del desarrollo de software (Software Development Life Cycle - SDLC), identificando los **puntos críticos de control** donde un fallo de diseño o implementación compromete la calidad global del sistema:

```
+-----------------------------------------------------------------------------+
|                     CICLO DE VIDA DEL PRODUCTO SOFTWARE                     |
+-----------------------------------------------------------------------------+
  |
  +-> 1. CONCEPCIÓN Y ANÁLISIS DE REQUERIMIENTOS
  |      [Delimitación del alcance, mecánicas de pesca y economía]
  |
  +-> 2. DISEÑO Y ARQUITECTURA TÉCNICA
  |      [Estructura de clases POO, bajo acoplamiento y modularidad]
  |      *** PUNTO CRÍTICO 1: Riesgo de diseño monolítico en Tienda ***
  |
  +-> 3. CONSTRUCCIÓN Y CODIFICACIÓN EN RUBY
  |      [Escritura de código en /Classes y /LogicaJuego bajo Ruby Style Guide]
  |
  +-> 4. ASEGURAMIENTO DE CALIDAD Y TESTING (QA)
  |      [Pruebas unitarias automatizadas con RSpec y linteo con RuboCop]
  |      *** PUNTO CRÍTICO 2: Regresiones funcionales (Bug de la caña) ***
  |
  +-> 5. DISTRIBUCIÓN, DESPLIEGUE Y OPERACIÓN
  |      [Versionado en Git, publicación de releases y ejecución por usuarios]
  |      *** PUNTO CRÍTICO 3: Corrupción de persistencia en /Data ***
  |
  +-> 6. MANTENIMIENTO, EVOLUCIÓN Y RETIRO (FIN DE VIDA)
         [Parches de seguridad, optimización y desmantelamiento limpio de datos]
```

### Tabla 6B: Descripción de Fases y Puntos Críticos del SDLC

| Fase del SDLC | Actividades Principales Desarrolladas | Punto Crítico de Control Identificado | Mecanismo de Control y Mitigación Aplicado |
|---|---|---|---|
| **1. Concepción y Requerimientos** | Definición de especificaciones funcionales (probabilidad de pique, especies, inventario). | Requerimientos ambiguos que causen retrabajo continuo. | Validación de historias de usuario y matriz de alcance con la cátedra. |
| **2. Diseño y Arquitectura** | Definición de clases (`Jugador`, `Pesca`, `Tienda`, etc.) y patrones de diseño. | **Punto Crítico 1:** Alta fricción por acoplamiento de responsabilidades (falla histórica de la tienda). | Refactorización temprana aplicando principios SOLID e Inyección de Dependencias. |
| **3. Construcción y Codificación** | Programación en Ruby 3.x, manipulación de streams y serialización. | Generación de deuda técnica y código espagueti. | Control diario con linters estáticos (`RuboCop`) y pautas unificadas de commit. |
| **4. Aseguramiento de Calidad** | Batería de pruebas funcionales y de límites con RSpec. | **Punto Crítico 2:** Regresiones donde modificaciones nuevas rompen mecánicas ya validadas (ej. equipar caña). | Ejecución obligatoria de la suite de pruebas unitarias en el pipeline de Integración Continua (CI). |
| **5. Despliegue y Operación** | Lanzamiento de versiones ejecutables y distribución a usuarios. | **Punto Crítico 3:** Bloqueos en ejecución o partidas corruptas en `/Data`. | Rutinas transaccionales atómicas de guardado y backups automatizados. |
| **6. Fin de Vida y Retiro** | Descontinuación de soporte y migración tecnológica. | Procesos residuales huérfanos o almacenamiento innecesario (basura digital). | Script de desinstalación limpia y sanitización de registros personales (Ley 25.326). |

---

## 3. Sostenibilidad: Modelo de Triple Impacto

Conforme al apunte *“Sostenibilidad: El Camino Hacia un Futuro Equilibrado”*, una organización moderna debe satisfacer sus demandas operativas presentes sin comprometer los recursos y oportunidades de las generaciones futuras, equilibrando armónicamente tres dimensiones fundamentales:

```
                                 [ SOSTENIBILIDAD ]
                                         |
         +-------------------------------+-------------------------------+
         |                               |                               |
         v                               v                               v
+------------------+            +------------------+            +------------------+
|   PILAR SOCIAL   |            | PILAR ECONÓMICO  |            | PILAR AMBIENTAL  |
+------------------+            +------------------+            +------------------+
| - Salud laboral  |            | - Viabilidad ARS |            | - Código liviano |
| - Pausas activas |            | - Monetización   |            | - Ahorro de CPU  |
| - Código abierto |            |   ética          |            | - Anti-obsolec.  |
| - Trabajo en     |            | - Financiación   |            | - Gestión RAEE   |
|   equipo sano    |            |   transparente   |            |   responsable    |
+------------------+            +------------------+            +------------------+
```

### A. Pilar Social: Viabilidad del Talento Humano y Comunidad
* **Salud Ocupacional y Clima Laboral:**  
  La sostenibilidad social comienza por el cuidado de los propios desarrolladores. Históricamente, la frustración técnica generó desaliento individual (*"me sacó las ganas de codear"*). Al redistribuir las tareas equitativamente entre los cuatro integrantes e implementar protocolos de ergonomía y pausas activas, se erradicó el riesgo de burnout.
* **Aporte a la Comunidad y Código Abierto:**  
  El proyecto adopta un modelo abierto y transparente. El código fuente es compartido con la comunidad educativa como material didáctico para futuros estudiantes de la especialidad Computación de la Escuela Técnica N.º 12, promoviendo la inclusión digital y la transferencia tecnológica sin barreras arancelarias.

### B. Pilar Económico: Viabilidad Financiera y Retorno Responsable
* **Monetización Ética:**  
  A diferencia de las prácticas predatorias comunes en la industria del videojuego (como *loot boxes* o sistemas *pay-to-win* que inducen ludopatía digital), el proyecto promueve un esquema económico ético basado en donaciones voluntarias transparentes (vía *GitHub Sponsors* o plataformas equivalentes) o venta directa a precio accesible para el soporte del desarrollo.
* **Autosustentabilidad Operativa:**  
  El presupuesto detallado (Sección 3) demuestra que con costos operativos optimizados ($ 70.000 ARS en conectividad y $ 90.000 ARS en electricidad), el estudio puede sostener el mantenimiento del producto de forma autofinanciada sin comprometer recursos personales críticos de los desarrolladores.

### C. Pilar Ambiental: Eficiencia Computacional y Lucha contra la Obsolescencia
* **Optimización Algorítmica y Eficiencia Energética:**  
  El software mal programado obliga al procesador a ejecutar bucles innecesarios, disparando el consumo energético de la red eléctrica. Al optimizar las rutinas de cálculo de pesca e inventario a complejidades mínimas $\mathcal{O}(1)$ y $\mathcal{O}(n)$, el software requiere menos del **2% de carga de CPU** durante su ejecución.
* **Extensión de la Vida Útil del Hardware:**  
  El diseño liviano para terminal permite que el juego corra con fluidez en computadoras de más de 10 años de antigüedad con procesadores modestos. Esto combate de forma directa la **obsolescencia programada**, posponiendo el reemplazo prematuro de computadoras y reduciendo la tasa de generación de residuos electrónicos (RAEE).
