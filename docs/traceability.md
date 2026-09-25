# Matriz de trazabilidad

La trazabilidad relaciona los eventos del negocio con los requerimientos funcionales, los procesos y las entidades del sistema. Los enlaces permiten consultar el requerimiento y su DFD.

## Eventos de negocio

| Evento | Descripción | Requerimientos |
| --- | --- | --- |
| E01 | Registro de información presupuestal por áreas | RF-01 |
| E02 | Consulta de información histórica | RF-02 |
| E03 | Solicitud de ampliación presupuestal | RF-03 |
| E04 | Revisión y decisión sobre ampliaciones | RF-04 y RF-05 |
| E05 | Registro y evaluación de proyectos de inversión | RF-06 |
| E06 | Consulta y aprobación de proyectos CAPEX | RF-07 y RF-08 |
| E07 | Solicitud de ampliación CAPEX | RF-09 |
| E08 | Evaluación de ampliación CAPEX por el comité | RF-10 |
| E09 | Registro de ejecución mensual | RF-11 |
| E10 | Análisis de variaciones presupuestales | RF-12 |
| E11 | Preparación de estados financieros consolidados | RF-13 |
| E12 | Aprobación anual del presupuesto | RF-14 |
| E13 | Carga del presupuesto aprobado al ERP | RF-15 |
| E14 | Consulta de información presupuestal | RF-16 |

## Requerimientos, procesos y datos

| Evento | Requerimiento | Procesos | Entidades principales | Diagrama |
| --- | --- | --- | --- | --- |
| E01 | [RF-01](02-requirements.md#rf-01) | P-01, P-02 | Detalle Gasto, Cuenta Contable, Centro Costo | [DFD](../assets/dfds/rf-01.png) |
| E02 | [RF-02](02-requirements.md#rf-02) | P-03, P-04 | Detalle Gasto, Detalle Inversión, Presupuesto Anual | [DFD](../assets/dfds/rf-02.png) |
| E03 | [RF-03](02-requirements.md#rf-03) | P-05 | Modificación Presupuestal, Detalle Gasto / Detalle Inversión | [DFD](../assets/dfds/rf-03.png) |
| E04 | [RF-04](02-requirements.md#rf-04) | P-06 | Modificación Presupuestal | [DFD](../assets/dfds/rf-04.png) |
| E04 | [RF-05](02-requirements.md#rf-05) | P-07, P-08 | Modificación Presupuestal, Empleado | [DFD](../assets/dfds/rf-05.png) |
| E05 | [RF-06](02-requirements.md#rf-06) | P-09, P-10 | Detalle Inversión, Centro Costo, Cuenta Contable, Empleado | [DFD](../assets/dfds/rf-06.png) |
| E06 | [RF-07](02-requirements.md#rf-07) | P-11 | Detalle Inversión | [DFD](../assets/dfds/rf-07.png) |
| E06 | [RF-08](02-requirements.md#rf-08) | P-12 | Detalle Inversión | [DFD](../assets/dfds/rf-08.png) |
| E07 | [RF-09](02-requirements.md#rf-09) | P-13, P-14 | Modificación Presupuestal, Detalle Inversión | [DFD](../assets/dfds/rf-09.png) |
| E08 | [RF-10](02-requirements.md#rf-10) | P-15, P-16 | Modificación Presupuestal, Detalle Inversión | [DFD](../assets/dfds/rf-10.png) |
| E09 | [RF-11](02-requirements.md#rf-11) | P-17, P-18 | Detalle Gasto, Cuenta Contable, Centro Costo | [DFD](../assets/dfds/rf-11.png) |
| E10 | [RF-12](02-requirements.md#rf-12) | P-19, P-20 | Presupuesto Anual, Detalle Gasto, Detalle Inversión | [DFD](../assets/dfds/rf-12.png) |
| E11 | [RF-13](02-requirements.md#rf-13) | P-21, P-22 | Plan Ventas, Detalle Gasto, Detalle Inversión | [DFD](../assets/dfds/rf-13.png) |
| E12 | [RF-14](02-requirements.md#rf-14) | P-23, P-24 | Presupuesto Anual | [DFD](../assets/dfds/rf-14.png) |
| E13 | [RF-15](02-requirements.md#rf-15) | P-25, P-26, P-27 | Presupuesto Anual, Detalle Gasto, Detalle Inversión, Centro Costo, Cuenta Contable | [DFD](../assets/dfds/rf-15.png) |
| E14 | [RF-16](02-requirements.md#rf-16) | P-28, P-29, P-30 | Presupuesto Anual, Detalle Gasto, Detalle Inversión | [DFD](../assets/dfds/rf-16.png) |

## Relación con los prototipos

| Prototipo | Requerimientos relacionados | Función representada |
| --- | --- | --- |
| [Gestión de proyectos CAPEX](../assets/wireframes/capex-projects.png) | RF-06, RF-07 | Listado, búsqueda, filtro y acceso al registro de proyectos. |
| [Centros de costo](../assets/wireframes/cost-centers.png) | RF-01, RF-11, RF-12, RF-16 | Acceso a detalles y consulta de presupuesto, ejecución e inversiones. |
| [Solicitud de ampliación](../assets/wireframes/budget-extension.png) | RF-03 | Registro de una solicitud OPEX. |
| [Reporte de ejecución](../assets/wireframes/budget-execution-report.png) | RF-12, RF-16 | Consulta comparativa de importes y variaciones. |

[Requerimientos](02-requirements.md) · [Diccionario de procesos](process-dictionary.md) · [Inicio](../README.md)
