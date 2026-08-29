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
| Fond clair (défaut) | Tuiles [OpenStreetMap](https://www.openstreetmap.org/copyright) (ODbL), éclaircies et désaturées par un filtre CSS (`.osm-light`) | aucune |
| Vue satellite | IGN / Géoplateforme — `ORTHOIMAGERY.ORTHOPHOTOS` (WMTS) | aucune |

Le fond précédent (`basemaps.cartocdn.com/dark_nolabels`) n'est plus utilisable :
CARTO renvoie désormais des tuiles tamponnées « API KEY REQUIRED ».
L'attribution OpenStreetMap doit rester visible (contrôle d'attribution Leaflet).

## Habillage de la carte

Les objets posés sur la carte (tracé du circuit, libellés, panneau des événements
sans localisation) sont réglés pour le fond clair. La vue satellite bascule la
classe `sat-on` sur `#sat-map`, qui rétablit un halo sombre et ravive les
couleurs des libellés — un seul jeu de libellés sert les deux vues.
