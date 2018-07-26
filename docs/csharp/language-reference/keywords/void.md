---
title: void (Référence C#)
ms.date: 07/20/2015
f1_keywords:
- void_CSharpKeyword
- void
helpviewer_keywords:
- void keyword [C#]
ms.assetid: 0d2d8a95-fe20-4fbd-bf5d-c1e54bce71d4
ms.openlocfilehash: e66efc287fc3ed0fcc15963a827fccb788c38753
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2018
ms.locfileid: "37960558"
---
# <a name="void-c-reference"></a><span data-ttu-id="ec98c-102">void (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="ec98c-102">void (C# Reference)</span></span>
<span data-ttu-id="ec98c-103">Quand le mot clé `void` est utilisé en tant que type de retour pour une méthode, il spécifie que cette méthode ne retourne aucune valeur.</span><span class="sxs-lookup"><span data-stu-id="ec98c-103">When used as the return type for a method, `void` specifies that the method doesn't return a value.</span></span>

<span data-ttu-id="ec98c-104">`void` n’est pas autorisé dans la liste des paramètres d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="ec98c-104">`void` isn't allowed in the parameter list of a method.</span></span> <span data-ttu-id="ec98c-105">Une méthode sans paramètres qui ne retourne aucune valeur se déclare comme suit :</span><span class="sxs-lookup"><span data-stu-id="ec98c-105">A method that takes no parameters and returns no value is declared as follows:</span></span>

```csharp
public void SampleMethod()
{
    // Body of the method.
}
```

<span data-ttu-id="ec98c-106">`void` est également utilisé dans un contexte unsafe pour déclarer un pointeur vers un type inconnu.</span><span class="sxs-lookup"><span data-stu-id="ec98c-106">`void` is also used in an unsafe context to declare a pointer to an unknown type.</span></span> <span data-ttu-id="ec98c-107">Pour plus d’informations, consultez [Types pointeur](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md).</span><span class="sxs-lookup"><span data-stu-id="ec98c-107">For more information, see [Pointer types](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md).</span></span>

<span data-ttu-id="ec98c-108">`void` est un alias du type <xref:System.Void?displayProperty=nameWithType> .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ec98c-108">`void` is an alias for the .NET Framework <xref:System.Void?displayProperty=nameWithType> type.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="ec98c-109">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="ec98c-109">C# Language Specification</span></span>
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="ec98c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec98c-110">See also</span></span>
 [<span data-ttu-id="ec98c-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ec98c-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="ec98c-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ec98c-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="ec98c-113">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="ec98c-113">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="ec98c-114">Types référence</span><span class="sxs-lookup"><span data-stu-id="ec98c-114">Reference Types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)  
 [<span data-ttu-id="ec98c-115">Types valeur</span><span class="sxs-lookup"><span data-stu-id="ec98c-115">Value Types</span></span>](../../../csharp/language-reference/keywords/value-types.md)  
 [<span data-ttu-id="ec98c-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ec98c-116">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)  
 [<span data-ttu-id="ec98c-117">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="ec98c-117">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)
