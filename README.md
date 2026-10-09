# Tarea 3 – Econometría Financiera (FZ4038)

**Maestría en Finanzas, EGADE Business School, Tecnológico de Monterrey**
Profesor: Dr. Raymundo Díaz Robles
Alumno: Daniel Mondragón Monroy (A01452205)
Fecha de entrega: 9 de octubre de 2026

## Descripción

Estimación de tres modelos de regresión lineal múltiple con cinco variables independientes cada uno, usando rendimientos de 30 minutos descargados de LSEG Workspace (1 de julio al 7 de octubre de 2026, 828 observaciones por modelo):

- **mt301 / mt301b:** Exxon Mobil (XOM) en función de Chevron, ConocoPhillips, XLE, USO y SPY. El modelo final (mt301b) excluye XLE por multicolinealidad.
- **mt302:** JPMorgan (JPM) en función de Bank of America, Goldman Sachs, TLT, Citigroup y SPY.
- **mt303:** Apple (AAPL) en función de Microsoft, Nvidia, SPY, TSMC y TLT.

La tarea incluye la detección y corrección de violaciones de supuestos (VIF, Breusch-Pagan, Goldfeld-Quandt, Durbin-Watson, Breusch-Godfrey, Jarque-Bera y errores estándar de Newey-West), la revisión de los modelos con TecGPT, el rebalanceo del portafolio en HowMarketsWork y las preguntas 12.1 a 12.3 del capítulo 12 de Gujarati.

## Archivos

| Archivo | Contenido |
|---|---|
| `Tarea3_A01452205_FZ4038.Rmd` | Código fuente en R Markdown con el análisis completo (Partes 1 a 5). |
| `Tarea3_A01452205_FZ4038.html` | Documento final generado a partir del Rmd (Knit). |
| `Tarea3_A01452205_datosLSEG.xlsx` | Precios de cierre de 30 minutos de LSEG Workspace. La hoja `30min` contiene las fórmulas de descarga y la hoja `30min_valores` los valores que lee el Rmd. |
| `Tarea3_A01452205_FZ4038_Anexo_TecGPT.pdf` | Anexo con la conversación completa con TecGPT (Parte 3). |
| `hmw_posiciones_antes.png` | Posiciones del portafolio en HowMarketsWork antes del rebalanceo. |
| `hmw_limite_25.png` | Aviso del límite de 25% por posición en HowMarketsWork. |
| `hmw_ordenes_tarea3.png` | Órdenes del rebalanceo colocadas antes de su ejecución. |
| `hmw_posiciones_despues.png` | Posiciones del portafolio después del rebalanceo. |

## Cómo reproducir el análisis

1. Descargar todos los archivos en una misma carpeta (el Rmd lee el xlsx y las imágenes desde la carpeta en la que se encuentra).
2. Abrir `Tarea3_A01452205_FZ4038.Rmd` en RStudio o Posit Cloud.
3. Instalar los paquetes necesarios, si no están instalados:
   `install.packages(c("readxl", "quantmod", "car", "lmtest", "tseries", "sandwich"))`
4. Ejecutar Knit para generar el HTML.
