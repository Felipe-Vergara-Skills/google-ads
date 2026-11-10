---
name: crear-campana-google
description: "Crea una campaña de Google Ads completa desde cero en una sola corrida: encadena marca, investigación de mercado, presupuesto, estructura por capas, textos de anuncios, ganchos creativos y nomenclatura, con solo dos pausas para pedirte datos, y entrega un único reporte HTML con todo lo necesario para montarla. Incluye el checklist de configuración de la cuenta: lo irreversible (moneda, zona horaria, facturación), el cupón de bienvenida, negativas de cuenta, vínculos y accesos. Úsala cuando diga \"crea una campaña\", \"arranca de cero\", \"quiero anunciarme en Google\", \"estrategia de Google Ads\", \"configurar mi cuenta de Google Ads\", \"monta mi cuenta nueva\", \"campaña completa\", o cuando pegue la URL de su negocio pidiendo campañas. Sirve para tienda online, servicios y negocio local. No toca la cuenta: entrega el plan para que lo monte quien tenga los accesos. No es para Meta Ads. No diagnostica campañas que ya están corriendo: para eso está metodologia-3qs-google."
---

# crear-campana-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"crear-campana-google"`
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
