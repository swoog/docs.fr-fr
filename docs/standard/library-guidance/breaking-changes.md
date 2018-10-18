---
title: Modifications avec rupture et les bibliothèques .NET
description: Meilleures pratiques recommandées pour parcourir les modifications avec rupture lors de la création de bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 83c01fdad7d836877bf692b87eeb0230219ded36
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370061"
---
# <a name="breaking-changes"></a><span data-ttu-id="dfbbf-103">Modifications avec rupture</span><span class="sxs-lookup"><span data-stu-id="dfbbf-103">Breaking changes</span></span>

<span data-ttu-id="dfbbf-104">Il est important pour une bibliothèque .NET trouver un équilibre entre la stabilité pour les utilisateurs existants et l’innovation pour l’avenir.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-104">It's important for a .NET library to find a balance between stability for existing users and innovation for the future.</span></span> <span data-ttu-id="dfbbf-105">Les auteurs de bibliothèque au plus juste pour la refactorisation et à repenser le code jusqu'à ce qu’il est parfait, mais avec rupture de vos utilisateurs existants a un impact négatif, en particulier pour les bibliothèques de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-105">Library authors lean towards refactoring and rethinking code until it's perfect, but breaking your existing users has a negative impact, especially for low-level libraries.</span></span>

## <a name="project-types-and-breaking-changes"></a><span data-ttu-id="dfbbf-106">Types de projets et des modifications avec rupture</span><span class="sxs-lookup"><span data-stu-id="dfbbf-106">Project types and breaking changes</span></span>

<span data-ttu-id="dfbbf-107">Comment une bibliothèque est utilisée par la Communauté .NET modifie l’effet des changements sur les développeurs de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-107">How a library is used by the .NET community changes the effect of breaking changes on end-user developers.</span></span>

* <span data-ttu-id="dfbbf-108">**Faible et des bibliothèques de niveau intermédiaire** comme un analyseur sérialiseur, HTML, mappeur relationnel objet de base de données ou infrastructure web sont plus affectés par les modifications avec rupture.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-108">**Low and middle-level libraries** like a serializer, HTML parser, database object-relational mapper, or web framework are the most affected by breaking changes.</span></span>

  <span data-ttu-id="dfbbf-109">Packages de bloc de construction sont utilisés par les développeurs de l’utilisateur final de créer des applications et par d’autres bibliothèques comme dépendances NuGet.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-109">Building block packages are used by end-user developers to build applications, and by other libraries as NuGet dependencies.</span></span> <span data-ttu-id="dfbbf-110">Par exemple, vous créez une application et que vous utilisez un client open source pour appeler un service web.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-110">For example, you're building an application and are using an open-source client to call a web service.</span></span> <span data-ttu-id="dfbbf-111">Une mise à jour avec rupture à une dépendance qu'utilise le client n’est pas quelque chose que vous pouvez résoudre.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-111">A breaking update to a dependency the client uses isn't something you can fix.</span></span> <span data-ttu-id="dfbbf-112">C’est le client open source qui doit être modifiée et que vous n’avez aucun contrôle dessus.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-112">It's the open-source client that needs to be changed and you have no control over it.</span></span> <span data-ttu-id="dfbbf-113">Vous devez déterminer les versions compatibles des bibliothèques ou soumettre un correctif à la bibliothèque cliente et attendre une nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-113">You have to find compatible versions of the libraries or submit a fix to the client library and wait for a new version.</span></span> <span data-ttu-id="dfbbf-114">La situation pire est si vous souhaitez utiliser les deux bibliothèques qui dépendent de versions mutuellement incompatibles d’une bibliothèque de tiers.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-114">The worst-case situation is if you want to use two libraries that depend on mutually incompatible versions of a third library.</span></span>

