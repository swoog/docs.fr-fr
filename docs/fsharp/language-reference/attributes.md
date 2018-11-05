---
title: Attributs (F#)
description: Découvrez comment F# attributs activer les métadonnées à appliquer à une construction de programmation.
ms.date: 05/16/2016
ms.openlocfilehash: 3e7f1d0ff383e1070b3db72e633f80ea37150548
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "49121751"
---
# <a name="attributes"></a><span data-ttu-id="64b39-103">Attributs</span><span class="sxs-lookup"><span data-stu-id="64b39-103">Attributes</span></span>

<span data-ttu-id="64b39-104">Attributs activent les métadonnées à appliquer à une construction de programmation.</span><span class="sxs-lookup"><span data-stu-id="64b39-104">Attributes enable metadata to be applied to a programming construct.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b39-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64b39-105">Syntax</span></span>

```fsharp
[<target:attribute-name(arguments)>]
```

## <a name="remarks"></a><span data-ttu-id="64b39-106">Notes</span><span class="sxs-lookup"><span data-stu-id="64b39-106">Remarks</span></span>

<span data-ttu-id="64b39-107">Dans la syntaxe précédente, le *cible* est facultatif et, s’il est présent, spécifie le type d’entité de programme qui l’attribut s’applique à.</span><span class="sxs-lookup"><span data-stu-id="64b39-107">In the previous syntax, the *target* is optional and, if present, specifies the kind of program entity that the attribute applies to.</span></span> <span data-ttu-id="64b39-108">Les valeurs valides pour *cible* figurent dans le tableau situé plus loin dans ce document.</span><span class="sxs-lookup"><span data-stu-id="64b39-108">Valid values for *target* are shown in the table that appears later in this document.</span></span>

<span data-ttu-id="64b39-109">Le *nom de l’attribut* fait référence au nom (éventuellement qualifié avec des espaces de noms) d’un type d’attribut valide, avec ou sans le suffixe `Attribute` qui est généralement utilisé dans les noms de type d’attribut.</span><span class="sxs-lookup"><span data-stu-id="64b39-109">The *attribute-name* refers to the name (possibly qualified with namespaces) of a valid attribute type, with or without the suffix `Attribute` that is usually used in attribute type names.</span></span> <span data-ttu-id="64b39-110">Par exemple, le type `ObsoleteAttribute` peut être abrégé en `Obsolete` dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="64b39-110">For example, the type `ObsoleteAttribute` can be shortened to just `Obsolete` in this context.</span></span>

<span data-ttu-id="64b39-111">Le *arguments* sont les arguments au constructeur pour le type d’attribut.</span><span class="sxs-lookup"><span data-stu-id="64b39-111">The *arguments* are the arguments to the constructor for the attribute type.</span></span> <span data-ttu-id="64b39-112">Si un attribut possède un constructeur par défaut, la liste d’arguments et les parenthèses peuvent être omis.</span><span class="sxs-lookup"><span data-stu-id="64b39-112">If an attribute has a default constructor, the argument list and parentheses can be omitted.</span></span> <span data-ttu-id="64b39-113">Attributs prennent en charge les arguments positionnels et des arguments nommés.</span><span class="sxs-lookup"><span data-stu-id="64b39-113">Attributes support both positional arguments and named arguments.</span></span> <span data-ttu-id="64b39-114">*Arguments de position* sont des arguments qui sont utilisés dans l’ordre dans lequel ils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="64b39-114">*Positional arguments* are arguments that are used in the order in which they appear.</span></span> <span data-ttu-id="64b39-115">Arguments nommés peuvent être utilisés si l’attribut a des propriétés publiques.</span><span class="sxs-lookup"><span data-stu-id="64b39-115">Named arguments can be used if the attribute has public properties.</span></span> <span data-ttu-id="64b39-116">Vous pouvez les définir à l’aide de la syntaxe suivante dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="64b39-116">You can set these by using the following syntax in the argument list.</span></span>

```
*property-name* = *property-value*
```

<span data-ttu-id="64b39-117">Ces initialisations de propriété peuvent être dans n’importe quel ordre, mais ils doivent suivre les arguments positionnels.</span><span class="sxs-lookup"><span data-stu-id="64b39-117">Such property initializations can be in any order, but they must follow any positional arguments.</span></span> <span data-ttu-id="64b39-118">Voici un exemple d’un attribut qui utilise des arguments positionnels et des initialisations de propriété.</span><span class="sxs-lookup"><span data-stu-id="64b39-118">Following is an example of an attribute that uses positional arguments and property initializations.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6202.fs)]

