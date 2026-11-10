---
name: calculadora-de-presupuestos-google
description: "Calcula cuánto invertir al mes en Google Ads y el número mágico del negocio: ROAS objetivo, costo por compra objetivo y CPC máximo en tienda online; costo por lead y costo por cliente objetivo en servicios y negocio local. Parte de la meta de ventas, el ticket promedio, el % del margen que el negocio está dispuesto a invertir y su tasa de conversión (de la tienda, o de leads a ventas). Úsala cuando el usuario quiera saber cuánto invertir en Google Ads, su presupuesto, su ROAS objetivo, su número mágico, cuánto puede pagar por una venta, un lead, un cliente o un clic, o diga que no sabe cuánto poner en sus campañas, aunque no diga \"calculadora\". No es para Meta Ads. No reparte el presupuesto entre campañas (estrategia-por-capas-google) ni analiza campañas (metodologia-3qs-google)."
---

# calculadora-de-presupuestos-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"calculadora-de-presupuestos-google"`
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
