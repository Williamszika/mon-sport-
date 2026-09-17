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
   - Sport : 3 séances/semaine en alternance A (haut du corps) / B (bas du
     corps), un jour de repos entre deux — voir `sport/planning-progressif.html`
     et l'état réel dans `sport/carnet.html`.
   - Études : un bloc par jour (réviser → apprendre → s'exercer), lecture le
     soir, dictée 3×/semaine — voir `etudes/routine-etudes.html`.

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
- **École** : Luisenhospital, Boxgraben 99 — horaires variables (~07:30/08:00 → 15:00/15:30).
- **Travail posté** : shift F 06:30–14:30 · shift S 13:30–20:30/21:00 — demander
  l'emploi du temps du jour, il change.
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
  poids modérés, cardio à chaque séance.
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
  William marque facilement. Pour les pieds : le soir sur peau sèche et saine,
  laver le matin, tient jusqu'à 3 jours (2×/semaine suffisent) — utile, il
  porte des chaussures fermées toute la journée à l'hôpital et à la salle.
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
  **IL MANQUE TOUJOURS un antitranspirant `ohne Parfüm`** (~2–3 € chez dm) :
  les deux produits achetés sont parfumés, donc **aucun n'est utilisable les
  jours d'hôpital**. Le parfum vient ensuite : un seul flacon, 70–120 €, choisi
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
