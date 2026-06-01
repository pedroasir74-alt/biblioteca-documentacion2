# 📏 Declaración de Alcance - Biblioteca Digital v1.0

## ✅ INCLUYE (In-Scope)
### Módulo Libros
- [ ] CRUD completo de libros (ISBN, título, autor, categoría, disponibilidad)
- [ ] Búsqueda por título/autor con filtros básicos
- [ ] Validación de formato ISBN-13

### Módulo Usuarios
- [ ] Registro de bibliotecarios (rol interno)
- [ ] Alta/baja de usuarios finales (lectores)
- [ ] Historial de préstamos por usuario

### Módulo Préstamos
- [ ] Flujo completo: solicitar → validar disponibilidad → registrar → devolver
- [ ] Cálculo automático de fecha de devolución (14 días por defecto)
- [ ] Notificación email al vencer (integración con SendGrid free tier)

### Infraestructura y Documentación
- [ ] API REST documentada con Swagger/OpenAPI en `/docs/api/swagger.yaml`
- [ ] Diagramas UML en `/docs/diagramas/` (Draw.io)
- [ ] Guías de uso en `/docs/manual/` (Markdown)
- [ ] Despliegue en entorno de staging *(AWS Free Tier)
* Un entorno de staging es una réplica exacta del sitio web en producción donde se realizan pruebas de cambios, actualizaciones y nuevas funcionalidades antes de implementarlas en el sitio público.

## ❌ NO INCLUYE (Out-of-Scope)
- [ ] Aplicación móvil para usuarios finales
- [ ] Integración con sistemas de otras bibliotecas **(Z39.50, OAI-PMH)
- [ ] Módulo de multas y pagos online
- [ ] Migración histórica de registros en papel
- [ ] Soporte multi-idioma o accesibilidad WCAG AA *** (fase 2)
** Z39.50 es un protocolo de búsqueda y recuperación de información diseñado originalmente para sistemas bibliotecarios, que permite a los clientes consultar bases de datos remotas y transferir registros MARC mediante una estructura cliente-servidor compleja.  Fue adoptado internacionalmente como ISO 23950 y facilita la interoperabilidad entre diferentes sistemas de gestión bibliotecaria, aunque su implementación es más costosa y técnica. 
OAI-PMH (Open Archives Initiative Protocol for Metadata Harvesting) es un protocolo más sencillo basado en HTTP y XML, creado para facilitar la recolección (harvesting) de metadatos entre repositorios digitales y archivos electrónicos.  Su objetivo principal es permitir que los servicios agreguen información de múltiples fuentes de manera eficiente, ofreciendo una interoperabilidad de "barrera baja" ideal para el acceso abierto y la ciencia, pero con funcionalidades más limitadas que Z39.50. 
*** El Nivel AA de las Directrices de Accesibilidad para el Contenido Web (WCAG) es el estándar global recomendado y el requisito legal obligatorio para la mayoría de las administraciones públicas y empresas en España.  Representa el equilibrio óptimo entre la viabilidad técnica de implementación y la mejora significativa de la accesibilidad para personas con discapacidad.

## 🎯 Criterios de Aceptación Generales
| Entregable | Criterio de Aceptación | Método de Verificación |
|-----------|----------------------|----------------------|
| API Libros | Responde con código 200 y JSON válido según schema | Prueba automatizada + validación swagger.yaml |
| Frontend Préstamo | Flujo completo en <3 clics, sin errores en consola | Prueba de usabilidad con 3 usuarios |
| Documentación | Todos los endpoints documentados, diagramas actualizados | Revisión manual + enlace funcional en README |

## 🔄 Proceso de Gestión de Cambios
1. **Solicitud**: Cualquier stakeholder puede abrir un Issue con etiqueta `scope-change`
2. **Análisis**: PM + Tech Lead evalúan impacto en tiempo/costo/riesgo (máx. 48h)
3. **Decisión**: Sponsor aprueba/rechaza basándose en el análisis
4. **Ejecución**: Si se aprueba, se actualiza WBS, cronograma y línea base
5. **Comunicación**: Se notifica a todo el equipo y stakeholders afectados