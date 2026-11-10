---
name: escanear-marca-google
description: "Escanea la web de una marca para extraer su ADN antes de hacer Google Ads: identidad visual (colores, tipografía, logo, estilo de imágenes), tono y voz, avatar con los 16 Deseos de Reiss, nivel de conciencia dominante del copy, tipo de oferta, propuesta de valor, producto y precio, más su presencia en Google: nombre para los anuncios (25 caracteres), ficha de Google Maps, páginas principales para vínculos al sitio, plataforma de la tienda y etiquetas de Google instaladas. Guarda marca-cliente.json para que las demás skills de Google Ads no repregunten la marca, y un HTML descriptivo. Úsala cuando diga \"escanear marca\", \"ADN de marca\", \"identidad de marca\", \"tono de marca\", \"colores de la marca\", \"avatar del cliente\", \"propuesta de valor\", o al arrancar con un cliente nuevo de Google Ads. No es para Meta Ads (para eso está escanear-marca). No investiga reseñas ni competidores (7-maletas-google)."
---

# escanear-marca-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"escanear-marca-google"`
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
