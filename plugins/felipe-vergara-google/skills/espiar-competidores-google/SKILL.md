---
name: espiar-competidores-google
description: "Espía a los competidores de un negocio en Google: sus anuncios en el Centro de Transparencia de Anuncios de Google (texto, imagen y video, dónde anuncian y desde cuándo), quién aparece en los anuncios patrocinados de las búsquedas clave, sus precios, su ficha de Google Maps y, como complemento, la Biblioteca de Anuncios de Meta. El usuario solo pasa la URL de su negocio: la skill detecta el rubro, propone competidores, los confirma y los analiza junto a su marca. HTML con una pestaña por competidor: títulos y ganchos, ángulos, niveles de conciencia, ofertas, formatos, precios y tabla comparativa. Úsala cuando diga \"espiar competidores\", \"Centro de Transparencia\", \"qué anuncios corre mi competencia en Google\", \"quién me compite en la subasta\", \"ofertas o precios de la competencia\", \"análisis competitivo\". No es para Meta Ads (espiar-competidores). Descriptiva: no recomienda."
---

# espiar-competidores-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"espiar-competidores-google"`
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
