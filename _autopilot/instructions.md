# Consignes de l'autopilote MonCalcul

Tu es lancé automatiquement chaque jour pour faire grossir le site MonCalcul, tout seul.
Dossier de travail : `/Users/antoninlopinto/BrainA/moncalcul`

## Ta mission (une seule page par exécution)

1. **Mets à jour le dépôt** : `git pull --rebase` (au cas où).
2. **Ouvre `_autopilot/queue.md`** et prends le PREMIER calculateur non coché (`- [ ]`).
3. **Si un item demande de vérifier un barème/taux de l'année en cours** (kilométrique, IRL, auto-entrepreneur…), fais une recherche web pour avoir le chiffre officiel à jour AVANT de coder. La justesse des calculs est non négociable.
4. **Construis la page** en copiant fidèlement la structure d'une page existante (`capacite-emprunt.html` est le modèle de référence) :
   - même en-tête `<nav>`, même `<footer>`, lien `styles.css`
   - balises `<title>` et `<meta name="description">` optimisées avec le mot-clé principal
   - le calculateur interactif (HTML + petit script JS dans la page, calcul côté navigateur)
   - une section "Comment ça se calcule" qui explique la formule (valeur SEO réelle)
   - une section FAQ avec 2-3 questions fréquentes
   - une `note` d'avertissement "estimation à valeur indicative"
5. **Ajoute une carte** vers la nouvelle page dans la grille `.grid` de `index.html` (icône emoji + titre + phrase courte).
6. **Coche l'item** dans `_autopilot/queue.md` (`- [x]`).
7. **Sauvegarde et publie** :
   ```
   git add -A
   git commit -m "Autopilote : ajout du calculateur [nom]"
   git push
   ```

## Règles de sécurité (à respecter absolument)

- **Que de l'AJOUT.** Ne supprime, ne casse, ne réécris jamais une page existante.
- **Une seule page par jour.** Pas de batch, on construit progressivement.
- Si la file d'attente est vide, n'invente pas n'importe quoi : ajoute 3-4 nouvelles idées de calculateurs pertinents en bas de `queue.md` (demande réelle + faible concurrence), puis arrête-toi sans rien construire ce jour-là.
- Si `git push` échoue, fais `git pull --rebase` puis réessaie (max 3 fois). Ne force jamais le push.
- Reste silencieux et autonome : tu n'as pas besoin de validation humaine pour une simple page additive.

## Rappel monétisation (pour plus tard, ne pas faire maintenant)

Quand le site aura du trafic, on branchera : AdSense (pub) + liens d'affiliation crédit/assurance sur les pages financières (emprunt, frais de notaire, mensualité). Pour l'instant, on construit juste l'audience.
