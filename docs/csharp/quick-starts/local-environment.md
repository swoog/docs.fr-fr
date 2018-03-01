---
title: "Didacticiel sur l’environnement local - Guides de démarrage rapide local en C#"
description: "Ce guide de démarrage rapide fournit les notions de base pour exécuter des démarrages rapides localement"
author: billwagner
ms.topic: article
ms.date: 12/07/2017
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.custom: mvc
ms.openlocfilehash: 9957f524e04f8ff64d4f640cf085b16cf9a2c0c6
ms.sourcegitcommit: d2da0142247ef42a219a5d2907f153e62dc6ea0d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/01/2018
---
# <a name="local-environment"></a><span data-ttu-id="61a79-103">Environnement local</span><span class="sxs-lookup"><span data-stu-id="61a79-103">Local environment</span></span>

<span data-ttu-id="61a79-104">La première étape pour tester un démarrage rapide localement consiste à configurer un environnement de développement sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="61a79-104">The first step to trying a quickstart locally is to setup a development environment on your local machine.</span></span>
<span data-ttu-id="61a79-105">La rubrique .NET [Bien démarrer en 10 minutes](https://www.microsoft.com/net/core) contient des instructions pour configurer votre environnement de développement local sur Mac, PC ou Linux.</span><span class="sxs-lookup"><span data-stu-id="61a79-105">The .NET topic [Get Started in 10 minutes](https://www.microsoft.com/net/core) has instructions for setting up your local development environment on Mac, PC or Linux.</span></span>

<span data-ttu-id="61a79-106">Vous pouvez aussi installer le [Kit SDK .NET Core](http://dot.net/core) et [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="61a79-106">Alternatively, you can install the [.NET Core SDK](http://dot.net/core) and [Visual Studio Code](https://code.visualstudio.com/).</span></span>

## <a name="basic-application-development-flow"></a><span data-ttu-id="61a79-107">Flux de développement d’une application de base</span><span class="sxs-lookup"><span data-stu-id="61a79-107">Basic application development flow</span></span>

<span data-ttu-id="61a79-108">Vous créez des applications à l’aide de la commande [`dotnet new`](../../core/tools/dotnet-new.md).</span><span class="sxs-lookup"><span data-stu-id="61a79-108">You'll create applications using the [`dotnet new`](../../core/tools/dotnet-new.md) command.</span></span> <span data-ttu-id="61a79-109">Cette commande génère les fichiers et ressources nécessaires pour votre application.</span><span class="sxs-lookup"><span data-stu-id="61a79-109">This command generates the files and assets necessary for your application.</span></span> <span data-ttu-id="61a79-110">Les démarrages rapides utilisent le type d’application `console`.</span><span class="sxs-lookup"><span data-stu-id="61a79-110">The quickstarts all use the `console` application type.</span></span>

<span data-ttu-id="61a79-111">Les autres commandes que vous utiliserez sont [`dotnet build`](../../core/tools/dotnet-build.md) pour générer le fichier exécutable et [`dotnet run`](../../core/tools/dotnet-run.md) pour exécuter le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="61a79-111">The other commands you'll use are [`dotnet build`](../../core/tools/dotnet-build.md) to build the executable, and [`dotnet run`](../../core/tools/dotnet-run.md) to run the executable.</span></span>

## <a name="pick-your-quickstart"></a><span data-ttu-id="61a79-112">Choisir le démarrage rapide</span><span class="sxs-lookup"><span data-stu-id="61a79-112">Pick your quickstart</span></span>

<span data-ttu-id="61a79-113">Vous pouvez commencer par l’un des guides de démarrage rapide suivants :</span><span class="sxs-lookup"><span data-stu-id="61a79-113">You can start with any of the following quickstarts:</span></span>

## <a name="numbers-in-cnumbers-in-csharp-localmd"></a>[<span data-ttu-id="61a79-114">Nombres en C#</span><span class="sxs-lookup"><span data-stu-id="61a79-114">Numbers in C#</span></span>](numbers-in-csharp-local.md)

<span data-ttu-id="61a79-115">Dans le guide de démarrage rapide [Nombres en C#](numbers-in-csharp-local.md), vous allez apprendre comment les ordinateurs stockent les nombres et comment effectuer des calculs avec différents types numériques.</span><span class="sxs-lookup"><span data-stu-id="61a79-115">In the [Numbers in C#](numbers-in-csharp-local.md) quickstart, you'll learn how computers store numbers and how to perform calculations with different numeric types.</span></span> <span data-ttu-id="61a79-116">Vous apprendrez les bases de l’arrondi et comment effectuer des calculs mathématiques à l’aide de C#.</span><span class="sxs-lookup"><span data-stu-id="61a79-116">You'll learn the basics of rounding, and how to perform mathematical calculations using C#.</span></span> 

<span data-ttu-id="61a79-117">Ce guide de démarrage rapide part du principe que vous avez terminé le didacticiel [Hello world](hello-world.yml).</span><span class="sxs-lookup"><span data-stu-id="61a79-117">This quickstart assumes that you have finished the [Hello world](hello-world.yml) tutorial.</span></span>

## <a name="branches-and-loopsbranches-and-loops-localmd"></a>[<span data-ttu-id="61a79-118">Branches et boucles</span><span class="sxs-lookup"><span data-stu-id="61a79-118">Branches and loops</span></span>](branches-and-loops-local.md)

<span data-ttu-id="61a79-119">Le guide de démarrage rapide [Branches et boucles](branches-and-loops-local.md) explique les bases de la sélection de différents chemins d’exécution de code en fonction des valeurs stockées dans des variables.</span><span class="sxs-lookup"><span data-stu-id="61a79-119">The [Branches and loops](branches-and-loops-local.md) quickstart teaches the basics of selecting different paths of code execution based on the values stored in variables.</span></span> <span data-ttu-id="61a79-120">Vous allez apprendre les principes fondamentaux du flux de contrôle, sur la base duquel les programmes prennent des décisions et choisissent différentes actions.</span><span class="sxs-lookup"><span data-stu-id="61a79-120">You'll learn the basics of control flow, which is the basis of how programs make decisions and choose different actions.</span></span> 

<span data-ttu-id="61a79-121">Cette leçon prend pour acquis que vous avez terminé les leçons [Hello World](hello-world.yml) et [Nombres en C#](numbers-in-csharp-local.md).</span><span class="sxs-lookup"><span data-stu-id="61a79-121">This beginning lesson assumes that you have finished the [Hello World](hello-world.yml) and [Numbers in C#](numbers-in-csharp-local.md) lessons.</span></span>

## <a name="list-collectionarrays-and-collectionsmd"></a>[<span data-ttu-id="61a79-122">Collection de listes</span><span class="sxs-lookup"><span data-stu-id="61a79-122">List collection</span></span>](arrays-and-collections.md)

<span data-ttu-id="61a79-123">La leçon [Collection de listes](arrays-and-collections.md) vous présente le type Collection de listes qui stocke les séquences de données.</span><span class="sxs-lookup"><span data-stu-id="61a79-123">The [List collection](arrays-and-collections.md) lesson gives you a tour of the List collection type that stores sequences of data.</span></span> <span data-ttu-id="61a79-124">Vous apprendrez à ajouter et à supprimer des éléments, à rechercher des éléments et à trier des listes.</span><span class="sxs-lookup"><span data-stu-id="61a79-124">You'll learn how to add and remove items, search for items, and sort the lists.</span></span> <span data-ttu-id="61a79-125">Vous découvrirez différents types de listes.</span><span class="sxs-lookup"><span data-stu-id="61a79-125">You'll explore different kinds of lists.</span></span> 

<span data-ttu-id="61a79-126">Ce guide de démarrage rapide prend pour acquis que vous avez terminé les guides de démarrage rapide répertoriés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="61a79-126">This beginning quickstart assumes that you have finished the quickstarts listed above.</span></span>

## <a name="introduction-to-classesintroduction-to-classesmd"></a>[<span data-ttu-id="61a79-127">Présentation des classes</span><span class="sxs-lookup"><span data-stu-id="61a79-127">Introduction to classes</span></span>](introduction-to-classes.md)

<span data-ttu-id="61a79-128">Ce dernier guide de démarrage rapide, qui s’exécute sur votre ordinateur, fait appel à votre propre environnement de développement local et à .NET Core.</span><span class="sxs-lookup"><span data-stu-id="61a79-128">This final quickstart is only available to run on your machine, using your own local development environment and .NET Core.</span></span>
<span data-ttu-id="61a79-129">Vous allez créer une application console et voir les fonctionnalités orientées objet de base qui font partie du langage C#.</span><span class="sxs-lookup"><span data-stu-id="61a79-129">You'll build a console application and see the basic object-oriented features that are part of the C# language.</span></span>
