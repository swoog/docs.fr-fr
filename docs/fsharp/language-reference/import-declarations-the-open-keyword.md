---
title: 'Déclarations d’importation : mot clé open (F#)'
description: 'En savoir plus sur les déclarations d’importation F # et comment ils spécifient un module ou un espace de noms dont les éléments que vous pouvez référencer sans utiliser un nom qualifié complet.'
ms.date: 05/16/2016
ms.openlocfilehash: 8cae4b4f5418689bfb0933b7db4ec23a313d5ed8
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43883150"
---
# <a name="import-declarations-the-open-keyword"></a><span data-ttu-id="6cb81-103">Déclarations d’importation : Le `open` mot clé</span><span class="sxs-lookup"><span data-stu-id="6cb81-103">Import Declarations: The `open` Keyword</span></span>

> [!NOTE]
<span data-ttu-id="6cb81-104">Les liens des informations de référence sur les API qui figurent dans cet article pointent vers MSDN.</span><span class="sxs-lookup"><span data-stu-id="6cb81-104">The API reference links in this article will take you to MSDN.</span></span>  <span data-ttu-id="6cb81-105">Les informations de référence sur les API docs.microsoft.com ne sont pas terminées.</span><span class="sxs-lookup"><span data-stu-id="6cb81-105">The docs.microsoft.com API reference is not complete.</span></span>

<span data-ttu-id="6cb81-106">Un *déclaration d’importation* spécifie un module ou un espace de noms dont les éléments que vous pouvez référencer sans utiliser un nom qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="6cb81-106">An *import declaration* specifies a module or namespace whose elements you can reference without using a fully qualified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb81-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cb81-107">Syntax</span></span>

```fsharp
open module-or-namespace-name
```

## <a name="remarks"></a><span data-ttu-id="6cb81-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6cb81-108">Remarks</span></span>

<span data-ttu-id="6cb81-109">Faisant référence à code en utilisant le chemin qualifié complet de l’espace de noms ou module chaque fois pouvez créer le code qui est difficile à écrire, lire et mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="6cb81-109">Referencing code by using the fully qualified namespace or module path every time can create code that is hard to write, read, and maintain.</span></span> <span data-ttu-id="6cb81-110">Au lieu de cela, vous pouvez utiliser le `open` mot clé pour utilisé fréquemment des modules et les espaces de noms afin que lorsque vous référencez un membre de ce module ou un espace de noms, vous pouvez utiliser la forme abrégée du nom au lieu du nom qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="6cb81-110">Instead, you can use the `open` keyword for frequently used modules and namespaces so that when you reference a member of that module or namespace, you can use the short form of the name instead of the fully qualified name.</span></span> <span data-ttu-id="6cb81-111">Ce mot clé est similaire à la `using` mot clé en c#, `using namespace` dans Visual C++, et `Imports` en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6cb81-111">This keyword is similar to the `using` keyword in C#, `using namespace` in Visual C++, and `Imports` in Visual Basic.</span></span>

<span data-ttu-id="6cb81-112">Le module ou un espace de noms fourni doit être dans le même projet ou dans un projet ou assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="6cb81-112">The module or namespace provided must be in the same project or in a referenced project or assembly.</span></span> <span data-ttu-id="6cb81-113">Si elle n’est pas le cas, vous pouvez ajouter une référence au projet, ou utiliser le `-reference` commande`-`option de ligne (ou son abréviation, `-r`).</span><span class="sxs-lookup"><span data-stu-id="6cb81-113">If it is not, you can add a reference to the project, or use the `-reference` command`-`line option (or its abbreviation, `-r`).</span></span> <span data-ttu-id="6cb81-114">Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="6cb81-114">For more information, see [Compiler Options](compiler-options.md).</span></span>

<span data-ttu-id="6cb81-115">La déclaration d’importation rend les noms disponibles dans le code qui suit la déclaration, jusqu'à la fin de l’espace de noms, module ou fichier englobante.</span><span class="sxs-lookup"><span data-stu-id="6cb81-115">The import declaration makes the names available in the code that follows the declaration, up to the end of the enclosing namespace, module, or file.</span></span>

<span data-ttu-id="6cb81-116">Lorsque vous utilisez plusieurs déclarations d’importation, ils doivent apparaître sur des lignes distinctes.</span><span class="sxs-lookup"><span data-stu-id="6cb81-116">When you use multiple import declarations, they should appear on separate lines.</span></span>

