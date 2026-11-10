---
name: columnas-google-ads
description: "Entrega la lista exacta y en orden de las columnas a configurar en Google Ads según el modelo de negocio (tienda online, servicios / leads o negocio local), con el nombre con que hay que buscar cada una en la interfaz en español (muchas cambian por la traducción: \"Tipo de estrategia de oferta\", \"Valor de conversión / costo\", \"Porcentaje de conversión\", \"Vistas de TrueView\", \"Nivel de calidad\"), qué columnas existen solo en ciertos tipos de campaña y las de nivel palabra clave. Úsala cuando el usuario pregunte qué columnas poner en Google Ads, qué métricas ver, cómo configurar su vista, no encuentre una métrica (ROAS, tasa de conversión, Quality Score), no entienda sus resultados o vaya a exportar un informe para analizar. No es para Meta Ads (para eso está columnas-ads-manager)."
---

# columnas-google-ads

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"columnas-google-ads"`
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
