# Backlog heavy-shop

## Contexte du projet

Le projet represente une boutique catalogue avec listes, recherche, detail produit, panier et checkout simplifie.

## Format attendu

Completer au minimum 3 user stories.
Remplacer chaque champ entre crochets par votre contenu.

## User story 1 : reduire le nombre de requêtes http

- Contexte: En tant que nouvel utilisateur, je veux consulter une fiche produit, afin de prendre une décision pour un achat.
- Objectif: Diminuer de 30% le temps de chargement de la page produit en réduisant le nombre de requêtes HTTP émises au chargement.
- Bonne pratique d eco-conception ciblee: Limiter le nombre de requêtes HTTP (GreenIT 0047)
- KPI associe: Nombre de requêtes HTTP au chargement initial (mesuré via DevTools / WebPageTest) et passer de ~80 requêtes à < 55 requêtes sur la page produit
- Repo ou ecran concerne: Page /product/:id (détail produit)
- Critere de reussite: Le nombre de requêtes HTTP sur la page produit est ≤ 55 (mesuré via Lighthouse en mode mobile)
- Niveau de priorite: haute

## User story 2 : Optimiser les images produits (compression + WebP)

- Contexte: En tant qu’utilisatrice qui navigue sur mobile avec une connexion 4G, je veux parcourir la liste des produits du catalogue, afin de trouver rapidement ce que je cherche sans attendre.
- Objectif: Réduire le poids total des images de la page catalogue de 60%, en passant au format WebP avec compression adaptative, pour un chargement perçu immédiat même sur réseau mobile.
- Bonne pratique d eco-conception ciblee: Compresser les images (BP1) + Utiliser des formats d’images adaptés — WebP (BP2)
- KPI associe: Poids total des images sur la page /catalogue (via DevTools > Network > Img)
- Repo ou ecran concerne: Page /catalogue (liste produits) et /product/:id (galerie images)
- Critere de reussite: 100% des images produits sont servies au format WebP avec fallback JPEG. Le poids moyen d’une image produit est ≤ 35 Ko (vs ~90 Ko avant). Aucune image n’est étirée ou pixelisée sur les écrans testés (mobile, tablette, desktop)
- Niveau de priorite: haute


## User story 3 : Minifier les fichiers CSS et JavaScript

- Contexte: En tant qu’utilisateur régulier de la boutique, je veux que chaque page se charge rapidement, quelle que soit la section visitée (catalogue, panier, checkout), afin de ne pas être freiné dans mon parcours d’achat.
- Objectif: Réduire le poids total des fichiers CSS et JS chargés sur l’ensemble du site de 40%, en supprimant le code mort et en minifiant les bundles, pour diminuer la consommation réseau à chaque visite.
- Bonne pratique d eco-conception ciblee: Optimiser le code — minification CSS/JS (BP7) + Limiter les scripts et plugins inutiles (BP6)
- KPI associe: Poids total CSS + JS au chargement initial (mesuré via DevTools > Coverage)
- Repo ou ecran concerne: Toutes les pages du shop : /catalogue, /product/:id, /cart, /checkout
- Critere de reussite: Le score Lighthouse “Performance” sur mobile est ≥ 80 (vs score baseline mesuré avant)
- Niveau de priorite: haute


## Notes

- Vous pouvez ajouter d autres user stories si necessaire.
- Le niveau de detail attendu doit permettre une priorisation exploitable.
