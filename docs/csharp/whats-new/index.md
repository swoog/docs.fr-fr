---
title: Nouveautés de C# | Guide C#
description: Évolution du langage C#
ms.date: 11/13/2017
ms.assetid: 77deec51-a14d-46d4-9bb3-faf449477149
ms.openlocfilehash: b079c21ee90a797b038b96ae68123a538464c382
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50201437"
---
# <a name="whats-new-in-c"></a>Nouveautés de C# #

Cette page fournit un Guide des nouvelles fonctionnalités de chaque version majeure du langage c#. Les articles liés fournissent des informations détaillées sur les principales fonctionnalités ajoutées dans chaque version. Vous trouverez des informations sur les nouvelles fonctionnalités qui ont été publiées dans une version générale ou dans une préversion publique. L’état détaillé des fonctionnalités de langage, notamment celles prises en compte pour les versions à venir, est disponible dans le [dépôt dotnet/roslyn](https://github.com/dotnet/roslyn/blob/master/docs/Language%20Feature%20Status.md) sur GitHub.

> [!IMPORTANT]
> Le langage c# s’appuie sur des types et des méthodes présents dans une *bibliothèque standard* pour certaines des fonctionnalités. Par exemple, le traitement des exceptions. Chaque instruction ou expression`throw` est vérifiée pour s’assurer de l’objet levé est dérivé de <xref:System.Exception>. De même, chaque `catch` est vérifié pour assurer que le type intercepté est dérivé de <xref:System.Exception>. Chaque version peut ajouter de nouvelles spécifications. Pour utiliser les dernières fonctionnalités de langage dans les environnements plus anciens, vous devrez peut-être installer des bibliothèques spécifiques. Ces dépendances sont décrites dans la page pour chaque version spécifique. Pour en savoir plus, consultez les [relations entre le langage et la bibliothèque](relationships-between-language-and-library.md) pour l’arrière-plan sur cette dépendance. 

Pour utiliser les fonctionnalités les plus récentes dans une version mineure, vous devez [configurer la version du langage du compilateur](../language-reference/configure-language-version.md) et sélectionner la version.

* [C# 7.3](csharp-7-3.md) :
  - Cette page décrit les dernières fonctionnalités du langage C#. C# 7.3 est actuellement disponible dans [Visual Studio 2017 version 15.7](https://visualstudio.microsoft.com/vs/whatsnew/) et dans le kit [.NET Core 2.1 SDK 2.1.300 RC1](../../core/whats-new/index.md).
* [C# 7.2](csharp-7-2.md) :
  - Cette page décrit les fonctionnalités ajoutées dans le langage C#. C# 7.2 est actuellement disponible dans [Visual Studio 2017 version 15.5](https://visualstudio.microsoft.com/vs/whatsnew/) et dans le kit [SDK .NET Core 2.0](../../core/whats-new/index.md).
* [C# 7.1](csharp-7-1.md):
  - Cette page décrit les fonctionnalités ajoutées dans C# 7.1. Ces fonctionnalités ont été ajoutées dans [Visual Studio 2017 version 15.3](https://visualstudio.microsoft.com/vs/whatsnew/) et dans le kit [SDK .NET Core 2.0](../../core/whats-new/index.md).
* [C# 7.0](csharp-7.md) :
  - Cette page décrit les fonctionnalités ajoutées dans C# 7.0. Ces fonctionnalités ont été ajoutées dans [Visual Studio 2017](https://visualstudio.microsoft.com/vs/whatsnew/) et [.NET Core 1.0](../../core/whats-new/index.md) et versions ultérieures
* [C# 6](csharp-6.md) :
  - Cette page décrit les nouvelles fonctionnalités de C# 6. Ces fonctionnalités sont disponibles dans Visual Studio 2015 pour les développeurs Windows, et dans .NET Core 1.0 pour les développeurs s’intéressant à C# sur Mac OS et Linux.
* [Prise en charge multiplateforme](../../core/index.md) :
  - Grâce à sa prise en charge de .NET Core, C# s’exécute sur plusieurs plateformes. Si vous voulez essayer C# sur macOS ou sur une des nombreuses distributions Linux prises en charge, découvrez plus d’informations sur .NET Core.
* [Kit SDK .NET Compiler Platform](../roslyn-sdk/index.md) :
  - Le kit .NET Compiler Platform SDK vous permet d’écrire du code qui effectue une analyse statique dans du code C#. Vous pouvez utiliser ces API pour rechercher les erreurs potentielles ou les mauvaises pratiques, suggérer des correctifs et même implémenter ces correctifs.

## <a name="previous-versions"></a>Versions antérieures

Les fonctionnalités clés répertoriées ci-dessous ont été introduites dans des versions antérieures du langage C# et de Visual Studio .NET.

* Visual Studio .NET 2013 :
  - Cette version de Visual Studio incluait des correctifs de bogues, des améliorations des performances ainsi que des préversions de la plateforme de compilation .NET (« Roslyn »), aujourd’hui connue sous le nom de [.NET Compiler Platform SDK](../roslyn-sdk/index.md).
* C# 5, Visual Studio .NET 2012 :
  - `Async` / `await`, et attributs des [informations sur l’appelant](../programming-guide/concepts/caller-information.md).
* C# 4, Visual Studio .NET 2010 :
  - `Dynamic`, [arguments nommés](../programming-guide/classes-and-structs/named-and-optional-arguments.md), paramètres facultatifs, et [covariance et contravariance](../programming-guide/concepts/covariance-contravariance/index.md) génériques.
* C# 3, Visual Studio .NET 2008 :
  - Initialiseurs d’objet et de collection, expressions lambda, méthodes d’extension, types anonymes, propriétés automatiques, inférence de type `var` locale, et [Language Integrated Query (LINQ)](../programming-guide/concepts/linq/index.md).
* C# 2, Visual Studio .NET 2005 :
  - Méthodes anonymes, génériques, types Nullable, itérateurs/yield, classes `static`, variance et contravariance pour les délégués.
* C# 1.1, Visual Studio .NET 2003 :
  - Pragma `#line` et commentaires de documentation XML.
* C# 1, Visual Studio .NET 2002 :
  - Première version de [C#](../csharp.md).
