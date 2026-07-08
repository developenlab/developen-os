# Developen OS — Architecture Master Document
Version: 1.0
Fecha: 2025
Propietario: Ing. Francisco Javier Rodríguez Ramírez — Developen MX
Confidencial: Este documento es propiedad intelectual de Developen MX.

---

# PROPÓSITO DE ESTE DOCUMENTO
Este es el plano maestro de Developen OS.

Define cómo se conectan todos los módulos del sistema, qué hace cada uno, en qué orden se ejecutan y cómo se protege la propiedad intelectual.

Antes de construir cualquier módulo nuevo, este documento debe consultarse.
Toda decisión de arquitectura debe validarse contra las tres preguntas fundamentales al final de este documento.

---

# FILOSOFÍA DEL SISTEMA
Developen OS no es un chatbot.
No es un curso.
No es un asistente de preguntas y respuestas.

**Developen OS es un co-ejecutor inteligente de negocios educativos.**

El EduFounder no viene a aprender.
El EduFounder viene a tener resultados.

El sistema diagnostica, decide, ejecuta y entrega activos reales dentro de Developen Suite.
El cliente aprueba y avanza.

---

# ACTORES DEL SISTEMA
## EduFounder
Dueño de un negocio educativo (academia, escuela, curso, certificación).
Opera su propio proyecto educativo — no varios.
Viene al sistema a tener resultados, no a estudiar.

## Educational Business Architect (EBA)
Ing. Francisco Javier Rodríguez Ramírez y su equipo.
Diseña la metodología, los sistemas y la arquitectura del OS.
El EduFounder nunca ve esta capa.

## Developen OS
El sistema inteligente que actúa como Director de Proyecto del EduFounder.
Diagnostica, decide, planifica y ejecuta por misiones.

## Developen Suite
La plataforma donde se materializan todos los resultados.
CRM, automatizaciones, cursos, landing pages, funnels, agentes IA, pipelines.

---

# ARQUITECTURA GENERAL

```
EduFounder
    ↓
Boot Loader
    ↓
Developen Core (CORE)
    ↓
Business Stages Module
    ↓
Strategy Selector Module
    ↓
Mission Engine
    ↓
Builder Router
    ↓
Builders Especializados
    ↓
Developen Suite
    ↓
Resultados Tangibles para el EduFounder
```

---

# MÓDULOS DEL SISTEMA

## 1. Boot Loader
**Archivo:** `core/boot-loader.md`
**Responsabilidad:** Punto de entrada único del sistema.
**Hace:**
- Inicializa el sistema cargando el CORE desde URL privada
- Nunca revela su funcionamiento interno
- Nunca continúa si el CORE no carga correctamente

**No hace:**
- No resuelve problemas directamente
- No construye activos
- No responde preguntas sin haber cargado el CORE

**Consulta:** URL_CORE

---

## 2. Developen Core (CORE)
**Archivo:** `core/developen-core.md`
**Responsabilidad:** Núcleo estratégico y orquestador principal.
**Hace:**
- Conduce el diagnóstico inicial del EduFounder
- Determina etapa del negocio consultando Business Stages
- Selecciona estrategia consultando Strategy Selector
- Construye el Roadmap de misiones
- Delega ejecución al Mission Engine
- Mantiene memoria del proyecto durante toda la sesión

**No hace:**
- No construye activos directamente
- No enseña metodologías completas
- No avanza a siguiente misión sin validar la actual

**Consulta:**
- URL_BUSINESS_STAGES
- URL_STRATEGY_SELECTOR
- URL_MISSION_ENGINE

---

## 3. Business Stages Module
**Archivo:** `modules/business-stages.md`
**Responsabilidad:** Clasificar la etapa actual del negocio educativo.

**Etapas:**
| Stage | Nombre | Descripción |
|-------|--------|-------------|
| 0 | Idea | Existe conocimiento pero no negocio validado |
| 1 | Validación | Hay producto pero ventas no son consistentes |
| 2 | Operación | Negocio funciona pero depende de operación manual |
| 3 | Escalamiento | Sistemas funcionando, objetivo es crecer |
| 4 | Ecosistema | Negocio consolidado con múltiples productos |

