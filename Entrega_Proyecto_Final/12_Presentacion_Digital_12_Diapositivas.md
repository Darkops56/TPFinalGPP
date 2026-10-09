# SECCIÓN 12: ESTRUCTURA DE PRESENTACIÓN DIGITAL (12 DIAPOSITIVAS PARA CANVA / POWERPOINT)

---

## 1. Guía de Diseño y Parámetros de la Presentación Oral

* **Duración Total:** 15 minutos exactos (exposición cronometrada de ~1 min 15 s por diapositiva).
* **Participación:** Distribución equilibrada entre los cuatro integrantes (Sebastián Zerpa, Ezequiel Lizasoain, Enzo Luna y Maycol Alconz).
* **Pautas Estéticas en Canva / PowerPoint:**
  - Fondo limpio y profesional (modo oscuro elegante o blanco institucional).
  - Incluir el logotipo oficial de la **Escuela Técnica N.º 12 D.E. 1**.
  - Frases breves, tipografía legible sin serifas (ej. *Inter*, *Montserrat* o *Roboto*), gráficos de alto contraste y esquemas conceptuales sin saturación de texto.

---

## 2. Contenido Estructurado Slide por Slide

```
================================================================================
DIAPOSITIVA 1: PORTADA INSTITUCIONAL Y PROTOTIPO
================================================================================
[Encabezado Visual]
- Logo Institucional: Escuela Técnica N.º 12 "Libertador Gral. José de San Martín"
- Materia: Gestión de los Procesos Productivos (GPP) | Curso: 6.º Año Computación
- Título Central: SISTEMA DE PESCA Y GESTIÓN ECONÓMICA EN RUBY
- Subtítulo: Integración de Estándares Industriales y Calidad al Desarrollo de Software
- Nombre del Estudio: AquaByte Development Studio

[Datos del Equipo]
- Integrantes: Sebastián Zerpa, Ezequiel Lizasoain, Enzo Luna, Maycol Alconz
- Elemento Gráfico: Captura de pantalla de la terminal con el juego en ejecución y
  diagrama en bloque de las clases (Jugador, Pesca, Tienda).
- Orador Inicial: Sebastián Zerpa (Tiempo: 1:00 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 2: CICLO PDCA (MEJORA CONTINUA EN EL SOFTWARE)
================================================================================
[Título]: CICLO PDCA: MEJORA CONTINUA DE DEMING APLICADA AL SOFTWARE
[Diagrama Circular Central: P -> D -> C -> A]
- PLANIFICAR (Plan):
  * Detección de fallas críticas: bug de equipamiento de caña y rigidez en la Tienda.
  * Meta fijada: 0 bugs críticos, cobertura de tests >= 85% y modularización en 4 semanas.
- HACER (Do):
  * Implementación de testing BDD con RSpec y refactorización orientada a objetos (SOLID).
- VERIFICAR (Check):
  * 28 tests unitarios en verde, cobertura alcanzada del 88,4% con SimpleCov, 0 regresiones.
- ACTUAR (Act):
  * Estandarización de integración continua (CI) en GitHub Actions obligatoria para merge.
- Orador: Sebastián Zerpa (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 3: SEGURIDAD E HIGIENE LABORAL Y EPP
================================================================================
[Título]: HIGIENE, SEGURIDAD LABORAL Y ERGONOMÍA INFORMÁTICA
[Marco Legal]: Ley Nacional 19.587, Dec. 351/79 y Resolución SRT 295/03 (Ergonomía).

[Columnas Comparativas de Riesgos y Controles]
1. Riesgo Ergonómico / Túnel Carpiano:
   * Sillas neumáticas regulables, mouse vertical anatómico y Pausas Activas (10 min/hora).
2. Riesgo Visual (Pantallas PVD):
   * Regla 20-20-20, iluminación homogénea a 500 lux y paneles mate antirreflejo.
3. Riesgo Eléctrico:
   * Zócalos ignífugos, disyuntor de 30 mA, puesta a tierra y matafuegos CO2 (Clase C).

[Elementos de Protección Personal (EPP)]:
- Lentes con filtro de luz azul, muñequeras ortopédicas y pulseras antiestáticas para hardware.
- Señalética IRAM 10.005: Pictogramas de Riesgo Eléctrico y Extintor Clase C.
- Orador: Maycol Alconz (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 4: CICLO DE VIDA DEL PRODUCTO (ACV SOFTWARE)
================================================================================
[Título]: CICLO DE VIDA DEL SOFTWARE (ACV) Y PUNTOS CRÍTICOS
[Diagrama de Flujo Horizontal con 6 Fases]
1. Requerimientos -> 2. Arquitectura -> 3. Codificación -> 4. QA/Tests -> 5. Release -> 6. Retiro

[Puntos Críticos de Control (Alarmas Rojas Identificadas)]:
- Punto Crítico 1 (Diseño): Acoplamiento excesivo en Tienda ("ganas de codear").
  * Solución: Inyección de dependencias y separación de lógica comercial.
- Punto Crítico 2 (Testing): Regresiones imprevistas en mecánicas validadas.
  * Solución: Batería automatizada de tests de regresión con RSpec.
- Punto Crítico 3 (Operación): Riesgo de corrupción de partidas en carpeta /Data.
  * Solución: Operaciones transaccionales atómicas y respaldos diarios.
- Orador: Enzo Luna (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 5: GESTIÓN AMBIENTAL Y RESIDUOS (RAEE)
================================================================================
[Título]: GESTIÓN DE RESIDUOS Y ACCIONES DE MITIGACIÓN AMBIENTAL
[Esquema de Clasificación en 3 Corrientes de Desechos]

1. Residuos Electrónicos (RAEE - Ley 24.051):
   * Fuentes de PC, placas madre, cables y periféricos dañados.
   * Destino: Acopio seguro y traslado a Puntos Verdes oficiales de CABA (reciclaje de metales).
2. Residuos Secos Reciclables:
   * Cajas de cartón, plásticos de embalajes e insumos de oficina.
   * Destino: Tacho verde para cooperativas de recicladores urbanos.
3. Basura Digital (Huella Cloud):
   * Purga mensual de ramas huérfanas en Git, logs infinitos y archivos temporales.
- Reducción de Consumo: Política de apagado total de laboratorio al finalizar la jornada.
- Orador: Maycol Alconz (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 6: NORMAS ISO 14001 (GESTIÓN AMBIENTAL)
================================================================================
[Título]: SISTEMA DE GESTIÓN AMBIENTAL (SGA - ISO 14001:2015)
[Compromiso de la Política Ambiental de AquaByte Studio]
"Minimizar la huella energética del cómputo y garantizar la gestión responsable de residuos".

[Matriz de Aspectos e Impactos Ambientales]:
- Aspecto 1: Consumo de energía de estaciones de desarrollo y servidores.
  * Impacto: Consumo de recursos fósiles y emisiones indirectas de CO2.
  * Control Operacional: Perfiles eco en PCs y optimización algorítmica de bajo consumo de CPU.
- Aspecto 2: Disipación térmica de gabinetes informáticos.
  * Control Operacional: Layout con espaciamiento de ventilación y limpieza de disipadores.
- Aspecto 3: Descarte de componentes defectuosos.
  * Control Operacional: Reutilización de piezas como repuestos y trazabilidad de RAEE.
- Orador: Maycol Alconz (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 7: METODOLOGÍA 5 S EN COMPUTACIÓN
================================================================================
[Título]: METODOLOGÍA 5 S EN EL TALLER Y EN EL CÓDIGO FUENTE
[Gráfico de las 5 Etapas con Doble Enfoque (Físico vs Digital)]:

1. SEIRI (Clasificar):
   * Taller: Descartar periféricos rotos. | Código: Purgar código muerto y gemas no usadas.
2. SEITON (Ordenar):
   * Taller: Puestos y herramientas rotuladas. | Código: Estructura fija /Classes, /Data, /Spec.
3. SEISO (Limpiar):
   * Taller: Aire comprimido en coolers. | Código: Formateo automático con RuboCop -a.
4. SEIKETSU (Estandarizar):
   * Taller: Protocolo de inicio/cierre. | Código: Adopción del Ruby Style Guide y plantillas PR.
5. SHITSUKE (Disciplina):
   * Taller: Orden sostenido en bancos. | Código: Revisiones de código cruzadas (Code Review).
- Orador: Ezequiel Lizasoain (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 8: PLAN DE MANTENIMIENTO TOTAL (TPM)
================================================================================
[Título]: PLAN DE MANTENIMIENTO TOTAL: PREVENTIVO, CORRECTIVO Y PREDICTIVO
[Tabla Operativa Resumida]:

- MANTENIMIENTO PREVENTIVO (Calendarizado):
  * Semanal: Auditoría de código estático con RuboCop (Responsable: E. Lizasoain).
  * Mensual: Auditoría de seguridad y gemas con Bundler-Audit (Responsable: S. Zerpa).
  * Diario: Respaldo automatizado de partidas en /Data mediante script cron (M. Alconz).
- MANTENIMIENTO CORRECTIVO (SLA de Respuesta):
  * Gestión de bugs mediante GitHub Issues (Triaje < 4 hs).
  * Protocolo de Hotfixes para mecánicas críticas (Resolución < 24 hs - S. Zerpa).
- MANTENIMIENTO PREDICTIVO 4.0 (Telemetría de Datos):
  * Detección de fugas de memoria RAM en Ruby con Machine Learning y Profiling (E. Luna).
  * Monitoreo de latencia en consultas de base de datos antes de saturación (S. Zerpa).
- Orador: Enzo Luna (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 9: SISTEMA DE CALIDAD (ISO 9001:2015)
================================================================================
[Título]: SISTEMA DE GESTIÓN DE LA CALIDAD (SGC - ISO 9001:2015)
[Esquema de los 5 Pilares de Calidad en Ruby]:
1. Gestión de Riesgos: Control de excepciones Timeout::Error y validación de inventario.
2. Control Operacional: Clases desacopladas (Jugador, Pesca, Tienda, Pez, Objeto).
3. Información Documentada: Trazabilidad en Git, commits atómicos y documentación técnica.
4. Evaluación del Desempeño: Testing exhaustivo con RSpec (Cobertura >= 85%).
5. Mejora Continua: Ciclo iterativo para refactorización basado en feedback del usuario.

[KPIs de Calidad]:
- 0 defectos críticos en release final.
- MTTR (Tiempo de reparación de incidentes) < 24 horas.
- 0 infracciones a las guías de estilo de código.
- Orador: Sebastián Zerpa (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 10: SOSTENIBILIDAD (TRIPLE IMPACTO)
================================================================================
[Título]: SOSTENIBILIDAD: MODELO DE TRIPLE IMPACTO EN SOFTWARE
[Gráfico de Tres Círculos Interconectados]

1. IMPACTO SOCIAL (Bienestar y Comunidad):
   * Erradicación de la sobrecarga y desmotivación en el equipo mediante equidad laboral.
   * Publicación bajo Licencia de Código Abierto (MIT) con valor educativo para la ET N.° 12.
2. IMPACTO ECONÓMICO (Viabilidad a Largo Plazo):
   * Modelo ético sin microtransacciones engañosas ni mecánicas pay-to-win.
   * Presupuesto balanceado: inversión controlada de $ 4.675.000 ARS y costos OPEX mínimos.
3. IMPACTO AMBIENTAL (Eficiencia Computacional):
   * Optimización algorítmica: código de bajo impacto con menos del 2% de uso de CPU.
   * Lucha contra la obsolescencia programada: ejecución fluida en PCs de bajos recursos.
- Orador: Ezequiel Lizasoain (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 11: LAYOUT FÍSICO Y LÓGICO DEL PROYECTO
================================================================================
[Título]: DISTRIBUCIÓN DEL ESPACIO DE TRABAJO Y ARQUITECTURA (LAYOUT)
[Esquema Visual del Layout Físico]:
- 4 puestos individuales en isla con iluminación natural lateral (anti-reflejo).
- Mesa central de reuniones ágiles (Scrum, Kanban y Code Review).
- Puesto de pruebas/servidor local aislado con UPS y switch gigabit.
- Tablero eléctrico general y matafuegos de CO2 Clase C en zona de acceso.
- Pasillos amplios de 1,60 m despejados hacia la salida de emergencia.

[Beneficios Clave]:
- Físicos: Comunicación directa, confort postural y seguridad eléctrica absoluta.
- Lógicos: Arquitectura en capas desacopladas (UI -> Lógica -> Dominio -> Persistencia /Data).
- Orador: Enzo Luna (Tiempo: 1:15 min).
================================================================================
```

