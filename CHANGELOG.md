# Changelog

Todos los cambios relevantes de este proyecto quedan documentados aquí.
Formato basado en [Keep a Changelog](https://keepachangelog.com/es/1.0.0/).

---

## [Unreleased]

---

## [3.0.0] — 2026-03-28

### Added
- Upload del Informe Anual de Boletas del SII (.xls) como fuente principal de datos
- Drag & drop + selección de archivo en la pestaña Ingresos
- Parser HTML-as-XLS: detecta año, extrae honorario bruto y retención de terceros por mes
- Detección automática de modo: año cerrado (análisis completo) vs año en curso (actuals + proyección)
- Grid visual de 12 meses con bruto mensual tras carga exitosa
- Badge "Tus datos nunca salen de tu browser"
- Instrucciones de 3 pasos con ruta correcta del SII para descargar el archivo
- Mensaje de error prominente junto a la zona de upload (con scroll automático)
- Fallback de ingreso manual mes a mes con toggle de retención por mes
- Archivo `.gitignore` (excluye CLAUDE.md, .DS_Store, archivos de prueba)

### Changed
- Modelo de datos: de `boletas[]` individual a `mesesActuales[12]` con `{bruto, retencion}` por mes
- Timeline chart: ahora muestra barras reales por mes en vez de promedio distribuido
- Pestaña Ingresos rediseñada completamente, inspirada en UX de Ahórratela

### Removed
- Ingreso manual boleta a boleta como flujo principal

---

## [2.0.0] — 2026-03-24

### Added
- Selector de año tributario (2024, 2025, 2026) con tramos SII correctos para cada año
- Escenarios de proyección: Pesimista −20% / Base / Optimista +20%
- Toggle Promedio mensual / Mes a mes
- Gráfico timeline de ingresos (actuals sólido, proyectados suave)
- Gráfico de barras apilado Sin APV vs Con APV
- Recomendaciones y alertas automáticas
- Cálculo de cotizaciones previsionales (17% sobre 80% de renta)

---

## [1.0.0] — 2026-03-24

### Added
- Versión inicial: calculadora tributaria standalone en HTML
- Ingreso manual de boletas con monto bruto y toggle retención
- Cálculo de impuesto por tramos SII
- APV Régimen A con bonus estatal 15%
