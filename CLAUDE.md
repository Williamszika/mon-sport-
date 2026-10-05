# Instructions pour Claude — dépôt mon-sport-

Dépôt personnel de William : suivi **soin** (Rituel Éclat), **sport** (FitX
Aachen) et **études** (Luisenhospital). Tout se passe en **français**, simple
et clair.

## Règle n° 1 — TOUJOURS vérifier la date et la météo avant un planning

Avant de donner un planning, une routine du jour, ou tout conseil dépendant du
moment (« ce soir », « demain », « cette semaine ») :

1. **Date et heure réelles d'Aachen** : `TZ=Europe/Berlin date '+%A %d %B %Y · %H:%M %Z'`
   — Aachen est sur le fuseau de Berlin (Europe/Berlin, CET/CEST) ; c'est
   l'heure locale de William, à Campus-Boulevard 62, 52074 Aachen. Ne jamais
   déduire le jour ou l'heure du fil de la conversation : toujours exécuter la
   commande. Afficher la date et l'heure vérifiées en tête de chaque planning.
   ⚠️ **Une vérification EXPIRE** : entre deux messages de William, des heures
   ou une nuit entière peuvent passer (erreur commise le 24/08 : répondu avec
   la date de la veille). Re-exécuter la commande à CHAQUE message lié au
   temps — « aujourd'hui », « hier », « ce soir », routine, planning — jamais
   se fier au check du message précédent. Les « hier / demain » de William se
   réfèrent à SA date au moment où il écrit, pas à celle du dernier check.
2. **Météo d'Aachen** : `curl -s "https://wttr.in/Aachen?format=j1"` — regarder
   surtout **l'indice UV** (dicte le SPF 30 vs SunDance 50), la température et
   la pluie (trajets en bus).
   ⚠️ **Si wttr.in échoue** (certificat expiré le 16/09/2026, erreur
   `SSL certificate problem: certificate has expired` — ne jamais désactiver la
   vérification TLS), utiliser **Open-Meteo**, qui donne les mêmes champs :
   `curl -s "https://api.open-meteo.com/v1/forecast?latitude=50.7753&longitude=6.0839&hourly=temperature_2m,precipitation_probability,uv_index,weathercode&daily=temperature_2m_min,temperature_2m_max,uv_index_max&timezone=Europe%2FBerlin&forecast_days=1"`
   (50.7753 N / 6.0839 E = Aachen). Toujours dire à William quelle source a
   servi si ce n'est pas la source habituelle.
