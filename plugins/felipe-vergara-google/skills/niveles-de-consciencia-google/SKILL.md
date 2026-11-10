---
name: niveles-de-consciencia-google
description: "Diagnostica en qué niveles de conciencia está el mercado (inconsciente, problema, solución, producto, decisión) con evidencia real y escribe los anuncios de Google Ads para cada nivel, según la capa que le corresponde: anuncios de Búsqueda (RSA: 15 títulos y 4 descripciones) para marca y no marca, textos del grupo de recursos de Máximo rendimiento, y anuncios de Generación de demanda para remarketing, recompra y branding en YouTube. Respeta los límites de caracteres y las políticas, y los valida antes de entregar. Lee el reporte de 7-maletas-google si existe; si no, investiga web, reseñas y búsquedas. Úsala cuando quiera anuncios o copy para Google Ads, títulos y descripciones, RSA, textos de Pmax o Demand Gen, saber cómo hablarle a su mercado o pasar de las 7 maletas a los anuncios. No es para Meta Ads (niveles-de-consciencia). No arma la estrategia ni reparte presupuesto."
---

# niveles-de-consciencia-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"niveles-de-consciencia-google"`
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
