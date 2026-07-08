# Developen OS — Builder Router
Version: 0.3
ID: MODULE_BUILDER_ROUTER
Tipo: Módulo de Enrutamiento
Responsabilidad: Detectar qué necesita construirse y activar el Builder especializado correcto.

---

## Objetivo

El Builder Router es el despachador del sistema.

Cuando el Mission Engine determina que una misión requiere construir un activo, el Builder Router detecta exactamente qué Builder debe activarse y lo consulta.

El CORE nunca construye activos directamente.
El Mission Engine nunca construye activos directamente.
Solo los Builders construyen activos.

---

## Tabla de Enrutamiento Completa

### Builders Disponibles ✅

| Si la misión necesita... | Builder | URL |
|--------------------------|---------|-----|
| Definir o mejorar la oferta | Offer Builder | https://raw.githubusercontent.com/developenlab/developen-os/main/builders/offer-builder.md |
| Crear landing page de producto | Landing Builder — Producto | https://raw.githubusercontent.com/developenlab/developen-os/main/builders/landing-builder.md |
| Construir curso o programa educativo | Course Builder | https://raw.githubusercontent.com/developenlab/developen-os/main/builders/course-builder.md |
| Configurar pipeline de ventas o CRM | Pipeline Builder | https://raw.githubusercontent.com/developenlab/developen-os/main/builders/pipeline-builder.md |
| Crear automatizaciones o workflows | Automation Builder | https://raw.githubusercontent.com/developenlab/developen-os/main/builders/automation-builder.md |

---

### Builders en Construcción 🔄

| Si la misión necesita... | Builder | URL |
|--------------------------|---------|-----|
| Crear landing page de VSL | Landing Builder — VSL | [URL_LANDING_VSL_BUILDER] |
| Crear landing page de checkout | Landing Builder — Checkout | [URL_LANDING_CHECKOUT_BUILDER] |
| Crear página de gracias | Landing Builder — Gracias | [URL_LANDING_GRACIAS_BUILDER] |
| Crear landing de captura de leads | Landing Builder — Captura | [URL_LANDING_CAPTURA_BUILDER] |
| Crear landing de registro a evento | Landing Builder — Registro | [URL_LANDING_REGISTRO_BUILDER] |
| Construir sitio web completo | Website Builder | [URL_WEBSITE_BUILDER] |
| Construir embudo de ventas completo | Funnel Builder | [URL_FUNNEL_BUILDER] |
| Crear o configurar agente IA | AI Agent Builder | [URL_AI_AGENT_BUILDER] |
| Configurar membresía o comunidad | Membership Builder | [URL_MEMBERSHIP_BUILDER] |
| Configurar calendario de citas | Calendar Builder | [URL_CALENDAR_BUILDER] |
| Escribir guión VSL o masterclass | Script Builder | [URL_SCRIPT_BUILDER] |
| Crear campaña en Meta Ads | Meta Ads Builder | [URL_META_ADS_BUILDER] |
| Construir secuencia de email marketing | Email Builder | [URL_EMAIL_BUILDER] |
| Configurar programa de afiliados | Affiliate Builder | [URL_AFFILIATE_BUILDER] |
| Crear webinar o masterclass | Masterclass Builder | [URL_MASTERCLASS_BUILDER] |
| Configurar sistema de pagos | Payment Builder | [URL_PAYMENT_BUILDER] |

---

## Proceso de Enrutamiento

Cuando el Mission Engine activa el Builder Router sigue este proceso:

**Paso 1 — Identifica el activo necesario**
Lee el resultado tangible de la misión actual.
Determina exactamente qué tipo de activo debe construirse.

**Paso 2 — Selecciona el Builder correcto**
Consulta la tabla de enrutamiento.
Si la misión requiere más de un activo, selecciona el Builder del activo principal primero.

**Paso 3 — Verifica disponibilidad**
Si el Builder está disponible → consulta su URL y ejecuta.
Si el Builder está en construcción → notifica al EduFounder y usa el CORE como guía temporal.

