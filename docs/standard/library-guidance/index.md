---
title: Aide sur les bibliothèques open source
description: Recommandations de bonne pratique à l’attention des développeurs qui créent des bibliothèques .NET de qualité.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 50fb745f7eb65abcaca76cebaf9991c48f559e59
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374903"
---
# <a name="open-source-library-guidance"></a>Aide sur les bibliothèques open source

Cette aide fournit des recommandations à l’attention des développeurs qui créent des bibliothèques .NET de qualité. Cette documentation se concentre sur le *quoi* et le *pourquoi* de la création d’une bibliothèque .NET, mais pas sur le *comment*.

Aspects des bibliothèques .NET open source de qualité :

> [!div class="checklist"]
> * **Inclusives** - Les bonnes bibliothèques .NET s’efforcent de prendre en charge de nombreuses plateformes et applications.
> * **Stables** - Les bonnes bibliothèques .NET coexistent dans l’écosystème .NET en s’exécutant dans les applications créées avec de nombreuses bibliothèques.
> * **Conçues pour évoluer** - Les bibliothèques .NET doivent s’améliorer et évoluer au fil du temps tout en prenant en charge les utilisateurs existants.
> * **Débogables** - Les bibliothèques .NET doivent utiliser les derniers outils afin de créer une excellente expérience de débogage pour les utilisateurs.
> * **Approuvées** - Les bibliothèques .NET ont la confiance des développeurs en publiant sur NuGet à l’aide des bonnes pratiques de sécurité.

> [!div class="nextstepaction"]
> [Bien démarrer](./get-started.md)

## <a name="recommendations"></a>Recommandations

Dans chaque article,vous verrez une liste de recommandations pour votre bibliothèque .NET, avec les libellés **À faire**, **Envisager**, **Éviter** et **À ne pas faire**. Le libellé de chaque recommandation indique si celle-ci doit être suivie ou pas.

Une recommandation **À faire** doit presque toujours être suivie :

**✔️ À FAIRE** : Distribuer votre bibliothèque à l’aide d’un package NuGet.

En revanche, les recommandations **Envisager** doivent généralement être appliquées, mais il existe des exceptions à la règle qui sont fondées, c’est pourquoi vous ne devez pas vous inquiéter si vous ne les suivez pas :

**✔️ ENVISAGER** d’utiliser [SemVer 2.0.0](https://semver.org/) pour versionner votre package NuGet.

Les recommandations **Éviter** indiquent quelque chose qui n’est généralement pas une bonne idée, mais enfreindre les règles peut parfois avoir du sens :

**❌ ÉVITER** les références de package NuGet qui exigent une version précise.

Et enfin, **À ne pas faire** désigne quelque chose que vous ne devez presque jamais faire :

**❌ À NE PAS FAIRE** : publier les versions avec nom fort et sans nom fort de votre bibliothèque. Par exemple : `Contoso.Api` et `Contoso.Api.StrongNamed`.

>[!div class="step-by-step"]
[Next](./get-started.md)
