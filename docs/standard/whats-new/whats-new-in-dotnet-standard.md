---
title: "Nouveautés de .NET Standard"
ms.custom: updateeachrelease
ms.date: 11/08/2017
ms.prod: .net
ms.topic: article
ms.technology: dotnet-standard
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 3a5833bdfcf1e3433ea82403908e9a06a88cde27
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="whats-new-in-the-net-standard"></a><span data-ttu-id="63f9f-102">Nouveautés de .NET Standard</span><span class="sxs-lookup"><span data-stu-id="63f9f-102">What's new in the .NET Standard</span></span>

<span data-ttu-id="63f9f-103">.NET Standard est une spécification formelle qui définit un ensemble par version de l’API qui doit être disponible sur des mises en œuvre .NET conformes à cette version de la norme.</span><span class="sxs-lookup"><span data-stu-id="63f9f-103">The .NET Standard is a formal specification that defines a versioned set of APIs which must be available on .NET implementations that comply with that version of the standard.</span></span> <span data-ttu-id="63f9f-104">.NET Standard est destiné aux développeurs de bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="63f9f-104">The .NET Standard is targeted at library developers.</span></span> <span data-ttu-id="63f9f-105">Une bibliothèque qui cible une version .NET Standard peut être utilisée sur n’importe quelle implémentation .NET Framework, .NET Core ou Xamarin prenant en charge cette version de la norme.</span><span class="sxs-lookup"><span data-stu-id="63f9f-105">A library that targets a .NET Standard version can be used on any .NET Framework, .NET Core, or Xamarin implementation that supports that version of the standard.</span></span>

<span data-ttu-id="63f9f-106">La version la plus récente de .NET Standard est 2.0.</span><span class="sxs-lookup"><span data-stu-id="63f9f-106">The most recent version of the .NET Standard is 2.0.</span></span> <span data-ttu-id="63f9f-107">Elle est incluse dans le Kit SDK .NET Core 2.0 et dans Visual Studio 2017 version 15.3 avec la charge de travail .NET Core installée.</span><span class="sxs-lookup"><span data-stu-id="63f9f-107">It is included with the .NET Core 2.0 SDK, as well as with Visual Studio 2017 Version 15.3 with the .NET Core workload installed.</span></span>

## <a name="supported-net-implementations"></a><span data-ttu-id="63f9f-108">Implémentations de .NET prises en charge</span><span class="sxs-lookup"><span data-stu-id="63f9f-108">Supported .NET implementations</span></span>

<span data-ttu-id="63f9f-109">Les implémentations .NET suivantes prennent en charge la norme .NET Standard 2.0 :</span><span class="sxs-lookup"><span data-stu-id="63f9f-109">The .NET Standard 2.0 is supported by the following .NET implementations:</span></span>

- <span data-ttu-id="63f9f-110">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="63f9f-110">.NET Core 2.0</span></span>
- <span data-ttu-id="63f9f-111">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="63f9f-111">.NET Framework 4.6.1</span></span>
- <span data-ttu-id="63f9f-112">Mono 5.4</span><span class="sxs-lookup"><span data-stu-id="63f9f-112">Mono 5.4</span></span>
- <span data-ttu-id="63f9f-113">Xamarin.iOS 10.14</span><span class="sxs-lookup"><span data-stu-id="63f9f-113">Xamarin.iOS 10.14</span></span>
- <span data-ttu-id="63f9f-114">Xamarin.Mac 3.8</span><span class="sxs-lookup"><span data-stu-id="63f9f-114">Xamarin.Mac 3.8</span></span>
- <span data-ttu-id="63f9f-115">Xamarin.Android 8.0</span><span class="sxs-lookup"><span data-stu-id="63f9f-115">Xamarin.Android 8.0</span></span>
- <span data-ttu-id="63f9f-116">Plateforme Windows universelle 10.0.16299</span><span class="sxs-lookup"><span data-stu-id="63f9f-116">Universal Windows Platform 10.0.16299</span></span>

## <a name="whats-new-in-the-net-standard-20"></a><span data-ttu-id="63f9f-117">Nouveautés de .NET Standard 2.0</span><span class="sxs-lookup"><span data-stu-id="63f9f-117">What's new in the .NET Standard 2.0</span></span>
 
