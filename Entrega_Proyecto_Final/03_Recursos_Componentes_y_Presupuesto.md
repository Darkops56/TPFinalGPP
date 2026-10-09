# SECCIÓN 3: RECURSOS, COMPONENTES TÉCNICOS Y PRESUPUESTO ESTIMADO

---

## 1. Materiales y Componentes Técnicos

Para llevar a cabo el ciclo completo de desarrollo, verificación y despliegue del software, se seleccionó un conjunto de recursos tecnológicos basados en la maximización de la eficiencia y el uso estratégico de herramientas de código abierto (*Open Source*).

### A. Componentes de Hardware
* **Estaciones de Desarrollo (x4):** Equipos informáticos tipo PC de escritorio / portátiles con microprocesadores Intel Core i5 / AMD Ryzen 5 o superior, memoria RAM de 16 GB DDR4 y unidades de estado sólido (SSD NVMe) de 512 GB para compilación e indexación ágil.
* **Periféricos de Interacción Ergonómica:** Teclados mecánicos con switches táctiles de bajo esfuerzo, ratones ergonómicos verticales con apoyamuñecas de gel y monitores LED IPS de 24 pulgadas con soporte regulable en altura e inclinación.
* **Infraestructura de Red y Servidor Local:** Switch Gigabit Ethernet de 8 puertos, cableado UTP Categoría 6 con conectores RJ-45 apantallados y router Wi-Fi doble banda (2.4 GHz / 5.0 GHz) con protección contra sobretensiones.
* **Suministro Eléctrico Estabilizado:** Unidad de Alimentación Ininterrumpida (UPS) de 1000 VA con supresor de picos térmicos para preservar la integridad de los datos ante cortes de energía o variaciones de tensión.

### B. Componentes de Software y Entorno Tecnológico
* **Sistema Operativo:** Distribución Linux (Ubuntu 22.04 LTS / Debian 12) y estaciones secundarias Windows 11 con WSL2 (Windows Subsystem for Linux), garantizando paridad entre entornos de desarrollo y producción.
* **Entorno de Ejecución:** Lenguaje de programación **Ruby versión 3.2.x**, instalado mediante gestor de versiones `rbenv` o `rvm`.
* **Gestor de Paquetes y Dependencias:** `Bundler` para la resolución y congelamiento determinístico de librerías mediante el archivo `Gemfile.lock`.
* **Framework de Testing Automatizado:** `RSpec` (versión 3.12+) para pruebas unitarias dirigidas por comportamiento (BDD/TDD).
* **Herramientas de Aseguramiento de Calidad y Linteo:** `RuboCop` para la imposición de estándares de estilo y `Bundler-Audit` para detección de vulnerabilidades conocidas (CVE) en gemas.
* **Sistema de Control de Versiones:** `Git` (versión 2.40+) con integración continua en repositorio remoto alojado en `GitHub`.
* **Entorno de Desarrollo Integrado (IDE):** `Visual Studio Code` con extensiones oficiales para Ruby, Ruby LSP y GitLens.

---

## 2. Presupuesto Económico Detallado del Proyecto

Para determinar la viabilidad comercial y el costo real de producción del software bajo condiciones de mercado profesional en la República Argentina, se confeccionó el siguiente presupuesto integral. Se distinguen los costos de inversión en activos fijos (CAPEX), gastos de mano de obra técnica calificada y costos operativos recurrentes (OPEX).

*Moneda de curso legal: Pesos Argentinos (ARS) — Estimación basada en costos de mercado y valores de referencia para el sector informático en CABA.*

### Tabla 1: Cuadro General de Presupuesto y Estructura de Costos

| Rubro / Categoría | Descripción Detallada | Cantidad | Costo Unitario (ARS) | Costo Subtotal (ARS) | Tipo de Gasto |
|---|---|:---:|:---:|:---:|:---:|
| **Hardware** | Estaciones de trabajo informático (Amortización mensual sobre 4 PCs) | 4 equipos | $ 200.000 / mes | $ 800.000 | CAPEX / Amort. |
| **Hardware** | UPS de 1000 VA estabilizada y regletas térmicas | 2 unidades | $ 180.000 | $ 360.000 | CAPEX |
| **Hardware** | Switch 8 bocas GbE + Cableado estructurado Cat 6 | 1 kit | $ 90.000 | $ 90.000 | CAPEX |
| **Software** | Entorno de desarrollo (Ruby, VS Code, Git, Linux) | 4 licencias | $ 0 (Open Source) | $ 0 | Gratuito |
| **Software / Cloud** | GitHub Team / Actions CI / Hosting de repositorios | 1 año | $ 60.000 | $ 60.000 | OPEX |
| **Mano de Obra (RRHH)** | Horas de desarrollo y QA (4 devs x 80 hs totales c/u = 320 hs) | 320 hs | $ 8.500 / h | $ 2.720.000 | Directo RRHH |
| **Conectividad** | Acceso a Internet banda ancha simétrica (300 Mbps) | 2 meses | $ 35.000 / mes | $ 70.000 | OPEX |
| **Energía Eléctrica** | Consumo eléctrico del laboratorio (Tarifa T1 Comercial CABA) | 2 meses | $ 45.000 / mes | $ 90.000 | OPEX |
| **Higiene y EPP** | Lentes antirreflejo luz azul, pads ergonómicos y pulseras antiestáticas | 4 kits | $ 35.000 / kit | $ 140.000 | Inversión SySO |
| **Seguridad Edilicia** | Matafuegos de CO2 (5 kg, Clase B-C) para equipos eléctricos | 1 unidad | $ 120.000 | $ 120.000 | Inversión SySO |
| **Contingencias** | Fondo de reserva imprevistos técnicos / reposición (5%) | Estimado | $ 225.000 | $ 225.000 | Imprevistos |
| **TOTAL GENERAL ESTIMADO** | | | | **$ 4.675.000** | **Costo Integral** |

---

## 3. Justificación Económica y Punto de Equilibrio

1. **Eficiencia por adopción de Open Source:**  
   La elección de Ruby y herramientas comunitarias representó un ahorro directo estimado en más de **$ 1.500.000 ARS** en licencias privativas de sistemas operativos comerciales y suites propietarias de testing.
2. **Estructura del Costo por Hora Técnica:**  
   La tarifa horaria adoptada ($ 8.500 ARS/hora) se ubica en el segmento inicial/junior de desarrollo de software en Argentina, garantizando que el costo de mano de obra represente el **58,1%** del presupuesto global, cifra alineada con los parámetros estándares de la industria del software.
3. **Punto de Equilibrio (Break-Even) y Retorno de Inversión:**  
   En caso de comercializarse el simulador bajo un modelo freemium o de compra única en plataformas independientes (como itch.io o Steam Indie) a un valor de $ 5.000 ARS por copia, el punto de equilibrio se alcanzaría comercializando aproximadamente **935 licencias**, lo que confirma la viabilidad económica y comercial del proyecto.
