---
title: "Les analyseurs de sécurité .NET - .NET"
description: "Découvrez comment utiliser les analyseurs de sécurité .NET dans le package Analyseurs .NET Framework pour rechercher et résoudre les problèmes de sécurité"
keywords: .NET, .NET Core
author: billwagner
ms.author: billwagner
ms.date: 01/25/2018
ms.topic: article
ms.prod: .net
ms.technology: dotnet-standard
ms.devlang: dotnet
ms.openlocfilehash: 06a387d72d06609182c8894dd874b241a5d7b69c
ms.sourcegitcommit: 3a96c706e4dbb4667bf3bf37edac9e1666646f93
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2018
---
# <a name="the-net-framework-analyzer"></a><span data-ttu-id="d1636-104">L’analyseur .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d1636-104">The .NET Framework Analyzer</span></span>

<span data-ttu-id="d1636-105">Vous pouvez utiliser l’Analyseur .NET Framework pour rechercher les problèmes potentiels dans votre code d’application basé sur .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d1636-105">You can use the .NET Framework Analyzer to find potential issues in your .NET Framework-based application code.</span></span> <span data-ttu-id="d1636-106">Cet analyseur recherche les problèmes potentiels et suggère des correctifs pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="d1636-106">This analyzer finds potential issues and suggests fixes to them.</span></span>

<span data-ttu-id="d1636-107">L’analyseur s’exécute de façon interactive dans Visual Studio au fil de l’écriture du code ou dans le cadre d’une build CI.</span><span class="sxs-lookup"><span data-stu-id="d1636-107">The analyzer runs interactively in Visual Studio as you write your code or as part of a CI build.</span></span> <span data-ttu-id="d1636-108">Il est recommandé d’ajouter l’analyseur à votre projet dès que possible dans votre développement.</span><span class="sxs-lookup"><span data-stu-id="d1636-108">You should add the analyzer to your project as early as possible in your development.</span></span> <span data-ttu-id="d1636-109">Plus tôt vous trouvez les problèmes potentiels dans votre code, plus ils sont faciles à corriger.</span><span class="sxs-lookup"><span data-stu-id="d1636-109">The sooner you find any potential issues in your code, the easier they are to fix.</span></span> <span data-ttu-id="d1636-110">Cependant, vous pouvez l’ajouter à tout moment au cours du cycle de développement.</span><span class="sxs-lookup"><span data-stu-id="d1636-110">However, you can add it at any time in the development cycle.</span></span> <span data-ttu-id="d1636-111">Il détecte les problèmes dans le code existant et signale les problèmes au fil de votre développement.</span><span class="sxs-lookup"><span data-stu-id="d1636-111">It finds any issues with the existing code and warns about new issues as you keep developing.</span></span>

## <a name="installing-and-configuring-the-net-framework-analyzer"></a><span data-ttu-id="d1636-112">Installation et configuration de l’Analyseur .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d1636-112">Installing and configuring the .NET Framework Analyzer</span></span>

<span data-ttu-id="d1636-113">Les analyseurs de sécurité .NET doivent être installés sous forme de package NuGet sur chaque projet où vous voulez qu’ils s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="d1636-113">The .NET Security Analyzers must be installed as a NuGet package on every project where you want them to run.</span></span> <span data-ttu-id="d1636-114">Il suffit qu’un seul développeur les ajoute au projet.</span><span class="sxs-lookup"><span data-stu-id="d1636-114">Only one developer needs to add them to the project.</span></span> <span data-ttu-id="d1636-115">Le package de l’analyseur est une dépendance de projet et il s’exécute sur la machine de chaque développeur une fois qu’il dispose de la solution mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d1636-115">The analyzer package is a project dependency and will run on every developer's machine once it has the updated solution.</span></span>

