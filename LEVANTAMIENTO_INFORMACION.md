## 1. VISIÓN GENERAL
- Nombre del proyecto: ORQClientes0007
- Tipo de solución global: ORQUESTADOR
- Componentes principales (servicios identificados):
  - WSClientes0114
    - Evidencia: L154 // SET Environment.MSSubflow.servicio  = 'WSClientes0114';
  - WSProductos0009
    - Evidencia: L242 // SET Environment.MSSubflow.servicio      = 'WSProductos0009';

---

## 2. INVENTARIO DE SERVICIOS (WSDL)

### Servicio: ORQClientes0007
- Endpoint: http://localhost:7800/IntegrationBus/soap/ORQClientes0007
  - Evidencia: ORQClientes0007.wsdl L42
- Operación: ActualizarCupoCuentaTransaccion31
  - Evidencia: ORQClientes0007.wsdl L23, L30

#### Operación: ActualizarCupoCuentaTransaccion31

##### Entrada
| Nivel | Campo (ruta completa) | Tipo | Obligatorio | minOccurs | maxOccurs | Origen (XSD/ComplexType) | Restricciones XSD/WSDL |
|---|---|---|---|---|---|---|---|
| 0 | ActualizarCupoCuentaTransaccion31.headerIn | bp:GenericHeaderIn | Sí | 1 | 1 | InlineSchema1.xsd elemento docRoot | Sin restricciones adicionales evidenciadas |
| 0 | ActualizarCupoCuentaTransaccion31.bodyIn | bp:bodyIn | Sí | 1 | 1 | InlineSchema1.xsd elemento docRoot | Sin restricciones adicionales evidenciadas |
| 1 | ActualizarCupoCuentaTransaccion31.bodyIn.ordenante | bp:Ordenante | Sí | 1 | 1 | complexType bodyIn | Sin restricciones adicionales evidenciadas |
| 2 | ActualizarCupoCuentaTransaccion31.bodyIn.ordenante.cif | xsd:string | Sí | 1 | 1 | complexType Ordenante | Sin pattern/length definidos |
| 2 | ActualizarCupoCuentaTransaccion31.bodyIn.ordenante.identificacion | xsd:string | Sí | 1 | 1 | complexType Ordenante | Sin pattern/length definidos |
| 2 | ActualizarCupoCuentaTransaccion31.bodyIn.ordenante.tipoIdentificacion | xsd:string | Sí | 1 | 1 | complexType Ordenante | Sin pattern/length definidos |
| 1 | ActualizarCupoCuentaTransaccion31.bodyIn.transacciones | bp:Transacciones | Sí | 1 | 1 | complexType bodyIn | Sin restricciones adicionales evidenciadas |
| 2 | ActualizarCupoCuentaTransaccion31.bodyIn.transacciones.transaccion | bp:Transaccion | Sí | 1 | unbounded | complexType Transacciones | Colección |
| 3 | ActualizarCupoCuentaTransaccion31.bodyIn.transacciones.transaccion.canal | xsd:string | Sí | 1 | 1 | complexType Transaccion | Sin pattern/length definidos |
| 3 | ActualizarCupoCuentaTransaccion31.bodyIn.transacciones.transaccion.medio | xsd:string | Sí | 1 | 1 | complexType Transaccion | Sin pattern/length definidos |
| 3 | ActualizarCupoCuentaTransaccion31.bodyIn.transacciones.transaccion.aplicacion | xsd:string | Sí | 1 | 1 | complexType Transaccion | Sin pattern/length definidos |
| 3 | ActualizarCupoCuentaTransaccion31.bodyIn.transacciones.transaccion.monto | xsd:string | Sí | 1 | 1 | complexType Transaccion | Sin pattern/length definidos |
| 3 | ActualizarCupoCuentaTransaccion31.bodyIn.transacciones.transaccion.activar | xsd:boolean | Sí | 1 | 1 | complexType Transaccion | Booleano |
| 1 | ActualizarCupoCuentaTransaccion31.bodyIn.flujo | bp:GenericFlow | Sí | 1 | 1 | complexType bodyIn | Tipo externo (GenericSoapORQ.xsd) |

##### Salida
| Nivel | Campo (ruta completa) | Tipo | Obligatorio | minOccurs | maxOccurs | Origen (XSD/ComplexType) | Restricciones XSD/WSDL |
|---|---|---|---|---|---|---|---|
| 0 | ActualizarCupoCuentaTransaccion31Response.headerOut | bp:GenericHeaderIn | Sí | 1 | 1 | InlineSchema1.xsd elemento docRoot | Tipo externo (GenericSoapORQ.xsd) |
| 0 | ActualizarCupoCuentaTransaccion31Response.bodyOut | bp:bodyOut | Sí | 1 | 1 | InlineSchema1.xsd elemento docRoot | Sin restricciones adicionales evidenciadas |
| 1 | ActualizarCupoCuentaTransaccion31Response.bodyOut.flujo | bp:GenericFlow | Sí | 1 | 1 | complexType bodyOut | Tipo externo (GenericSoapORQ.xsd) |
| 0 | ActualizarCupoCuentaTransaccion31Response.error | bp:GenericError | Sí | 1 | 1 | InlineSchema1.xsd elemento docRoot | Tipo externo (GenericSoapORQ.xsd) |