3. **Croiser avec les calendriers** avant de prescrire :
   - Soin (rituel d'août) : rétinol **mardi & vendredi** soir · gommage corps
     **mercredi & dimanche** · peeling visage AHA/PHA **dimanche** soir ·
     Vitamine C + SPF 30 chaque matin · lendemain de rétinol ou de peeling =
     SPF obligatoire même temps gris.
   - Sport : **corps entier** — adopté le 29 septembre, **première séance le
     lundi 5 octobre** (fin de l'alternance A/B) — 3 séances/semaine (lundi · mercredi · vendredi), un jour de repos
     entre deux. Ordre : vélo 8 min → **Shoulder Press** → Vertical Traction →
     Leg Press → Chest Press → Low Row → Seitheben (élévations latérales,
     haltères) → Leg Curl → planche. **Version courte** = les quatre premières
     lignes, 2 × 12. Voir la section « Le corps entier » de
     `sport/planning-progressif.html` et le tableau « Corps entier » de
     `sport/carnet.html`. Vue d'ensemble de la semaine (page publiée) :
     https://claude.ai/artifact/XcJggXvWpvEar7NDkXF9yb — la page du jour reste
     https://claude.ai/artifact/Ucbs5BkTi3abNpVMQXAtqG.
   - **Souplesse & Kegels — chaque jour** : 7 min d'étirements le soir (6
     postures : pectoraux, fente basse, ischio-jambiers, fessiers, posture de
     l'enfant, mollets) · **Kegels 3 fois par jour** (matin, midi, soir :
     10 contractions tenues 5 s + 10 rapides). À inclure dans le planning.
   - Études : un bloc par jour (réviser → apprendre → s'exercer), lecture le
     soir, dictée 3×/semaine — voir `etudes/routine-etudes.html`.
   - **Santé AOK — la prochaine démarche dans chaque planning**, jusqu'à ce que
     William confirme qu'elle est faite. Ordre (voir `sante/carte-aok.html`,
     section « Ton calendrier santé », page publiée
     https://claude.ai/artifact/S1onjqBpXr7WJWFEFEKtA2) : inscription au bonus
     **Vital+** dans l'app Meine AOK → appels Hausarzt (Check-up + vaccin
     grippe), Hautarzt (dépistage peau), Zahnarzt (contrôle + détartrage) →
     vaccin grippe en octobre → Check-up → dentiste et dépistage peau →
     deux cours gratuits par an (Rückenschule, yoga ou Pilates). Les appels se
     placent les jours sans salle, après la pause.
     **Cabinets près de chez lui** (30/09, temps de marche depuis
     Campus-Boulevard calculé sur OpenStreetMap — section « Les cabinets » de
     la page) : Hausarzt **Praxis Steppenberg**, Steppenbergallee 12, 20 min,
     Doctolib, 0241 / 89 40 40 4 (ou Fritz König, Auf der Hörn 125, 16 min,
     0241 81080) · Zahnarzt **MH Dental**, Steppenbergallee 14, 20 min,
     Doctolib, 0241 87 77 81 · Hautarzt : aucun conventionné à pied — en ville
     un jour de cours, Dr. Harst (Doctolib) ou Dr. Alberty, 0241 / 44 67 30.
   - **Déo & parfum — À INCLURE DANS CHAQUE PLANNING QUOTIDIEN** (demandé par
     William le 18 septembre). Trois produits, trois zones, jamais superposés ;
     donner à chaque fois **lequel, où et quand** pour CE jour-là :
     · **bruno banani** (spray parfumé) — **le matin**, 2 pulvérisations **sur
       le torse**. Mais **lundi, mercredi et samedi** (lendemains de peeling et
       de rétinol) : **sur les vêtements seulement**, jamais sur le cou.
     · **Balea MEN Fresh** (antitranspirant) — **le soir**, à 15 cm, sur
       **aisselles propres et sèches**, après la douche. Bien secouer. Jamais
       le matin, jamais sur des aisselles fraîchement rasées.
     · **Perspirex Foot Lotion** — **jeudi et dimanche soir** en entretien
       (chaque soir s'il est en semaine de lancement), plante des pieds, peau
       sèche, laisser sécher à l'air, **laver le matin**.
     · **Jour d'hôpital / stage / ambulante Pflege = ZÉRO des deux parfumés**,
       ni la veille au soir pour le Balea. Ne restent que : douche juste avant
       de partir, chemise lavée à 40°, Perspirex aux pieds — et le **sebamed
       parfumfrei** une fois acheté. L'ambulante Pflege (soins à domicile)
       suit la même règle que l'hôpital : contact direct avec des patients
       (appliqué le 28/09). Toujours demander si la journée est école (parfum
       autorisé) ou hôpital / ambulante Pflege (zéro).
     Détail complet : `soin/parfum.html`, sections « Le planning des trois
     produits » et « La semaine, jour par jour ».

## Règle n° 2 — Tout noter au journal

Chaque séance de sport, chaque changement de programme, chaque événement
notable : mettre à jour `sport/carnet.html` (poids, n° de siège, chronos),
`JOURNAL.md` **et** `journal.html`, puis **commit + push** sur la branche de
travail. Les poids réels priment sur le plan ; ne jamais inventer un chiffre.

## Règle n° 3 — Planifier comme un humain, pas comme une machine

- **William a 32 ans** — parler d'adulte à adulte, sans sur-expliquer.
- **Toujours une vraie pause (30–60 min)** entre l'école/le travail et tout
  bloc planifié (études ou salle) : manger, souffler. Le bloc commence après,
  pas à la descente du bus.
- Plannings avec **des fourchettes et de l'air**, pas de minutage militaire.
  Une journée a du temps libre non assigné ; le plan est un guide, pas une
  prison.
- **Études : William étudie depuis SON propre dépôt de sujets.** Claude
  planifie les créneaux et tient le journal — résumés, exercices, corrections
  et dictées **uniquement sur demande explicite**.
- **Objectif langue : examen B2 l'année prochaine** (écrire, parler, écouter)
  — voir `etudes/plan-allemand-b2.html`. Examen exact (Goethe / telc /
  telc B2 Pflege) et date à confirmer par William.
- **Photos : aucun besoin de photos de lui.** Les poids, chronos et sensations
  suffisent au suivi. Les photos de machines ou d'écrans restent bienvenues
  pour identifier ou régler quelque chose.

## Contexte fixe

- **Domicile** : Campus-Boulevard 62, 52074 Aachen (Melaten).
- **Assurance santé** : **AOK Rheinland/Hamburg** — confirmé sur la carte
  (photo du 30/09, non conservée : aucun numéro d'assuré ni photo de lui dans
  le dépôt). Service AOK 0211 8195-0000 · hotline médicale gratuite
  0800 1 265 265 · carte européenne au dos, valable jusqu'en 09/2029. Droits vérifiés le 30/09 dans la
  Satzung en vigueur au 01/07/2026 : Check-up 1× entre 18 et 34 ans ·
  dépistage peau **tous les 2 ans de 18 à 34 ans** (contrat AOK – KV Nordrhein)
  · dentiste 2×/an + détartrage 1×/an · vaccins STIKO (grippe chaque automne,
  soignant) · **2 cours gratuits/an** (bon AOK, 80 % de présence) · médecine
  du sport 100 % jusqu'à 70 €/an (certificat + Sportmediziner) · vaccins de
  voyage jusqu'à 120 €/an. **Pas pour lui** : PZR à 35 € (16–25 ans seulement),
  ostéopathie à 200 € (Kostenerstattung seulement) — les deux passent par le
  bonus Vital+ (20 € par mesure, utilisable aussi pour l'abonnement FitX).
  Détail et sources : `sante/carte-aok.html`.
- **École** : Luisenhospital, Boxgraben 99 — horaires variables (~07:30/08:00 → 15:00/15:30).
- **Travail posté** : shift F 06:30–14:30 · shift S 13:30–20:30/21:00 — demander
  l'emploi du temps du jour, il change. **Depuis le 28/09 : ambulante Pflege**
  (soins à domicile) — du 28/09 au 02/10 de 07:00 à 15:00, samedi 3 et
  dimanche 4 le soir. **Semaine du 5 au 11 octobre : 06:30–14:30 tous les
  jours, week-end compris** (confirmé le 5/10 ; horaires du week-end supposés
  identiques), **salle à 19 h 30** lun · mer · ven (choix de William) : rentrer,
  manger, vraie pause hors du lit, 30 min d'études, départ vers 18 h 50, retour
  vers 21 h, au lit 22 h–22 h 30. **Zéro parfum les sept jours** : ni bruno
  banani ni Balea de toute la semaine, le sebamed est le seul déo possible
  (pas encore acheté au 5/10). Règle d'une semaine de
  travail : la salle après une vraie pause et assez tôt pour dormir sept heures
  (17 h 30 quand le travail finissait à 15 h, la semaine du 28/09) ; la séance
  complète est prévue, la version courte reste le plancher.
- **Salle** : FitX Aachen-Europaplatz, Europaplatz 17 — ouverte 24 h/24, arrêt
  de bus **Wiesental** à 160 m. Il se déplace **en bus** : toujours penser au
  bus du retour.
- **Régularité — engagement pris le 4 septembre.** À partir du **lundi
  7 septembre**, trois séances par semaine à jours fixes : **lundi · mercredi ·
  vendredi**, vers 20 h 30. Les jours ne se rediscutent pas. Le suivi est la
  section **« La chaîne »** de `sport/carnet.html` (12 semaines, jusqu'au
  27 novembre). Une case cochée = une séance faite, **maison et version courte
  comprises**. Les jours de séance, demander le résultat et cocher la case ;
  ne jamais laisser une séance non renseignée.
- **Le matériel de la salle : LIRE `sport/machines-fitx.html` EN PREMIER.** Ce
  document (16 août) décrit les **7 zones** et l'équipement de FitX Europaplatz
  — 60+ machines Technogym, Hammer Strength, zone *Freihantel* (poulies
  **Kabelturm**, haltères jusqu'à 60 kg, barres, bancs), zone *Functional*
  (kettlebells, medicine balls, tapis), *Zirkel*, *Kursraum*, et au cardio :
  tapis, Crosstrainer, rameurs, **Stairclimber**, vélos. ⚠️ Erreur commise le
  13 septembre : avoir affirmé qu'aucune liste n'existait, sans avoir lu ce
  fichier. **Toujours le consulter avant de dire qu'une machine est inconnue.**
  **Inventaire vérifié en photo le 14 septembre** (section « L'inventaire » du
  même fichier) : tout le cardio, les 8 machines du programme, plus le
  **Multi Hip** (99 Abduktion / 100 Adduktion), une machine **Klimmzug/Dip
  assisté**, trois **bancs à abdos** (Bauchbank), les rameurs Concept2 et la
  zone Hammer Strength. **Toujours pas vus : le Kabelturm (poulies) et un
  éventuel Butterfly/Pec Deck.** Ce qui manque encore partout : **le pas des
  piles et les numéros de siège** — ils se relèvent en direct devant la
  machine, jamais en photo. Chiffré au carnet : Leg Press (pile de **10 en 10**), Leg
  Extension, Leg Curl, Chest Press, Vertical Traction, Low Row, Shoulder Press,
  Abdominal Crunch (repérée), machines d'abduction, haltères, vélo, tapis,
  elliptique, rameur, **Treppensteiger** (= le Stairclimber, déjà décrit le
  16 août), Turnecke. **Ne jamais inventer un pas de pile ni un réglage.**
  Pacte du 13 septembre : quand une machine non chiffrée entre au programme, **la nommer dans le message qui PRÉCÈDE la séance** (nom allemand,
  allure, muscle travaillé) — William va la chercher tranquillement, jamais
  pendant la séance. Si elle n'est pas trouvée en deux minutes : séance sans
  elle. Ordre prévu : **poulie (Kabelzug)** → Butterfly/Pec Deck → biceps &
  triceps. Rien ne viendra sur rack à squat, barres libres, kettlebells, TRX ni
  Hip Thrust. Voir `sport/planning-progressif.html`, section « Les machines
  qu'on n'a pas encore ».
- **Respiration sous charge** : expirer pendant l'effort, inspirer au retour,
  **ne jamais bloquer** (pression sur le plancher pelvien). Le test : pouvoir
  dire un mot en série. Aucune machine ne travaille le plancher pelvien — les
  Kegels quotidiens sont le seul entraînement.
- **Créneau salle qui marche : ~20 h 30.** Les séances réellement faites ont
  toutes eu lieu le soir (15/08 après un shift, 21/08 et 28/08 à 20 h 30). Le
  créneau « 16 h en sortant de l'école » a échoué **quatre fois d'affilée**
  (30/08 → 02/09) : après sept heures de cours, il ne reste rien à 16 h. Le
  schéma qui tient : rentrer → manger → souffler une vraie heure → partir. Ne
  jamais reproposer 16 h les jours d'école.
- **Objectif sport** : physique sec et dessiné, pas massif — 12–15 répétitions,
  poids modérés. Il est **déjà sec** (photos du 3/09, `sport/silhouette.html`) :
  épaules étroites par rapport aux hanches, un peu enroulées, jambes déjà bien
  fournies. **Priorité : élargir les épaules** (Shoulder Press en premier,
  élévations latérales), puis le dos. Cardio = l'échauffement au vélo ; le
  Treppensteiger devient facultatif.
- **Peau** : marque facilement — douceur d'abord, jamais deux actifs forts le
  même soir.
- **La trousse est close — douze produits, vérifiés en photo le 3 septembre**
  (section « Ta trousse » de `soin/rituel-eclat-aout-2026.html`). **Ne jamais
  citer, prescrire ou supposer un produit qui n'y figure pas.** C'est William
  qui annonce quand un produit se termine ou quand il en achète un nouveau ;
  la liste n'est mise à jour que sur son signalement.
- **Parfum & déodorant — hors trousse, en cours de mise en place.** William a
  un **Perspirex Foot Lotion** (Riemann, 100 ml — Alcohol Denat., Aluminum
  Chloride, PEG-12 Dimethicone), vérifié en photo le 14 septembre : c'est un
  antitranspirant **pour les PIEDS uniquement**. **Ne jamais le conseiller sous
  les bras** — formule concentrée pour peau plantaire épaisse, et la peau de
  William marque facilement. Pour les pieds, **protocole du fabricant**
  (vérifié le 18/09) : le soir sur peau sèche et saine, laisser sécher à l'air,
  **laver le matin** ; **chaque soir la première semaine**, puis **2 à 3 fois
  par semaine** — une application tient **3 à 5 jours**. Si ça irrite, sauter
  la semaine de lancement. Utile : il porte des chaussures fermées toute la
  journée à l'hôpital et à la salle. ⚠️ **William l'utilisait sous les bras**
  (signalé le 17/09) — corrigé, c'est le Balea qui prend cette place.
  **Achetés le 17 septembre, vérifiés en photo :**
  (1) **Balea MEN Fresh Anti-Transpirant**, 200 ml spray — *Aluminum
  Chlorohydrate*, **0 % alcool**, 48 h, parfumé (Duftkapsel + **menthol, huile
  de menthe, camphre, romarin**). C'est bien un antitranspirant et c'est le bon
  produit du quotidien : **le soir, à 15 cm, sur aisselles sèches**. ⚠️ Le
  menthol et le camphre piquent sur peau irritée — **jamais juste après un
  rasage des aisselles** (l'étiquette le dit : *nicht auf gereizter Haut*).
  (2) **bruno banani Loyal Man**, 150 ml — spray corporel **parfumé** (gingembre,
  géranium, ambre), base alcool, **sans sels d'aluminium** : ce n'est ni un
  antitranspirant ni un vrai parfum. À porter sur le torse ou les vêtements,
  **jamais superposé au Balea sous les bras**. Famille boisé/épicé — utile pour
  savoir gratuitement si cette famille lui plaît avant le flacon à 70–120 €.
  **IL MANQUE TOUJOURS un produit sans parfum** : les deux achats sont
  parfumés, donc **aucun n'est utilisable les jours d'hôpital**. Produit
  identifié chez dm : **sebamed Deo Roll-on Balsam parfumfrei**, 50 ml (les
  Balea « Sensitive » sont sans aluminium mais pas garantis sans parfum).
  Vérifié sur dm.de le 28/09 : **déodorant, pas antitranspirant** — sans sels
  d'aluminium, sans alcool, **sans parfum**, pH 5,5, bisabolol, 48 h contre les
  odeurs, toléré après rasage. Il ne coupe pas la transpiration, il neutralise
  l'odeur : le matin sur aisselles sèches, à reprendre dans la journée si
  besoin. Pas encore acheté au 28/09. **Planning
  d'utilisation des trois produits** : sections « Le planning des trois
  produits » et « La semaine, jour par jour » de `soin/parfum.html`. Le parfum vient ensuite : un seul flacon, 70–120 €, choisi
  après essai sur la peau. **Zéro parfum à l'hôpital, autorisé en cours.** Lendemains
  d'actifs (lundi, mercredi, samedi) : parfum sur les vêtements seulement.
  Voir `soin/parfum.html`. Ces produits ne font PAS partie des douze de la
  trousse — ne jamais les y compter.
- **Allemand** : apprenant (~B1) ; pour les études, résumés en allemand simple
  avec les termes durs expliqués en français ; dictées avec score de fautes.

## Style

Français chaleureux et direct, tableaux courts, pas de jargon. Les documents
HTML partagent une charte (porcelaine/prune/miel) — la respecter pour tout
nouveau document, et vérifier les collisions de classes CSS avant de pousser.
