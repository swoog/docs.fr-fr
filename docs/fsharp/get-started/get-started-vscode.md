---
title: 'Bien démarrer avec F # dans Visual Studio Code'
description: 'Découvrez comment utiliser F # avec Visual Studio Code et la suite de plug-in Ionide.'
ms.date: 05/28/2018
ms.openlocfilehash: e962be2796cf0d6eb90d459730659e492f864716
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192666"
---
# <a name="get-started-with-f-in-visual-studio-code"></a>Bien démarrer avec F # dans Visual Studio Code

Vous pouvez écrire F # dans [Visual Studio Code](https://code.visualstudio.com) avec la [plug-in Ionide](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp) pour obtenir une bonne expérience d’un environnement de développement intégré (IDE), multiplateforme et léger, des IntelliSense et le code de base refactorisations. Visitez [Ionide.io](http://ionide.io) pour en savoir plus sur le plug-in.

Pour commencer, assurez-vous d’avoir [F # et le plug-in Ionide correctement installé](install-fsharp.md#install-f-with-visual-studio-code).

## <a name="creating-your-first-project-with-ionide"></a>Créer votre premier projet avec Ionide

Pour créer un nouveau projet F #, ouvrez Visual Studio Code dans un nouveau dossier (vous pouvez le nommer comme vous le souhaitez).

Ensuite, ouvrez la palette de commandes (**vue > Palette de commandes**) et tapez la commande suivante :

```
> F# new project
```

Cela est alimenté par le [FORGE](https://github.com/fsharp-editing/Forge) projet.

> [!NOTE]
Si vous ne voyez pas les options de modèle, essayez d’actualiser les modèles en exécutant la commande suivante dans la Palette de commandes : `>F#: Refresh Project Templates`.

Sélectionnez « F #: nouveau projet » en appuyant sur **entrée**. Vous accédez à l’étape suivante, ce qui concerne la sélection d’un modèle de projet.

Choisir le `classlib` modèle et le positionnement **entrée**.

Ensuite, choisissez un répertoire pour créer le projet dans. Si vous laissez vide, il utilise le répertoire actif.

Enfin, nommez votre projet dans l’étape finale. F # utilise [casse Pascal](http://c2.com/cgi/wiki?PascalCase) pour les noms de projet. Cet article utilise `ClassLibraryDemo` comme nom. Une fois que vous avez entré le nom souhaité pour votre projet, appuyez sur **entrée**.

Si vous avez suivi l’étape précédente, vous devez obtenir le Visual Studio Code espace de travail sur le côté gauche apparaissent avec les éléments suivants :

1. F # projet lui-même, en dessous du `ClassLibraryDemo` dossier.
2. La structure de répertoire correct pour l’ajout de packages via [ `Paket` ](https://fsprojects.github.io/Paket/).
3. Un multiplates-générer le script avec [ `FAKE` ](https://fsharp.github.io/FAKE/).
4. Le `paket.exe` exécutable qui peut extraire les packages et résoudre les dépendances pour vous.
5. Un `.gitignore` fichier si vous souhaitez ajouter ce projet au contrôle de code source Git.

## <a name="writing-some-code"></a>Écrire du code

Ouvrez le *ClassLibraryDemo* dossier.  Vous devez voir les fichiers suivants :

1. `ClassLibraryDemo.fs`, un fichier d’implémentation F # avec une classe définie.
2. `ClassLibraryDemo.fsproj`, un fichier de projet F # est utilisé pour générer ce projet.
3. `Script.fsx`, un fichier de script F # qui charge le fichier source.
4. `paket.references`, un fichier Paket qui spécifie les dépendances du projet.

Ouvrez `Script.fsx`et ajoutez le code suivant à la fin de celle-ci :

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx)]

Cette fonction convertit un mot à un formulaire de [Pig Latin](https://en.wikipedia.org/wiki/Pig_Latin). L’étape suivante consiste à évaluer à l’aide de F # Interactive (FSI).

Mettez en surbrillance de la fonction entière (il doit être 11 lignes longues). Une fois qu’elle est mise en surbrillance, maintenez la **Alt** clé, puis appuyez sur **entrée**. Vous remarquerez une fenêtre contextuelle ci-dessous, et il doit s’afficher quelque chose comme ceci :

![Exemple de sortie de F # Interactive avec Ionide](media/getting-started-vscode/vscode-fsi.png)

Cela fait trois choses :

1. Il a démarré le processus FSI.
2. Il envoyé le code que vous avez sélectionnée sur le processus FSI.
3. Le processus FSI évalué le code que vous avez envoyé via.

Étant donné que ce que vous avez envoyé via a été un [fonction](../language-reference/functions/index.md), vous pouvez maintenant appeler cette fonction avec FSI ! Dans la fenêtre interactive, tapez la commande suivante :

```fsharp
toPigLatin "banana";;
```

Vous devez voir le résultat suivant :

```fsharp
val it : string = "ananabay"
```

À présent, essayons avec une voyelle en tant que la première lettre. Entrez les informations suivantes :

```fsharp
toPigLatin "apple";;
```

Vous devez voir le résultat suivant :

```fsharp
val it : string = "appleyay"
```

La fonction semble fonctionner comme prévu. Félicitations, que vous venez d’écrire votre première fonction F # dans Visual Studio Code et il évaluée avec FSI !

>[!NOTE]
Comme vous l’avez peut-être remarqué, les lignes dans FSI sont terminent par `;;`. Il s’agit, car FSI vous permet d’entrer plusieurs lignes. Le `;;` à la fin informe FSI lorsque le code est terminé.

## <a name="explaining-the-code"></a>Explication du code

Si vous n’êtes pas sûr de ce que le code est en fait, Voici un pas à pas.

Comme vous pouvez le voir, `toPigLatin` est une fonction qui accepte un mot comme entrée et le convertit en une représentation sous forme de Pig Latin de ce mot. Les règles pour ce sont les suivantes :

Si le premier caractère dans un mot commence par une voyelle, ajoutez « hourra » à la fin du mot. Si elle ne commence pas par une voyelle, déplacer ce premier caractère à la fin du mot et « ay » lui ajouter.

Vous avez peut-être remarqué ce qui suit dans FSI :

```fsharp
val toPigLatin : word:string -> string
```

Cela indique que `toPigLatin` est une fonction qui accepte un `string` en tant qu’entrée (appelé `word`), ainsi qu’un autre `string`. Il s’agit du [signature de type de la fonction](https://fsharpforfunandprofit.com/posts/function-signatures/), un élément fondamental de F # qui est essentiel à comprendre le code F #. Vous pouvez également constater si vous pointez sur la fonction dans Visual Studio Code.

Dans le corps de la fonction, vous remarquerez deux parties distinctes :

1. Une fonction interne, appelée `isVowel`, qui détermine si un caractère donné (`c`) est une voyelle en vérifiant si elle correspond à un des modèles fournis par le biais de [critères spéciaux](../language-reference/pattern-matching.md):

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L2-L6)]

2. Un [ `if..then..else` ](../language-reference/conditional-expressions-if-then-else.md) expression qui vérifie si le premier caractère est une voyelle et les constructions de la valeur renvoyée hors les caractères d’entrée selon que le premier caractère a été une voyelle ou non :

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L8-L11)]

Le flux de `toPigLatin` est donc :

Vérifiez si le premier caractère du mot d’entrée est une voyelle. Dans le cas, attachez « hourra » à la fin du mot. Sinon, déplacez ce premier caractère à la fin du mot et « ay » lui ajouter.

Il existe une dernière chose à noter à ce sujet : il n’existe aucune instruction explicite à retourner à partir de la fonction, contrairement à nombreux autres langages disponibles. Il s’agit comme F # est basée sur une Expression et la dernière expression dans le corps d’une fonction est la valeur de retour. Étant donné que `if..then..else` lui-même est une expression, le corps de la `then` bloc ou dans le corps de la `else` bloc s’affichera en fonction de la valeur d’entrée.

## <a name="moving-your-script-code-into-the-implementation-file"></a>Déplacement de votre code de script dans le fichier d’implémentation

Les sections précédentes de cet article démontré une première étape dans l’écriture de code F # courantes : écriture d’une fonction initiale et l’exécuter interactivement avec FSI. On parle de développement piloté par les REPL, où [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) est l’acronyme « Read-Evaluate-Print boucle ». Il est un excellent moyen de faire des essais avec des fonctionnalités jusqu'à ce que vous avez quelque chose fonctionne.

L’étape suivante dans le développement piloté par REPL consiste à déplacer le code de travail dans un fichier d’implémentation F #. Il peut ensuite être compilé par le compilateur F # dans un assembly qui peut être exécuté.

Pour commencer, ouvrez `ClassLibraryDemo.fs`.  Vous remarquerez que du code existe déjà dans. Continuer et supprimer la définition de classe, mais veillez à laisser le [ `namespace` ](../language-reference/namespaces.md) déclaration en haut.

Ensuite, créez un nouveau [ `module` ](../language-reference/modules.md) appelé `PigLatin` et copiez le `toPigLatin` fonction dedans ainsi :

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]

