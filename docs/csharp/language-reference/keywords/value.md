---
title: value, mot clé contextuel - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- value_CSharpKeyword
helpviewer_keywords:
- value keyword [C#]
ms.assetid: c99d6468-687f-4a46-89b4-a95e1b00bf6d
ms.openlocfilehash: ee80888a57e999fa44e891dd6e0d64caa698009c
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612060"
---
# <a name="value-c-reference"></a><span data-ttu-id="9769b-102">value (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9769b-102">value (C# Reference)</span></span>

<span data-ttu-id="9769b-103">Le mot clé contextuel `value` est utilisé dans l’accesseur set de déclarations de propriété ordinaires.</span><span class="sxs-lookup"><span data-stu-id="9769b-103">The contextual keyword `value` is used in the set accessor in ordinary property declarations.</span></span> <span data-ttu-id="9769b-104">Il est similaire à un paramètre d’entrée sur une méthode.</span><span class="sxs-lookup"><span data-stu-id="9769b-104">It is similar to an input parameter on a method.</span></span> <span data-ttu-id="9769b-105">Le mot `value` fait référence à la valeur que le code client tente d’assigner à la propriété.</span><span class="sxs-lookup"><span data-stu-id="9769b-105">The word `value` references the value that client code is attempting to assign to the property.</span></span> <span data-ttu-id="9769b-106">Dans l’exemple suivant, `MyDerivedClass` a une propriété appelée `Name` qui utilise le paramètre `value` pour assigner une nouvelle chaîne au `name` du champ de stockage.</span><span class="sxs-lookup"><span data-stu-id="9769b-106">In the following example, `MyDerivedClass` has a property called `Name` that uses the `value` parameter to assign a new string to the backing field `name`.</span></span> <span data-ttu-id="9769b-107">Du point de vue du code client, l’opération est écrite comme une assignation simple.</span><span class="sxs-lookup"><span data-stu-id="9769b-107">From the point of view of client code, the operation is written as a simple assignment.</span></span>

[!code-csharp[csrefKeywordsModifiers#26](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#26)]

<span data-ttu-id="9769b-108">Pour plus d’informations sur l’utilisation de `value`, consultez [Propriétés](../../programming-guide/classes-and-structs/properties.md).</span><span class="sxs-lookup"><span data-stu-id="9769b-108">For more information about the use of `value`, see [Properties](../../programming-guide/classes-and-structs/properties.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="9769b-109">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9769b-109">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="9769b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9769b-110">See also</span></span>

- [<span data-ttu-id="9769b-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9769b-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="9769b-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9769b-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="9769b-113">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="9769b-113">C# Keywords</span></span>](index.md)