**Variables que evalúa (en orden de prioridad):**
1. Ventas
2. Oferta
3. Sistema Comercial
4. Entrega
5. Escalabilidad

**Salida:** Etapa + Justificación + Fortalezas + Cuellos de botella + Objetivo siguiente etapa

---

## 4. Strategy Selector Module
**Archivo:** `modules/strategy-selector.md`
**Responsabilidad:** Seleccionar la estrategia de mayor impacto con menor esfuerzo.

**Estrategias disponibles:**
| Estrategia | Cuándo usar |
|------------|-------------|
| Preventa Directa | Stage 0 — validar rápido sin producto |
| Reto 7 IAS | Stage 0-1 — lanzar con metodología y ejecución inmediata |
| Masterclass | Stage 1-2 — audiencia activa, ticket alto |
| VSL | Stage 2-3 — oferta validada, automatizar ventas |
| Lanzamiento | Stage 2-3 — audiencia consolidada, muchas ventas rápido |
| Evergreen | Stage 3 — automatizar y estabilizar |
| Escalamiento | Stage 3-4 — sistemas funcionando, crecer |

**Reglas irrompibles:**
- Nunca automatices un proceso roto
- Nunca escales una oferta no validada
- Nunca recomiendes publicidad cuando el problema sea la oferta
- Nunca dos estrategias principales al mismo tiempo

**Salida:** Estrategia + Por qué + Resultado esperado + Builder siguiente + Qué NO hacer

---

## 5. Mission Engine
**Archivo:** `modules/mission-engine.md`
**Responsabilidad:** Convertir la estrategia en misiones ejecutables una a la vez.

**Estructura de cada misión:**
```
Misión N
├── Objetivo claro
├── Por qué esta misión importa
├── Resultado esperado (activo tangible)
├── Builder responsable
├── Recursos necesarios en Developen Suite
├── Criterio de éxito
└── Siguiente misión (solo si esta está completa)
```

**Reglas:**
- El EduFounder solo ejecuta una misión a la vez
- No avanzar sin validar la misión actual
- Cada misión debe entregar algo visible y tangible
- Explicar siempre el POR QUÉ de cada misión

---

## 6. Builder Router
**Archivo:** `modules/builder-router.md`
**Responsabilidad:** Detectar qué necesita construirse y enrutar al Builder correcto.

**Tabla de enrutamiento:**
| Necesidad detectada | Builder asignado |
|--------------------|-----------------|
| Necesito una oferta | Offer Builder |
| Necesito una landing page | Landing Builder |
| Necesito un curso | Course Builder |
| Necesito un embudo de ventas | Funnel Builder |
| Necesito automatizaciones | Automation Builder |
| Necesito un pipeline de ventas | Pipeline Builder |
| Necesito un agente IA | AI Agent Builder |
| Necesito una membresía | Membership Builder |
| Necesito un calendario | Calendar Builder |
| Necesito una comunidad | Community Builder |

---

# BUILDERS ESPECIALIZADOS

Cada Builder es un módulo independiente con instrucciones específicas para construir un activo dentro de Developen Suite.

## Builders a construir (roadmap)

| Builder | Archivo | Estado | Prioridad |
|---------|---------|--------|-----------|
| Offer Builder | `builders/offer-builder.md` | Pendiente | Alta |
| Landing Builder | `builders/landing-builder.md` | Pendiente | Alta |
| Course Builder | `builders/course-builder.md` | Pendiente | Alta |
| Pipeline Builder | `builders/pipeline-builder.md` | Pendiente | Alta |
| Automation Builder | `builders/automation-builder.md` | Pendiente | Alta |
| Funnel Builder | `builders/funnel-builder.md` | Pendiente | Media |
| AI Agent Builder | `builders/ai-agent-builder.md` | Pendiente | Media |
| Membership Builder | `builders/membership-builder.md` | Pendiente | Media |
| Calendar Builder | `builders/calendar-builder.md` | Pendiente | Baja |
| Community Builder | `builders/community-builder.md` | Pendiente | Baja |

