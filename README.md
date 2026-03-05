# Real-time Fraud/Risk Scoring Platform

## General objective
Design and implement an enterprise-oriented claims management platform for insurance, where requests are processed asynchronously and reliably using API Management + Service Bus + Functions, ensuring traceability, error handling (DLQ), secret security, and observability.

## Specific objectives
 * 3 microservices in AKS (e.g., ingestion, scoring, decision).
 * Data flow via Event Hubs: producer → consumer groups (scoring/decision).
 * Persistence in PostgreSQL for scoring results and minimal auditing.
 * Resilience: timeouts/retries + documented idempotence strategy.
 * Distributed observability: end-to-end traces (a visible transaction traversing services).
 * APIM exposes endpoints (e.g., querying score/decision) and adds basic policies.

## Arquitectura (alto nivel)
- **Entrada**: Azure API Management (APIM)
- **Compute**: AKS (microservicios .NET)
- **Eventos**: Event Hubs (hub + consumer groups)
- **Datos**: Azure Database for PostgreSQL (managed)
- **Seguridad**: Managed Identity / Key Vault (según implementación)
- **Observabilidad**: OpenTelemetry + Application Insights/Azure Monitor

Diagramas: ver `docs/c4/`.

## Requisitos no funcionales (NFR)
Ver `docs/nfr/`.

## ADRs (decisiones)
Ver `docs/adrs/`.

## Contratos
Esquemas de eventos: `docs/contracts/`

## Deploy (Terraform + AKS)
- Terraform: `infra/terraform/`
- Manifests/Helm: (definir estándar aquí) **Pendiente**

## Observabilidad y operación
- Runbooks: `docs/runbooks/`

## Demo para entrevistas
- `docs/interview/`

## Licencia / Uso
Copyright (c) 2026 Diego Quiñonez. Todos los derechos reservados.

Este repositorio es público únicamente para fines de revisión y evaluación.  
No se otorga permiso para usar, copiar, modificar o redistribuir este contenido sin autorización escrita del autor.
