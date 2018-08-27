---
title: partial, type (référence C#)
ms.date: 07/20/2015
f1_keywords:
- partialtype
- partialtype_CSharpKeyword
helpviewer_keywords:
- partial types [C#]
ms.assetid: 27320743-a22e-4c7b-b0b3-53afe3607334
ms.openlocfilehash: 362a02815cb249d57c0bd19706714df1d71644f4
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42929661"
---
# <a name="partial-type-c-reference"></a><span data-ttu-id="18b76-102">partial, type (référence C#)</span><span class="sxs-lookup"><span data-stu-id="18b76-102">partial (Type) (C# Reference)</span></span>
<span data-ttu-id="18b76-103">Les définitions de type partiel permettent le fractionnement de la définition d’une classe, d’un struct ou d’une interface entre plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="18b76-103">Partial type definitions allow for the definition of a class, struct, or interface to be split into multiple files.</span></span>  
  
 <span data-ttu-id="18b76-104">Dans File1.cs :</span><span class="sxs-lookup"><span data-stu-id="18b76-104">In File1.cs:</span></span>  
  
 [!code-csharp[csrefKeywordsContextual#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/partial-type_1.cs)]  
  
 <span data-ttu-id="18b76-105">Déclaration dans File2.cs :</span><span class="sxs-lookup"><span data-stu-id="18b76-105">In File2.cs the declaration:</span></span>  
  
 [!code-csharp[csrefKeywordsContextual#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/partial-type_2.cs)]  
  
## <a name="remarks"></a><span data-ttu-id="18b76-106">Notes</span><span class="sxs-lookup"><span data-stu-id="18b76-106">Remarks</span></span>  
 <span data-ttu-id="18b76-107">Fractionner un type de classe, de struct ou d’interface entre plusieurs fichiers peut être utile si vous travaillez sur des projets volumineux ou des projets contenant du code généré automatiquement, comme celui fourni par le [Concepteur Windows Forms](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="18b76-107">Splitting a class, struct or interface type over several files can be useful when you are working with large projects, or with automatically generated code such as that provided by the [Windows Forms Designer](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md).</span></span> <span data-ttu-id="18b76-108">Un type partiel peut contenir une [méthode partielle](../../../csharp/language-reference/keywords/partial-method.md).</span><span class="sxs-lookup"><span data-stu-id="18b76-108">A partial type may contain a [partial method](../../../csharp/language-reference/keywords/partial-method.md).</span></span> <span data-ttu-id="18b76-109">Pour plus d’informations, consultez [Classes et méthodes partielles](../../../csharp/programming-guide/classes-and-structs/partial-classes-and-methods.md).</span><span class="sxs-lookup"><span data-stu-id="18b76-109">For more information, see [Partial Classes and Methods](../../../csharp/programming-guide/classes-and-structs/partial-classes-and-methods.md).</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="18b76-110">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="18b76-110">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="18b76-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18b76-111">See Also</span></span>

- [<span data-ttu-id="18b76-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="18b76-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="18b76-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="18b76-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="18b76-114">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="18b76-114">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)  
- [<span data-ttu-id="18b76-115">Introduction aux génériques</span><span class="sxs-lookup"><span data-stu-id="18b76-115">Introduction to Generics</span></span>](../../../csharp/programming-guide/generics/introduction-to-generics.md)
