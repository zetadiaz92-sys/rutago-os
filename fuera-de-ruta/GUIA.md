# Fuera de ruta — guía de inicio

<img src="assets/mango.jpg" alt="Mango, el gato de Fuera de ruta" width="240">

*Con Mango 🐱☁️, el gato que vive en la nube y te recuerda la tarea de cada día.*

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

## 3. Mango diario (mensaje cada mañana por Telegram)

En tu n8n está el flujo **"Mango diario · Fuera de ruta"** (creado como borrador, apagado).
Cada día a las 08:00 te manda: el día del plan (1 a 30), la tarea de hoy, cómo vas (barra
de progreso) y la frase para pedirle ayuda a Fuera de ruta.

Para encenderlo:
1. En Telegram, abre **@BotFather** → `/newbot` → ponle nombre (p. ej. *Mango*) → copia el token.
2. En n8n crea la credencial **"Bot de Mango"** (tipo Telegram) y pega el token ahí — nunca en un chat.
3. Escríbele `/start` a tu bot. Pide tu *chat ID* a **@userinfobot** y pégalo en el nodo
   "Enviar a Telegram".
4. Pulsa *Execute workflow* para probar y, si te llega el mensaje, publícalo/actívalo.
5. La fecha de inicio está en el nodo "Plan de 30 días" (`inicio`), por defecto 2026-11-12.

**¿Y WhatsApp?** Se puede, pero es más difícil: necesitas WhatsApp Business Cloud API (Meta)
con un número verificado y plantillas aprobadas para mensajes que inicia el bot, o un
proveedor como Twilio (de pago). Por eso empezamos con Telegram, que es gratis e inmediato.

## 4. Ruta de aprendizaje sugerida

| Semana | Aprendes | Pide al agente |
| --- | --- | --- |
| 1 | Guiones y ganchos | "Dame 10 ideas para mi nicho y guioniza la mejor" |
| 2 | Video con IA | "Convierte este guion en prompts de Higgsfield, imagen primero" |
| 3 | Publicar y medir | "Prepárame descripción, hashtags y calendario de 2 semanas" |
| 4 | Dinero | "¿Qué vía de ingresos me conviene empezar con lo que tengo?" |
| 5 | Automatizar | "Diseña un flujo n8n que me proponga ideas cada lunes" |
| 6 | Skills propias | "Enséñame a crear una skill para mi nicho" |

## 5. Mejorar tu agente

Cada vez que algo salga mal, dile: *"Mejora la skill X para que la próxima vez haga Y."*
Así el agente aprende contigo. La skill `crear-skills` explica cómo funciona por dentro.