<span data-ttu-id="64b39-119">Dans cet exemple, l’attribut est `DllImportAttribute`, utilisé ici sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="64b39-119">In this example, the attribute is `DllImportAttribute`, here used in shortened form.</span></span> <span data-ttu-id="64b39-120">Le premier argument est un paramètre positionnel et le second est une propriété.</span><span class="sxs-lookup"><span data-stu-id="64b39-120">The first argument is a positional parameter and the second is a property.</span></span>

<span data-ttu-id="64b39-121">Les attributs sont une construction de programmation .NET qui permet à un objet appelé un *attribut* à associer à un type ou un autre élément de programme.</span><span class="sxs-lookup"><span data-stu-id="64b39-121">Attributes are a .NET programming construct that enables an object known as an *attribute* to be associated with a type or other program element.</span></span> <span data-ttu-id="64b39-122">L’élément de programme auquel un attribut est appliqué est appelé le *cible de l’attribut*.</span><span class="sxs-lookup"><span data-stu-id="64b39-122">The program element to which an attribute is applied is known as the *attribute target*.</span></span> <span data-ttu-id="64b39-123">L’attribut contient généralement des métadonnées sur sa cible.</span><span class="sxs-lookup"><span data-stu-id="64b39-123">The attribute usually contains metadata about its target.</span></span> <span data-ttu-id="64b39-124">Dans ce contexte, les métadonnées peuvent être des données sur le type autre que les champs et leurs membres.</span><span class="sxs-lookup"><span data-stu-id="64b39-124">In this context, metadata could be any data about the type other than its fields and members.</span></span>

<span data-ttu-id="64b39-125">Attributs en F# peuvent être appliqués pour les constructions de programmation suivantes : fonctions, méthodes, assemblys, modules, types (classes, enregistrements, structures, interfaces, délégués, énumérations, unions et ainsi de suite), constructeurs, propriétés, champs, paramètres, paramètres de type et les valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="64b39-125">Attributes in F# can be applied to the following programming constructs: functions, methods, assemblies, modules, types (classes, records, structures, interfaces, delegates, enumerations, unions, and so on), constructors, properties, fields, parameters, type parameters, and return values.</span></span> <span data-ttu-id="64b39-126">Les attributs ne sont pas autorisées sur `let` liaisons à l’intérieur des classes, des expressions ou des expressions de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="64b39-126">Attributes are not allowed on `let` bindings inside classes, expressions, or workflow expressions.</span></span>

<span data-ttu-id="64b39-127">En règle générale, la déclaration d’attribut apparaît directement avant la déclaration de l’attribut cible.</span><span class="sxs-lookup"><span data-stu-id="64b39-127">Typically, the attribute declaration appears directly before the declaration of the attribute target.</span></span> <span data-ttu-id="64b39-128">Plusieurs déclarations d’attribut peuvent être utilisées ensemble, comme suit.</span><span class="sxs-lookup"><span data-stu-id="64b39-128">Multiple attribute declarations can be used together, as follows.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6603.fs)]

<span data-ttu-id="64b39-129">Vous pouvez interroger les attributs au moment de l’exécution en utilisant la réflexion .NET.</span><span class="sxs-lookup"><span data-stu-id="64b39-129">You can query attributes at run time by using .NET reflection.</span></span>

