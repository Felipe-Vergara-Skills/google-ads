---
name: diversificacion-creativa-google
description: "Genera una matriz de 30 ganchos para anuncios de Google Ads cruzando los 3 deseos de Reiss de la marca, 2 perfiles de cliente y los 5 niveles de conciencia, con la capa de Google que le corresponde a cada nivel (Capa 6 branding en YouTube, Capa 3 Máximo rendimiento, Capas 4 y 5 remarketing y recompra). Cada gancho trae su ángulo y un título listo para Pmax o Generación de demanda, validado contra los límites de caracteres. Lee marca-cliente.json; si no existe, escanea la web primero. Después puede desarrollar un gancho como guion de video para YouTube, anuncio de imagen o carrusel de Generación de demanda. Úsala cuando quiera ideas o ganchos para anuncios de Google, no sepa qué decir en sus imágenes o videos, sus anuncios se parezcan entre sí, pida diversificar creativos, una matriz de anuncios o hooks para YouTube, Demand Gen o Pmax. No es para Meta Ads (diversificacion-creativa)."
---

# diversificacion-creativa-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"diversificacion-creativa-google"`
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
