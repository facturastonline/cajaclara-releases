# CajaClara — Manual de usuario

Versión 0.4 · Para dueños, encargados y cajeros

CajaClara es un punto de venta para **panaderías, abarrotes, talleres mecánicos y tiendas de celulares
y electrónica**. Funciona en la
computadora del negocio **sin necesidad de internet**; solo lo usa para buscar actualizaciones.

---

## Contenido

1. [Instalación y primer arranque](#1-instalación-y-primer-arranque)
2. [Licencia y demostración](#2-licencia-y-demostración)
3. [Usuarios, roles e inicio de sesión](#3-usuarios-roles-e-inicio-de-sesión)
4. [Caja: abrir turno, entradas, salidas y corte](#4-caja-abrir-turno-entradas-salidas-y-corte)
5. [Venta](#5-venta)
6. [Cancelar una venta y reimprimir tickets](#6-cancelar-una-venta-y-reimprimir-tickets)
7. [Cotizaciones](#7-cotizaciones)
8. [Productos (o Refacciones y servicios)](#8-productos-o-refacciones-y-servicios)
9. [Inventario](#9-inventario)
10. [Taller mecánico: clientes, vehículos y órdenes](#10-taller-mecánico-clientes-vehículos-y-órdenes)
11. [Celulares y electrónica: IMEI, garantías y reparaciones](#11-celulares-y-electrónica-imei-garantías-y-reparaciones)
12. [Crédito y apartados](#12-crédito-y-apartados)
13. [Pagos con tarjeta y transferencia](#13-pagos-con-tarjeta-y-transferencia)
14. [Reportes](#14-reportes)
15. [Ajustes](#15-ajustes)
16. [Problemas frecuentes](#16-problemas-frecuentes)
17. [Otros equipos: celulares y tablets en el Wi-Fi](#17-otros-equipos-celulares-y-tablets-en-el-wi-fi)
18. [Atajos de teclado](#18-atajos-de-teclado)

---

## 1. Instalación y primer arranque

**Requisitos:** Windows 10 u 11. Opcional: impresora térmica de tickets (58 u 80 mm) instalada en
Windows y lector de código de barras.

1. Ejecuta `CajaClara_X.Y.Z_x64-setup.exe`.
2. Si aparece **"Windows protegió su PC"**, haz clic en **Más información → Ejecutar de todas formas**.
   Es normal: el instalador todavía no tiene certificado de firma de Windows.
3. Al abrir CajaClara por primera vez, llena:
   - **Nombre del negocio** (aparece en los tickets).
   - **Giro**: *Abarrotes / Panadería*, *Taller mecánico* o *Celulares y electrónica*. Cambia las pantallas
     disponibles. Celulares y electrónica trae activado **crédito y apartados**.
   - **¿El negocio emite facturas?** Si dices que sí, se piden datos fiscales de clientes y claves del SAT
     de productos.
   - **Tu nombre** y un **PIN** de 4 a 6 números. Serás el **dueño**.
4. Se muestra el **código de recuperación** (ejemplo `68SC-D8XA-F2CZ-ZCYZ`). **Anótalo o imprímelo y
   guárdalo fuera de la caja.** Sirve si el dueño olvida su PIN. Solo se muestra una vez.

> Los datos se guardan en la computadora, en `%APPDATA%\mx.cajaclara.pos`. Actualizar o reinstalar
> el programa **no borra** los datos.

---

## 2. Licencia y demostración

- Al instalar, CajaClara funciona completo durante **15 días de demostración**. Arriba verás
  *"Demostración: N días"*.
- Para activarla, ve a **Ajustes → Licencia**, copia el **código de este equipo** (botón *Copiar*) y
  mándalo a tu proveedor. Te enviará un texto que empieza con `CAJACLARA-LICENCIA:`. Pégalo y presiona
  **Activar licencia**.
- La licencia es **para esa computadora**. Si cambias de computadora, pide una nueva.
- La licencia incluye **todo el programa**: cualquier giro (puedes cambiarlo en **Ajustes**), crédito y
  apartados, comisiones y vendedores, y marcar al cobrar que el cliente **requiere factura**. Lo único que se
  contratará aparte es el **timbrado** de facturas desde CajaClara (próximamente).
- Si la licencia vence (o termina la demostración), CajaClara entra en **modo consulta**: puedes ver
  reportes, caja, inventario y respaldos, pero **no registrar ventas, órdenes ni cotizaciones** hasta
  renovar.
- Tu plan incluye actualizaciones hasta cierta fecha (visible en Ajustes → Licencia). Después de esa
  fecha la app no ofrece versiones nuevas; la que tienes sigue funcionando.

---

## 3. Usuarios, roles e inicio de sesión

**Entrar:** toca tu nombre y escribe tu PIN (con el teclado de la pantalla o el del equipo). Tras 5
intentos fallidos se bloquea 30 segundos.

**Cambiar de persona:** botón **Cambiar usuario** arriba a la derecha.

| Rol | Puede |
|---|---|
| **Cajero** | Vender, cotizar, abrir caja, registrar entradas/salidas y hacer el corte **sin ver el efectivo esperado**. Para cancelar una venta necesita el PIN de un encargado o del dueño. En taller también recibe vehículos y maneja órdenes. |
| **Encargado** | Todo lo del cajero, más productos, inventario, reportes, conciliación de pagos y ver el efectivo esperado en caja. |
| **Dueño** | Acceso total: usuarios, ajustes, licencia, respaldos. |
| **Vendedor (sin acceso)** | No entra al programa: no tiene PIN ni aparece en "¿Quién eres?". Solo aparece para asignarle **comisiones** al cobrar (vendedores de piso, técnicos). |

**Agregar o editar usuarios** (dueño): pestaña **Usuarios** → *+ Nuevo usuario*. Puedes cambiar el
PIN, el rol o desactivar a alguien. Siempre debe quedar al menos un dueño activo. Si un vendedor sin
acceso pasa a cajero, encargado o dueño, se le pide un PIN; si alguien pasa a vendedor sin acceso, su PIN
se borra y ya no puede entrar.

---

## 4. Caja: abrir turno, entradas, salidas y corte

**Abrir caja.** Antes de vender, CajaClara pide el **fondo inicial** (el efectivo con el que empieza
el turno). Escribe 0 si la caja empieza vacía. El punto junto a tu nombre se pone **verde** con caja
abierta y **rojo** con caja cerrada.

**Entradas y salidas de efectivo** (pestaña **Caja**): para registrar dinero que entra o sale sin ser
venta, por ejemplo *pago a proveedor de harina*, *retiro parcial* o *cambio extra*. Siempre con motivo.

**Ventas del turno** (pestaña **Caja**): lista de las ventas del turno. Toca una para **reimprimir** o
**cancelar**.

**Corte de caja:**
1. Pestaña **Caja → Hacer corte**.
2. Cuenta el efectivo de la caja (incluido el fondo) y escribe el total.
3. Confirma. CajaClara calcula lo **esperado** (fondo + cobrado en efectivo + entradas − salidas) y te
   dice si hay **sobrante** o **faltante**.
4. Imprime el ticket del corte para firmarlo.

Después del corte ya no se pueden registrar ventas en ese turno; el siguiente turno abre caja de nuevo.
Se hace un **respaldo automático** al cerrar cada turno.

**Comisiones a empleados** (vienen activadas en Celulares y electrónica; en otros giros se activan en
**Ajustes → Comisiones a empleados**):
1. Al **Cobrar**, marca **Esta venta lleva comisión**. Aparece quien cobra; cámbialo si la venta fue de
   otro empleado y escribe **cuánto** le toca. Con **+ Otro empleado** se reparte entre varios (cada
   uno con su monto). Aparecen todos los usuarios activos de la pestaña **Usuarios**, incluidos
   los **vendedores sin acceso** (empleados que no usan la caja).
2. En **Caja → Comisiones del turno** se ve, por empleado, cuántas ventas, cuánto ganó, cuánto se le
   pagó y cuánto **falta por pagar**.
3. El encargado o el dueño puede tocar **Pagar en efectivo**: el dinero sale de la caja como salida
   *Comisión de …* y el corte cuadra. Si no se paga desde la caja, queda como "por pagar".
4. El ticket del **corte** trae la sección **COMISIONES** con lo de cada empleado. Si una venta se
   cancela, su comisión deja de contar.
5. Para pagar por semana o por mes, **Reporte** muestra **Comisiones por empleado** del periodo.

La comisión no aparece en el ticket del cliente; se ve al tocar la venta en **Caja**.

---

## 5. Venta

1. Busca el producto escribiendo su nombre o **escanea su código de barras** (el cursor siempre regresa
   al buscador). También puedes tocar el producto en la cuadrícula.
2. Los productos **por peso** piden los kilos (ejemplo `0.350`).
3. En el carrito ajusta cantidades con **−** y **+**, o quita productos con **×**.
4. Presiona **Cobrar** o **F12**:
   - **Efectivo:** escribe lo recibido (o usa los botones *Exacto, $50, $100…*). Se muestra el cambio.
   - **Tarjeta:** escribe el **número de autorización** del voucher y marca que la terminal lo imprimió
     como APROBADO.
   - **Transferencia:** escribe la **clave de rastreo** y marca que viste el comprobante.
   - **Cliente (opcional):** toca **+ Cliente**. Al tocar el buscador aparecen los clientes registrados;
     escribe para filtrar o usa **+ Cliente nuevo**. Sale en el ticket.
   - **El cliente requiere factura** (si el negocio factura, en Ajustes): pide elegir al cliente. Si le
     faltan sus datos fiscales, CajaClara avisa para completarlos en **Clientes**. El ticket dice
     *Requiere factura* y en **Caja → Ventas de este turno** la venta aparece con "· factura".
5. Al confirmar se muestra el ticket: **Imprimir ticket**, **Enviar por WhatsApp** (al teléfono del cliente o
   al que escribas; se abre WhatsApp con el ticket listo) o **Nueva venta** (Enter).
6. **Reimprimir o reenviar un ticket:** en Venta, botón **Tickets** (arriba del carrito). Lista las ventas
   del turno y busca por **folio**; toca una para **Reimprimir** o **Enviar por WhatsApp**.

> Puedes ir a otra pestaña a mitad de una venta: **el carrito se conserva** al regresar.

**Imprimir:** en la ventana de impresión elige tu impresora térmica. Para ahorrar papel, en las
preferencias de la impresora usa el tamaño 80 mm (o 58 mm).

---

## 6. Cancelar una venta y reimprimir tickets

- Desde **Venta → Tickets** (también busca por folio), **Caja → Ventas de este turno**, o (encargado/dueño)
  **Reporte → Día → Tickets**, toca la venta.
- **Enviar por WhatsApp:** manda el ticket como texto al cliente.
- **Reimprimir:** imprime el ticket marcado como *REIMPRESIÓN*.
- **Cancelar venta:** escribe el motivo. Si eres cajero, elige quién autoriza y escribe **su PIN**.
  - Los productos **regresan al inventario**.
  - Si la venta era de **otro turno**, la devolución del efectivo se registra sola como **salida** de la
    caja actual.
  - Si se pagó con tarjeta o transferencia, el reembolso se hace desde la terminal o el banco.
  - Si venía de una cotización u orden de taller, estas vuelven a quedar abiertas.

---

## 7. Cotizaciones

1. Pestaña **Cotizaciones → + Nueva cotización**.
2. **Cliente** (opcional): toca el buscador y elige uno de tus clientes registrados (o escribe para
   filtrar), o registra uno con **+ Cliente nuevo**. Se usan su nombre y su WhatsApp. Después pon la
   vigencia y las notas.
3. Busca y agrega productos. Puedes **cambiar la cantidad y el precio** de cada línea (descuentos).
4. **Guardar cotización**. Después puedes:
   - **Imprimir / PDF** (tamaño carta; para PDF elige "Guardar como PDF").
   - **Enviar por WhatsApp** (abre WhatsApp con el texto listo) o **Copiar texto**.
   - **Cobrar en caja**: pasa a Venta con los precios cotizados y el cliente; al cobrar queda como **vendida**.
5. Mientras esté **abierta** puedes editarla (agregar o quitar cosas). Pasada la vigencia aparece como
   **vencida** pero aún puede cobrarse.

---

## 8. Productos (o Refacciones y servicios)

Pestaña **Productos** (en taller: **Refacciones**). Encargado y dueño.

- **+ Nuevo producto**: nombre, código de barras (o número de parte), se vende por **pieza** o **peso**,
  precio **con IVA**, costo, IVA (0 %, 8 % frontera o 16 %), **existencia inicial** y aviso de existencia
  mínima. La existencia inicial queda en el historial de Inventario como *Existencia inicial*.
- **Productos e Inventario van juntos:** en Productos das de alta lo que vendes (nombre, precio, código);
  en Inventario mueves su existencia. Al editar un producto la existencia solo se ve: se cambia con una
  entrada, merma o ajuste en **Inventario**, así cada cambio queda registrado con fecha y usuario.
- **Código de barras:** si un producto no trae, toca **Generar código** en su ficha, o **Etiquetas → Generar códigos
  faltantes** para todos. Son códigos internos de 13 dígitos que empiezan con 20, solo para tu tienda.
- **Etiquetas** (botón arriba en Productos): escribe cuántas quieres de cada producto o toca **Según existencia**, elige
  el papel (rollo de 50 × 25 mm, impresora de tickets u hoja carta de 30 etiquetas) y si llevan precio. Los equipos con
  IMEI llevan una etiqueta por equipo, con su IMEI. Al imprimir, usa escala 100% y el tamaño de papel correcto.
- En **taller** eliges si es **Refacción / producto** (con inventario) o **Servicio (mano de obra)**
  (sin inventario).
- Con **facturación activa** se piden la clave de producto/servicio y la clave de unidad del SAT.
- Toca un producto para editarlo o eliminarlo. Los productos con poca existencia aparecen en rojo, y los que ya no tienen dicen
  **Agotado** (en Venta y en Productos). Si la existencia quedó negativa (se vendió sin tenerla registrada),
  se ve como *Agotado (−2)*: corrígela con un **ajuste por conteo** en Inventario.

---

## 9. Inventario

Pestaña **Inventario** (encargado y dueño). Mueve la existencia de los productos dados de alta en
**Productos**; las ventas y cancelaciones descuentan y regresan solas. Las acciones cambian según el giro:

| Acción | Para qué | Efecto |
|---|---|---|
| **Producción** (solo abarrotes / panadería) | Lo que se horneó o elaboró hoy | Suma existencia |
| **Entrada de mercancía** | Compras a proveedores | Suma existencia y actualiza el costo |
| **Merma** | Lo que se tira, caduca o se echa a perder | Resta existencia |
| **Ajuste por conteo** | Después de contar físicamente | Escribes lo contado; calcula la diferencia |

**Tip para panadería:** en Producción usa **Agregar todos los productos** y escribe solo las cantidades;
los que dejes en 0 se ignoran.

**Bodega y mostrador:** si guardas mercancía aparte de lo que tienes a la venta, enciéndelo en
**Ajustes → Negocio** (viene encendido al configurar un negocio de celulares y electrónica). Entonces:

- Cada producto muestra cuánto hay en **mostrador** y cuánto en **bodega**. Al encenderlo, toda tu existencia
  actual queda en mostrador; pasa a bodega lo que corresponda con un **ajuste por conteo** o un **traspaso**.
- Las entradas, mermas y ajustes preguntan **dónde** ocurren. La nueva acción **Traspaso** mueve mercancía de
  una a otra sin cambiar el total.
- Las ventas salen de **mostrador**. Si se vende más de lo que hay ahí, lo que falte se descuenta de bodega.
  Si en mostrador no queda nada pero sí hay en bodega, en la pantalla de venta se ve *En bodega: 5*.
- Los equipos con IMEI llevan su propia ubicación: se elige al agregarlos y se cambia con **Pasar a bodega**
  o **Pasar a mostrador** en la ficha del equipo (Productos → abre el modelo → toca el equipo).

**Cargar factura:** elige el XML (CFDI) que te mandó el proveedor y revisa cada concepto:

- **Producto existente:** CajaClara lo propone si ya lo relacionaste antes con ese proveedor, o si coincide el código
  o el nombre. **Crear nuevo:** escribe su precio de venta. **Sin entrada:** para fletes u otros conceptos que no son mercancía.
- **Piezas por unidad:** si la factura dice 1 caja y trae 12 piezas, escribe 12. Se recuerda para la próxima.
- Los **equipos con IMEI** piden un IMEI por pieza.
- El **costo** de cada producto se actualiza con lo que pagaste por pieza, **con IVA y descuentos incluidos**.
- Una misma factura **no se puede cargar dos veces**. Si te equivocaste, corrige con un **ajuste por conteo** o una **merma**.

Abajo está el **historial de movimientos** por fechas y tipo, con totales **a costo** (por ejemplo,
cuánto dinero se fue en mermas). Las ventas y cancelaciones también aparecen ahí.

---

## 10. Taller mecánico: clientes, vehículos y órdenes

*Solo con giro Taller mecánico.*

### Recibir un vehículo
1. **Órdenes → + Recibir vehículo**.
2. Busca por **placas**, cliente o teléfono. Si no existe, **+ Cliente nuevo** y luego sus datos del
   vehículo (placas, marca, modelo, año, color, número de serie, kilometraje).
3. Anota cómo llega: **kilometraje**, **gasolina**, lo que **trae** (desmarca lo que falte: gato,
   refacción, estéreo…), **golpes o rayones**, la **falla** que reporta el cliente, el **mecánico** y la
   **fecha promesa**.
4. **Crear orden de servicio**. Imprime la orden para que el cliente **firme de recibido**.

### Trabajar la orden
- Cambia la **etapa** con los botones: Recibido → En diagnóstico → Autorizado → En reparación →
  Esperando refacción → Terminado.
- Escribe el **diagnóstico** y agrega **mano de obra y refacciones** (precio editable). **Guardar cambios**.
- **Avisar por WhatsApp**: manda al cliente el estado, el presupuesto y el saldo.
- **Registrar anticipo**: efectivo, tarjeta o transferencia. Entra a la caja del turno.

### Cobrar y entregar
1. **Cobrar y entregar** → indica el **próximo servicio** (fecha o kilometraje).
2. Pasa a Venta con los conceptos y **descuenta los anticipos**: solo se cobra el **saldo**.
3. Al cobrar: la orden queda **entregada**, las refacciones se descuentan del inventario.

### Clientes y vehículos
Pestaña **Clientes**: busca vehículos por placas, consulta el **historial de servicios** de cada uno y
la lista de **próximos servicios** (vencidos o en los próximos 15 días) para llamar a los clientes.

---

## 11. Celulares y electrónica: IMEI, garantías y reparaciones

*Solo con giro Celulares y electrónica.*

### Registrar un equipo que llega
Todo se hace en **Productos → + Nuevo producto**, en el momento en que llega el equipo:
1. **Modelo**: por ejemplo *iPhone 13 128 GB* o *iPad 9 64 GB*.
2. Marca **Es un equipo con IMEI o número de serie**.
3. **Código de barras / IMEI**: escanéalo con la lectora o escríbelo a mano (en el teléfono se ve
   marcando `*#06#`). El Enter de la lectora no guarda el formulario, así puedes seguir llenando.
4. **Condición (grado)**: Nuevo, A+, A-, B o C. Con *Nuevo* la batería se pone en 100%.
5. **Salud de la batería** (%), **color**, **precio de venta y costo de ese equipo**, IVA y **días de
   garantía**.
6. **Registrar equipo**.

Si ya existe un modelo con ese nombre, CajaClara pregunta y agrega el equipo a ese modelo, con su propio
precio. Así la existencia y los reportes quedan por modelo.

**Varios equipos seguidos del mismo modelo:** toca el modelo en la lista de Productos → **+ Agregar
equipo** → escanea, llena la condición → **Agregar y seguir con otro** (conserva el grado y el precio,
limpia el IMEI, la batería y el color).

**Ver y corregir los equipos de un modelo:** toca el modelo en Productos. Abajo aparecen sus equipos
(en tienda, apartados, vendidos) con IMEI, grado, batería, color y precio. Toca uno para **Editar datos**
o **Dar de baja** (dañado o devuelto al proveedor; queda como merma). En la lista de modelos, el precio es
el base y la existencia es cuántos equipos hay en tienda.

### Accesorios y mano de obra
- **Accesorios** (fundas, micas, cargadores): producto normal con código de barras y existencia; también
  pueden llevar días de garantía. Sus entradas y mermas van en **Inventario**.
- **Mano de obra** de reparaciones (*Cambio de pantalla*, *Centro de carga*): elige **Servicio**.

### Vender un equipo
- En **Venta**, **escanea el IMEI** de la caja del equipo: entra ese equipo exacto.
- O toca el modelo y elige de la lista: se ve el **grado, color, batería y precio** de cada equipo.
- El ticket imprime el equipo con su grado, color y batería, el **IMEI** y la fecha en que **termina la
  garantía**.
- Si escaneas un IMEI que ya se vendió o está apartado, CajaClara te dice a quién y si su garantía está
  vigente.

### Consultar una garantía
- **Cajero:** en **Venta**, escanea el IMEI. Si ya se vendió, dice a quién y hasta cuándo tiene garantía.
- **Encargado o dueño:** en **Productos**, escribe o escanea el IMEI en el buscador. Arriba aparece el
  equipo con su estado, cliente y garantía; tócalo para ver la venta completa.
- Al **recibir un equipo para reparación**, si se vendió aquí, se avisa su garantía de venta.

### Reparaciones
1. **Reparaciones → + Recibir equipo**.
2. Busca al **cliente** por nombre o teléfono (o **+ Cliente nuevo**).
3. Datos del equipo: tipo, **marca, modelo, IMEI** (se ve marcando `*#06#`), color y la **contraseña o
   patrón** para poder probarlo.
4. Si el equipo **ya vino antes**, se avisa y se muestra si tiene **garantía vigente** de esa reparación.
5. Anota la **falla**, lo que **deja con el equipo** (chip, memoria, funda, cargador…), el **estado
   físico** (pantalla estrellada, tapa rayada), el técnico y la fecha promesa. **Crear orden de reparación**.
6. Imprime la orden para que el cliente **firme**. Incluye el aviso de respaldo de información y de
   equipos no recogidos.
7. Trabaja la orden igual que en el taller (sección 10): diagnóstico, piezas y mano de obra, anticipos,
   **Avisar por WhatsApp** para que el cliente autorice el presupuesto.
8. **Cobrar y entregar** → elige los **días de garantía** de la reparación → cobra el saldo. El ticket
   imprime hasta cuándo cubre la garantía.

En la lista, las órdenes **terminadas que llevan 30 días o más sin recogerse** se marcan en rojo con los
días que llevan.

---

## 12. Crédito y apartados

Viene activado en *Celulares y electrónica*. En otros giros se activa en **Ajustes → Crédito y apartados**.

### Vender a crédito
1. En **Venta**, al cobrar elige **Crédito**.
2. Busca o da de alta al **cliente**. Se ve cuánto debe y cuánto crédito le queda.
3. Si deja **enganche**, escríbelo y elige con qué paga (efectivo, tarjeta o transferencia).
4. **Registrar venta a crédito**. El ticket dice cuánto queda **a crédito** y tiene línea para la
   **firma** del cliente.

### Cobrar abonos
**Clientes → Crédito**: lista de quién debe y el total por cobrar. Toca al cliente para ver su **estado
de cuenta** (compras y abonos), **Registrar abono** (imprime comprobante con saldo anterior y nuevo),
**Recordar por WhatsApp** y **Cambiar límite** (vacío = sin límite; 0 = ya no se le vende a crédito).

### Apartar
1. En **Venta**, agrega lo que se va a apartar y toca **Apartar**.
2. Elige al cliente, el **abono inicial**, la **fecha límite** para liquidar y notas.
3. Se imprime el comprobante. Los equipos con IMEI quedan **reservados**: no se pueden vender a otro.

En la pestaña **Apartados**: abonos, comprobante, recordatorio por WhatsApp y **Liquidar y entregar**
(pasa a Venta y solo cobra lo que resta). Los vencidos se marcan en rojo. **Cancelar apartado** libera
la mercancía; escribe cuánto se le devuelve al cliente (lo que no se devuelva queda como cargo por
cancelación) y se registra como salida de caja.

### En la caja
Los abonos de crédito y de apartados **entran a la caja del turno** en que se reciben y aparecen en el
corte como **Abonos y apartados**. Lo vendido a crédito aparece aparte (**Vendido a crédito**): no es
dinero en caja. Si se cancela una venta a crédito, esa deuda se quita de la cuenta del cliente.

---

## 13. Pagos con tarjeta y transferencia

Pestaña **Pagos** (encargado y dueño). Cada pago con tarjeta, transferencia, anticipo o abono queda
**pendiente** hasta que alguien lo compare con el banco o la terminal:

1. Elige las fechas.
2. Revisa cada pago contra tu app del banco o de la terminal (monto y referencia).
3. Marca **Verificar** si llegó, o **Rechazar** con el motivo si no. *Deshacer* regresa a pendiente.

Arriba ves cuánto falta por conciliar.

---

## 14. Reportes

Pestaña **Reporte** (encargado y dueño).

- Elige **Día, Semana, Mes o Año** y muévete con **‹ ›** (*Hoy* regresa al actual).
- Total vendido con **comparación contra el periodo anterior**, número de ventas, ticket promedio,
  totales por forma de pago e IVA incluido.
- **Gráfica** de ventas por hora, día o mes. Pasa el cursor sobre una barra para ver el detalle;
  **Ver tabla** muestra los mismos datos en lista.
- **Más vendidos** y, en el día, la lista de **tickets** (tócalos para reimprimir o cancelar).
- **Comisiones por empleado** del periodo (si se registraron).

---

## 15. Ajustes

Solo el dueño.

- **Licencia:** estado, código del equipo y activación (ver sección 2).
- **Versión:** número de versión y **Buscar actualizaciones**. Cuando hay una nueva, arriba aparece
  **Actualizar a X.Y.Z**: se hace un respaldo, se instala y CajaClara se vuelve a abrir sola.
- **Negocio:** nombre, dirección, teléfono, RFC y mensaje al pie del ticket. También **razón social, régimen fiscal y
  código postal**, que salen en el ticket (no sustituye a una factura), y el **logo**, que sale en tickets, cortes,
  cotizaciones y órdenes. El logo no viaja en el ticket por WhatsApp, que es solo texto. **Giro**, **facturación** y
  **crédito y apartados**, **comisiones a empleados** y **bodega y mostrador** (el giro y la facturación piden confirmación; los datos no se borran).
- **Respaldos:**
  - Automáticos al abrir, cada 4 horas y al cerrar cada turno (se guardan los últimos 60).
  - **Respaldar ahora** y **Guardar una copia en…** (por ejemplo una USB).
  - **Copia adicional automática**: elige una carpeta de USB, Google Drive u OneDrive. Cada respaldo
    se copia ahí también y se conservan los últimos 60. Si la USB no está conectada, se avisa en
    "Último problema" y se reintenta en el siguiente respaldo.
  - **Restaurar**: reemplaza todos los datos por los de un respaldo (antes guarda una copia del estado
    actual).
- **Recuperación de acceso:** genera un código de recuperación nuevo (el anterior deja de servir).

---

## 16. Problemas frecuentes

**Olvidé mi PIN (cajero o encargado).** El dueño lo cambia en **Usuarios**.

**El dueño olvidó su PIN.** En el inicio: **¿El dueño olvidó su PIN?** → escribe el código de
recuperación → pon un PIN nuevo. Se genera un código nuevo: guárdalo.

**Perdí el código de recuperación.** En la misma pantalla: **No tengo el código**. Toma foto del QR y
mándala a tu proveedor; después de confirmar que eres el dueño te dictará el código.

**Dice "Modo consulta".** La licencia venció o terminó la demostración. Dueño: **Ajustes → Licencia**.

**El ticket sale muy ancho o pequeño.** En la ventana de impresión elige la impresora térmica y el papel
de 80 mm (o 58 mm), márgenes "Ninguno".

**Cambié de computadora.** En la vieja: **Ajustes → Guardar una copia en…** a una USB. En la nueva:
instala CajaClara, crea el negocio, y en **Ajustes → Restaurar desde archivo…** elige la copia. Pide a
tu proveedor la licencia para el nuevo equipo.

**Se descompuso la computadora.** Si tenías la **copia adicional automática** en USB o Drive, instala en
otra y restaura desde ahí.

---

## 17. Otros equipos: celulares y tablets en el Wi-Fi

Con esto un vendedor o técnico usa CajaClara desde su celular, sin instalar nada y sin internet. Trabaja
sobre los mismos datos de la caja: precios, existencias, clientes, cotizaciones y reparaciones.

**Encenderlo (dueño, en la PC de la caja):**
1. **Ajustes → Otros equipos → Permitir otros equipos**. La primera vez Windows pregunta si permite la
   conexión: acepta en **redes privadas**. Queda encendido aunque cierres y abras CajaClara.
2. Aparecen un **código QR** y una dirección como `http://192.168.1.20:8787`.

**Terminales:** cada equipo conectado (caja adicional o vendedor) ocupa una terminal de tu licencia, y la PC principal
no cuenta. En Ajustes ves cuántas tienes; para agregar más, pídele a tu proveedor una licencia nueva. Durante la
demostración puedes conectar 2. Si dejas de tener lugar para un equipo, se queda sin entrar el último que se conectó.

**Conectar un celular:**
1. Conéctalo al mismo Wi-Fi y escanea el QR, o escribe la dirección en Chrome.
2. En la PC toca **Conectar un equipo**: aparece un código de 6 números que dura 5 minutos.
3. En el celular escribe el nombre del equipo y ese código.
4. Cada persona entra con su nombre y **su PIN**. En el menú de Chrome, **Agregar a la pantalla principal**
   deja un ícono como si fuera app.

**Qué se puede hacer en el celular:**
- **Consulta:** precios y existencias; en celulares, los equipos en tienda con su grado, batería, color y
  precio, y buscar un IMEI para ver su estado y garantía.
- **Cotizaciones:** crearlas con clientes registrados o nuevos, y mandarlas por WhatsApp.
- **Reparaciones u órdenes:** recibir equipos y darles seguimiento.
- **Clientes:** consultarlos y darlos de alta.

**Caja adicional:** en **Ajustes → Otros equipos**, cambia un equipo a **Caja adicional** y recarga la página en él.
Ese equipo ya puede abrir su propio turno, cobrar y hacer su corte, con las mismas formas de pago. Conviene usar una
computadora o tablet, conectada a la red del negocio.

- Los **tickets llevan una sola numeración** entre todas las cajas, para que no se repita un folio.
- Cada caja tiene su **turno y su corte**. En la PC principal, la pestaña **Caja** muestra los turnos abiertos de
  las otras cajas (y permite cerrar uno si esa caja ya no se puede usar) y los cortes de todas.
- Un mismo **IMEI no se puede vender dos veces**: si dos cajas lo intentan a la vez, la segunda recibe un aviso y
  esa venta no se registra.
- Si se pierde la conexión al cobrar, revisa en **Tickets** si la venta quedó antes de repetirla.
- Sigue dependiendo de la PC principal: si se apaga o se cae la red, las cajas adicionales no pueden cobrar.
- **Cancelar ventas** y lo que se indica abajo sigue en la caja principal; la caja adicional puede ver e imprimir sus tickets.

**Lo que se queda en la caja principal:** cancelar ventas, conciliar pagos, abonos y apartados, productos, inventario, reportes, usuarios
y ajustes. Un equipo de vendedor tampoco cobra, ni recibe anticipos ni hace cortes: para cobrar una cotización del celular, en una caja ábrela en **Cotizaciones → Cobrar en caja**. Si
la venta lleva comisión, se propone a quien hizo la cotización.

**Quitar un equipo** (si se pierde el celular o se va un empleado): **Ajustes → Otros equipos → Quitar**. Deja
de entrar de inmediato.

**Si dice "Sin conexión con la caja":** revisa que la PC esté prendida con CajaClara abierto y que el celular
esté en el mismo Wi-Fi. Si la dirección de la PC cambió, vuelve a escanear el QR. Usa Wi-Fi **con contraseña**:
la información viaja sin cifrar dentro de la red del negocio.

---

## 18. Atajos de teclado

| Tecla | Acción |
|---|---|
| **F1 a F11** | Cambiar de pestaña (el número de cada una aparece junto a su nombre). Si hay más de 11 pestañas, las últimas se abren con clic |
| **F12** | Cobrar (en Venta) |
| **Enter** | En el buscador de Venta: agregar el producto o IMEI escaneado; con el buscador vacío: cobrar |
| **Esc** | Cerrar la ventana abierta / limpiar el buscador |
