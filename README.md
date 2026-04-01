# ATELIER NSI - Conception d'un site web en Réalité Augmentée

DEMO : https://soupollet.github.io/AtelierNSI/

Le fichier : VISUELS_ATELIER_NSI.pdf (https://github.com/SouPollet/AtelierNSI/blob/main/VISUELS_ATELIER_NSI.pdf) est un appui pour mieux comprendre visuellement chaque étape.

🚀 Atelier Découverte : De la 3D à la Réalité Augmentée (AR) dans le navigateur.

En quelques étapes simples, vous allez apprendre à modéliser un objet en 3D, le texturer avec réalisme, et le déployer sur le web pour le visualiser en AR depuis votre smartphone.

👨‍🏫 Animé par : Antoine POLLET
Fabmanager à l'IUT Nancy Charlemagne / CHARLY LAB.
Prestations AR+VR pour les entreprises, associations et artistes.

🛠️ Le Workflow 100% Web
Aucun logiciel à installer ! Notre pipeline de création se déroule entièrement dans votre navigateur grâce à ces outils gratuits :

- Modélisation ➔ [TinkerCAD] https://www.tinkercad.com/
- Dépliage UV ➔ [UV Unwrapper] https://uv-unwrapper.vercel.app/
- Textures (PBR) ➔ [AmbientCG] https://ambientcg.com/
- Assemblage ➔ [Three JS Editor] https://threejs.org/editor/
- Préparation AR ➔ [ModelViewer] https://modelviewer.dev/ 
- Hébergement ➔ [GitHub] https://github.com/  (GitHub Pages)

📝 Déroulé de la séance

1️⃣ Modéliser une pièce en 3D avec TinkerCAD
L'objectif : Prendre en main la 3D en créant une brique de LEGO, avant de passer à vos propres cas d'usage.

Création de compte : Inscrivez-vous sur TinkerCAD et découvrez l'interface de Conception 3D.

Les bases :

+ Ajouter de la matière et fusionner des formes.
+ Se déplacer et naviguer autour de son modèle.
+ Retirer de la matière (formes perçages).
+ Modifier son modèle de manière non-destructive.
+ (Optionnel) Importer un modèle 3D existant ou un fichier vectoriel SVG.
+ Export : Exportez votre pièce en 3D au format GLB (⚠️ Rappel : un objet à la fois).

2️⃣ Préparer son modèle pour le Texturing (Les UVs)
L'objectif : Comprendre comment on plaque une image 2D sur un volume 3D (ex: le motif damier sur votre brique LEGO).

Le concept d'UV : Imaginez un emballage de Père Noël en chocolat que l'on déplie pour le mettre à plat. C'est ça, le dépliage UV ! [Une photo peut aider à visualiser] https://i.redd.it/9ef5pds969ac1.jpeg

Démonstration : Rapide aperçu d'un dépliage sur Blender pour comprendre la mécanique.

À vous de jouer :

Rendez-vous sur le site [UV Unwrapper]([url](https://uv-unwrapper.vercel.app/)).

Importez votre modèle et générez vos UVs automatiquement.

3️⃣ Texturer son modèle (Le PBR)
L'objectif : Transformer votre brique en bois, en métal, en roche ou en marbre.

Comprendre les textures PBR (Physically Based Rendering) :
- 🎨 Color (Albedo) : La couleur de base peinte sur le modèle.
- 👻 Alpha : La transparence du modèle.
- 🪨 Roughness : La rugosité (de parfaitement mat à ultra-brillant).
- ⚙️ Metallic : L'objet est-il conducteur (métal avec reflets purs) ou diélectrique (plastique/bois) ?
- 🌄 NormalMap : Illusion de relief (réflexion de la lumière truquée).
- 🏔️ DisplacementMap : Véritable relief (déforme réellement la géométrie selon les valeurs noir/blanc).
- 🌑 Ambient Occlusion (AO) : Assombrit les zones inaccessibles à la lumière (creux, interstices).

L'assemblage :

Téléchargez vos matériaux sur AmbientCG.
Ouvrez Three JS Editor et importez votre modèle.
Appliquez une homothétie (Scale 50, 50, 50) pour mettre à l'échelle.
Appliquez vos textures. N'hésitez pas à dupliquer votre objet pour lui assigner différents matériaux.
Exportez le résultat final au format .GLB.

4️⃣ Préparer le module AR
L'objectif : Rendre le modèle interactif et prêt pour la Réalité Augmentée.

Rendez-vous sur ModelViewer (onglet Editor).
Cliquez sur "Select a model" et importez votre fichier .GLB.
Vérifiez que tout s'affiche correctement.

Ajoutez de la vie :
Configurez l'environnement (Environment map).
Ajoutez des points d'intérêts (Hotspots).
Activez la rotation automatique (Auto-rotate).

Téléchargez/Enregistrez le dossier du site web généré.

5️⃣ Publier sur le web
L'objectif : Mettre votre création en ligne gratuitement pour la scanner avec votre smartphone.

Créez un compte sur GitHub.
Créez un nouveau Repository (dépôt public).
Cliquez sur "Upload new files" et glissez-déposez tous les fichiers du dossier ModelViewer.

🛠️ Corrections de code nécessaires (Bug fix) :

Ouvrez le fichier index.html.
Mettez à jour la version du script ModelViewer. (Retournez sur le site de Modelviewer, copiez la balise <script type="module" src="..."></script> et remplacez l'ancienne dans votre code). Sauvegardez.
Ouvrez le fichier styles.css. Changez la valeur de la hauteur (Height) du model-viewer de 90% à 100%. Sauvegardez.

🌐 Mise en ligne avec GitHub Pages :

Allez dans Settings > Pages.
Sous Branch, choisissez main (ou master) et sauvegardez.
Allez dans l'onglet Actions pour voir la progression de la mise en ligne.
Retournez dans Settings > Pages au bout de quelques minutes pour récupérer le lien de votre site web !

💡 Astuce sur index.html : Sur le web, c'est le fichier lu par défaut à la racine d'un site. Ne gardez qu'un seul fichier portant ce nom. Pour gérer plusieurs modèles, renommez vos pages (ex: lego.html) et créez un index.html qui servira de menu de redirection.

🚀 Pour aller plus loin...
L'AR et la 3D vous passionnent ? Voici de quoi poursuivre l'aventure :

📥 Trouver des modèles 3D :

Sketchfab
Thingiverse (Fonctionne aussi pour l'impression 3D)

🛠️ Logiciels de modélisation avancés :

Classiques/Pros : Blender, Fusion 360, OpenSCAD.
Web & Accessibles : Spline, Womp.

🤖 Génération 3D par Intelligence Artificielle :

Fast3D, MeshyAI, Hunyuan3D.

🌌 Créer des expériences complètes (Moteurs & Frameworks) :

Web : Three.js, Babylon.js, Spline, Spatial.io.
Moteurs de jeu professionnels : Godot Engine, Unity, Unreal Engine.

✉️ Me contacter : 
antoine.pollet@univ-lorraine.fr
