---
title: void - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- void_CSharpKeyword
- void
helpviewer_keywords:
- void keyword [C#]
ms.assetid: 0d2d8a95-fe20-4fbd-bf5d-c1e54bce71d4
ms.openlocfilehash: af79d39282ea38811777ea1f23054120afc39d2c
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632952"
---
# <a name="void-c-reference"></a><span data-ttu-id="7ae6d-102">void (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="7ae6d-102">void (C# Reference)</span></span>

<span data-ttu-id="7ae6d-103">Quand le mot clé `void` est utilisé en tant que type de retour pour une méthode, il spécifie que cette méthode ne retourne aucune valeur.</span><span class="sxs-lookup"><span data-stu-id="7ae6d-103">When used as the return type for a method, `void` specifies that the method doesn't return a value.</span></span>

<span data-ttu-id="7ae6d-104">`void` n’est pas autorisé dans la liste des paramètres d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="7ae6d-104">`void` isn't allowed in the parameter list of a method.</span></span> <span data-ttu-id="7ae6d-105">Une méthode sans paramètres qui ne retourne aucune valeur se déclare comme suit :</span><span class="sxs-lookup"><span data-stu-id="7ae6d-105">A method that takes no parameters and returns no value is declared as follows:</span></span>

```csharp
public void SampleMethod()
{
    // Body of the method.
}
```

<span data-ttu-id="7ae6d-106">`void` est également utilisé dans un contexte unsafe pour déclarer un pointeur vers un type inconnu.</span><span class="sxs-lookup"><span data-stu-id="7ae6d-106">`void` is also used in an unsafe context to declare a pointer to an unknown type.</span></span> <span data-ttu-id="7ae6d-107">Pour plus d’informations, consultez [Types pointeur](../../programming-guide/unsafe-code-pointers/pointer-types.md).</span><span class="sxs-lookup"><span data-stu-id="7ae6d-107">For more information, see [Pointer types](../../programming-guide/unsafe-code-pointers/pointer-types.md).</span></span>

<span data-ttu-id="7ae6d-108">`void` est un alias du type <xref:System.Void?displayProperty=nameWithType> .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7ae6d-108">`void` is an alias for the .NET Framework <xref:System.Void?displayProperty=nameWithType> type.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="7ae6d-109">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="7ae6d-109">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="7ae6d-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ae6d-110">See also</span></span>

- [<span data-ttu-id="7ae6d-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="7ae6d-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="7ae6d-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="7ae6d-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="7ae6d-113">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="7ae6d-113">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="7ae6d-114">Types référence</span><span class="sxs-lookup"><span data-stu-id="7ae6d-114">Reference Types</span></span>](reference-types.md)
- [<span data-ttu-id="7ae6d-115">Types valeur</span><span class="sxs-lookup"><span data-stu-id="7ae6d-115">Value Types</span></span>](value-types.md)
- [<span data-ttu-id="7ae6d-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7ae6d-116">Methods</span></span>](../../programming-guide/classes-and-structs/methods.md)
- [<span data-ttu-id="7ae6d-117">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="7ae6d-117">Unsafe Code and Pointers</span></span>](../../programming-guide/unsafe-code-pointers/index.md)
