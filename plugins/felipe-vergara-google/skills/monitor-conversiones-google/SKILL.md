---
name: monitor-conversiones-google
description: "Monitorea la salud de las conversiones de Google Ads: revisa cada acción de conversión (estado, principal o secundaria, recuento, valor, ventana y modelo de atribución) contra lo que enseña el curso, compara las conversiones de los últimos 7 días contra los 7 previos y lanza una ALERTA si alguna cayó más del 20%, revisa el etiquetado automático y revisa en la web la etiqueta de Google (AW-), Analytics, Tag Manager y el modo de consentimiento v2. Lee la cuenta por MCP de Google Ads o por CSV. Úsala cuando diga revisar conversiones, seguimiento de conversiones, etiqueta de Google, \"mis conversiones bajaron\", \"no me marca las ventas\", conversión inactiva, Tag Assistant, modo de consentimiento, o quiera saber si Google Ads está midiendo bien. También sirve como revisión semanal programada. No es para Meta (monitor-pixel)."
---

# monitor-conversiones-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"monitor-conversiones-google"`
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
