# File d'attente des calculateurs à construire

L'autopilote prend le PREMIER item non coché, construit sa page, le coche, puis recommence le lendemain.
Chaque item donne le nom de fichier, le titre, et la formule EXACTE à coder (la justesse est non négociable).

---

- [x] **tva.html** — Calcul de la TVA (HT ↔ TTC)
  - Inputs : montant, sens (HT→TTC ou TTC→HT), taux (20 % / 10 % / 5,5 % / 2,1 %)
  - Formule : TTC = HT × (1 + taux) ; HT = TTC / (1 + taux) ; TVA = TTC − HT
  - Demande : très forte ("calcul tva", "ht en ttc")

- [ ] **frais-de-notaire.html** — Calcul des frais de notaire
  - Inputs : prix du bien, type (ancien / neuf)
  - Formule : ancien ≈ 7,5 % du prix ; neuf ≈ 2,5 % du prix (estimation). Préciser "frais de notaire" = surtout droits de mutation.
  - Monétisation : très bon (lead crédit immo / assurance emprunteur)

- [ ] **indemnite-kilometrique.html** — Barème kilométrique (frais réels)
  - Inputs : puissance fiscale (3 CV et moins, 4, 5, 6, 7 CV et plus), km parcourus/an
  - Formule : barème fiscal voiture. ⚠️ L'autopilote DOIT vérifier le barème de l'année en cours avant de coder (recherche web "barème kilométrique [année] impots.gouv").
  - Demande : forte chaque printemps (déclaration impôts)

- [ ] **conges-payes.html** — Calcul des congés payés
  - Inputs : mois travaillés
  - Formule : 2,5 jours ouvrables acquis par mois, plafond 30 jours/an (5 semaines)

- [ ] **taux-horaire.html** — Salaire mensuel → taux horaire
  - Inputs : salaire mensuel, heures/semaine (défaut 35)
  - Formule : mensuel base 35h = 151,67 h/mois ; taux horaire = mensuel / (heures_hebdo × 52 / 12)

- [ ] **augmentation-loyer-irl.html** — Révision de loyer (IRL)
  - Inputs : loyer actuel, ancien IRL, nouvel IRL
  - Formule : nouveau loyer = loyer × (nouvel IRL / ancien IRL). ⚠️ Vérifier le dernier IRL publié (INSEE) avant de coder.

- [ ] **plus-value-immobiliere.html** — Plus-value immobilière (résidence secondaire)
  - Inputs : prix d'achat, prix de vente, durée de détention (années)
  - Formule : plus-value brute = vente − achat ; abattement progressif par année de détention (exonération IR à 22 ans, prélèvements sociaux à 30 ans). Détailler le barème d'abattement.

- [ ] **prime-precarite-cdd.html** — Prime de précarité (fin de CDD)
  - Inputs : total des salaires bruts perçus sur le CDD
  - Formule : indemnité de fin de contrat = 10 % de la rémunération brute totale

- [ ] **mensualite-pret.html** — Mensualité d'un prêt
  - Inputs : capital, taux annuel, durée (années)
  - Formule : M = C × t / (1 − (1 + t)^−n), t = taux mensuel, n = nb de mois. Afficher aussi coût total des intérêts.

- [ ] **auto-entrepreneur-net.html** — Chiffre d'affaires → net (auto-entrepreneur)
  - Inputs : CA, activité (vente ≈ 12,3 %, prestation BIC ≈ 21,2 %, libéral BNC ≈ 21,1 %/24,6 %)
  - Formule : net ≈ CA × (1 − taux de cotisations selon activité). ⚠️ Vérifier les taux de l'année en cours.
