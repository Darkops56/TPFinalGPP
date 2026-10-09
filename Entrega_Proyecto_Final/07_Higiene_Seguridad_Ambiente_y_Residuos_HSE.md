# SECCIÓN 7: HIGIENE, SEGURIDAD LABORAL, MEDIO AMBIENTE Y GESTIÓN DE RESIDUOS (HSE)

---

## 1. Higiene y Seguridad Laboral en la Industria del Software

El desarrollo computacional se encuentra comúnmente asociado a una baja tasa de accidentes traumáticos visibles; sin embargo, genera patologías profesionales crónicas severas derivadas de posturas estáticas prolongadas, movimientos repetitivos y exposición continua a Pantallas de Visualización de Datos (PVD).

### A. Marco Legal Obligatorio en la República Argentina
El plan de prevención de *AquaByte Development Studio* se encuadra estrictamente en:
* **Ley Nacional N.º 19.587 de Higiene y Seguridad en el Trabajo:** Establece los principios fundamentales de protección psicofísica de los trabajadores.
* **Decreto Reglamentario N.º 351/79:** Fija condiciones ambientales obligatorias (iluminación, ventilación, protección contra incendios e instalaciones eléctricas).
* **Resolución SRT N.º 295/03 (Anexo I - Ergonomía):** Regula específicamente los factores de riesgo ergonómico por movimientos repetitivos en miembros superiores y posturas forzadas en tareas de digitación.

---

## 2. Matriz de Identificación de Riesgos y Medidas Preventivas

### Tabla 5: Matriz de Riesgos Laborales en el Laboratorio de Computación

| Categoría de Riesgo | Agente / Causa Raíz | Daño Potencial para la Salud | Medidas Preventivas y Controles de Ingeniería |
|---|---|---|---|
| **Ergonómico** | Digitación continua y uso intensivo de mouse sin apoyo adecuado | Síndrome del túnel carpiano, tendinitis de muñeca y epicondilitis | - Ratones ergonómicos verticales con pads de gel.<br>- Teclados de bajo recorrido.<br>- Programa de **Pausas Activas obligatorias** (10 minutos cada 60 minutos de codificación con estiramiento guiado). |
| **Ergonómico Postural** | Sedentarismo prolongado en sillas no configurables | Lumbalgias crónicas, dorsalgias y contracturas cervicales | - Sillas neumáticas giratorias con soporte lumbar regulable y respaldo reclinable.<br>- Regulación de altura de pantalla de modo que el borde superior quede a la línea de los ojos. |
| **Visual (PVD)** | Fijación de la mirada en monitores con brillo inadecuado | Fatiga ocular (astenia visual), xeroftalmía (ojo seco) y cefaleas | - Aplicación de la **Regla 20-20-20** (cada 20 min, mirar a 6 metros durante 20 segundos).<br>- Iluminación general difusa a 500 lux sin parpadeos.<br>- Monitores con paneles mate antirreflejo y modo lectura cálido. |
| **Eléctrico** | Conexión de múltiples PCs, fuentes y periféricos | Cortocircuitos, arcos voltaicos y riesgo de electrocución | - Canalización en zócalos ignífugos estandarizados.<br>- Tablero con disyuntor diferencial de $30\text{ mA}$ y llaves termomagnéticas calibradas.<br>- Puesta a tierra verificada periódicamente ($< 5\ \Omega$). |
| **Psicosocial** | Bloqueos lógicos complejos y plazos de entrega (*Deadlines*) | Estrés laboral crónico, síndrome de agotamiento (*Burnout*) | - Planificación realista en sprints ágiles de 1 semana.<br>- Rotación de integrantes en módulos difíciles (ej. refactorización de Tienda).<br>- Clima de acompañamiento técnico sin penalización de errores. |

---

## 3. Elementos de Protección Personal (EPP) y Señalética Reglamentaria

### A. Elementos de Protección Personal (EPP) Asignados al Equipo
Aun cuando el programador opera en entornos de oficina, el laboratorio técnico escolar y la manipulación de hardware exigen el uso de EPP específicos certificados:
1. **Lentes de Descanso con Filtro de Luz Azul y Tratamiento Antirreflejo:**  
   Protegen el cristalino y la retina frente a la radiación azul de onda corta emitida por pantallas LED, reduciendo el insomnio y la fatiga visual.
2. **Muñequeras Ortopédicas Elásticas con Soporte Anatómico:**  
   Mantienen la articulación de la muñeca en posición neutra durante extensas sesiones de testeo y digitación, previniendo la compresión del nervio mediano.
3. **Pulseras Antiestáticas (ESD) con Descarga a Tierra:**  
   Utilizadas de forma obligatoria durante tareas de apertura y mantenimiento de gabinetes de PC o servidores locales, protegiendo tanto los circuitos integrados de descargas electrostáticas como al técnico de tensiones parásitas.
4. **Calzado Dieléctrico con Suela Aislante de Goma:**  
   Requerido para el personal que ejecuta tareas de inspección en el tablero eléctrico o conexionado de la UPS del laboratorio.

