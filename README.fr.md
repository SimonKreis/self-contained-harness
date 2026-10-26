<!-- translation-of: README.md @ 4fca54a9de5746a949b3c038638df90dbced5851 -->

# Le harnais autonome

[English](README.md) · **Français**

*Un thème, un dossier, une note vivante.*

**Le harnais autonome** est un manuscrit qui propose un cadre pour garder le contexte
personnel et professionnel utilisable à l'ère des agents d'IA. Il s'attaque à deux
problèmes : l'explosion de l'information, que l'IA générative a aggravée (la matière croît
désormais plus vite que quiconque ne peut la lire, et elle est éparpillée entre applications
de notes, espaces de stockage en ligne et historiques de conversation), et le renouvellement
incessant des choix d'outils d'IA, où chaque changement de modèle, de moteur ou d'abonnement
devient une migration. Son idée centrale : tenir **un dossier autonome par thème**, autour
d'une note vivante, en fichiers ordinaires et portables. La personne agence les dossiers comme
elle pense ; les agents distillent, recyclent et élaguent ce qui y est capturé.
**La structure est personnelle ; la distillation ne l'est pas.**

> **État : version provisoire, travail en cours, commentaires bienvenus.**
> C'est une version provisoire complète, pas un travail achevé. Des sections changeront, et
> les parties datées (la partie IV et la section 3.7) sont faites pour être révisées à mesure
> que les outils et les bancs d'essai évoluent.

> **Thèse.** L'IA agentique est à la fois la cause de l'explosion de l'information et,
> paradoxalement, son remède : un dossier autonome par thème autour d'une note vivante,
> agencé par vous et distillé par des agents, pour que vous et eux vous appuyiez sur le même
> contexte, dans des formats portables qui survivent à n'importe quel outil.

**Le lire :** [the-self-contained-harness.fr.md](the-self-contained-harness.fr.md).

**Simon Kreis & Claude.** Réalisé avec l'IA, principalement Claude (Anthropic), qui a contribué en partie ou en totalité au travail. Simon Kreis en est responsable. D'après une idée originale de Simon Kreis.

Version provisoire, mise à jour en octobre 2026.

---

## Ce que propose le manuscrit

Les noms ci-dessous sont ceux qu'emploie le manuscrit.

**Un problème, deux victimes.** Le contexte est produit plus vite que jamais et éparpillé en
plus d'endroits que jamais. L'agent paie en résultats : il ne peut pas se servir d'un contexte
qu'il ne trouve pas, et il travaille moins bien quand on lui en donne trop. La personne paie en
attention : boucles ouvertes, bruit, reconstruction. Une description complète, à jour et
distillée de chaque travail, en un seul endroit, répond aux deux.

**L'unité.** *Un thème = un dossier = une note vivante = un système de données autonome.* Un
thème est tout ce que vous pensez comme un tout : une carrière, votre santé, un manuscrit, un
voyage. Il a un dossier, désigné par un seul nom court : en son centre, une **note** qui
contient tout ce qui est vivant (actions, contexte, idées, brouillons entrants), aussi
complète que possible, et à côté d'elle `files/` pour les ressources gardées telles quelles.
Une note par thème, jamais deux. « Autonome » veut dire
autonome par **domaine**, pas par **capacité** : ce qui est commun à tous les thèmes vit une
seule fois, à la racine.

**Votre vrai harnais, c'est le dossier.** Le programme qui fait tourner un modèle est un
*moteur* interchangeable ; la partie qui mérite d'être conçue est le dossier, avec son fichier
d'entrée, ses règles, ses compétences et ses notes distillées. L'ordre que pose le manuscrit :
le contexte et les compétences comptent plus que le moteur, et le moteur compte plus que le
modèle.

