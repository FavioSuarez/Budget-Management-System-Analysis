# Análisis del negocio

## Contexto

La organización gestiona múltiples áreas funcionales y centros de costo, entre ellos tiendas, oficinas y almacenes. Su proceso presupuestal integra proyecciones de ventas, necesidades de compra, gastos operativos y proyectos de inversión.

**PROC01: Planeamiento presupuestal y control de gestión** comprende la planificación, consolidación, aprobación y seguimiento de los recursos financieros destinados a operaciones y proyectos.

El proceso combina dos actividades: planificar los siguientes ejercicios y controlar mensualmente la ejecución del ejercicio vigente. El plan de ventas orienta la estimación de compras, gastos y recursos necesarios.

## Objetivo

Diseñar un sistema de información que centralice el presupuesto, facilite la validación de registros y permita dar seguimiento a la ejecución y a las modificaciones autorizadas.

## Actores y responsabilidades

| Actor | Responsabilidad |
| --- | --- |
| Área Comercial | Preparar el plan de ventas que orienta la planificación. |
| Jefes y responsables de área | Elaborar propuestas de gasto, justificar ajustes y participar en su revisión. |
| Planeamiento Financiero / Finanzas | Coordinar, consolidar, analizar y presentar el presupuesto. |
| Subgerente de Finanzas | Revisar ampliaciones y variaciones, registrar aprobaciones y coordinar la carga. |
| Contabilidad | Registrar información real y revisar la imputación contable del cierre. |
| Responsable de Proyecto | Proponer proyectos CAPEX y sustentar ampliaciones. |
| Comité de Inversiones | Evaluar proyectos y cambios con impacto en rentabilidad. |
| Directorio y Gerencia General | Revisar y autorizar el presupuesto corporativo. |

## Proceso actual (AS-IS)

| Código | Subproceso | Descripción |
| --- | --- | --- |
| SUBPR01 | Planificación inicial y coordinación | Definir objetivos, roles, formatos y fechas en el kick-off. |
| SUBPR02 | Recolección de información base | Revisar información histórica y supuestos externos. |
| SUBPR03 | Elaboración del plan de ventas | Proyectar ingresos y establecer la base para compras y gastos. |
| SUBPR04 | Determinación de requerimientos de compras y gastos | Estimar recursos, servicios, gastos fijos y variables. |
| SUBPR05 | Consolidación de información presupuestal | Integrar las propuestas de las áreas y revisar su consistencia. |
| SUBPR06 | Aprobación del presupuesto | Presentar el presupuesto al Directorio y obtener autorización. |
| SUBPR07 | Carga del presupuesto en el ERP | Registrar y validar importes por cuenta, centro y periodo; liberar para ejecución. |
| SUBPR08 | Control y seguimiento presupuestal | Registrar ejecución, cerrar el mes y analizar variaciones. |
| SUBPR09 | Gestión de ampliaciones | Solicitar, evaluar y aplicar ampliaciones o traslados autorizados. |
| SUBPR10 | Gestión de inversiones CAPEX | Evaluar rentabilidad, aprobar proyectos y controlar cambios de inversión. |

Las áreas elaboran sus proyecciones en hojas de cálculo y comparten la información mediante Teams, OneDrive o SharePoint. Finanzas consolida los datos, revisa su clasificación y prepara el presupuesto para su aprobación y carga al ERP.

Durante el seguimiento mensual, Contabilidad registra la ejecución y Finanzas analiza las variaciones con apoyo de reportes y herramientas de BI. Las ampliaciones se comunican por correo y se aplican después de la evaluación de los responsables.

## Necesidades del negocio

| Necesidad | Impacto esperado | Requerimientos relacionados |
| --- | --- | --- |
| Estandarizar el registro presupuestal | Reducir el trabajo de consolidación y homogeneizar la información. | RF-01 |
| Consultar información histórica | Comparar ejercicios y apoyar nuevas proyecciones. | RF-02 |
| Formalizar las ampliaciones | Mantener seguimiento de solicitantes, decisiones y fechas. | RF-03 a RF-05 |
| Integrar la evaluación de inversiones | Relacionar montos, responsables y rentabilidad de los proyectos. | RF-06 a RF-10 |
| Validar la imputación contable | Mantener consistencia entre cuentas, centros y periodos. | RF-11 |
| Comparar presupuesto y ejecución | Detectar desviaciones y orientar decisiones de gestión. | RF-12 y RF-16 |
| Consolidar y cargar el presupuesto aprobado | Agilizar la preparación de información para el Directorio y el ERP. | RF-13 a RF-15 |

## Propuesta de proceso (TO-BE)

La propuesta organiza la información alrededor del presupuesto anual y sus detalles de gasto e inversión. Los registros se clasifican por cuenta contable y centro de costo, y se diferencian según correspondan a presupuesto o ejecución.

Las solicitudes de modificación reúnen monto, motivo, justificación y responsables. Las decisiones quedan asociadas a su estado y fecha. En inversiones CAPEX, la evaluación considera el impacto en los indicadores financieros.

Los reportes permiten consultar información consolidada y comparar importes por periodo, área y centro de costo. La aprobación anual habilita la carga del presupuesto al ERP.

[Requerimientos funcionales](02-requirements.md) · [Inicio](../README.md)
