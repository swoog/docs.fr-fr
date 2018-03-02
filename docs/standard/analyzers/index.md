---
title: Les analyseurs de Roslyn - .NET
description: "En savoir plus sur les analyseurs de Roslyn capables de détecter les problèmes et de suggérer des correctifs pour les résoudre."
keywords: .NET, .NET Core
author: billwagner
ms.author: billwagner
ms.date: 01/24/2018
ms.topic: article
ms.prod: .net
ms.technology: dotnet-standard
ms.devlang: dotnet
ms.openlocfilehash: 8c6524716ba403bc426df8dc33e64b8b2934d3d7
ms.sourcegitcommit: 3a96c706e4dbb4667bf3bf37edac9e1666646f93
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2018
---
# <a name="the-roslyn-based-analyzers"></a><span data-ttu-id="8b0f6-104">Les analyseurs de Roslyn</span><span class="sxs-lookup"><span data-stu-id="8b0f6-104">The Roslyn based Analyzers</span></span>

<span data-ttu-id="8b0f6-105">Les analyseurs de Roslyn utilisent le Kit de développement logiciel du compilateur .NET (API Roslyn) pour analyser le code source de votre projet pour détecter les problèmes et suggérer des corrections.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-105">Roslyn-based analyzers use the .NET Compiler SDK (Roslyn APIs) to analyze your project's source code to find issues and suggest corrections.</span></span> <span data-ttu-id="8b0f6-106">Différents analyseurs recherchent différentes classes de problèmes, allant des pratiques susceptibles de provoquer des bogues à des problèmes de sécurité liés à la compatibilité avec les API.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-106">Different analyzers look for different classes of issues, ranging from practices that are likely to cause bugs to security concerns to API compatibility.</span></span>

<span data-ttu-id="8b0f6-107">Les analyseurs de Roslyn fonctionnent à la fois et de manière interactive pendant les builds.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-107">Roslyn-based analyzers work both interactively and during builds.</span></span> <span data-ttu-id="8b0f6-108">L’analyseur guide de différentes façons dans Visual Studio ou dans les builds de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-108">The analyzer provides different guidance when in Visual Studio or in command-line builds.</span></span>

<span data-ttu-id="8b0f6-109">Lorsque vous modifiez le code dans Visual Studio, les analyseurs s’exécutent au moment de l’apport des modifications, interceptant d’éventuels problèmes dès que vous créez le code qui déclenche des problèmes.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-109">While you edit code in Visual Studio, the analyzers run as you make changes, catching possible issues as soon as you create code that trigger concerns.</span></span> <span data-ttu-id="8b0f6-110">Les problèmes sont mis en surbrillance avec des tildes en-dessous.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-110">Any issues are highlighted with squiggles under any issue.</span></span> <span data-ttu-id="8b0f6-111">Visual Studio affiche une ampoule et lorsque vous cliquez dessus l’analyseur propose des solutions possibles à ce problème.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-111">Visual Studio displays a light bulb, and when you click on it the analyzer will suggest possible fixes for that issue.</span></span> <span data-ttu-id="8b0f6-112">Lorsque vous générez le projet, dans Visual Studio ou à partir de la ligne de commande, tout le code source est analysé et l’analyseur fournit une liste complète des problèmes potentiels.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-112">When you build the project, either in Visual Studio or from the command line, all the source code is analyzed and the analyzer provides a full list of potential issues.</span></span> <span data-ttu-id="8b0f6-113">La figure suivante illustre un exemple.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-113">The following figure shows one example.</span></span>

![problèmes signalés par l’analyseur d’infrastructure](./media/framework-analyzers-2.png)

<span data-ttu-id="8b0f6-115">Les analyseurs de roslyn signalent des problèmes potentiels sous forme d’erreurs, d’avertissements ou d’informations en fonction de la gravité du problème.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-115">Roslyn-based analyzers report potential issues as errors, warnings, or information based on the severity of the issue.</span></span>

<span data-ttu-id="8b0f6-116">Vous installez des analyseurs de Roslyn sous forme de packages NuGet dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-116">You install Roslyn-based analyzers as NuGet packages in your project.</span></span> <span data-ttu-id="8b0f6-117">Les analyseurs configurés et tous les paramètres de chaque analyseur sont restaurés et s’exécutent sur l’ordinateur d’un développeur pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-117">The configured analyzers and any settings for each analyzer are restored and run on any developer's machine for that project.</span></span>

> [!NOTE]
> <span data-ttu-id="8b0f6-118">L’expérience utilisateur des analyseurs de Roslyn est différente de celle pour les bibliothèques d’analyse du code telles que les versions plus anciennes de FxCop et les outils d’analyse de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-118">The user experience for Roslyn-based analyzers is different than that of the Code Analysis libraries like the older versions of FxCop and the security analysis tools.</span></span>  <span data-ttu-id="8b0f6-119">Vous n’avez pas besoin exécuter explicitement les analyseurs de Roslyn.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-119">You don't need to explicitly run the Roslyn-based analyzers.</span></span> <span data-ttu-id="8b0f6-120">Il est inutile d’utiliser les éléments de menu « Exécuter l’analyse du code » dans le menu « Analyser » de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-120">There's no need to use the "Run Code Analysis" menu items on the "Analyze" menu in Visual Studio.</span></span> <span data-ttu-id="8b0f6-121">Les analyseurs de Roslyn s’exécutent de façon asynchrone lorsque vous travaillez.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-121">Roslyn-based analyzers run asychronously as you work.</span></span> 

## <a name="more-information-on-specific-analyzers"></a><span data-ttu-id="8b0f6-122">En savoir plus sur les analyseurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="8b0f6-122">More information on specific analyzers</span></span>

<span data-ttu-id="8b0f6-123">Les analyseurs suivants sont couverts dans la présente section :</span><span class="sxs-lookup"><span data-stu-id="8b0f6-123">The following analyzers are covered in this section:</span></span>

<span data-ttu-id="8b0f6-124">[Analyseur d’API](api-analyzer.md) : cet analyseur examine votre code à la recherche de risques potentiels de compatibilité ou utilisations d’API déconseillées.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-124">[API Analyzer](api-analyzer.md): This analyzer examines your code for potential compatibility risks or uses of deprecated APIs.</span></span>    
<span data-ttu-id="8b0f6-125">[Analyseur d’infrastructure](framework-analyzer.md) : cet outil examine votre code pour s’assurer qu’il suit les instructions pour les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-125">[Framework Analyzer](framework-analyzer.md): This analyzer examines your code to ensure it follows the guidelines for .NET Framework applications.</span></span> <span data-ttu-id="8b0f6-126">Ces règles incluent plusieurs recommandations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8b0f6-126">These rules include several security-based recommendations.</span></span>