### B. Pictogramas y Señalética de Seguridad (Norma IRAM 10.005)
* **Cartel de Riesgo Eléctrico:** Señal triangular amarilla con borde negro y rayo, fijada sobre la tapa del tablero eléctrico general.
* **Señalización de Extintor Clase C:** Cartel cuadrado rojo con pictograma reglamentario ubicado a $1,80\text{ m}$ sobre el matafuegos de $CO_2$. Se emplea exclusivamente dióxido de carbono para no dañar los circuitos electrónicos ni dejar residuos químicos conductores.
* **Flechas de Vía de Escape Fotoluminiscentes:** Señales verdes que marcan la trayectoria expedita hacia la puerta de salida de emergencia.
* **Cartel de Botiquín de Primeros Auxilios:** Ubicado sobre el gabinete de curaciones de emergencia.

---

## 4. Sistema de Gestión Ambiental (ISO 14001:2015)

De acuerdo con el documento de la norma **ISO 14001** incluido en los apuntes, la sustentabilidad en la industria digital exige identificar y controlar los aspectos ambientales directos e indirectos generados por el proceso de manufactura de software.

### A. Política Ambiental de AquaByte Development Studio
> *“AquaByte Development Studio se compromete a minimizar el impacto ambiental derivado de sus actividades de computación, promoviendo el uso racional y eficiente de la energía eléctrica, prolongando el ciclo de vida de los equipos mediante mantenimiento preventivo y asegurando la disposición final ambientalmente segura de los residuos electrónicos generados, en estricto cumplimiento de la normativa ambiental argentina vigente.”*

### B. Matriz de Aspectos e Impactos Ambientales

| Proceso / Actividad | Aspecto Ambiental | Impacto Ambiental Asociado | Medida de Mitigación y Control Operacional |
|---|---|---|---|
| **Ejecución y Testeo de Código** | Consumo continuo de energía eléctrica de la red | Agotamiento de recursos energéticos no renovables y emisiones indirectas de $CO_2$ | - Configuración de perfiles de energía eco-friendly en las PCs.<br>- Apagado total de monitores y periféricos al finalizar la jornada.<br>- Optimización algorítmica para reducir ciclos ociosos de CPU. |
| **Disipación Térmica de PCs** | Emisión de calor por fuentes y microprocesadores | Necesidad de refrigeración forzada (mayor consumo energético del aula) | - Distribución espacial espaciada en el Layout.<br>- Limpieza regular de disipadores de calor para máxima eficiencia térmica. |
| **Mantenimiento y Bajas de Hardware** | Generación de rezagos electrónicos (RAEE) | Contaminación del suelo y mantos freáticos por metales pesados (plomo, cadmio, mercurio) | - Segregación diferenciada en taller.<br>- Reutilización de memorias y discos como repuestos.<br>- Entrega formal en Puntos Verdes habilitados. |

---

## 5. Gestión y Clasificación Técnica de Residuos

Para evitar el desecho indiferenciado en la vía pública, se implementa una clasificación en tres corrientes de residuos:

```
       +-------------------------------------------------------------+
       |             CLASIFICACIÓN INTEGRAL DE RESIDUOS              |
       +-------------------------------------------------------------+
         |
         +--> CORRIENTE 1: RAEE (Residuos Electrónicos - Ley 24.051)
         |    [Placas madre, fuentes quemadas, cables, periféricos rotos]
         |    ==> Almacenamiento seguro y entrega en Puntos Verdes CABA.
         |
         +--> CORRIENTE 2: RESIDUOS SECOS RECICLABLES
         |    [Cajas de componentes, cartones, embalajes, papel de oficina]
         |    ==> Tacho verde y entrega a cooperativas de reciclado urbano.
         |
         +--> CORRIENTE 3: BASURA DIGITAL (E-Waste Lógico)
              [Ramas huérfanas en Git, logs infinitos, archivos temporales]
              ==> Scripts de purga para reducir la huella de servidores cloud.
```

1. **Residuos de Aparatos Eléctricos y Electrónicos (RAEE):**  
   Comprende fuentes de alimentación quemadas, motherboards obsoletas, cables cortados y teclados averiados. Se almacenan transitoriamente en recipientes plásticos cerrados, secos y rotulados. Su disposición final se efectúa mediante traslado a los **Puntos Verdes Móviles y Centros Verdes del Gobierno de la Ciudad de Buenos Aires**, amparados en la Ley Nacional de Residuos Peligrosos N.º 24.051 y normativas locales de RAEE.
2. **Residuos Sólidos Secos (Reciclables Urbanos):**  
   Cajas de cartón corrugado donde se reciben insumos, envoltorios de polietileno y documentación técnica impresa obsoleta. Se depositan limpios y secos en el contenedor verde del laboratorio para su recolección diferenciada.
3. **Basura Digital (Desechos Lógicos en la Nube):**  
   Aunque inmateriales, los terabytes de registros (*logs*) huérfanos, compilados temporales y copias de seguridad redundantes alojados en servidores consumen energía eléctrica permanente en centros de datos remotos. El equipo aplica rutinas mensuales de purga de ramas Git cerradas y limpieza de carpetas `/tmp` para mitigar la huella de carbono digital indirecta.