##### ComplexType asociados (si aplica)
| ComplexType | Campo | Tipo | Obligatorio | minOccurs | maxOccurs | Restricciones XSD/WSDL |
|---|---|---|---|---|---|---|
| Ordenante | cif | xsd:string | Sí | 1 | 1 | N/A |
| Ordenante | identificacion | xsd:string | Sí | 1 | 1 | N/A |
| Ordenante | tipoIdentificacion | xsd:string | Sí | 1 | 1 | N/A |
| Transacciones | transaccion | bp:Transaccion | Sí | 1 | unbounded | Colección |
| Transaccion | canal | xsd:string | Sí | 1 | 1 | N/A |
| Transaccion | medio | xsd:string | Sí | 1 | 1 | N/A |
| Transaccion | aplicacion | xsd:string | Sí | 1 | 1 | N/A |
| Transaccion | monto | xsd:string | Sí | 1 | 1 | N/A |
| Transaccion | activar | xsd:boolean | Sí | 1 | 1 | N/A |
| bodyIn | ordenante | bp:Ordenante | Sí | 1 | 1 | N/A |
| bodyIn | transacciones | bp:Transacciones | Sí | 1 | 1 | N/A |
| bodyIn | flujo | bp:GenericFlow | Sí | 1 | 1 | Tipo externo |
| bodyOut | flujo | bp:GenericFlow | Sí | 1 | 1 | Tipo externo |

Evidencias contrato:
- ORQClientes0007.wsdl L13 // <xsd:include schemaLocation="ORQClientes0007_InlineSchema1.xsd"/>
- ORQClientes0007_InlineSchema1.xsd L8 // <xsd:include schemaLocation="../TCSProcesarOrquestacionSOAP/GenericSoapORQ.xsd"/>
- ORQClientes0007_InlineSchema1.xsd L34 // <xsd:complexType name="Ordenante">
- ORQClientes0007_InlineSchema1.xsd L42 // <xsd:complexType name="Transacciones">
- ORQClientes0007_InlineSchema1.xsd L48 // <xsd:complexType name="Transaccion">
- ORQClientes0007_InlineSchema1.xsd L66 // <xsd:complexType name="bodyIn">
- ORQClientes0007_InlineSchema1.xsd L79 // <xsd:complexType name="bodyOut">

---

## 3. INVENTARIO DE XSD
- Estructuras principales (solo nombres)
  - ORQClientes0007.xsd (wrapper de include)
  - ORQClientes0007_InlineSchema1.xsd (modelo principal request/response)
  - IBMdefined/soap.xsd
  - IBMdefined/org/xmlsoap/schemas/soap/envelope/soapenv11.xsd
  - IBMdefined/org/w3/www/xml/_1998/namespace/xml.xsd
- Tipos complejos (solo nombres)
  - Ordenante
  - Transacciones
  - Transaccion
  - bodyIn
  - bodyOut
- Reutilización de esquemas
  - ORQClientes0007.wsdl incluye ORQClientes0007_InlineSchema1.xsd (L13)
  - ORQClientes0007.xsd incluye ORQClientes0007_InlineSchema1.xsd
  - ORQClientes0007_InlineSchema1.xsd incluye ../TCSProcesarOrquestacionSOAP/GenericSoapORQ.xsd (L8)
- Reglas de validación por campo
  - Evidenciado: `minOccurs`/`maxOccurs` en todos los campos definidos localmente.
  - FALTA DETALLE: reglas `pattern`, `length`, `enumeration`, `minInclusive`, `maxInclusive` no aparecen en los XSD locales.
  - Pista: revisar `GenericSoapORQ.xsd` en el repositorio de recursos compartidos `TCSProcesarOrquestacionSOAP`.

---

## 4. ANÁLISIS ESQL

### 4.1 Flujos del servicio
| Flujo (valor de flujoIn.estado) | Línea/evidencia (Línea + comentario con texto ESQL) | Descripción funcional inferida |
|---|---|---|
| iniciar | L87 // IF flujoIn.estado = 'iniciar' THEN | Ejecuta carga de configuración de canales, consulta cuentas activas y luego activa/desactiva cupos por cuenta/canal. |
| no parametrizado | L133-L137 // ELSE ... código='4' mensaje='valor del estado del flujo no parametrizado' | Corta ejecución y retorna error de flujo inválido. |

### 4.2 Validaciones de campos
| Campo (ruta completa) | Tipo | Validación | Código error | Mensaje de error | Acción adicional (si aplica) | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|---|---|---|
| Environment.entrada.bodyIn.ordenante.identificacion | String | `= '' OR = '0'` | 1 | identificación incorrecta | Set tipo=ERROR y RETURN FALSE | L58 // IF ordenante.identificacion = '' OR ordenante.identificacion = '0' THEN |
| Environment.entrada.bodyIn.ordenante.tipoIdentificacion | String | `= '' OR = '0'` | 2 | tipoIdentificacion incorrecta | Set tipo=ERROR y RETURN FALSE | L66 // IF ordenante.tipoIdentificacion = '' OR ordenante.tipoIdentificacion = '0' THEN |

### 4.3 Flujo principal — Main
| Condición | Procedimiento origen | Código respuesta | Mensaje respuesta | Resultado (RETURN) |
|---|---|---|---|---|
| ValidarEntrada falla | Main | Heredado de ValidarEntrada | Heredado de ValidarEntrada | FALSE |
| OrquestarTX falla | Main | Heredado de OrquestarTX o service.error | Heredado de OrquestarTX o service.error | FALSE |
| ValidarEntrada y OrquestarTX exitosos | Main | 0 | OK | TRUE |

