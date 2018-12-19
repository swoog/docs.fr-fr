---
title: public, mot clé - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- public
- public_CSharpKeyword
helpviewer_keywords:
- public keyword [C#]
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
ms.openlocfilehash: 15b86920736f1220553b462d103841ac98d88b7c
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53239301"
---
# <a name="public-c-reference"></a><span data-ttu-id="42c37-102">public (référence C#)</span><span class="sxs-lookup"><span data-stu-id="42c37-102">public (C# Reference)</span></span>

<span data-ttu-id="42c37-103">Le mot clé `public` est un modificateur d’accès pour les types et les membres de types.</span><span class="sxs-lookup"><span data-stu-id="42c37-103">The `public` keyword is an access modifier for types and type members.</span></span> <span data-ttu-id="42c37-104">L’accès public est le niveau d’accès le plus permissif.</span><span class="sxs-lookup"><span data-stu-id="42c37-104">Public access is the most permissive access level.</span></span> <span data-ttu-id="42c37-105">Il n’existe pas de restrictions d’accès aux membres publics, comme dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="42c37-105">There are no restrictions on accessing public members, as in this example:</span></span>

```csharp
class SampleClass
{
    public int x; // No access restrictions.
}
```

<span data-ttu-id="42c37-106">Pour plus d’informations, consultez [Modificateurs d’accès](../../programming-guide/classes-and-structs/access-modifiers.md) et [Niveaux d’accessibilité](accessibility-levels.md).</span><span class="sxs-lookup"><span data-stu-id="42c37-106">See [Access Modifiers](../../programming-guide/classes-and-structs/access-modifiers.md) and [Accessibility Levels](accessibility-levels.md) for more information.</span></span>

## <a name="example"></a><span data-ttu-id="42c37-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="42c37-107">Example</span></span>

<span data-ttu-id="42c37-108">Dans l’exemple suivant, deux classes sont déclarées, `PointTest` et `MainClass`.</span><span class="sxs-lookup"><span data-stu-id="42c37-108">In the following example, two classes are declared, `PointTest` and `MainClass`.</span></span> <span data-ttu-id="42c37-109">L’accès aux membres publics `x` et `y` de `PointTest` s’effectue directement à partir de `MainClass`.</span><span class="sxs-lookup"><span data-stu-id="42c37-109">The public members `x` and `y` of `PointTest` are accessed directly from `MainClass`.</span></span>

[!code-csharp[csrefKeywordsModifiers#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#13)]

<span data-ttu-id="42c37-110">Si vous remplacez le niveau d’accès `public` par [private](private.md) ou [protected](protected.md), le message d’erreur suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="42c37-110">If you change the `public` access level to [private](private.md) or [protected](protected.md), you will get the error message:</span></span>

<span data-ttu-id="42c37-111">'PointTest.y' est inaccessible en raison de son niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="42c37-111">'PointTest.y' is inaccessible due to its protection level.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="42c37-112">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="42c37-112">C# language specification</span></span>  

<span data-ttu-id="42c37-113">Pour plus d’informations, consultez [Accessibilité déclarée](~/_csharplang/spec/basic-concepts.md#declared-accessibility) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="42c37-113">For more information, see [Declared accessibility](~/_csharplang/spec/basic-concepts.md#declared-accessibility) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="42c37-114">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="42c37-114">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="42c37-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42c37-115">See also</span></span>

- [<span data-ttu-id="42c37-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="42c37-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="42c37-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="42c37-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="42c37-118">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="42c37-118">Access Modifiers</span></span>](../../programming-guide/classes-and-structs/access-modifiers.md)
- [<span data-ttu-id="42c37-119">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="42c37-119">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="42c37-120">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="42c37-120">Access Modifiers</span></span>](access-modifiers.md)
- [<span data-ttu-id="42c37-121">Niveaux d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="42c37-121">Accessibility Levels</span></span>](accessibility-levels.md)
- [<span data-ttu-id="42c37-122">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="42c37-122">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="42c37-123">private</span><span class="sxs-lookup"><span data-stu-id="42c37-123">private</span></span>](private.md)
- [<span data-ttu-id="42c37-124">protected</span><span class="sxs-lookup"><span data-stu-id="42c37-124">protected</span></span>](protected.md)
- [<span data-ttu-id="42c37-125">internal</span><span class="sxs-lookup"><span data-stu-id="42c37-125">internal</span></span>](internal.md)