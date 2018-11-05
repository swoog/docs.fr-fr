---
title: Présentation de C# -vous familiariser avec les outils de développement
description: Cet article constitue une introduction aux outils que vous utiliserez pour développer des applications C# et .NET sur votre ordinateur.
ms.date: 10/23/2018
ms.openlocfilehash: ec7e55fbf2a89a8ec45db956fc575edeb2283f56
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50200146"
---
# <a name="become-familiar-with-the-net-development-tools"></a>Vous familiariser avec les outils de développement .NET

La première étape pour exécuter un tutoriel sur votre ordinateur consiste à configurer un environnement de développement.
La rubrique .NET [Bien démarrer en 10 minutes](https://www.microsoft.com/net/core) contient des instructions pour configurer votre environnement de développement local sur Mac, PC ou Linux.

Vous pouvez aussi installer le [Kit SDK .NET Core](https://www.microsoft.com/net/download) et [Visual Studio Code](https://code.visualstudio.com/).

## <a name="basic-application-development-flow"></a>Flux de développement d’une application de base

Vous créez des applications à l’aide de la commande [`dotnet new`](../../../core/tools/dotnet-new.md). Cette commande génère les fichiers et ressources nécessaires pour votre application. Les tutoriels de présentation de C# utilisent tous le type d’application `console`. Une fois que vous avez les bases, vous pouvez développer d’autres types d’applications.

Les autres commandes que vous utiliserez sont [`dotnet build`](../../../core/tools/dotnet-build.md) pour générer le fichier exécutable et [`dotnet run`](../../../core/tools/dotnet-run.md) pour exécuter le fichier exécutable.

## <a name="pick-your-turorial"></a>Choisir votre turoriel

Vous pouvez commencer par l’un des tutoriels suivants :

## <a name="numbers-in-cnumbers-in-csharp-localmd"></a>[Nombres en C#](numbers-in-csharp-local.md)

Dans le tutoriel [Nombres en C#](numbers-in-csharp-local.md), vous allez apprendre comment les ordinateurs stockent les nombres et comment effectuer des calculs avec différents types numériques. Vous apprendrez les bases de l’arrondi et comment effectuer des calculs mathématiques à l’aide de C#.

Ce tutoriel part du principe que vous avez terminé la leçon [Hello world](hello-world.yml).

## <a name="branches-and-loopsbranches-and-loops-localmd"></a>[Branches et boucles](branches-and-loops-local.md)

Le tutoriel [Branches et boucles](branches-and-loops-local.md) explique les bases de la sélection de différents chemins d’exécution de code en fonction des valeurs stockées dans des variables. Vous allez apprendre les principes fondamentaux du flux de contrôle, sur la base duquel les programmes prennent des décisions et choisissent différentes actions.

Ce tutoriel part du principe que vous avez fini les leçons [Hello world](hello-world.yml) et [Nombres en C#](numbers-in-csharp-local.md).

## <a name="string-interpolationinterpolated-strings-localmd"></a>[Interpolation de chaîne](interpolated-strings-local.md)

Le tutoriel [Interpolation de chaîne](interpolated-strings-local.md) vous montre comment insérer des valeurs dans une chaîne. Vous allez apprendre à créer une chaîne interpolée avec des expressions C# incorporées et à contrôler la mise en forme de la chaîne de résultat.

Ce tutoriel part du principe que vous avez fini les leçons [Hello world](hello-world.yml), [Nombres en C#](numbers-in-csharp-local.md) et [Branches et boucles](branches-and-loops-local.md).

## <a name="list-collectionarrays-and-collectionsmd"></a>[Collection de listes](arrays-and-collections.md)

La leçon [Collection de listes](arrays-and-collections.md) vous présente le type Collection de listes qui stocke les séquences de données. Vous apprendrez à ajouter et à supprimer des éléments, à rechercher des éléments et à trier des listes. Vous découvrirez différents types de listes. 

Ce tutoriel part du principe que vous avez fini les leçons listées ci-dessus.

## <a name="introduction-to-classesintroduction-to-classesmd"></a>[Présentation des classes](introduction-to-classes.md)

Ce dernier tutoriel de présentation de C#, qui s’exécute sur votre ordinateur, fait appel à votre propre environnement de développement local et à .NET Core.
Vous allez créer une application console et voir les fonctionnalités orientées objet de base qui font partie du langage C#.
