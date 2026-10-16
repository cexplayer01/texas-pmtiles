# texas-pmtiles

A self-hosted basemap of **Texas** as a single file — our fallback if the free
OpenStreetMap services ever go down or cut us off. No tile server, no database:
one static file, loaded directly by the browser.

- **File:** `texas.pmtiles` — 562 MB, zoom 0–14.
- **Live file:** https://texas-tiles.netlify.app/texas.pmtiles (Netlify, Range requests supported). A live viewer is at https://texas-tiles.netlify.app/. (GitHub Releases could not take the 562 MB upload with our API credential, so the file is hosted on Netlify instead; this repo is the documentation home.)
- **Data:** © OpenStreetMap contributors ([ODbL](https://opendatacommons.org/licenses/odbl/)),
  Geofabrik Texas extract, built with [Planetiler](https://github.com/onthegomap/planetiler) (OpenMapTiles schema)
- **Use:** serve or link the file over HTTPS with HTTP Range requests, then in
  MapLibre GL JS register the [PMTiles protocol](https://docs.protomaps.com/pmtiles/) and
  point a vector source at `pmtiles://<url-to-texas.pmtiles>`.

Current release is rebuilt weekly from the latest Texas extract.
