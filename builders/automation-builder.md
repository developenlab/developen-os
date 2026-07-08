# Developen OS — Automation Builder
Version: 0.2
ID: BUILDER_AUTOMATION
Tipo: Builder Especializado
Responsabilidad: Crear automatizaciones y workflows dentro de Developen Suite para que el negocio del EduFounder opere sin intervención manual.

---

## Objetivo

El Automation Builder elimina el trabajo manual repetitivo del EduFounder.

Cada automatización que se construye aquí es tiempo que el EduFounder recupera y prospectos que dejan de perderse por falta de seguimiento.

Al terminar esta misión el EduFounder tiene workflows activos que trabajan solos — mientras duerme, mientras da clases, mientras vive.

---

## Qué Entrega al EduFounder

Al completar esta misión el EduFounder tiene:

- Automatizaciones activas en Developen Suite
- Seguimiento automático de prospectos
- Entrega automática del producto al comprar
- Mensajes automáticos en los momentos correctos
- Un negocio que opera sin depender completamente de él

---

## Automatizaciones Prioritarias

### Automatización 1 — Bienvenida a Nuevo Prospecto
**Trigger:** Nuevo contacto llega al pipeline (desde landing, WhatsApp o formulario)
**Objetivo:** Contactar en menos de 5 minutos sin que el EduFounder tenga que hacerlo manualmente

**Flujo:**
```
TRIGGER: Contacto entra al pipeline → Etapa "Nuevo Prospecto"
↓
ESPERA: 2 minutos
↓
ACCIÓN: Enviar WhatsApp
MENSAJE:
"Hola [nombre] 👋 
Gracias por tu interés en [producto].
Soy [nombre del EduFounder] y estoy aquí para ayudarte.
¿Me puedes contar brevemente qué tipo de negocio educativo tienes o quieres construir?"
↓
ACCIÓN: Crear tarea para el EduFounder
"Dar seguimiento a [nombre] — llegó hace 5 minutos"
```

---

### Automatización 2 — Seguimiento a Prospecto Sin Respuesta
**Trigger:** Prospecto no respondió en 24 horas
**Objetivo:** Reactivar el contacto sin esfuerzo manual

**Flujo:**
```
TRIGGER: Contacto en etapa "Contactado" sin actividad por 24 horas
↓
ACCIÓN: Enviar WhatsApp
MENSAJE:
"Hola [nombre], quería ver si tuviste oportunidad de leer mi mensaje de ayer.
Entiendo que el tiempo es poco — te prometo que seré breve.
¿Tienes 2 minutos para contarme tu situación?"
↓
ESPERA: 48 horas sin respuesta
↓
ACCIÓN: Enviar WhatsApp final
MENSAJE:
"[Nombre], este es mi último mensaje para no ser molesto 😊
Si en algún momento quieres explorar cómo [resultado de la oferta], con gusto te ayudo.
Aquí estaré."
↓
ACCIÓN: Mover a etapa "Perdido" y agregar tag "Seguimiento 30 días"
```

---

### Automatización 3 — Entrega Automática del Producto
**Trigger:** Pago confirmado
**Objetivo:** El alumno recibe acceso inmediato sin intervención manual del EduFounder

**Flujo:**
```
TRIGGER: Pago confirmado para [producto]
↓
ACCIÓN: Dar acceso al curso en Developen Suite
↓
ACCIÓN: Enviar email de bienvenida
ASUNTO: "¡Bienvenido a [producto]! Aquí está tu acceso"
CONTENIDO:
"Hola [nombre],

¡Felicidades por dar este paso! Tu acceso a [producto] ya está activo.

Ingresa aquí: [link de acceso]

En los próximos minutos recibirás un WhatsApp mío para darte la bienvenida personalmente.

[Firma del EduFounder]"
↓
ESPERA: 5 minutos
↓
ACCIÓN: Enviar WhatsApp de bienvenida
MENSAJE:
"¡Bienvenido [nombre]! 🎉
Ya tienes acceso a [producto].
¿Pudiste ingresar sin problema?
Aquí estoy para cualquier duda que tengas."
↓
ACCIÓN: Mover contacto a etapa "Ganado" en el pipeline
↓
ACCIÓN: Agregar tag "Alumno Activo"
↓
ACCIÓN: Crear tarea "Verificar que [nombre] inició el programa en 48 horas"
```

---

### Automatización 4 — Recordatorio de Seguimiento Post-Compra
**Trigger:** 7 días después de la compra
**Objetivo:** Verificar que el alumno esté avanzando y generar testimonio

**Flujo:**
```
TRIGGER: 7 días después de etiqueta "Alumno Activo"
↓
ACCIÓN: Enviar WhatsApp
MENSAJE:
"Hola [nombre], ya llevas una semana en [producto] 🚀
¿Cómo vas? ¿Has tenido alguna duda o necesitas apoyo en algo?
Me interesa saber cómo te está yendo."
↓
ESPERA: 14 días después de la compra
↓
ACCIÓN: Enviar WhatsApp de check-in
MENSAJE:
"[Nombre], dos semanas ya 💪
¿Cuál ha sido tu mayor aprendizaje o resultado hasta ahora?
Me encantaría saber cómo va tu proceso."
```

