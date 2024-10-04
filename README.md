# Projet d'exercice MMI 2025

# Setup

## Dupliquer le dépôt d'exercice
> [!NOTE]
> Étapes extraites du tutorial Git pour [Dupliquer un référentiel](https://docs.github.com/fr/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo#forking-a-repository)

1. Dans le coin supérieur droit de la page, cliquez sur **Fork**.
2. Sous « Propriétaire », sélectionnez le menu déroulant et cliquez sur un propriétaire pour le dépôt dupliqué.
3. Dans le champ « Nom du dépôt », changer le nom du référentiel en suffixant par votre prénom.
4. Sélectionnez "Copier la branche **PAR DÉFAUT** uniquement".
5. Cliquez sur "**Créer une duplication**".

## Cloner le dépôt dupliqué
> [!NOTE]
> Étapes extraites du tutorial Git pour [Cloner un dépôt dupliqué](https://docs.github.com/fr/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo#cloning-your-forked-repository)

1. Sur GitHub.com, accédez à votre duplication du dépôt
2. Au-dessus de la liste des fichiers, cliquez sur Code.
3. Copiez l’URL du dépôt.
4. Ouvrez [Git Bash](https://git-scm.com/downloads)
5. Naviguez jusqu'à l’emplacement où vous voulez mettre le répertoire cloné en utilisant la [commande _cd_](https://graphite.dev/guides/change-directories-git-bash-windows)
6. Tapez git clone, puis collez l’URL que vous avez copiée précédemment.
7. Appuyez sur Entrée. Votre clone local va être créé.

## Ouvrir votre projet Unity

1. Ouvrez Unity Hub et sélectionnez l'onglet Projects dans la barre de menu à gauche
2. Appuyez sur le bouton Add en haut à droite
3. Sélectionnez le répertoire du projet
4. Cliquez sur le bouton Open et attendez l'ouverture du projet

# Premiers pas dans Unity

> [!NOTE]
> Pour plus de détails vous pouvez suivre le tutorial [ici](https://learn.unity.com/tutorial/explore-the-unity-editor-1)

## L'interface de l'éditeur
![Image d'illustration dez zones de l'éditeur](https://unity-connect-prd.storage.googleapis.com/20220606/learn/images/7fabb375-5282-4852-9ecf-d8acc254052b_EditorExplore.png)

### Scene view et Game view 
Zones de visualisation des objets 3D (**Scene**) et la vue joueur (**Game**)
> [!TIP]
> Avec le layout par défaut la Game View apparaît au même endroit. Utiliser les onglets pour naviguer.

### Hierarchy window 
Collection d’objets dans la scene.

### Project window 
Équivalent d’un explorateur de fichiers pour le projet.

### Toolbar 
Outils de navigation et de manipulation dans la scène

### Inspector window 
Panneau de configuration d’un objet sélectionné.

## Manipuler les objets 3D
![Image d'illustration des outils de transformation](https://unity-connect-prd.storage.googleapis.com/20220601/learn/images/057c859e-04d5-429a-b980-b852a80b2015_gizmos.png)

- W: Outil de déplacement, pour sélectionner et bouger un objet
- E: Outil de rotation, pour sélectionner et tourner un objet
- R: Outil de dimensionnement, pour sélection et changer la taille d'un objet

> [!TIP]
> Utilisez les raccourcis par défaut W (Move), E (Rotate), R (Scale) pour sélectionner l'outil rapidement.

Pour chacun des outils de transformation, un Gizmo apparaît qui vous permet de manipuler le GameObject le long de chaque axe spécifique. 
Lorsque vous manipulez ces contrôles, les valeurs du composant Transform changent en conséquence.

## Créer une nouvelle scène
### Scène vide
1. Ouvrez le dossier **Assets/Scenes** dans la fenêtre Project
2. Cliquez droit pour ouvrir le menu contextuel
3. Sélectionnez **Create/Scene** 
4. Nommez la scène

### Template
1. Ouvrez le menu **File / New Scene…**
2. Sélectionnez le template souhaité
3. Sauvegardez la scène ouverte

### Ajouter la nouvelle scène au build
1. Ouvrez le sous-menu **Build Settings** depuis le menu **File**
2. Glissez/déposez la nouvelle scène
> [!TIP]
> Utilisez le raccourcis Ctrl+Shift+B pour ouvrir rapidement les Build Settings

## Prefabs

Un Prefab agit comme un modèle à partir duquel vous pouvez créer de nouvelles instances préfabriquées d'un GameObject dans la scène. 
Cela vous permet de créer, configurer et stocker un GameObject complet avec tous ses composants, valeurs de propriété et enfants en tant qu'asset réutilisable.

### Créer un Prefab
> [!NOTE]
> Plus de détails dans le [manuel](https://docs.unity3d.com/Manual/CreatingPrefabs.html)

Faites glisser un GameObject de la fenêtre Hierarchy vers la fenêtre Project.
Le GameObject, ainsi que tous ses composants et enfants, deviennent un nouvel Asset dans votre fenêtre Project. 

> [!TIP]
> Ce processus de création du Prefab transforme également le GameObject d'origine en une instance du nouveau Prefab.

Les Prefabs dans la fenêtre Project sont affichés avec une vue miniature du GameObject ou l'icône Prefab en forme de cube bleu en fonction de la manière dont vous avez paramétré l'affichage.

![Image d'illustration](https://docs.unity3d.com/uploads/Main/PrefabsInProjectWindow1.png)
	
Toutes les modifications sont automatiquement répercutées dans les instances du Prefab modifié. 
Cela permet des changements à l'échelle du projet sans avoir à effectuer à plusieurs reprises la même modification sur chaque copie de l'élément.

Vous pouvez remplacer les paramètres des instances de Prefab individuelles si vous souhaitez que certaines instances d'un Prefab diffèrent des autres. 
Vous pouvez également créer des variantes de Prefab qui vous permettent de regrouper un ensemble de remplacements dans une variation significative d'un Prefab appelée Prefab Variant.

### Modifier un Prefab
> [!NOTE]
> Plus de détails dans le [manuel](https://docs.unity3d.com/Manual/EditingInPrefabMode.html)

Ouvrez-le dans le Prefab Mode en cliquant sur la flèche à droite de son nom dans la scène.
Ou en double-cliquant sur le Prefab dans la fenêtre Project.

![Image d'illustration](https://docs.unity3d.com/uploads/Main/PrefabHierarchyOpenArrow.png)

Ce mode vous permet d'afficher et de modifier le contenu du Prefab séparément de tout autre GameObject dans votre scène. 
Les modifications que vous effectuez dans le Prefab Mode affectent toutes les instances de ce Prefab.

![Image d'illustration](https://docs.unity3d.com/uploads/Main/PrefabContextVsIsolation.png)

En Prefab Mode, la vue Scene affiche une barre de navigation en haut. 
L'entrée la plus à droite correspond au Prefab actuellement ouvert. 
Utilisez la barre de navigation pour revenir aux scènes principales ou aux autresPrefabs que vous avez peut-être ouvertes en naviguant la hiérarchie.

### Prefab Variants
> [!NOTE]
> Plus de détails dans le [manuel](https://docs.unity3d.com/Manual/PrefabVariants.html)

Une variante de Prefab hérite des propriétés d'un autre Prefab, appelée la base. 
Les modifications apportés à la variante de Prefab ont priorité sur les valeurs de la base. 
Une variante de Prefab peut avoir n'importe quelle autre Prefab comme base, y compris les Prefab de modèle ou d'autres variantes de Prefab.

Les Prefab Variant sont affichées avec l'icône préfabriquée bleue décorée de flèches.

![Image d'illustration](https://docs.unity3d.com/uploads/Main/PrefabsBasicAndVariant.png)

Cliquez avec le bouton droit sur un Prefab dans la vue Project et sélectionner Create > Prefab Variant. 
Cela crée une variante du Prefab sélectionné, qui ne comporte initialement aucune substitution. 
Vous pouvez ouvrir la variante de Prefab dans le Prefab Mode pour commencer à y ajouter des substitutions.

Vous pouvez également faire glisser une instance de Prefab de la **Hierarchy** vers la fenêtre **Project**. 
Une boîte de dialogue vous demande si vous souhaitez créer un nouveau Prefab ou un Prefab Variant. 
Si vous choisissez Prefab Variant, vous obtenez une nouvelle variante basée sur l'instance de Prefab que vous avez fait glisser. 
Toutes les substitutions que vous aviez sur cette instance se trouvent désormais à l'intérieur de la nouvelle variante. 
Vous pouvez l'ouvrir dans le Prefab Mode pour ajouter des substitutions supplémentaires ou pour modifier ou supprimer des substitutions.

## Créer un nouveau script
> [!NOTE]
> Plus de détails dans le [manuel](https://docs.unity3d.com/Manual/CreatingAndUsingScripts.html)

- À partir du menu Créer en haut à gauche du panneau Projet
- À partir du menu contextuel (clic droit) Create / C# Script
- En sélectionnant Assets > Create > C# Script dans le menu principal

> [!TIP]
> Lorsque vous créez un script C# à partir de la fenêtre de projet d’Unity, il hérite automatiquement de [MonoBehaviour](https://docs.unity3d.com/Manual/class-MonoBehaviour.html) et vous fournit un template.

## Ajouter un nouveau component
> [!NOTE]
> Plus de détails dans le [manuel](https://docs.unity3d.com/Manual/UsingComponents.html)

Une fois sélectionné le GameObject
- À partir du menu Component si il s'agit d'un composant natif
- Par le Component Browser dans l'inspecteur

## Input System
> [!NOTE]
> Plus de détails dans le [manuel](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.11/manual/index.html)

Obtenir un Input directement à partir d'un périphérique d'entrée est rapide et pratique, mais nécessite un chemin distinct pour chaque type de périphérique.
Cela rend également plus difficile de modifier ultérieurement le contrôle du périphérique qui déclenche un événement spécifique dans le jeu.

À la place il est possible d'utiliser les actions comme intermédiaire entre les Inputs des périphériques et les réponses qu'ils déclenchent.
Le moyen le plus simple est d'utiliser le composant PlayerInput sur le GameObject d'un joueur. 

> [!IMPORTANT]
> Chaque PlayerInput représente un joueur différent dans le jeu.

### Modifier un asset Input Action

Pour afficher l'éditeur d'actions
- double-cliquez sur un élément .inputactions dans le navigateur de projet
- ou sélectionnez le bouton Modifier l'élément dans l'inspecteur de cet élément

L'éditeur d'actions apparaît sous la forme d'une fenêtre distincte, que vous pouvez également ancrer dans l'interface  pour ne pas avoir à accéder à l'asset systématiquement.

![Image d'illustration](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.11/manual/images/ActionsEditorCallout.png)

> [!CAUTION]
> Par défaut, Unity n'enregistre pas les modifications que vous effectuez dans l'éditeur d'actions lorsque vous enregistrez le projet.
> Pour enregistrer vos modifications, sélectionnez Save Asset dans la barre d'outils de la fenêtre.
> Ou bien activez l'enregistrement automatique en activant la case à cocher Auto Save dans la barre d'outils.








