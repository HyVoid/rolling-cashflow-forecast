[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)

# Plantilla Excel de Pronóstico de Flujo de Caja Rodante de 16 Semanas: Planificador de Liquidez por Método Directo, Rastreador de Compromisos de PO y Modelo de Capital de Trabajo

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Focus](https://img.shields.io/badge/focus-Working%20Capital%20%26%20Treasury-orange)

**Una hoja de cálculo de pronóstico de flujo de caja rodante de 16 semanas por método directo, construida en Microsoft Excel para empresas mayoristas, de importación/exportación, de inventario de comercio electrónico y manufactureras que gestionan pedidos de compra (PO) abiertos, prepagos a proveedores, depósitos de clientes y capital de trabajo a corto plazo.**

[Lanzar la Demostración Interactiva del Simulador de Flujo de Caja Rodante de 16 Semanas](https://hyvoid.github.io/rolling-cashflow-forecast/) ·

[Descargar el Libro de Excel Completo de Flujo de Caja Rodante de 16 Semanas](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

</div>

**El Libro de Trabajo de Pronóstico de Flujo de Caja Rodante de 16 Semanas** es un **planificador de liquidez a corto plazo en Microsoft Excel** automatizado y un **rastreador de compromisos de efectivo abiertos**. Ampliando los **modelos estándar de flujo de caja de 13 semanas** para cubrir plazos completos de inventario y producción de 110 días, consolida las **Cuentas por Cobrar (AR)**, las **Cuentas por Pagar (AP)**, los **Pedidos de Venta (SO) no facturados** y los **Pedidos de Compra (PO) comprometidos** en una única línea de tiempo semanal de efectivo, señalando faltantes de capital de trabajo e infracciones del colchón mínimo de caja semanas antes de las fechas de vencimiento de los pagos.

---

## Vista Previa Visual: Panel de Línea de Tiempo de Caja de 16 Semanas y Alertas de Umbral

<img width="1672" height="941" alt="16-Week Rolling Cash Flow Forecast Excel Template showing weekly cash inflows, supplier PO prepayments, net liquidity balance, and shortfall alerts" src="https://github.com/user-attachments/assets/d43699bc-4a15-470c-901e-7b372c953861" />

> Pruebe el mapeo semanal de compromisos y las alertas de umbral de liquidez en su navegador: [Demostración Interactiva del Pronóstico de Flujo de Caja por Método Directo de 16 Semanas](https://hyvoid.github.io/rolling-cashflow-forecast/)

---

## Por Qué la Contabilidad de Devengo No Logra Prevenir los Faltantes de Caja a Corto Plazo

Las empresas mayoristas, manufactureras y de productos físicos rentables experimentan rutinariamente apremios agudos de liquidez durante las fases de crecimiento. Estos faltantes de caja ocurren porque los **depósitos de clientes**, las **facturaciones de progreso por hitos**, los **prepagos contratados a proveedores** y las **condiciones de pago escalonadas Net 30/60/90** ocurren semanas antes de que una factura contable alguna vez se registre en el libro mayor.

**El Flujo de Trabajo Reactivo de Saldo Bancario y AR/AP (Alto Riesgo de Impago):**

```text
Supplier wire due date arrives
-> Finance checks current bank balance and billed AP aging
-> Unbilled PO prepayments and freight commitments overlooked
-> Working capital shortfall discovered 48 hours before wire deadline

```

**El Flujo de Trabajo Proactivo de Pronóstico de Compromisos de 16 Semanas (Control Previo a la Decisión):**

```text
New customer order or supplier Purchase Order (PO) proposed
-> Prepayment and balance milestones logged once in the commitment ledger
-> 16-week rolling cash flow timeline updates automatically
-> Liquidity gap and minimum buffer breach flagged 6–12 weeks in advance

```

Los gerentes de finanzas, los controladores y los líderes de operaciones necesitan visibilidad de liquidez previa a la decisión. Antes de firmar un pedido de compra a un proveedor o de otorgar condiciones Net 60 a un comprador mayorista, los operadores deben verificar que el valle de caja semanal se mantenga por encima de la reserva mínima de caja operativa de la empresa.

---

## La Lógica de Negocio y la Metodología: Pronóstico de Compromisos por Método Directo

Este libro de trabajo resuelve el **problema de ceguera de capital de trabajo previo a la factura** combinando el **Pronóstico Rodante de Flujo de Caja por Método Directo** con la **Deduplicación de Compromisos de Pedido a Factura**.

### El Problema Comercial: La Brecha de Temporización entre Devengo y Efectivo en las Cadenas de Suministro Físicas

El software contable estándar (QuickBooks, Xero, NetSuite GL) reconoce los eventos financieros solo cuando se emite una **Factura** o un **Bill**. Sin embargo, en la manufactura, la distribución mayorista y las operaciones de importación, el efectivo queda legalmente comprometido en la **Capa de Pedido**:

1. **Salidas de Efectivo de Aprovisionamiento:** Una fábrica requiere un depósito del 30% al emitir el Pedido de Compra (PO) y un saldo del 70% contra el conocimiento de embarque (B/L) o la llegada al almacén, semanas antes de que se registre una factura de proveedor formal en AP.
2. **Entradas de Efectivo de Ventas:** Un cliente B2B paga un depósito del 25% al confirmar el Pedido de Venta (SO) y el 75% restante antes del envío o en condiciones Net 30/60 después de la entrega.
3. **Por Qué 16 Semanas Superan a los Modelos Estándar de 13 Semanas:** Un pronóstico corporativo estándar de 13 semanas (90 días) se corta justo antes de que se liquiden un ciclo de producción de 60 días más un tránsito oceánico de 30 días más una cobranza de cliente Net 30. Ampliar la ventana rodante a **16 semanas (112 días)** captura todo el ciclo de conversión de efectivo desde el depósito inicial del PO hasta la cobranza final del cliente.

### La Metodología Central: Mapeo Determinista de Caja en Tres Etapas

En lugar de proyectar el efectivo a partir de promedios generales del estado de resultados, el libro de trabajo ejecuta un cálculo determinista de tres etapas a lo largo de una ventana deslizante de 16 semanas ($t \in [1, 16]$):

1. **Motor de Deduplicación de Compromiso a Factura:**

$$\text{Active Cash Events} = \{ \text{Billed AR} \} \cup \{ \text{Billed AP} \} \cup \{ \text{Open SOs} \setminus \text{Invoiced SOs} \} \cup \{ \text{Open POs} \setminus \text{Billed POs} \}$$



*Efecto Comercial:* Una vez que un Pedido de Compra se convierte en una factura de proveedor formal en su sistema contable, la bandera de deduplicación excluye la línea original del PO para que la salida de efectivo nunca se cuente dos veces.
2. **Traducción de Compensación de Fechas por Hitos:**
Cada compromiso activo se descompone en tramos discretos de efectivo (p. ej., Tramo de Depósito + Tramo de Saldo) mapeados a semanas calendario objetivo según fechas operativas de activación (Fecha de Pedido, Fecha de Envío Estimada, Fecha de Llegada Estimada o Fecha de Factura) más las condiciones de pago contratadas ($\Delta \text{Days}$).
3. **Evaluación Rodante de Liquidez Semanal e Infracciones del Colchón:**

$$\text{Ending Cash}_{w} = \text{Opening Cash}_{w} + \sum \text{Committed Inflows}_{w} - \sum \text{Committed Outflows}_{w}$$


$$\text{Liquidity Variance}_{w} = \text{Ending Cash}_{w} - \text{Minimum Safe Cash Threshold}$$



*Efecto Comercial:* Cualquier semana en la que $\text{Ending Cash}_{w} < \text{Minimum Safe Cash Threshold}$ activa una alerta visual inmediata y aísla el PO exacto o la partida de AR retrasada que causa el valle de capital de trabajo.

---

## Tres Trampas de Capital de Trabajo en las Hojas de Cálculo Manuales de Flujo de Caja

### Trampa 1: Confiar en el Estado de Resultados Mensual y los Informes de Antigüedad de AR/AP Facturados para la Liquidez

Los informes estándar de antigüedad de Cuentas por Cobrar y Cuentas por Pagar solo muestran las **transacciones facturadas**.

Considere un importador que tiene $80,000 en depósitos de pedidos de clientes no facturados y enfrenta $60,000 en pagos de saldo contratados a la fábrica al llegar el contenedor el próximo mes. Ninguna de las dos obligaciones aparece en el estado de resultados ni en el informe estándar de antigüedad de AP hasta que el inventario llega y se registran las facturas de proveedores. Gestionar la tesorería semanal a partir de estados de devengo mensuales deja al equipo de finanzas con cuatro a seis semanas de retraso respecto a los compromisos reales de efectivo.

### Trampa 2: Rastreo Aislado entre Pedidos de Venta (CRM) y Pedidos de Compra (Aprovisionamiento)

Cuando el equipo de ventas acepta un depósito de cliente del 30% el lunes y el equipo de compras compromete un prepago a proveedor del 40% el jueves, ambas acciones provienen de la misma cuenta bancaria operativa. Sin embargo, en la mayoría de las pymes, los compromisos de ventas viven en un CRM o una hoja de pedidos, mientras que los PO de proveedores viven en un rastreador de aprovisionamiento separado.

Mantener hojas de cálculo desconectadas para las entradas de clientes y las salidas a proveedores impide a los operadores ver la **posición neta de caja semanal** cuando las fechas de cumplimiento se retrasan aunque sea una semana.

### Trampa 3: Valles de Caja Intramensuales Ocultos Dentro de Totales Mensuales Positivos

Un resumen mensual de flujo de caja puede mostrar un saldo neto de caja saludable y positivo al cierre del mes mientras oculta un sobregiro fatal de varios días en la Semana 2 o la Semana 3.

Los faltantes de caja semanales surgen del desfase de temporización entre seis variables operativas:

* Saldo bancario operativo de apertura
* Fechas de recepción de depósitos de clientes e hitos
* Condiciones de cobranza del saldo final del cliente (p. ej., Antes del Envío vs. Net 30)
* Fechas de prepago de PO de proveedores y de transferencia contra llegada de mercancía
* Desembolsos de flete, aranceles y despacho aduanero
* Aceleración del volumen de pedidos durante las construcciones de temporada alta

Mapear cada compromiso a un intervalo específico de 7 días expone los valles de caja intramensuales mientras aún se dispone de 6 a 10 semanas para negociar condiciones con proveedores, acelerar cobranzas de clientes o echar mano de una línea de crédito renovable.

---

## Para Quién Es Esta Plantilla Excel de Flujo de Caja Rodante de 16 Semanas

Diseñada para equipos de finanzas operativas y propietarios de negocios que necesitan **pronóstico de tesorería por método directo dentro de Microsoft Excel** sin los costos de software TMS empresarial:

| Rol y Perfil de Búsqueda | Escenario Operativo Específico y Caso de Uso de la Plantilla |
| --- | --- |
| **Gerentes de Finanzas y Controladores** *(Plantilla Excel de Pronóstico de Flujo de Caja de 16 Semanas / 13 Semanas)* | Reemplace las conciliaciones bancarias manuales de los viernes con un pronóstico rodante de liquidez por método directo de 16 semanas que señala infracciones del colchón de caja con 6–12 semanas de anticipación. |
| **Directores de Cadena de Suministro y Operaciones** *(Flujo de Caja de Pedidos de Compra y Rastreador de Prepagos)* | Simule el impacto semanal exacto en caja de colocar un PO estacional grande a la fábrica o de retrasar una fecha de envío antes de firmar contratos con proveedores. |
| **Fundadores y CEOs con Mucho Inventario** *(Hoja de Cálculo de Capital de Trabajo y Pronóstico de Runway)* | Mantenga un único panel prospectivo de liquidez operativa neta durante la expansión rápida de SKU, el cumplimiento mayorista y los ciclos de construcción de inventario. |
| **Líderes de Aprovisionamiento y Compras** *(Planificador de Depósitos a Proveedores y Condiciones de Pago)* | Evalúe las exigencias de prepago de proveedores (p. ej., esquema 30/70 vs. 50/50) frente a la disponibilidad semanal de caja proyectada real. |
| **CFOs Externos y CPAs de Asesoría** *(Modelo de Caja de Tesorería a Corto Plazo y de Reestructuración)* | Despliegue una herramienta estandarizada y lista para auditoría de control semanal de flujo de caja para clientes pyme que enfrentan capital de trabajo ajustado o convenios de reporte con prestamistas. |

---

## Casos de Uso Reales: Resolución de Escenarios de Capital de Trabajo y Liquidez Previos a la Factura

### Escenario A: Importadores/Exportadores y Distribuidores Mayoristas que Gestionan Prepagos a Fábrica 30/70

Los importadores pagan rutinariamente 30% al colocar el PO y 70% contra conocimiento de embarque o llegada al puerto, mientras que los compradores minoristas mayoristas pagan Net 30 o Net 60 después de la entrega en el almacén. Al registrar los PO abiertos y los SO mayoristas en la **Línea de Tiempo de Caja de 16 Semanas**, el controlador ve el valle exacto de capital de trabajo de 4 a 8 semanas entre pagar a la fábrica en el extranjero y cobrar al minorista nacional.

### Escenario B: Manufactureros por Contrato y Fabricantes de Equipos a Medida que Rastrean la Facturación por Hitos

Los manufactureros que ejecutan construcciones multi-etapa cobran pagos de progreso del cliente (p. ej., 40% de depósito, 30% en el subensamblaje, 30% antes del despacho) mientras compran materias primas por adelantado. Cuando un hito de producción se retrasa dos semanas, actualizar la fecha de envío estimada en el libro de trabajo desplaza automáticamente la entrada de caja del cliente aguas abajo y revela si las cuentas por pagar de materias primas infringirán la reserva mínima de caja.

### Escenario C: CFOs Externos que Dirigen Salas de Guerra de Caja Semanales y Reportes de Convenios con Prestamistas

Durante reestructuraciones de capital de trabajo o disponimientos estacionales de líneas de crédito, los bancos y los equipos directivos requieren un pronóstico semanal directo de caja transparente (a menudo solicitado como un reporte rodante de flujo de caja de 13 o 16 semanas). Esta plantilla proporciona desgloses a nivel de transacción que muestran exactamente qué facturas de clientes y qué PO de proveedores impulsan el flujo de caja neto de cada semana.

---

## Qué Rastrea el Libro de Trabajo: Mapeo de Punto de Dolor a Solución

| Punto de Dolor de Tesorería y Gestión de Caja | Requisito de Búsqueda de Alta Frecuencia | Solución Integrada del Libro de Excel |
| --- | --- | --- |
| **POs No Facturados Ausentes en los Pronósticos de Caja** | *Cómo incluir pedidos de compra abiertos en un pronóstico de flujo de caja en Excel* | **Registro Unificado de Compromisos Abiertos:** Captura el AR facturado, el AP facturado, los Pedidos de Venta no facturados y los Pedidos de Compra abiertos en una única tabla de entrada estructurada. |
| **Doble Conteo de POs Después de la Facturación** | *Prevenir entradas duplicadas de PO y factura en la proyección de caja* | **Deduplicación Automatizada de PO a Factura:** Identifica y excluye los pedidos de compra que ya se convirtieron en facturas formales de AP para que cada dólar se cuente una sola vez. |
| **Sobregiros Intramensuales y Faltantes Sorpresa** | *Plantilla de pronóstico rodante de flujo de caja semanal con alertas de caja baja* | **Capa de Alertas de Umbral Configurable:** Compara el cierre de caja semanal proyectado con su Saldo Mínimo Seguro de Caja personalizado y resalta las semanas de infracción en tiempo real. |
| **Estimaciones de Envío y Entrega Obsoletas** | *Modelo dinámico de flujo de caja basado en fechas de envío y condiciones de pago* | **Mapeo Automatizado de Condiciones a Semanas:** Traduce fechas operativas (Fecha de Envío Estimada, Fecha de Llegada, Fecha de Factura) y condiciones de pago en intervalos semanales exactos de caja. |
| **Verificaciones Lentas de Aprobación Previas al Compromiso** | *Probar el impacto en caja de un nuevo PO de proveedor antes de comprar* | **Caja de Arena de Liquidez Previa a la Decisión:** Ingrese un PO propuesto o un pedido de cliente para ver de inmediato si el nuevo compromiso crea un déficit de caja a 6–16 semanas. |

---

## Estudio de Caso: Ceguera de Devengo Mensual vs. Visibilidad Rodante de Caja de 16 Semanas

**Perfil del Negocio:** Importador de bienes de consumo que gestiona entre $2M y $10M de facturación anual, operando con condiciones mixtas de depósito de clientes, calendarios de prepago a proveedores en el extranjero y un equipo financiero reducido de un solo gerente.

**El Colapso Operativo:** Cada semana, el gerente de finanzas dedicaba dos horas a cruzar referencias entre los pedidos de venta del CRM, los recibos de depósitos de clientes, los PO de fábrica abiertos y los calendarios de llegada de fletes en hojas de cálculo desconectadas. A pesar de mostrar un flujo de caja neto mensual positivo sobre el papel, el negocio sufrió dos faltantes de caja de emergencia en un solo trimestre, ambos descubiertos menos de 48 horas antes del vencimiento de las transferencias internacionales a proveedores.

### Comparación: Hojas de Cálculo AR/AP Desconectadas vs. Modelo Automatizado de Compromisos de 16 Semanas

| Operación de Tesorería | Hojas de Cálculo Manuales Desconectadas (Antes) | Libro de Trabajo Automatizado de Flujo de Caja Rodante de 16 Semanas (Después) |
| --- | --- | --- |
| **Arquitectura de Datos de Compromisos** | Hojas de ventas del CRM aisladas, rastreadores de PO de aprovisionamiento y exportaciones contables de AR/AP | **Registro único unificado de compromisos** que cubre AR, AP, SOs abiertos y POs abiertos con deduplicación |
| **Tiempo de Preparación del Pronóstico Semanal** | ~2 horas de VLOOKUPs manuales y referencias cruzadas de fechas cada viernes | **Menos de 5 minutos por semana**; la ventana rodante de 16 semanas se actualiza dinámicamente al ingresar las fechas |
| **Visibilidad de Prepagos Previos a la Factura** | Ciego a los depósitos a proveedores y a los saldos por hitos hasta que se registran las facturas de proveedores | **Mapeo completo de hitos** a lo largo de tramos de depósito, pagos previos al envío y transferencias de entrega |
| **Ventana de Detección de Faltantes de Liquidez** | Descubierto 24–48 horas antes de la fecha de vencimiento de la transferencia (disponimientos de crédito de emergencia forzados) | **Señalado con 6–12 semanas de anticipación** mediante alertas automatizadas de infracción del umbral mínimo de caja |

### El Punto de Inflexión Exacto que Este Libro de Trabajo Saca a la Luz

Considere un **Pedido de Venta de Cliente de $100,000** y su **Pedido de Compra a Proveedor de $50,000** vinculado, partiendo de un **Saldo de Caja de Apertura de $10,000**:

* **Saldo del PO de Proveedor ($30,000 de salida):** 60% pagadero a la llegada de la mercancía en la **Semana 5**.
* **Saldo del SO de Cliente ($70,000 de entrada):** 70% pagadero antes del despacho del almacén en la **Semana 6**.

| Granularidad de Reporte | Posición Neta de Caja de la Semana 5 | Posición Neta de Caja de la Semana 6 | Conclusión Operativa |
| --- | --- | --- | --- |
| **Resumen Mensual Tradicional de Caja** | *Oculto dentro del total mensual* | **+$50,000 de Caja al Cierre del Mes** | Luz verde falsa; finanzas aprueba las condiciones sin ver el impago de mitad de mes |
| **Modelo Rodante Semanal de 16 Semanas** | **−$20,000 de Faltante de Caja** ($10K − $30K) | **+$50,000 de Recuperación** (−$20K + $70K) | **Señala el déficit de $20,000 de la Semana 5 con 5 semanas de anticipación**, permitiendo al equipo alinear las condiciones de transferencia con el proveedor y el recibo del cliente |

---

## Estándares de Tesorería Detrás del Pronóstico Rodante de Caja por Método Directo

Los equipos de tesorería corporativa confían en el **pronóstico rodante de flujo de caja a corto plazo por método directo** porque los estados de resultados de devengo miden la rentabilidad, no la solvencia de caja. Los negocios de productos en rápido crecimiento frecuentemente generan márgenes contables sólidos mientras se quedan sin caja operativa debido a la temporización de los prepagos de inventario.

El método directo omite los ajustes de la contabilidad de devengo y mapea el **100% de los recibos brutos de caja esperados y los desembolsos brutos de caja** a intervalos semanales específicos:

| Método Tradicional de Reporte | Limitación Estructural en las Operaciones | Cómo lo Resuelve el Modelo de Método Directo de 16 Semanas |
| --- | --- | --- |
| **Estimación de Caja Indirecta desde el Estado de Resultados** | Confunde el ingreso neto contable con los fondos líquidos del banco; oculta los picos de capital de trabajo de mitad de mes | Mapea **recibos de caja fechados reales y desembolsos por transferencia** semana a semana |
| **Verificación Diaria del Saldo Bancario** | Puramente retrospectivo; muestra el efectivo liquidado ignorando más de $100K en transferencias de PO comprometidas próximas | Proyecta **saldos de caja corrientes hacia adelante** a lo largo de las próximas 16 semanas consecutivas |
| **Informes Mensuales de Antigüedad de AR / AP** | Excluye los pedidos de compra no facturados y los hitos de clientes previos al envío | Integra **compromisos de pedidos previos a la factura** junto con las cuentas por cobrar y por pagar facturadas |

**Marcos de Referencia Autoritativos de Tesorería y Gestión de Caja:**

* [AICPA: Pronóstico de Flujo de Caja por Método Directo y Gestión de Capital de Trabajo](https://www.aicpa-cima.com)
* [Association for Financial Professionals (AFP): Estándares de Tesorería a Corto Plazo y Pronóstico Rodante de Caja](https://www.afponline.org)

---

## Cómo Funcionan el Horizonte Rodante de 16 Semanas y el Mapeo de Compensación de Fechas

El horizonte de pronóstico de 16 semanas avanza semana a semana. Cada pedido abierto o factura se asigna a una semana futura específica de caja combinando su **fecha de hito operativa** con su **condición de pago contratada**:

| Entrada de Hito Operativa | Condición de Pago Contratada | Evento Semanal de Flujo de Caja Derivado en el Modelo |
| --- | --- | --- |
| **Fecha de Envío Estimada del Cliente** | *Saldo Pagadero Antes del Envío* | **Entrada de Caja (Recibo)** mapeada a la semana inmediatamente anterior al envío estimado |
| **Fecha de Llegada Estimada de la Mercancía (ETA)** | *Saldo Pagadero Contra Entrega / Llegada* | **Salida de Caja (Transferencia a Proveedor)** mapeada a la semana estimada de llegada al almacén/puerto |
| **Fecha de Emisión de la Factura del Cliente** | *Condición de Crédito Net 30 Días* | **Entrada de Caja (Recibo)** mapeada 4 semanas adelante desde la fecha de factura |

**Por Qué la Precisión del Pronóstico se Divide entre el Horizonte Cercano (Semanas 1–8) y el Horizonte Exterior (Semanas 9–16):**

* **Semanas 1–8 (Ventana de Ejecución de Alta Confianza):** Impulsada por facturas confirmadas, calendarios de embarque bloqueados y pedidos de compra activos ya en producción. Se usa para la programación estricta de pagos, las aprobaciones de transferencias y las decisiones de disponimiento de líneas de crédito.
* **Semanas 9–16 (Ventana de Planificación Estratégica y Aprovisionamiento):** Impulsada por plazos de producción estimados y pedidos de venta en el pipeline. Se usa para probar de manera exigente si los nuevos PO de proveedores pueden financiarse con el flujo de caja interno antes de firmar los contratos.

---

## Tutorial de Inicio Rápido: Cómo Construir Su Pronóstico Rodante de Flujo de Caja de 16 Semanas en 7 Pasos

Siga este flujo de trabajo paso a paso para transicionar a su equipo de finanzas y operaciones desde las verificaciones reactivas de saldo bancario hacia la gestión proactiva de liquidez de 16 semanas:

1. **Pruebe Escenarios de Compromisos en la Demostración Interactiva del Navegador**
Abra el [Simulador Web Interactivo de Flujo de Caja Rodante de 16 Semanas](https://hyvoid.github.io/rolling-cashflow-forecast/) para explorar cómo los PO abiertos, los depósitos de clientes y los retrasos de envío desplazan los saldos semanales de caja en tiempo real.
2. **Configure el Saldo de Caja de Apertura y el Colchón Mínimo Seguro de Caja**
Ingrese su saldo bancario operativo actual, defina su fecha de inicio del pronóstico en lunes y establezca el **Umbral Mínimo Seguro de Caja** de su empresa (p. ej., $25,000 o 1 mes de nómina/gastos operativos fijos).
3. **Registre las Cuentas por Cobrar (AR) y las Cuentas por Pagar (AP) Facturadas**
Introduzca las facturas de clientes pendientes y las facturas de proveedores con sus fechas de vencimiento contratadas para establecer su línea de tiempo base de caja posterior a la factura.
4. **Ingrese los Pedidos de Venta (SO) No Facturados y los Pedidos de Compra (PO) Abiertos**
Registre los pedidos de clientes confirmados y los PO de proveedores activos junto con los porcentajes de depósito, los porcentajes de saldo, las fechas estimadas de envío/llegada y las condiciones de pago.
5. **Ejecute la Deduplicación Automatizada de PO a Factura**
Marque o vincule los pedidos de compra que ya fueron facturados por los proveedores para que el motor de deduplicación los excluya de los compromisos abiertos y evite el doble conteo.
6. **Inspeccione las Alertas Semanales de Infracción de Umbral y Diagnostique los Valles de Caja**
Revise la línea de tiempo de caja de 16 semanas para detectar cualquier semana que caiga por debajo de su colchón mínimo, luego filtre la tabla de compromisos por ese número de semana para identificar el PO de proveedor exacto o la cobranza de cliente retrasada que causa la brecha.
7. **Estandarice Su Revisión Semanal de Caja con el Libro de Excel Reutilizable**
Una vez que haya probado la lógica en la vista previa web de sesión única, **[Descargue la Plantilla Excel Completa y Reutilizable de Flujo de Caja Rodante de 16 Semanas](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)** para guardar los datos continuos de su empresa, personalizar el rastreo de contrapartes y ejecutar su revisión semanal de liquidez de 5 minutos sin conexión en Microsoft Excel.

*Aviso: Este libro de trabajo es un modelo operativo de planificación de caja y de apoyo a la decisión. Complementa, en lugar de reemplazar, el software contable formal GAAP/IFRS, los estados financieros auditados y el asesoramiento con licencia en tesorería o financiamiento.*

---

## Descargue la Plantilla Excel Completa

¿Listo para eliminar los faltantes sorpresa en las fechas de pago y unificar sus compromisos de AR, AP y pedidos abiertos en una única línea de tiempo rodante?

👉 **[Obtenga el Libro de Excel Completo de Pronóstico de Flujo de Caja Rodante de 16 Semanas](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)**

---

## Alcance Técnico y Limitaciones Operativas

* **Dependencia de la Frescura de los Datos:** La precisión del pronóstico se basa en estimaciones operativas actuales; los PO de proveedores no registrados o las fechas de llegada de fletes desactualizadas subestimarán o desalinearán las salidas semanales de caja.
* **Cadencia de Mantenimiento Rodante Semanal:** Diseñado para una actualización semanal de 5 minutos (actualizar la caja de apertura, rodar la fecha de inicio hacia adelante y ajustar las ETA de envío desplazadas).
* **Capa de Apoyo a la Decisión (No es un GL Contable):** Construido para la planificación prospectiva de liquidez; no reemplaza los sistemas ERP, el software de partida doble ni los registros fiscales legales.
* **Mapeo Determinista de Fechas:** Modela cada tramo de compromiso en una fecha y un monto objetivo específicos; los descuentos probabilísticos por pagos atrasados o las pruebas de estrés de cancelación de pedidos requieren anulaciones manuales de fecha/monto.
* **Varianza del Horizonte Exterior (Semanas 9–16):** Las Semanas 1–8 reflejan compromisos casi bloqueados, mientras que las Semanas 9–16 reflejan estimaciones operativas sujetas a cambios en los plazos de la cadena de suministro.
* **Arquitectura de Moneda Base Única:** Los PO de proveedores multidivisa (p. ej., USD vs. EUR/CNY) deben ingresarse a su tipo de cambio presupuestado o cubierto a futuro en la moneda base.
* **Escala Operativa Recomendada:** Optimizado para pymes que gestionan activamente **de 5 a 50 pedidos/POs abiertos concurrentes** por ciclo rodante en Microsoft Excel.

---

## Acerca de Theseus Workshop

Construimos modelos financieros y operativos prácticos y listos para auditoría en Microsoft Excel para negocios mayoristas, manufactureras y empresas lideradas por operadores que necesitan control institucional de tesorería y contabilidad dentro de hojas de cálculo estándar.

Cada libro de trabajo utiliza fórmulas nativas transparentes de Excel sin macros de caja negra, dando a los equipos de finanzas y operaciones visibilidad completa sobre cada cálculo semanal de caja.

¿Resolviendo problemas complejos de capital de trabajo, aprovisionamiento de inventario o asignación de capital en hojas de cálculo? **[Explore Nuestra Colección Completa de Plantillas Excel Financieras y Operativas en Theseus Workshop →](https://www.theseusworkshop.com)**

---

## Licencia

Distribuido bajo la [Licencia de Código Abierto Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

