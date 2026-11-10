---
name: investigador-keywords-google
description: "Investiga y construye las palabras clave de una campaña de Google Ads con respaldo de fuente. Descubre términos por el Planificador (MCP o export), por Semrush si lo tienes, y por investigación web gratuita (autocompletar, \"Más preguntas\", búsquedas relacionadas, vocabulario de competidores y lenguaje de reseñas). Clasifica cada término por intención —transaccional, comercial, informacional o de marca— y lo enruta: los que vale pagar van a grupos de 5-7 en concordancia de frase con su landing, los informacionales van a una lista de contenido SEO en vez de quemar presupuesto, y los que no deben activar salen como negativas de arranque. Cada palabra clave lleva su fuente y su volumen real, o `—` si no se pudo medir. Úsala cuando pida investigación de palabras clave, keyword research, qué palabras poner, volumen de búsqueda, concordancias, agrupar keywords o negativas iniciales. No usar para Meta Ads."
---

# investigador-keywords-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"investigador-keywords-google"`
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
