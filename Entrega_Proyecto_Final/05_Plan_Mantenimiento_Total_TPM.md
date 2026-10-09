# SECCIÓN 5: PLAN DE MANTENIMIENTO TOTAL (TPM: PREVENTIVO, CORRECTIVO Y PREDICTIVO)

---

## 1. Fundamentos y Enfoque del Mantenimiento Total

El Mantenimiento Productivo Total (TPM) persigue la maximización de la efectividad operativa de los activos productivos, orientándose hacia el objetivo de **cero averías, cero defectos y cero tiempos improductivos**.

En el ámbito del desarrollo y soporte de software, el mantenimiento no se limita a intervenir tras una caída imprevista del sistema, sino que abarca un conjunto integrado de disciplinas operativas estructuradas en tres niveles tácticos: **Preventivo**, **Correctivo** y **Predictivo 4.0**, en estricta consonancia con los apuntes de *“Mantenimiento Predictivo 4.0”* y la *“Guía de Herramientas para el Mantenimiento Predictivo”* provistos por la cátedra.

---

## 2. Los Tres Niveles Tácticos de Mantenimiento

### A. Mantenimiento Preventivo (Planificado y Sistemático)
Tiene como objetivo primordial anticiparse al desgaste funcional del software, prevenir vulnerabilidades de seguridad y conservar el rendimiento óptimo del entorno de ejecución mediante acciones periódicas:
1. **Auditoría Estática de Código (Semanal):**  
   Ejecución programada de la gema `RuboCop` para auditar el cumplimiento de los estándares de estilo de Ruby, detectar olores en el código (*code smells*) y controlar la complejidad ciclomática de los métodos antes de que se integren en el repositorio.
2. **Actualización de Gemas y Parches de Seguridad (Mensual):**  
   Mantenimiento de dependencias mediante `bundle outdated` y auditoría de vulnerabilidades con `bundler-audit` contra la base de datos comunitaria de CVEs de Ruby. Esto evita la inserción inadvertida de librerías comprometidas.
3. **Respaldo Automatizado de Partidas y Persistencia (Diario):**  
   Ejecución de un script cron que genera copias comprimidas de seguridad (`tar.gz` o zip rotativo) de los archivos alojados en `/Data` hacia almacenamiento secundario, asegurando la no pérdida de información de usuarios.

### B. Mantenimiento Correctivo (Reactivo y Estandarizado)
Se orienta a diagnosticar, aislar y subsanar fallas funcionales o lógicas de forma inmediata tras su manifestación en producción:
1. **Canal Formal de Clasificación de Incidentes:**  
   Implementación del módulo de *GitHub Issues* configurado con plantillas de severidad (*Crítico / Alto / Medio / Bajo*), pasos de reproducción y logs de entorno.
2. **Protocolo Ágil de "Hotfixes":**  
   Flujo de trabajo para emergencias operativas (como el error histórico donde la caña de pescar no se equipaba). Se crea una rama temporal `hotfix/`, se escribe un test de regresión en RSpec que reproduzca el bug, se aplica la corrección puntual y se despliega con alta prioridad hacia la rama principal.
3. **Plan de Restauración ante Falla de Persistencia:**  
   Protocolo de recuperación rápida en caso de corrupción del archivo de datos por cierre abrupto de la terminal, restaurando automáticamente el último estado consistente respaldado.

### C. Mantenimiento Predictivo 4.0 (Monitoreo Basado en Datos y Telemetría)
*¿El proyecto lo requiere?* En una ejecución estrictamente monousuario local, el mantenimiento preventivo y correctivo es suficiente. Sin embargo, al proyectar el simulador hacia una arquitectura de servidor multiusuario en la nube o modelo SaaS (Software as a Service), **el mantenimiento predictivo resulta indispensable**.

Basándonos en la guía de Mantenimiento Predictivo para la Industria 4.0, se incorporan técnicas analíticas para anticipar la degradación de recursos antes de que ocurran interrupciones:
1. **Detección Predictiva de Fugas de Memoria (RAM Leaks en Ruby):**  
   A través de agentes de telemetría y perfiles de consumo (`ObjectSpace` y métricas de recolector de basura de Ruby - GC), se analizan series temporales del consumo de memoria RAM de los procesos. Mediante modelos estadísticos de regresión y machine learning supervisado, se detectan tendencias anómalas de crecimiento de memoria residual generadas por colecciones de datos no liberadas en los bucles de pesca, permitiendo programar el reinicio o parcheo del proceso días antes de un colapso por *Out-Of-Memory* (OOM).
2. **Análisis de Degradación en Operaciones de Disco y Persistencia:**  
   Monitoreo continuo de los tiempos de lectura y escritura en la carpeta `/Data`. Al registrar un incremento sostenido en la latencia media de I/O ($> 150\text{ ms}$), se predice la saturación del sistema de almacenamiento o la fragmentación de archivos de guardado, activando una compactación automática de datos.

---

## 3. Plan Operativo de Mantenimiento Total

La siguiente matriz estandariza las rutinas de mantenimiento del proyecto, definiendo frecuencias, responsables, herramientas y Acuerdos de Nivel de Servicio (SLAs):

### Tabla 4: Plan Operativo de Mantenimiento del Sistema de Pesca

| Nivel Táctico | Tarea Específica de Mantenimiento | Frecuencia | Responsable Asignado | Herramienta de Soporte | SLA / Tiempo Límite | Criterio de Aprobación |
|---|---|:---:|:---:|:---:|:---:|---|
| **Preventivo** | Auditoría estática de estilo y complejidad | Semanal | Ezequiel Lizasoain | `RuboCop` | 1 hora | 0 ofensas o advertencias críticas de estilo |
| **Preventivo** | Auditoría de vulnerabilidades en gemas | Mensual | Sebastián Zerpa | `Bundler-Audit` | 2 horas | 0 vulnerabilidades conocidas (CVE) |
| **Preventivo** | Respaldo automático de la carpeta `/Data` | Diario | Maycol Alconz | Cron Script + Bash | 15 minutos | Copia íntegra verificada y comprimida |
| **Preventivo** | Verificación de integridad física de PCs | Quincenal | Enzo Luna | Checklist 5S + Aire comprimido | 1 hora | Gabinetes libres de polvo y cables seguros |
| **Correctivo** | Clasificación y triaje de nuevos bugs | Diario | Ezequiel Lizasoain | GitHub Issues | $< 4\text{ horas}$ | Issue etiquetado con severidad y asignado |
| **Correctivo** | Resolución de bugs bloqueantes (*Hotfix*) | A demanda | Sebastián Zerpa | Git + RSpec | $< 24\text{ horas}$ | Test de regresión verde y merge aprobado |
| **Correctivo** | Recuperación ante corrupción de partidas | A demanda | Maycol Alconz | Script de restauración | $< 30\text{ minutos}$ | Partida restablecida sin pérdida mayor a 24h |
| **Predictivo** | Telemetría de consumo de memoria RAM | Quincenal | Enzo Luna | Profiler / Data Analytics | 2 horas | Pendiente de curva de RAM estable (sin fugas) |
| **Predictivo** | Monitoreo de latencia en consultas `/Data` | Mensual | Sebastián Zerpa | Benchmark Ruby | 1 hora | Latencia media de lectura/escritura $< 50\text{ ms}$ |
