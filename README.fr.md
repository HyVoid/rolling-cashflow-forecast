[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)
# Prévenez les pénuries de trésorerie avant qu'elles n'atteignent la date d'échéance

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Focus](https://img.shields.io/badge/focus-Operations--Stage%20Business-orange)

**Conçu pour les entreprises de biens de consommation, de gros et de fabrication qui doivent suivre les mouvements de trésorerie engagés, les obligations de prépaiement et la liquidité glissante avant qu'une pénurie ne survienne.**

[Aperçu en direct](https://hyvoid.github.io/rolling-cashflow-forecast/) · [Acheter la version Excel complète](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

</div>

Suivez les engagements de trésorerie des commandes ouvertes, détectez les écarts de liquidité des semaines à l'avance et conservez une source de vérité unique et prospective sur la viabilité de trésorerie à court terme.

---

## Aperçu rapide

<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 03_53_03 PM" src="https://github.com/user-attachments/assets/d43699bc-4a15-470c-901e-7b372c953861" />

> Consultez l'aperçu interactif du classeur : [démo de flux de trésorerie sur 16 semaines](https://hyvoid.github.io/rolling-cashflow-forecast/)

---

## Pourquoi cela existe

La plupart des pénuries de trésorerie dans les entreprises en croissance ne sont pas causées par des opérations non rentables.

Elles surviennent généralement parce que les prépaiements clients, les encaissements jalonnés, les bons de commande engagés et les échéances de paiement échelonnées sont difficiles à consolider manuellement — et les enregistrements comptables standard sont structurellement aveugles à leur égard jusqu'à ce qu'une facture soit émise.

Le risque est simple :

```
Payment due date arrives
-> Manual bank balance check
-> Prior commitments missed
-> Shortfall discovered at the wire
```

Ce classeur est conçu pour changer le workflow :

```
New order or supplier PO considered
-> Commitment entered once
-> 16-week cash timeline updated automatically
-> Liquidity gap flagged before it becomes a crisis
```

Le problème commercial n'est pas seulement la gestion de trésorerie. C'est la visibilité opérationnelle. Les équipes financières et les opérateurs doivent savoir si l'entreprise peut couvrir sa prochaine obligation — avant d'accepter des conditions de paiement.

---

## Trois pièges de trésorerie qui surprennent les entreprises en croissance

### Piège 1 — Les relevés mensuels sont mal lus comme une image de liquidité

Les rapports AR/AP standard reflètent ce qui a été facturé. Ils ne reflètent pas ce qui a été engagé.

Une entreprise détenant 80 000 $ de dépôts clients confirmés et 60 000 $ de prépaiements fournisseurs contractuels dus le mois prochain ne montre ni l'un ni l'autre dans son compte de résultat jusqu'à ce que les marchandises circulent et que les factures soient émises. L'équipe financière voit aujourd'hui un solde bancaire sain. La pénurie à venir est invisible.

Les équipes financières qui gèrent la trésorerie à partir des relevés mensuels travaillent routinièrement à partir d'une image structurellement en retard de quatre à six semaines sur la réalité. Le modèle mental semble complet ; les données ne le sont pas.

### Piège 2 — Les prépaiements et les bons de commande sont suivis dans des systèmes séparés

Lorsque la même entreprise reçoit un acompte client de 30 % lundi et émet un prépaiement fournisseur de 40 % jeudi, les deux transactions affectent le même réservoir de trésorerie — mais elles vivent généralement dans des systèmes, des tableurs ou des équipes différents.

Les opérations qui maintiennent un suivi séparé des engagements commerciaux et des obligations d'approvisionnement — une division naturelle du workflow — ne parviennent pas systématiquement à voir la position de trésorerie nette. La réglementation ne reconnaît pas cette frontière opérationnelle. Le compte bancaire non plus.

### Piège 3 — Les écarts sont découverts à la date d'échéance du paiement

La vérification manuelle se produit généralement lorsqu'un paiement arrive à échéance ou lorsque quelqu'un consulte le compte bancaire. Au moment où un écart est identifié, la fenêtre d'action s'est refermée. Les réponses réactives — tirages de crédit d'urgence, renégociations avec les fournisseurs, salaires retardés — ont un coût réel et causent de réels dommages relationnels.

L'interception avant l'écart exige que le risque de liquidité soit visible des semaines avant l'échéance de l'obligation — ce qui exige que tous les engagements ouverts soient à jour et que tous les calculs de calendrier s'exécutent automatiquement au moment de la planification.

L'écart se cache généralement dans la relation entre :

- le solde de trésorerie d'ouverture
- le calendrier d'encaissement des dépôts et des prépaiements
- les dates d'encaissement des soldes clients
- les dates d'échéance des paiements fournisseurs
- les conditions de paiement contractuelles
- le volume des commandes et le taux de croissance

C'est pourquoi le rapprochement manuel fait souvent surface trop tard sur le problème — ou le manque entièrement.

---

## À qui cet outil est destiné

| Utilisateur | Cas d'usage pratique |
|---|---|
| Directeurs financiers | Identifier les écarts de liquidité à 6–16 semaines avant qu'ils ne deviennent des crises |
| Directeurs des opérations | Comprendre l'impact de trésorerie d'une nouvelle commande ou d'un bon de commande fournisseur avant de s'engager |
| Fondateurs et PDG | Maintenir une vue prospective unique de la viabilité de trésorerie à mesure que l'entreprise se développe |
| Équipes d'approvisionnement | Évaluer les exigences de prépaiement par rapport à la liquidité réellement disponible |
| Comptables externes | Fournir des conseils de trésorerie à court terme sans construire un modèle à partir de zéro |

Convient mieux aux entreprises fonctionnant avec des structures mixtes de prépaiement client et de prépaiement fournisseur, où les logiciels de trésorerie sont trop coûteux mais où les approches manuelles ne passent plus à l'échelle.

---

## Ce que fait le classeur

### Journalisation des engagements ouverts
Un point d'entrée de données unique pour tous les AR, AP, commandes clients ouvertes et bons de commande ouverts. Les équipes saisissent une seule fois les informations d'engagement et de calendrier ; les calculs du calendrier de trésorerie s'exécutent automatiquement en arrière-plan.

### Calendrier de trésorerie sur 16 semaines
Cartographie automatique de chaque engagement ouvert vers une semaine et une direction de trésorerie spécifiques. La fenêtre glissante se met à jour chaque semaine à mesure que de nouvelles entrées sont ajoutées et que les semaines antérieures se clôturent.

### Statut de liquidité pré-décision
Le solde de trésorerie projeté de chaque semaine est visible avant d'accepter une nouvelle commande ou de convenir d'une nouvelle condition fournisseur. Aucun recoupement manuel. Aucune découverte le jour du paiement.

### Logique de déduplication
Les bons de commande déjà convertis en factures sont automatiquement identifiés et exclus — garantissant que chaque mouvement de trésorerie attendu est compté exactement une fois et que la vue des engagements ouverts reste propre.

### Couche d'alertes par seuil
Un solde de trésorerie sûr minimal est configuré par l'entreprise. Le modèle met en évidence les semaines qui franchissent le seuil et les transactions spécifiques qui alimentent chaque écart — donnant aux équipes un diagnostic au niveau transactionnel, et pas seulement un drapeau rouge.

### Structure prête pour l'audit
Chaque entrée est structurée et traçable dès le premier jour. L'enregistrement complet des engagements sur 16 semaines peut être filtré par direction, contrepartie ou semaine et revu sans post-traitement.

---

## Exemple de scénario

**Profil de l'entreprise :** Importateur de biens de consommation. Conditions mixtes de prépaiement client et d'exigences de prépaiement fournisseur. Fonction financière unique.

**Le problème :** Chaque semaine, le directeur financier recoupe manuellement les commandes clients ouvertes, les dépôts clients en attente, les factures fournisseurs en instance et les dates d'arrivée des marchandises prévues pour estimer la trésorerie disponible. Les engagements clients sont suivis dans le CRM. Les engagements fournisseurs sont suivis dans la feuille d'approvisionnement. Réconcilier les deux en une position de trésorerie nette prend deux heures et produit une vue déjà périmée d'une semaine.

Sur un trimestre d'exploitation, deux écarts de liquidité ont été identifiés — tous deux dans les 48 heures suivant la date d'échéance du paiement.

| | Avant | Après |
|---|---|---|
| Structure des engagements | Deux feuilles séparées, une par équipe | Un classeur unifié unique |
| Temps de vérification hebdomadaire de la trésorerie | ~2 heures sur toutes les positions ouvertes | Moins de 5 minutes par semaine |
| Consolidation des prépaiements | Recoupement manuel | Automatique sur AR, AP, commandes clients, BDC |
| Découverte des écarts | À la date d'échéance du paiement ; réponse réactive | À 6–8 semaines ; réponse planifiée |

**Le point d'inflexion spécifique que cet outil révèle :**

Une commande client de 100 000 $ comporte un solde de 70 % dû avant expédition, estimé en semaine 6. Le bon de commande fournisseur associé comporte un solde de 60 % dû à l'arrivée des marchandises, estimé en semaine 5. Solde de trésorerie d'ouverture : 10 000 $.

Position nette semaine 5 : 10 000 $ − 30 000 $ = **−20 000 $.** Un écart existe.
Position nette semaine 6 : −20 000 $ + 70 000 $ = **50 000 $.** Résolu.

Une vue mensuelle montre le mois net-positif. La fenêtre hebdomadaire montre une véritable pénurie de 20 000 $ en semaine 5 qui exige une action avant qu'elle n'arrive — pas après.

---

## Pourquoi la prévision de trésorerie à court terme fonctionne ainsi

La prévision de flux de trésorerie glissante — méthode directe, horizon prospectif court — est une discipline de trésorerie standard maintenue par la plupart des grandes entreprises comme fonction opérationnelle centrale. Dans les entreprises plus grandes, elle est gérée par des fonctions de trésorerie dédiées utilisant des logiciels spécialisés.

La méthode directe fonctionne en cartographiant les mouvements de trésorerie réels attendus — et non les écritures comptables — sur des dates spécifiques. Chaque entrée et sortie engagée est traduite en une semaine, une direction et un montant. Le solde courant à tout moment reflète ce que l'entreprise s'attend réellement à détenir, et non ce que ses enregistrements comptables montrent.

Cette approche est structurellement distincte de :

- **L'estimation de trésorerie basée sur le compte de résultat** — confond rentabilité et liquidité ; une entreprise peut être rentable et illiquide simultanément
- **La gestion du solde bancaire** — ne reflète que ce qui a déjà bougé ; les sorties futures engagées sont invisibles
- **Le reporting AR/AP mensuel** — exclut entièrement les engagements pré-facture ; structurellement aveugle à la couche opérationnelle

La raison pour laquelle la plupart des entreprises en croissance n'ont pas cette vue n'est pas la complexité. C'est l'absence d'un mécanisme structuré pour consolider les engagements opérationnels — qui vivent répartis entre les ventes, l'approvisionnement et la finance — en un calendrier de trésorerie unique.

Contexte de référence utile :
- [AICPA : Prévision de flux de trésorerie par la méthode directe](https://www.aicpa.org)
- [AFP : Fondamentaux de la gestion de trésorerie](https://www.afponline.org)

---

## Comment fonctionne la fenêtre de 16 semaines

La fenêtre de 16 semaines glisse vers l'avant chaque semaine, et non chaque mois. Chaque nouvelle entrée est cartographiée vers une semaine future spécifique sur la base des dates opérationnelles estimées et des conditions de paiement contractuelles.

| Entrée opérationnelle | Événement de trésorerie dérivé |
|---|---|
| Date d'expédition estimée + condition « paiement avant expédition » | Encaissement client la semaine précédant l'expédition estimée |
| Date d'arrivée des marchandises estimée + condition « paiement à la livraison » | Sortie fournisseur la semaine d'arrivée estimée |
| Date de facture + condition « Net 30 » | Encaissement client environ 4 semaines plus tard |

**Le piège en chiffres :**

Une entreprise gérant 10 commandes ouvertes simultanément — chacune avec sa propre structure d'acompte, son calendrier de paiement du solde et son échéancier de prépaiement fournisseur — porte plus de 30 événements de trésorerie en interaction à tout moment. Chaque événement dépend d'une estimation opérationnelle à jour pour rester exact. La consolidation manuelle introduit une erreur à chaque étape.

Le modèle mental de remise à zéro mensuelle approuve des positions que la fenêtre hebdomadaire glissante n'approuve pas. Le calcul est structurel, et non subjectif. L'automatisation élimine entièrement cette classe d'erreurs.

**Pourquoi la fiabilité de la prévision se dégrade à l'horizon externe :** L'horizon proche des semaines 1–8 est peuplé d'engagements déjà en mouvement — des dates d'expédition et des conditions de paiement confirmées ou presque. Les semaines 9–16 dépendent d'estimations opérationnelles qui peuvent évoluer sensiblement à mesure que les commandes sont passées ou retardées. Le modèle est plus fiable dans l'horizon proche de 6–8 semaines. La fenêtre externe est utile directionnellement pour la planification ; ce n'est pas une garantie.

---

## Logique du classeur

Le classeur est organisé autour d'un workflow pratique de planification de trésorerie :

1. Saisissez tous les AR, AP, commandes clients et bons de commande ouverts avec les dates estimées et les conditions de paiement.
2. Appliquez la déduplication pour identifier et exclure les bons de commande déjà convertis en factures.
3. Cartographiez chaque engagement ouvert vers sa semaine et sa direction de trésorerie attendues.
4. Calculez le solde glissant sur 16 semaines à partir de la position de trésorerie d'ouverture.
5. Comparez le solde projeté de chaque semaine au seuil sûr minimal.
6. Signalez les semaines d'écart et identifiez les transactions spécifiques qui alimentent chaque écart.
7. Conservez le registre des engagements pour la revue hebdomadaire glissante et la communication d'équipe.

Le classeur est destiné à être un outil d'aide à la décision et de planification. Il ne remplace pas les logiciels comptables, les registres financiers auditables ni les conseils professionnels pour les décisions de financement complexes.

---

## Achat

Utilisez le classeur Excel complet ici :

[Acheter le classeur Excel complet →](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

---

## Limites

- **Dépendance aux entrées** — la précision de la prévision est limitée par la qualité des données saisies ; des estimations d'expédition périmées ou des engagements manquants produisent un faux sentiment de visibilité sans avertissement
- **Actualisation manuelle requise** — le modèle ne se met pas à jour automatiquement ; sans maintenance hebdomadaire régulière, la fenêtre glissante se dégrade et les écarts redeviennent invisibles
- **Pas un système d'enregistrement** — c'est une couche d'aide à la décision ; elle ne remplace pas les logiciels comptables, un ERP ni les registres financiers auditables
- **Déterministe, non probabiliste** — chaque événement de trésorerie est modélisé comme une date fixe et un montant fixe ; les risques de retard de paiement, les mouvements de change et les scénarios d'annulation de commande nécessitent une surcouche manuelle
- **Fiabilité de l'horizon externe** — les semaines 10–16 dépendent d'estimations opérationnelles qui peuvent évoluer sensiblement ; le modèle est plus fiable dans l'horizon proche de 6–8 semaines
- **Multi-devises non modélisé** — les entreprises avec une exposition significative au change devront appliquer des hypothèses de taux de change comme surcouche manuelle
- **Contexte d'échelle** — conçu pour les entreprises gérant 5–50 positions ouvertes simultanées ; au-delà de cette plage, le modèle de saisie manuelle nécessite une adaptation structurelle

---

## À propos de ce projet

Ce classeur s'inscrit dans un effort plus large de traduction des exigences opérationnelles et financières complexes en outils légers que les petites et moyennes organisations peuvent réellement utiliser.

Pas d'ERP. Pas d'abonnement à un logiciel de trésorerie. Pas de projet de développement sur mesure.

Juste une logique métier claire, des données structurées et une aide à la décision reproductible — livrées dans des logiciels que votre équipe possède déjà.

Si votre exploitation implique la gestion de trésorerie, les cycles d'approvisionnement ou les structures de facturation client qui vivent actuellement dans la tête de quelqu'un ou dans un tableur déconnecté, [découvrez ce qui est disponible →](https://www.theseusworkshop.com)

---

## Licence

Distribué sous [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
