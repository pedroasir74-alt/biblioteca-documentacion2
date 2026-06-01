# 📜 ACTA DE CONSTITUCIÓN DEL PROYECTO
## Proyecto: Biblioteca Digital - MVP v1.0

### 1. Información Básica
| Campo | Valor |
|-------|-------|
| **Nombre del Proyecto** | Sistema de Gestión Bibliotecaria Digital |
| **ID del Proyecto** | BIB-DIG-2026-001 |
| **Fecha de Emisión** | 15 de mayo de 2026 |
| **Sponsor / Patrocinador** | María López, Directora de Tecnologías |
| **Project Manager** | Carlos Ruiz |
| **Duración Estimada** | 3 meses (12 semanas) |

---

### 2. Justificación de Negocio
**Problema actual:**
- La biblioteca gestiona préstamos en papel, generando errores, retrasos y pérdida de historial.
- Los usuarios no pueden consultar disponibilidad en tiempo real.

**Oportunidad:**
- Digitalizar el flujo básico permitirá atender un 30% más de usuarios con los mismos recursos.
- Sentará las bases para futuras integraciones (e-book, reservas online).

**ROI Esperado:**
- Ahorro operativo: ~€18K/año en reducción de errores y tiempo administrativo.
- Mejora en satisfacción de usuarios: objetivo NPS > 7.

---

### 3. Objetivos SMART
🎯 **Objetivo Principal:**
"Lanzar un MVP funcional que permita registrar libros, consultar disponibilidad y gestionar préstamos básicos, con una tasa de éxito del 95% en transacciones, antes del 15 de septiembre de 2026."

📊 **Objetivos Secundarios:**
| Objetivo | Métrica | Target | Fecha |
|----------|---------|--------|-------|
| Reducir tiempo de préstamo | Tiempo medio por operación | < 2 minutos | 15/09/2026 |
| Eliminar errores de registro | % de préstamos con datos inconsistentes | < 1% | 15/09/2026 |
| Validar con usuarios reales | NPS de usuarios piloto | ≥ 7 | 30/09/2026 |

---

### 4. Alcance del Proyecto

#### ✅ INCLUYE (In-Scope):
- Registro y búsqueda de libros (ISBN, título, autor, disponibilidad)
- Gestión de usuarios básicos (alta, baja, consulta)
- Flujo de préstamo/devolución con validación de disponibilidad
- API REST documentada con Swagger/OpenAPI
- Frontend web responsive para bibliotecarios
- Documentación técnica en repositorio GitHub

#### ❌ NO INCLUYE (Out-of-Scope):
- Aplicación móvil para usuarios finales
- Integración con sistemas de otras bibliotecas
- Módulo de multas y pagos online
- Migración histórica de datos en papel (se hará en fase 2)
- Soporte para múltiples sedes o sucursales

---

### 5. Stakeholders Clave

| Rol | Nombre / Área | Nivel de Influencia | Expectativa Principal |
|-----|--------------|-------------------|---------------------|
| Sponsor | María López (Dir. TI) | 🔴 Alta | ROI claro y entrega en plazo |
| Usuario Final | Ana Gómez (Bibliotecaria Jefe) | 🟡 Media | Interfaz simple y estable |
| Equipo Técnico | Carlos Ruiz (PM) + 3 devs | 🟡 Media | Alcance estable y herramientas adecuadas |
| Legal / Compliance | Departamento Jurídico | 🔴 Alta | Cumplimiento GDPR en datos de usuarios |
| Soporte IT | Miguel Sánchez (Infraestructura) | 🟢 Baja | Documentación para mantenimiento |

---

### 6. Riesgos Iniciales y Mitigación

| Riesgo | Probabilidad | Impacto | Mitigación Propuesta | Owner |
|--------|-------------|---------|---------------------|-------|
| Cambio en normativa de protección de datos | Media | Alto | Revisión legal en Sprint 1; diseño privacy-by-default | María López |
| Dependencia de API externa para validación ISBN | Alta | Medio | Crear capa de adaptación + mock para desarrollo | Carlos Ruiz |
| Rotación de desarrollador clave | Baja | Alto | Documentación continua + pair programming | Carlos Ruiz |
| Requisitos cambiantes tras ver prototipo | Alta | Medio | Proceso formal de cambios + buffer de alcance 15% | María López |








### 7. Recursos y Presupuesto

#### 👥 Equipo Asignado:
| Rol | Dedicación | Responsabilidades Clave |
|-----|-----------|------------------------|
| Project Manager | 50% | Planificación, comunicación, gestión de riesgos |
| Backend Developer | 100% | API, base de datos, lógica de negocio |
| Frontend Developer | 100% | Interfaz web, integración con API |
| QA / Tester | 30% | Pruebas manuales, automatización básica |

#### 💰 Presupuesto Aprobado:
| Concepto | Importe | Notas |
|----------|---------|-------|
| Desarrollo (equipo interno) | €35.000 | Basado en coste horario interno |
| Herramientas (GitHub Pro, hosting) | €2.500 | Plan anual, escalable |
| Formación / Certificaciones | €1.500 | Swagger, accesibilidad web |
| Contingencia (15%) | €6.000 | Para imprevistos gestionados |
| **TOTAL** | **€45.000** | |

#### 🛠️ Stack Tecnológico Aprobado:
- Backend: Node.js + Express
- Frontend: React + TypeScript
- Base de datos: PostgreSQL (AWS RDS Free Tier)
- Documentación: GitHub + Markdown + Swagger
- CI/CD (integración y distribución): GitHub Actions







### 8. Criterios de Éxito del Proyecto
El proyecto se considerará **exitoso** si, al finalizar:

✅ **Funcionalidad:**
- Los 3 flujos críticos (registro libro, consulta disponibilidad, préstamo) funcionan sin errores críticos
- API documentada y probada con Postman/Swagger

✅ **Calidad:**
- Cobertura de tests unitarios > 80% en lógica de negocio
- Tiempo de respuesta p95 < 2s para operaciones críticas

✅ **Adopción:**
- 3 bibliotecarios piloto completan 10 préstamos reales sin asistencia
- NPS ≥ 7 en encuesta post-uso

✅ **Entregables:**
- Código en repositorio GitHub con README, documentación y ADRs
- Acta de cierre firmada por Sponsor y Usuario Final

---

### 9. Autorizaciones

Al firmar este documento, los abajo firmantes:
- ✅ Autorizan formalmente el inicio del proyecto
- ✅ Confirman la disponibilidad de recursos descritos
- ✅ Aceptan los límites de alcance y criterios de éxito
- ✅ Otorgan autoridad al Project Manager para ejecutar el plan

| Rol | Nombre | Firma | Fecha |
|-----|--------|-------|-------|
| **Sponsor / Patrocinador** | María López | __________________ | ___/___/2026 |
| **Project Manager** | Carlos Ruiz | __________________ | ___/___/2026 |
| **Representante Usuarios** | Ana Gómez | __________________ | ___/___/2026 |
| **Legal / Compliance** | Departamento Jurídico | __________________ | ___/___/2026 |

---

📎 **Anexos:**
- [ ] Anexo A: Mapa completo de stakeholders
- [ ] Anexo B: Estimación detallada de esfuerzo (PERT)
- [ ] Anexo C: Prototipo de baja fidelidad (Draw.io)