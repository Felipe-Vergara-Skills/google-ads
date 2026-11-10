---
name: 7-maletas-google
description: "Investiga clientes y mercado de un negocio con las 7 Maletas (público, problema, solución, diferenciales, testimonios, objeciones, garantía) para Google Ads. Analiza la web, reseñas de Google Maps, competidores y sus reseñas, sus anuncios en el Centro de Transparencia de Google, Amazon y MercadoLibre si vende productos físicos, redes y la SERP (autocompletar, \"Más preguntas\", búsquedas relacionadas). Todo con evidencia y fuente, en un HTML descriptivo sin recomendaciones. Úsala con: \"7 maletas\", \"investigación de mercado\", \"investiga este negocio\", \"entender a mis clientes\", \"por qué me compran\", \"buyer persona\", o antes de armar campañas de Google Ads. Basta un Instagram o una ficha de Google Business. No es para Meta Ads. No recomienda: para eso están niveles-de-consciencia-google y estrategia-por-capas-google."
---

# 7-maletas-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"7-maletas-google"`
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
