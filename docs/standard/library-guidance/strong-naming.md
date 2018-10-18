---
title: Utilisation de noms forts et les bibliothèques .NET
description: Meilleures pratiques recommandées pour les bibliothèques .NET d’affectation de noms forts.
author: jamesnk
ms.author: mairaw
ms.date: 10/16/2018
ms.openlocfilehash: e3f7d443eb9acc84c800ea2611b803733085391c
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49372804"
---
# <a name="strong-naming"></a><span data-ttu-id="f571f-103">Affectation de noms forts</span><span class="sxs-lookup"><span data-stu-id="f571f-103">Strong naming</span></span>

<span data-ttu-id="f571f-104">Utilisation de noms forts fait référence à la signature d’un assembly avec une clé, produisant un [assembly avec nom fort](../../framework/app-domains/strong-named-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="f571f-104">Strong naming refers to signing an assembly with a key, producing a [strong-named assembly](../../framework/app-domains/strong-named-assemblies.md).</span></span> <span data-ttu-id="f571f-105">Lorsqu’un assembly est un nom fort, il crée une identité unique basée sur le numéro de version d’assembly et un nom, et il peut aider à éviter les conflits de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="f571f-105">When an assembly is strong-named, it creates a unique identity based on the name and assembly version number, and it can help prevent assembly conflicts.</span></span>

<span data-ttu-id="f571f-106">L’inconvénient de l’utilisation de noms forts est que le .NET Framework sur Windows permet strict lors du chargement des assemblys une fois qu’un assembly possède un nom fort.</span><span class="sxs-lookup"><span data-stu-id="f571f-106">The downside to strong naming is that the .NET Framework on Windows enables strict loading of assemblies once an assembly is strong named.</span></span> <span data-ttu-id="f571f-107">Une référence d’assembly avec nom fort doit correspondre exactement à la version référencée par un assembly, forcer les développeurs à [configurer des redirections de liaison](../../framework/configure-apps/redirect-assembly-versions.md) lors de l’utilisation de l’assembly :</span><span class="sxs-lookup"><span data-stu-id="f571f-107">A strong-named assembly reference must exactly match the version referenced by an assembly, forcing developers to [configure binding redirects](../../framework/configure-apps/redirect-assembly-versions.md) when using the assembly:</span></span>

```xml
<configuration>
   <runtime>
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
         <dependentAssembly>
            <assemblyIdentity name="myAssembly" publicKeyToken="32ab4ba45e0a69a1" culture="neutral" />
            <bindingRedirect oldVersion="1.0.0.0" newVersion="2.0.0.0"/>
         </dependentAssembly>
      </assemblyBinding>
   </runtime>
</configuration>
```

<span data-ttu-id="f571f-108">Lorsque les développeurs .NET se plaignent de noms forts, qu’ils sont généralement plaignent est strict chargement d’assembly.</span><span class="sxs-lookup"><span data-stu-id="f571f-108">When .NET developers complain about strong naming, what they're usually complaining about is strict assembly loading.</span></span> <span data-ttu-id="f571f-109">Heureusement, ce problème est isolé sur le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f571f-109">Fortunately, this issue is isolated to the .NET Framework.</span></span> <span data-ttu-id="f571f-110">.NET core, Xamarin, UWP et la plupart des autres implémentations .NET n’avez pas le chargement des assemblys strict et supprime le principal inconvénient des noms forts.</span><span class="sxs-lookup"><span data-stu-id="f571f-110">.NET Core, Xamarin, UWP, and most other .NET implementations don't have strict assembly loading and removes the main downside of strong naming.</span></span>

<span data-ttu-id="f571f-111">Un aspect important des noms forts est qu’il s’agit viral : un nom fort référence qu’assembly autres fort nommé assemblys.</span><span class="sxs-lookup"><span data-stu-id="f571f-111">One important aspect of strong naming is that it's viral: a strong named assembly can only reference other strong named assemblies.</span></span> <span data-ttu-id="f571f-112">Si votre bibliothèque n’est pas forte nommé, vous avez exclus des développeurs qui créent une application ou une bibliothèque qui a besoin des noms forts à partir de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="f571f-112">If your library isn't strong named, then you have excluded developers who are building an application or library that needs strong naming from using it.</span></span>

<span data-ttu-id="f571f-113">Les avantages de l’utilisation de noms forts sont :</span><span class="sxs-lookup"><span data-stu-id="f571f-113">The benefits of strong naming are:</span></span>

1. <span data-ttu-id="f571f-114">L’assembly peut être référencé et utilisé par d’autres assemblys avec nom fort.</span><span class="sxs-lookup"><span data-stu-id="f571f-114">The assembly can be referenced and used by other strong-named assemblies.</span></span>
2. <span data-ttu-id="f571f-115">L’assembly peut être stocké dans le Global Assembly Cache (GAC).</span><span class="sxs-lookup"><span data-stu-id="f571f-115">The assembly can be stored in the Global Assembly Cache (GAC).</span></span>
3. <span data-ttu-id="f571f-116">L’assembly peut être chargé côte à côte avec d’autres versions de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="f571f-116">The assembly can be loaded side by side with other versions of the assembly.</span></span> <span data-ttu-id="f571f-117">Le chargement des assemblys côte à côte sont généralement requise par les applications avec des architectures de plug-in.</span><span class="sxs-lookup"><span data-stu-id="f571f-117">Side-by-side assembly loading is commonly required by applications with plug-in architectures.</span></span>

## <a name="create-strong-named-net-libraries"></a><span data-ttu-id="f571f-118">Créer fort nommé des bibliothèques .NET</span><span class="sxs-lookup"><span data-stu-id="f571f-118">Create strong named .NET libraries</span></span>

<span data-ttu-id="f571f-119">Vous devez nommer strong vos bibliothèques de .NET open source.</span><span class="sxs-lookup"><span data-stu-id="f571f-119">You should strong name your open-source .NET libraries.</span></span> <span data-ttu-id="f571f-120">Un assembly de nom fort garantit le plupart des personnes puissent l’utiliser, et strict assembly en le chargeant uniquement affecte le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f571f-120">Strong naming an assembly ensures the most people can use it, and strict assembly loading only affects the .NET Framework.</span></span>

> [!NOTE]
> <span data-ttu-id="f571f-121">Ce guide est spécifique aux seules bibliothèques .NET distribuées publiquement, telles que les bibliothèques .NET publiés sur NuGet.org. Utilisation de noms forts n’est pas requis par la plupart des applications .NET et ne doit pas être effectuée par défaut.</span><span class="sxs-lookup"><span data-stu-id="f571f-121">This guidance is specific to publicly distributed .NET libraries, such as .NET libraries published on NuGet.org. Strong naming is not required by most .NET applications and should not be done by default.</span></span>

<span data-ttu-id="f571f-122">**ENVISAGEZ de ✔️** strong naming les assemblys de votre bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="f571f-122">**✔️ CONSIDER** strong naming your library's assemblies.</span></span>

<span data-ttu-id="f571f-123">**ENVISAGEZ de ✔️** archiver la clé utilisée pour le nom fort dans votre système de contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="f571f-123">**✔️ CONSIDER** checking in the key used to strong name into your source control system.</span></span>

> <span data-ttu-id="f571f-124">Une clé disponible publiquement permet aux développeurs de modifier et recompiler votre code source de la bibliothèque avec la même clé.</span><span class="sxs-lookup"><span data-stu-id="f571f-124">A publicly available key lets developers modify and recompile your library source code with the same key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f571f-125">Lorsqu’une identité de chiffrement est souhaitée, [Authenticode](/windows-hardware/drivers/install/authenticode) et [la signature du Package NuGet](/nuget/create-packages/sign-a-package) sont recommandés.</span><span class="sxs-lookup"><span data-stu-id="f571f-125">When a cryptographic identity is desired, [Authenticode](/windows-hardware/drivers/install/authenticode) and [NuGet Package Signing](/nuget/create-packages/sign-a-package) are recommended.</span></span> <span data-ttu-id="f571f-126">Utilisation de noms forts ne doit pas être utilisée pour les considérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f571f-126">Strong naming should not be used for security considerations.</span></span>

<span data-ttu-id="f571f-127">**ENVISAGEZ de ✔️** incrémentation de la version d’assembly sur les modifications de version principale uniquement pour aider les utilisateurs à réduire les redirections de liaison et la fréquence à laquelle ils sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f571f-127">**✔️ CONSIDER** incrementing the assembly version on only major version changes to help users reduce binding redirects, and how often they're updated.</span></span>

> <span data-ttu-id="f571f-128">En savoir plus sur [le contrôle de version et la version d’assembly](./versioning.md#assembly-version).</span><span class="sxs-lookup"><span data-stu-id="f571f-128">Read more about [versioning and the assembly version](./versioning.md#assembly-version).</span></span>

<span data-ttu-id="f571f-129">**N’est pas le cas de ❌** ajouter, supprimer ou modifier la clé d’affectation de noms forte.</span><span class="sxs-lookup"><span data-stu-id="f571f-129">**❌ DO NOT** add, remove, or change the strong naming key.</span></span>

> <span data-ttu-id="f571f-130">Modification de la clé d’affectation de noms forts d’un assembly modifie l’identité de l’assembly et altère le code compilé qui l’utilise.</span><span class="sxs-lookup"><span data-stu-id="f571f-130">Modifying an assembly's strong naming key changes the assembly's identity and breaks compiled code that uses it.</span></span> <span data-ttu-id="f571f-131">Pour plus d’informations, consultez [binaire de modifications avec rupture](./breaking-changes.md#binary-breaking-change).</span><span class="sxs-lookup"><span data-stu-id="f571f-131">For more information, see [binary breaking changes](./breaking-changes.md#binary-breaking-change).</span></span>

<span data-ttu-id="f571f-132">**N’est pas le cas de ❌** publier avec nom fort et non-fort des versions de votre bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="f571f-132">**❌ DO NOT** publish strong-named and non-strong-named versions of your library.</span></span> <span data-ttu-id="f571f-133">Par exemple : `Contoso.Api` et `Contoso.Api.StrongNamed`.</span><span class="sxs-lookup"><span data-stu-id="f571f-133">For example, `Contoso.Api` and `Contoso.Api.StrongNamed`.</span></span>

> <span data-ttu-id="f571f-134">Publication deux branchements de packages de votre écosystème de développeur.</span><span class="sxs-lookup"><span data-stu-id="f571f-134">Publishing two packages forks your developer eco-system.</span></span> <span data-ttu-id="f571f-135">En outre, si une application se retrouve selon les deux packages le développeur peut rencontrer des conflits de noms de type.</span><span class="sxs-lookup"><span data-stu-id="f571f-135">Also, if an application ends up depending on both packages the developer can encounter type name conflicts.</span></span> <span data-ttu-id="f571f-136">Comme ce qui concerne .NET est qu’ils sont différents types dans des assemblys différents.</span><span class="sxs-lookup"><span data-stu-id="f571f-136">As far as .NET is concerned they are different types in different assemblies.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="f571f-137">[Précédent](./cross-platform-targeting.md)
[Suivant](./nuget.md)</span><span class="sxs-lookup"><span data-stu-id="f571f-137">[Previous](./cross-platform-targeting.md)
[Next](./nuget.md)</span></span>
