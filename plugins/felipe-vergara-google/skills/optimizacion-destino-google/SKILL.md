---
name: optimizacion-destino-google
description: "Audita a dónde llegan las personas después del clic en Google Ads (la tienda online, la landing de servicios o la ficha de Google Business de un negocio local) navegándolo de verdad y compara lo que encuentra contra el checklist del curso: precio y reseñas visibles, velocidad e imágenes de más de 150 KB, botón de compra, formulario, testimonios, contacto, WhatsApp, categoría, fotos, horario y respuestas a reseñas. Cruza con las métricas de la cuenta (porcentaje de conversión, experiencia en la página de destino, CTR del recurso de ubicación) si las hay y entrega acciones específicas a lo encontrado, no genéricas. Úsala SOLO cuando el usuario la pida: dice que tiene clics pero no vende, que su porcentaje de conversión es bajo, que los leads no son buenos, que su ficha no trae visitas o que quiere mejorar su página. No se dispara desde otras skills. No es para Meta Ads."
---

# optimizacion-destino-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"optimizacion-destino-google"`
- `goal`: el pedido del alumno verbatim (sin reescribir; incluye las URLs, IDs o archivos que haya dado)

La tool puede aparecer con un prefijo distinto según el cliente (`mcp__felipe-google__fvg_run_playbook`, `mcp__plugin_felipe-vergara-google_felipe-google__fvg_run_playbook`, un UUID). Usa la que termine en `fvg_run_playbook`. Si no la ves en tu lista, búscala con tu buscador de tools por `fvg_run_playbook` antes de darla por inexistente. No uses una tool `run_playbook` de otro MCP: esa es de otro curso y no conoce esta skill.

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del proyecto, ni preguntas preliminares al alumno. La skill que devuelve el MCP ya trae su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual, empezando por el PASO 0 (tener en disco los archivos de la skill).

Si la llamada falla:

- La tool no existe, pide autenticación, responde 401 o "Couldn't reach": dispara la skill `configurar-token-google`.
- 403: dile al alumno, con tus palabras y sin tecnicismos, lo que indica el mensaje del servidor (su token fue renovado o su acceso venció, y dónde sacar el vigente).
- 429: "dame 1 minuto" y reintenta después.
- 503: espera unos segundos y reintenta una vez.

No reconstruyas ni improvises la skill si el MCP no responde. NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