Evidencia:
- L26 // CALL ValidarEntrada() INTO respuesta;
- L32 // CALL OrquestarTX() INTO respuesta;
- L38 // SET Environment.salida.error.codigo = '0';
- L39 // SET Environment.salida.error.mensaje = 'OK';

### 4.4 Orquestación de servicios — Secuencia por flujo
| # Orden | Servicio invocado (procedimiento) | Flujo (estado) | Condición de ejecución | Reintento (SI/NO) | Error si falla (origen) | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|---|---|---|
| 1 | GestionarRecursoXML (carga config) | iniciar | Siempre al iniciar | NO | Retorna FALSE y log opcional | L92 // CALL ...GestionarRecursoXML(...) INTO respuesta; |
| 2 | ConsultarCuentasActivas | iniciar | Por cada `transacciones.transaccion[]` con configuración existente en cacheN | NO | Retorna FALSE al primer fallo | L109 // CALL ConsultarCuentasActivas(..., TRUE, canal.monto) INTO respuesta; |
| 3 | ConsultarCuentasActivas | iniciar | Por cada transacción cuando `canal.activar IS FALSE` | NO | Retorna FALSE al primer fallo | L114 // CALL ConsultarCuentasActivas(..., FALSE, canal.monto) INTO respuesta; |
| 4 | ActivarCupoCuentaTransaccion | iniciar | Por cada cuenta acumulada en `OutputLocalEnvironment.cuentas[]` | NO | Retorna FALSE al primer fallo | L127 // CALL ActivarCupoCuentaTransaccion(cuenta.cuenta, cuenta.canales) INTO respuesta; |

Tabla de errores directos:
| Condición | Código error | Mensaje de error | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|
| flujoIn.estado no parametrizado | 4 | valor del estado del flujo no parametrizado | L134-L135 // SET Environment.salida.error.codigo='4' ... mensaje='valor del estado...' |

### 4.5 Lógica de negocio por estado de flujo
#### Flujo: iniciar
| # Paso | Acción | Condición previa | Servicio invocado | Si falla | Si éxito |
|---|---|---|---|---|---|
| 1 | Cargar configuración de canales | flujo= iniciar | GestionarRecursoXML | RETURN FALSE | Continúa |
| 2 | Iterar transacciones de entrada | existe `bodyIn.transacciones.transaccion[]` | ConsultarCuentasActivas | RETURN FALSE | Acumula cuentas/canales en OutputLocalEnvironment |
| 3 | Filtrar cuentas por moneda/producto/estado | Respuesta WSClientes0114 | N/A (lógica local) | Descarta/retorna según validación | Estructura cuentas para activar/desactivar |
| 4 | Iterar cuentas acumuladas | existe `OutputLocalEnvironment.cuentas[]` | ActivarCupoCuentaTransaccion | RETURN FALSE | Fin exitoso de orquestación |

#### Flujo: no parametrizado
| # Paso | Acción | Condición previa | Servicio invocado | Si falla | Si éxito |
|---|---|---|---|---|---|
| 1 | Construir error de flujo inválido | flujo!=iniciar | N/A | RETURN FALSE | N/A |

### 4.6 Pseudocódigo del flujo completo
```text
FUNCTION Main():
  ok = ValidarEntrada()
  IF not ok:
    RETURN FALSE

  ok = OrquestarTX()
  IF not ok:
    RETURN FALSE

  Environment.salida.error.codigo = '0'
  Environment.salida.error.mensaje = 'OK'
  RETURN TRUE

PROCEDURE ValidarEntrada():
  IF ordenante.identificacion is '' OR '0':
    set error(1, 'identificación incorrecta', 'ERROR')
    RETURN FALSE

  IF ordenante.tipoIdentificacion is '' OR '0':
    set error(2, 'tipoIdentificacion incorrecta', 'ERROR')
    RETURN FALSE

  RETURN TRUE

PROCEDURE OrquestarTX():
  IF flujoIn.estado == 'iniciar':
    ok = GestionarRecursoXML(configuraciones)
    IF not ok: RETURN FALSE

    FOR EACH transaccion IN bodyIn.transacciones.transaccion:
      IF exists channel mapping in cache:
        derive ac and bt
        IF transaccion.activar == TRUE:
          ok = ConsultarCuentasActivas(ac, bt, TRUE, transaccion.monto)
        ELSE:
          ok = ConsultarCuentasActivas(ac, bt, FALSE, transaccion.monto)
        IF not ok: RETURN FALSE

    FOR EACH cuenta IN OutputLocalEnvironment.cuentas:
      ok = ActivarCupoCuentaTransaccion(cuenta.cuenta, cuenta.canales)
      IF not ok: RETURN FALSE

    RETURN TRUE

  ELSE:
    set error(4, 'valor del estado del flujo no parametrizado', 'ERROR')
    RETURN FALSE
```

### 4.7 Mapeo de APIs / servicios invocados

##### API: `ConsultarCuentasActivas` → Servicio: `WSClientes0114`
- URL/Endpoint: https://tnd-msa-sp-wsclientes0114-enp.apps.ocptest.uiotest.bpichinchatest.test/IntegrationBus/soap/WSClientes0114
  - Evidencia: WSClientes0114.txt L1