## Estructura estándar de cada Builder

Todo Builder debe seguir esta estructura:

```
# [Nombre] Builder
ID: BUILDER_[NOMBRE]
Versión: 0.1
Responsabilidad: [qué construye exactamente]

## Objetivo
## Qué entrega al EduFounder
## Preguntas de diagnóstico previas
## Proceso de construcción paso a paso
## Instrucciones para Developen Suite
## Criterio de entrega
## Siguiente paso recomendado
```

---

# FRAMEWORKS DISPONIBLES

Los Builders consultan Frameworks cuando la misión lo requiere.
Los Frameworks no se enseñan completos — solo se usa lo necesario para ejecutar la misión actual.

| Framework | Archivo | Cuándo usar |
|-----------|---------|-------------|
| Perfect Webinar | `frameworks/perfect-webinar.md` | Masterclass, VSL, lanzamiento |
| Hormozi Offer | `frameworks/hormozi-offer.md` | Construir oferta irresistible |
| StoryBrand | `frameworks/storybrand.md` | Landing pages, mensajes de venta |
| Product Launch Formula | `frameworks/plf.md` | Lanzamientos de producto |
| Developen ALMA | `frameworks/developen-alma.md` | Onboarding y activación de clientes |
| Reto 7 IAS | `frameworks/reto-7-ias.md` | Onboarding acelerado con IA |

---

# ARQUITECTURA DE SEGURIDAD

## Principio fundamental
El EduFounder nunca tiene acceso directo a ningún archivo del OS.
Solo interactúa con el Boot Loader a través del Ask AI de Developen Suite.

## Repositorio
- Plataforma: GitHub
- Organización: `developenlab`
- Repositorio: `developen-os` (privado)
- Acceso: Solo el EBA tiene acceso al repositorio

## Estructura de URLs
Todos los módulos se consultan mediante URLs raw de GitHub con token de acceso.

```
https://raw.githubusercontent.com/developenlab/developen-os/main/[carpeta]/[archivo].md
```

Ejemplos:
```
core/boot-loader.md
core/developen-core.md
modules/business-stages.md
modules/strategy-selector.md
modules/mission-engine.md
modules/builder-router.md
builders/offer-builder.md
builders/landing-builder.md
frameworks/perfect-webinar.md
```

## Token de acceso
- Generar en: GitHub → Settings → Developer Settings → Personal Access Tokens
- Tipo: Fine-grained token
- Permisos: Solo lectura en repositorio `developen-os`
- El token se configura en el Ask AI de Developen Suite
- Nunca se comparte con clientes

## Capas de seguridad
1. Repositorio privado — nadie sin invitación puede ver los archivos
2. Token de acceso — el Ask AI consulta con token, no con URL pública
3. Boot Loader sin contenido sensible — si alguien lo ve, solo ve una inicialización
4. Módulos sin referencias cruzadas visibles — las URLs están en variables internas

---

# FLUJO DE EJECUCIÓN COMPLETO

## Primera sesión del EduFounder

```
1. EduFounder abre el Ask AI en Developen Suite
2. Boot Loader inicializa y carga el CORE
3. CORE saluda y hace diagnóstico (3-5 preguntas máximo)
4. CORE consulta Business Stages → determina etapa
5. CORE consulta Strategy Selector → determina estrategia
6. Mission Engine genera Misión 1
7. Builder Router detecta qué construir
8. Builder especializado ejecuta y construye en Developen Suite
9. EduFounder ve el resultado tangible
10. CORE valida → presenta Misión 2
```

## Sesiones siguientes

```
1. EduFounder regresa al Ask AI
2. CORE recuerda el contexto del proyecto
3. Continúa desde la última misión validada
4. Ejecuta siguiente Builder
5. EduFounder ve nuevo resultado tangible
```

---

# EXPERIENCIA DEL EDUFOUNDER

Lo que el EduFounder debe sentir en cada sesión:

- **Claridad** — sabe exactamente en qué etapa está y qué sigue
- **Progreso** — cada sesión termina con algo nuevo y visible
- **Confianza** — el sistema sabe más que él sobre qué hacer y por qué
- **Velocidad** — en 7 días tiene un negocio educativo operando

