[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)
# Prevenga los faltantes de liquidez antes de que lleguen a la fecha de pago

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Focus](https://img.shields.io/badge/focus-Operations--Stage%20Business-orange)

**Diseñado para empresas de bienes de consumo, mayoristas y manufactureras que necesitan rastrear movimientos de efectivo comprometidos, obligaciones de prepago y liquidez rodante antes de que ocurra un faltante.**

[Vista previa en vivo](https://hyvoid.github.io/rolling-cashflow-forecast/) · [Comprar la versión Excel completa](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

</div>

Rastree los compromisos de efectivo de pedidos abiertos, detecte brechas de liquidez con semanas de anticipación y mantenga una única fuente de verdad prospectiva para la viabilidad de efectivo a corto plazo.

---

## Vista previa rápida

<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 03_53_03 PM" src="https://github.com/user-attachments/assets/d43699bc-4a15-470c-901e-7b372c953861" />

> Vea la vista previa interactiva del libro de trabajo: [demostración de flujo de caja de 16 semanas](https://hyvoid.github.io/rolling-cashflow-forecast/)

---

## Por qué existe esto

La mayoría de los faltantes de liquidez en empresas en crecimiento no son causados por operaciones no rentables.

Generalmente ocurren porque los prepagos de clientes, los ingresos por hitos, los pedidos de compra comprometidos y las condiciones de pago escalonadas son difíciles de consolidar manualmente — y los registros contables estándar son estructuralmente ciegos a ellos hasta que se emite una factura.

El riesgo es simple:

```
Payment due date arrives
-> Manual bank balance check
-> Prior commitments missed
-> Shortfall discovered at the wire
```

Este libro de trabajo está diseñado para cambiar el flujo de trabajo:

```
New order or supplier PO considered
-> Commitment entered once
-> 16-week cash timeline updated automatically
-> Liquidity gap flagged before it becomes a crisis
```

El problema comercial no es solo la gestión del efectivo. Es la visibilidad operativa. Los equipos de finanzas y los operadores necesitan saber si la empresa puede cubrir su próxima obligación — antes de aceptar condiciones de pago.

---

## Tres trampas de liquidez que atrapan a las empresas en crecimiento

### Trampa 1 — Los estados mensuales se leen mal como una imagen de liquidez

Los informes estándar de AR/AP reflejan lo que se ha facturado. No reflejan lo que se ha comprometido.

Una empresa que tiene $80,000 en depósitos de clientes confirmados y $60,000 en prepagos a proveedores contratados que vencen el mes próximo no muestra ninguno de los dos en su estado de resultados hasta que las mercancías se muevan y se emitan las facturas. El equipo de finanzas ve hoy un saldo bancario saludable. El faltante próximo es invisible.

Los equipos de finanzas que gestionan el efectivo a partir de estados mensuales trabajan rutinariamente con una imagen que está estructuralmente cuatro a seis semanas por detrás de la realidad. El modelo mental se siente completo; los datos no lo están.

### Trampa 2 — Los prepagos y los pedidos de compra se rastrean en sistemas separados

Cuando la misma empresa recibe un depósito de cliente del 30% el lunes y emite un prepago a proveedor del 40% el jueves, ambas transacciones afectan el mismo fondo de efectivo — pero típicamente viven en sistemas diferentes, hojas de cálculo diferentes o equipos diferentes.

Las operaciones que mantienen un rastreo separado para los compromisos de ventas y las obligaciones de adquisiciones — una división natural del flujo de trabajo — no logran ver sistemáticamente la posición neta de efectivo. La regulación no reconoce esa frontera operativa. La cuenta bancaria tampoco.

### Trampa 3 — Las brechas se descubren en la fecha de vencimiento del pago

La verificación manual generalmente ocurre cuando un pago vence o cuando alguien revisa la cuenta bancaria. Para cuando se identifica una brecha, la ventana de acción se ha cerrado. Las respuestas reactivas — giros de crédito de emergencia, renegociaciones con proveedores, nómina retrasada — tienen un costo real y causan daños reales en las relaciones.

La interceptación previa a la brecha requiere que el riesgo de liquidez sea visible semanas antes de que la obligación madure — lo que requiere que todos los compromisos abiertos estén actualizados y que todos los cálculos de temporización se ejecuten automáticamente en el momento de la planificación.

La brecha generalmente está oculta en la relación entre:

- el saldo de efectivo de apertura
- la temporización de recepción de depósitos y prepagos
- las fechas de recepción de saldos de clientes
- las fechas de vencimiento de pagos a proveedores
- las condiciones de pago contractuales
- el volumen de pedidos y la tasa de crecimiento

Por eso la conciliación manual a menudo saca a la luz el problema tarde, o lo omite por completo.

---

## Para quién es esta herramienta

| Usuario | Caso de uso práctico |
|---|---|
| Gerentes de finanzas | Identificar brechas de liquidez de 6–16 semanas antes de que se conviertan en crisis |
| Gerentes de operaciones | Entender el impacto en efectivo de un nuevo pedido o PO de proveedor antes de comprometerse |
| Fundadores y CEO | Mantener una vista prospectiva única de la viabilidad de efectivo a medida que la empresa escala |
| Equipos de adquisiciones | Evaluar las exigencias de prepago frente a la liquidez realmente disponible |
| Contadores externos | Brindar asesoría de efectivo a corto plazo sin construir un modelo desde cero |

Es más adecuada para empresas que operan con estructuras mixtas de prepago de clientes y prepago a proveedores, donde el software de tesorería es prohibitivamente costoso pero los enfoques manuales ya no escalan.

---

## Lo que hace el libro de trabajo

### Registro de compromisos abiertos
Un único punto de entrada de datos para todos los AR, AP, pedidos de venta abiertos y pedidos de compra abiertos. Los equipos ingresan la información básica de compromiso y temporización una sola vez; los cálculos de la línea de tiempo de efectivo se ejecutan automáticamente en segundo plano.

### Línea de tiempo de efectivo de 16 semanas
Mapeo automático de cada compromiso abierto a una semana específica y una dirección de efectivo. La ventana rodante se actualiza cada semana a medida que se agregan nuevas entradas y las semanas previas se cierran.

### Estado de liquidez previo a la decisión
El saldo de efectivo proyectado de cada semana es visible antes de aceptar un nuevo pedido o acordar una nueva condición de proveedor. Sin referencias cruzadas manuales. Sin descubrimiento el día del pago.

### Lógica de deduplicación
Los pedidos de compra ya convertidos en facturas se identifican y excluyen automáticamente — garantizando que cada movimiento de efectivo esperado se cuente exactamente una vez y que la vista de compromisos abiertos se mantenga limpia.

### Capa de alertas por umbral
La empresa configura un saldo mínimo seguro de efectivo. El modelo resalta qué semanas infringen el umbral y qué transacciones específicas impulsan cada brecha — dando a los equipos un diagnóstico a nivel de transacción, no solo una bandera roja.

### Estructura lista para auditoría
Cada entrada está estructurada y es rastreable desde el primer día. El registro completo de compromisos de 16 semanas puede filtrarse por dirección, contraparte o semana y revisarse sin posprocesamiento.

---

## Escenario de ejemplo

**Perfil de la empresa:** Importador de bienes de consumo. Condiciones mixtas de prepago de clientes y requisitos de prepago a proveedores. Función financiera única.

**El problema:** Cada semana, el gerente de finanzas concilia manualmente los pedidos de venta abiertos, los depósitos de clientes pendientes, las facturas de proveedores pendientes y las fechas de llegada previstas de mercancías para estimar el efectivo disponible. Los compromisos de clientes se rastrean en el CRM. Los compromisos de proveedores se rastrean en la hoja de adquisiciones. Conciliar ambos en una posición neta de efectivo toma dos horas y produce una vista que ya tiene una semana de antigüedad.

En un trimestre de operaciones, se identificaron dos brechas de liquidez — ambas dentro de las 48 horas de la fecha de vencimiento del pago.

| | Antes | Después |
|---|---|---|
| Estructura de compromisos | Dos hojas separadas, una por equipo | Un libro de trabajo unificado |
| Tiempo de verificación semanal de efectivo | ~2 horas en todas las posiciones abiertas | Menos de 5 minutos por semana |
| Consolidación de prepagos | Referencia cruzada manual | Automática en AR, AP, pedidos de venta, POs |
| Descubrimiento de brechas | En la fecha de vencimiento del pago; respuesta reactiva | De 6–8 semanas; respuesta planificada |

**El punto de inflexión específico que esta herramienta saca a la luz:**

Un pedido de cliente de $100,000 lleva un saldo del 70% que vence antes del envío, estimado en la semana 6. El PO de proveedor relacionado lleva un saldo del 60% que vence a la llegada de la mercancía, estimado en la semana 5. Saldo de efectivo de apertura: $10,000.

Posición neta semana 5: $10,000 − $30,000 = **−$20,000.** Existe una brecha.
Posición neta semana 6: −$20,000 + $70,000 = **$50,000.** Resuelta.

Una vista mensual muestra el mes neto-positivo. La ventana semanal muestra un faltante real de $20,000 en la semana 5 que requiere acción antes de que llegue — no después.

---

## Por qué el pronóstico de efectivo a corto plazo funciona de esta manera

El pronóstico de flujo de caja rodante — método directo, horizonte prospectivo corto — es una disciplina de tesorería estándar mantenida por la mayoría de las grandes corporaciones como función operativa central. En las empresas más grandes, la gestionan funciones de tesorería dedicadas con software especializado.

El método directo funciona mapeando los movimientos de efectivo reales esperados — no los asientos contables — a fechas específicas. Cada entrada y salida comprometida se traduce en una semana, una dirección y un monto. El saldo corriente en cualquier momento refleja lo que la empresa realmente espera mantener, no lo que muestran sus registros contables.

Este enfoque es estructuralmente distinto de:

- **La estimación de efectivo basada en el estado de resultados** — confunde rentabilidad con liquidez; una empresa puede ser rentable e ilíquida simultáneamente
- **La gestión del saldo bancario** — solo refleja lo que ya se ha movido; las salidas futuras comprometidas son invisibles
- **Los informes mensuales de AR/AP** — excluyen por completo los compromisos previos a la factura; ciegos sistemáticamente a la capa operativa

La razón por la que la mayoría de las empresas en crecimiento carecen de esta vista no es la complejidad. Es la ausencia de un mecanismo estructurado para consolidar los compromisos operativos — que viven repartidos entre ventas, adquisiciones y finanzas — en una única línea de tiempo de efectivo.

Contexto de referencia útil:
- [AICPA: Pronóstico de flujo de caja por el método directo](https://www.aicpa.org)
- [AFP: Fundamentos de la gestión de tesorería](https://www.afponline.org)

---

## Cómo funciona la ventana de 16 semanas

La ventana de 16 semanas se desliza hacia adelante cada semana, no cada mes. Cada nueva entrada se mapea a una semana futura específica según las fechas operativas estimadas y las condiciones de pago contractuales.

| Entrada operativa | Evento de efectivo derivado |
|---|---|
| Fecha de envío estimada + condición "pago antes del envío" | Recepción del cliente en la semana previa al envío estimado |
| Fecha de llegada de mercancía estimada + condición "pago contra entrega" | Salida al proveedor en la semana de llegada estimada |
| Fecha de factura + condición "Net 30" | Recepción del cliente aproximadamente 4 semanas adelante |

**La trampa en números:**

Una empresa que gestiona 10 pedidos abiertos simultáneamente — cada uno con su propia estructura de depósito, temporización de pago del saldo y calendario de prepago a proveedores — carga más de 30 eventos de efectivo interactuantes en un momento dado. Cada evento depende de una estimación operativa actual para mantenerse exacto. La consolidación manual introduce error en cada paso.

El modelo mental de reinicio mensual aprueba posiciones que la ventana semanal rodante no aprueba. El cálculo es estructural, no subjetivo. La automatización elimina esa clase de error por completo.

**Por qué la confiabilidad del pronóstico decae en el horizonte exterior:** El horizonte cercano de las semanas 1–8 está poblado de compromisos ya en marcha — fechas de envío y condiciones de pago confirmadas o casi confirmadas. Las semanas 9–16 dependen de estimaciones operativas que pueden desplazarse materialmente a medida que los pedidos se colocan o retrasan. El modelo es más confiable dentro del horizonte cercano de 6–8 semanas. La ventana exterior es útil direccionalmente para la planificación; no es una garantía.

---

## Lógica del libro de trabajo

El libro de trabajo está organizado en torno a un flujo de trabajo práctico de planificación de efectivo:

1. Ingrese todos los AR, AP, pedidos de venta y pedidos de compra abiertos con las fechas estimadas y las condiciones de pago.
2. Aplique la deduplicación para identificar y excluir los pedidos de compra ya convertidos en facturas.
3. Mapee cada compromiso abierto a su semana y dirección de efectivo esperadas.
4. Calcule el saldo rodante de 16 semanas hacia adelante desde la posición de efectivo de apertura.
5. Compare el saldo proyectado de cada semana con el umbral mínimo seguro.
6. Marque las semanas con brecha e identifique las transacciones específicas que impulsan cada brecha.
7. Preserve el registro de compromisos para la revisión semanal rodante y la comunicación con el equipo.

El libro de trabajo está destinado a ser una herramienta de apoyo a la decisión y planificación. No reemplaza el software de contabilidad, los registros financieros auditables ni el asesoramiento profesional para decisiones de financiamiento complejas.

---

## Compra

Utilice el libro de trabajo Excel completo aquí:

[Comprar el libro de trabajo Excel completo →](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

---

## Limitaciones

- **Dependencia de las entradas** — la exactitud del pronóstico está limitada por la calidad de los datos ingresados; estimaciones de envío obsoletas o compromisos faltantes producen una falsa sensación de visibilidad sin advertencia
- **Se requiere actualización manual** — el modelo no se actualiza automáticamente; sin un mantenimiento semanal consistente, la ventana rodante se degrada y las brechas vuelven a ser invisibles
- **No es un sistema de registro** — esta es una capa de apoyo a la decisión; no reemplaza el software de contabilidad, un ERP ni los registros financieros auditables
- **Determinista, no probabilista** — cada evento de efectivo se modela como una fecha fija y un monto fijo; el riesgo de retraso en el pago, el movimiento de divisas y los escenarios de cancelación de pedidos requieren una superposición manual
- **Confiabilidad del horizonte exterior** — las semanas 10–16 dependen de estimaciones operativas que pueden desplazarse materialmente; el modelo es más confiable dentro del horizonte cercano de 6–8 semanas
- **Multidivisa no modelada** — las empresas con exposición significativa a divisas deberán aplicar supuestos de tipo de cambio como superposición manual
- **Contexto de escala** — diseñado para empresas que gestionan de 5 a 50 posiciones abiertas simultáneas; más allá de este rango, el modelo de entrada manual requiere adaptación estructural

---

## Acerca de este proyecto

Este libro de trabajo es parte de un esfuerzo más amplio por traducir requisitos operativos y financieros complejos en herramientas ligeras que las organizaciones pequeñas y medianas realmente puedan usar.

Sin ERP. Sin suscripción a software de tesorería. Sin proyecto de desarrollo personalizado.

Solo lógica de negocio clara, datos estructurados y apoyo a la decisión repetible — entregado en software que tu equipo ya tiene.

Si tu operación involucra gestión de efectivo, ciclos de adquisiciones o estructuras de facturación a clientes que actualmente viven en la cabeza de alguien o en una hoja de cálculo desconectada, [ve qué más hay disponible →](https://www.theseusworkshop.com)

---

## Licencia

Distribuido bajo la [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
