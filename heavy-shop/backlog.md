# Backlog heavy-shop

## Contexte du projet

Le projet represente une boutique catalogue avec listes, recherche, detail produit, panier et checkout simplifie.

## Format attendu

Completer au minimum 3 user stories.
Remplacer chaque champ entre crochets par votre contenu.

## User story 1: Réduire le nombre de requêtes HTTP

- Contexte: En tant que nouvel utilisateur, je veux consulter une fiche produit, afin de prendre une décision pour un achat.
- Objectif: Diminuer de 30% le temps de chargement de la page produit en réduisant le nombre de requêtes HTTP émises au chargement.
- Bonne pratique d eco-conception ciblee: RWEB_0047 — "Limiter le nombre de requêtes HTTP" 
- KPI associe: Nombre de requêtes HTTP au chargement initial (mesuré via DevTools / WebPageTest). Passer de environ 80 requêtes à 55 requêtes.
- Repo ou ecran concerne: [Page `/product/:id` (détail produit)
- Critere de reussite: Le nombre de requêtes HTTP sur la page produit est ≤ 55 (mesuré via Lighthouse en mode mobile)
- Niveau de priorite: haute

## User story 2 : Optimiser les images produits (compression + WebP)

- Contexte: En tant qu'utilisatrice qui navigue sur mobile avec une connexion 4G, je veux parcourir la liste des produits du catalogue, afin de trouver rapidement ce que je cherche sans attendre.
- Objectif: Réduire le poids total des images de la page catalogue de 60%, en passant au format WebP avec compression adaptative, pour un chargement perçu immédiat même sur réseau mobile.
- Bonne pratique d eco-conception ciblee: RWEB_0082 "Optimiser les images bitmap"
- KPI associe: Poids total des images sur la page `/catalogue` (via DevTools > Network > Img). Passer de environ 3,5 Mo à 1,4 Mo sur la page liste.
- Repo ou ecran concerne: Page `/catalogue` (liste produits) et `/product/:id` (galerie images). 
- Critere de reussite: 100% des images produits sont servies au format WebP avec fallback JPEG. Les images sont redimensionnées côté serveur selon le viewport (`srcset`). Aucune image n'est étirée ou pixelisée sur les écrans testés (mobile, tablette, desktop)
- Niveau de priorite: haute

## User story 3 : Minifier les fichiers CSS et JavaScript

- Contexte: En tant qu'utilisateur régulier de la boutique, je veux que chaque page se charge rapidement, quelle que soit la section visitée (catalogue, panier, checkout), afin de ne pas être freiné dans mon parcours d'achat.
- Objectif: Réduire le poids total des fichiers CSS et JS chargés sur l'ensemble du site de 40%, en supprimant le code mort et en minifiant les bundles, pour diminuer la consommation réseau à chaque visite.
- Bonne pratique d eco-conception ciblee: RWEB_0077 "Minifier les fichiers CSS, JS, HTML et SVG"
- KPI associe: Poids total CSS + JS au chargement initial (mesuré via DevTools > Coverage). passer de environ 1,2 Mo à 720 Ko de Js/CSS chargé.
- Repo ou ecran concerne: Toutes les pages du shop : `/catalogue`, `/product/:id`, `/cart`, `/checkout`
- Critere de reussite: Tous les fichiers CSS et JS sont minifiés et compressés (gzip ou Brotli) en production. Le Total Blocking Time est ≤ 200ms sur la page catalogue.

- Niveau de priorite: haute

## Notes

- Vous pouvez ajouter d autres user stories si necessaire.
- Le niveau de detail attendu doit permettre une priorisation exploitable.
