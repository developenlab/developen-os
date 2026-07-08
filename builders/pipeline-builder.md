# Developen OS — Pipeline Builder
Version: 0.2
ID: BUILDER_PIPELINE
Tipo: Builder Especializado
Responsabilidad: Configurar el CRM y pipeline de ventas del EduFounder dentro de Developen Suite.

---

## Objetivo

El Pipeline Builder configura el sistema de gestión de prospectos y alumnos del EduFounder dentro de Developen Suite.

Sin un pipeline el EduFounder pierde prospectos, no sabe en qué etapa están y depende de su memoria para dar seguimiento.

Con el pipeline correcto el EduFounder tiene visibilidad total de su proceso comercial y nunca más pierde una venta por falta de seguimiento.

Al terminar esta misión el EduFounder tiene su CRM configurado, su pipeline activo y sus prospectos organizados dentro de Developen Suite.

---

## Qué Entrega al EduFounder

Al completar esta misión el EduFounder tiene:

- Pipeline de ventas configurado en Developen Suite
- Etapas del proceso comercial definidas
- Campos personalizados para su negocio
- Primer prospecto de prueba cargado
- Vista clara de todos sus prospectos y su estado

---

## Proceso de Construcción

### Fase 1 — Definir el Proceso Comercial

Antes de configurar el pipeline en la plataforma, define las etapas del proceso de ventas del EduFounder.

**Preguntas clave:**
- ¿Cómo llegan los prospectos actualmente? (WhatsApp, redes, referidos, página web)
- ¿Cuántos pasos hay desde que llega un prospecto hasta que compra?
- ¿Hay una llamada o demo de por medio?
- ¿Cuánto tarda normalmente en decidir un prospecto?

**Pipeline estándar para negocio educativo:**

```
ETAPA 1 — Nuevo Prospecto
El prospecto llegó pero aún no ha sido contactado.
Acción: Contactar en menos de 5 minutos.

ETAPA 2 — Contactado
Se estableció primer contacto. Está respondiendo.
Acción: Calificar — entender su situación y necesidad.

ETAPA 3 — Calificado
El prospecto tiene el perfil correcto y tiene interés.
Acción: Presentar la oferta o agendar llamada/demo.

ETAPA 4 — Oferta Presentada
Se presentó el producto y el precio.
Acción: Seguimiento hasta decisión.

ETAPA 5 — Negociación / Objeciones
El prospecto tiene dudas o pidió tiempo para decidir.
Acción: Resolver objeciones y crear urgencia.

ETAPA 6 — Ganado
El prospecto compró.
Acción: Dar acceso al producto y activar onboarding.

ETAPA 7 — Perdido
El prospecto no compró.
Acción: Registrar motivo y activar seguimiento a futuro.
```

---

### Fase 2 — Configurar en Developen Suite

**Paso 1 — Crear el Pipeline**
```
En Developen Suite ve a:
CRM → Pipelines → Agregar pipeline

Nombre: [Nombre del negocio] — Ventas
Tipo: Personalizado
```

**Paso 2 — Crear las etapas**
```
Agrega cada etapa en orden:

Etapa 1: Nuevo Prospecto
  Color: Gris
  
Etapa 2: Contactado
  Color: Azul
  
Etapa 3: Calificado
  Color: Amarillo
  
Etapa 4: Oferta Presentada
  Color: Naranja
  
Etapa 5: Negociación
  Color: Morado
  
Etapa 6: Ganado ✓
  Color: Verde
  
Etapa 7: Perdido ✗
  Color: Rojo
```

**Paso 3 — Configurar campos personalizados del contacto**
```
Ve a:
Configuración → Campos Personalizados → Contactos

Agrega estos campos según el negocio:
- Tipo de negocio educativo
- Número de alumnos actuales
- Producto de interés
- Presupuesto aproximado
- Fuente de origen (¿cómo llegó?)
- Fecha de seguimiento
- Notas de la conversación
```

**Paso 4 — Configurar la vista del pipeline**
```
En el pipeline ve a:
Configuración de vista

Activa que se muestre en cada tarjeta:
- Nombre del contacto
- Producto de interés
- Fecha del último contacto
- Próxima acción
- Valor de la oportunidad
```

**Paso 5 — Crear oportunidad de prueba**
```
Click en "Agregar oportunidad"
Nombre: [Tu nombre] — Prueba
Etapa: Nuevo Prospecto
Valor: $[precio del producto]
Contacto: Crear contacto de prueba

Mueve la tarjeta manualmente por cada etapa para verificar que funciona.
```

---

