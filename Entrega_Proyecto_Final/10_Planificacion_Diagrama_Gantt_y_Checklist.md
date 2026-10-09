# SECCIÓN 10: PLANIFICACIÓN TEMPORAL, DIAGRAMA DE GANTT Y CONTROL DE GESTIÓN

---

## 1. Planificación Temporal del Proyecto (Diagrama de Gantt)

Para asegurar la ejecución ordenada del proyecto, el cumplimiento de los hitos pedagógicos y la correcta distribución de la carga de trabajo entre los cuatro integrantes del equipo, se estructuró un cronograma en **seis semanas operativas**.

Las tareas fueron secuenciadas considerando sus dependencias lógicas: la arquitectura y modelado de datos preceden necesariamente a la implementación de mecánicas y tiendas, mientras que las pruebas de regresión, auditorías de calidad y documentación final consolidan el cierre del ciclo productivo.

### A. Diagrama de Gantt (Cronograma Visual en Barras)

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

### Tabla 8: Matriz Operativa de Planificación y Asignación de Tareas

| N.° | Tarea / Entregable Específico | Semana de Ejecución | Horas Estimadas | Precedencia / Dependencia | Responsable Directo | Entregable Verificable |
|:---:|---|:---:|:---:|:---:|---|---|
| **1** | Requerimientos, historias de usuario y alcance funcional | **Semana 1** | 20 hs | Ninguna (Inicio) | Equipo Completo | Documento de especificación de requerimientos |
| **2** | Diseño del modelo de dominio de clases (`Jugador`, `Pez`, `Objeto`) | **Semana 2** | 30 hs | Tarea 1 | **Sebastián Zerpa** | Clases base compilables en `/Classes` |
| **3** | Programación del módulo `Pesca`, cálculo de pique y eventos `Timeout` | **Semanas 2 y 3** | 45 hs | Tarea 2 | **Maycol Alconz** | Mecánica de pesca funcional en consola |
| **4** | Refactorización de la `Tienda`, balance económico y corrección bug de caña | **Semanas 3 y 4** | 50 hs | Tarea 2, 3 | **Ezequiel Lizasoain** | Módulo de compras desacoplado sin bloqueos |
| **5** | Implementación de pruebas BDD con `RSpec` y linteo con `RuboCop` | **Semanas 4 y 5** | 45 hs | Tarea 3, 4 | **Sebastián Zerpa** | Suite de tests con cobertura $\ge 85\%$ en verde |
| **6** | Despliegue de Metodología 5S en taller/código y Plan TPM de Mantenimiento | **Semana 5** | 35 hs | Tarea 4, 5 | **Enzo Luna** | Tablas de 5S, rutinas de backup y telemetría RAM |
| **7** | Diseño de Layout (planta de oficina), protocolos SySO, RAEE y Matriz Legal | **Semana 5** | 45 hs | Tarea 1 | **Maycol Alconz** | Planos de planta, fichas de EPP y matriz legal |
| **8** | Consolidación del Informe Técnico final y maquetado de 12 Diapositivas | **Semana 6** | 50 hs | Todas (Cierre) | Equipo Completo | Informe Word unificado y diapositivas en Canva/PPT |
| **TOTAL** | **Esfuerzo Acumulado de Ingeniería del Proyecto** | **6 Semanas** | **320 hs** | | **4 Integrantes** | **Proyecto Final 100% Aprobado** |

---

## 2. Puntos de Control y Gestión de Hitos (Milestones)

1. **Hito 1 (Fin de Semana 2) - *Core Engine Aprobado*:**  
   Clases de dominio estructuralmente validadas y repositorio Git configurado con control de ramas.
2. **Hito 2 (Fin de Semana 4) - *Alfa Funcional y Desacoplamiento*:**  
   Módulos de tienda y pesca totalmente operativos; bug crítico de la caña resuelto y persistencia verificada en la carpeta `/Data`.
3. **Hito 3 (Fin de Semana 5) - *Release Candidate y Cumplimiento Normativo*:**  
   Suite de RSpec ejecutando en Integración Continua con cobertura superior al 85%; matriz de riesgos laborales, layout de planta y plan de mantenimiento finalizados.
4. **Hito 4 (Fin de Semana 6) - *Entrega Definitiva y Defensa Oral*:**  
   Informe técnico consolidado de 3 a 5 páginas impreso/subido a Classroom y presentación digital de 12 diapositivas ensayada para la defensa oral de 15 minutos.
