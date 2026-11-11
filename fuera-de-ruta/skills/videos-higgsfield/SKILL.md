---
name: videos-higgsfield
description: Genera y mejora videos e imágenes con IA usando Higgsfield (texto→video, imagen→video, movimientos de cámara, personajes consistentes). Úsala cuando pidan crear un clip, una toma, una imagen o mejorar un prompt de video.
---

# Videos con Higgsfield

## Conexión (una sola vez)
Ver `GUIA.md` → "Conectar Higgsfield". Si las herramientas de Higgsfield (MCP) no están
disponibles en la sesión, **no inventes resultados**: entrega los prompts listos para pegar
en la web de Higgsfield y explica cómo conectar el MCP.

## Flujo
1. Toma la columna "Lo que se ve" del guion (`guion-viral`). Cada fila = un clip de 3–10 s.
2. Escribe un prompt por clip con esta fórmula:

   `[Sujeto] + [acción] + [lugar] + [luz/hora] + [movimiento de cámara] + [estilo] + [formato]`

   Ejemplo: *"Joven repartidor en moto cruzando una avenida de noche, luces de neón
   reflejadas en el asfalto mojado, cámara en travelling lateral siguiendo la moto, estilo
   cinematográfico, 9:16 vertical."*
3. **Imagen primero, luego video:** genera una imagen base del personaje/escena y anímala
   (imagen→video). Así mantienes el mismo personaje entre clips.
4. Muestra el plan (n.º de clips, modelo, créditos aprox.) y **pide confirmación** antes de generar.
5. Revisa cada resultado: ¿manos/caras raras?, ¿movimiento coherente?, ¿texto ilegible?
   Si falla, cambia **una sola variable** del prompt y vuelve a intentar.

## Formatos
- TikTok / Reels / Shorts: **9:16**, 1080×1920.
- YouTube largo: **16:9**.
- Miniatura: imagen 16:9 de alto contraste.

## Montaje
Higgsfield da clips sueltos; el montaje (voz, música, subtítulos) va en CapCut, DaVinci
Resolve u otra herramienta de edición. Indica el orden de clips y dónde va cada texto.

## Enseñanza
Explica qué parte del prompt cambió el resultado. Así el dueño aprende a "dirigir" la IA.
