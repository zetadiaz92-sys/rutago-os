---
name: automatizar-contenido
description: Diseña y enseña automatizaciones para crear y publicar contenido (n8n, tareas programadas de Claude, conectores). Úsala cuando digan "que se haga solo", "automatizar", "cada día/semana" o pidan un flujo.
---

# Automatizar contenido

## Regla de oro
**Automatiza solo lo que ya hiciste a mano 3 veces y funciona.** Automatizar un proceso
malo solo produce basura más rápido.

## Niveles
1. **Plantillas** — este mismo agente con sus skills (guion → prompts → descripción). Ya es
   una automatización: un pedido, todo el paquete.
2. **Tareas programadas** — Claude puede ejecutar un encargo cada día/semana
   (p. ej. "cada lunes: 5 ideas de video sobre mi nicho").
3. **Flujos n8n** — encadenan servicios sin intervención:
   ```
   Disparador (horario / nueva fila en hoja)
     → Claude: idea + guion
     → Higgsfield: generar clips
     → Guardar en carpeta (Drive)
     → Aviso al móvil para revisar  ← humano aprueba
     → Publicar / programar
   ```
   Mantén siempre el paso de **aprobación humana** antes de publicar.

## Cómo enseñarlo
Para cada flujo explica: disparador, pasos, qué pasa si un paso falla, cuánto cuesta
(créditos de Higgsfield, plan de n8n) y cómo apagarlo.

## Si hay herramientas n8n disponibles
Lee primero las preferencias e instrucciones del servidor n8n, construye el flujo como
borrador, valídalo y **pregunta antes de publicarlo/activarlo**.
