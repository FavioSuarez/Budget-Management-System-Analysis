# Requerimientos funcionales

El sistema contempla **16 requerimientos funcionales**, organizados en **14 eventos de negocio**. Cubren registro presupuestal, consulta histórica, ampliaciones, inversiones CAPEX, ejecución, reportes, aprobación anual y carga al ERP.

## Índice

| RF | Evento | Funcionalidad | Actor principal |
| --- | --- | --- | --- |
| [RF-01](#rf-01) | E01 | Registrar detalle presupuestal | Jefe de Área |
| [RF-02](#rf-02) | E02 | Consultar información histórica | Subgerente de Finanzas / usuario autorizado |
| [RF-03](#rf-03) | E03 | Solicitar ampliación presupuestal | Jefe de Área |
| [RF-04](#rf-04) | E04 | Consultar solicitudes pendientes | Jefe de Área / Subgerente de Finanzas |
| [RF-05](#rf-05) | E04 | Aprobar o rechazar solicitudes | Jefe de Área / Subgerente de Finanzas |
| [RF-06](#rf-06) | E05 | Registrar y evaluar proyectos CAPEX | Responsable de Proyecto |
| [RF-07](#rf-07) | E06 | Consultar proyectos propuestos | Comité de Inversiones |
| [RF-08](#rf-08) | E06 | Registrar aprobación de proyectos CAPEX | Comité de Inversiones |
| [RF-09](#rf-09) | E07 | Solicitar ampliación CAPEX | Responsable de Proyecto |
| [RF-10](#rf-10) | E08 | Resolver ampliaciones CAPEX | Comité de Inversiones |
| [RF-11](#rf-11) | E09 | Registrar ejecución presupuestal mensual | Contabilidad |
| [RF-12](#rf-12) | E10 | Analizar variaciones presupuestales | Subgerente de Finanzas |
| [RF-13](#rf-13) | E11 | Generar estados financieros consolidados | Subgerente de Finanzas |
| [RF-14](#rf-14) | E12 | Registrar aprobación del presupuesto anual | Subgerente de Finanzas |
| [RF-15](#rf-15) | E13 | Cargar el presupuesto aprobado al ERP | Subgerente de Finanzas |
| [RF-16](#rf-16) | E14 | Consultar dashboard presupuestal | Usuario autorizado |

<a id="rf-01"></a>

## RF-01: Registrar detalle presupuestal

El sistema permitirá a cada área registrar líneas de detalle presupuestal ingresando obligatoriamente: cuenta contable, centro de costo, partida presupuestal, periodo mensual (1-12) y monto presupuestado. El sistema validará que la cuenta contable y el centro de costo existan y estén activos antes de permitir el registro.

[Ver DFD](../assets/dfds/rf-01.png).

<a id="rf-02"></a>

## RF-02: Consultar información histórica

El sistema permitirá consultar y visualizar información histórica presupuestal y de ejecución real de años anteriores, filtrando por año fiscal, área, centro de costo y cuenta contable. El sistema mostrará tanto montos presupuestados como ejecutados de periodos cerrados, permitiendo análisis comparativos año a año.

[Ver DFD](../assets/dfds/rf-02.png).

<a id="rf-03"></a>

## RF-03: Solicitar ampliación presupuestal

El sistema permitirá registrar solicitudes de ampliación presupuestal especificando: tipo de detalle afectado (gasto operativo o inversión), identificador del detalle presupuestal origen, monto de ampliación solicitado, motivo breve, justificación detallada, y empleado solicitante. El sistema asignará automáticamente el estado "solicitado" y la fecha de solicitud.

[Ver DFD](../assets/dfds/rf-03.png).

<a id="rf-04"></a>

## RF-04: Consultar solicitudes pendientes

El sistema permitirá al jefe de área responsable y al Subgerente de Finanzas visualizar solicitudes de ampliación presupuestal pendientes, consultar el detalle completo (monto, justificación, impacto en indicadores).

[Ver DFD](../assets/dfds/rf-04.png).

<a id="rf-05"></a>

## RF-05: Aprobar o rechazar solicitudes

El sistema permitirá al jefe de área responsable y al Subgerente de Finanzas registrar su decisión (aprobar o rechazar) junto con observaciones sobre una solicitud de ampliación presupuestal. El sistema actualizará el estado de la solicitud y registrará el empleado aprobador con fecha y hora de decisión.

[Ver DFD](../assets/dfds/rf-05.png).

<a id="rf-06"></a>

## RF-06: Registrar y evaluar proyectos CAPEX

El sistema permitirá registrar proyectos de inversión (CAPEX) propuestos incluyendo: código de proyecto, nombre, descripción, centro de costo asociado, cuenta contable de activo fijo, monto total, empleado responsable, fechas planificadas y justificación de negocio. El sistema calculará automáticamente indicadores financieros (ROI, TIR, VAN) basándose en flujos de caja ingresados, facilitando la evaluación por parte del Comité de Inversiones.

[Ver DFD](../assets/dfds/rf-06.png).

<a id="rf-07"></a>

## RF-07: Consultar proyectos propuestos

El sistema permitirá a los miembros del Comité de Inversiones consultar los proyectos de inversión propuestos, mostrando indicadores financieros (ROI, TIR, VAN), flujos de caja, empleado que propuso el proyecto y monto total, como apoyo a la evaluación.

[Ver DFD](../assets/dfds/rf-07.png).

<a id="rf-08"></a>

## RF-08: Registrar aprobación de proyectos CAPEX

El sistema permitirá que los miembros del Comité de Inversiones registren la aprobación formal de un proyecto de inversión propuesto. Al aprobar, el sistema actualizará el estado del proyecto a "aprobado_comite", registrará la fecha de aprobación, y habilitará el proyecto para su inclusión en el presupuesto anual con su monto total, cronograma de ejecución, líder responsable y centro de costo asignado.

[Ver DFD](../assets/dfds/rf-08.png).

<a id="rf-09"></a>

## RF-09: Solicitar ampliación CAPEX

El sistema permitirá al responsable de un proyecto de inversión registrar solicitudes de ampliación de presupuesto CAPEX especificando el monto adicional requerido y justificación detallada. El sistema recalculará automáticamente y mostrará el impacto en los indicadores financieros (VAN, TIR, ROI) con el nuevo monto, y requerirá aprobación del Comité de Inversiones debido al cambio en la rentabilidad proyectada.

[Ver DFD](../assets/dfds/rf-09.png).

<a id="rf-10"></a>

## RF-10: Resolver ampliaciones CAPEX

El sistema permitirá que los miembros del Comité de Inversiones accedan a las solicitudes de ampliación CAPEX pendientes, visualicen el análisis de impacto en indicadores (VAN, TIR, ROI), consulten la justificación presentada por el responsable del proyecto, y registren la decisión colegiada del comité (aprobar o rechazar) junto con las observaciones de la sesión, fecha de decisión y acta correspondiente. El sistema notificará al responsable del proyecto y al Subgerente de Finanzas sobre la resolución.

[Ver DFD](../assets/dfds/rf-10.png).

<a id="rf-11"></a>

## RF-11: Registrar ejecución presupuestal mensual

El sistema permitirá al área de Contabilidad registrar la ejecución real mensual del presupuesto ingresando: cuenta contable, centro de costo, periodo, monto ejecutado y tipo de registro "ejecutado". El sistema validará automáticamente que la cuenta contable y el centro de costo existan, estén activos y correspondan a combinaciones previamente presupuestadas. Si se detectan inconsistencias, el sistema solicitará su revisión antes de permitir el registro definitivo.

[Ver DFD](../assets/dfds/rf-11.png).

<a id="rf-12"></a>

## RF-12: Analizar variaciones presupuestales

El sistema permitirá al Subgerente de Finanzas generar reportes de variación presupuestal seleccionando el periodo mensual a analizar. El sistema calculará y mostrará las diferencias entre montos ejecutados y presupuestados, desagregados por cuenta contable, centro de costo, área responsable y tipo (OPEX/CAPEX). El reporte incluirá porcentajes de desviación y destacará variaciones que superen umbrales configurables.

[Ver DFD](../assets/dfds/rf-12.png).

<a id="rf-13"></a>

## RF-13: Generar estados financieros consolidados

El sistema permitirá al Subgerente de Finanzas generar estados financieros consolidados (Estado de Resultados, Flujo de Caja, Balance General) ingresando manualmente el año fiscal y mes de corte deseados. El sistema consolidará automáticamente la información presupuestal y de ejecución de todas las áreas, clasificando correctamente ventas (del Plan de Ventas), gastos operativos (Detalle_Gasto) y costos, presentando los reportes en formato estándar para presentación al Directorio.

[Ver DFD](../assets/dfds/rf-13.png).

<a id="rf-14"></a>

## RF-14: Registrar aprobación del presupuesto anual

El sistema permitirá al Subgerente de Finanzas registrar la aprobación formal del presupuesto anual indicando la fecha de sesión del Directorio, número de acta, y observaciones relevantes. Al registrar la aprobación, el sistema actualizará automáticamente el estado del presupuesto de "consolidado" a "aprobado", habilitará las funcionalidades de carga al ERP, y generará notificaciones a todas las áreas responsables sobre el presupuesto autorizado.

[Ver DFD](../assets/dfds/rf-14.png).

<a id="rf-15"></a>

## RF-15: Cargar el presupuesto aprobado al ERP

El sistema permitirá la carga masiva del presupuesto aprobado al módulo presupuestal del ERP mediante interfaz directa, sin necesidad de exportar a Excel. Durante la carga, el sistema validará automáticamente la consistencia y completitud de: centros de costo activos, cuentas contables vigentes, correspondencia entre clasificación OPEX/CAPEX, y totalización correcta. Si se detectan inconsistencias, el sistema generará un reporte detallado de validación para revisar los registros antes de completar la carga.

[Ver DFD](../assets/dfds/rf-15.png).

<a id="rf-16"></a>

## RF-16: Consultar dashboard presupuestal

El sistema proporcionará dashboards interactivos en tiempo real con información presupuestal y de ejecución, accesibles según perfiles de usuario autorizados. Los dashboards permitirán filtrar por área, centro de costo, cuenta contable y periodo, mostrando gráficos de avance presupuestal, principales desviaciones, y alertas de sobre-ejecución. Los datos se actualizarán automáticamente conforme se registren ejecuciones, sin necesidad de generar archivos Excel para distribución.

[Ver DFD](../assets/dfds/rf-16.png).


## Reglas de negocio

| Regla | Relación |
| --- | --- |
| La cuenta contable y el centro de costo deben existir y estar activos para registrar una línea. | RF-01 y RF-11 |
| El periodo del detalle de gasto corresponde a un mes del 1 al 12. | RF-01 |
| Presupuesto y ejecución se diferencian mediante el tipo de registro. | RF-11 y modelo de datos |
| Una solicitud registra monto, motivo, justificación, solicitante, fecha y estado inicial. | RF-03 |
| La decisión conserva aprobador, observaciones y fecha y hora. | RF-05 |
| Una ampliación CAPEX requiere analizar su impacto en rentabilidad y obtener la decisión del comité. | RF-09 y RF-10 |
| La carga al ERP requiere un presupuesto aprobado y validaciones de consistencia. | RF-14 y RF-15 |
| Un traslado relaciona detalles del mismo tipo; las ampliaciones no requieren detalle de destino. | Modificación Presupuestal |

## Criterios de calidad

- **Trazabilidad:** asociar las solicitudes y decisiones con responsables, fechas y estados.
- **Integridad:** validar cuentas, centros de costo y combinaciones presupuestadas.
- **Acceso por rol:** organizar las funciones según las responsabilidades del usuario.
- **Consulta oportuna:** actualizar la información de seguimiento conforme se registre la ejecución.
- **Usabilidad:** mantener navegación consistente, campos obligatorios y retroalimentación durante el registro.

[Modelo de procesos](04-process-model.md) · [Matriz de trazabilidad](traceability.md) · [Inicio](../README.md)