---

### Automatización 5 — Solicitud de Testimonio
**Trigger:** 21 días después de la compra
**Objetivo:** Obtener testimonios de forma automática

**Flujo:**
```
TRIGGER: 21 días después de etiqueta "Alumno Activo"
↓
ACCIÓN: Enviar WhatsApp
MENSAJE:
"[Nombre], ya llevas 3 semanas en [producto] y quiero pedirte un favor 🙏

Estoy ayudando a más personas como tú y un video corto tuyo (1-2 minutos) 
contando tu experiencia sería de mucho valor para ellos.

Solo respóndeme estas 3 preguntas en video:
1. ¿Cómo estabas antes de entrar al programa?
2. ¿Qué resultado o cambio has notado?
3. ¿A quién se lo recomendarías?

¿Me lo puedes grabar cuando tengas un momento?"
```

---

## Proceso de Construcción en Developen Suite

### Paso 1 — Acceder al Constructor de Automatizaciones
```
En Developen Suite ve a:
Automatización → Workflows → Crear workflow
```

### Paso 2 — Configurar el Trigger
```
Selecciona el evento que dispara la automatización:
- Contacto añadido al pipeline
- Etapa del pipeline cambiada
- Formulario enviado
- Pago completado
- Tag agregado
- Fecha específica
- Tiempo transcurrido desde evento
```

### Paso 3 — Agregar Acciones
```
Disponibles en Developen Suite:
- Enviar WhatsApp (mensaje de texto)
- Enviar Email
- Crear tarea
- Cambiar etapa del pipeline
- Agregar o remover tag
- Esperar X tiempo
- Condición (si/sino)
- Asignar a usuario
- Crear oportunidad
- Notificación interna
```

### Paso 4 — Configurar Condiciones
```
Usa condiciones para personalizar el flujo:
SI [condición] ENTONCES [acción A]
DE LO CONTRARIO [acción B]

Ejemplo:
SI el contacto respondió en 24 horas → mover a "Calificado"
DE LO CONTRARIO → enviar mensaje de seguimiento
```

### Paso 5 — Activar y Probar
```
1. Guarda el workflow
2. Activa el workflow (toggle ON)
3. Crea un contacto de prueba
4. Ejecuta el trigger manualmente
5. Verifica que cada acción se ejecuta correctamente
6. Ajusta tiempos o mensajes si es necesario
```

---

## Mensajes Listos para Usar

El Automation Builder entrega todos los mensajes escritos y listos para pegar en Developen Suite.

Los mensajes se personalizan con las variables del sistema:
- `[nombre]` → nombre del contacto
- `[producto]` → nombre del producto
- `[link]` → link de acceso o landing
- `[EduFounder]` → nombre del EduFounder

---

## Automatizaciones Entregadas — Formato de Resumen

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
TUS AUTOMATIZACIONES ACTIVAS
[NOMBRE DEL NEGOCIO]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✅ AUTO 1 — Bienvenida nuevo prospecto
   Trigger: Contacto nuevo en pipeline
   Acción: WhatsApp en 2 minutos
   Estado: ACTIVO

✅ AUTO 2 — Seguimiento sin respuesta
   Trigger: 24 horas sin respuesta
   Acción: 2 mensajes de reactivación
   Estado: ACTIVO

✅ AUTO 3 — Entrega del producto
   Trigger: Pago confirmado
   Acción: Acceso + Email + WhatsApp
   Estado: ACTIVO

✅ AUTO 4 — Check-in post-compra
   Trigger: 7 y 14 días post-compra
   Acción: Mensajes de seguimiento
   Estado: ACTIVO

✅ AUTO 5 — Solicitud de testimonio
   Trigger: 21 días post-compra
   Acción: Solicitud de video testimonio
   Estado: ACTIVO

LO QUE HACE TU SISTEMA AHORA SOLO:
→ Contacta prospectos en menos de 5 minutos
→ Da seguimiento automático sin que lo olvides
→ Entrega el producto inmediatamente al comprar
→ Verifica que tus alumnos estén avanzando
→ Pide testimonios en el momento correcto
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Criterio de Éxito

Esta misión está completa cuando:

- ✅ Las 5 automatizaciones prioritarias están activas en Developen Suite
- ✅ Cada automatización fue probada con un contacto de prueba
- ✅ Los mensajes se envían en los tiempos correctos
- ✅ El pipeline se mueve automáticamente según las acciones del prospecto
- ✅ El EduFounder recibe notificaciones de lo que hace el sistema

---

## Siguiente Misión

Una vez completadas las automatizaciones reporta al Mission Engine.

La siguiente misión es:
**Misión 6 — Course Builder** si el producto aún no está construido.
O
**Misión 7 — AI Agent Builder** para agregar inteligencia artificial al proceso de ventas y soporte.
