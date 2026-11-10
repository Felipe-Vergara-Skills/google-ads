---
name: feed-de-productos-google
description: "Optimiza el feed de productos de Google Merchant Center, que es el anuncio real en Shopping y Máximo rendimiento: reescribe los títulos con la fórmula del curso (tipo de producto + atributo diferenciador + material + marca, lo buscado en los primeros 70 caracteres), limpia las descripciones de emojis, precios, enlaces y texto promocional que Google sanciona, completa color, talla, material, género, grupo etario y la categoría de producto de Google, y saca del feed lo que no debería estar (tarjetas de regalo, donaciones, productos de otra categoría). Trabaja sobre el archivo exportado de Merchant Center, Shopify, WooCommerce o VTEX, y aguanta catálogos de decenas de miles de productos. Entrega el CSV listo para subir como fuente complementaria, un archivo de comparación y un reporte HTML. Úsala cuando sus productos no reciban clics o impresiones, tenga productos rechazados, quiera mejorar Shopping o Pmax, o pida optimizar su catálogo o su Merchant Center. No es para Meta Ads."
---

# feed-de-productos-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"feed-de-productos-google"`
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
