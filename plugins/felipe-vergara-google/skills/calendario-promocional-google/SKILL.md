---
name: calendario-promocional-google
description: "Arma el calendario promocional del año para Google Ads: investiga qué fechas mueven ventas en los países donde el negocio vende y en su nicho (comerciales como Black Friday, Cyber Monday, Día de la Madre o Navidad, festivos propios de cada país, días temáticos del rubro y fechas de la marca como aniversario, lanzamiento o preventa), y recomienda las 3 o 4 iniciativas del año que valen la pena. De cada una entrega fechas de inicio y fin, estructura de campañas (Máximo rendimiento sola o con Generación de demanda en remarketing a 180 días), públicos y si hay que excluir clientes, cuántos anuncios preparar, el mensaje, cuándo empezar a producir los creativos y si corresponde o no un ajuste de estacionalidad, con el cálculo. Entrega un HTML. Úsala cuando pregunte qué promociones lanzar, cómo planear Black Friday o Navidad, su calendario de marketing o de campañas del año. No es para Meta Ads."
---

# calendario-promocional-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"calendario-promocional-google"`
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
