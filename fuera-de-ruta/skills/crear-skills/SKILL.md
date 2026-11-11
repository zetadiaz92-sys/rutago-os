---
name: crear-skills
description: Explica qué son las skills, agentes, plugins y MCP, cómo se estructuran, y ayuda a crear, mejorar, combinar y mezclar skills. Úsala cuando pregunten cómo funciona una skill o un plugin, o quieran crear/mejorar uno.
---

# Cómo funcionan las skills (y cómo mejorarlas)

## Las 4 piezas
| Pieza | Qué es | Analogía |
| --- | --- | --- |
| **Skill** | Carpeta con un `SKILL.md`: instrucciones para UNA tarea | Una receta |
| **Agente** | Personalidad + reglas que decide qué skill usar | El chef |
| **MCP / conector** | Puente a un servicio externo (Higgsfield, n8n, YouTube…) | Los proveedores |
| **Plugin** | Paquete que junta agentes + skills + MCP para instalar de una vez | El restaurante completo |

Este mismo plugin (`fuera-de-ruta/`) es el ejemplo vivo: ábrelo y muéstraselo al dueño.

## Anatomía de una skill
```
skills/mi-skill/
├── SKILL.md          ← obligatorio
├── plantillas/       ← opcional: ejemplos, formatos
└── scripts/          ← opcional: código que la skill ejecuta
```
`SKILL.md`:
```markdown
---
name: mi-skill
description: QUÉ hace y CUÁNDO usarla (esto decide si Claude la activa).
---
# Instrucciones paso a paso, ejemplos, formato de salida.
```

## Cómo mejorar una skill
1. **La `description` es lo más importante:** incluye las palabras que el dueño usaría
   ("video", "subir", "ganar dinero").
2. **Pasos numerados y formato de salida fijo** (tablas) → resultados consistentes.
3. **Un ejemplo bueno** vale más que diez reglas.
4. **Prueba y ajusta:** usa la skill 3 veces, anota qué salió mal, corrige solo eso.
5. Si crece mucho, mueve detalles a archivos aparte y enlázalos.

## Unir y mezclar skills
- **Encadenar:** la salida de una es la entrada de otra (guion → video → publicar).
  Se hace en el agente, que define el orden.
- **Fusionar:** si dos skills siempre se usan juntas, únelas en una.
- **Dividir:** si una skill hace demasiadas cosas, sepárala.
- **Especializar:** copia una skill y adáptala a un nicho (`guion-viral` → `guion-recetas`).

## Instalar / compartir
Con el plugin en un repo de GitHub: `/plugin marketplace add <usuario>/<repo>` y luego
`/plugin install <nombre>`. Ver `GUIA.md`.

Para crear skills nuevas con evaluación incluida, existe la skill oficial `skill-creator`.