<span data-ttu-id="d1636-116">L’Analyseur .NET Framework est livré dans le package NuGet [Microsoft.NetFramework.Analyzers](https://www.nuget.org/packages/Microsoft.NetFramework.Analyzers/).</span><span class="sxs-lookup"><span data-stu-id="d1636-116">The .NET Framework Analyzer is delivered in the [Microsoft.NetFramework.Analyzers](https://www.nuget.org/packages/Microsoft.NetFramework.Analyzers/) NuGet package.</span></span> <span data-ttu-id="d1636-117">Ce package fournit seulement les analyseurs spécifiques à .NET Framework, qui comprend des analyseurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d1636-117">This package provides only the analyzers specific to the .NET Framework, which includes security analyzers.</span></span> <span data-ttu-id="d1636-118">Dans la plupart des cas, vous allez utiliser le package NuGet [Microsoft.CodeAnalysis.FxCopAnalyzers](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers).</span><span class="sxs-lookup"><span data-stu-id="d1636-118">In most cases, you'll want the [Microsoft.CodeAnalysis.FxCopAnalyzers](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers) NuGet package.</span></span> <span data-ttu-id="d1636-119">Le package d’agrégation FxCopAnalyzers contient tous les analyseurs de framework inclus dans le package Framework.Analyzers, ainsi que les analyseurs suivants :</span><span class="sxs-lookup"><span data-stu-id="d1636-119">The FxCopAnalyzers aggregate package contains all the framework analyzers included in the Framework.Analyzers package as well as the following analyzers:</span></span>
- <span data-ttu-id="d1636-120">[Microsoft.CodeQuality.Analyzers](https://www.nuget.org/packages/Microsoft.CodeQuality.Analyzers) : fournit des indications générales et des conseils pour les API .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="d1636-120">[Microsoft.CodeQuality.Analyzers](https://www.nuget.org/packages/Microsoft.CodeQuality.Analyzers): Provides general guidance and guidance for .NET Standard APIs</span></span>
- <span data-ttu-id="d1636-121">[Microsoft.NetCore.Analyzers](https://www.nuget.org/packages/Microsoft.NetCore.Analyzers) : fournit des analyseurs spécifiques aux API .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d1636-121">[Microsoft.NetCore.Analyzers](https://www.nuget.org/packages/Microsoft.NetCore.Analyzers): Provides analyzers specific to .NET Core APIs.</span></span>
- <span data-ttu-id="d1636-122">[Text.Analyzers](https://www.nuget.org/packages/Text.Analyzers) : fournit des conseils pour le texte inclus en tant que code, notamment les commentaires.</span><span class="sxs-lookup"><span data-stu-id="d1636-122">[Text.Analyzers](https://www.nuget.org/packages/Text.Analyzers): Provides guidance for text included as code, including comments.</span></span>

<span data-ttu-id="d1636-123">Pour l’installer, cliquez avec le bouton droit sur le projet et sélectionnez « Gérer les dépendances ».</span><span class="sxs-lookup"><span data-stu-id="d1636-123">To install it, right-click on the project, and select "Manage Dependencies".</span></span>
<span data-ttu-id="d1636-124">Dans l’Explorateur NuGet, recherchez « NetFramework Analyzer » ou, si vous préférez, « Fx Cop Analyzerx ».</span><span class="sxs-lookup"><span data-stu-id="d1636-124">From the NuGet explorer, search for "NetFramework Analyzer", or if you prefer, "Fx Cop Analyzer".</span></span> <span data-ttu-id="d1636-125">Installez la dernière version stable dans tous les projets de votre solution.</span><span class="sxs-lookup"><span data-stu-id="d1636-125">Install the latest stable version in all projects in your solution.</span></span>

## <a name="using-the-net-framework-analyzer"></a><span data-ttu-id="d1636-126">Utilisation de l’Analyseur .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d1636-126">Using the .NET Framework Analyzer</span></span>

<span data-ttu-id="d1636-127">Une fois le package NuGet installé, générez votre solution.</span><span class="sxs-lookup"><span data-stu-id="d1636-127">Once the NuGet package is installed, build your solution.</span></span> <span data-ttu-id="d1636-128">L’analyseur signale les éventuels problèmes qu’il trouve dans votre code base.</span><span class="sxs-lookup"><span data-stu-id="d1636-128">The analyzer will report any issues it locates in your codebase.</span></span> <span data-ttu-id="d1636-129">Les problèmes sont signalés sous forme d’avertissements dans la fenêtre Liste d’erreurs de Visual Studio, comme le montre l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="d1636-129">The issues are reported as warnings in the Visual Studio Error List window, as shown in the following image:</span></span>

![problèmes signalés par l’analyseur d’infrastructure](./media/framework-analyzers-2.png)

<span data-ttu-id="d1636-131">Au fil de l’écriture du code, vous voyez des marques ondulées sous les problèmes potentiels de votre code.</span><span class="sxs-lookup"><span data-stu-id="d1636-131">As you write code, you see squiggles underneath any potential issue in your code.</span></span>
<span data-ttu-id="d1636-132">Placez le curseur sur un problème pour voir plus d’informations sur celui-ci, ainsi que des suggestions pour une correction possible, comme le montre l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="d1636-132">Hover over any issue and you see details about the issue, and suggestions for any possible fix, as shown in the following image:</span></span>

![rapport interactif des problèmes détectés par l’Analyseur de framework](./media/framework-analyzers-1.png)

<span data-ttu-id="d1636-134">Les analyseurs examinent le code de votre solution et vous fournissent une liste d’avertissements pour ces problèmes :</span><span class="sxs-lookup"><span data-stu-id="d1636-134">The analyzers examine the code in your solution and provide you with a list of warnings for any of these issues:</span></span>

### <a name="ca1058-types-should-not-extend-certain-base-types"></a><span data-ttu-id="d1636-135">CA1058 : Les types ne doivent pas étendre certains types de base</span><span class="sxs-lookup"><span data-stu-id="d1636-135">CA1058: Types should not extend certain base types</span></span>

<span data-ttu-id="d1636-136">Vous ne devez rien dériver directement d’un petit nombre de types du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d1636-136">There are a small number of types in the .NET Framework that you should not derived from directly.</span></span> 

<span data-ttu-id="d1636-137">**Catégorie :** Conception</span><span class="sxs-lookup"><span data-stu-id="d1636-137">**Category:** Design</span></span>

<span data-ttu-id="d1636-138">**Gravité :** Avertissement</span><span class="sxs-lookup"><span data-stu-id="d1636-138">**Severity:** Warning</span></span>

<span data-ttu-id="d1636-139">Informations supplémentaires : [CA1058 : Les types ne doivent pas étendre certains types de base](/visualstudio/code-quality/ca1058-types-should-not-extend-certain-base-types)</span><span class="sxs-lookup"><span data-stu-id="d1636-139">Additional information: [CA:1058: Types should not extend certain base types](/visualstudio/code-quality/ca1058-types-should-not-extend-certain-base-types)</span></span>

### <a name="ca2153-do-not-catch-corrupted-state-exceptions"></a><span data-ttu-id="d1636-140">CA2153 : Ne pas intercepter des exceptions d’état endommagé</span><span class="sxs-lookup"><span data-stu-id="d1636-140">CA2153: Do not catch corrupted state exceptions</span></span>

<span data-ttu-id="d1636-141">L’interception des exceptions d’état endommagé pourrait masquer des erreurs (comme des violations d’accès), aboutissant à un état d’exécution incohérent ou facilitant la compromission d’un système par des attaquants.</span><span class="sxs-lookup"><span data-stu-id="d1636-141">Catching corrupted state exceptions could mask errors (such as access violations), resulting in an inconsistent state of execution or making it easier for attackers to compromise a system.</span></span> <span data-ttu-id="d1636-142">Au lieu de cela, il faut intercepter et gérer un ensemble de types d’exception plus spécifiques, ou lever à nouveau l’exception.</span><span class="sxs-lookup"><span data-stu-id="d1636-142">Instead, catch and handle a more specific set of exception type(s) or re-throw the exception</span></span>

<span data-ttu-id="d1636-143">**Catégorie :** Sécurité</span><span class="sxs-lookup"><span data-stu-id="d1636-143">**Category:** Security</span></span>

<span data-ttu-id="d1636-144">**Gravité :** Avertissement</span><span class="sxs-lookup"><span data-stu-id="d1636-144">**Severity:** Warning</span></span>

<span data-ttu-id="d1636-145">Informations supplémentaires : [## CA2153 : Ne pas intercepter les exceptions d’état endommagé](/visualstudio/code-quality/ca2153-avoid-handling-corrupted-state-exceptions)</span><span class="sxs-lookup"><span data-stu-id="d1636-145">Additional information: [## CA2153: Do not catch corrupted state exceptions](/visualstudio/code-quality/ca2153-avoid-handling-corrupted-state-exceptions)</span></span>

### <a name="ca2229-implement-serialization-constructors"></a><span data-ttu-id="d1636-146">CA2229 : Implémentez des constructeurs de sérialisation</span><span class="sxs-lookup"><span data-stu-id="d1636-146">CA2229: Implement serialization constructors</span></span>

<span data-ttu-id="d1636-147">L’analyseur génère cet avertissement quand vous créez un type qui implémente l’interface <xref:System.Runtime.Serialization.ISerializable>, mais ne définit pas le constructeur de sérialisation nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d1636-147">The analyzer generates this warning when you create a type that implements the <xref:System.Runtime.Serialization.ISerializable> interface but does not define the required serialization constructor.</span></span> <span data-ttu-id="d1636-148">Pour corriger une violation de cette règle, implémentez le constructeur de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="d1636-148">To fix a violation of this rule, implement the serialization constructor.</span></span> <span data-ttu-id="d1636-149">Dans le cas d'une classe sealed, rendez le constructeur privé ; sinon, attribuez-lui l'état protégé.</span><span class="sxs-lookup"><span data-stu-id="d1636-149">For a sealed class, make the constructor private; otherwise, make it protected.</span></span> <span data-ttu-id="d1636-150">Le constructeur de sérialisation a la signature suivante :</span><span class="sxs-lookup"><span data-stu-id="d1636-150">The serialization constructor has the following signature:</span></span>

```csharp
public class MyItemType
{
    // The special constructor is used to deserialize values.
    public MyItemType(SerializationInfo info, StreamingContext context)
    {
        // implementation removed.
    }
}
```

<span data-ttu-id="d1636-151">**Catégorie :** Utilisation</span><span class="sxs-lookup"><span data-stu-id="d1636-151">**Category:** Usage</span></span>

<span data-ttu-id="d1636-152">**Gravité :** Avertissement</span><span class="sxs-lookup"><span data-stu-id="d1636-152">**Severity:** Warning</span></span>

<span data-ttu-id="d1636-153">Informations supplémentaires : [CA2229 : Implémentez des constructeurs de sérialisation](/visualstudio/code-quality/ca2229-implement-serialization-constructors)</span><span class="sxs-lookup"><span data-stu-id="d1636-153">Additional information: [CA2229: Implement serialization constructors](/visualstudio/code-quality/ca2229-implement-serialization-constructors)</span></span>

### <a name="ca2235-mark-all-non-serializable-fields"></a><span data-ttu-id="d1636-154">CA2235 : Marquez tous les champs non sérialisés</span><span class="sxs-lookup"><span data-stu-id="d1636-154">CA2235: Mark all non-serializable fields</span></span>

<span data-ttu-id="d1636-155">Un champ d'instance d'un type non sérialisable est déclaré dans un type sérialisable.</span><span class="sxs-lookup"><span data-stu-id="d1636-155">An instance field of a type that is not serializable is declared in a type that is serializable.</span></span> <span data-ttu-id="d1636-156">Vous devez marquer explicitement ce champ avec <xref:System.NonSerializedAttribute> pour résoudre cet avertissement.</span><span class="sxs-lookup"><span data-stu-id="d1636-156">You must explicitly mark that field with the <xref:System.NonSerializedAttribute> to fix this warning.</span></span>

<span data-ttu-id="d1636-157">**Catégorie :** Utilisation</span><span class="sxs-lookup"><span data-stu-id="d1636-157">**Category:** Usage</span></span>

<span data-ttu-id="d1636-158">**Gravité :** Avertissement</span><span class="sxs-lookup"><span data-stu-id="d1636-158">**Severity:** Warning</span></span>

<span data-ttu-id="d1636-159">Informations supplémentaires : [CA2235 : Marquez tous les champs non sérialisables](/visualstudio/code-quality/ca2235-mark-all-non-serializable-fields)</span><span class="sxs-lookup"><span data-stu-id="d1636-159">Additional information: [CA2235: Mark all non-serializable fields](/visualstudio/code-quality/ca2235-mark-all-non-serializable-fields)</span></span>

### <a name="ca2237-mark-iserializable-types-with-serializable"></a><span data-ttu-id="d1636-160">CA2237 : Marquez les types ISerializable comme étant sérialisables</span><span class="sxs-lookup"><span data-stu-id="d1636-160">CA2237: Mark ISerializable types with serializable</span></span>

<span data-ttu-id="d1636-161">Pour être reconnus par le Common Language Runtime comme étant sérialisables, les types doivent être marqués avec l’attribut <xref:System.SerializableAttribute>, même s’ils utilisent une routine de sérialisation personnalisée en implémentant l’interface <xref:System.Runtime.Serialization.ISerializable>.</span><span class="sxs-lookup"><span data-stu-id="d1636-161">To be recognized by the common language runtime as serializable, types must be marked by using the <xref:System.SerializableAttribute> attribute even when the type uses a custom serialization routine by implementing the <xref:System.Runtime.Serialization.ISerializable> interface.</span></span>

<span data-ttu-id="d1636-162">**Catégorie :** Utilisation</span><span class="sxs-lookup"><span data-stu-id="d1636-162">**Category:** Usage</span></span>

<span data-ttu-id="d1636-163">**Gravité :** Avertissement</span><span class="sxs-lookup"><span data-stu-id="d1636-163">**Severity:** Warning</span></span>

<span data-ttu-id="d1636-164">Informations supplémentaires : [CA2237 : Marquez les types ISerializable comme étant sérialisables](/visualstudio/code-quality/ca2237-mark-iserializable-types-with-serializableattribute)</span><span class="sxs-lookup"><span data-stu-id="d1636-164">Additional information: [CA2237: Mark ISerializable types with serializable](/visualstudio/code-quality/ca2237-mark-iserializable-types-with-serializableattribute)</span></span>

### <a name="ca3075-insecure-dtd-processing-in-xml"></a><span data-ttu-id="d1636-165">CA3075 : Traitement du DTD non sécurisé dans XML</span><span class="sxs-lookup"><span data-stu-id="d1636-165">CA3075: Insecure DTD processing in XML</span></span>

<span data-ttu-id="d1636-166">Si vous utilisez des instances de <xref:System.Xml.XmlReaderSettings.DtdProcessing%2A> non sécurisées ou référencez des sources d’entités externes, l’analyseur peut accepter une entrée non fiable et divulguer des informations sensibles à des personnes malveillantes.</span><span class="sxs-lookup"><span data-stu-id="d1636-166">If you use insecure <xref:System.Xml.XmlReaderSettings.DtdProcessing%2A> instances or reference external entity sources, the parser may accept untrusted input and disclose sensitive information to attackers.</span></span>  

<span data-ttu-id="d1636-167">**Catégorie :** Sécurité</span><span class="sxs-lookup"><span data-stu-id="d1636-167">**Category:** Security</span></span>

<span data-ttu-id="d1636-168">**Gravité :** Avertissement</span><span class="sxs-lookup"><span data-stu-id="d1636-168">**Severity:** Warning</span></span>

<span data-ttu-id="d1636-169">Informations supplémentaires : [A3075 : Traitement du DTD non sécurisé dans XML](/visualstudio/code-quality/ca2237-mark-iserializable-types-with-serializableattribute)</span><span class="sxs-lookup"><span data-stu-id="d1636-169">Additional information: [A3075: Insecure DTD processing in XML](/visualstudio/code-quality/ca2237-mark-iserializable-types-with-serializableattribute)</span></span>


### <a name="ca5350-do-not-use-weak-cryptographic-algorithms"></a><span data-ttu-id="d1636-170">CA5350 : N’utilisez pas d’algorithmes de chiffrement faibles</span><span class="sxs-lookup"><span data-stu-id="d1636-170">CA5350: Do not use weak cryptographic algorithms</span></span>

<span data-ttu-id="d1636-171">Les algorithmes de chiffrement se dégradent au fil du temps, car les attaques deviennent plus sophistiquées.</span><span class="sxs-lookup"><span data-stu-id="d1636-171">Cryptographic algorithms degrade over time as attacks become more advanced.</span></span> <span data-ttu-id="d1636-172">Selon le type et l’application de cet algorithme de chiffrement, une dégradation progressive de sa force de chiffrement peut permettre aux attaquants de lire des messages chiffrés, de falsifier des messages chiffrés, de falsifier des signatures numériques, de falsifier du contenu haché ou de compromettre les systèmes de chiffrement basés sur cet algorithme.</span><span class="sxs-lookup"><span data-stu-id="d1636-172">Depending on the type and application of this cryptographic algorithm, further degradation of its cryptographic strength may allow attackers to read enciphered messages, tamper with enciphered messages, forge digital signatures, tamper with hashed content, or otherwise compromise any cryptosystem based on this algorithm.</span></span> <span data-ttu-id="d1636-173">Pour le chiffrement, utilisez un algorithme AES (AES-256, AES-192 et AES-128 sont acceptables) avec une longueur de clé supérieure ou égale à 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d1636-173">For encryption, use an AES algorithm (AES-256, AES-192 and AES-128 are acceptable) with a key length greater than or equal to 128 bits.</span></span> <span data-ttu-id="d1636-174">Pour le hachage, utilisez une fonction de hachage de la famille SHA-2, comme SHA-2 512, SHA-2 384 ou SHA-2 256.</span><span class="sxs-lookup"><span data-stu-id="d1636-174">For hashing, use a hashing function in the SHA-2 family, such as SHA-2 512, SHA-2 384, or SHA-2 256.</span></span>

<span data-ttu-id="d1636-175">**Catégorie :** Sécurité</span><span class="sxs-lookup"><span data-stu-id="d1636-175">**Category:** Security</span></span>

<span data-ttu-id="d1636-176">**Gravité :** Avertissement</span><span class="sxs-lookup"><span data-stu-id="d1636-176">**Severity:** Warning</span></span>

<span data-ttu-id="d1636-177">Informations supplémentaires : [CA5350 : N’utilisez pas d’algorithmes de chiffrement faibles](/visualstudio/code-quality/ca5350-do-not-use-weak-cryptographic-algorithms)</span><span class="sxs-lookup"><span data-stu-id="d1636-177">Additional information: [CA5350: Do not use weak cryptographic algorithms](/visualstudio/code-quality/ca5350-do-not-use-weak-cryptographic-algorithms)</span></span>

### <a name="ca5351-do-not-use-broken-cryptographic-algorithms"></a><span data-ttu-id="d1636-178">CA5351 : N’utilisez pas les algorithmes de chiffrement cassés</span><span class="sxs-lookup"><span data-stu-id="d1636-178">CA5351: Do not use broken cryptographic algorithms</span></span>

<span data-ttu-id="d1636-179">Il existe une attaque qui permet de casser cet algorithme par voie informatique.</span><span class="sxs-lookup"><span data-stu-id="d1636-179">An attack making it computationally feasible to break this algorithm exists.</span></span> <span data-ttu-id="d1636-180">Ceci permet aux attaquants de passer outre les garanties en matière de chiffrement qu’il doit normalement fournir.</span><span class="sxs-lookup"><span data-stu-id="d1636-180">This allows attackers to break the cryptographic guarantees it is designed to provide.</span></span> <span data-ttu-id="d1636-181">Selon le type et l’application de cet algorithme de chiffrement, ceci peut permettre aux attaquants de lire des messages chiffrés, de falsifier des messages chiffrés, de falsifier des signatures numériques, de falsifier du contenu haché ou de compromettre les systèmes de chiffrement basés sur cet algorithme.</span><span class="sxs-lookup"><span data-stu-id="d1636-181">Depending on the type and application of this cryptographic algorithm, this may allow attackers to read enciphered messages, tamper with enciphered messages, forge digital signatures, tamper with hashed content, or otherwise compromise any cryptosystem based on this algorithm.</span></span> <span data-ttu-id="d1636-182">Pour le chiffrement, utilisez un algorithme AES (AES-256, AES-192 et AES-128 sont acceptables) avec une longueur de clé supérieure ou égale à 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d1636-182">For encryption, use an AES algorithm (AES-256, AES-192 and AES-128 are acceptable) with a key length greater than or equal to 128 bits.</span></span> <span data-ttu-id="d1636-183">Pour le hachage, utilisez une fonction de hachage de la famille SHA-2, comme SHA512, SHA384 ou SHA256.</span><span class="sxs-lookup"><span data-stu-id="d1636-183">For hashing, use a hashing function in the SHA-2 family, such as SHA512, SHA384, or SHA256.</span></span> <span data-ttu-id="d1636-184">Pour les signatures numériques, utilisez RSA avec une longueur de clé supérieure ou égale à 2048 bits, ou ECDSA avec une longueur de clé supérieure ou égale à 256 bits.</span><span class="sxs-lookup"><span data-stu-id="d1636-184">For digital signatures, use RSA with a key length greater than or equal to 2048-bits, or ECDSA with a key length greater than or equal to 256 bits.</span></span>

<span data-ttu-id="d1636-185">**Catégorie :** Sécurité</span><span class="sxs-lookup"><span data-stu-id="d1636-185">**Category:** Security</span></span>

<span data-ttu-id="d1636-186">**Gravité :** Avertissement</span><span class="sxs-lookup"><span data-stu-id="d1636-186">**Severity:** Warning</span></span>

<span data-ttu-id="d1636-187">Informations supplémentaires : [CA5351 : N’utilisez pas d’algorithmes de chiffrement cassés](/visualstudio/code-quality/ca5351-do-not-use-broken-cryptographic-algorithms)</span><span class="sxs-lookup"><span data-stu-id="d1636-187">Additional Information: [CA5351: Do not use broken cryptographic algorithms](/visualstudio/code-quality/ca5351-do-not-use-broken-cryptographic-algorithms)</span></span>