* <span data-ttu-id="dfbbf-115">**Bibliothèques de haut niveau** comme une suite de l’interface utilisateur des contrôles sont moins sensibles aux modifications avec rupture.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-115">**High-level libraries** like a suite of UI controls are less sensitive to breaking changes.</span></span>

  <span data-ttu-id="dfbbf-116">Bibliothèques de haut niveau sont directement référencés dans une application de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-116">High-level libraries are directly referenced in an end-user application.</span></span> <span data-ttu-id="dfbbf-117">En cas de modifications avec rupture, le développeur peut choisir de mettre à jour vers la dernière version, ou permettre modifier leur application de fonctionner avec la modification avec rupture.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-117">If breaking changes occur, the developer can choose to update to the latest version, or can modify their application to work with the breaking change.</span></span>

<span data-ttu-id="dfbbf-118">**FAIRE ✔️** réflexion sur l’utilisation de votre bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-118">**✔️ DO** think about how your library will be used.</span></span> <span data-ttu-id="dfbbf-119">Effet des modifications avec rupture aura sur les applications et les bibliothèques qui l’utilisent ?</span><span class="sxs-lookup"><span data-stu-id="dfbbf-119">What effect will breaking changes have on applications and libraries that use it?</span></span>

<span data-ttu-id="dfbbf-120">**FAIRE ✔️** minimiser les modifications avec rupture lors du développement d’une bibliothèque .NET de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-120">**✔️ DO** minimize breaking changes when developing a low-level .NET library.</span></span>

<span data-ttu-id="dfbbf-121">**ENVISAGEZ de ✔️** publication majeur de réécriture d’une bibliothèque en tant qu’un nouveau package NuGet.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-121">**✔️ CONSIDER** publishing a major rewrite of a library as a new NuGet package.</span></span>

## <a name="types-of-breaking-changes"></a><span data-ttu-id="dfbbf-122">Types de modifications avec rupture</span><span class="sxs-lookup"><span data-stu-id="dfbbf-122">Types of breaking changes</span></span>

<span data-ttu-id="dfbbf-123">Modifications avec rupture se répartissent en différentes catégories et ne sont pas aussi efficaces.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-123">Breaking changes fall into different categories and aren't equally impactful.</span></span>

### <a name="source-breaking-change"></a><span data-ttu-id="dfbbf-124">Modification avec rupture de code source</span><span class="sxs-lookup"><span data-stu-id="dfbbf-124">Source breaking change</span></span>

<span data-ttu-id="dfbbf-125">Une source de modification avec rupture n’affecte pas l’exécution du programme mais provoquera des erreurs de compilation la prochaine fois que l’application est recompilée.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-125">A source breaking change doesn't affect program execution but will cause compilation errors the next time the application is recompiled.</span></span> <span data-ttu-id="dfbbf-126">Par exemple, une nouvelle surcharge peut créer une ambiguïté dans les appels de méthode qui étaient précédemment non équivoque, ou un paramètre renommé interrompra les appelants qui utilisent des paramètres nommés.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-126">For example, a new overload can create an ambiguity in method calls that were unambiguous previously, or a renamed parameter will break callers that use named parameters.</span></span>

```csharp
public class Task
{
    // Adding a type called Task could conflict with System.Threading.Tasks.Task at compilation
}
```

<span data-ttu-id="dfbbf-127">Étant une source de modification avec rupture uniquement dangereuse lorsque les développeurs recompiler leurs applications, il est la moins perturbatrices modification avec rupture.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-127">Because a source breaking change is only harmful when developers recompile their applications, it's the least disruptive breaking change.</span></span> <span data-ttu-id="dfbbf-128">Les développeurs peuvent résoudre leur propre code source rompu facilement.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-128">Developers can fix their own broken source code easily.</span></span>

### <a name="behavior-breaking-change"></a><span data-ttu-id="dfbbf-129">Changement de comportement</span><span class="sxs-lookup"><span data-stu-id="dfbbf-129">Behavior breaking change</span></span>