<span data-ttu-id="63f9f-118">.NET Standard 2.0 inclut les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="63f9f-118">The .NET Standard 2.0 includes the following new features:</span></span>

<span data-ttu-id="63f9f-119">**Un ensemble d’API beaucoup plus complet**</span><span class="sxs-lookup"><span data-stu-id="63f9f-119">**A vastly expanded set of APIs**</span></span>

<span data-ttu-id="63f9f-120">Jusqu'à la version 1.6, .NET Standard incluait un sous-ensemble d’API relativement limité.</span><span class="sxs-lookup"><span data-stu-id="63f9f-120">Through version 1.6, the .NET Standard included a comparatively small subset of APIs.</span></span> <span data-ttu-id="63f9f-121">Ce sous-ensemble excluait de nombreuses API utilisées dans .NET Framework ou Xamarin.</span><span class="sxs-lookup"><span data-stu-id="63f9f-121">Among those excluded were many APIs that were commonly used in the .NET Framework or Xamarin.</span></span> <span data-ttu-id="63f9f-122">Cela complique le développement en obligeant les développeurs à trouver des remplacements appropriés pour les API courantes lorsqu’ils développent des applications et des bibliothèques ciblant plusieurs implémentations .NET.</span><span class="sxs-lookup"><span data-stu-id="63f9f-122">This complicates development, since it requires that developers find suitable replacements for familiar APIs when they develop applications and libraries that target multiple .NET implementations.</span></span> <span data-ttu-id="63f9f-123">.NET Standard 2.0 lève cette limitation en ajoutant plus de 20 000 API supplémentaires par rapport à .NET Standard 1.6, la version précédente de la norme.</span><span class="sxs-lookup"><span data-stu-id="63f9f-123">The .NET Standard 2.0 addresses this limitation by adding over 20,000 more APIs than were available in .NET Standard 1.6, the previous version of the standard.</span></span> <span data-ttu-id="63f9f-124">Pour obtenir la liste des API ajoutées à .NET Standard 2.0, voir [.NET Standard 2.0 vs 1.6](https://raw.githubusercontent.com/dotnet/standard/master/docs/versions/netstandard2.0_diff.md).</span><span class="sxs-lookup"><span data-stu-id="63f9f-124">For a list of the APIs that have been added to the .NET Standard 2.0, see [.NET Standard 2.0 vs 1.6](https://raw.githubusercontent.com/dotnet/standard/master/docs/versions/netstandard2.0_diff.md).</span></span> 

<span data-ttu-id="63f9f-125">Voici certains des ajouts à l’espace de noms <xref:System> dans .NET Standard 2.0 :</span><span class="sxs-lookup"><span data-stu-id="63f9f-125">Some of the additions to the <xref:System> namespace in .NET Standard 2.0 include:</span></span>

