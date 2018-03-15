---
title: Guide F#
description: "Ce guide fournit une vue d’ensemble des différents documents de formation pour F #, un langage de programmation fonctionnels qui s’exécute sur .NET."
author: jackfoxy
ms.author: phcart
ms.date: 02/28/2018
ms.topic: article
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: ea27fb37-dad1-4bd4-a3cc-4f5c70767ae9
ms.openlocfilehash: b7cf3feb5699f85bf09a47f008fdaf70ac7c8d77
ms.sourcegitcommit: 83dd5ec003e788ccb3e33f3412a7af39ae347646
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2018
---
# <a name="f-guide"></a><span data-ttu-id="7c54f-103">Guide F#</span><span class="sxs-lookup"><span data-stu-id="7c54f-103">F# Guide</span></span>

<span data-ttu-id="7c54f-104">F # est un langage de programmation fonctionnels qui s’exécute sur .NET.</span><span class="sxs-lookup"><span data-stu-id="7c54f-104">F# is a functional programming language that runs on .NET.</span></span> <span data-ttu-id="7c54f-105">Il possède également une prise en charge complète pour les objets, ce qui vous permet de blend fonctionnel et la programmation de l’objet pour les solutions pragmatiques à n’importe quel problème.</span><span class="sxs-lookup"><span data-stu-id="7c54f-105">It also has full support for objects, letting you blend functional and object programming for pragmatic solutions to any problem.</span></span>

```fsharp
open System // Get access to functionality in System namespace.

// Function: takes a name and produces a greeting.
let getGreeting name =
    sprintf "Hello, %s! Isn't F# great?" name

// Use the EntryPoint attribute to run the program.
[<EntryPoint>]
let main args =
    args                     // Use F# pipe operators to send the args into some functions.
    |> Array.map getGreeting // Turn each name into a friendly greeting.
    |> Array.iter printfn    // Print them!

    0
```

<span data-ttu-id="7c54f-106">F # est sur la productivité son cœur.</span><span class="sxs-lookup"><span data-stu-id="7c54f-106">F# is about productivity at its heart.</span></span> <span data-ttu-id="7c54f-107">La prise en charge des outils pour F # est omniprésent et complet des fonctionnalités avancées.</span><span class="sxs-lookup"><span data-stu-id="7c54f-107">The tooling support for F# is ubiquitous and full of advanced features.</span></span>

## <a name="learning-f"></a><span data-ttu-id="7c54f-108">Apprentissage de F #</span><span class="sxs-lookup"><span data-stu-id="7c54f-108">Learning F#</span></span> #

