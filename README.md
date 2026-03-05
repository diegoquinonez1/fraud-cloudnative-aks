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

## Licencia / Uso
Copyright (c) 2026 Diego Quiñonez. Todos los derechos reservados.

Este repositorio es público únicamente para fines de revisión y evaluación.  
No se otorga permiso para usar, copiar, modificar o redistribuir este contenido sin autorización escrita del autor.