<span data-ttu-id="64b39-130">Vous pouvez déclarer plusieurs attributs individuellement, comme dans l’exemple de code précédent, ou vous pouvez les déclarer dans un jeu de crochets si vous utilisez un point-virgule pour séparer les différents attributs et les constructeurs, comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="64b39-130">You can declare multiple attributes individually, as in the previous code example, or you can declare them in one set of brackets if you use a semicolon to separate the individual attributes and constructors, as shown here.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6604.fs)]

<span data-ttu-id="64b39-131">Attributs généralement rencontrés incluent le `Obsolete` attribut, les attributs en matière de sécurité, les attributs de prise en charge COM, les attributs qui se rapportent à la propriété de code et les attributs indiquant si un type peut être sérialisé.</span><span class="sxs-lookup"><span data-stu-id="64b39-131">Typically encountered attributes include the `Obsolete` attribute, attributes for security considerations, attributes for COM support, attributes that relate to ownership of code, and attributes indicating whether a type can be serialized.</span></span> <span data-ttu-id="64b39-132">L’exemple suivant illustre l’utilisation de la `Obsolete` attribut.</span><span class="sxs-lookup"><span data-stu-id="64b39-132">The following example demonstrates the use of the `Obsolete` attribute.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6605.fs)]

<span data-ttu-id="64b39-133">Pour les cibles d’attribut `assembly` et `module`, vous appliquez les attributs à un niveau supérieur `do` liaison dans votre assembly.</span><span class="sxs-lookup"><span data-stu-id="64b39-133">For the attribute targets `assembly` and `module`, you apply the attributes to a top-level `do` binding in your assembly.</span></span> <span data-ttu-id="64b39-134">Vous pouvez inclure le mot `assembly` ou `module` dans la déclaration d’attribut, comme suit.</span><span class="sxs-lookup"><span data-stu-id="64b39-134">You can include the word `assembly` or `module` in the attribute declaration, as follows.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6606.fs)]

<span data-ttu-id="64b39-135">Si vous omettez la cible d’attribut pour un attribut appliqué à un `do` de liaison, le compilateur F# tente de déterminer la cible d’attribut qui a du sens pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="64b39-135">If you omit the attribute target for an attribute applied to a `do` binding, the F# compiler attempts to determine the attribute target that makes sense for that attribute.</span></span> <span data-ttu-id="64b39-136">Plusieurs classes d’attributs ont un attribut de type `System.AttributeUsageAttribute` qui inclut des informations sur les cibles possibles prises en charge pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="64b39-136">Many attribute classes have an attribute of type `System.AttributeUsageAttribute` that includes information about the possible targets supported for that attribute.</span></span> <span data-ttu-id="64b39-137">Si le `System.AttributeUsageAttribute` indique que l’attribut prend en charge les fonctions en tant que cibles, l’attribut est pris à appliquer au point d’entrée principal du programme.</span><span class="sxs-lookup"><span data-stu-id="64b39-137">If the `System.AttributeUsageAttribute` indicates that the attribute supports functions as targets, the attribute is taken to apply to the main entry point of the program.</span></span> <span data-ttu-id="64b39-138">Si le `System.AttributeUsageAttribute` indique que l’attribut prend en charge les assemblys en tant que cibles, le compilateur prend l’attribut à appliquer à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="64b39-138">If the `System.AttributeUsageAttribute` indicates that the attribute supports assemblies as targets, the compiler takes the attribute to apply to the assembly.</span></span> <span data-ttu-id="64b39-139">La plupart des attributs ne s’appliquent pas aux fonctions et assemblys, mais dans les cas où ils le font, l’attribut est effectuée à appliquer à la fonction principale du programme.</span><span class="sxs-lookup"><span data-stu-id="64b39-139">Most attributes do not apply to both functions and assemblies, but in cases where they do, the attribute is taken to apply to the program's main function.</span></span> <span data-ttu-id="64b39-140">Si la cible d’attribut est spécifiée explicitement, l’attribut est appliqué à la cible spécifiée.</span><span class="sxs-lookup"><span data-stu-id="64b39-140">If the attribute target is specified explicitly, the attribute is applied to the specified target.</span></span>

