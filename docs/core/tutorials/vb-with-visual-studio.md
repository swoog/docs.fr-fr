---
title: Application Hello World .NET Core avec Visual Basic dans Visual Studio 2017
description: Découvrez comment générer une application de console .NET Core simple avec Visual Basic à l’aide de Visual Studio 2017.
author: rpetrusha
ms.author: ronpet
ms.date: 08/07/2017
dev_langs:
- vb
ms.custom: vs-dotnet, seodec18
ms.openlocfilehash: e743cb496aca101b4594435c86e48951870cf8ef
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53170026"
---
# <a name="build-a-net-core-visual-basic-hello-world-application-in-visual-studio-2017"></a>Générer une application Hello World Visual Basic .NET Core dans Visual Studio 2017

Cette rubrique fournit une introduction pas à pas pour la création, le débogage et la publication d’une application de console .NET Core à l’aide de Visual Basic dans Visual Studio 2017. Visual Studio 2017 fournit un environnement de développement complet pour la création d’applications .NET Core. Tant que l’application n’a pas de dépendances spécifiques à la plateforme, elle peut s’exécuter sur n’importe quelle plateforme ciblée par .NET Core et sur tout système où .NET Core est installé.

## <a name="prerequisites"></a>Prérequis

[Visual Studio 2017](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs), avec la charge de travail « Développement multiplateforme .Net Core » installée. Vous pouvez développer votre application avec .NET Core 2.0.

Pour plus d’informations, consultez [Configuration requise pour .NET Core sur Windows](../../core/windows-prerequisites.md).

## <a name="a-simple-hello-world-application"></a>Une application Hello World simple

Commencez par créer une application console « Hello World » simple. Procédez comme suit :

1. Lancez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue *Nouveau projet**, sélectionnez le nœud **Visual Basic** suivi du nœud **.NET Core**. Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**. Dans la zone de texte **Nom**, tapez « HelloWorld ». Sélectionnez le bouton **OK**.

   ![Boîte de dialogue Nouveau projet avec Application console sélectionné](./media/vb-with-visual-studio/visual-studio-new-project.png)
   
1. Visual Studio utilise le modèle pour créer votre projet. Le modèle d’application console Visual Basic pour .NET Core définit automatiquement une classe, `Program`, avec une méthode unique, `Main`, qui accepte un tableau de <xref:System.String> comme argument. `Main` est le point d’entrée de l’application. Cette méthode est appelée automatiquement par le runtime lors du lancement de l’application. Tous les arguments de ligne de commande fournis au lancement de l’application sont disponibles dans le tableau *args*.

   ![Visual Studio et le nouveau projet HelloWorld](./media/vb-with-visual-studio/visual-studio-main-window.png)

   Le modèle crée une application « Hello World » simple. Il appelle la méthode <xref:System.Console.WriteLine(System.String)?displayProperty=nameWithType> pour afficher la chaîne littérale « Hello World ! » dans la fenêtre de console. En sélectionnant le bouton **HelloWorld** avec la flèche verte dans la barre d’outils, vous pouvez exécuter le programme en mode débogage. Si vous le faites, la fenêtre de console est visible seulement pendant un court intervalle de temps avant sa fermeture. Cela se produit, car la méthode `Main` se termine et l’application se termine dès que l’instruction unique de la méthode `Main` s’exécute.

1. Pour que la console ne se ferme pas d'elle-même, ajoutez le code suivant immédiatement après l’appel de la méthode <xref:System.Console.WriteLine(System.String)?displayProperty=nameWithType> :

   ```vb
   Console.Write("Press any key to continue...")
   Console.ReadKey(true)
   ```
   Ce code invite l’utilisateur à appuyer sur une touche. Le programme s'arrête lorsque l’utilisateur appuie sur une touche.

1. Dans la barre de menus, sélectionnez **Générer** > **Générer la solution**. Ceci compile votre programme en un langage intermédiaire, qui est ensuite converti en code binaire par un compilateur juste-à-temps (JIT).

1. Exécutez le programme en sélectionnant le bouton **HelloWorld** avec la flèche verte dans la barre d’outils.

   ![Fenêtre de console affichant « Hello World Press any key to continue »](./media/with-visual-studio/hello-world-console.png)

1. Appuyez sur une touche pour fermer la fenêtre de console.

## <a name="enhancing-the-hello-world-application"></a>Amélioration de l’application Hello World

Améliorez votre application pour inviter l’utilisateur à entrer son nom, et pour l’afficher avec la date et l’heure. Pour modifier et tester le programme, procédez comme suit :

1. Entrez le code Visual Basic suivant dans la fenêtre de code immédiatement après le crochet ouvrant qui suit la ligne `Sub Main(args As String())` et avant le premier crochet fermant :

   [!code-vb[GettingStarted#1](../../../samples/snippets/core/tutorials/vb-with-visual-studio/helloworld.vb#1)]

   Ce code remplace les instructions <xref:System.Console.WriteLine%2A?displayProperty=nameWithType>, <xref:System.Console.Write%2A?displayProperty=nameWithType> et <xref:System.Console.ReadKey%2A?displayProperty=nameWithType> existantes.

   ![Fichier du programme Visual Studio avec la méthode Main mise à jour](./media/vb-with-visual-studio/visual-basic-code-window.png)

   Ce code affiche « What is your name? ». dans la fenêtre de console et attend que l’utilisateur entre une chaîne suivie de la touche Entrée. Il stocke cette chaîne dans une variable nommée `name`. Elle récupère également la valeur de la propriété <xref:System.DateTime.Now?displayProperty=nameWithType>, qui contient l’heure locale actuelle et l’assigne à une variable nommée `currentDate`. Enfin, elle utilise une [chaîne interpolée](../../visual-basic/programming-guide/language-features/strings/interpolated-strings.md) pour afficher ces valeurs dans la fenêtre de console.

1. Recompilez le programme en choisissant **Build** > **Générer la solution**.

1. Exécutez le programme en mode débogage dans Visual Studio en sélectionnant la flèche verte dans la barre d’outils, en appuyant sur F5 ou en choisissant l’élément de menu **Déboguer** > **Démarrer le débogage**. Répondez à l’invite en entrant un nom et en appuyant sur la touche Entrée.

   ![Fenêtre de console avec la sortie du programme modifié](./media/with-visual-studio/hello-world-update.png)

1. Appuyez sur une touche pour fermer la fenêtre de console.

Vous avez créé et exécuté votre application. Pour développer une application professionnelle, appliquez quelques étapes supplémentaires pour rendre votre application prête à être publiée :

- Pour plus d’informations sur le débogage de votre application, consultez [Débogage de votre application C# Hello World avec Visual Studio 2017](debugging-with-visual-studio.md).

- Pour plus d’informations sur le développement et la publication d’une version distribuable de votre application, consultez [Publication de votre application C# Hello World avec Visual Studio 2017](publishing-with-visual-studio.md).

<!--
## Related topics

Instead of a console application, you can also build a class library with .NET Core and Visual Studio 2017. For a step-by-step introduction, see [Building a class library with C# and .NET Core in Visual Studio 2017](library-with-visual-studio.md).

You can also develop a .NET Core console app on Mac, Linux, and Windows by using [Visual Studio Code](https://code.visualstudio.com/), a downloadable code editor. For a step-by-step tutorial, see [Getting Started with Visual Studio Code](with-visual-studio-code.md). -->
