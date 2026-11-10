---
name: analizador-ads-estaticos-google
description: "Deconstruye un anuncio estático (imagen) en sus componentes de marketing, diseño y copywriting y explica por qué funciona, con un reporte Markdown de 32 secciones: jerarquía visual, copywriting, nivel de conciencia y sofisticación de Schwartz, LF8, NESB, emociones, posicionamiento, fórmula del anuncio, recreación para un producto ficticio y cómo llevar esa fórmula a Google Ads (capa, formato de Generación de demanda o Máximo rendimiento, recortes y políticas). Acepta una imagen adjunta, una captura del Centro de Transparencia de Google o un enlace a un anuncio de ese centro. Úsala cuando adjunte un anuncio de Google (Demand Gen, Display, Pmax, YouTube, Discover, Gmail) o de otra plataforma y pida analizarlo, entender por qué funciona, hacerle ingeniería inversa o extraer aprendizajes para sus campañas de Google. Si quiere recrearlo con su producto y el prompt de imagen → deconstructor-de-imagenes-google. No es para Meta Ads (analizador-ads-estaticos)."
---

# analizador-ads-estaticos-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"analizador-ads-estaticos-google"`
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
