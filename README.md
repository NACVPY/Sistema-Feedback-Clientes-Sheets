# 💬 Sistema Automatizado de Feedback e Incidencias de Clientes

## 📌 Descripción del Proyecto
Este proyecto desarrolla un **sistema centralizado de recepción, procesamiento y análisis de feedback de clientes** diseñado en Google Sheets para equipos de Operaciones y Soporte CRM.

El objetivo del proyecto es resolver la falta de visibilidad sobre la satisfacción del cliente ($CSAT$) mediante:
1. **Triaje y Clasificación Automatizada:** Filtrado dinámico de quejas e incidencias críticas sin manipulación manual de datos.
2. **Cuadro de Mando Interactivo:** Dashboard analítico con KPIs ejecutivos y controles de filtro en tiempo real para la toma de decisiones por departamento.

---

## 🛠️ Funcionalidades y Técnicas Utilizadas

- **Procesamiento de Datos con SQL en Sheets (`QUERY`):** Implementación de la función `=QUERY()` con sintaxis SQL (`SELECT`, `WHERE`, `ORDER BY`, funciones de texto `LOWER` y patrones `LIKE`) para la extracción y ordenación automática de incidencias según gravedad.
- **Indicadores Clave de Rendimiento (KPIs):** Cálculo de métricas ejecutivas globales mediante `=CONTARA()`, `=CONTAR.SI()` y `=PROMEDIO()` para evaluar el nivel de satisfacción ($CSAT$) e incidencias abiertas.
- **Segmentación Dinámica de Datos (Slicers):** Integración de un **Control de Filtro** interactivo vinculado a la base de datos centralizada para habilitar vistas personalizadas por tipo de feedback y estado del ticket.
- **Modelado de Datos Relacional:** Estructura limpia basada en separación de capas (Datos Crudos ➔ Capa de Procesamiento ➔ Capa de Presentación/Dashboard).

---

## 📂 Estructura del Libro de Trabajo

1. **`01_Respuestas_Form` (Entrada de Datos):** Registro histórico transaccional de tickets recibidos (ID, Cliente, Tipo de Feedback, Departamento, Puntuación CSAT y Estado).
2. **`02_Analisis_Query` (Motor de Procesamiento):** Vista automatizada donde la función `QUERY` filtra en tiempo real las quejas de clientes ordenadas por puntuación ascendente para atención prioritaria.
3. **`03_Dashboard` (Panel Ejecutivo):** Resumen analítico interactivo con métricas clave, tabla dinámica por departamento y control de filtro desplegable.

---

## 📊 Principales Hallazgos (Insights)

- **Distribución de Quejas:** Las incidencias por servicio se encuentran distribuidas de forma crítica en **Logística** (50% de las quejas registradas) y **Soporte Técnico**.
- **Atención Prioritaria:** Las quejas de los clientes *Marcos Peña* y *David Gil* registraron la puntuación mínima de satisfacción ($CSAT = 1$), requiriendo intervención inmediata del equipo de operaciones.
- **Eficiencia Operativa:** La automatización mediante `QUERY` elimina el trabajo repetitivo de filtrado manual, permitiendo responder a las incidencias críticas en minutos.

---

## 🚀 Cómo Utilizar este Repositorio

1. Descarga el archivo de hoja de cálculo adjunto o haz una copia en tu Google Drive.
2. Navega a la pestaña `03_Dashboard`.
3. Utiliza el **Control de Filtro** superior para alternar la visualización según el tipo de feedback (*Queja*, *Felicitación*, *Sugerencia*).
