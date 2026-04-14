# Backlog heavy-shop

## Contexte du projet

Le projet represente une boutique catalogue avec listes, recherche, detail produit, panier et checkout simplifie.

## Format attendu

Completer au minimum 3 user stories.
Remplacer chaque champ entre crochets par votre contenu.

## User story 1

- Contexte: En tant que nouvel utilisateur, je veux consulter une fiche produit, afin de prendre une décision pour un achat.
- Objectif: Diminuer de 30% le temps de chargement de la page produit en réduisant le nombre de requêtes HTTP émises au chargement.
- Bonne pratique d eco-conception ciblee: Limiter le nombre de requêtes HTTP (GreenIT 0047)
- KPI associe: Nombre de requêtes HTTP au chargement initial (mesuré via DevTools / WebPageTest). Passer de environ 80 requêtes à 55 requêtes.
- Repo ou ecran concerne: [Page `/product/:id` (détail produit)
- Critere de reussite: Le nombre de requêtes HTTP sur la page produit est ≤ 55 (mesuré via Lighthouse en mode mobile)
- Niveau de priorite: haute

## User story 2

- Contexte: En tant que [role], je veux [action], afin de [valeur attendue].
- Objectif: [objectif qualitatif ou chiffre]
- Bonne pratique d eco-conception ciblee: [bonne pratique]
- KPI associe: [indicateur de suivi]
- Repo ou ecran concerne: [page, composant, parcours ou endpoint]
- Critere de reussite: [resultat observable ou mesurable]
- Niveau de priorite: [haute, moyenne ou basse]

## User story 3

- Contexte: En tant que [role], je veux [action], afin de [valeur attendue].
- Objectif: [objectif qualitatif ou chiffre]
- Bonne pratique d eco-conception ciblee: [bonne pratique]
- KPI associe: [indicateur de suivi]
- Repo ou ecran concerne: [page, composant, parcours ou endpoint]
- Critere de reussite: [resultat observable ou mesurable]
- Niveau de priorite: [haute, moyenne ou basse]

## Notes

- Vous pouvez ajouter d autres user stories si necessaire.
- Le niveau de detail attendu doit permettre une priorisation exploitable.
