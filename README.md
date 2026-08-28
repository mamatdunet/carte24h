# Carte 24h du Mans

Carte interactive historique du Circuit de la Sarthe (24 Heures du Mans) :
71 événements, frise chronologique, vue 3D et vue satellite IGN.

Site : https://carte24h.vercel.app/

## Contenu

- `index.html` — l'application complète (page unique, sans build).
- `og-image.svg` — image Open Graph.

## Fonds de carte

| Vue | Source | Clé d'API |
|---|---|---|
| Fond sombre (défaut) | Tuiles [OpenStreetMap](https://www.openstreetmap.org/copyright) (ODbL), assombries par un filtre CSS (`.osm-dark`) | aucune |
| Vue satellite | IGN / Géoplateforme — `ORTHOIMAGERY.ORTHOPHOTOS` (WMTS) | aucune |

Le fond précédent (`basemaps.cartocdn.com/dark_nolabels`) n'est plus utilisable :
CARTO renvoie désormais des tuiles tamponnées « API KEY REQUIRED ».
L'attribution OpenStreetMap doit rester visible (contrôle d'attribution Leaflet).