```
================================================================================
DIAPOSITIVA 12: MATRIZ LEGAL, PLANIFICACIÓN GANTT Y CONCLUSIONES
================================================================================
[Título]: MATRIZ LEGAL, GANTT Y CONCLUSIONES GENERALES DEL GRUPO
[Matriz Legal Sintética]:
- Ley 11.723 (Propiedad Intelectual de Software) -> Licencia MIT y autoría compartida.
- Ley 25.326 (Protección de Datos Personales) -> Privacidad por diseño, guardado local.
- Ley 19.587 / Res. SRT 295/03 -> Higiene, seguridad y ergonomía obligatoria.
- Ley 24.051 (Residuos Peligrosos) -> Entrega de RAEE en Puntos Verdes de CABA.
- Ley 24.240 (Defensa del Consumidor) -> Transparencia y honestidad con el usuario.

[Cronograma Gantt Resumido]:
- 6 semanas de desarrollo, 320 horas totales de ingeniería, checklist 100% aprobado.

[Reflexión Final del Grupo]:
"La aplicación de normas industriales (ISO 9001/14001, 5S, HSE y TPM) transformó un script
vulnerable en un producto de software profesional, seguro, sustentable y escalable."
- Orador Final: Sebastián Zerpa / Cierre Conjunto del Equipo (Tiempo: 1:30 min).
================================================================================
```
