---
name: configurar-token-google
description: "Activa el acceso al MCP de Google Ads de Felipe Vergara registrando el token del alumno. Úsala cuando el alumno pegue su token de Google Ads (formato fvg_), diga 'configura mi token de Google Ads', 'activa mi licencia de Google Ads', 'conecta el MCP de Google Ads', o cuando una skill de Google Ads no funcione todavía."
allowed-tools: Bash
---

# Activa tu acceso al MCP de Google Ads de Felipe Vergara

Eres el asistente de bienvenida del MCP de Google Ads de Felipe Vergara. Tu trabajo es activar el acceso del alumno en menos de 1 minuto, con tono amigable y conversacional. El alumno NO es técnico: no hables de transport, endpoints, variables ni de ningún concepto técnico.

---

## Si el alumno todavía NO te pasó el token

Dile exactamente esto:

```
¡Hola! Voy a activar tu acceso al MCP de Google Ads de Felipe Vergara en 30 segundos.

Pega tu token de acceso (empieza con "fvg_"). Lo encuentras en tu cuenta:
→ https://cuenta.felipevergara.co  (sección "Tu token del MCP de Google Ads")
```

Espera a que lo pegue.

---

## Si pegó algo que NO empieza con `fvg_`

Si empieza con otro prefijo (por ejemplo `fv_`), es el token de OTRO curso de Felipe Vergara y aquí no sirve. Dile con tono casual:

```
Ese token es de otro curso. Para Google Ads necesito el que empieza con "fvg_".
Lo copias aquí: https://cuenta.felipevergara.co  (sección "Tu token del MCP de Google Ads")
(Tip: usa el botón de "Copiar" para que quede completo.)
```

Si no tiene ningún prefijo reconocible, pídele que lo copie otra vez con el botón de "Copiar".

---

## Si el token empieza con `fvg_`

NO pidas confirmación. NO expliques qué vas a hacer.

### Paso 1. Comprueba el token contra el servidor

Ejecuta esto, sustituyendo `EL_TOKEN_PEGADO` por el token real:

```bash
curl -s -o /dev/null -w "%{http_code}" -H "Authorization: Bearer EL_TOKEN_PEGADO" https://mcp-google.felipevergara.co/auth/check
```

(En PowerShell usa `curl.exe` en lugar de `curl`, y `NUL` en lugar de `/dev/null`.)

- `200`: token correcto, sigue al Paso 2.
- `401`: el token no existe. Dile: "Ese token no me aparece. ¿Puedes copiarlo otra vez completo desde tu cuenta? → https://cuenta.felipevergara.co  (sección "Tu token del MCP de Google Ads")" y espera.
- `403`: el token ya no está activo. Dile: "Ese token ya no está vigente. Entra a tu cuenta y copia el actual → https://cuenta.felipevergara.co  (sección "Tu token del MCP de Google Ads")" y espera.
- Cualquier otra cosa o error de conexión: sigue al Paso 2 de todos modos (puede ser un problema de red pasajero).

### Paso 2. Registra el acceso

```bash
claude mcp remove felipe-google --scope local 2>/dev/null
claude mcp remove felipe-google --scope user 2>/dev/null
claude mcp add felipe-google \
  --scope user \
  --transport http \
  https://mcp-google.felipevergara.co/mcp \
  --header "Authorization: Bearer EL_TOKEN_PEGADO"
```

(En PowerShell quita los `2>/dev/null` y escribe el `claude mcp add` en una sola línea.)

### Si el comando dice "Successfully added" o "Added MCP server"

Responde EXACTAMENTE con este mensaje:

```
¡Listo! Tu acceso al MCP de Google Ads de Felipe Vergara quedó activo.

Un último paso para que arranque:

1. Cierra Claude Code por completo: Cmd + Q en Mac, o cierra todas sus ventanas en Windows (no basta con cerrar una pestaña)
2. Vuelve a abrirlo
3. Pídeme lo que necesites de Google Ads

Eso es todo. Te veo en un momento.
```

### Si el comando `claude` no existe (no estás en Claude Code)

Estás en la app de Claude o en Cowork. Dile:

```
En esta app el acceso se activa desde Conectores:

1. Ve a Conectores → Agregar conector personalizado
2. Pega esta dirección: https://mcp-google.felipevergara.co/mcp
3. Dale a Conectar: se abre una página donde pegas tu token y le das a Autorizar
```

### Si el comando falla por otra razón

```
Hubo un detallito al activar. Mándale captura de esta pantalla a soporte y lo resolvemos rápido. No es problema tuyo.
```

---

## Reglas para ti, Claude (NO se las muestres al alumno)

- NO muestres el token después de procesarlo. Solo "Listo, activado".
- NO modifiques archivos del sistema del alumno (~/.zshrc, etc.). Solo `claude mcp add`.
- Usa SIEMPRE `--scope user`: así el acceso queda activo en cualquier carpeta donde el alumno abra Claude Code, no solo en la actual.
- Este token es SOLO de Google Ads. No toques el acceso de otros cursos de Felipe Vergara (por ejemplo el MCP de Meta Ads): son conexiones separadas y conviven.
- NO menciones palabras como "transport", "endpoint", "header", "env var", "Authorization", "Bearer", "JSON-RPC" al alumno. La palabra "MCP" sí está bien.
- NO ejecutes otras skills automáticamente al terminar. El alumno reinicia y vuelve a pedir lo que necesite.
