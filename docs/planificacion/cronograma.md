# 📅 Cronograma - Biblioteca Digital v1.0

## 🎯 Hitos Principales
| Hito | Fecha Objetivo | Entregable Clave | Estado |
|------|---------------|-----------------|--------|
| H1: Alcance y arquitectura aprobados | 2026-06-01 | WBS + Diagrama C4 + ADR-001 | ✅ |
| H2: API base funcional y documentada | 2026-06-22 | swagger.yaml válido + endpoints CRUD | 🟡 |
| H3: MVP integrado en staging | 2026-07-13 | Frontend + Backend + DB conectados | ⚪ |
| H4: Lanzamiento piloto | 2026-07-27 | 3 usuarios externos activos + NPS ≥ 7 | ⚪ |

## 🗓️ Detalle por Sprint (Sprint 1: 03-14 jun)
| Tarea | Asignado | Estimación (días) | Dependencia | Estado | Issue |
|-------|----------|------------------|-------------|--------|-------|
| Configurar repo + CI/CD básico | @carlos | 1 | - | ✅ | #1 |
| Diseñar modelo de datos (ERD) | @maria | 2 | - | ✅ | #2 |
| Implementar GET /libros | @maria | 3 | #2 | 🔄 | #3 |
| Implementar POST /libros con validación | @maria | 4 | #3 | ⚪ | #4 |
| Documentar endpoints en swagger.yaml | @ana | 2 | #3, #4 | ⚪ | #5 |
| Revisión técnica + aprobación H2 | @carlos | 1 | #5 | ⚪ | #6 |

## 🔗 Dependencias Críticas
```mermaid
graph LR
    A[#2: Modelo de datos] --> B[#3: GET /libros]
    A --> C[#4: POST /libros]
    B --> D[#5: Documentar]
    C --> D
    D --> E[#6: Revisión H2] 