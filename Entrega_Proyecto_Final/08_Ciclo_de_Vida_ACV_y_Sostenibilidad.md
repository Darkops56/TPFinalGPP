# SECCIÓN 8: ANÁLISIS DE CICLO DE VIDA DEL SOFTWARE (ACV), PUNTOS CRÍTICOS Y SOSTENIBILIDAD

---

## 1. Ciclo de Vida del Software (ACV)

En la ingeniería de procesos productivos, el Análisis de Ciclo de Vida (ACV) evalúa todas las etapas por las que transita un producto desde su concepción inicial hasta su retiro definitivo del servicio. 

Para nuestro prototipo de simulación en Ruby, el ciclo se estructuró en **seis fases interconectadas**, identificando los puntos críticos de control donde un fallo puede comprometer la calidad o viabilidad del proyecto:

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

### Tabla 6: Descripción de Fases y Puntos Críticos del Ciclo de Vida

| Fase del Ciclo de Vida | Actividades Principales Desarrolladas | Punto Crítico de Control Identificado | Mecanismo de Control y Mitigación Aplicado |
|---|---|---|---|
| **1. Concepción y Requerimientos** | Definición de especificaciones funcionales (probabilidad de pique, especies, inventario). | Requerimientos ambiguos que causen retrabajo continuo. | Validación de historias de usuario y matriz de alcance con el cliente/cátedra. |
| **2. Diseño y Arquitectura** | Definición de clases (`Jugador`, `Pesca`, `Tienda`, etc.) y patrones de diseño. | **Punto Crítico 1:** Alta fricción por acoplamiento de responsabilidades (falla histórica de la tienda). | Refactorización temprana aplicando principios SOLID e Inyección de Dependencias. |
| **3. Construcción y Codificación** | Programación en Ruby 3.x, manipulación de streams y serialización. | Generación de deuda técnica y código espagueti. | Control diario con linters estáticos (`RuboCop`) y pautas unificadas de commit. |
| **4. Aseguramiento de Calidad** | Batería de pruebas funcionales y de límites con RSpec. | **Punto Crítico 2:** Regresiones donde modificaciones nuevas rompen mecánicas ya validadas (ej. equipar caña). | Ejecución obligatoria de la suite de pruebas unitarias en el pipeline de Integración Continua (CI). |
| **5. Despliegue y Operación** | Lanzamiento de versiones ejecutables y distribución a usuarios. | **Punto Crítico 3:** Bloqueos en ejecución o partidas corruptas en `/Data`. | Rutinas transaccionales atómicas de guardado y backups automatizados. |
| **6. Fin de Vida y Retiro** | Descontinuación de soporte y migración tecnológica. | Procesos residuales huérfanos o almacenamiento innecesario (basura digital). | Script de desinstalación limpia y sanitización de registros personales (Ley 25.326). |

---

## 2. Sostenibilidad: Modelo de Triple Impacto

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