- <span data-ttu-id="63f9f-126">Prise en charge de la classe <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-126">Support for the <xref:System.AppDomain> class.</span></span>
- <span data-ttu-id="63f9f-127">Meilleure prise en charge de l’utilisation de tableaux provenant d’autres membres de la classe <xref:System.Array>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-127">Better support for working with arrays from additional members in the <xref:System.Array> class.</span></span>
- <span data-ttu-id="63f9f-128">Meilleure prise en charge de l’utilisation d’attributs provenant d’autres membres de la classe <xref:System.Attribute>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-128">Better support for working with attributes from additional members in the <xref:System.Attribute> class.</span></span>
- <span data-ttu-id="63f9f-129">Meilleure prise en charge du calendrier et d’autres options de mise en forme pour les valeurs <xref:System.DateTime>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-129">Better calendar support and additional formatting options for <xref:System.DateTime> values.</span></span>
- <span data-ttu-id="63f9f-130">Ajout d’une fonctionnalité d’arrondi <xref:System.Decimal>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-130">Additional <xref:System.Decimal> rounding functionality.</span></span>
- <span data-ttu-id="63f9f-131">Ajout d’une fonctionnalité à la classe <xref:System.Environment>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-131">Additional functionality in the <xref:System.Environment> class.</span></span>
- <span data-ttu-id="63f9f-132">Meilleur contrôle du récupérateur de mémoire via la classe <xref:System.GC>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-132">Enhanced control over the garbage collector through the <xref:System.GC> class.</span></span>
- <span data-ttu-id="63f9f-133">Meilleure prise en charge de la comparaison de chaînes, de l’énumération et de la normalisation dans la classe <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-133">Enhanced support for string comparison, enumeration, and normalization in the <xref:System.String> class.</span></span>
- <span data-ttu-id="63f9f-134">Prise en charge des ajustements à l’heure d’été et des durées de transition dans les classes <xref:System.TimeZoneInfo.AdjustmentRule> et <xref:System.TimeZoneInfo.TransitionTime>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-134">Support for daylight saving adjustments and transition times in the <xref:System.TimeZoneInfo.AdjustmentRule> and <xref:System.TimeZoneInfo.TransitionTime> classes.</span></span>
- <span data-ttu-id="63f9f-135">Importante amélioration de la fonctionnalité dans la classe <xref:System.Type>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-135">Significantly enhanced functionality in the <xref:System.Type> class.</span></span>
- <span data-ttu-id="63f9f-136">Meilleure prise en charge de la désérialisation des objets d’exception par ajout d’un constructeur d’exception avec les paramètres <xref:System.Runtime.Serialization.SerializationInfo> et <xref:System.Runtime.Serialization.StreamingContext>.</span><span class="sxs-lookup"><span data-stu-id="63f9f-136">Better support for deserialization of exception objects by adding an exception constructor with <xref:System.Runtime.Serialization.SerializationInfo> and <xref:System.Runtime.Serialization.StreamingContext> parameters.</span></span>

<span data-ttu-id="63f9f-137">**Prise en charge des bibliothèques .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="63f9f-137">**Support for .NET Framework libraries**</span></span>