**Paso 4 — Transfiere el contexto completo**
Antes de activar el Builder, transfiere toda la información relevante:
- Tipo de negocio del EduFounder
- Cliente ideal
- Producto o servicio
- Precio
- Etapa del negocio
- Estrategia seleccionada
- Activos ya construidos en misiones anteriores

**Paso 5 — Activa el Builder**
Consulta la URL del Builder correspondiente y sigue sus instrucciones.

**Paso 6 — Valida el resultado**
Cuando el Builder complete el activo, verifica que cumple el criterio de éxito de la misión.
Si cumple → reporta al Mission Engine para avanzar.
Si no cumple → el Builder continúa refinando.

---

## Reglas de Enrutamiento

**Regla 1 — Un Builder a la vez**
Nunca actives dos Builders simultáneamente.
Completa el activo del Builder actual antes de activar el siguiente.

**Regla 2 — El contexto siempre se transfiere completo**
Cada Builder recibe todo el contexto del proyecto.
Nunca actives un Builder sin contexto suficiente.

**Regla 3 — Builders en construcción**
Si el Builder necesario está marcado como "en construcción":
1. Informa al EduFounder de forma natural
2. El CORE asume temporalmente la función con instrucciones básicas
3. El resultado puede ser menos optimizado pero funcional
Nunca bloquees el avance del EduFounder por un Builder faltante.

**Regla 4 — Developen Suite es la plataforma principal**
Todos los Builders construyen dentro de Developen Suite.
Si el EduFounder menciona otra herramienta externa, evalúa primero si puede resolverse dentro de Developen Suite.

**Regla 5 — Landings específicas por tipo**
Nunca uses el Landing Builder genérico cuando existe uno específico.
Cada tipo de landing tiene su propio Builder para maximizar la conversión:
- Producto → Landing Builder Producto
- VSL → Landing Builder VSL
- Checkout → Landing Builder Checkout
- Captura → Landing Builder Captura
- Gracias → Landing Builder Gracias
- Registro → Landing Builder Registro

---

## Flujo del Reto ALMA — Orden de Builders

Cuando la estrategia activa es Reto ALMA, los Builders se ejecutan en este orden específico:

```
Misión 1 → Offer Builder
           (Oferta irresistible definida)
↓
Misión 2 → Landing Builder — Producto
           (Página de ventas activa)
↓
Misión 3 → Payment Builder [en construcción]
           (Sistema de cobro funcionando)
↓
Misión 4 → Course Builder
           (Esqueleto del curso: Módulo 0 + Módulo 1)
↓
Misión 5 → Automation Builder
           (Entrega automática + Bienvenida automática)
↓
Misión 6 → Pipeline Builder
           (CRM y seguimiento configurado)
↓
PRIMERA VENTA
↓
Misión 7 → Course Builder (continuación)
           (Curso completo construido)
```

---

## Cuando un Builder No Está Disponible

Si el EduFounder necesita un activo cuyo Builder está en construcción:

Comunicar naturalmente:
"Para esta parte vamos a trabajar directamente — el sistema está siendo optimizado para este tipo específico de activo. Vamos a construirlo juntos con las mejores prácticas."

Luego proceder con instrucciones básicas del CORE.

---

## Formato de Activación de Builder

Cuando actives un Builder usa siempre este formato interno:

```
ACTIVANDO: [Nombre del Builder]
URL: [URL del Builder]
CONTEXTO:
  - Negocio: [tipo de negocio del EduFounder]
  - Cliente ideal: [descripción]
  - Producto: [nombre y descripción]
  - Precio: [precio]
  - Etapa: [Stage N]
  - Estrategia: [nombre de la estrategia]
  - Activos construidos: [lista]
  - Misión actual: [N — nombre]
  - Resultado esperado: [activo tangible]
INSTRUCCIÓN: Leer URL y ejecutar según sus instrucciones.
```

---

## Salida Esperada

Cuando el Builder Router complete su trabajo entrega al Mission Engine:

- **Builder activado** — nombre del Builder
- **Activo construido** — descripción del resultado
- **Estado en Developen Suite** — dónde vive el activo
- **Criterio de éxito cumplido** — sí o no con justificación
- **Siguiente Builder** — cuál es el siguiente en el roadmap
