---
title: value (référence C#)
ms.date: 07/20/2015
f1_keywords:
- value_CSharpKeyword
helpviewer_keywords:
- value keyword [C#]
ms.assetid: c99d6468-687f-4a46-89b4-a95e1b00bf6d
ms.openlocfilehash: 1e120d68fc4a42f24feb225f652c14525fde3d71
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43521144"
---
# <a name="value-c-reference"></a><span data-ttu-id="3acd7-102">value (référence C#)</span><span class="sxs-lookup"><span data-stu-id="3acd7-102">value (C# Reference)</span></span>
<span data-ttu-id="3acd7-103">Le mot clé contextuel `value` est utilisé dans l’accesseur set de déclarations de propriété ordinaires.</span><span class="sxs-lookup"><span data-stu-id="3acd7-103">The contextual keyword `value` is used in the set accessor in ordinary property declarations.</span></span> <span data-ttu-id="3acd7-104">Il est similaire à un paramètre d’entrée sur une méthode.</span><span class="sxs-lookup"><span data-stu-id="3acd7-104">It is similar to an input parameter on a method.</span></span> <span data-ttu-id="3acd7-105">Le mot `value` fait référence à la valeur que le code client tente d’assigner à la propriété.</span><span class="sxs-lookup"><span data-stu-id="3acd7-105">The word `value` references the value that client code is attempting to assign to the property.</span></span> <span data-ttu-id="3acd7-106">Dans l’exemple suivant, `MyDerivedClass` a une propriété appelée `Name` qui utilise le paramètre `value` pour assigner une nouvelle chaîne au `name` du champ de stockage.</span><span class="sxs-lookup"><span data-stu-id="3acd7-106">In the following example, `MyDerivedClass` has a property called `Name` that uses the `value` parameter to assign a new string to the backing field `name`.</span></span> <span data-ttu-id="3acd7-107">Du point de vue du code client, l’opération est écrite comme une assignation simple.</span><span class="sxs-lookup"><span data-stu-id="3acd7-107">From the point of view of client code, the operation is written as a simple assignment.</span></span>  
  
 [!code-csharp[csrefKeywordsModifiers#26](../../../csharp/language-reference/keywords/codesnippet/CSharp/value_1.cs)]  
  
 <span data-ttu-id="3acd7-108">Pour plus d’informations sur l’utilisation de `value`, consultez [Propriétés](../../../csharp/programming-guide/classes-and-structs/properties.md).</span><span class="sxs-lookup"><span data-stu-id="3acd7-108">For more information about the use of `value`, see [Properties](../../../csharp/programming-guide/classes-and-structs/properties.md).</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="3acd7-109">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="3acd7-109">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3acd7-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3acd7-110">See Also</span></span>

- [<span data-ttu-id="3acd7-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="3acd7-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="3acd7-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="3acd7-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="3acd7-113">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="3acd7-113">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
