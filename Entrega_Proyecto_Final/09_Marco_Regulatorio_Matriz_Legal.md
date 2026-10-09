# SECCIÓN 9: MARCO REGULATORIO Y MATRIZ LEGAL APLICABLE

---

## 1. Fundamentación del Marco Regulatorio

Todo emprendimiento de base tecnológica e industrial debe encuadrarse de forma estricta dentro del marco normativo vigente del territorio donde opera. 

Para *AquaByte Development Studio*, el desarrollo y explotación del sistema de simulación en Ruby requiere el cumplimiento simultáneo de legislaciones en materia de **propiedad intelectual**, **privacidad y seguridad de datos**, **condiciones laborales y ergonomía**, **protección ambiental y residuos**, y **derechos del consumidor**, conforme a las leyes de la República Argentina y la normativa jurisdiccional de la Ciudad Autónoma de Buenos Aires.

---

## 2. Matriz Legal Integral del Proyecto

### Tabla 7: Matriz de Cumplimiento Legal y Normativo en la República Argentina

| Norma / Ley | Denominación Oficial y Jurisdicción | Objeto y Alcance Jurídico | Aplicación Concreta al Proyecto | Mecanismo y Modo de Cumplimiento en el Software |
|---|---|---|---|---|
| **Ley N.º 11.723** | Régimen Legal de la Propiedad Intelectual *(República Argentina)* | Ampara las obras científicas, literarias y artísticas. Asimila expresamente el **software y código fuente** a obras protegidas (Dec. 165/94). | Protección de la autoría sobre el código en Ruby, mecánicas del simulador y diseño de clases. | - Declaración expresa de autoría de los cuatro integrantes.<br>- Adopción de la **Licencia de Código Abierto MIT** adjunta al repositorio, permitiendo uso y estudio libre pero protegiendo los derechos morales de los autores.<br>- Registro opcional de obra inédita ante la DNDA. |
| **Ley N.º 25.326** | Ley de Protección de los Datos Personales *(Habeas Data)* | Garantiza el honor e intimidad de las personas y el tratamiento legítimo de datos personales asentados en archivos o bancos de datos. | Gestión de perfiles de usuario, nombres de jugador, donaciones y registros de partidas en `/Data`. | - Principio de finalidad: únicamente se almacenan apodos locales de juego sin solicitar datos sensibles (DNI, tarjetas o correos).<br>- Almacenamiento local descentralizado (en la PC del propio usuario).<br>- Cero transferencia de datos a terceras partes. |
| **Ley N.º 19.587 y Res. SRT 295/03** | Ley de Higiene y Seguridad Laboral / Anexo Ergonomía | Fija pautas psicofísicas de trabajo seguro y límites de esfuerzo repetitivo en miembros superiores para puestos con PVD. | Puestos de trabajo de los desarrolladores durante las jornadas de programación y testing. | - Provisión de puestos ergonómicos regulables y mouses verticales.<br>- Cumplimiento del régimen de pausas activas obligatorias (10 min/hora).<br>- Iluminación calibrada a 500 lux y cableado bajo canaletas seguras. |
| **Ley N.º 24.051 y Ley N.º 25.675** | Régimen de Residuos Peligrosos y Ley General del Ambiente | Regula la generación, manipulación y disposición de sustancias peligrosas (metales pesados) y consagra la sustentabilidad ambiental. | Descarte y sustitución de hardware, fuentes, placas y periféricos dañados durante el proyecto. | - Prohibición de desecho de partes electrónicas en la basura domiciliaria.<br>- Protocolo formal de almacenamiento seguro y entrega en los **Puntos Verdes de CABA** para su tratamiento calificado como RAEE. |
| **Ley N.º 24.240** | Ley de Defensa del Consumidor | Regula las relaciones de consumo, obligando a los proveedores a suministrar información cierta, clara y detallada. | Transparencia ante el usuario en los canales de financiamiento, compras y soporte del juego. | - Información transparente en la documentación: el juego es gratuito y no contiene microtransacciones ocultas obligatorias.<br>- Términos de donaciones claros, explicitando que los aportes son voluntarios y no otorgan ventajas desleales de juego. |
| **Licencia MIT** | *Massachusetts Institute of Technology Open Source License* | Estándar internacional de licenciamiento permisivo de código abierto reconocido por la OSI. | Marco contractual público que regula la distribución del repositorio en GitHub. | - Se incluye el archivo `LICENSE` en la raíz del repositorio.<br>- Otorga derecho a usar, copiar, modificar y distribuir el código, con cláusula explícita de **exención de responsabilidad civil y garantía** ante fallas operativas imprevistas. |

---

## 3. Justificación y Conclusiones del Análisis Normativo

El cumplimiento riguroso de esta matriz legal confiere al proyecto una sólida seguridad jurídica y operativa:
1. **Seguridad frente a Reclamos de Terceros:** La cláusula de exención de garantía de la Licencia MIT salvaguarda legalmente al equipo ante cualquier contingencia derivada del uso del simulador en sistemas de terceros.
2. **Cumplimiento Ético de Privacidad:** Al no recopilar telemetría intrusiva ni datos financieros en servidores externos, el proyecto cumple por diseño (*Privacy by Design*) con las directivas de la Agencia de Acceso a la Información Pública (AAIP) de Argentina.
3. **Resguardo de la Salud Técnica:** La aplicación de la normativa de ergonomía laboral (Res. SRT 295/03) transforma la práctica escolar en un entorno formativo profesional de alto estándar.
