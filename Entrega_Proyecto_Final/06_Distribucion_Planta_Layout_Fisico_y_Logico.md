# SECCIÓN 6: DISTRIBUCIÓN DEL ESPACIO DE TRABAJO Y ARQUITECTURA (LAYOUT FÍSICO Y LÓGICO)

---

## 1. Layout Físico del Laboratorio de Desarrollo Informático

La disposición física del puesto de trabajo en la industria del software no es un aspecto secundario: incide de manera directa en la productividad, la agilidad de la comunicación del equipo, la prevención de accidentes eléctricos y la salud postural de los desarrolladores.

Para las actividades de desarrollo de *AquaByte Development Studio*, se diseñó un plano de distribución de planta funcional de **35 m² (7,0 m × 5,0 m)** representativo del laboratorio técnico escolar y de una oficina de desarrollo profesional.

### A. Plano Esquemático de Distribución en Planta (Layout Físico)

```
+-----------------------------------------------------------------------------+
| [VENTANA - LUZ NATURAL CONTROLADA]     [VENTANA - LUZ NATURAL CONTROLADA]   |
|                                                                             |
|  +--------------------+                     +--------------------+          |
|  | Puesto Dev 1       |                     | Puesto Dev 2       |          |
|  | (S. Zerpa - QA)    |                     | (E. Lizasoain)     |          |
|  | [Monitor][Teclado] |                     | [Monitor][Teclado] |          |
|  +--------------------+                     +--------------------+          |
|            |                                           |                    |
|            +------------------ PASILLO ----------------+                    |
|                               (1,60 m)                                      |
|            +------------------ CENTRAL ---------------+                     |
|            |                                          |                     |
|  +--------------------+                     +--------------------+          |
|  | Puesto Dev 3       |                     | Puesto Dev 4       |          |
|  | (E. Luna - TPM)    |                     | (M. Alconz - HSE)  |          |
|  | [Monitor][Teclado] |                     | [Monitor][Teclado] |          |
|  +--------------------+                     +--------------------+          |
|                                                                             |
|  +---------------------------------------------------------------+          |
|  | MESA DE REUNIONES Y PUESTA EN COMÚN (Scrum / Kanban / Code Review)|      |
|  +---------------------------------------------------------------+          |
|                                                                             |
| [PUESTO QA / SERVIDOR LOCAL]               [PUNTO ECOLÓGICO / RECIPIENTES]  |
| [Switch / UPS / Rack UTP]                 [RAEE / Secos / Cartón]           |
|                                                                             |
| [TABLERO ELÉCTRICO / TERMICAS]             [EXTINTOR CO2 CLASE C / BOTIQUÍN]|
|                                                                             |
| +==================== PUERTA DE ACCESO / EVACUACIÓN =====================+  |
+-----------------------------------------------------------------------------+
```

### B. Elementos Principales del Layout Físico
1. **Puestos de Trabajo Individuales (4 Estaciones):**  
   Disposición en isla enfrentada 2 a 2. Garantiza que la luz natural incida de forma lateral respecto a los monitores para evitar reflejos directos en las pantallas o deslumbramientos conforme a la norma IRAM-AADL J 20-06.
2. **Mesa Central Ágil de Coordinación:**  
   Espacio común destinado a reuniones diarias breves (*Daily Stand-ups*), revisiones de código cruzadas (*Pair Programming* y *Code Reviews*) y pizarrón Kanban para la asignación visual de tareas.
3. **Puesto de Servidor Local, Redes y Aseguramiento de Calidad:**  
   Módulo aislado donde se emplazan el Switch Gigabit, la UPS de respaldo y el servidor de pruebas para ejecutar las suites automatizadas de RSpec sin sobrecargar las máquinas de los desarrolladores.
4. **Área de Seguridad y Emergencias:**  
   Tablero eléctrico general ubicado junto al acceso, dotado de llaves termomagnéticas bipolares y disyuntor diferencial de alta sensibilidad ($30\text{ mA}$). Matafuegos de dióxido de carbono ($CO_2$, 5 kg, apto Clase C para fuegos eléctricos) y botiquín de primeros auxilios colocados a $1,50\text{ m}$ de altura con señalización fotoluminiscente.
5. **Punto Verde de Segregación de Residuos:**  
   Sector delimitado para la separación de residuos secos reciclables (papel y embalajes) y contenedor específico acolchado para rezagos electrónicos (RAEE).

---

## 2. Beneficios Productivos y Ergonómicos del Layout Físico

* **Optimización de la Comunicación Colaborativa:**  
  La cercanía controlada entre los puestos permite resolver bloqueos lógicos en minutos sin necesidad de canales asincrónicos, favoreciendo la dinámica de equipo.
* **Ergonomía Postural y Prevención de Lesiones:**  
  Pasillos amplios de $1,60\text{ m}$ garantizan el libre desplazamiento de las sillas ergonómicas, permitiendo a los desarrolladores estirar las extremidades y realizar las pausas activas reglamentarias.
* **Seguridad Operativa y Rutas de Escape:**  
  Ausencia total de cables flotantes gracias a zócalos perimetrales ignífugos. La vía hacia la puerta de salida permanece 100% despejada ante emergencias de evacuación.
* **Eficiencia Térmica y Disipación de Equipos:**  
  La separación entre estaciones asegura un flujo continuo de aireación que evita el sobrecalentamiento pasivo de los gabinetes, prolongando la vida útil del hardware.

---

## 3. Layout Lógico: Arquitectura Modular del Software

De forma análoga al espacio físico, el software requiere una distribución ordenada de sus componentes lógicos para garantizar la separación de intereses (*Separation of Concerns*) y facilitar el mantenimiento.

```
+-----------------------------------------------------------------------------+
|                      CAPA 1: INTERFAZ Y PRESENTACIÓN                        |
|   (Entrada y Salida en Consola / Menús interactivos / Formateo visual ANSI) |
+-----------------------------------------------------------------------------+
                                       |
                                       v
+-----------------------------------------------------------------------------+
|                    CAPA 2: LÓGICA DE NEGOCIO Y CONTROL                      |
|         Clase Pesca                         Clase Tienda                    |
|   - Eventos temporizados (Timeout)     - Transacciones económicas           |
|   - Probabilidad y rareza              - Validación de saldo y stock        |
+-----------------------------------------------------------------------------+
                                       |
                                       v
+-----------------------------------------------------------------------------+
|                     CAPA 3: MODELO DE DOMINIO (ENTIDADES)                   |
|       Clase Jugador             Clase Pez              Clase Objeto         |
|   - Saldo y nivel         - Especie y peso       - Cebos y herramientas     |
|   - Inventario activo     - Valor de mercado     - Cañas equipables         |
+-----------------------------------------------------------------------------+
                                       |
                                       v
+-----------------------------------------------------------------------------+
|                    CAPA 4: INFRAESTRUCTURA Y PERSISTENCIA                   |
|           Directorio /Data (Serialización, guardado y lectura atómica)       |
+-----------------------------------------------------------------------------+
```

### Justificación del Layout Lógico
Esta arquitectura en 4 capas desacopla totalmente la lógica transaccional de la interfaz. De este modo, si en el futuro se reemplaza la consola por una interfaz gráfica (GUI) o web, las clases de negocio (`Pesca`, `Tienda`, `Jugador`) permanecerán inalteradas, reduciendo el costo de mantenimiento a cero en el núcleo de la aplicación.