<span data-ttu-id="6cb81-117">Le code suivant illustre l’utilisation de la `open` mot clé pour simplifier le code.</span><span class="sxs-lookup"><span data-stu-id="6cb81-117">The following code shows the use of the `open` keyword to simplify code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6801.fs)]

<span data-ttu-id="6cb81-118">Le compilateur F # n’émet pas une erreur ou un avertissement lorsque des ambiguïtés se produisent lorsque le même nom se produit dans plus d’un module open ou espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6cb81-118">The F# compiler does not emit an error or warning when ambiguities occur when the same name occurs in more than one open module or namespace.</span></span> <span data-ttu-id="6cb81-119">Lorsque des ambiguïtés se produisent, F # donne la priorité au module ou un espace de noms plus récemment ouverts.</span><span class="sxs-lookup"><span data-stu-id="6cb81-119">When ambiguities occur, F# gives preference to the more recently opened module or namespace.</span></span> <span data-ttu-id="6cb81-120">Par exemple, dans le code suivant, `empty` signifie `Seq.empty`, même si `empty` se trouve à la fois dans le `List` et `Seq` modules.</span><span class="sxs-lookup"><span data-stu-id="6cb81-120">For example, in the following code, `empty` means `Seq.empty`, even though `empty` is located in both the `List` and `Seq` modules.</span></span>

```fsharp
open List
open Seq
printfn "%A" empty
```

<span data-ttu-id="6cb81-121">Par conséquent, soyez prudent lorsque vous ouvrez des modules ou espaces de noms tels que `List` ou `Seq` qui contiennent des membres qui ont des noms identiques ; au lieu de cela, envisagez d’utiliser les noms qualifiés.</span><span class="sxs-lookup"><span data-stu-id="6cb81-121">Therefore, be careful when you open modules or namespaces such as `List` or `Seq` that contain members that have identical names; instead, consider using the qualified names.</span></span> <span data-ttu-id="6cb81-122">Vous devez éviter toute situation dans laquelle le code dépend de l’ordre des déclarations d’importation.</span><span class="sxs-lookup"><span data-stu-id="6cb81-122">You should avoid any situation in which the code is dependent upon the order of the import declarations.</span></span>

## <a name="namespaces-that-are-open-by-default"></a><span data-ttu-id="6cb81-123">Espaces de noms qui sont ouverts par défaut</span><span class="sxs-lookup"><span data-stu-id="6cb81-123">Namespaces That Are Open by Default</span></span>

<span data-ttu-id="6cb81-124">Certains espaces de noms sont si souvent utilisés dans le code F # qu’ils sont ouverts implicitement sans avoir besoin d’une déclaration d’importation explicite.</span><span class="sxs-lookup"><span data-stu-id="6cb81-124">Some namespaces are so frequently used in F# code that they are opened implicitly without the need of an explicit import declaration.</span></span> <span data-ttu-id="6cb81-125">Le tableau suivant présente les espaces de noms qui sont ouverts par défaut.</span><span class="sxs-lookup"><span data-stu-id="6cb81-125">The following table shows the namespaces that are open by default.</span></span>

|<span data-ttu-id="6cb81-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6cb81-126">Namespace</span></span>|<span data-ttu-id="6cb81-127">Description</span><span class="sxs-lookup"><span data-stu-id="6cb81-127">Description</span></span>|
|---------|-----------|
|`Microsoft.FSharp.Core`|<span data-ttu-id="6cb81-128">Contient des définitions de type F # de base pour les types intégrés tels que `int` et `float`.</span><span class="sxs-lookup"><span data-stu-id="6cb81-128">Contains basic F# type definitions for built-in types such as `int` and `float`.</span></span>|
|`Microsoft.FSharp.Core.Operators`|<span data-ttu-id="6cb81-129">Contient des opérations arithmétiques de base telles que `+` et `*`.</span><span class="sxs-lookup"><span data-stu-id="6cb81-129">Contains basic arithmetic operations such as `+` and `*`.</span></span>|
|`Microsoft.FSharp.Collections`|<span data-ttu-id="6cb81-130">Contient des classes de collection immuable comme `List` et `Array`.</span><span class="sxs-lookup"><span data-stu-id="6cb81-130">Contains immutable collection classes such as `List` and `Array`.</span></span>|
|`Microsoft.FSharp.Control`|<span data-ttu-id="6cb81-131">Contient des types pour les constructions de contrôle telles que l’évaluation paresseuse et flux de travail asynchrones.</span><span class="sxs-lookup"><span data-stu-id="6cb81-131">Contains types for control constructs such as lazy evaluation and asynchronous workflows.</span></span>|
|`Microsoft.FSharp.Text`|<span data-ttu-id="6cb81-132">Contient des fonctions pour les e/s mise en forme, telles que le `printf` (fonction).</span><span class="sxs-lookup"><span data-stu-id="6cb81-132">Contains functions for formatted IO, such as the `printf` function.</span></span>|

