# SECCIÓN 8: ANÁLISIS DE CICLO DE VIDA DEL PRODUCTO (ACV), PUNTOS CRÍTICOS Y SOSTENIBILIDAD

---

## 1. Mapeo de la Cadena de Valor y Ciclo de Vida del Producto Tecnológico

En concordancia con los apuntes de la cátedra (*"Actividad de Indagación: Mapeo de la Cadena de Valor de un Producto Tecnológico"* y *"Ciclo de Vida (Proyecto)"*), el Análisis de Ciclo de Vida (ACV) y el Mapeo de la Cadena de Valor evalúan exhaustivamente todas las fases por las que transita un producto técnico desde la extracción de materias primas hasta su descarte o reciclaje final.

Aun tratándose de un producto de software programado en Ruby, el sistema interactúa de manera indisociable con la infraestructura física de hardware (estaciones de trabajo, servidores, redes y componentes electrónicos). Por ello, el análisis articula tanto la dimensión física de los equipos como la lógica del código, cubriendo las **seis etapas del ciclo de vida**:

### Tabla 6A: Mapeo del Ciclo de Vida del Producto (Cadena de Valor Integral)

| Etapa del ciclo de vida | Actividades principales | Impactos ambientales / sociales | Aspectos de calidad, higiene y seguridad | Propuestas de mejora |
|---|---|---|---|---|
| **1. Extracción de materias primas** | Obtención de metales y materiales de los equipos que usamos: cobre, silicio, oro, estaño, plomo (baterías de las UPS) y plásticos.<br><br>Ruby y las herramientas son open source, por lo que no requieren extracción física directa. | Minería con contaminación de agua y suelo, alto consumo de energía y explotación laboral en la cadena global del hardware.<br><br>Es un impacto indirecto del proyecto, porque utilizamos equipos informáticos ya existentes. | No controlamos esta etapa directamente. Existen riesgos laborales severos en minería y escasa trazabilidad de origen de los materiales. | Reutilizar PCs existentes o reacondicionadas de la institución.<br><br>Priorizar la adquisición de equipos con certificaciones ambientales (Energy Star, EPEAT).<br><br>Desarrollar software liviano que no obligue al usuario a renovar su hardware. |
| **2. Fabricación de componentes** | **Hardware:** Terceros fabrican placas madre, unidades SSD, monitores IPS y cableado estructurado UTP Cat 6.<br><br>**Software:** Desarrollo de las clases del modelo (`Jugador`, `Pesca`, `Tienda`, `Pez`, `Objeto`), suite de pruebas en RSpec y uso de gems. | **Hardware:** Emisiones de gases de efecto invernadero y generación de residuos industriales peligrosos.<br><br>**Software:** Consumo eléctrico continuo de las PCs y de los minutos de cómputo de CI en GitHub Actions (centros de datos). | Riesgos ergonómicos (posturas forzadas, movimientos repetitivos) y fatiga visual por largas jornadas frente a pantallas.<br><br>Controles de calidad: Pruebas RSpec (cobertura 88,4%), linteo estático con RuboCop, normas ISO 9001 y revisiones cruzadas de código (*Code Reviews*). | Programación de algoritmos eficientes con baja complejidad temporal ($\mathcal{O}(1)$ y $\mathcal{O}(n)$).<br><br>Pausas activas y adecuación ergonómica según Res. SRT 295/03.<br><br>Apagar equipos al terminar la jornada y optimizar los minutos de ejecución del pipeline de CI. |
| **3. Ensamblado** | **Software:** Integración modular de las clases, persistencia transaccional en `/Data` y pipeline automatizado de CI.<br><br>**Físico:** Montaje del laboratorio escolar con 4 puestos informáticos, canalización de cables y conexión de UPS estabilizada. | Consumo energético de compilación, ejecución de builds y pruebas.<br><br>Residuos de embalaje de componentes de hardware (cajas de cartón, film de polietileno, telgopor) y recortes de cables UTP. | Riesgos eléctricos (contacto directo/indirecto) y de descargas electrostáticas (ESD).<br><br>Medidas: Uso de pulseras antiestáticas ESD, conexión a UPS y disponibilidad de matafuegos de $CO_2$ (Clase C).<br><br>Calidad: Batería de 28 pruebas automatizadas de integración y regresión en RSpec. | Cableado canalizado bajo zócalos ignífugos para despejar vías de paso.<br><br>Segregación en origen de residuos de embalaje (cartón y plásticos secos).<br><br>Integración Continua automatizada y capacitación obligatoria en seguridad eléctrica. |
| **4. Distribución** | Publicación digital de versiones estables en *GitHub Releases* y descarga directa por parte de los usuarios finales.<br><br>No requiere empaquetado físico, estuches plásticos ni fletes terrestres. | Consumo energético de servidores cloud de GitHub y de la transferencia de datos por la red.<br><br>Frente a la distribución de productos físicos o consolas dedicadas, se ahorra el 100% de embalajes materiales y la huella de transporte. | Auditoría estricta de seguridad en dependencias con `Bundler-Audit` para descartar CVEs.<br><br>Adopción de Licencia MIT abierta.<br><br>Cumplimiento de la Ley 25.326 de Protección de Datos Personales.<br><br>El riesgo físico del usuario en esta fase es prácticamente nulo. | Generación de paquetes ejecutables livianos.<br><br>Mantenimiento de un archivo `.gitignore` estricto para no subir archivos residuales, logs ni binarios basura al repositorio público.<br><br>Documentación técnica y manual de instalación claros en el `README.md`. |
| **5. Uso** | El usuario ejecuta el juego en su consola/terminal, realiza pescas con eventos temporizados de pique, gestiona su inventario y guarda la partida en `/Data`.<br><br>Mantenimiento post-lanzamiento: Recepción de issues y corrección ágil de errores. | Impacto energético sumamente bajo: Demanda menos del 2% de CPU y solo 25 MB de memoria RAM.<br><br>Funciona fluidamente en computadoras de más de 10 años, evitando recambios prematuros y mitigando la generación de basura electrónica.<br><br>Sin mecánicas predatorias de monetización (libre de *loot boxes*).<br><br>Riesgo social: Tiempo excesivo de exposición a pantallas. | Guardado transaccional atómico con copias de seguridad automáticas para evitar la corrupción de archivos en `/Data`.<br><br>Manejo seguro de excepciones temporizadas (`Timeout::Error`) sin caída brusca de la consola.<br><br>Recomendaciones en consola sobre pausas de descanso visual y postura corporal saludable. | Optimización continua del código en parches menores.<br><br>Incorporación de alertas programadas dentro del juego invitando al usuario a realizar pausas.<br><br>Distribución de actualizaciones diferenciales ultralivianas. |
| **6. Fin de vida útil** | Fin del ciclo de soporte de versiones antiguas, desinstalación del programa por el usuario, purga de ramas muertas y registros en servidores, y eventual baja de equipos informáticos escolares. | La acumulación de archivos y branches obsoletas en servidores cloud (*basura digital*) genera un consumo fantasma de electricidad.<br><br>Los rezagos electrónicos (RAEE) contienen sustancias ecotóxicas como plomo, cadmio y mercurio si se descartan en basurales a cielo abierto. | Desinstalación limpia y sanitización de registros de usuario sin dejar procesos huérfanos ni rastros personales (Ley 25.326).<br><br>Disposición física de rezagos de hardware en recipientes rotulados para RAEE, cumpliendo con la Ley Nacional 24.051 y la Ley CABA 2.807. | Protocolo de purga mensual en Git (`git fetch --prune`) y eliminación periódica de logs antiguos.<br><br>Entrega formal de hardware obsoleto en Puntos Verdes autorizados de CABA.<br><br>Reutilización de memorias RAM, discos y placas sanas como repuestos pedagógicos para años inferiores.<br><br>Mantenimiento del repositorio público como software libre educativo. |

---

## 2. Ciclo de Vida del Software (SDLC) y Puntos Críticos de Control

De forma complementaria al análisis integral de la cadena de valor, la ingeniería del producto de software analiza las fases técnicas del desarrollo (Software Development Life Cycle - SDLC), identificando los **puntos críticos de control** donde un defecto de diseño o codificación compromete la estabilidad del sistema:

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