Ensuite, ouvrez le `Script.fsx` à nouveau de fichiers et de supprimer l’intégralité de `toPigLatin` de fonctionner, mais veillez à conserver les deux lignes suivantes dans le fichier :

```fsharp
#load "ClassLibraryDemo.fs"
open ClassLibraryDemo
```

La première ligne est nécessaire pour FSI de script pour charger `ClassLibraryDemo.fs`. La deuxième ligne est une commodité : en l’omettant est facultative, mais vous devrez taper `open ClassLibraryDemo` dans une fenêtre FSI si vous souhaitez mettre le `ToPigLatin` module dans la portée.

Ensuite, dans la fenêtre FSI, appelez la fonction avec le `PigLatin` module que vous avez défini précédemment :

```
> PigLatin.toPigLatin "banana";;
val it : string = "ananabay"
> PigLatin.toPigLatin "apple";;
val it : string = "appleyay"
```

Opération réussie Vous obtenez les mêmes résultats en tant qu’avant, mais maintenant chargé à partir d’un fichier d’implémentation F #. La principale différence ici est que les fichiers de code source F # sont compilés dans des assemblys qui peuvent être exécutées n’importe où, pas seulement dans FSI.

## <a name="summary"></a>Récapitulatif

Dans cet article, vous avez appris :