<span data-ttu-id="7c54f-109">[Visite guidée de F #](tour.md) donne une vue d’ensemble des fonctionnalités de langue principale avec un grand nombre d’exemples de code.</span><span class="sxs-lookup"><span data-stu-id="7c54f-109">[Tour of F#](tour.md) gives an overview of major language features with lots of code samples.</span></span> <span data-ttu-id="7c54f-110">Cette opération est recommandée si vous débutez en F # et que vous souhaitez faire une idée des comment fonctionne le langage.</span><span class="sxs-lookup"><span data-stu-id="7c54f-110">This is recommended if you are new to F# and want to get a feel for how the language works.</span></span>

<span data-ttu-id="7c54f-111">[Prise en main) (F # dans Visual Studio](get-started/get-started-visual-studio.md) si vous êtes sur Windows et que vous souhaitez une expérience complète de Visual Studio IDE (environnement de développement Integraded).</span><span class="sxs-lookup"><span data-stu-id="7c54f-111">[Get started with F# in Visual Studio](get-started/get-started-visual-studio.md) if you're on Windows and want the full Visual Studio IDE (Integraded Development Environment) experience.</span></span>

<span data-ttu-id="7c54f-112">[Prise en main) (F # dans Visual Studio pour Mac](get-started/get-started-with-visual-studio-for-mac.md) si vous êtes sur macOS et que vous souhaitez utiliser un IDE de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7c54f-112">[Get started with F# in Visual Studio for Mac](get-started/get-started-with-visual-studio-for-mac.md) if you're on macOS and want to use a Visual Studio IDE.</span></span>

<span data-ttu-id="7c54f-113">[Prise en main) (F # dans Visual Studio Code](get-started/get-started-vscode.md) si vous voulez un léger et inter-plateformes, et que l’expérience de fonctionnalités l’IDE.</span><span class="sxs-lookup"><span data-stu-id="7c54f-113">[Get Started with F# in Visual Studio Code](get-started/get-started-vscode.md) if you want a lightweight, cross-platform, and feature-packed IDE experience.</span></span>

<span data-ttu-id="7c54f-114">[Prise en main) (F # avec l’interface de ligne de base .NET](get-started/get-started-command-line.md) si vous souhaitez utiliser les outils de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7c54f-114">[Get started with F# with the .NET Core CLI](get-started/get-started-command-line.md) if you want to use command-line tools.</span></span>

## <a name="references"></a><span data-ttu-id="7c54f-115">Références</span><span class="sxs-lookup"><span data-stu-id="7c54f-115">References</span></span>

<span data-ttu-id="7c54f-116">[Référence du langage F #](language-reference/index.md) est la référence officielle et complète pour toutes les fonctionnalités du langage F #.</span><span class="sxs-lookup"><span data-stu-id="7c54f-116">[F# Language Reference](language-reference/index.md) is the official, comprehensive reference for all F# language features.</span></span> <span data-ttu-id="7c54f-117">Chaque article explique la syntaxe et présente des exemples de code.</span><span class="sxs-lookup"><span data-stu-id="7c54f-117">Each article explains the syntax and shows code samples.</span></span> <span data-ttu-id="7c54f-118">Vous pouvez utiliser la barre de filtre dans la table des matières pour rechercher des articles spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7c54f-118">You can use the filter bar in the table of contents to find specific articles.</span></span>

<span data-ttu-id="7c54f-119">[Référence de bibliothèque F # Core](https://msdn.microsoft.com/visualfsharpdocs/conceptual/fsharp-core-library-reference) est la référence d’API pour la bibliothèque principale F #.</span><span class="sxs-lookup"><span data-stu-id="7c54f-119">[F# Core Library Reference](https://msdn.microsoft.com/visualfsharpdocs/conceptual/fsharp-core-library-reference) is the API reference for the F# Core Library.</span></span>

## <a name="additional-guides"></a><span data-ttu-id="7c54f-120">Guides supplémentaires</span><span class="sxs-lookup"><span data-stu-id="7c54f-120">Additional guides</span></span>

<span data-ttu-id="7c54f-121">[F # et bénéfices](https://swlaschin.gitbooks.io/fsharpforfunandprofit/content/) est un livre complet et très détaillé sur l’apprentissage de F #.</span><span class="sxs-lookup"><span data-stu-id="7c54f-121">[F# for Fun and Profit](https://swlaschin.gitbooks.io/fsharpforfunandprofit/content/) is a comprehensive and very detailed book on learning F#.</span></span> <span data-ttu-id="7c54f-122">Son contenu et son auteur sont bien-aimée par la Communauté F #.</span><span class="sxs-lookup"><span data-stu-id="7c54f-122">Its contents and author are beloved by the F# community.</span></span> <span data-ttu-id="7c54f-123">La cible s’adresse principalement aux développeurs de l’arrière-plan d’une programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="7c54f-123">The target audience is primarily developers with an object oriented programming background.</span></span>

<span data-ttu-id="7c54f-124">[Wikibook programmation F #](https://en.wikibooks.org/wiki/F_Sharp_Programming) est un wikibook d’apprentissage F #.</span><span class="sxs-lookup"><span data-stu-id="7c54f-124">[F# Programming Wikibook](https://en.wikibooks.org/wiki/F_Sharp_Programming) is a wikibook about learning F#.</span></span> <span data-ttu-id="7c54f-125">Il est également un produit de la Communauté F #.</span><span class="sxs-lookup"><span data-stu-id="7c54f-125">It is also a product of the F# community.</span></span> <span data-ttu-id="7c54f-126">Le public visé est personnes qui débutent dans F #, avec un peu familiarisé avec la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="7c54f-126">The target audience is people who are new to F#, with a little bit of object oriented programming background.</span></span>

## <a name="learn-f-through-videos"></a><span data-ttu-id="7c54f-127">Apprendre F # grâce à des vidéos</span><span class="sxs-lookup"><span data-stu-id="7c54f-127">Learn F# through videos</span></span>

<span data-ttu-id="7c54f-128">[Didacticiel F # sur YouTube](https://www.youtube.com/watch?v=c7eNDJN758U) est une bonne introduction à F # à l’aide de Visual Studio, en affichant un grand nombre de bons exemples au cours de 1,5 heures.</span><span class="sxs-lookup"><span data-stu-id="7c54f-128">[F# tutorial on YouTube](https://www.youtube.com/watch?v=c7eNDJN758U) is a great introduction to F# using Visual Studio, showing lots of great examples over the course of 1.5 hours.</span></span> <span data-ttu-id="7c54f-129">Le public visé est de développeurs Visual Studio qui débutent à F #.</span><span class="sxs-lookup"><span data-stu-id="7c54f-129">The target audience is Visual Studio developers who are new to F#.</span></span>

<span data-ttu-id="7c54f-130">[Introduction à la programmation avec F #](https://www.youtube.com/watch?v=Teak30_pXHk&list=PLEoMzSkcN8oNiJ67Hd7oRGgD1d4YBxYGC) est une série vidéo qui utilise le Code de Visual Studio comme éditeur principal.</span><span class="sxs-lookup"><span data-stu-id="7c54f-130">[Introduction to Programming with F#](https://www.youtube.com/watch?v=Teak30_pXHk&list=PLEoMzSkcN8oNiJ67Hd7oRGgD1d4YBxYGC) is a great video series that uses Visual Studio Code as the main editor.</span></span> <span data-ttu-id="7c54f-131">La série de vidéos démarre à partir de rien et se termine par la création d’un jeu de vidéo RPG textuel.</span><span class="sxs-lookup"><span data-stu-id="7c54f-131">The video series starts from nothing and ends with building a text-based RPG video game.</span></span> <span data-ttu-id="7c54f-132">Le public visé est les développeurs qui préfèrent Visual Studio Code (ou un IDE léger) et qui sont nouvelles pour F #.</span><span class="sxs-lookup"><span data-stu-id="7c54f-132">The target audience is developers who prefer Visual Studio Code (or a lightweight IDE) and are new to F#.</span></span>

<span data-ttu-id="7c54f-133">[Nouveautés de Visual Studio 2017, pour F # pour les développeurs](https://www.linkedin.com/learning/what-s-new-in-visual-studio-2017-for-f-sharp-for-developers) un cours vidéo qui montre certaines des nouvelles fonctionnalités de F # dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="7c54f-133">[What's New in Visual Studio 2017 for F# For Developers](https://www.linkedin.com/learning/what-s-new-in-visual-studio-2017-for-f-sharp-for-developers) is a video course that shows some of the newer features for F# in Visual Studio 2017.</span></span> <span data-ttu-id="7c54f-134">Le public visé est de développeurs Visual Studio qui débutent à F #.</span><span class="sxs-lookup"><span data-stu-id="7c54f-134">The target audience is Visual Studio developers who are new to F#.</span></span>

## <a name="other-useful-resources"></a><span data-ttu-id="7c54f-135">Autres ressources utiles.</span><span class="sxs-lookup"><span data-stu-id="7c54f-135">Other useful resources</span></span>

<span data-ttu-id="7c54f-136">Le [site Web d’extraits de code F #](http://www.fssnip.net) contient un ensemble massif d’extraits de code montrant comment effectuer n’importe quoi en F #, allant de débutant à des extraits de code hautement avancées.</span><span class="sxs-lookup"><span data-stu-id="7c54f-136">The [F# Snippets Website](http://www.fssnip.net) contains a massive set of code snippets showing how to do just about anything in F#, ranging from absolute beginner to highly advanced snippets.</span></span>

<span data-ttu-id="7c54f-137">Le [F # Software Foundation Slack](http://fsharp.org/guides/slack/) est l’endroit idéal pour les débutants et les experts similaires, est très actifs, et possède certains meilleures F # aux programmeurs monde de disponibles pour une conversation.</span><span class="sxs-lookup"><span data-stu-id="7c54f-137">The [F# Software Foundation Slack](http://fsharp.org/guides/slack/) is a great place for beginners and experts alike, is highly active, and has some of world's best F# programmers available for a chat.</span></span> <span data-ttu-id="7c54f-138">Nous vous recommandons vivement de jointure.</span><span class="sxs-lookup"><span data-stu-id="7c54f-138">We highly recommend joining.</span></span>

## <a name="the-f-software-foundation"></a><span data-ttu-id="7c54f-139">F# Software Foundation</span><span class="sxs-lookup"><span data-stu-id="7c54f-139">The F# Software Foundation</span></span>

<span data-ttu-id="7c54f-140">Bien que Microsoft est le principal développeur du langage F # et ses outils dans Visual Studio, F # est soutenu par une base indépendante, le F # Software Foundation (FSSF).</span><span class="sxs-lookup"><span data-stu-id="7c54f-140">Although Microsoft is the primary developer of the F# language and its tools in Visual Studio, F# is also backed by an independent foundation, the F# Software Foundation (FSSF).</span></span>

<span data-ttu-id="7c54f-141">La FSSF a pour but non seulement de promouvoir, protéger et développer le langage de programmation F#, mais aussi de soutenir et d’étendre la communauté internationale et diversifiée de programmeurs F#.</span><span class="sxs-lookup"><span data-stu-id="7c54f-141">The mission of the F# Software Foundation is to promote, protect, and advance the F# programming language, and to support and facilitate the growth of a diverse and international community of F# programmers.</span></span>

<span data-ttu-id="7c54f-142">Pour en savoir plus et vous impliquer, consultez [fsharp.org](http://fsharp.org). Il est gratuit joindre, et le réseau des développeurs F # dans la base de quelque chose que vous ne souhaitez pas manquez !</span><span class="sxs-lookup"><span data-stu-id="7c54f-142">To learn more and get involved, check out [fsharp.org](http://fsharp.org). It's free to join, and the network of F# developers in the foundation is something you don't want to miss out on!</span></span>