**Vous agencez, l'agent distille.** La division du travail suit la ligne entre ce qui est
personnel et ce qui ne l'est pas. **L'humain fait quatre choses : capturer, agencer, décider,
supprimer.** La façon dont une vie est découpée en thèmes, et l'emplacement de ces thèmes,
sont une carte de la façon dont une personne pense : la personne crée, déplace, regroupe et
élague des dossiers aussi souvent qu'elle le veut. L'agent ne déplace jamais rien de son
propre chef ; il traite chaque agencement comme intentionnel, retrouve chaque note par son nom
où qu'elle soit désormais, et tient à jour sa propre image de l'arborescence. **L'agent fait le
reste : distiller, recycler, dédoublonner, vérifier**, par une seule boucle : capturer,
qualifier, loger, propager, élaguer, vérifier.

**L'élagage, une opération à part entière.** Le texte est coupé, pas copié : tout ce que
l'humain a écrit ne quitte une note qu'après qu'un script l'a retrouvé, mot pour mot, dans un
seul `trash.md` pour toute la racine. Les fichiers partent entiers vers la corbeille ; l'agent
ne supprime que les doublons prouvés et les fichiers texte vérifiés mot pour mot dans une note,
et l'humain vide la corbeille. **Vérifier, ne pas journaliser** : ni manifestes ni journaux
d'exécution, mais une vérification avant chaque retrait et une contre-vérification avant la
suppression de toute sauvegarde. Les distillations volumineuses ou sensibles sont relues par
un agent neuf, par échantillonnage quand elles sont très volumineuses. Deux propriétés rendent
le résultat vérifiable :
la **traçabilité** (chaque source peut être suivie jusqu'à sa destination) et la
**convergence** (lancer deux fois la même passe ne produit rien la seconde fois).

**Capitalisation, portabilité et longévité.** Le travail est produit à l'intérieur du thème et
nourrit en retour son contexte, et tout est un fichier ordinaire : changer d'outil devient un
changement de pointeur plutôt qu'une migration.

**Une troisième génération du second cerveau.** La méthode se présente comme une contribution
à la lignée de *Getting Things Done* de David Allen et de *Building a Second Brain* de Tiago
Forte, avec sa structure PARA (Projets, Domaines, Ressources, Archives), et non comme une
rupture avec elle : chaque idée antérieure survit, et ce qui change, c'est qui la met en
œuvre. De PARA, elle garde le classement selon l'actionnabilité, mais **le statut est une
propriété de la note, jamais un emplacement** (active, area, archived) : l'emplacement d'un
dossier de thème est le choix de la personne, rien de ce sur quoi un agent s'appuie n'est
encodé dans un chemin, et la méthode désencombre au lieu d'accumuler.

**Architecture (partie III).**

- *La couche racine* : un seul `AGENTS.md`, `USER.md` (la personne), toutes les compétences
  dans `.agents/skills/`, les dossiers propres à l'humain `0-dashboard/` et `1-inbox/` (hors
  de portée des agents), les dossiers de thème regroupés comme la personne le veut
  (`<name>/<name>.md` et `files/`), et `9-trash/`.
- *La note de projet* : quatre sections (Actions, Context, Ideas, Incoming, toujours en
  dernier) et un `status:` dans son en-tête ; un seul fichier Markdown vivant au-dessus d'un
  corpus de matière statique, aussi complet que possible, où les fichiers de contexte isolés
  sont réintégrés.
- *Lire une note par tranches* : **l'adressabilité plutôt que le nombre de fichiers**, avec des
  statuts visibles (la décision de l'humain, une hypothèse, une suggestion d'un assistant) et
  des orientations plutôt que des règles.
- *Permissions et garanties* : un court tableau des droits de l'agent, et une échelle des
  garanties, de la plus souple à la plus ferme (relais, inscription, injection, mécanisme).
  **La mémoire du moteur est un cache.**
- *Une maintenance sans dérive* : une seule compétence `declutter`, dont la routine est de
  vider la section Incoming d'une note dans Actions, Context et Ideas, et de se remettre à jour
  après que la personne a réagencé l'arborescence, les vérifications mécaniques étant laissées
  à un petit script.
- *Protection de la vie privée dès la conception* : le périmètre de lecture, ce que couvre et
  ne couvre pas un engagement de zéro conservation des données, les copies stockées comme risque à long
  terme, le chiffrement au repos pour les thèmes sensibles.
