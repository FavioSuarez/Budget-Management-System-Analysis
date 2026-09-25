# Diccionario de procesos

El catálogo describe 30 procesos asociados a los requerimientos funcionales. Incluye operaciones de registro, consulta, filtrado, validación, cálculo, aprobación, consolidación y transferencia de información.

| Código | Proceso | Descripción |
| --- | --- | --- |
| P-01 | Registrar detalle presupuestal | Captura y almacena una nueva línea de detalle presupuestal ingresada por el jefe de área, incluyendo partida, cuenta contable, centro de costo, periodo y monto presupuestado. |
| P-02 | Validar cuenta y centro | Verifica que la cuenta contable y el centro de costo ingresados existan en el sistema y estén en estado activo antes de permitir el registro del detalle presupuestal. |
| P-03 | Consultar información histórica | Recupera datos presupuestales y de ejecución de años fiscales anteriores desde múltiples entidades del sistema. |
| P-04 | Filtrar por criterios | Aplica filtros especificados por el usuario (año, área, centro de costo, cuenta contable) sobre la información histórica consultada para presentar únicamente los datos relevantes. |
| P-05 | Crear solicitud de ampliación | Registra una nueva solicitud de ampliación presupuestal, validando la existencia del detalle a ampliar y capturando motivo, justificación y monto solicitado. |
| P-06 | Consultar solicitudes pendientes | Recupera del sistema todas las solicitudes de modificación presupuestal que se encuentran en estado "solicitado" y pendientes de aprobación. |
| P-07 | Aprobar/Rechazar solicitud | Registra la decisión del aprobador (jefe de área o subgerente de finanzas) sobre una solicitud de ampliación o traslado presupuestal. |
| P-08 | Actualizar estado | Modifica el estado de una solicitud de modificación presupuestal y registra el empleado aprobador, fecha y observaciones de la decisión. |
| P-09 | Registrar proyecto CAPEX | Captura todos los datos de un nuevo proyecto de inversión propuesto, incluyendo código, nombre, centro de costo, cuenta contable, montos, fechas y flujos de caja proyectados. |
| P-10 | Calcular indicadores | Calcula automáticamente los indicadores financieros ROI, TIR y VAN de un proyecto de inversión basándose en los flujos de caja ingresados. |
| P-11 | Consultar proyectos propuestos | Recupera del sistema todos los proyectos de inversión que se encuentran en estado "propuesto" y pendientes de evaluación por el Comité de Inversiones. |
| P-12 | Registrar aprobación del Comité | Documenta la decisión formal del Comité de Inversiones sobre un proyecto propuesto, actualizando su estado y registrando fecha de acta y observaciones. |
| P-13 | Crear solicitud ampliación CAPEX | Registra una solicitud de incremento presupuestal para un proyecto de inversión en ejecución que enfrenta sobrecostos o imprevistos. |
| P-14 | Recalcular indicadores | Recalcula los indicadores financieros (ROI, TIR, VAN) de un proyecto de inversión considerando el monto adicional solicitado, para evaluar el impacto en la rentabilidad. |
| P-15 | Consultar ampliaciones CAPEX pendientes | Recupera todas las solicitudes de ampliación de inversión CAPEX en estado "solicitado" con sus respectivos análisis de impacto en indicadores financieros. |
| P-16 | Registrar decisión del Comité | Documenta la decisión colegiada del Comité de Inversiones sobre una solicitud de ampliación CAPEX, registrando acta, observaciones y notificando a los involucrados. |
| P-17 | Registrar ejecución real | Captura los gastos realmente incurridos durante el periodo, registrados por el área de Contabilidad con cuenta contable, centro de costo, periodo y monto ejecutado. |
| P-18 | Validar combinación presupuestada | Verifica que la combinación cuenta-centro-periodo del gasto ejecutado corresponda a una partida previamente presupuestada, y que cuenta y centro estén activos. |
| P-19 | Generar reporte de variaciones | Consulta los montos presupuestados y ejecutados de un periodo específico para preparar el análisis comparativo de desviaciones. |
| P-20 | Calcular desviaciones | Calcula las diferencias absolutas y porcentuales entre montos ejecutados y presupuestados, agrupando por cuenta contable, centro de costo y área responsable. |
| P-21 | Generar estados financieros | Consulta información presupuestal y de ejecución de todas las fuentes (ventas, gastos, inversiones) para un año y mes específicos ingresados por el usuario. |
| P-22 | Consolidar información | Clasifica y estructura la información consultada para generar los tres estados financieros: Estado de Resultados, Flujo de Caja y Balance General. |
| P-23 | Registrar aprobación del Directorio | Documenta la aprobación formal del presupuesto anual por parte del Directorio, registrando fecha de sesión, número de acta y observaciones. |
| P-24 | Actualizar estado y notificar | Cambia el estado del presupuesto anual a "aprobado", habilita funcionalidades de carga al ERP y envía notificaciones automáticas a todas las áreas de la empresa. |
| P-25 | Iniciar carga masiva | Dispara el proceso de carga del presupuesto aprobado al módulo presupuestal del ERP, verificando que el presupuesto esté en estado "aprobado". |
| P-26 | Validar consistencia | Ejecuta validaciones exhaustivas sobre todos los detalles presupuestales: existencia y estado de centros de costo y cuentas contables, totalización correcta, clasificación OPEX/CAPEX. |
| P-27 | Cargar al ERP | Transfiere todos los datos del presupuesto aprobado al sistema ERP mediante interfaz directa, registrando el resultado de la transferencia y las incidencias de validación. |
| P-28 | Consultar dashboard | Recupera información presupuestal y de ejecución actualizada en tiempo real desde las entidades del sistema según los filtros aplicados por el usuario. |
| P-29 | Filtrar información | Aplica los criterios de filtrado especificados (área, centro de costo, cuenta contable, periodo) sobre los datos consultados del dashboard. |
| P-30 | Actualizar en tiempo real | Genera visualizaciones interactivas (gráficos, alertas, indicadores) con la información filtrada, actualizándose automáticamente conforme se registren nuevas ejecuciones. |

[Diagramas de flujo de datos](04-process-model.md) · [Matriz de trazabilidad](traceability.md) · [Inicio](../README.md)
