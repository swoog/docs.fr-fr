---
title: Guide F#
description: 'Ce guide fournit une vue d’ensemble des différents documents de formation pour F #, un langage de programmation fonctionnels qui s’exécute sur .NET.'
author: jackfoxy
ms.author: phcart
ms.date: 03/19/2018
ms.topic: conceptual
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 9c03148d42f3cf8731580e36990aa21c68f705f6
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="f-guide"></a>Guide F#

F # est un langage de programmation fonctionnels qui s’exécute sur .NET. Il possède également une prise en charge complète pour les objets, ce qui vous permet de blend fonctionnel et la programmation de l’objet pour les solutions pragmatiques à n’importe quel problème.

```fsharp
open System // Get access to functionality in System namespace.

// Function: takes a name and produces a greeting.
let getGreeting name =
    sprintf "Hello, %s! Isn't F# great?" name

// Use the EntryPoint attribute to run the program.
[<EntryPoint>]
let main args =
    // Define a list of names
    let names = [| "Don"; "Julia"; "Xi" |]
    
    // Print a fun greeting for each name!
    names
    |> Array.map getGreeting
    |> Array.iter (fun greeting -> printfn "%s" greeting)

    0
```

F # est sur la productivité son cœur. La prise en charge des outils pour F # est omniprésent et complet des fonctionnalités avancées.

## <a name="learning-f"></a>Apprentissage de F # #

[Visite guidée de F #](tour.md) donne une vue d’ensemble des fonctionnalités de langue principale avec un grand nombre d’exemples de code. Cette opération est recommandée si vous débutez en F # et que vous souhaitez faire une idée des comment fonctionne le langage.

[Prise en main) (F # dans Visual Studio](get-started/get-started-visual-studio.md) si vous êtes sur Windows et que vous souhaitez une expérience complète de Visual Studio IDE (environnement de développement Integraded).

[Prise en main) (F # dans Visual Studio pour Mac](get-started/get-started-with-visual-studio-for-mac.md) si vous êtes sur macOS et que vous souhaitez utiliser un IDE de Visual Studio.

[Prise en main) (F # dans Visual Studio Code](get-started/get-started-vscode.md) si vous voulez un léger et inter-plateformes, et que l’expérience de fonctionnalités l’IDE.

[Prise en main) (F # avec l’interface de ligne de base .NET](get-started/get-started-command-line.md) si vous souhaitez utiliser les outils de ligne de commande.

[Prise en main F # et Xamarin](https://docs.microsoft.com/xamarin/cross-platform/platform/fsharp/) pour la programmation mobile avec F #.

## <a name="references"></a>Références

[Référence du langage F #](language-reference/index.md) est la référence officielle et complète pour toutes les fonctionnalités du langage F #. Chaque article explique la syntaxe et présente des exemples de code. Vous pouvez utiliser la barre de filtre dans la table des matières pour rechercher des articles spécifiques.

[Référence de bibliothèque F # Core](https://msdn.microsoft.com/visualfsharpdocs/conceptual/fsharp-core-library-reference) est la référence d’API pour la bibliothèque principale F #.


## <a name="additional-guides"></a>Guides supplémentaires

[F # et bénéfices](https://swlaschin.gitbooks.io/fsharpforfunandprofit/content/) est un livre complet et très détaillé sur l’apprentissage de F #. Son contenu et son auteur sont bien-aimée par la Communauté F #. La cible s’adresse principalement aux développeurs de l’arrière-plan d’une programmation orientée objet.

[Wikibook programmation F #](https://en.wikibooks.org/wiki/F_Sharp_Programming) est un wikibook d’apprentissage F #. Il est également un produit de la Communauté F #. Le public visé est personnes qui débutent dans F #, avec un peu familiarisé avec la programmation orientée objet.

## <a name="learn-f-through-videos"></a>Apprendre F # grâce à des vidéos

[Didacticiel F # sur YouTube](https://www.youtube.com/watch?v=c7eNDJN758U) est une bonne introduction à F # à l’aide de Visual Studio, en affichant un grand nombre de bons exemples au cours de 1,5 heures. Le public visé est de développeurs Visual Studio qui débutent à F #.

[Introduction à la programmation avec F #](https://www.youtube.com/watch?v=Teak30_pXHk&list=PLEoMzSkcN8oNiJ67Hd7oRGgD1d4YBxYGC) est une série vidéo qui utilise le Code de Visual Studio comme éditeur principal. La série de vidéos démarre à partir de rien et se termine par la création d’un jeu de vidéo RPG textuel. Le public visé est les développeurs qui préfèrent Visual Studio Code (ou un IDE léger) et qui sont nouvelles pour F #.

[Nouveautés de Visual Studio 2017, pour F # pour les développeurs](https://www.linkedin.com/learning/what-s-new-in-visual-studio-2017-for-f-sharp-for-developers) un cours vidéo qui montre certaines des nouvelles fonctionnalités de F # dans Visual Studio 2017. Le public visé est de développeurs Visual Studio qui débutent à F #.

## <a name="other-useful-resources"></a>Autres ressources utiles.

Le [site Web d’extraits de code F #](http://www.fssnip.net) contient un ensemble massif d’extraits de code montrant comment effectuer n’importe quoi en F #, allant de débutant à des extraits de code hautement avancées.

Le [F # Software Foundation Slack](http://fsharp.org/guides/slack/) est l’endroit idéal pour les débutants et les experts similaires, est très actifs, et possède certains meilleures F # aux programmeurs monde de disponibles pour une conversation. Nous vous recommandons vivement de jointure.

## <a name="the-f-software-foundation"></a>F# Software Foundation

Bien que Microsoft est le principal développeur du langage F # et ses outils dans Visual Studio, F # est soutenu par une base indépendante, le F # Software Foundation (FSSF).

La FSSF a pour but non seulement de promouvoir, protéger et développer le langage de programmation F#, mais aussi de soutenir et d’étendre la communauté internationale et diversifiée de programmeurs F#.

Pour en savoir plus et vous impliquer, consultez [fsharp.org](http://fsharp.org). Il est gratuit joindre, et le réseau des développeurs F # dans la base de quelque chose que vous ne souhaitez pas manquez !
