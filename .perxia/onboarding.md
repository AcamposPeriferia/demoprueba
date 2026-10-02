# Onboarding

## Insumos revisados
- `LevantamientoRequerimiento/` contiene cuatro diagramas Draw.io; la versión más completa es `dg_core_banking_arch_v4_R1-R4_2 (2).drawio`.
- El repositorio no contiene código ni documentos en formatos soportados por Graphify; los `.drawio` se revisaron directamente como XML.

## Línea base de producto
Programa de Core Banking para Vanti, con Mambu como maestro del crédito y Vanti Listo como canal/orquestador. El alcance está organizado en cuatro releases:
- R1, Q4-2026: originación para clientes Gas, con impacto mínimo en SAP.
- R2, Q1-2027: migración del producto RPO desde SAP al Core.
- R3, Q2-2027: migración del stock de créditos activos.
- R4, Q3-2027: financiación No Gas, nueva metodología de riesgo y antifraude.

## Capacidades y componentes principales
- Identidad, elegibilidad, oferta, calificación y decisión de crédito; originación y ciclo de vida del préstamo.
- Vanti Listo, Mi Vanti en Línea, API Management público/privado, orquestación de integración, identidad/biometría, OTP/firma electrónica, notificaciones y motor de riesgo/decisión parametrizable.
- Integraciones: Core ↔ SAP para cargos, recaudos, compensaciones y estados; eventos a Data Lake; contrato de marca de origen y conciliación con Cerebro de Cartera.

## Riesgos y decisiones abiertas
- Definir FICA vs. SD, responsables Ayesa/NTT y uso de BPA con SAP: bloquea las interfaces Core-SAP en las cuatro releases.
- Formalizar cobertura contractual del módulo de liquidaciones de aliados antes de construirlo.
- Cerrar el contrato de datos de marca de origen en Cerebro de Cartera desde R1; es prerrequisito para R3 y R4.
- Precisar criterios de aceptación para la ETL y conciliación de migración en R3.
- Validar la arquitectura con Sofka, Mambu y consultoría SAP antes de convertirla en especificación técnica.