- Método: POST (SOAP)

Tabla de mapeo de entrada:
| Campo request (servicio) | Origen (campo bodyIn / Environment) | Valor fijo (si aplica) | Tipo | Path XML SOAP origen | Path XML SOAP destino | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|---|---|---|
| identificacion | bodyIn.ordenante.identificacion | N/A | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/ordenante/identificacion | /Envelope/Body/ConsultarCuentasActivasCliente01/bodyIn/identificacion | L164 // SET entrada.identificacion = ordenante.identificacion; |
| tipoIdentificacion | bodyIn.ordenante.tipoIdentificacion | N/A | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/ordenante/tipoIdentificacion | /Envelope/Body/ConsultarCuentasActivasCliente01/bodyIn/tipoIdentificacion | L165 // SET entrada.tipoIdentificacion = ordenante.tipoIdentificacion; |
| filtroCuenta | fijo | AH | String | N/A | /Envelope/Body/ConsultarCuentasActivasCliente01/bodyIn/filtroCuenta | L166 // SET entrada.filtroCuenta = 'AH'; |
| canal.referido | parámetro bt (derivado de cacheN) | N/A | String | /Environment/cache/.../BT/id | /Envelope/Body/ConsultarCuentasActivasCliente01/bodyIn/canal/referido | L167 // SET entrada.canal.referido = bt; |
| canal.acceso | parámetro ac (derivado de cacheN) | N/A | String | /Environment/cache/.../ACactivacion/id | /Envelope/Body/ConsultarCuentasActivasCliente01/bodyIn/canal/acceso | L168 // SET entrada.canal.acceso = ac; |

