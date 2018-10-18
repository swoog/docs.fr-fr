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
# <a name="open-source-library-guidance"></a><span data-ttu-id="d175d-103">Aide sur les bibliothèques open source</span><span class="sxs-lookup"><span data-stu-id="d175d-103">Open-source library guidance</span></span>

<span data-ttu-id="d175d-104">Cette aide fournit des recommandations à l’attention des développeurs qui créent des bibliothèques .NET de qualité.</span><span class="sxs-lookup"><span data-stu-id="d175d-104">This guidance provides recommendations for developers to create high-quality .NET libraries.</span></span> <span data-ttu-id="d175d-105">Cette documentation se concentre sur le *quoi* et le *pourquoi* de la création d’une bibliothèque .NET, mais pas sur le *comment*.</span><span class="sxs-lookup"><span data-stu-id="d175d-105">This documentation focuses on the *what* and the *why* when building a .NET library, not the *how*.</span></span>

<span data-ttu-id="d175d-106">Aspects des bibliothèques .NET open source de qualité :</span><span class="sxs-lookup"><span data-stu-id="d175d-106">Aspects of high-quality open-source .NET libraries:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d175d-107">**Inclusives** - Les bonnes bibliothèques .NET s’efforcent de prendre en charge de nombreuses plateformes et applications.</span><span class="sxs-lookup"><span data-stu-id="d175d-107">**Inclusive** - Good .NET libraries strive to support many platforms and applications.</span></span>
> * <span data-ttu-id="d175d-108">**Stables** - Les bonnes bibliothèques .NET coexistent dans l’écosystème .NET en s’exécutant dans les applications créées avec de nombreuses bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="d175d-108">**Stable** - Good .NET libraries coexist in the .NET ecosystem, running in applications built with many libraries.</span></span>
> * <span data-ttu-id="d175d-109">**Conçues pour évoluer** - Les bibliothèques .NET doivent s’améliorer et évoluer au fil du temps tout en prenant en charge les utilisateurs existants.</span><span class="sxs-lookup"><span data-stu-id="d175d-109">**Designed to evolve** - .NET libraries should improve and evolve over time, while supporting existing users.</span></span>
> * <span data-ttu-id="d175d-110">**Débogables** - Les bibliothèques .NET doivent utiliser les derniers outils afin de créer une excellente expérience de débogage pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d175d-110">**Debuggable** - .NET libraries should use the latest tools to create a great debugging experience for users.</span></span>
> * <span data-ttu-id="d175d-111">**Approuvées** - Les bibliothèques .NET ont la confiance des développeurs en publiant sur NuGet à l’aide des bonnes pratiques de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d175d-111">**Trusted** - .NET libraries have developers' trust by publishing to NuGet using security best practices.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d175d-112">Bien démarrer</span><span class="sxs-lookup"><span data-stu-id="d175d-112">Get Started</span></span>](./get-started.md)

## <a name="recommendations"></a><span data-ttu-id="d175d-113">Recommandations</span><span class="sxs-lookup"><span data-stu-id="d175d-113">Recommendations</span></span>

<span data-ttu-id="d175d-114">Dans chaque article,vous verrez une liste de recommandations pour votre bibliothèque .NET, avec les libellés **À faire**, **Envisager**, **Éviter** et **À ne pas faire**.</span><span class="sxs-lookup"><span data-stu-id="d175d-114">With each article, there is a list of recommendations for your .NET library using **Do**, **Consider**, **Avoid**, and **Do not**.</span></span> <span data-ttu-id="d175d-115">Le libellé de chaque recommandation indique si celle-ci doit être suivie ou pas.</span><span class="sxs-lookup"><span data-stu-id="d175d-115">The wording of each recommendation indicates how strongly it should be followed.</span></span>

<span data-ttu-id="d175d-116">Une recommandation **À faire** doit presque toujours être suivie :</span><span class="sxs-lookup"><span data-stu-id="d175d-116">A **Do** recommendation is one that should almost always be followed:</span></span>

<span data-ttu-id="d175d-117">**✔️ À FAIRE** : Distribuer votre bibliothèque à l’aide d’un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="d175d-117">**✔️ DO** distribute your library using a NuGet package.</span></span>

<span data-ttu-id="d175d-118">En revanche, les recommandations **Envisager** doivent généralement être appliquées, mais il existe des exceptions à la règle qui sont fondées, c’est pourquoi vous ne devez pas vous inquiéter si vous ne les suivez pas :</span><span class="sxs-lookup"><span data-stu-id="d175d-118">On the other hand, **Consider** recommendations should generally be followed, but there are legitimate exceptions to the rule and you shouldn't feel bad about not following the guidance:</span></span>

<span data-ttu-id="d175d-119">**✔️ ENVISAGER** d’utiliser [SemVer 2.0.0](https://semver.org/) pour versionner votre package NuGet.</span><span class="sxs-lookup"><span data-stu-id="d175d-119">**✔️ CONSIDER** using [SemVer 2.0.0](https://semver.org/) to version your NuGet package.</span></span>

<span data-ttu-id="d175d-120">Les recommandations **Éviter** indiquent quelque chose qui n’est généralement pas une bonne idée, mais enfreindre les règles peut parfois avoir du sens :</span><span class="sxs-lookup"><span data-stu-id="d175d-120">**Avoid** recommendations are things that are generally not a good idea, but breaking the rule sometimes makes sense:</span></span>

<span data-ttu-id="d175d-121">**❌ ÉVITER** les références de package NuGet qui exigent une version précise.</span><span class="sxs-lookup"><span data-stu-id="d175d-121">**❌ AVOID** NuGet package references that demand an exact version.</span></span>

<span data-ttu-id="d175d-122">Et enfin, **À ne pas faire** désigne quelque chose que vous ne devez presque jamais faire :</span><span class="sxs-lookup"><span data-stu-id="d175d-122">And finally, **do not** indicates something you should almost never do:</span></span>

<span data-ttu-id="d175d-123">**❌ À NE PAS FAIRE** : publier les versions avec nom fort et sans nom fort de votre bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d175d-123">**❌ DO NOT** publish strong-named and non-strong-named versions of your library.</span></span> <span data-ttu-id="d175d-124">Par exemple : `Contoso.Api` et `Contoso.Api.StrongNamed`.</span><span class="sxs-lookup"><span data-stu-id="d175d-124">For example, `Contoso.Api` and `Contoso.Api.StrongNamed`.</span></span>

>[!div class="step-by-step"]
[<span data-ttu-id="d175d-125">Next</span><span class="sxs-lookup"><span data-stu-id="d175d-125">Next</span></span>](./get-started.md)
