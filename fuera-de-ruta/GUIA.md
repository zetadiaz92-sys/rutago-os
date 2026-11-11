# Fuera de ruta — guía de inicio

Tu primer agente personal. Crea videos con IA, te ayuda a publicarlos, a automatizar y a
buscar formas reales de ganar dinero, y de paso te enseña cómo está construido.

## Qué hay dentro

```
fuera-de-ruta/
├── .claude-plugin/plugin.json      ← "carnet" del plugin
├── agents/fuera-de-ruta.md         ← el agente: personalidad y reglas
├── skills/
│   ├── guion-viral/                ← ideas, ganchos, guiones, títulos
│   ├── videos-higgsfield/          ← videos e imágenes con IA
│   ├── publicar-redes/             ← descripciones, hashtags, calendario
│   ├── automatizar-contenido/      ← flujos n8n y tareas programadas
│   ├── ganar-dinero/               ← monetización y compra-venta
│   └── crear-skills/               ← cómo funcionan y se mejoran las skills
└── .mcp.json.ejemplo               ← conexión a Higgsfield
```

## 1. Instalar el plugin (Claude Code)

```
/plugin marketplace add zetadiaz92-sys/rutago-os
/plugin install fuera-de-ruta@rutago
```

Después escribe, por ejemplo: *"Fuera de ruta, hazme un guion de 30 s para TikTok sobre
cómo ahorrar gasolina en moto y los prompts de video para Higgsfield."*

## 2. Conectar Higgsfield

Higgsfield cobra por créditos; necesitas una cuenta en higgsfield.ai.

**Opción A — conector alojado (más fácil).** Hay reportes de un servidor MCP oficial en
`https://mcp.higgsfield.ai/mcp` con inicio de sesión de tu cuenta. **Compruébalo en la
documentación de Higgsfield** antes de usarlo. Si existe:
- En claude.ai: Ajustes → Conectores → *Añadir conector personalizado* → pega la URL.
- En Claude Code: renombra `.mcp.json.ejemplo` a `.mcp.json` y reinstala el plugin
  (o `claude mcp add --transport http higgsfield https://mcp.higgsfield.ai/mcp`).

**Opción B — servidor comunitario con clave API.** Existen servidores MCP de terceros
(p. ej. `geopopos/higgsfield_ai_mcp` en GitHub) que usan tu clave y secreto del panel de
Higgsfield como variables de entorno. Revisa su código antes de darle tus claves.

**Nunca pegues tus claves en el chat ni las subas a GitHub.**

Sin conexión el agente sigue funcionando: te da los prompts listos para pegar en la web.

## 3. Ruta de aprendizaje sugerida

| Semana | Aprendes | Pide al agente |
| --- | --- | --- |
| 1 | Guiones y ganchos | "Dame 10 ideas para mi nicho y guioniza la mejor" |
| 2 | Video con IA | "Convierte este guion en prompts de Higgsfield, imagen primero" |
| 3 | Publicar y medir | "Prepárame descripción, hashtags y calendario de 2 semanas" |
| 4 | Dinero | "¿Qué vía de ingresos me conviene empezar con lo que tengo?" |
| 5 | Automatizar | "Diseña un flujo n8n que me proponga ideas cada lunes" |
| 6 | Skills propias | "Enséñame a crear una skill para mi nicho" |

## 4. Mejorar tu agente

Cada vez que algo salga mal, dile: *"Mejora la skill X para que la próxima vez haga Y."*
Así el agente aprende contigo. La skill `crear-skills` explica cómo funciona por dentro.
