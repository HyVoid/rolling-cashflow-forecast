[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)

# Modèle Excel de prévision glissante de trésorerie sur 16 semaines : planificateur de liquidité par la méthode directe, suivi des engagements de bons de commande & modèle de fonds de roulement

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Focus](https://img.shields.io/badge/focus-Working%20Capital%20%26%20Treasury-orange)

**Une feuille de calcul de prévision glissante de trésorerie sur 16 semaines par la méthode directe, construite dans Microsoft Excel pour les entreprises de négoce, d'import/export, de e-commerce avec stocks et de fabrication qui gèrent des bons de commande (PO) ouverts, des prépaiements fournisseurs, des acomptes clients et un fonds de roulement à court terme.**

[Lancer la démo interactive du simulateur de trésorerie glissante sur 16 semaines](https://hyvoid.github.io/rolling-cashflow-forecast/) ·

[Télécharger le classeur Excel complet de prévision glissante de trésorerie sur 16 semaines](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

</div>

**Le classeur de prévision glissante de trésorerie sur 16 semaines** est un **planificateur de liquidité à court terme Microsoft Excel** automatisé et un **suivi de trésorerie des engagements ouverts**. Allant au-delà des **modèles de flux de trésorerie sur 13 semaines** standards pour couvrir des délais complets d'approvisionnement et de production de 110 jours, il consolide les **comptes clients (AR)**, les **comptes fournisseurs (AP)**, les **commandes clients (SO) non facturées** et les **bons de commande (PO) engagés** dans une chronologie de trésorerie hebdomadaire unique — signalant les insuffisances de fonds de roulement et les franchissements du tampon de trésorerie minimal plusieurs semaines avant les échéances de paiement.

---

## Aperçu visuel : chronologie de trésorerie sur 16 semaines et tableau de bord d'alertes de seuil

<img width="1672" height="941" alt="16-Week Rolling Cash Flow Forecast Excel Template showing weekly cash inflows, supplier PO prepayments, net liquidity balance, and shortfall alerts" src="https://github.com/user-attachments/assets/d43699bc-4a15-470c-901e-7b372c953861" />

> Testez la cartographie hebdomadaire des engagements et les alertes de seuil de liquidité dans votre navigateur : [Démo interactive de prévision de trésorerie par la méthode directe sur 16 semaines](https://hyvoid.github.io/rolling-cashflow-forecast/)

---

## Pourquoi la comptabilité d'exercice ne prévient pas les pénuries de trésorerie à court terme

Les entreprises de négoce, de fabrication et de produits physiques rentables connaissent régulièrement des crises de liquidité aiguës pendant les phases de croissance. Ces pénuries de trésorerie surviennent parce que les **acomptes clients**, les **facturations à jalons de progression**, les **prépaiements fournisseurs contractuels** et les **conditions de paiement Net 30/60/90 échelonnées** interviennent plusieurs semaines avant qu'une facture comptable ne soit jamais comptabilisée au grand livre.

**Le workflow réactif solde bancaire & AR/AP (risque de défaut élevé) :**

```text
Supplier wire due date arrives
-> Finance checks current bank balance and billed AP aging
-> Unbilled PO prepayments and freight commitments overlooked
-> Working capital shortfall discovered 48 hours before wire deadline

```

**Le workflow proactif de prévision des engagements sur 16 semaines (contrôle pré-décision) :**

```text
New customer order or supplier Purchase Order (PO) proposed
-> Prepayment and balance milestones logged once in the commitment ledger
-> 16-week rolling cash flow timeline updates automatically
-> Liquidity gap and minimum buffer breach flagged 6–12 weeks in advance

```

Les directeurs financiers, les contrôleurs de gestion et les responsables des opérations ont besoin d'une visibilité de liquidité avant la décision. Avant de signer un bon de commande fournisseur ou d'accorder des conditions Net 60 à un acheteur en gros, les opérateurs doivent vérifier que le point bas de trésorerie hebdomadaire reste au-dessus de la réserve de trésorerie opérationnelle minimale de l'entreprise.

---

## La logique métier et la méthodologie : prévision des engagements par la méthode directe

Ce classeur résout le **problème de cécité du fonds de roulement pré-facture** en combinant la **prévision glissante de trésorerie par la méthode directe** avec le **dédoublonnage des engagements de la commande à la facture**.

### Le problème commercial : l'écart de calendrier entre l'exercice et la trésorerie dans les chaînes d'approvisionnement physiques

Les logiciels comptables standards (QuickBooks, Xero, NetSuite GL) ne reconnaissent les événements financiers que lorsqu'une **facture** ou une **facture fournisseur** est émise. Cependant, dans la fabrication, la distribution en gros et les opérations d'importation, la trésorerie est juridiquement engagée au **niveau de la commande** :

1. **Sorties de trésorerie d'approvisionnement :** une usine exige un acompte de 30% à l'émission du bon de commande (PO) et un solde de 70% au connaissement (B/L) ou à l'arrivée entrepôt — plusieurs semaines avant la comptabilisation d'une facture fournisseur AP formelle.
2. **Entrées de trésorerie des ventes :** un client B2B verse un acompte de 25% à la confirmation de la commande client (SO) et le solde restant de 75% soit avant expédition, soit en Net 30/60 après livraison.
3. **Pourquoi 16 semaines battent les modèles standard de 13 semaines :** une prévision de trésorerie d'entreprise standard sur 13 semaines (90 jours) s'interrompt juste avant qu'un cycle de production de 60 jours plus un transit maritime de 30 jours plus un encaissement client Net 30 ne soit soldé. Étendre la fenêtre glissante à **16 semaines (112 jours)** capture l'intégralité du cycle de conversion de trésorerie, de l'acompte initial du PO à l'encaissement final du client.

### La méthodologie centrale : cartographie déterministe de la trésorerie en trois étapes

Au lieu de projeter la trésorerie à partir de moyennes du compte de résultat, le classeur exécute un calcul déterministe en trois étapes sur une fenêtre glissante de 16 semaines ($t \in [1, 16]$) :

1. **Moteur de dédoublonnage engagement-facture :**

$$\text{Active Cash Events} = \{ \text{Billed AR} \} \cup \{ \text{Billed AP} \} \cup \{ \text{Open SOs} \setminus \text{Invoiced SOs} \} \cup \{ \text{Open POs} \setminus \text{Billed POs} \}$$



*Effet métier :* lorsqu'un bon de commande se convertit en facture fournisseur formelle dans votre système comptable, le drapeau de dédoublonnage exclut la ligne PO d'origine afin que la sortie de trésorerie ne soit jamais comptée deux fois.
2. **Traduction des dates de jalons en décalages :**
Chaque engagement actif est décomposé en tranches de trésorerie discrètes (par exemple, tranche d'acompte + tranche de solde) mappées vers des semaines civiles cibles en fonction des dates de déclenchement opérationnelles (date de commande, date d'expédition estimée, date d'arrivée estimée ou date de facture) plus les conditions de paiement contractuelles ($\Delta \text{Days}$).
3. **Évaluation glissante hebdomadaire de la liquidité et des franchissements de la zone de sécurité :**

$$\text{Ending Cash}_{w} = \text{Opening Cash}_{w} + \sum \text{Committed Inflows}_{w} - \sum \text{Committed Outflows}_{w}$$


$$\text{Liquidity Variance}_{w} = \text{Ending Cash}_{w} - \text{Minimum Safe Cash Threshold}$$



*Effet métier :* toute semaine où $\text{Ending Cash}_{w} < \text{Minimum Safe Cash Threshold}$ déclenche une alerte visuelle immédiate et isole le PO exact ou la ligne AR retardée qui provoque le point bas du fonds de roulement.

---

## Trois pièges du fonds de roulement dans les feuilles de calcul de trésorerie manuelles

### Piège 1 : se fier aux rapports mensuels de compte de résultat et de balance âgée AR/AP facturée pour la liquidité

Les rapports de balance âgée standards des comptes clients et des comptes fournisseurs n'affichent que les **transactions facturées**.

Considérez un importateur détenant $80,000 d'acomptes clients non facturés et faisant face à $60,000 de soldes d'usine contractuels dus à l'arrivée du conteneur le mois prochain. Aucune de ces obligations n'apparaît au compte de résultat ni dans la balance âgée AP standard tant que le stock n'est pas dédouané et que les factures fournisseurs ne sont pas saisies. Gérer la trésorerie hebdomadaire à partir d'états d'exercice mensuels laisse l'équipe financière avec quatre à six semaines de retard sur les engagements de trésorerie réels.

### Piège 2 : suivi cloisonné entre les commandes clients (CRM) et les bons de commande (approvisionnement)

Lorsque l'équipe commerciale accepte un acompte client de 30% le lundi et que l'équipe achats s'engage sur un prépaiement fournisseur de 40% le jeudi, les deux actions puisent dans le même compte bancaire opérationnel. Pourtant, dans la plupart des PME, les engagements commerciaux vivent dans un CRM ou une feuille de commandes tandis que les PO fournisseurs vivent dans un tableau de suivi d'approvisionnement séparé.

Maintenir des feuilles de calcul déconnectées pour les entrées clients et les sorties fournisseurs empêche les opérateurs de voir la **position de trésorerie nette hebdomadaire** lorsque les dates de réalisation glissent ne serait-ce que d'une semaine.

### Piège 3 : points bas de trésorerie intra-mois cachés dans des totaux mensuels positifs

Une synthèse mensuelle de flux de trésorerie peut afficher un solde de trésorerie net sain et positif à la fin du mois tout en masquant un découvert fatal de plusieurs jours en semaine 2 ou semaine 3.

Les pénuries de trésorerie hebdomadaires émergent du décalage de calendrier entre six variables opérationnelles :

* Solde bancaire opérationnel d'ouverture
* Dates de réception des acomptes clients et des jalons
* Conditions d'encaissement du solde client final (par exemple, avant expédition vs. Net 30)
* Dates de virement des prépaiements PO fournisseurs et des marchandises à l'arrivée
* Décaissements de fret, droits de douane et dédouanement
* Accélération du volume de commandes pendant les pics de production saisonniers

Mapper chaque engagement à une fenêtre hebdomadaire spécifique de 7 jours expose les points bas de trésorerie intra-mois alors qu'il vous reste encore 6 à 10 semaines pour négocier les conditions fournisseurs, accélérer les encaissements clients ou tirer sur une ligne de crédit renouvelable.

---

## À qui s'adresse ce modèle Excel de prévision glissante de trésorerie sur 16 semaines

Conçu pour les équipes financières opérationnelles et les entrepreneurs qui ont besoin d'une **prévision de trésorerie par la méthode directe dans Microsoft Excel** sans les coûts des logiciels TMS d'entreprise :

| Rôle et persona de recherche | Scénario opérationnel spécifique et cas d'usage du modèle |
| --- | --- |
| **Directeurs financiers et contrôleurs de gestion** *(Modèle Excel de prévision de trésorerie sur 16 semaines / 13 semaines)* | Remplacez les rapprochements bancaires manuels du vendredi par une prévision de liquidité glissante sur 16 semaines par la méthode directe qui signale les franchissements de la zone de sécurité de trésorerie 6 à 12 semaines à l'avance. |
| **Directeurs de la chaîne d'approvisionnement et des opérations** *(Suivi des flux de trésorerie des bons de commande et des prépaiements)* | Simulez l'impact de trésorerie hebdomadaire exact de la passation d'un gros PO d'usine saisonnier ou du report d'une date d'expédition avant de signer les contrats fournisseurs. |
| **Fondateurs et PDG à forte intensité de stocks** *(Feuille de calcul de fonds de roulement et de runway)* | Maintenez un tableau de bord prospectif unique de la liquidité opérationnelle nette à travers une expansion rapide des SKU, la réalisation en gros et les cycles de constitution de stocks. |
| **Responsables achats et approvisionnement** *(Planificateur des acomptes et des conditions de paiement fournisseurs)* | Évaluez les exigences de prépaiement des fournisseurs (par exemple, conditions 30/70 vs. 50/50) par rapport à la disponibilité de trésorerie hebdomadaire réellement projetée. |
| **CFO à temps partagé et CPA conseil** *(Modèle de trésorerie à court terme et de redressement)* | Déployez un outil de contrôle de flux de trésorerie hebdomadaire standardisé et prêt pour l'audit pour des clients PME confrontés à un fonds de roulement tendu ou à des covenants de reporting bancaire. |

---

## Cas d'usage réels : résoudre les scénarios de fonds de roulement et de liquidité pré-facture

### Scénario A : importateurs/exportateurs et distributeurs en gros gérant les prépaiements d'usine 30/70

Les importateurs paient régulièrement 30% à la passation du PO et 70% au connaissement ou à l'arrivée au port, tandis que les acheteurs de détail en gros paient en Net 30 ou Net 60 après la livraison entrepôt. En consignant les PO ouverts et les SO en gros dans la **chronologie de trésorerie sur 16 semaines**, le contrôleur voit le point bas exact du fonds de roulement de 4 à 8 semaines entre le paiement de l'usine outre-mer et l'encaissement auprès du détaillant national.

### Scénario B : fabricants sous contrat et constructeurs d'équipements sur mesure suivant la facturation à jalons

Les fabricants réalisant des constructions multi-étapes encaissent des paiements de progression clients (par exemple, 40% d'acompte, 30% au sous-assemblage, 30% avant expédition) tout en achetant les matières premières d'avance. Lorsqu'un jalon de production glisse de deux semaines, la mise à jour de la date d'expédition estimée dans le classeur décale automatiquement l'entrée de trésorerie client en aval et révèle si les dettes fournisseurs en matières premières franchiront la réserve de trésorerie minimale.

### Scénario C : CFO à temps partagé animant des cellules de crise de trésorerie hebdomadaires et le reporting de covenants bancaires

Pendant les redressements de fonds de roulement ou les tirages saisonniers de ligne de crédit, les banques et les équipes de direction exigent une prévision de trésorerie directe hebdomadaire transparente (souvent demandée sous forme de rapport de flux de trésorerie glissant sur 13 ou 16 semaines). Ce modèle fournit des analyses détaillées au niveau des transactions montrant précisément quelles factures clients et quels PO fournisseurs pilotent le flux de trésorerie net de chaque semaine.

---

## Ce que le classeur suit : correspondance entre points de douleur et solutions

| Point de douleur en gestion de trésorerie | Exigence de recherche à haute fréquence | Solution intégrée au classeur Excel |
| --- | --- | --- |
| **PO non facturés absents des prévisions de trésorerie** | *Comment inclure les bons de commande ouverts dans une prévision de trésorerie Excel* | **Registre unifié des engagements ouverts :** capture les AR facturés, les AP facturés, les commandes clients non facturées et les bons de commande ouverts dans une seule table de saisie structurée. |
| **Double comptage des PO après facturation** | *Empêcher les doublons de PO et de factures dans la projection de trésorerie* | **Dédoublonnage automatisé PO-vers-facture :** identifie et exclut les bons de commande déjà convertis en factures AP formelles afin que chaque dollar ne soit compté qu'une seule fois. |
| **Découverts intra-mois et pénuries surprises** | *Modèle de prévision de trésorerie glissante hebdomadaire avec alertes de trésorerie basse* | **Couche d'alertes de seuil configurable :** compare la trésorerie de fin de semaine projetée à votre solde de trésorerie minimale de sécurité personnalisé et met en évidence les semaines de franchissement en temps réel. |
| **Estimations d'expédition et de livraison périmées** | *Modèle de flux de trésorerie dynamique basé sur les dates d'expédition et les conditions de paiement* | **Mappage automatisé des conditions en semaines :** traduit les dates opérationnelles (date d'expédition estimée, date d'arrivée, date de facture) et les conditions de paiement en fenêtres de trésorerie hebdomadaires exactes. |
| **Contrôles d'approbation pré-engagement lents** | *Tester l'impact de trésorerie d'un nouveau bon de commande fournisseur avant d'acheter* | **Bac à sable de liquidité pré-décision :** saisissez un PO proposé ou une commande client pour voir immédiatement si le nouvel engagement crée un déficit de trésorerie à 6 à 16 semaines. |

---

## Étude de cas : cécité de l'exercice mensuel vs. visibilité glissante de trésorerie sur 16 semaines

**Profil de l'entreprise :** importateur de biens de consommation réalisant $2M–$10M de chiffre d'affaires annuel, opérant avec des conditions d'acomptes clients mixtes, des calendriers de prépaiement fournisseurs outre-mer et une équipe financière restreinte à un seul gestionnaire.

**La panne opérationnelle :** chaque semaine, le responsable financier passait deux heures à recouper les commandes clients du CRM, les reçus d'acomptes clients, les PO d'usine ouverts et les calendriers d'arrivée du fret dans des feuilles de calcul déconnectées. Malgré un flux de trésorerie net mensuel positif sur le papier, l'entreprise a subi deux pénuries de trésorerie d'urgence en un seul trimestre — toutes deux découvertes moins de 48 heures avant l'échéance des virements fournisseurs internationaux.

### Comparaison : feuilles AR/AP déconnectées vs. modèle automatisé d'engagements sur 16 semaines

| Opération de trésorerie | Feuilles de calcul manuelles déconnectées (avant) | Classeur automatisé de flux de trésorerie glissant sur 16 semaines (après) |
| --- | --- | --- |
| **Architecture des données d'engagements** | Feuilles de ventes CRM cloisonnées, tableaux de suivi des PO d'approvisionnement et exports AR/AP comptables | **Registre d'engagements unifié unique** couvrant AR, AP, SO ouverts et PO ouverts avec dédoublonnage |
| **Temps de préparation de la prévision hebdomadaire** | ~2 heures de VLOOKUP manuels et de recoupements de dates chaque vendredi | **Moins de 5 minutes par semaine** ; la fenêtre glissante de 16 semaines se met à jour dynamiquement à la saisie des dates |
| **Visibilité des prépaiements pré-facture** | Aveugle aux acomptes fournisseurs et aux soldes de jalons tant que les factures fournisseurs ne sont pas comptabilisées | **Mappage complet des jalons** à travers les tranches d'acompte, les paiements avant expédition et les virements de livraison |
| **Fenêtre de détection des insuffisances de liquidité** | Découverte 24 à 48 heures avant l'échéance du virement (tirages de crédit d'urgence forcés) | **Signalée 6 à 12 semaines à l'avance** via des alertes automatisées de franchissement du seuil de trésorerie minimale |

### Le point d'inflexion exact que ce classeur met en évidence

Considérez une **commande client de $100,000** et le **bon de commande fournisseur de $50,000** qui lui est lié, à partir d'un **solde de trésorerie d'ouverture de $10,000** :

* **Solde du PO fournisseur ($30,000 de sortie) :** 60% dus à l'arrivée des marchandises en **semaine 5**.
* **Solde de la SO client ($70,000 d'entrée) :** 70% dus avant l'expédition entrepôt en **semaine 6**.

| Granularité de reporting | Position de trésorerie nette semaine 5 | Position de trésorerie nette semaine 6 | Conclusion opérationnelle |
| --- | --- | --- | --- |
| **Synthèse mensuelle de trésorerie traditionnelle** | *Cachée dans le total mensuel* | **+$50,000 de trésorerie fin de mois** | Feu vert fallacieux ; la finance approuve les conditions sans voir le défaut de milieu de mois |
| **Modèle glissant hebdomadaire sur 16 semaines** | **−$20,000 de pénurie de trésorerie** ($10K − $30K) | **+$50,000 de redressement** (−$20K + $70K) | **Signale le déficit de $20,000 de la semaine 5 avec 5 semaines d'avance**, permettant à l'équipe d'aligner les conditions de virement fournisseur sur la réception client |

---

## Normes de trésorerie derrière la prévision glissante de trésorerie par la méthode directe

Les équipes de trésorerie d'entreprise s'appuient sur la **prévision glissante de flux de trésorerie à court terme par la méthode directe** parce que les comptes de résultat en exercice mesurent la rentabilité plutôt que la solvabilité de trésorerie. Les entreprises de produits en forte croissance affichent fréquemment de solides marges comptables tout en manquant de trésorerie opérationnelle en raison du calendrier des prépaiements de stocks.

La méthode directe contourne les ajustements de la comptabilité d'exercice et mappe **100% des encaissements bruts et des décaissements bruts attendus** vers des fenêtres hebdomadaires spécifiques :

| Méthode de reporting traditionnelle | Limitation structurelle dans les opérations | Comment le modèle par la méthode directe sur 16 semaines la résout |
| --- | --- | --- |
| **Estimation de trésorerie indirecte via le compte de résultat** | Confond le résultat net comptable avec les fonds bancaires liquides ; masque les pics de fonds de roulement de milieu de mois | Mappe **les encaissements et virements de décaissement datés réels** semaine par semaine |
| **Vérification quotidienne du solde bancaire** | Purement rétrospective ; montre la trésorerie réglée en ignorant plus de $100K de virements de PO engagés à venir | Projette **des soldes de trésorerie courants prospectifs** sur les 16 semaines consécutives à venir |
| **Rapports mensuels de balance âgée AR / AP** | Exclut les bons de commande non facturés et les jalons clients avant expédition | Intègre **les engagements de commandes pré-facture** aux créances et dettes facturées |

**Référentiels faisant autorité en trésorerie et gestion de trésorerie cités :**

* [AICPA : Prévision de flux de trésorerie par la méthode directe et gestion du fonds de roulement](https://www.aicpa-cima.com)
* [Association for Financial Professionals (AFP) : normes de trésorerie à court terme et de prévision glissante de trésorerie](https://www.afponline.org)

---

## Fonctionnement de l'horizon glissant sur 16 semaines et du mappage des dates en décalages

L'horizon de prévision de 16 semaines glisse vers l'avant semaine après semaine. Chaque commande ouverte ou facture est affectée à une semaine de trésorerie future spécifique en combinant sa **date de jalon opérationnel** avec sa **condition de paiement contractuelle** :

| Entrée de jalon opérationnel | Condition de paiement contractuelle | Événement de flux de trésorerie hebdomadaire dérivé dans le modèle |
| --- | --- | --- |
| **Date d'expédition client estimée** | *Solde dû avant l'expédition* | **Entrée de trésorerie (encaissement)** mappée sur la semaine précédant immédiatement l'expédition estimée |
| **Date d'arrivée des marchandises estimée (ETA)** | *Solde dû à la livraison / à l'arrivée* | **Sortie de trésorerie (virement fournisseur)** mappée sur la semaine d'arrivée estimée entrepôt/port |
| **Date d'émission de la facture client** | *Condition de crédit Net 30 jours* | **Entrée de trésorerie (encaissement)** mappée 4 semaines après la date de facture |

**Pourquoi la précision de la prévision se scinde entre l'horizon proche (semaines 1–8) et l'horizon lointain (semaines 9–16) :**

* **Semaines 1–8 (fenêtre d'exécution à haute confiance) :** pilotée par les factures confirmées, les calendriers de navires verrouillés et les bons de commande actifs déjà en production. Utilisée pour la planification stricte des paiements, les approbations de virements et les décisions de tirage de ligne de crédit.
* **Semaines 9–16 (fenêtre de planification stratégique et d'approvisionnement) :** pilotée par les délais de production estimés et les commandes clients en pipeline. Utilisée pour tester si de nouveaux PO fournisseurs peuvent être financés par la trésorerie interne avant la signature des contrats.

---

## Tutoriel de démarrage rapide : construire votre prévision glissante de trésorerie sur 16 semaines en 7 étapes

Suivez ce workflow étape par étape pour faire passer votre équipe financière et opérationnelle des vérifications réactives du solde bancaire à une gestion proactive de la liquidité sur 16 semaines :

1. **Testez les scénarios d'engagements dans la démo interactive du navigateur**
Ouvrez le [simulateur web de flux de trésorerie glissant sur 16 semaines](https://hyvoid.github.io/rolling-cashflow-forecast/) pour explorer comment les PO ouverts, les acomptes clients et les retards d'expédition décalent les soldes de trésorerie hebdomadaires en temps réel.
2. **Configurez le solde de trésorerie d'ouverture et la zone de sécurité de trésorerie minimale**
Saisissez votre solde bancaire opérationnel actuel, définissez votre date de prévision de départ (lundi) et fixez le **seuil de trésorerie minimale de sécurité** de votre entreprise (par exemple, $25,000 ou 1 mois de masse salariale/charges fixes).
3. **Consignez les comptes clients (AR) et comptes fournisseurs (AP) facturés**
Saisissez les factures clients en attente et les factures fournisseurs avec leurs dates d'échéance contractuelles pour établir votre chronologie de trésorerie de base post-facture.
4. **Saisissez les commandes clients (SO) non facturées et les bons de commande (PO) ouverts**
Enregistrez les commandes clients confirmées et les PO fournisseurs actifs avec les pourcentages d'acompte, les pourcentages de solde, les dates d'expédition/arrivée estimées et les conditions de paiement.
5. **Exécutez le dédoublonnage automatisé PO-vers-facture**
Marquez ou liez les bons de commande déjà facturés par les fournisseurs afin que le moteur de dédoublonnage les exclue des engagements ouverts et empêche tout double comptage.
6. **Inspectez les alertes de franchissement de seuil hebdomadaires et diagnostiquez les points bas de trésorerie**
Parcourez la chronologie de trésorerie sur 16 semaines pour repérer toute semaine passant sous votre zone de sécurité minimale, puis filtrez la table des engagements par le numéro de cette semaine pour identifier le PO fournisseur exact ou l'encaissement client retardé qui provoque l'écart.
7. **Standardisez votre revue de trésorerie hebdomadaire avec le classeur Excel réutilisable**
Une fois la logique testée dans l'aperçu web à session unique, **[téléchargez le modèle Excel complet et réutilisable de prévision glissante de trésorerie sur 16 semaines](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)** pour enregistrer les données continues de votre entreprise, personnaliser le suivi des contreparties et exécuter votre revue de liquidité hebdomadaire de 5 minutes hors ligne dans Microsoft Excel.

*Avertissement : ce classeur est un modèle de planification de trésorerie opérationnelle et d'aide à la décision. Il complète — sans les remplacer — les logiciels comptables GAAP/IFRS formels, les états financiers audités et les conseils autorisés en trésorerie ou en financement.*

---

## Télécharger le modèle Excel complet

Prêt à éliminer les pénuries surprises aux dates de paiement et à unifier vos AR, AP et engagements de commandes ouverts dans une chronologie glissante unique ?

👉 **[Obtenir le classeur Excel complet de prévision glissante de trésorerie sur 16 semaines](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)**

---

## Périmètre technique et limites opérationnelles

* **Dépendance à la fraîcheur des données :** la précision de la prévision repose sur des estimations opérationnelles à jour ; des PO fournisseurs non consignés ou des dates d'arrivée de fret périmées sous-estimeront ou désaligneront les sorties de trésorerie hebdomadaires.
* **Cadence de maintenance glissante hebdomadaire :** conçu pour une actualisation hebdomadaire de 5 minutes (mise à jour de la trésorerie d'ouverture, avancement de la date de départ et ajustement des ETA d'expédition décalées).
* **Couche d'aide à la décision (pas un grand livre comptable) :** conçu pour la planification prospective de la liquidité ; ne remplace pas les systèmes ERP, les logiciels de comptabilité en partie double ni les registres fiscaux statutaires.
* **Mappage déterministe des dates :** modélise chaque tranche d'engagement sur une date cible et un montant spécifiques ; les décotes probabilistes pour paiements tardifs ou les tests de stress d'annulation de commandes nécessitent des dépassements manuels de dates/montants.
* **Variance de l'horizon lointain (semaines 9–16) :** les semaines 1–8 reflètent des engagements quasi verrouillés, tandis que les semaines 9–16 reflètent des estimations opérationnelles soumises aux variations des délais de la chaîne d'approvisionnement.
* **Architecture à devise de base unique :** les PO fournisseurs multidevises (par exemple, USD vs. EUR/CNY) doivent être saisis au taux de change budgété ou couvert à terme dans la devise de base.
* **Échelle opérationnelle recommandée :** optimisé pour les PME gérant activement **5 à 50 commandes/PO ouverts simultanés** par cycle glissant dans Microsoft Excel.

---

## À propos de Theseus Workshop

Nous construisons des modèles financiers et opérationnels Microsoft Excel pratiques et prêts pour l'audit pour les entreprises de négoce, de fabrication et pilotées par les opérateurs qui ont besoin d'un contrôle de trésorerie et comptable institutionnel dans des feuilles de calcul standard.

Chaque classeur utilise des formules Excel natives transparentes sans aucune macro boîte noire, donnant aux équipes financières et opérationnelles une visibilité complète sur chaque calcul de trésorerie hebdomadaire.

Vous résolvez des problèmes complexes de fonds de roulement, d'approvisionnement en stocks ou d'allocation de capital dans des feuilles de calcul ? **[Explorez notre collection complète de modèles Excel financiers et opérationnels chez Theseus Workshop →](https://www.theseusworkshop.com)**

---

## Licence

Distribué sous la [licence open source Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

