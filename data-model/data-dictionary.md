# Diccionario de atributos

El diccionario define los 75 atributos de las nueve entidades del modelo conceptual. Cada entrada incluye el nombre del atributo, su identificador técnico y su significado dentro del sistema.

## Empleado

| Atributo | Nombre técnico | Descripción |
| --- | --- | --- |
| id empleado | `id_empleado` | Identificador único del empleado en el sistema (clave primaria). |
| nombre | `nombre` | Nombre(s) del empleado. |
| apellidos | `apellidos` | Apellido(s) del empleado. |
| email | `email` | Correo electrónico corporativo del empleado. |
| cargo | `cargo` | Posición o puesto que desempeña en la organización (ej. Gerente, Jefe, Asistente, Subgerente). |
| fecha ingreso | `fecha_ingreso` | Fecha de incorporación del empleado a la empresa. |
| estado | `estado` | Estado laboral actual del empleado (ej. activo, inactivo, suspendido). |

## Área

| Atributo | Nombre técnico | Descripción |
| --- | --- | --- |
| id area | `id_area` | Identificador único del área funcional (clave primaria). |
| nombre area | `nombre_area` | Nombre oficial del área (ej. Comercial, Marketing, Finanzas, Contabilidad, Gestión Humana, TI). |
| descripción | `descripcion` | Descripción de las funciones y responsabilidades principales del área. |
| tipo area | `tipo_area` | Clasificación del área según su naturaleza (ej. operativa, administrativa, soporte). |

## Plan Ventas

| Atributo | Nombre técnico | Descripción |
| --- | --- | --- |
| id plan ventas | `id_plan_ventas` | Identificador único del plan de ventas (clave primaria). |
| año inicio | `ano_inicio` | Año de inicio de vigencia del plan de ventas. |
| año fin | `ano_fin` | Año de finalización del plan (para planes multianuales como 2026-2028). |
| tipo registro | `tipo_registro` | Dimensión que diferencia si es proyección presupuestada o venta real ejecutada (valores: 'presupuestado', 'real'). |
| monto proyectado | `monto_proyectado` | Monto total de ventas proyectadas o ejecutadas para el periodo. |
| fecha creacion | `fecha_creacion` | Fecha en que se creó o registró el plan de ventas. |
| estado | `estado` | Estado actual del plan (ej. borrador, aprobado, vigente, cerrado). |
| observaciones | `observaciones` | Comentarios o aclaraciones adicionales sobre el plan de ventas. |

## Presupuesto Anual

| Atributo | Nombre técnico | Descripción |
| --- | --- | --- |
| id presupuesto | `id_presupuesto` | Identificador único del presupuesto anual (clave primaria). |
| año | `ano` | Año fiscal al que corresponde el presupuesto. |
| monto total opex | `monto_total_opex` | Monto total consolidado de gastos operativos (suma de todos los Detalle_Gasto presupuestados). |
| monto total capex | `monto_total_capex` | Monto total consolidado de inversiones de capital (suma de todos los Detalle_Inversión presupuestados). |
| fecha kickoff | `fecha_kickoff` | Fecha de la reunión inicial de arranque del proceso presupuestal donde se definieron roles y responsabilidades. |
| fecha aprobación | `fecha_aprobacion` | Fecha en que el Directorio aprobó formalmente el presupuesto. |
| fecha carga sistema | `fecha_carga_sistema` | Fecha en que el presupuesto aprobado fue cargado al sistema ERP. |
| fecha liberacion | `fecha_liberacion` | Fecha en que el presupuesto fue liberado para ejecución operativa. |
| estado | `estado` | Estado del presupuesto (ej. en_elaboracion, consolidado, aprobado, vigente, cerrado). |

## Detalle Gasto

| Atributo | Nombre técnico | Descripción |
| --- | --- | --- |
| id detalle gasto | `id_detalle_gasto` | Identificador único del detalle de gasto (clave primaria). |
| partida presupuestal | `partida_presupuestal` | Descripción específica de la partida de gasto (ej. Mantenimiento de vehículos, Servicios públicos, Sueldos administrativos). |
| periodo | `periodo` | Número del mes dentro del año fiscal al que corresponde el registro (1=enero, 2=febrero, ..., 12=diciembre). |
| tipo registro | `tipo_registro` | Dimensión diferenciadora que indica si es un monto presupuestado o realmente ejecutado (valores: 'presupuestado', 'ejecutado'). |
| monto | `monto` | Monto en soles del gasto presupuestado o ejecutado para el periodo específico. |
| fecha registro | `fecha_registro` | Fecha en que se registró la información en el sistema. |
| observaciones | `observaciones` | Comentarios, aclaraciones o justificaciones adicionales sobre el detalle de gasto. |

## Detalle Inversión

