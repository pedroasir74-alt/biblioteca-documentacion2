## ⚠️ Plan 3: Gestión de Riesgos (Risk Management Plan)

### 📌 Objetivo
Identificar, analizar y preparar respuestas para **eventos inciertos que podrían impactar el éxito del proyecto**.

### 🧱 Componentes esenciales para software

| Componente | Descripción | Ejemplo práctico |
|-----------|-------------|-----------------|
| **📋 Registro de Riesgos** | Lista viva de riesgos con probabilidad, impacto, mitigación y owner | "Riesgo: API externa de ISBN cambia → Mitigación: Adapter layer + mock" |
| **🎯 Matriz Probabilidad/Impacto** | Clasificación visual para priorizar acciones | Alto/Alto = actuar ya; Bajo/Bajo = monitorear |
| **🛡️ Planes de Respuesta** | Estrategias concretas: Evitar, Mitigar, Transferir, Aceptar | "Si el QA se enferma, activar cross-training con dev backend" |
| **🔄 Revisión periódica** | Frecuencia y formato para actualizar el registro | "15 min al inicio de cada sprint planning" |
| **📊 Indicadores de Alerta Temprana** | Señales que activan planes de contingencia | "Si una tarea crítica se retrasa >2 días, escalar a Sponsor" |

### 📄 Ejemplo: Registro de Riesgos (Markdown para GitHub)
```markdown
# ⚠️ Registro de Riesgos - Biblioteca Digital v1.0

## 🎯 Matriz de Priorización
| Probabilidad \ Impacto | Bajo (1) | Medio (2) | Alto (3) |
|----------------------|----------|-----------|----------|
| **Alta (3)** | 🟡 Monitorear | 🔴 Actuar ya | 🔴 Actuar ya |
| **Media (2)** | 🟢 Aceptar | 🟡 Monitorear | 🔴 Actuar ya |
| **Baja (1)** | 🟢 Aceptar | 🟢 Aceptar | 🟡 Monitorear |

## 📋 Riesgos Identificados

### 🔴 Riesgo Crítico #1: Cambio en normativa de protección de datos
| Campo | Valor |
|-------|-------|
| **Descripción** | Nueva regulación GDPR local podría requerir cambios en almacenamiento de datos de usuarios |
| **Probabilidad** | Media (2) |
| **Impacto** | Alto (3) → Retraso 2-3 semanas + coste adicional |
| **Señal de Alerta** | Publicación de borrador de ley en BOE |
| **Mitigación** | 1. Revisión legal en Sprint 1<br>2. Diseñar privacy-by-default (datos mínimos, encriptación)<br>3. ADR-002: Estrategia de cumplimiento |
| **Owner** | María López (Sponsor) |
| **Estado** | 🟡 En mitigación |

### 🔴 Riesgo Crítico #2: API externa de validación ISBN no disponible
| Campo | Valor |
|-------|-------|
| **Descripción** | Servicio gratuito de validación ISBN podría cambiar formato o dejar de funcionar |
| **Probabilidad** | Alta (3) |
| **Impacto** | Medio (2) → Funcionalidad degradada, no bloqueo total |
| **Señal de Alerta** | Error 5xx en logs de validación >5% de peticiones |
| **Mitigación** | 1. Crear adapter layer para aislar dependencia<br>2. Implementar mock para desarrollo/testing<br>3. Fallback: validación básica por regex si API falla |
| **Owner** | Carlos Ruiz (PM) |
| **Estado** | ✅ Mitigado (adapter implementado en Sprint 1) |

### 🟡 Riesgo Medio #3: Rotación de desarrollador clave
| Campo | Valor |
|-------|-------|
| **Descripción** | Uno de los 3 devs asignados podría dejar el proyecto antes de finalizar |
| **Probabilidad** | Baja (1) |
| **Impacto** | Alto (3) → Retraso significativo en entrega |
| **Señal de Alerta** | Ausencias frecuentes, disminución de commits, comentarios en 1:1 |
| **Mitigación** | 1. Documentación continua en /docs/tech/<br>2. Pair programming en tareas críticas<br>3. Cross-training: cada módulo tiene 2 personas con conocimiento |
| **Owner** | Carlos Ruiz (PM) |
| **Estado** | 🟢 Monitoreado |

## 🔄 Proceso de Revisión
- **Frecuencia**: 15 minutos al inicio de cada Sprint Planning
- **Participantes**: PM, Tech Lead, Representante de Usuarios
- **Salida**: Actualización de estado, nuevos riesgos, cierre de riesgos mitigados
- **Registro**: Issues con etiqueta `risk` en GitHub + actualización de este documento

## 🚨 Plan de Contingencia General
Si un riesgo 🔴 se materializa:
1. Activar owner del riesgo en <2 horas
2. Ejecutar mitigación predefinida o improvisar solución temporal
3. Comunicar impacto a stakeholders en <24 horas
4. Actualizar cronograma y presupuesto si es necesario
5. Documentar lección aprendida en /docs/retro/