- *Archétypes de pile logicielle : en prendre, en laisser* : des exemples d'outils datés et
  facultatifs, chacun choisi parce qu'il incarne l'un des principes.

**Rester à jour (partie IV, datée de septembre 2026).** Des principes pour choisir modèles et
moteurs sans migration permanente (le poids du harnais comme curseur, « la salle de réflexion »
et « l'atelier », le dernier modèle de pointe à faible effort comme choix par défaut), des
bancs d'essai pour le travail intellectuel, l'accès et la conservation des données, la mise en
cache des prompts, et les déclencheurs pour mettre le cadre à jour.

**Démarrage rapide (partie V) et annexe A.** Un `AGENTS.md` à la racine, un seul prompt
d'amorçage, une seule compétence (`declutter`) pour tout le flux de travail, six prompts
déclencheurs, et une spécification d'une page de la note de projet, avec un exemple fictif.

**Approches voisines et limites.** La section 2.10 situe la méthode par rapport aux conventions
de fichier d'entrée, aux mémoires intégrées des assistants, aux serveurs de mémoire, à la
recherche par plongements et à l'ingénierie du contexte, et dit où s'arrête le modèle de la
note unique. Une section finale énumère ce qui n'est pas encore connu.

---

## Comment le lire

- **L'argument** : les parties I et II (le problème, puis la solution).
- **La spécification** : la partie III et l'annexe A. Les parties I à III et l'annexe A sont
  faites pour changer rarement.
- **Les conseils datés** : la partie IV et la section 3.7, révisées quand les modèles, les
  fournisseurs ou les bancs d'essai changent.
- **Pour l'essayer** : la partie V, puis l'annexe A. Les gabarits sont volontairement
  simples ; le système est censé les affiner à partir de votre propre contexte. Lancez
  d'abord le prompt d'amorçage sur une copie.

Le manuscrit distingue trois niveaux d'appui et dit lequel s'applique là où cela compte :
*validé par* des preuves directes sur les modèles de langage et les agents, *compatible avec*
des résultats des sciences cognitives (employés comme analogies), et *jugement d'ingénieur*.
Les sources sont données en notes de bas de page et ont été vérifiées pour la dernière fois le
29 septembre 2026.

## Organisation du dépôt

```text
self-contained-harness/
├── README.md                        this page
├── the-self-contained-harness.md    the manuscript (single file, GitHub-flavoured Markdown)
├── references/bibliography.md       the sources, labelled by level of support
├── LICENSE                          CC BY 4.0 (text)
├── LICENSE-CC0                      CC0 1.0 (Appendix A and Part V templates)
└── CITATION.cff                     citation metadata
```

## Commentaires

Les commentaires sont bienvenus : ouvrez un ticket sur
[ce dépôt](https://github.com/SimonKreis/self-contained-harness/issues).
Les corrections portant sur les sources et les faits datés (partie IV, section 3.7) sont
particulièrement utiles, tout comme les retours de quiconque essaie la méthode sur un vrai
dossier.

## Licence

- **Texte** : Creative Commons Attribution 4.0 International (CC BY 4.0).
- **L'annexe A et les gabarits, prompts et compétences de la partie V** : CC0 1.0 (dédicace au
  domaine public).

Voir `LICENSE` et `LICENSE-CC0`.

## Citation

```bibtex
@misc{kreis2026harness,
  author       = {Kreis, Simon and Claude},
  title        = {The Self-Contained Harness: One Theme, One Folder, One Living Note},
  year         = {2026},
  note         = {Draft, work in progress. Made with AI, mainly Claude (Anthropic)},
  howpublished = {\url{https://github.com/SimonKreis/self-contained-harness}}
}
```

Texte brut : Kreis, S., & Claude (2026). *Le harnais autonome : un thème, un dossier,
une note vivante* (version provisoire).
<https://github.com/SimonKreis/self-contained-harness>

GitHub propose aussi un bouton « Cite this repository », généré à partir de `CITATION.cff`.

Contact : Simon Kreis, M. Sc., [simon@kreisconsulting.ca](mailto:simon@kreisconsulting.ca).