| Atributo | Nombre técnico | Descripción |
| --- | --- | --- |
| id detalle inversión | `id_detalle_inversion` | Identificador único del detalle de inversión (clave primaria). |
| código proyecto | `codigo_proyecto` | Código único de identificación del proyecto (ej. CAPEX-2026-001). |
| nombre proyecto | `nombre_proyecto` | Nombre descriptivo del proyecto de inversión (ej. Apertura Tienda Manchay, Renovación Equipos Planta). |
| descripción | `descripcion` | Descripción detallada del alcance, objetivos y entregables del proyecto. |
| tipo registro | `tipo_registro` | Dimensión diferenciadora que indica si es inversión presupuestada o ejecutada (valores: 'presupuestado', 'ejecutado'). |
| monto | `monto` | Monto en soles de la inversión presupuestada o ejecutada. |
| roi proyectado | `roi_proyectado` | Retorno sobre la inversión proyectado expresado en porcentaje. |
| tir proyectado | `tir_proyectado` | Tasa Interna de Retorno proyectada expresada en porcentaje. |
| van proyectado | `van_proyectado` | Valor Actual Neto proyectado del proyecto en soles. |
| fecha inicio planificada | `fecha_inicio_planificada` | Fecha estimada de inicio de ejecución del proyecto. |
| fecha fin planificada | `fecha_fin_planificada` | Fecha estimada de finalización del proyecto. |
| periodo recuperacion meses | `periodo_recuperacion_meses` | Tiempo estimado en meses para recuperar la inversión inicial. |
| estado | `estado` | Estado actual del proyecto (ej. propuesto, aprobado_comite, en_ejecucion, completado, cancelado). |
| justificación negocio | `justificacion_negocio` | Razón estratégica, comercial o técnica que sustenta la necesidad de la inversión. |

## Centro Costo

| Atributo | Nombre técnico | Descripción |
| --- | --- | --- |
| id centro costo | `id_centro_costo` | Identificador único del centro de costo (clave primaria). |
| código centro costo | `codigo_centro_costo` | Código alfanumérico formal del centro de costo según nomenclatura contable (ej. CC-001, CC-MARANGA). |
| nombre | `nombre` | Nombre descriptivo del centro de costo (ej. Tienda Maranga, Tienda Surquillo, Oficina Central, Almacén Arequipa). |
| tipo | `tipo` | Clasificación del centro de costo según su naturaleza (ej. tienda, almacén, oficina, planta_produccion). |
| ubicación | `ubicacion` | Dirección física o ubicación geográfica del centro de costo. |
| estado | `estado` | Estado operativo del centro de costo (ej. activo, inactivo, en_construccion). |

## Cuenta Contable

| Atributo | Nombre técnico | Descripción |
| --- | --- | --- |
| id cuenta contable | `id_cuenta_contable` | Identificador único de la cuenta contable (clave primaria). |
| codigo cuenta | `codigo_cuenta` | Código numérico de la cuenta según el plan contable general (ej. 6361 para Energía Eléctrica, 6211 para Sueldos). |
| nombre cuenta | `nombre_cuenta` | Nombre descriptivo de la cuenta contable (ej. Energía Eléctrica, Agua, Teléfono, Sueldos, Publicidad Digital). |
| tipo cuenta | `tipo_cuenta` | Clasificación de la cuenta según su naturaleza contable (valores: gasto, costo, ingreso, activo_fijo). |
| categoría | `categoria` | Agrupación funcional de la cuenta (ej. servicios_publicos, personal, suministros, marketing, inversiones). |
| estado | `estado` | Estado de vigencia de la cuenta en el plan contable (ej. activa, inactiva, obsoleta). |

## Modificación Presupuestal

| Atributo | Nombre técnico | Descripción |
| --- | --- | --- |
| id modificación | `id_modificacion` | Identificador único de la solicitud de modificación presupuestal (clave primaria). |
| tipo modificación | `tipo_modificacion` | Tipo de operación presupuestal realizada (valores: 'ampliacion' = incremento de monto, 'traslado' = movimiento entre partidas). |
| tipo detalle origen | `tipo_detalle_origen` | Indica si la modificación afecta un Detalle_Gasto o Detalle_Inversión en el origen (valores: 'gasto', 'inversion'). |
| id detalle origen | `id_detalle_origen` | Identificador del detalle (gasto o inversión) desde el cual se solicita la modificación (clave foránea polimórfica). |
| tipo detalle destino | `tipo_detalle_destino` | Indica si el destino es un Detalle_Gasto o Detalle_Inversión (valores: 'gasto', 'inversion', NULL para ampliaciones). Debe ser del mismo tipo que el origen (gasto con gasto, inversión con inversión). Solo aplica para traslados; en ampliaciones este campo es NULL. |
| id detalle destino | `id_detalle_destino` | Identificador del detalle (gasto o inversión) hacia el cual se traslada el presupuesto (clave foránea polimórfica, NULL en ampliaciones). |
| monto | `monto` | Monto en soles que se amplía o traslada entre partidas. |
| motivo | `motivo` | Razón breve y concisa que justifica la necesidad de la modificación. |
| justificación detallada | `justificacion_detallada` | Explicación completa y documentada que sustenta la solicitud de modificación presupuestal. |
| fecha solicitud | `fecha_solicitud` | Fecha en que se registró formalmente la solicitud en el sistema. |
| fecha aprobación | `fecha_aprobacion` | Fecha en que la solicitud fue aprobada o rechazada por el responsable autorizado. |
| fecha ejecución | `fecha_ejecucion` | Fecha en que la modificación fue efectivamente aplicada al presupuesto en el sistema ERP. |
| estado | `estado` | Estado actual de la solicitud (ej. solicitado, en_revision, aprobado, rechazado, ejecutado). |
| impacto indicadores | `impacto_indicadores` | Descripción del impacto de la modificación en indicadores financieros (especialmente para ampliaciones CAPEX que afectan ROI, TIR, VAN). |


[Diccionario de entidades](entities.md) · [Modelo conceptual](../docs/03-data-model.md) · [Inicio](../README.md)
