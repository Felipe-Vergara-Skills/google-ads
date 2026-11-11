# Felipe Vergara · MCP de Google Ads

Acceso al MCP de Felipe Vergara con las skills del curso de Google Ads.

---

## Cómo instalarlo (3 pasos)

### Paso 1. Copiar tu token de acceso

Entra a **https://ifs0gqumun7cmigvfniyxqec.apps.felipevergara.co** con el email con el que compraste el curso.

En la sección **Tu token del MCP de Google Ads** está tu token: empieza con `fvg_…`. Cópialo con el botón **Copiar**.

> Si también tienes el curso de Meta Ads: ese token (`fv_…`) es otro. Cada curso tiene el suyo y los dos pueden estar conectados a la vez.

### Paso 2. Instalar el plugin

Abre **Claude Code** y corre:

```
/plugin marketplace add Felipe-Vergara-Skills/google-ads
```

```
/plugin install felipe-vergara-google@felipe-vergara-google
```

### Paso 3. Conectar el MCP con tu token

#### Si usas Claude Code

Dile a Claude en el chat:

> *configura mi token de Google Ads*

Te pide el token, lo comprueba, lo registra y te avisa cuándo reiniciar Claude Code.

#### Si usas la app de Claude o Cowork

1. Ve a **Conectores → Agregar conector personalizado**
2. URL del servidor:
   ```
   https://mcp-google.felipevergara.co/mcp
   ```
3. Click en **Conectar**
4. Se abre el navegador con un formulario: **pega tu token** y dale a **Autorizar**

---

## Cómo usar las skills

Una vez conectado, las 19 skills se disparan hablando normal. No tienes que memorizar nombres.

| Skill | Qué hace |
|---|---|
| `7-maletas-google` | Investiga clientes y mercado de un negocio con las 7 Maletas (público, problema, solución, diferenciales, testimonios, objeciones, garantía) para G... |
| `analizador-ads-estaticos-google` | Deconstruye un anuncio estático (imagen) en sus componentes de marketing, diseño y copywriting y explica por qué funciona, con un reporte Markdown ... |
| `calculadora-de-presupuestos-google` | Calcula cuánto invertir al mes en Google Ads y el número mágico del negocio: ROAS objetivo, costo por compra objetivo y CPC máximo en tienda online... |
| `calendario-promocional-google` | Arma el calendario promocional del año para Google Ads: investiga qué fechas mueven ventas en los países donde el negocio vende y en su nicho (come... |
| `columnas-google-ads` | Entrega la lista exacta y en orden de las columnas a configurar en Google Ads según el modelo de negocio (tienda online, servicios / leads o negoci... |
| `constructor-de-landing-google` | Construye la primera versión de una landing page para Google Ads y la entrega como archivo HTML listo para alojar, una por grupo de anuncios, con e... |
| `crear-campana-google` | Crea una campaña de Google Ads completa desde cero en una sola corrida: encadena marca, investigación de mercado, presupuesto, estructura por capas... |
| `diversificacion-creativa-google` | Genera una matriz de 30 ganchos para anuncios de Google Ads cruzando los 3 deseos de Reiss de la marca, 2 perfiles de cliente y los 5 niveles de co... |
| `escanear-marca-google` | Escanea la web de una marca para extraer su ADN antes de hacer Google Ads: identidad visual (colores, tipografía, logo, estilo de imágenes), tono y... |
| `espiar-competidores-google` | Espía a los competidores de un negocio en Google: sus anuncios en el Centro de Transparencia de Anuncios de Google (texto, imagen y video, dónde an... |
| `estrategia-por-capas-google` | Genera la estrategia de campañas de Google Ads por capas: 1 Búsqueda de marca, 2 Shopping o Búsqueda no-marca, 3 Máximo rendimiento, 4 Remarketing,... |
| `feed-de-productos-google` | Optimiza el feed de productos de Google Merchant Center, que es el anuncio real en Shopping y Máximo rendimiento: reescribe los títulos con la fórm... |
| `generador-de-nombres-google` | Genera nombres estandarizados para campañas, grupos de anuncios, grupos de recursos (Máximo rendimiento) y anuncios (Generación de demanda) de Goog... |
| `investigador-keywords-google` | Investiga y construye las palabras clave de una campaña de Google Ads con respaldo de fuente. |
| `metodologia-3qs-google` | Analiza campañas de Google Ads con las 3 Q's (¿Qué pasó? |
| `monitor-conversiones-google` | Monitorea la salud de las conversiones de Google Ads: revisa cada acción de conversión (estado, principal o secundaria, recuento, valor, ventana y ... |
| `niveles-de-consciencia-google` | Diagnostica en qué niveles de conciencia está el mercado (inconsciente, problema, solución, producto, decisión) con evidencia real y escribe los an... |
| `optimizacion-destino-google` | Audita a dónde llegan las personas después del clic en Google Ads (la tienda online, la landing de servicios o la ficha de Google Business de un ne... |
| `simulador-resultados-google` | Simulador de campañas de Google Ads: predice clics, impresiones, ventas, leads, llamadas, conversiones, vistas de YouTube, costo por resultado y RO... |

---

## Cómo actualizar (para recibir las skills nuevas)

Dile a Claude: *"actualiza el plugin de Google Ads"* y sigue lo que te indique.

O hazlo a mano:

1. Actualiza Claude Code a la versión **2.1.296 o superior** (`claude update` en la terminal).
2. Dentro de Claude Code:
   ```
   /plugin marketplace update felipe-vergara-google
   ```
   ```
   /plugin update felipe-vergara-google@felipe-vergara-google
   ```
3. Reinicia Claude Code.

**Para no hacerlo cada vez:** escribe `/plugin` → pestaña **Marketplaces** → elige `felipe-vergara-google` → **Enable auto-update**.

Si usas la app de Claude o Cowork con el conector, no tienes que actualizar nada: las skills nuevas te aparecen solas en un chat nuevo.

---

## Problemas comunes

**"Couldn't reach the MCP server" o "Missing license token"**
Tu token no está registrado en este cliente. Repite el Paso 3.

**"Este token ya no está activo" o "Tu acceso expiró"**
Tu token fue renovado o tu acceso venció. Entra a https://ifs0gqumun7cmigvfniyxqec.apps.felipevergara.co, copia tu token actual y vuelve a conectar: en Claude Code di *"configura mi token de Google Ads"*; en la app de Claude o Cowork edita el conector y vuelve a autorizar.

**"Token no encontrado" al pegarlo**
Revisa que sea el de Google Ads (empieza con `fvg_`) y no el de otro curso.

**Las skills no se disparan solas**
Cierra Claude Code por completo (Cmd + Q en Mac; en Windows cierra todas sus ventanas) y vuelve a abrirlo.

**No me deja actualizar el plugin**
Actualiza primero Claude Code (`claude update`, necesitas la 2.1.296 o superior) y repite los pasos.

---

## Seguridad

- El servidor solo entrega las skills si tu token es válido.
- Tu token va vinculado al email con el que compraste: no lo compartas.
- Este plugin no contiene las skills: solo sabe pedirlas al servidor con tu licencia.
