# SECCIÓN 9: MARCO REGULATORIO Y MATRIZ LEGAL APLICABLE

---

## 1. Fundamentación del Marco Regulatorio

Todo emprendimiento de base tecnológica e industrial debe encuadrarse de forma estricta dentro del marco normativo vigente del territorio donde opera. 

Para *AquaByte Development Studio*, el desarrollo y explotación del sistema de simulación en Ruby requiere el cumplimiento simultáneo de legislaciones en materia de **propiedad intelectual**, **privacidad y seguridad de datos**, **condiciones laborales, higiene, seguridad y riesgos del trabajo**, **protección ambiental y residuos**, y **derechos del consumidor**, conforme a las leyes de la República Argentina y la normativa jurisdiccional de la Ciudad Autónoma de Buenos Aires.

---

## 2. Matriz Legal Integral del Proyecto

### Tabla 7: Matriz de Cumplimiento Legal y Normativo en la República Argentina

| Norma / Ley | Denominación Oficial y Jurisdicción | Objeto y Alcance Jurídico | Aplicación Concreta al Proyecto | Mecanismo y Modo de Cumplimiento en el Software |
|---|---|---|---|---|
| **Ley N.º 11.723** | Régimen Legal de la Propiedad Intelectual *(República Argentina)* | Ampara las obras científicas, literarias y artísticas. Asimila expresamente el **software y código fuente** a obras protegidas (Dec. 165/94). | Protección de la autoría sobre el código en Ruby, mecánicas del simulador y diseño de clases. | - Declaración expresa de autoría de los cuatro integrantes.<br>- Adopción de la **Licencia de Código Abierto MIT** adjunta al repositorio, permitiendo uso y estudio libre pero protegiendo los derechos morales de los autores.<br>- Registro opcional de obra inédita ante la DNDA. |
| **Ley N.º 25.326** | Ley de Protección de los Datos Personales *(Habeas Data)* | Garantiza el honor e intimidad de las personas y el tratamiento legítimo de datos personales asentados en archivos o bancos de datos. | Gestión de perfiles de usuario, nombres de jugador, donaciones y registros de partidas en `/Data`. | - Principio de finalidad: únicamente se almacenan apodos locales de juego sin solicitar datos sensibles (DNI, tarjetas o correos).<br>- Almacenamiento local descentralizado (en la PC del propio usuario).<br>- Cero transferencia de datos a terceras partes. |
| **Ley N.º 19.587 y Dec. 351/79** | Ley de Higiene y Seguridad en el Trabajo *(Nacional)* | Fija pautas psicofísicas de trabajo seguro, condiciones edilicias, térmicas, lumínicas y eléctricas en establecimientos productivos. | Puestos de trabajo de los desarrolladores durante las jornadas de programación, ensamble y testing en el aula-taller. | - Provisión de puestos ergonómicos y distribución espacial según Layout (pasillo de 1,60 m).<br>- Tablero con disyuntor de 30 mA, puesta a tierra $< 5\ \Omega$ y matafuegos de $CO_2$.<br>- Iluminación calibrada a 500 lux y cableado bajo canaletas ignífugas. |
| **Ley N.º 24.557** | Ley de Riesgos del Trabajo (LRT) – Sistema SRT / ART *(Nacional)* | Establece el sistema de aseguramiento obligatorio frente a accidentes de trabajo y enfermedades profesionales; promueve la prevención y la rehabilitación. | Cobertura integral del equipo técnico frente a contingencias en el laboratorio informático o en trayectos (*in itinere*). | - Registro ante aseguradora de riesgos del trabajo (ART) y cumplimiento de directivas de la Superintendencia de Riesgos del Trabajo (SRT).<br>- Adopción de un Sistema de Gestión de Riesgos documentado con auditorías internas periódicas. |
| **Resolución SRT N.º 295/03** | Anexo I – Especificaciones Técnicas sobre Ergonomía *(Nacional)* | Regula los factores de riesgo ergonómico por movimientos repetitivos en miembros superiores y posturas forzadas en usuarios de PVD. | Puestos de trabajo con pantallas de visualización de datos de los 4 programadores. | - Ratones verticales ergonómicos con pad de descanso de gel.<br>- Sillas con regulación neumática lumbar.<br>- Cumplimiento del régimen de pausas activas obligatorias (10 min cada 60 min). |
| **Ley N.º 24.051 y Ley N.º 25.675** | Régimen de Residuos Peligrosos y Ley General del Ambiente *(Nacional)* | Regula la generación, manipulación y disposición de sustancias peligrosas (metales pesados) y consagra la sustentabilidad ambiental. | Descarte y sustitución de hardware, fuentes, placas y periféricos dañados durante el proyecto. | - Prohibición de desecho de partes electrónicas en la basura domiciliaria.<br>- Protocolo formal de almacenamiento seguro y entrega en los **Puntos Verdes de CABA** para su tratamiento calificado como RAEE. |
| **Ley CABA N.º 1.854 y N.º 2.807** | Ley de Basura Cero y Régimen de Gestión de RAEE *(CABA)* | Fija la reducción progresiva de residuos con disposición final diferenciada y regula los aparatos eléctricos y electrónicos en CABA. | Residuos secos y electrónicos originados en el laboratorio escolar de la Comuna 1. | - Segregación en origen en tacho verde (papel, cartón, envoltorios secos) y caja plástica rotulada para rezagos de hardware. |
| **Ley N.º 24.240** | Ley de Defensa del Consumidor *(Nacional)* | Regula las relaciones de consumo, obligando a los proveedores a suministrar información cierta, clara y detallada. | Transparencia ante el usuario en los canales de financiamiento, compras y soporte del juego. | - Información transparente en la documentación: el juego es gratuito y no contiene microtransacciones ocultas obligatorias.<br>- Términos de donaciones claros, explicitando que los aportes son voluntarios y no otorgan ventajas desleales de juego. |
| **Licencia MIT** | *Massachusetts Institute of Technology Open Source License* | Estándar internacional de licenciamiento permisivo de código abierto reconocido por la OSI. | Marco contractual público que regula la distribución del repositorio en GitHub. | - Se incluye el archivo `LICENSE` en la raíz del repositorio.<br>- Otorga derecho a usar, copiar, modificar y distribuir el código, con cláusula explícita de **exención de responsabilidad civil y garantía** ante fallas operativas imprevistas. |

---

## 3. Justificación y Conclusiones del Análisis Normativo

El cumplimiento riguroso de esta matriz legal confiere al proyecto una sólida seguridad jurídica y operativa:
1. **Seguridad frente a Reclamos de Terceros:** La cláusula de exención de garantía de la Licencia MIT salvaguarda legalmente al equipo ante cualquier contingencia derivada del uso del simulador en sistemas de terceros.
2. **Cumplimiento Ético de Privacidad:** Al no recopilar telemetría intrusiva ni datos financieros en servidores externos, el proyecto cumple por diseño (*Privacy by Design*) con las directivas de la Agencia de Acceso a la Información Pública (AAIP) de Argentina.
3. **Resguardo de la Salud Integral y Cobertura ART:** La articulación de la Ley 19.587, el Decreto 351/79, la Ley 24.557 y la Resolución SRT 295/03 transforma la práctica escolar en un entorno formativo profesional de alto estándar, garantizando la prevención técnica y la cobertura médico-asistencial obligatoria frente a eventuales siniestros.
4. **Responsabilidad Ambiental Efectiva:** La sujeción a la Ley 24.051 y a la normativa de CABA asegura que ningún componente de hardware termine contaminando cursos hídricos o suelos urbanos.