<span data-ttu-id="dfbbf-130">Changements de comportement sont le type le plus courant de modification avec rupture : une personne peut inhiber les presque n’importe quel changement de comportement.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-130">Behavior changes are the most common type of breaking change: almost any change in behavior could break someone.</span></span> <span data-ttu-id="dfbbf-131">Modifications à votre bibliothèque, telles que les signatures de méthode, les exceptions levées ou d’entrée ou de sortie des formats de données, tout impact négatif sur vos consommateurs de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-131">Changes to your library, such as method signatures, exceptions thrown or input or output data formats, could all negatively impact your library consumers.</span></span> <span data-ttu-id="dfbbf-132">Même un correctif de bogue peut considéré comme une modification avec rupture Si les utilisateurs s’appuyaient sur le comportement précédemment interrompue.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-132">Even a bug fix can qualify as a breaking change if users relied on the previously broken behavior.</span></span>

<span data-ttu-id="dfbbf-133">Ajout de fonctionnalités et l’amélioration de mauvais comportements sont une bonne chose, mais sans les soins il peut rendre très difficile pour les utilisateurs existants à mettre à niveau.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-133">Adding features and improving bad behaviors is a good thing, but without care it can make it very hard for existing users to upgrade.</span></span> <span data-ttu-id="dfbbf-134">Une approche pour aider les développeurs à gérer avec les dernières modifications de comportement consiste à les masquer derrière les paramètres.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-134">One approach to helping developers deal with behavior breaking changes is to hide them behind settings.</span></span> <span data-ttu-id="dfbbf-135">Paramètres permettent aux développeurs de mettre à jour vers la dernière version de votre bibliothèque tout en choisissant d’accepter ou refuser de modifications avec rupture.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-135">Settings let developers update to the latest version of your library while at the same time choosing to opt in or opt out of breaking changes.</span></span> <span data-ttu-id="dfbbf-136">Cette stratégie permet aux développeurs de rester à jour tout en permettant à leur code de consommation de s’adapter au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-136">This strategy lets developers stay up to date while letting their consuming code adapt over time.</span></span>

<span data-ttu-id="dfbbf-137">Par exemple, ASP.NET Core MVC a le concept d’un [version compatibilité](/aspnet/core/mvc/compatibility-version) qui modifie les fonctionnalités activées et désactivées sur `MvcOptions`.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-137">For example, ASP.NET Core MVC has the concept of a [compatibility version](/aspnet/core/mvc/compatibility-version) that modifies the features enabled and disabled on `MvcOptions`.</span></span>

<span data-ttu-id="dfbbf-138">**ENVISAGEZ de ✔️** si vous omettez nouvelles fonctionnalités par défaut, si elles affectent les utilisateurs existants et permettent aux développeurs de s’abonner à la fonctionnalité avec un paramètre.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-138">**✔️ CONSIDER** leaving new features off by default, if they affect existing users, and let developers opt in to the feature with a setting.</span></span>

### <a name="binary-breaking-change"></a><span data-ttu-id="dfbbf-139">Modification avec rupture binaire</span><span class="sxs-lookup"><span data-stu-id="dfbbf-139">Binary breaking change</span></span>

<span data-ttu-id="dfbbf-140">Un fichier binaire modification avec rupture qui se produit lorsque vous modifiez l’API publique de votre bibliothèque, afin des assemblys compilés par rapport à des versions antérieures de votre bibliothèque ne sont plus en mesure d’appeler l’API.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-140">A binary breaking change happens when you change the public API of your library, so assemblies compiled against older versions of your library are no longer able to call the API.</span></span> <span data-ttu-id="dfbbf-141">Par exemple, la modification de signature d’une méthode en ajoutant un nouveau paramètre entraîne assemblys compilés avec l’ancienne version de la bibliothèque lever une <xref:System.MissingMethodException>.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-141">For example, changing a method's signature by adding a new parameter will cause assemblies compiled against the older version of the library to throw a <xref:System.MissingMethodException>.</span></span>

<span data-ttu-id="dfbbf-142">Un fichier binaire modification avec rupture peut également être rompus un **assembly entier**.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-142">A binary breaking change can also break an **entire assembly**.</span></span> <span data-ttu-id="dfbbf-143">Modification du nom d’un assembly avec `AssemblyName` changera identité de l’assembly, de même que l’ajout, suppression ou modification d’une clé forte d’affectation de noms de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-143">Renaming an assembly with `AssemblyName` will change the assembly's identity, as will adding, removing, or changing the assembly's strong naming key.</span></span> <span data-ttu-id="dfbbf-144">Une modification de l’identité d’un assembly va interrompre tout le code compilé qui l’utilise.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-144">A change of an assembly's identity will break all compiled code that uses it.</span></span>