Tabla de mapeo de salida:
| Campo respuesta (servicio) | Destino (campo Environment / salida) | Tipo | Path XML SOAP origen (response) | Path XML SOAP destino (Environment) | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|---|---|
| salida.cuentas.ahorros.ahorro[].numeroCuenta | OutputLocalEnvironment.cuentas.C{numeroCuenta}.cuenta | String | /Envelope/Body/ConsultarCuentasActivasCliente01Response/bodyOut/cuentas/ahorros/ahorro/numeroCuenta | /OutputLocalEnvironment/cuentas/C{numeroCuenta}/cuenta | L200 // SET OutputLocalEnvironment.cuentas.{'C' || cuenta.numeroCuenta}.cuenta = cuenta.numeroCuenta; |
| salida.cuentas.ahorros.ahorro[].activaTransaccionar | lógica condicional local | Boolean | /.../ahorro/activaTransaccionar | N/A (control de flujo) | L192 // IF cuenta.activaTransaccionar IS FALSE THEN |
| salida.cuentas.ahorros.ahorro[].moneda | filtro local con cache config | String | /.../ahorro/moneda | N/A (control de flujo) | L182 // ... propiedades.monedaLocal <> cuenta.moneda |
| error.* | Environment.salida.error | Objeto | /Envelope/Body/ConsultarCuentasActivasCliente01Response/error/* | /Environment/salida/error/* | L175 // SET Environment.salida.error = service.error; |

Manejo de respuesta:
| Resultado | Condición | Acción | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|
| Error | service.error.codigo <> '0' | Propaga `service.error` a salida y retorna FALSE | L174-L176 // IF service.error.codigo <> '0' THEN ... |
| Éxito | service.error.codigo = '0' | Itera cuentas ahorros y construye estructura de activación/desactivación | L178-L229 // DECLARE cuenta... WHILE LASTMOVE... |

##### API: `ActivarCupoCuentaTransaccion` → Servicio: `WSProductos0009`
- URL/Endpoint: https://tnd-msa-sp-wsproductos0009-enp.apps.ocptest.uiotest.bpichinchatest.test/IntegrationBus/soap/WSProductos0009
  - Evidencia: WSProductos0009.txt L1
- Método: POST (SOAP)

Tabla de mapeo de entrada:
| Campo request (servicio) | Origen (campo bodyIn / Environment) | Valor fijo (si aplica) | Tipo | Path XML SOAP origen | Path XML SOAP destino | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|---|---|---|
| numeroCuenta | parámetro cuenta (procede de OutputLocalEnvironment) | N/A | String | /OutputLocalEnvironment/cuentas/C{numeroCuenta}/cuenta | /Envelope/Body/ActualizarMontoTransferenciaCuenta31/bodyIn/numeroCuenta | L252 // SET entrada.numeroCuenta = cuenta; |
| canales.canal[].codigoCanal | canalIn.ac | N/A | String | /OutputLocalEnvironment/.../canales/canal/ac | /Envelope/Body/ActualizarMontoTransferenciaCuenta31/bodyIn/canales/canal/codigoCanal | L261 // SET canal.codigoCanal = canalIn.ac; |
| canales.canal[].montoTransferencia | canalIn.monto | N/A | String | /OutputLocalEnvironment/.../canales/canal/monto | /Envelope/Body/ActualizarMontoTransferenciaCuenta31/bodyIn/canales/canal/montoTransferencia | L262 // SET canal.montoTransferencia = canalIn.monto; |
| canales.canal[].activaTransferencia | canalIn.estado | N/A | Boolean | /OutputLocalEnvironment/.../canales/canal/estado | /Envelope/Body/ActualizarMontoTransferenciaCuenta31/bodyIn/canales/canal/activaTransferencia | L263 // SET canal.activaTransferencia = canalIn.estado; |

Tabla de mapeo de salida:
| Campo respuesta (servicio) | Destino (campo Environment / salida) | Tipo | Path XML SOAP origen (response) | Path XML SOAP destino (Environment) | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|---|---|
| error.* | Environment.salida.error | Objeto | /Envelope/Body/*Response/error/* | /Environment/salida/error/* | L272 // SET Environment.salida.error = service.error; |
| bodyOut.* | FALTA DETALLE | FALTA DETALLE | FALTA DETALLE | FALTA DETALLE | Pista: validar contrato real de `ActualizarMontoTransferenciaCuenta31` en repositorio WSProductos0009 |

Manejo de respuesta:
| Resultado | Condición | Acción | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|
| Error | service.error.codigo <> '0' | Propaga `service.error` y retorna FALSE | L271-L273 // IF service.error.codigo <> '0' THEN ... |
| Éxito | service.error.codigo = '0' | Retorna TRUE sin mapeo adicional | L275 // RETURN TRUE; |

### 4.8 Mapeo de entrada del orquestador
| Campo (ruta bodyIn) | Tipo | Path XML SOAP (request orquestador) | Descripción / Uso | Tipo de evidencia (directa/inferida) |
|---|---|---|---|---|
| bodyIn.ordenante.cif | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/ordenante/cif | Identificador CIF del ordenante (no usado en lógica ESQL de validación) | directa |
| bodyIn.ordenante.identificacion | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/ordenante/identificacion | Clave de consulta de cuentas activas | directa |
| bodyIn.ordenante.tipoIdentificacion | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/ordenante/tipoIdentificacion | Tipo documento para consulta WSClientes0114 | directa |
| bodyIn.transacciones.transaccion.canal | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/transacciones/transaccion/canal | Selección de canal a parametrizar | directa |
| bodyIn.transacciones.transaccion.medio | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/transacciones/transaccion/medio | Subsegmentación de canal | directa |
| bodyIn.transacciones.transaccion.aplicacion | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/transacciones/transaccion/aplicacion | Clave de aplicación para resolver AC/BT | directa |
| bodyIn.transacciones.transaccion.monto | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/transacciones/transaccion/monto | Monto de activación de cupo | directa |
| bodyIn.transacciones.transaccion.activar | Boolean | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/transacciones/transaccion/activar | Define activación vs desactivación de cupo | directa |
| bodyIn.flujo.estado | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31/bodyIn/flujo/estado | Controla ruta de orquestación (`iniciar`) | inferida |

Evidencias:
- L82 // DECLARE flujoIn REFERENCE TO Environment.entrada.bodyIn.flujo;
- L101 // DECLARE canal REFERENCE TO Environment.entrada.bodyIn.transacciones.transaccion[1];
- ORQClientes0007_InlineSchema1.xsd L68-L74

### 4.9 Mapeo de salida del orquestador
| Campo (ruta Environment.salida) | Tipo | Path XML SOAP (response orquestador) | Origen del dato (servicio / validación / fijo) | Tipo de evidencia (directa/inferida) |
|---|---|---|---|---|
| Environment.salida.error.codigo | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31Response/error/codigo | Validaciones (1,2), flujo inválido (4), éxito (`0`), o propagación de service.error | directa |
| Environment.salida.error.mensaje | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31Response/error/mensaje | Validaciones, flujo inválido, éxito (`OK`) o service.error | directa |
| Environment.salida.error.tipo | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31Response/error/tipo | Validaciones/flujo inválido (`ERROR`) o propagación de service.error | directa |
| Environment.salida.error.recurso | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31Response/error/recurso | Solo por propagación de service.error desde servicios dependientes | inferida |
| Environment.salida.error.componente | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31Response/error/componente | Solo por propagación de service.error desde servicios dependientes | inferida |
| Environment.salida.error.backend | String | /Envelope/Body/ActualizarCupoCuentaTransaccion31Response/error/backend | Solo por propagación de service.error desde servicios dependientes | inferida |
| Environment.salida.bodyOut.flujo | bp:GenericFlow | /Envelope/Body/ActualizarCupoCuentaTransaccion31Response/bodyOut/flujo | FALTA DETALLE en ESQL (no se asigna explícitamente) | inferida |

Evidencias:
- L38-L39 // success code/message
- L59-L61, L67-L69, L134-L136 // errores de validación y flujo
- L175, L272 // propagación `Environment.salida.error = service.error`
- Pista bodyOut: revisar nodos de salida en subflow `et_msSoap` y mapping node del flujo IIB.

### 4.10 Consolidado de mensajes de error
| # | Código error | Mensaje de error | Tipo | Origen (procedimiento/función) | Condición que lo genera | Línea/evidencia (Línea + comentario con texto ESQL) |
|---|---|---|---|---|---|---|
| 1 | 1 | identificación incorrecta | ERROR | ValidarEntrada | `ordenante.identificacion = '' OR '0'` | L59-L61 // SET Environment.salida.error.codigo='1'... |
| 2 | 2 | tipoIdentificacion incorrecta | ERROR | ValidarEntrada | `ordenante.tipoIdentificacion = '' OR '0'` | L67-L69 // SET Environment.salida.error.codigo='2'... |
| 3 | 4 | valor del estado del flujo no parametrizado | ERROR | OrquestarTX | `flujoIn.estado` distinto de `iniciar` | L134-L136 // SET Environment.salida.error.codigo='4'... |
| 4 | service.error.codigo | service.error.mensaje | service.error.tipo | ConsultarCuentasActivas | Respuesta dependiente con código distinto de 0 | L174-L176 // IF service.error.codigo <> '0' THEN ... |
| 5 | service.error.codigo | service.error.mensaje | service.error.tipo | ActivarCupoCuentaTransaccion | Respuesta dependiente con código distinto de 0 | L271-L273 // IF service.error.codigo <> '0' THEN ... |

Ordenación: códigos fijos ascendentes y luego errores propagados.

---

## 12. RESUMEN GLOBAL DE SERVICIOS INVOCADOS
| # | Nombre del servicio | Procedimiento ESQL que lo invoca | Flujo(s) donde se usa | Tipo (SOAP/REST/MQ) | URL / Endpoint | Resumen de función |
|---|---|---|---|---|---|---|
| 1 | WSClientes0114 | ConsultarCuentasActivas | iniciar | SOAP | https://tnd-msa-sp-wsclientes0114-enp.apps.ocptest.uiotest.bpichinchatest.test/IntegrationBus/soap/WSClientes0114 | Consulta cuentas activas del cliente y devuelve cuentas para decidir activación/desactivación de cupo. |
| 2 | WSProductos0009 | ActivarCupoCuentaTransaccion | iniciar | SOAP | https://tnd-msa-sp-wsproductos0009-enp.apps.ocptest.uiotest.bpichinchatest.test/IntegrationBus/soap/WSProductos0009 | Actualiza monto/estado de transferencia por canal para cada cuenta seleccionada. |

---

## 13. DTOs DE ENTRADA Y SALIDA POR SERVICIO

### 13.1 Matriz consolidada — Campos de entrada por servicio
| Servicio | Operación | Campo de entrada (ruta DTO) | Tipo Java | Obligatorio | Origen (bodyIn/Environment/fijo/transformación) | Evidencia (línea/sección + comentario ESQL cuando aplique) |
|---|---|---|---|---|---|---|
| WSClientes0114 | ConsultarCuentasActivasCliente01 | request.identificacion | String | Sí | bodyIn.ordenante.identificacion | L164 // SET entrada.identificacion = ordenante.identificacion; |
| WSClientes0114 | ConsultarCuentasActivasCliente01 | request.tipoIdentificacion | String | Sí | bodyIn.ordenante.tipoIdentificacion | L165 // SET entrada.tipoIdentificacion = ordenante.tipoIdentificacion; |
| WSClientes0114 | ConsultarCuentasActivasCliente01 | request.filtroCuenta | String | Sí | fijo | L166 // SET entrada.filtroCuenta = 'AH'; |
| WSClientes0114 | ConsultarCuentasActivasCliente01 | request.canal.referido | String | Sí | transformación (bt desde cacheN) | L167 // SET entrada.canal.referido = bt; |
| WSClientes0114 | ConsultarCuentasActivasCliente01 | request.canal.acceso | String | Sí | transformación (ac desde cacheN) | L168 // SET entrada.canal.acceso = ac; |
| WSProductos0009 | ActualizarMontoTransferenciaCuenta31 | request.numeroCuenta | String | Sí | OutputLocalEnvironment.cuentas | L252 // SET entrada.numeroCuenta = cuenta; |
| WSProductos0009 | ActualizarMontoTransferenciaCuenta31 | request.canales.canal.codigoCanal | String | Sí | canales.canal.ac | L261 // SET canal.codigoCanal = canalIn.ac; |
| WSProductos0009 | ActualizarMontoTransferenciaCuenta31 | request.canales.canal.montoTransferencia | String | Sí | canales.canal.monto | L262 // SET canal.montoTransferencia = canalIn.monto; |
| WSProductos0009 | ActualizarMontoTransferenciaCuenta31 | request.canales.canal.activaTransferencia | Boolean | Sí | canales.canal.estado | L263 // SET canal.activaTransferencia = canalIn.estado; |

### 13.2 Matriz consolidada — Campos de salida por servicio
| Servicio | Operación | Campo de salida (ruta DTO) | Tipo Java | Destino (Environment.salida / tempDatos / otro) | Origen de respuesta (bodyOut/error/header) | Evidencia (línea/sección + comentario ESQL cuando aplique) |
|---|---|---|---|---|---|---|
| WSClientes0114 | ConsultarCuentasActivasCliente01 | response.bodyOut.cuentas.ahorros.ahorro.numeroCuenta | String | tempDatos (OutputLocalEnvironment.cuentas) | bodyOut | L178, L200 // DECLARE cuenta ... SET OutputLocalEnvironment... |
| WSClientes0114 | ConsultarCuentasActivasCliente01 | response.bodyOut.cuentas.ahorros.ahorro.activaTransaccionar | Boolean | control lógico interno | bodyOut | L192 // IF cuenta.activaTransaccionar IS FALSE THEN |
| WSClientes0114 | ConsultarCuentasActivasCliente01 | response.error.codigo | String | Environment.salida.error.codigo | error | L174-L176 // IF service.error.codigo <> '0' THEN ... |
| WSClientes0114 | ConsultarCuentasActivasCliente01 | response.error.mensaje | String | Environment.salida.error.mensaje | error | L175 // SET Environment.salida.error = service.error; |
| WSClientes0114 | ConsultarCuentasActivasCliente01 | response.error.tipo | String | Environment.salida.error.tipo | error | L175 // SET Environment.salida.error = service.error; |
| WSProductos0009 | ActualizarMontoTransferenciaCuenta31 | response.error.codigo | String | Environment.salida.error.codigo | error | L271-L273 // IF service.error.codigo <> '0' THEN ... |
| WSProductos0009 | ActualizarMontoTransferenciaCuenta31 | response.error.mensaje | String | Environment.salida.error.mensaje | error | L272 // SET Environment.salida.error = service.error; |
| WSProductos0009 | ActualizarMontoTransferenciaCuenta31 | response.error.tipo | String | Environment.salida.error.tipo | error | L272 // SET Environment.salida.error = service.error; |
| WSProductos0009 | ActualizarMontoTransferenciaCuenta31 | response.bodyOut | String // TODO: verificar tipo | FALTA DETALLE | FALTA DETALLE | Pista: contrato real WSProductos0009 para `ActualizarMontoTransferenciaCuenta31Response` |

### 13.3 Detalle DTO por servicio

#### Servicio: WSClientes0114

**DTO Request:**
| Campo | Tipo Java | Obligatorio | Origen (campo bodyIn / valor fijo / transformación) | Descripción |
|---|---|---|---|---|
| identificacion | String | Sí | bodyIn.ordenante.identificacion | Identificador del cliente |
| tipoIdentificacion | String | Sí | bodyIn.ordenante.tipoIdentificacion | Tipo de documento |
| filtroCuenta | String | Sí | fijo='AH' | Filtro de tipo de cuenta |
| canal | ConsultarCuentasActivasCanalDto | Sí | transformación | Datos de referido/acceso |

**DTO Response:**
| Campo | Tipo Java | Descripción | Destino (campo Environment.salida) |
|---|---|---|---|
| bodyOut | ConsultarCuentasActivasBodyOutDto | Cuentas del cliente | temp OutputLocalEnvironment |
| error | ErrorResponseGeneralDTO | Estado técnico/negocio del servicio | Environment.salida.error |

**Desglose recursivo completo (sin omitir clases internas):**
- ConsultarCuentasActivasRequestDto
  - identificacion: String
  - tipoIdentificacion: String
  - filtroCuenta: String
  - canal: ConsultarCuentasActivasCanalDto
- ConsultarCuentasActivasCanalDto
  - referido: String
  - acceso: String
- ConsultarCuentasActivasResponseDto
  - bodyOut: ConsultarCuentasActivasBodyOutDto
  - error: ErrorResponseGeneralDTO
- ConsultarCuentasActivasBodyOutDto
  - cuentas: ConsultarCuentasActivasCuentasDto
- ConsultarCuentasActivasCuentasDto
  - ahorros: ConsultarCuentasActivasAhorrosDto
- ConsultarCuentasActivasAhorrosDto
  - ahorro: List<ConsultarCuentasActivasAhorroDto>
- ConsultarCuentasActivasAhorroDto
  - numeroCuenta: String
  - moneda: String
  - producto: String
  - subProducto: String
  - activaTransaccionar: Boolean

#### Servicio: WSProductos0009

**DTO Request:**
| Campo | Tipo Java | Obligatorio | Origen (campo bodyIn / valor fijo / transformación) | Descripción |
|---|---|---|---|---|
| numeroCuenta | String | Sí | OutputLocalEnvironment.cuentas | Cuenta a actualizar |
| canales | List<ActualizarMontoTransferenciaCanalDto> | Sí | canales.canal[] | Lista de canales a activar/desactivar |

**DTO Response:**
| Campo | Tipo Java | Descripción | Destino (campo Environment.salida) |
|---|---|---|---|
| error | ErrorResponseGeneralDTO | Estado técnico/negocio del servicio | Environment.salida.error |
| bodyOut | String // TODO: verificar tipo | No usado en ESQL | FALTA DETALLE |

**Desglose recursivo completo (sin omitir clases internas):**
- ActualizarMontoTransferenciaCuenta31RequestDto
  - numeroCuenta: String
  - canales: List<ActualizarMontoTransferenciaCanalDto>
- ActualizarMontoTransferenciaCanalDto
  - codigoCanal: String
  - montoTransferencia: String
  - activaTransferencia: Boolean
- ActualizarMontoTransferenciaCuenta31ResponseDto
  - error: ErrorResponseGeneralDTO
  - bodyOut: String // TODO: verificar tipo
- FALTA DETALLE
  - Pista: WSProductos0009.txt presenta un response ejemplo inconsistente (`OperacionDemograficosCliente51Response`) y no confirma estructura de `ActualizarMontoTransferenciaCuenta31Response`.

---

## 14. JSON REQUEST DE EJEMPLO POR SERVICIO

```json
// Servicio: WSClientes0114
// Procedimiento: ConsultarCuentasActivas
{
  "identificacion": "1701077511",
  "tipoIdentificacion": "0001",
  "filtroCuenta": "AH",
  "canal": {
    "referido": "06",
    "acceso": "05"
  }
}
```

```json
// Servicio: WSProductos0009
// Procedimiento: ActivarCupoCuentaTransaccion
{
  "numeroCuenta": "2204049481",
  "canales": [
    {
      "codigoCanal": "05",
      "montoTransferencia": "5000",
      "activaTransferencia": true
    }
  ]
}
```

---

## 15. CLASES CANDIDATAS

### Servicio: WSClientes0114
| Clase candidata | Tipo (Request/Response/Anidada/Error) | Origen (WSDL/XSD orquestador / Servicio dependencia / ESQL) | Campos principales (resumen) | Observaciones |
|---|---|---|---|---|
| ConsultarCuentasActivasRequestDto | Request | ESQL + WSClientes0114.txt | identificacion, tipoIdentificacion, filtroCuenta, canal | Mapea entrada construida en L164-L168 |
| ConsultarCuentasActivasCanalDto | Anidada | ESQL + WSClientes0114.txt | referido, acceso | Equivale a bodyIn.canal |
| ConsultarCuentasActivasResponseDto | Response | ESQL + WSClientes0114.txt | bodyOut, error | bodyOut se usa para poblar OutputLocalEnvironment |
| ConsultarCuentasActivasBodyOutDto | Anidada | WSClientes0114.txt | cuentas | Nodo raíz de respuesta funcional |
| ConsultarCuentasActivasCuentasDto | Anidada | WSClientes0114.txt | ahorros | El ESQL procesa ahorro[] |
| ConsultarCuentasActivasAhorrosDto | Anidada | WSClientes0114.txt | ahorro(List) | Colección |
| ConsultarCuentasActivasAhorroDto | Anidada | ESQL + WSClientes0114.txt | numeroCuenta, moneda, producto, subProducto, activaTransaccionar | Campos usados en filtros/reglas |
| ErrorResponseGeneralDTO | Error | ESQL + servicios dependencia | codigo, mensaje, tipo, recurso, componente, backend | Clase común reutilizable |

### Servicio: WSProductos0009
| Clase candidata | Tipo (Request/Response/Anidada/Error) | Origen (WSDL/XSD orquestador / Servicio dependencia / ESQL) | Campos principales (resumen) | Observaciones |
|---|---|---|---|---|
| ActualizarMontoTransferenciaCuenta31RequestDto | Request | ESQL + WSProductos0009.txt | numeroCuenta, canales(List) | Construido en L252-L263 |
| ActualizarMontoTransferenciaCanalDto | Anidada | ESQL + WSProductos0009.txt | codigoCanal, montoTransferencia, activaTransferencia | Iterado en L255-L264 |
| ActualizarMontoTransferenciaCuenta31ResponseDto | Response | ESQL + WSProductos0009.txt | error, bodyOut | bodyOut no evidenciado de forma confiable |
| ErrorResponseGeneralDTO | Error | ESQL + servicios dependencia | codigo, mensaje, tipo, recurso, componente, backend | Clase común reutilizable |
| FALTA DETALLE | Anidada | Servicio dependencia | PENDIENTE | Pista: confirmar contrato real WSProductos0009 en repositorio técnico del servicio |

Clase candidata obligatoria:
`ErrorResponseGeneralDTO`

Campos mínimos:
- `codigo: String`
- `mensaje: String`
- `tipo: String`

Campos opcionales (evidenciados en servicios dependencia):
- `recurso: String`
- `componente: String`
- `backend: String`

---

## Resumen de completitud de checklists

### Paso 1 — 01_vision_general
- [x] Nombre del proyecto identificado
- [x] Tipo de solución = ORQUESTADOR
- [x] Lista de servicios identificados desde ESQL (vía MSSubflow.servicio)
- [x] Sección 1 generada

### Paso 2 — 02_contratos_wsdl_xsd
- [x] WSDL del proyecto inventariado
- [x] Operación documentada con entrada/salida/complexType
- [x] Restricciones XSD extraídas (`minOccurs`/`maxOccurs`)
- [x] Inventario XSD completo del repositorio
- [x] Secciones 2 y 3 generadas
- [ ] FALTA DETALLE: restricciones avanzadas (pattern/enumeration/length) en esquemas externos

### Paso 3 — 03_analisis_esql_flujos_validaciones
- [x] Flujos identificados (4.1)
- [x] Validaciones documentadas (4.2)
- [x] Flujo Main documentado (4.3)
- [x] Orquestación por estado documentada (4.4)
- [x] Lógica por flujo (4.5)
- [x] Pseudocódigo generado (4.6)

### Paso 4 — 04_mapeo_apis_servicios
- [x] APIs/procedimientos del ESQL documentados
- [x] Mapeo de entrada por API
- [x] Mapeo de salida por API
- [x] Manejo de respuesta documentado
- [x] Paths XML SOAP origen/destino completados
- [x] Sección 4.7 generada

### Paso 5 — 05_mapeo_entrada_salida_errores
- [x] Campos de entrada del orquestador documentados (4.8)
- [x] Campos de salida documentados (4.9)
- [x] Consolidado de errores completo (4.10)
- [x] Secciones 4.8, 4.9 y 4.10 generadas
- [ ] FALTA DETALLE: asignación explícita de `bodyOut` en ESQL

### Paso 6 — 06_resumen_servicios_dtos
- [x] Tabla consolidada de servicios (sección 12)
- [x] Matriz de DTOs entrada/salida por servicio (13.1/13.2)
- [x] JSON request por servicio (sección 14)
- [x] Clases candidatas por servicio (sección 15)
- [x] Clase general `ErrorResponseGeneralDTO` incluida
- [x] Cobertura 1:1 por servicio en 13.3/14/15
- [ ] FALTA DETALLE: response confiable de `ActualizarMontoTransferenciaCuenta31`
