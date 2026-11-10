---
name: estrategia-por-capas-google
description: "Genera la estrategia de campañas de Google Ads por capas: 1 Búsqueda de marca, 2 Shopping o Búsqueda no-marca, 3 Máximo rendimiento, 4 Remarketing, 5 Recompra, 6 Branding con Demand Gen; para tienda online, servicios o negocio local, con el presupuesto repartido según el escenario (2, 4 o 6 capas). Por campaña entrega la configuración completa (puja, presupuesto, ubicación, redes, grupos, públicos, exclusiones), palabras clave por grupo con concordancia, negativas y recursos (vínculos, textos destacados, llamada, ubicación). HTML con una pestaña por capa. Úsala cuando quiera armar su estrategia de Google Ads, no sepa cuántas campañas crear ni cómo repartir el presupuesto, o pida estructura, palabras clave, negativas o extensiones. No es para Meta Ads. No calcula cuánto invertir (calculadora-de-presupuestos-google) ni escribe anuncios RSA (niveles-de-consciencia-google)."
---

# estrategia-por-capas-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"estrategia-por-capas-google"`
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
