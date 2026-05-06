# NG Group - Monitor de licitaciones

Dashboard web para consultar oportunidades de licitaciones vinculadas a comunicaciones, conectividad, redes, internet, WiFi, servidores, cableado estructurado y servicios tecnológicos.

## Versión web

El sitio estático se publica desde:

- `index.html`
- `assets/ng-logo.png`

Al subir este repositorio a GitHub, puede compartirse con GitHub Pages desde la rama `main` y carpeta raíz.

## Datos actuales

El monitor combina oportunidades de Argentina y España. La tabla permite filtrar por:

- Relevancia
- Fecha de cierre/oferta
- Rubro
- País
- Región
- Búsqueda libre

## Actualización local

Para actualizar datos y regenerar el dashboard:

```powershell
& 'C:\Program Files\QGIS 3.44.9\apps\Python312\python.exe' scrape.py
& 'C:\Program Files\QGIS 3.44.9\apps\Python312\python.exe' render_dashboard.py
Copy-Item -LiteralPath dashboard.html -Destination index.html -Force
```

## Fuentes principales

- Argentina: COMPR.AR, CONTRAT.AR, BAC, Boletín Oficial y portales provinciales/municipales configurados.
- España: PLACSP y plataformas agregadas oficiales.
