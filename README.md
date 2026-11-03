# grun-fichas-pages — Fichas propias de Grunwaldt

Ficha pública de cada propiedad, con la marca de Grunwaldt, para reemplazar el link de
amaira (`ficha.amaira.com.ar/nue/ficha.php?ficha=SOW205`) que manda el agente.

```
/SOW224  (o ?ref=SOW224)  →  GitHub Pages (index.html / 404.html)
                               ↓ fetch ?ref=
                          n8n "Grunwaldt - API Fichas" (PFD729GBXZAweplk)
                               ↓
                          Supabase grun.grun_ofrecibles (+ fotos de grun_propiedades)
```

- **Solo datos publicados.** La API lee de `grun_ofrecibles` (activo, publicado, no
  pausado) y nunca toca `nota_interna`. Si la propiedad no está, la página dice que ya no
  está publicada y ofrece escribir por WhatsApp.
- **Rutas.** `404.html` es una copia exacta de `index.html`: así GitHub Pages sirve la
  ficha para cualquier ruta (`/SOW224`). Si se edita uno, copiar al otro.
- **Fotos.** Se muestran directo del CDN de Xintel (`cdn-images.xintelweb.com`), que no
  bloquea el hotlink (verificado el 26/10/2026).
- **CORS.** El webhook acepta `https://fichas.appgrun.giwa-ia.com` y
  `https://sechavarria-star.github.io` (este último ya redirige al dominio; se puede sacar).
- **Botón WhatsApp.** Abre la línea del asistente (`5493795768454`) con un mensaje con la
  dirección y la REF. "Ver propiedades parecidas" abre la misma línea pidiendo opciones.
- **Diseño:** variante "B · Negro premium" de los mockups (26/10/2026), con el lenguaje de
  su Instagram: negro, rojo #D7193A (texto rojo sobre negro: #FF4D66 por contraste),
  Montserrat en negrita. Mockups: https://claude.ai/artifact/DM1XaBRHihErY1Nko3a8qC

## Dominio

`https://fichas.appgrun.giwa-ia.com/SOW224` (desde el 03/11/2026). DNS en Squarespace:
`CNAME fichas.appgrun → sechavarria-star.github.io`, archivo `CNAME` en el repo y HTTPS
forzado en GitHub Pages. El link viejo de `github.io` redirige solo.
