# Mapa de la RIEC (prototipo)

Web estática para GitHub Pages. No necesita base de datos.

## Archivos
- `index.html`: la web.
- `data/entidades.json`: comarcas, entidades y redes. Es lo único que se edita.

## Cómo publicar una entidad validada
Añade una línea en `entidades` con `"estado": "validada"` y su fecha. Mientras se revisa, usa `"estado": "revision"` (se cuenta, pero no se muestra el nombre).
Cuando una red municipal entregue el acta (Anexo 3), añádela en `redesMunicipales`. Igual con `redesComarcales`.
Actualiza `actualizado` con la fecha del día.

## Conectar el formulario al Chat CRM
En `index.html`, rellena `CRM_ENDPOINT` con la URL del formulario o webhook del Chat CRM y sustituye el mensaje de prototipo por el envío real (fetch con FormData).
Los documentos y datos personales solo deben llegar al CRM: nunca al repositorio.

## Probar en local
`python3 -m http.server` y abre http://localhost:8000 (abrir el archivo con doble clic no carga el JSON).