<span data-ttu-id="dfbbf-145">**N’est pas le cas de ❌** modifier un nom d’assembly.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-145">**❌ DO NOT** change an assembly name.</span></span>

<span data-ttu-id="dfbbf-146">**N’est pas le cas de ❌** ajouter, supprimer ou modifier la clé d’affectation de noms forte.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-146">**❌ DO NOT** add, remove, or change the strong naming key.</span></span>

<span data-ttu-id="dfbbf-147">**ENVISAGEZ de ✔️** à l’aide des classes de base abstraites au lieu d’interfaces.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-147">**✔️ CONSIDER** using abstract base classes instead of interfaces.</span></span>

> <span data-ttu-id="dfbbf-148">Ajouter quoi que ce soit à une interface entraîne des types existants qui implémentent son échec.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-148">Adding anything to an interface will cause existing types that implement it to fail.</span></span> <span data-ttu-id="dfbbf-149">Classe de base abstraite permet de vous permet d’ajouter une implémentation virtuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-149">An abstract base class allows you to add a default virtual implementation.</span></span>

<span data-ttu-id="dfbbf-150">**✔️ Envisagez** placer le <xref:System.ObsoleteAttribute> sur les types et membres que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-150">**✔️ CONSIDER** placing the <xref:System.ObsoleteAttribute> on types and members that you intend to remove.</span></span> <span data-ttu-id="dfbbf-151">L’attribut doit avoir des instructions pour la mise à jour de code de ne plus utiliser l’API obsolète.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-151">The attribute should have instructions for updating code to no longer use the obsolete API.</span></span>

> <span data-ttu-id="dfbbf-152">Code qui appelle des types et méthodes avec les <xref:System.ObsoleteAttribute> génère un avertissement de build avec le message fourni à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-152">Code that calls types and methods with the <xref:System.ObsoleteAttribute> will generate a build warning with the message supplied to the attribute.</span></span> <span data-ttu-id="dfbbf-153">Les personnes de donnent des avertissements qui utilisent l’heure de surface d’API obsolète pour migrer afin que lors de l’API obsolète est supprimé, la plupart n’est plus l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="dfbbf-153">The warnings give people who use the obsolete API surface time to migrate so that when the obsolete API is removed, most are no longer using it.</span></span>

```csharp
public class Document
{
    [Obsolete("LoadDocument(string) is obsolete. Use LoadDocument(Uri) instead.")]
    public static Document LoadDocument(string uri)
    {
        return LoadDocument(new Uri(uri));
    }

    public static Document LoadDocument(Uri uri)
    {
        // Load the document
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dfbbf-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfbbf-154">See also</span></span>

* [<span data-ttu-id="dfbbf-155">Considérations relatives à la version et de mise à jour pour les développeurs c#</span><span class="sxs-lookup"><span data-stu-id="dfbbf-155">Version and update considerations for C# developers</span></span>](../../csharp/whats-new/version-update-considerations.md)
* [<span data-ttu-id="dfbbf-156">Un guide de référence pour les modifications avec rupture des API dans .NET</span><span class="sxs-lookup"><span data-stu-id="dfbbf-156">A definitive guide to API-breaking changes in .NET</span></span>](https://stackoverflow.com/questions/1456785/a-definitive-guide-to-api-breaking-changes-in-net)
* [<span data-ttu-id="dfbbf-157">Règles de modification avec rupture CoreFX</span><span class="sxs-lookup"><span data-stu-id="dfbbf-157">CoreFX Breaking Change Rules</span></span>](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/breaking-change-rules.md)

>[!div class="step-by-step"]
[<span data-ttu-id="dfbbf-158">Précédent</span><span class="sxs-lookup"><span data-stu-id="dfbbf-158">Previous</span></span>](./versioning.md)