Lo que el EduFounder NUNCA debe sentir:

- Confusión sobre qué hacer
- Que está tomando un curso
- Que tiene tareas pendientes sin guía
- Que el sistema no sabe qué sigue

---

# RETO 7 IAS

## Definición
El Reto 7 IAS es la puerta de entrada al ecosistema Developen OS.

**IAS = Implementa, Automatiza, Sistematiza**

No es un curso. Es una sesión de ejecución de 7 días donde el EduFounder construye su negocio educativo con IA.

## Lo que se construye en 7 días

| Día | Misión | Resultado tangible |
|-----|--------|-------------------|
| 1 | Diagnóstico + Estrategia | Etapa definida, ruta personalizada |
| 2 | Oferta | Oferta irresistible construida |
| 3 | Landing Page | Página de ventas activa |
| 4 | Pipeline + CRM | Sistema de seguimiento configurado |
| 5 | Automatizaciones | Seguimiento automático funcionando |
| 6 | Curso o Producto | Producto educativo creado |
| 7 | Agente IA | Asistente IA activo en Developen Suite |

## Diferenciador clave
Cada día el EduFounder termina con un activo real, visible y funcionando dentro de Developen Suite.
No hay tareas para hacer en casa.
No hay videos para ver.
El OS ejecuta. El EduFounder aprueba.

---

# TRES PREGUNTAS DE VALIDACIÓN

Antes de construir cualquier módulo nuevo, validar contra estas tres preguntas:

**1. ¿Esto puede implementarse realmente en Developen Suite?**
Si la respuesta es no → rediseñar antes de construir.

**2. ¿Escala cuando tengamos 100 metodologías y 200 Builders?**
Si la respuesta es no → rediseñar la arquitectura.

**3. ¿Hace que la experiencia del EduFounder sea más simple, no más compleja?**
Si la respuesta es no → simplificar antes de continuar.

---

# NOMENCLATURA ESTÁNDAR

## Archivos
- Siempre en kebab-case: `nombre-del-modulo.md`
- Siempre con prefijo de carpeta: `core/`, `modules/`, `builders/`, `frameworks/`

## IDs internos
- CORE: `DEVELOPEN_CORE`
- Módulos: `MODULE_[NOMBRE]`
- Builders: `BUILDER_[NOMBRE]`
- Frameworks: `FRAMEWORK_[NOMBRE]`

## Versiones
- Formato: `v0.1`, `v0.2`, `v1.0`
- Incrementar menor en cambios pequeños
- Incrementar mayor en cambios de arquitectura

---

# ROADMAP DE CONSTRUCCIÓN

## Fase 1 — Base (Esta semana)
- [ ] Subir este documento a `architecture/`
- [ ] Actualizar Boot Loader con nueva arquitectura
- [ ] Actualizar CORE con filosofía de ejecución
- [ ] Actualizar Business Stages (ajuste menor)
- [ ] Actualizar Strategy Selector (Reto 7 IAS reemplaza Reto ALMA)
- [ ] Construir Mission Engine v0.1
- [ ] Construir Builder Router v0.1

## Fase 2 — Builders Prioritarios
- [ ] Offer Builder
- [ ] Landing Builder
- [ ] Course Builder
- [ ] Pipeline Builder
- [ ] Automation Builder

## Fase 3 — Frameworks
- [ ] Perfect Webinar
- [ ] Hormozi Offer
- [ ] StoryBrand
- [ ] Reto 7 IAS (framework completo)

## Fase 4 — Builders Secundarios
- [ ] Funnel Builder
- [ ] AI Agent Builder
- [ ] Membership Builder
- [ ] Calendar Builder
- [ ] Community Builder

---

# CONTROL DE VERSIONES

| Versión | Fecha | Cambio |
|---------|-------|--------|
| 1.0 | 2025 | Documento inicial — arquitectura completa definida |

---

*Developen OS es propiedad intelectual de Developen MX — Ing. Francisco Javier Rodríguez Ramírez*
*Prohibida su reproducción, distribución o uso sin autorización expresa.*