## <a name="autoopen-attribute"></a><span data-ttu-id="6cb81-133">AutoOpen (attribut)</span><span class="sxs-lookup"><span data-stu-id="6cb81-133">AutoOpen Attribute</span></span>

<span data-ttu-id="6cb81-134">Vous pouvez appliquer le `AutoOpen` d’attribut à un assembly si vous souhaitez ouvrir automatiquement un espace de noms ou un module à l’assembly est référencé.</span><span class="sxs-lookup"><span data-stu-id="6cb81-134">You can apply the `AutoOpen` attribute to an assembly if you want to automatically open a namespace or module when the assembly is referenced.</span></span> <span data-ttu-id="6cb81-135">Vous pouvez également appliquer le `AutoOpen` d’attribut à un module pour ouvrir automatiquement ce module lorsque le module parent ou un espace de noms est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6cb81-135">You can also apply the `AutoOpen` attribute to a module to automatically open that module when the parent module or namespace is opened.</span></span> <span data-ttu-id="6cb81-136">Pour plus d’informations, consultez [Core.AutoOpenAttribute, classe](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.autoopenattribute-class-%5bfsharp%5d).</span><span class="sxs-lookup"><span data-stu-id="6cb81-136">For more information, see [Core.AutoOpenAttribute Class](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.autoopenattribute-class-%5bfsharp%5d).</span></span>

## <a name="requirequalifiedaccess-attribute"></a><span data-ttu-id="6cb81-137">RequireQualifiedAccess (attribut)</span><span class="sxs-lookup"><span data-stu-id="6cb81-137">RequireQualifiedAccess Attribute</span></span>

<span data-ttu-id="6cb81-138">Certains modules, des enregistrements ou les types d’union peuvent spécifier le `RequireQualifiedAccess` attribut.</span><span class="sxs-lookup"><span data-stu-id="6cb81-138">Some modules, records, or union types may specify the `RequireQualifiedAccess` attribute.</span></span> <span data-ttu-id="6cb81-139">Lorsque vous référencez des éléments de ces modules, des enregistrements ou unions, vous devez utiliser un nom qualifié, quel que soit ou non d’une déclaration d’importation.</span><span class="sxs-lookup"><span data-stu-id="6cb81-139">When you reference elements of those modules, records, or unions, you must use a qualified name regardless of whether you include an import declaration.</span></span> <span data-ttu-id="6cb81-140">Si vous utilisez cet attribut de façon stratégique sur les types qui définissent généralement utilisé des noms, vous aider à éviter les collisions de nom et code rendre plus résistante aux modifications dans les bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="6cb81-140">If you use this attribute strategically on types that define commonly used names, you help avoid name collisions and thereby make code more resilient to changes in libraries.</span></span> <span data-ttu-id="6cb81-141">Pour plus d’informations, consultez [Core.RequireQualifiedAccessAttribute, classe](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.requirequalifiedaccessattribute-class-%5Bfsharp%5D).</span><span class="sxs-lookup"><span data-stu-id="6cb81-141">For more information, see [Core.RequireQualifiedAccessAttribute Class](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.requirequalifiedaccessattribute-class-%5Bfsharp%5D).</span></span>

## <a name="see-also"></a><span data-ttu-id="6cb81-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cb81-142">See also</span></span>

- [<span data-ttu-id="6cb81-143"># Référence du langage</span><span class="sxs-lookup"><span data-stu-id="6cb81-143"># Language Reference</span></span>](index.md)
- [<span data-ttu-id="6cb81-144">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="6cb81-144">Namespaces</span></span>](namespaces.md)
- [<span data-ttu-id="6cb81-145">Modules</span><span class="sxs-lookup"><span data-stu-id="6cb81-145">Modules</span></span>](modules.md)
