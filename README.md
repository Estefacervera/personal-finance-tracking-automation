# Seguimiento Automatizado de Presupuesto Personal 💰📊

Este proyecto integra automatización con **n8n**, procesamiento inteligente con **modelos de lenguaje**, y visualización en **Power BI** para llevar el control completo y en tiempo real de los movimientos financieros personales.

## 🚀 Objetivo

Construir una solución automatizada que registre todos los movimientos (ingresos y gastos) recibidos por correo electrónico desde Bancolombia, los clasifique inteligentemente en categorías financieras, y los visualice en Power BI para una mejor toma de decisiones personales.

---

## 🛠️ Tecnologías y herramientas

- **n8n**: Automatización de flujos de trabajo.
- **Gmail API**: Lectura de correos electrónicos.
- **OpenAI / GPT-4**: Clasificación inteligente de los movimientos financieros.
- **Google Sheets**: Base de datos dinámica.
- **Power BI**: Visualización de datos financieros.

---

## 🔁 Flujo Automatizado en n8n

1. **Detonador (Gmail)**: Escucha nuevos correos del remitente `alertasynotificaciones@notificacionesbancolombia.com`.
2. **Procesamiento de contenido**: Extrae y limpia el mensaje recibido.
3. **Clasificación con LLM**: Se envía el mensaje al modelo GPT para analizar:
   - Tipo de transacción (Ingreso, Gasto, Pago)
   - Medio de pago
   - Establecimiento
   - Valor del movimiento
   - Categoría de gasto (ej. Transporte, Hogar, Salud, Supermercado, etc.)
4. **Registro**: Se guarda la información estructurada en Google Sheets.
5. **Etiqueta el correo**: Para evitar reprocesamiento.
6. **Power BI**: Se conecta al Google Sheet para mostrar insights como:
   - Top de establecimientos
   - Categorías más costosas
   - Evolución de gastos por fecha
   - Medios de pago utilizados

---

## 📊 Dashboard en Power BI

El dashboard muestra:

- Gastos totales por categoría.
- Evolución diaria de los movimientos.
- Establecimientos donde más se gasta.
- Distribución de medios de pago.
- Filtros por fecha y categoría.


---

## 📂 Archivos del proyecto

| Archivo                        | Descripción                                        |
|-------------------------------|----------------------------------------------------|
| `Follow Financial.json`       | Flujo completo de n8n exportado.                   |
| `BudgetDashboard.pbix`        | Dashboard en Power BI.                             |
| `financial_data.xlsx`         | Datos estructurados extraídos automáticamente.     |

---

## 📌 Notas adicionales

- Se incluyen validaciones y alertas automáticas por correo en caso de error.
- Se etiqueta cada correo ya procesado.
- Puede adaptarse a otros bancos o métodos de ingreso de datos (como SMS, API, etc.)

---

## 📥 Cómo usar

1. Importar el flujo `Follow Financial.json` en n8n.
2. Conectar Gmail, OpenAI y Google Sheets.
3. Crear un Google Sheet con las columnas: Fecha, tipoTransaccion, medioPago, establecimiento, valor, categoria.
4. Abrir el archivo `.pbix` en Power BI y conectar con la hoja de cálculo.
5. Comenzar a recibir visualizaciones automáticas.

---

## 💡 Resultado

Este proyecto permite llevar control de tus finanzas personales sin intervención manual, automatizando desde la captura de datos hasta su visualización, y facilitando decisiones más informadas.

---

## 👩‍💻 Autor

**Estefanía Cervera** – [LinkedIn](https://www.linkedin.com/in/estefacervera)  
