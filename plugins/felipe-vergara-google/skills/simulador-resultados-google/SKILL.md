---
name: simulador-resultados-google
description: "Simulador de campañas de Google Ads: predice clics, impresiones, ventas, leads, llamadas, conversiones, vistas de YouTube, costo por resultado y ROAS a partir de un presupuesto y sus métricas (CPC medio, porcentaje de conversión, CPM, CTR, tasa de vistas). Cuatro modos: ventas en tienda online (Búsqueda, Shopping, Pmax), leads, mensajes o llamadas (servicios y negocio local), Generación de demanda y vistas en YouTube. Toma las métricas reales de la cuenta por MCP o CSV si el usuario quiere, genera 3 escenarios (conservador, moderado, optimista) y los compara contra el número mágico de calculadora-de-presupuestos-google si existe. Úsala cuando pregunte qué resultados tendrá si invierte X en Google Ads, cuántas ventas, leads o llamadas va a sacar, qué ROAS o costo por lead esperar, o pida simular o proyectar una campaña. No es para Meta Ads. No calcula cuánto invertir (calculadora)."
---

# simulador-resultados-google

**Acción única: hazla ahora, sin nada previo.**

Llama a la tool **`fvg_run_playbook`** (del MCP de Google Ads de Felipe Vergara) con estos argumentos:

- `skillId`: `"simulador-resultados-google"`
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