<span data-ttu-id="64b39-141">Bien que vous n’avez généralement pas besoin de spécifier l’attribut cible explicitement, les valeurs valides pour *cible* dans un attribut sont affichés dans le tableau ci-dessous, ainsi que des exemples d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="64b39-141">Although you do not usually need to specify the attribute target explicitly, valid values for *target* in an attribute are shown in the following table, along with examples of usage.</span></span>

<table>
  <tr>
    <th><span data-ttu-id="64b39-142">Cible d’attribut</span><span class="sxs-lookup"><span data-stu-id="64b39-142">Attribute target</span></span></td>
    <th><span data-ttu-id="64b39-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="64b39-143">Example</span></span></td> 
  </tr>
  <tr>
    <td><span data-ttu-id="64b39-144">assembly</span><span class="sxs-lookup"><span data-stu-id="64b39-144">assembly</span></span></td>
    <td><span data-ttu-id="64b39-145">`[<assembly: AssemblyVersionAttribute("1.0.0.0")>]`</span><span class="sxs-lookup"><span data-stu-id="64b39-145">`[<assembly: AssemblyVersionAttribute("1.0.0.0")>]`</span></span></td> 
  </tr>
  <tr>
    <td><span data-ttu-id="64b39-146">return</span><span class="sxs-lookup"><span data-stu-id="64b39-146">return</span></span></td>
    <td><span data-ttu-id="64b39-147">' fonction1 permettent de x : [<return: Obsolete>] int = x + 1'</span><span class="sxs-lookup"><span data-stu-id="64b39-147">`let function1 x : [<return: Obsolete>] int = x + 1`</span></span></td> 
  </tr>
  <tr>
    <td><span data-ttu-id="64b39-148">champ</span><span class="sxs-lookup"><span data-stu-id="64b39-148">field</span></span></td>
    <td><span data-ttu-id="64b39-149">« [<field: DefaultValue>] x: int mutable val »</span><span class="sxs-lookup"><span data-stu-id="64b39-149">`[<field: DefaultValue>] val mutable x: int`</span></span></td> 
  </tr>
  <tr>
    <td><span data-ttu-id="64b39-150">propriété</span><span class="sxs-lookup"><span data-stu-id="64b39-150">property</span></span></td>
    <td><span data-ttu-id="64b39-151">' [<property: Obsolete>] cela. MyProperty = x'</span><span class="sxs-lookup"><span data-stu-id="64b39-151">`[<property: Obsolete>] this.MyProperty = x`</span></span></td> 
  </tr>
  <tr>
    <td><span data-ttu-id="64b39-152">param</span><span class="sxs-lookup"><span data-stu-id="64b39-152">param</span></span></td>
    <td><span data-ttu-id="64b39-153">' membre cela. MyMethod ([<param: Out>] x : ref<int>) = x : = 10'</span><span class="sxs-lookup"><span data-stu-id="64b39-153">`member this.MyMethod([<param: Out>] x : ref<int>) = x := 10`</span></span></td> 
  </tr>
  <tr>
    <td><span data-ttu-id="64b39-154">type</span><span class="sxs-lookup"><span data-stu-id="64b39-154">type</span></span></td>
    <td><span data-ttu-id="64b39-155">
        ```
        [<type: StructLayout(Sequential)>] tapez MyStruct = struct x : y de l’octet : int fin ```
    </span><span class="sxs-lookup"><span data-stu-id="64b39-155">
        ```
        [<type: StructLayout(Sequential)>] type MyStruct = struct x : byte y : int end ```
    </span></span></td> 
  </tr>
</table>

## <a name="see-also"></a><span data-ttu-id="64b39-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64b39-156">See also</span></span>

- [<span data-ttu-id="64b39-157">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="64b39-157">F# Language Reference</span></span>](index.md)