### Fase 3 — Conectar Fuentes de Entrada

Configura de dónde llegan los prospectos al pipeline automáticamente:

**Desde la Landing Page:**
```
En el formulario de la landing page:
Configuración → Al enviar el formulario
→ Crear contacto en CRM
→ Agregar al pipeline: [nombre del pipeline]
→ Etapa inicial: Nuevo Prospecto
→ Asignar a: [nombre del usuario]
```

**Desde WhatsApp:**
```
En Developen Suite:
Conversaciones → Configuración
→ Cuando llegue mensaje nuevo de número desconocido
→ Crear contacto en CRM
→ Agregar al pipeline
→ Etapa: Nuevo Prospecto
```

**Carga manual inicial:**
```
Si el EduFounder ya tiene prospectos en WhatsApp o en su lista de contactos:
CRM → Contactos → Importar
→ Subir archivo CSV con: Nombre, WhatsApp, Email
→ Asignar a pipeline: Nuevo Prospecto
```

---

### Fase 4 — Definir las Acciones por Etapa

Para cada etapa del pipeline define qué debe hacer el EduFounder:

```
ETAPA 1 — Nuevo Prospecto
⏱ Tiempo máximo: 5 minutos
📱 Acción: Enviar mensaje de bienvenida
💬 Mensaje:
"Hola [nombre], vi que te interesó [producto]. 
¿Tienes 5 minutos para contarme un poco de tu situación y ver si puedo ayudarte?"

ETAPA 2 — Contactado
⏱ Tiempo máximo: 24 horas
📱 Acción: Calificar con preguntas
💬 Preguntas de calificación:
1. ¿Qué tipo de negocio educativo tienes o quieres tener?
2. ¿Cuál es tu mayor reto ahorita?
3. ¿Has intentado resolverlo antes? ¿Cómo?

ETAPA 3 — Calificado
⏱ Tiempo máximo: 48 horas
📱 Acción: Presentar oferta o agendar llamada
💬 Mensaje:
"Con base en lo que me cuentas, creo que [producto] es exactamente lo que necesitas. 
¿Te cuento cómo funciona?"

ETAPA 4 — Oferta Presentada
⏱ Tiempo máximo: 72 horas
📱 Acción: Seguimiento si no ha respondido
💬 Mensaje de seguimiento:
"[Nombre], ¿tuviste oportunidad de revisar la información que te compartí? 
Cualquier duda que tengas, aquí estoy."

ETAPA 5 — Negociación
⏱ Tiempo máximo: 5 días
📱 Acción: Resolver objeción específica
💬 Estrategia: Alex Dey — doble alternativa
"¿Prefieres empezar esta semana o la próxima?"

ETAPA 6 — Ganado
⏱ Inmediato
📱 Acción: Enviar acceso y mensaje de bienvenida
💬 Mensaje:
"¡Felicidades [nombre]! Bienvenido a [producto]. 
Aquí está tu acceso: [link]. 
¿Tienes alguna duda para empezar?"

ETAPA 7 — Perdido
📝 Acción: Registrar motivo y programar seguimiento a 30 días
```

---

## Pipeline Configurado — Formato de Entrega

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
TU PIPELINE DE VENTAS
[NOMBRE DEL NEGOCIO]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PIPELINE: [Nombre]
PRODUCTO: [Nombre del producto]
PRECIO: $[precio]

ETAPAS CONFIGURADAS:
1. Nuevo Prospecto (gris)
2. Contactado (azul)
3. Calificado (amarillo)
4. Oferta Presentada (naranja)
5. Negociación (morado)
6. Ganado (verde)
7. Perdido (rojo)

FUENTES DE ENTRADA CONECTADAS:
✓ Landing Page → Pipeline automático
✓ WhatsApp → Pipeline automático
✓ Carga manual → Lista importada

PRÓXIMA MISIÓN:
Configurar automatizaciones para que el seguimiento 
ocurra automáticamente sin depender del EduFounder.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Criterio de Éxito

Esta misión está completa cuando:

- ✅ El pipeline está creado en Developen Suite con todas las etapas
- ✅ Los campos personalizados están configurados
- ✅ Al menos una fuente de entrada está conectada al pipeline
- ✅ El EduFounder puede mover prospectos entre etapas manualmente
- ✅ El EduFounder tiene al menos un prospecto real cargado en el pipeline

---

## Siguiente Misión

Una vez completado el pipeline reporta al Mission Engine.

La siguiente misión es:
**Misión 5 — Automation Builder** (crear automatizaciones para que el seguimiento ocurra solo)