<span data-ttu-id="63f9f-138">La très grande majorité des bibliothèques ciblent .NET Framework plutôt que .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="63f9f-138">The overwhelming majority of libraries target the .NET Framework rather than .NET Standard.</span></span> <span data-ttu-id="63f9f-139">Toutefois, la plupart des appels dans ces bibliothèques sont dirigés vers les API incluses dans .NET Standard 2.0.</span><span class="sxs-lookup"><span data-stu-id="63f9f-139">However, most of the calls in those libraries are to APIs that are included in the .NET Standard 2.0.</span></span> <span data-ttu-id="63f9f-140">À partir de .NET Standard 2.0, vous pouvez accéder aux bibliothèques .NET Framework depuis une bibliothèque .NET Standard en utilisant un [correctif de compatibilité](https://github.com/dotnet/standard/blob/master/docs/netstandard-20/README.md#assembly-unification).</span><span class="sxs-lookup"><span data-stu-id="63f9f-140">Starting with the .NET Standard 2.0, you can access .NET Framework libraries from a .NET Standard library by using a [compatibility shim](https://github.com/dotnet/standard/blob/master/docs/netstandard-20/README.md#assembly-unification).</span></span> <span data-ttu-id="63f9f-141">Cette couche de compatibilité est transparente pour les développeurs ; vous n’avez rien à faire pour tirer parti des bibliothèques .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="63f9f-141">This compatibility layer is transparent to developers; you don't have to do anything to take advantage of .NET Framework libraries.</span></span>

<span data-ttu-id="63f9f-142">La seule condition est que les API appelées par la bibliothèque de classes .NET Framework doivent être incluses dans .NET Standard 2.0.</span><span class="sxs-lookup"><span data-stu-id="63f9f-142">The single requirement is that the APIs called by the .NET Framework class library must be included in the .NET Standard 2.0.</span></span>

<span data-ttu-id="63f9f-143">**Prise en charge de Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="63f9f-143">**Support for Visual Basic**</span></span>

<span data-ttu-id="63f9f-144">Vous pouvez désormais développer des bibliothèques .NET Standard dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="63f9f-144">You can now develop .NET Standard libraries in Visual Basic.</span></span> <span data-ttu-id="63f9f-145">Pour les développeurs Visual Basic qui utilisent Visual Studio 2017 version 15.3 ou ultérieure avec la charge de travail .NET Core installée, Visual Studio inclut désormais un modèle de bibliothèque de classe .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="63f9f-145">For Visual Basic developers using Visual Studio 2017 Version 15.3 or later with the .NET Core workload installed, Visual Studio now includes a .NET Standard Class Library template.</span></span> <span data-ttu-id="63f9f-146">Pour les développeurs Visual Basic qui utilisent d’autres outils de développement et environnements, vous pouvez utiliser la commande [dotnet new](../../core/tools/dotnet-new.md) pour créer un projet de bibliothèque .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="63f9f-146">For Visual Basic developers who use other development tools and environments, you can use the [dotnet new](../../core/tools/dotnet-new.md) command to create a .NET Standard Library project.</span></span> <span data-ttu-id="63f9f-147">Pour plus d’informations, consultez [Prise en charge des outils pour les bibliothèques .NET Standard](#tooling).</span><span class="sxs-lookup"><span data-stu-id="63f9f-147">For more information, see the [Tooling support for .NET Standard libraries](#tooling).</span></span>

<span data-ttu-id="63f9f-148"><a name="tooling" />**Prise en charge des outils pour les bibliothèques .NET Standard**</span><span class="sxs-lookup"><span data-stu-id="63f9f-148"><a name="tooling" />**Tooling support for .NET Standard libraries**</span></span>

<span data-ttu-id="63f9f-149">Avec les versions .NET Core 2.0 et .NET Standard 2.0, Studio Visual 2017 et l[’interface de ligne de commande (CLI) .NET Core](../../core/tools/index.md) incluent la prise en charge des outils pour la création de bibliothèques .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="63f9f-149">With the release of .NET Core 2.0 and .NET Standard 2.0, both Visual Studio 2017 and the [.NET Core Command Line Interface (CLI)](../../core/tools/index.md) include tooling support for creating .NET Standard libraries.</span></span> 

<span data-ttu-id="63f9f-150">Si vous installez Visual Studio avec la charge de travail **Développement multiplateforme .NET Core**, vous pouvez créer un projet de bibliothèque .NET Standard 2.0 à l’aide d’un modèle de projet, comme le montre l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="63f9f-150">If you install Visual Studio with the **.NET Core cross-platform development** workload, you can create a .NET Standard 2.0 library project by using a project template, as the following figure shows.</span></span> 

# <a name="ctabcsharp"></a>[<span data-ttu-id="63f9f-151">C#</span><span class="sxs-lookup"><span data-stu-id="63f9f-151">C#</span></span>](#tab/csharp)
![Ajouter un nouveau projet de bibliothèque .NET Standard](./media/std-project-cs.png)
# <a name="visual-basictabvisual-basic"></a>[<span data-ttu-id="63f9f-153">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="63f9f-153">Visual Basic</span></span>](#tab/visual-basic)
<a name="add-new-net-standard-library-projectmediastd-project-vbpng"></a>![Ajouter un nouveau projet de bibliothèque .NET Standard](./media/std-project-vb.png)
---

<span data-ttu-id="63f9f-155">Si vous utilisez l’interface CLI .NET Core, la commande [dotnet new](../../core/tools/dotnet-new.md) suivante crée un projet de bibliothèque de classes qui cible .NET Standard 2.0.</span><span class="sxs-lookup"><span data-stu-id="63f9f-155">If you are using the .NET Core CLI, the following [dotnet new](../../core/tools/dotnet-new.md) command creates a class library project that targets the .NET Standard 2.0.</span></span>

```csharp
dotnet new classlib
```
```vb
dotnet new classlib -lang vb
```
  
## <a name="see-also"></a><span data-ttu-id="63f9f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63f9f-156">See Also</span></span>
<span data-ttu-id="63f9f-157">[.NET Standard](../net-standard.md)
[Présentation de .NET Standard](https://blogs.msdn.microsoft.com/dotnet/2016/09/26/introducing-net-standard/)</span><span class="sxs-lookup"><span data-stu-id="63f9f-157">[.NET Standard](../net-standard.md)
[Introducing .NET Standard](https://blogs.msdn.microsoft.com/dotnet/2016/09/26/introducing-net-standard/)</span></span>
