---
title: Présentation de C# -vous familiariser avec les outils de développement
description: Cet article constitue une introduction aux outils que vous utiliserez pour développer des applications C# et .NET sur votre ordinateur.
ms.date: 10/23/2018
ms.openlocfilehash: cf5bf68c1497bf62826656aa9cd2bd981128d3a2
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53129985"
---
# <a name="become-familiar-with-the-net-development-tools"></a><span data-ttu-id="15079-103">Vous familiariser avec les outils de développement .NET</span><span class="sxs-lookup"><span data-stu-id="15079-103">Become familiar with the .NET development tools</span></span>

<span data-ttu-id="15079-104">La première étape pour exécuter un tutoriel sur votre ordinateur consiste à configurer un environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="15079-104">The first step in running a tutorial on your machine is to set up a development environment.</span></span>
<span data-ttu-id="15079-105">La rubrique .NET [Bien démarrer en 10 minutes](https://www.microsoft.com/net/core) contient des instructions pour configurer votre environnement de développement local sur Mac, PC ou Linux.</span><span class="sxs-lookup"><span data-stu-id="15079-105">The .NET topic [Get Started in 10 minutes](https://www.microsoft.com/net/core) has instructions for setting up your local development environment on Mac, PC or Linux.</span></span>

<span data-ttu-id="15079-106">Vous pouvez aussi installer le [Kit SDK .NET Core](https://www.microsoft.com/net/download) et [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="15079-106">Alternatively, you can install the [.NET Core SDK](https://www.microsoft.com/net/download) and [Visual Studio Code](https://code.visualstudio.com/).</span></span>

## <a name="basic-application-development-flow"></a><span data-ttu-id="15079-107">Flux de développement d’une application de base</span><span class="sxs-lookup"><span data-stu-id="15079-107">Basic application development flow</span></span>

<span data-ttu-id="15079-108">Vous créez des applications à l’aide de la commande [`dotnet new`](../../../core/tools/dotnet-new.md).</span><span class="sxs-lookup"><span data-stu-id="15079-108">You'll create applications using the [`dotnet new`](../../../core/tools/dotnet-new.md) command.</span></span> <span data-ttu-id="15079-109">Cette commande génère les fichiers et ressources nécessaires pour votre application.</span><span class="sxs-lookup"><span data-stu-id="15079-109">This command generates the files and assets necessary for your application.</span></span> <span data-ttu-id="15079-110">Les tutoriels de présentation de C# utilisent tous le type d’application `console`.</span><span class="sxs-lookup"><span data-stu-id="15079-110">The introduction to C# tutorials all use the `console` application type.</span></span> <span data-ttu-id="15079-111">Une fois que vous avez les bases, vous pouvez développer d’autres types d’applications.</span><span class="sxs-lookup"><span data-stu-id="15079-111">Once you've got the basics, you can expand to other application types.</span></span>

<span data-ttu-id="15079-112">Les autres commandes que vous utiliserez sont [`dotnet build`](../../../core/tools/dotnet-build.md) pour générer le fichier exécutable et [`dotnet run`](../../../core/tools/dotnet-run.md) pour exécuter le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="15079-112">The other commands you'll use are [`dotnet build`](../../../core/tools/dotnet-build.md) to build the executable, and [`dotnet run`](../../../core/tools/dotnet-run.md) to run the executable.</span></span>

## <a name="pick-your-tutorial"></a><span data-ttu-id="15079-113">Choisir un tutoriel</span><span class="sxs-lookup"><span data-stu-id="15079-113">Pick your tutorial</span></span>

<span data-ttu-id="15079-114">Vous pouvez commencer par l’un des tutoriels suivants :</span><span class="sxs-lookup"><span data-stu-id="15079-114">You can start with any of the following tutorials:</span></span>

## <a name="numbers-in-cnumbers-in-csharp-localmd"></a>[<span data-ttu-id="15079-115">Nombres en C#</span><span class="sxs-lookup"><span data-stu-id="15079-115">Numbers in C#</span></span>](numbers-in-csharp-local.md)

<span data-ttu-id="15079-116">Dans le tutoriel [Nombres en C#](numbers-in-csharp-local.md), vous allez apprendre comment les ordinateurs stockent les nombres et comment effectuer des calculs avec différents types numériques.</span><span class="sxs-lookup"><span data-stu-id="15079-116">In the [Numbers in C#](numbers-in-csharp-local.md) tutorial, you'll learn how computers store numbers and how to perform calculations with different numeric types.</span></span> <span data-ttu-id="15079-117">Vous apprendrez les bases de l’arrondi et comment effectuer des calculs mathématiques à l’aide de C#.</span><span class="sxs-lookup"><span data-stu-id="15079-117">You'll learn the basics of rounding and how to perform mathematical calculations using C#.</span></span>

<span data-ttu-id="15079-118">Ce tutoriel part du principe que vous avez terminé la leçon [Hello world](hello-world.yml).</span><span class="sxs-lookup"><span data-stu-id="15079-118">This tutorial assumes that you have finished the [Hello world](hello-world.yml) lesson.</span></span>

## <a name="branches-and-loopsbranches-and-loops-localmd"></a>[<span data-ttu-id="15079-119">Branches et boucles</span><span class="sxs-lookup"><span data-stu-id="15079-119">Branches and loops</span></span>](branches-and-loops-local.md)

<span data-ttu-id="15079-120">Le tutoriel [Branches et boucles](branches-and-loops-local.md) explique les bases de la sélection de différents chemins d’exécution de code en fonction des valeurs stockées dans des variables.</span><span class="sxs-lookup"><span data-stu-id="15079-120">The [Branches and loops](branches-and-loops-local.md) tutorial teaches the basics of selecting different paths of code execution based on the values stored in variables.</span></span> <span data-ttu-id="15079-121">Vous allez apprendre les principes fondamentaux du flux de contrôle, sur la base duquel les programmes prennent des décisions et choisissent différentes actions.</span><span class="sxs-lookup"><span data-stu-id="15079-121">You'll learn the basics of control flow, which is the basis of how programs make decisions and choose different actions.</span></span>

<span data-ttu-id="15079-122">Ce tutoriel part du principe que vous avez fini les leçons [Hello world](hello-world.yml) et [Nombres en C#](numbers-in-csharp-local.md).</span><span class="sxs-lookup"><span data-stu-id="15079-122">This tutorial assumes that you have finished the [Hello world](hello-world.yml) and [Numbers in C#](numbers-in-csharp-local.md) lessons.</span></span>

## <a name="string-interpolationinterpolated-strings-localmd"></a>[<span data-ttu-id="15079-123">Interpolation de chaîne</span><span class="sxs-lookup"><span data-stu-id="15079-123">String interpolation</span></span>](interpolated-strings-local.md)

<span data-ttu-id="15079-124">Le tutoriel [Interpolation de chaîne](interpolated-strings-local.md) vous montre comment insérer des valeurs dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="15079-124">The [String interpolation](interpolated-strings-local.md) tutorial shows you how to insert values into a string.</span></span> <span data-ttu-id="15079-125">Vous allez apprendre à créer une chaîne interpolée avec des expressions C# incorporées et à contrôler la mise en forme de la chaîne de résultat.</span><span class="sxs-lookup"><span data-stu-id="15079-125">You'll learn how to create an interpolated string with embedded C# expressions and how to control the formatting of the result string.</span></span>

<span data-ttu-id="15079-126">Ce tutoriel part du principe que vous avez fini les leçons [Hello world](hello-world.yml), [Nombres en C#](numbers-in-csharp-local.md) et [Branches et boucles](branches-and-loops-local.md).</span><span class="sxs-lookup"><span data-stu-id="15079-126">This tutorial assumes that you have finished the [Hello world](hello-world.yml), [Numbers in C#](numbers-in-csharp-local.md), and [Branches and loops](branches-and-loops-local.md) lessons.</span></span>

## <a name="list-collectionarrays-and-collectionsmd"></a>[<span data-ttu-id="15079-127">Collection de listes</span><span class="sxs-lookup"><span data-stu-id="15079-127">List collection</span></span>](arrays-and-collections.md)

<span data-ttu-id="15079-128">La leçon [Collection de listes](arrays-and-collections.md) vous présente le type Collection de listes qui stocke les séquences de données.</span><span class="sxs-lookup"><span data-stu-id="15079-128">The [List collection](arrays-and-collections.md) lesson gives you a tour of the List collection type that stores sequences of data.</span></span> <span data-ttu-id="15079-129">Vous apprendrez à ajouter et à supprimer des éléments, à rechercher des éléments et à trier des listes.</span><span class="sxs-lookup"><span data-stu-id="15079-129">You'll learn how to add and remove items, search for items, and sort the lists.</span></span> <span data-ttu-id="15079-130">Vous découvrirez différents types de listes.</span><span class="sxs-lookup"><span data-stu-id="15079-130">You'll explore different kinds of lists.</span></span> 

<span data-ttu-id="15079-131">Ce tutoriel part du principe que vous avez fini les leçons listées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="15079-131">This tutorial assumes that you have finished the lessons listed above.</span></span>

## <a name="introduction-to-classesintroduction-to-classesmd"></a>[<span data-ttu-id="15079-132">Présentation des classes</span><span class="sxs-lookup"><span data-stu-id="15079-132">Introduction to classes</span></span>](introduction-to-classes.md)

<span data-ttu-id="15079-133">Ce dernier tutoriel de présentation de C#, qui s’exécute sur votre ordinateur, fait appel à votre propre environnement de développement local et à .NET Core.</span><span class="sxs-lookup"><span data-stu-id="15079-133">This final introduction to C# tutorial is only available to run on your machine, using your own local development environment and .NET Core.</span></span>
<span data-ttu-id="15079-134">Vous allez créer une application console et voir les fonctionnalités orientées objet de base qui font partie du langage C#.</span><span class="sxs-lookup"><span data-stu-id="15079-134">You'll build a console application and see the basic object-oriented features that are part of the C# language.</span></span>