1. Comment configurer Visual Studio Code avec Ionide.
2. Comment créer votre premier projet F # avec Ionide.
3. Comment utiliser F # script pour écrire votre première fonction F # dans Ionide puis l’exécuter dans FSI.
4. Comment migrer votre code de script vers le code source F #, puis appelez ce code à partir de FSI.

Vous êtes désormais équipés pour écrire du code F # beaucoup plus à l’aide de Visual Studio Code et Ionide.

## <a name="troubleshooting"></a>Résolution des problèmes

Voici quelques façons que vous pouvez résoudre certains problèmes que vous pouvez rencontrer :

1. Pour obtenir les fonctionnalités de Ionide de modification du code, vos fichiers F # doivent être enregistrés sur disque et à l’intérieur d’un dossier qui est ouvert dans l’espace de travail Visual Studio Code.
2. Si vous avez apporté des modifications à votre système ou installé des composants requis de Ionide avec Visual Studio Code open, redémarrez Visual Studio Code.
3. Vérifiez que vous pouvez utiliser le compilateur F # et F # interactive à partir de la ligne de commande sans un chemin d’accès qualifié complet. Vous pouvez le faire en tapant `fsc` dans une ligne de commande pour le compilateur F #, et `fsi` ou `fsharpi` pour Visual F # tools sur Windows et Mono sur Mac/Linux, respectivement.
4. Si vous avez des caractères non valides dans vos répertoires de projet, Ionide peut ne pas fonctionne.  Renommez vos répertoires de projet si c’est le cas.
5. Si aucun des commandes Ionide travaillez, vérifiez votre [les combinaisons de touches Visual Studio Code](https://code.visualstudio.com/docs/customization/keybindings#_customizing-shortcuts) pour voir si vous êtes les remplaçant par inadvertance.
6. Si Ionide est rompue sur votre ordinateur et aucun d'entre eux a résolu votre problème, essayez de supprimer le `ionide-fsharp` répertoire sur votre ordinateur et réinstaller la suite de plug-in.

Ionide est un projet open source construit et géré par les membres de la Communauté F #. Veuillez signaler des problèmes et n’hésitez pas à contribuer à la [Ionide-VSCode : dépôt GitHub de FSharp](https://github.com/ionide/ionide-vscode-fsharp).

Si vous rencontrez un problème au rapport, suivez [les instructions pour obtenir les journaux à utiliser lorsque vous signalez un problème](https://github.com/ionide/ionide-vscode-fsharp#how-to-get-logs-for-debugging--issue-reporting).

Vous pouvez également demander de l’aide supplémentaire des développeurs de Ionide et de la Communauté F # dans le [Ionide Gitter canal](https://gitter.im/ionide/ionide-project).

## <a name="next-steps"></a>Étapes suivantes

Pour en savoir plus sur F # et les fonctionnalités du langage, consultez [visite guidée de F #](../tour.md).
