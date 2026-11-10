---
name: generador-de-nombres-google
description: "Genera nombres estandarizados para campañas, grupos de anuncios, grupos de recursos (Máximo rendimiento) y anuncios (Generación de demanda) de Google Ads, con la nomenclatura del generador de nombres del curso: anunciante, capa de la estrategia por capas (C1 a C6), objetivo, estrategia de puja, temporada, segmentación, landing, concordancia, formato, nivel de conciencia y llamado a la acción. Nombra una pieza suelta o la estructura completa de una vez, leyendo el reporte de la estrategia por capas si existe. Úsala cuando el usuario quiera nombrar campañas de Google Ads, estandarizar la nomenclatura, no sepa cómo llamar una campaña, grupo o anuncio, o diga \"ponle nombre\", \"nomenclatura\", \"cómo nombro esto en Google\". No es para Meta Ads (para eso está generador-de-nombres)."
---

# generador-de-nombres-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"generador-de-nombres-google"`
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
