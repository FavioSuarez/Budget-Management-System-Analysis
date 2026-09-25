# Diccionario de entidades

El modelo conceptual reúne nueve entidades para representar a los participantes, la planificación, los registros presupuestales y las modificaciones.

| Entidad | Identificador | Atributos | Descripción |
| --- | --- | --- | --- |
| Empleado | `id_empleado` | 7 | Representa a los trabajadores de la empresa que participan en el proceso presupuestal como responsables, solicitantes o aprobadores de distintas operaciones presupuestales y de inversión. |
| Área | `id_area` | 4 | Representa las unidades funcionales de la empresa (Comercial, Marketing, Finanzas, Contabilidad, etc.) que participan en la elaboración, ejecución y control del presupuesto. |
| Plan Ventas | `id_plan_ventas` | 8 | Contiene las proyecciones de ventas elaboradas por el área comercial como base para la planificación presupuestal de la empresa, con vigencia de uno o varios años. |
| Presupuesto Anual | `id_presupuesto` | 9 | Representa el presupuesto consolidado de la empresa para un año fiscal específico, desde su elaboración en el kick-off hasta su aprobación por el Directorio y posterior liberación para ejecución. |
| Detalle Gasto | `id_detalle_gasto` | 7 | Almacena el nivel más granular del presupuesto operativo (OPEX), registrando tanto los montos presupuestados como los montos realmente ejecutados por partida presupuestal, diferenciados mediante una dimensión de tipo de registro. |
| Detalle Inversión | `id_detalle_inversion` | 14 | Registra los proyectos de inversión de capital (CAPEX) evaluados por el Comité de Inversiones, incluyendo tanto las inversiones presupuestadas como las ejecutadas, principalmente relacionados con apertura de nuevas tiendas y mejoras de infraestructura. |
| Centro Costo | `id_centro_costo` | 6 | Representa las unidades organizacionales o ubicaciones físicas donde se imputan los gastos e inversiones, tales como tiendas, oficinas o almacenes, permitiendo el control presupuestal por ubicación. |
| Cuenta Contable | `id_cuenta_contable` | 6 | Contiene las cuentas del plan contable utilizadas para clasificar contablemente los gastos, costos, ingresos e inversiones según su naturaleza (energía eléctrica, agua, sueldos, maquinaria, etc.). |
| Modificación Presupuestal | `id_modificacion` | 14 | Registra todas las solicitudes de ajuste presupuestal, ya sean ampliaciones (incremento de monto) o traslados (movimiento entre partidas), incluyendo su justificación y proceso de aprobación con trazabilidad completa. |

Los atributos describen la identificación, clasificación, temporalidad, importes y estados de cada entidad. El conjunto comprende **75 atributos**.

[Diccionario de atributos](data-dictionary.md) · [Modelo conceptual](../docs/03-data-model.md) · [Inicio](../README.md)
