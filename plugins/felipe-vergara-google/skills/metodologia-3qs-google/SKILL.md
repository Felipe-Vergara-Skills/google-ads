---
name: metodologia-3qs-google
description: "Analiza campañas de Google Ads con las 3 Q's (¿Qué pasó? / ¿Por qué pasó? / ¿Qué haremos?) y benchmarks semáforo (🔴/🟡/🟢) por nicho: tienda online, servicios / leads y negocio local. Lee la cuenta por MCP de Google Ads (solo lectura) o por CSV exportado, a nivel campaña, grupo y anuncio, con palabras clave y términos de búsqueda opcionales. Cubre Búsqueda, Shopping, Pmax y Demand Gen. Mide contra el objetivo (ROAS, costo por lead o por conversión local), diagnostica el cuello de botella y entrega acciones en un HTML. Úsala SIEMPRE que quiera analizar campañas de Google Ads, saber por qué no convierten, evaluar ROAS, CPA, CTR, Nivel de calidad o cuota de impresiones, revisar términos o negativas, decidir qué pausar u optimizar, o suba un CSV de Google Ads. Actívala aunque no diga \"Google\" si habla de Búsqueda, Shopping, Pmax, Demand Gen o Merchant Center. No usar para Meta Ads, TikTok ni LinkedIn, ni para crear campañas."
---

# metodologia-3qs-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"metodologia-3qs-google"`
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
