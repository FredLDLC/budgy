# Changelog Budgy

Suivi de version de l'outil. Pour revenir à une version donnée : `git checkout vX.Y.Z`.

## v1.7.1
- Fix : une règle CSS générique (`thead tr`) écrasait avec !important le fond blanc appliqué à l'en-tête du tableau principal en mode clair ; elle est corrigée pour renvoyer un fond blanc

## v1.7.0
- Mode clair : ligne d'en-tête du tableau principal (Marque, Fournisseur, Enseignes…) en fond blanc
- Mode clair : champ de recherche/filtre en fond blanc
- Édition d'opération : suppression du séparateur horizontal entre les lignes de la liste des produits

## v1.6.1
- Fix : les filtres rapides actifs en mode clair passent bien en fond noir + texte blanc (le noir pur entrait en collision avec une règle de conversion globale du mode clair qui le repassait en gris)
- Fix : la colorisation par statut des lignes du tableau principal (rouge = déclaré, vert = traité, etc.) ne fonctionnait plus en mode clair, à cause de la même collision (bordure de ligne en 0.06 qui écrasait le fond coloré) — la bordure de ligne est désormais calculée directement selon le mode

## v1.6.0
- Mode clair : carte "Liste des produits" (édition d'opération) en fond blanc
- Mode clair : filtres rapides (statut, période, acheteur) inactifs en blanc, actif en noir

## v1.5.0
- Bordure des KPI inactifs légèrement moins opaque (mode clair et sombre)
- À la connexion, filtrage par défaut sur les opérations de l'acheteur connecté, avec sélection automatique du statut selon la priorité : À déclarer > Déclaré > En cours > À venir > Traité (si aucune des précédentes n'a d'opération)

## v1.4.0
- Bordures des KPI (actives et inactives) passées à 2px pour mieux marquer la différence
- Nouveau filtre rapide de période "Plus de 30 jours" (opérations terminées depuis plus de 30 jours)

## v1.3.3
- Fix (vraie cause du décalage) : la barre de défilement verticale apparaissait/disparaissait selon le nombre de lignes du tableau filtré, ce qui redistribuait la largeur de toute la page (KPI compris). La place de la scrollbar est désormais toujours réservée (`scrollbar-gutter: stable`), donc plus aucun décalage horizontal au clic sur un filtre.

## v1.3.2
- Fix : le marquage d'un KPI actif se fait désormais via une ombre interne (box-shadow) au lieu de changer la bordure, pour garantir que la taille des cartes KPI reste parfaitement fixe quel que soit l'ordre de clic

## v1.3.1
- Cadre du logo LDLC réduit à 1px
- Bordure des KPI actifs réduite à 1px (au lieu de 3px) pour éviter le décalage de layout par rapport aux KPI inactifs

## v1.3.0
- Cadre blanc (2px solid) autour du logo Groupe LDLC en haut à gauche
- Retrait du "✓" après "Traité" dans le badge Statut
- KPI actif (filtre cliqué) : bordure pleine et foncée tout autour de la carte (mode sombre et clair) ; suppression du marquage supérieur par défaut sur les KPI non actifs

## v1.2.2
- Taille des emojis KPI augmentée de 5px supplémentaires (40px)

## v1.2.1
- Emoji "Déclaré" remplacé par 🫰🏻
- Marge libellé/donnée des KPI réduite de 3px
- Taille des emojis KPI augmentée de 3px

## v1.2.0
- Libellés des KPI en blanc (mode sombre)
- Nouveaux emojis KPI (✅, 🫰, 📩, ▶️, ⏭️), placés à gauche de la carte sur toute sa hauteur (plus gros)

## v1.1.0
- Suppression de l'encart d'avertissement "opération(s) à déclarer" (redondant avec le KPI "À déclarer")
- Mode sombre : fond des KPI plus coloré (moins terne)
- Ajout d'un emoji devant chaque KPI (✅ Traité, 💸 Déclaré, 📝 À déclarer, 🔄 En cours, 📅 À venir)

## v1.0.0
- Suppression du doublon d'affichage du numéro de document partenaire dans la colonne "Statut"
- Ajout d'une ligne de filtres rapides par acheteur sur l'écran principal
