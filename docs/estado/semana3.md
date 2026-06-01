# 📊 Estado del Proyecto - Semana 3

## ✅ Logros de la semana
- [x] Endpoint GET /libros implementado y documentado (#3)
- [x] Validación de formato ISBN-13 añadida (#4)
- [x] Diagrama de secuencia "Flujo de préstamo" actualizado

## 🔄 En progreso
- [ ] Endpoint POST /prestamos (70% completo) - @maria
- [ ] Frontend: formulario de préstamo (50% completo) - @carlos
- [ ] Pruebas de integración para módulo Libros - @ana

## 🚨 Bloqueos / Riesgos
| Bloqueo | Impacto | Acción / Owner |
|---------|---------|---------------|
| API externa de ISBN responde lento | Validación puede fallar en producción | Implementar timeout + fallback a regex - @maria |
| QA con carga compartida en otro proyecto | Pruebas podrían retrasarse | Priorizar tests críticos; solicitar apoyo - @pm |

## 📅 Próximos hitos
| Hito | Fecha | Estado |
|------|-------|--------|
| H2: API base funcional | 22/06 | 🟡 En riesgo (ver bloqueos) |
| H3: MVP integrado | 13/07 | ⚪ En planificación |

## 🔗 Enlaces rápidos
- [GitHub Projects - Tablero Kanban](https://github.com/.../projects/1)
- [Swagger API - Vista interactiva](https://editor.swagger.io/?url=...)
- [Última demo grabada (Loom)](https://loom.com/...)

*Última actualización: 2026-06-10 | Próxima revisión: 2026-06-17* 
