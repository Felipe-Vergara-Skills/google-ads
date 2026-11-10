---
name: constructor-de-landing-google
description: "Construye la primera versión de una landing page para Google Ads y la entrega como archivo HTML listo para alojar, una por grupo de anuncios, con el método RCCA (Relevancia, Claridad, Confianza, Acción) y los 15 puntos del checklist de destino del curso. El titular refleja la palabra clave de su grupo, y el reporte declara la tabla de calce palabra clave → anuncio → landing, que es lo que mueve la Experiencia en la página de destino del Nivel de calidad. No inventa testimonios, cifras, garantías ni certificaciones: los deja como marcadores visibles y no declara la página lista mientras falte un punto de prioridad alta. Deja el botón y el formulario cableados para medir la conversión. Modos: servicios, producto único y negocio local sin web. Úsala cuando pida crear o armar una landing, una página de destino o un esqueleto de landing, o no tenga a dónde mandar el tráfico. Para auditar una que ya existe, usa optimizacion-destino-google. No usar para Meta Ads ni para montar una tienda online."
---

# constructor-de-landing-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"constructor-de-landing-google"`
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
