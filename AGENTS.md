# Site de Hazak Lausanne : guide pour l'IA

Ce dépôt contient tout le site de Hazak (hazak.ch). Quand quelqu'un de Hazak te demande une modification, suis ces règles.

## Structure
- `index.html` : la page entière (HTML + CSS dans la balise `<style>`). Pas de framework, pas de build.
- `img/` : images. Les affiches d'événements sont en JPEG, environ 900 px de large ; les logos sont en PNG.
- Chaque push sur `main` met le site en ligne automatiquement (GitHub Pages) en une à deux minutes.

## Sections de index.html (ancres)
- `#about` : Qui sommes-nous / Mission Statement
- `#students` : services aux étudiants (cartes `.srv .card`) et To-Go (`.togo .card`)
- `#torah` : cours de Torah
- `#events` : affiches d'événements (`.flyers figure`, la plus récente en premier)
- `#rabbin` : le mot du Rabbin et les articles (`.post`)
- `#donate` : coordonnées de dons
- `#contact` : contact et réseaux sociaux

## Demandes fréquentes
- **Ajouter un événement** : enregistrer l'affiche dans `img/` (nom en minuscules avec tirets, ex. `hanoucca-2026.jpg`, JPEG d'environ 900 px de large), puis ajouter en tête de `.flyers` :
  `<figure><img src="img/hanoucca-2026.jpg" alt="Affiche : …" loading="lazy"><figcaption>Titre · lieu</figcaption></figure>`
- **Retirer un événement passé** : supprimer sa `<figure>` (et l'image si plus utilisée).
- **Changer un texte, un horaire, un numéro** : modifier le texte directement dans `index.html`. Le téléphone et l'e-mail apparaissent à plusieurs endroits (services, dons, contact, pied de page) : les changer partout.
- **Ajouter un article** : ajouter un bloc `.post` en tête de la colonne `.posts`.

## Règles
- Ne rien inventer : n'écrire que ce que la personne a demandé ou fourni.
- Garder le style existant (couleurs dans `:root`, polices Frank Ruhl Libre et Figtree) et vérifier que la page reste lisible sur téléphone.
- Commits courts en français, qui décrivent le changement (« Ajoute l'affiche de Hanoucca 2026 »).
- En cas de doute (suppression d'une section, changement de domaine), demander confirmation avant de pousser.
