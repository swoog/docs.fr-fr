---
title: '[], opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- '[]_CSharpKeyword'
helpviewer_keywords:
- subscript operator [C#]
- square brackets [ ] operator [C#]
- '[] operator [C#]'
- indexing operator [C#]
ms.assetid: 5c16bb45-88f7-45ff-b42c-1af1972b042c
ms.openlocfilehash: 65908bb3bcd8912ef81fc094e5958ae8dc4ae1f1
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2018
ms.locfileid: "37961438"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="9f7c0-102">[], opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9f7c0-102">[] Operator (C# Reference)</span></span>
<span data-ttu-id="9f7c0-103">Les crochets (`[]`) sont utilisés pour les tableaux, les indexeurs et les attributs.</span><span class="sxs-lookup"><span data-stu-id="9f7c0-103">Square brackets (`[]`) are used for arrays, indexers, and attributes.</span></span> <span data-ttu-id="9f7c0-104">Ils peuvent également être utilisés avec les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="9f7c0-104">They can also be used with pointers.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9f7c0-105">Notes</span><span class="sxs-lookup"><span data-stu-id="9f7c0-105">Remarks</span></span>  
 <span data-ttu-id="9f7c0-106">Un type tableau est un type suivi de `[]` :</span><span class="sxs-lookup"><span data-stu-id="9f7c0-106">An array type is a type followed by `[]`:</span></span>  
  
 [!code-csharp[csRefOperators#43](../../../csharp/language-reference/operators/codesnippet/CSharp/index-operator_1.cs)]  
  
 <span data-ttu-id="9f7c0-107">Pour accéder à un élément d’un tableau, vous devez placer l’index de l’élément souhaité entre crochets :</span><span class="sxs-lookup"><span data-stu-id="9f7c0-107">To access an element of an array, the index of the desired element is enclosed in brackets:</span></span>  
  
 [!code-csharp[csRefOperators#44](../../../csharp/language-reference/operators/codesnippet/CSharp/index-operator_2.cs)]  
  
 <span data-ttu-id="9f7c0-108">Une exception est levée si un index de tableau est hors portée.</span><span class="sxs-lookup"><span data-stu-id="9f7c0-108">An exception is thrown if an array index is out of range.</span></span>  
  
 <span data-ttu-id="9f7c0-109">L’opérateur d’indexation de tableau ne peut pas être surchargé. Toutefois, les types peuvent définir les indexeurs, ainsi que les propriétés qui acceptent un ou plusieurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="9f7c0-109">The array indexing operator cannot be overloaded; however, types can define indexers, and properties that take one or more parameters.</span></span> <span data-ttu-id="9f7c0-110">Les paramètres d’indexeur sont placés entre crochets, comme les index de tableau, mais ils peuvent être déclarés comme étant de tout type, contrairement aux index de tableau, qui doivent être intégraux.</span><span class="sxs-lookup"><span data-stu-id="9f7c0-110">Indexer parameters are enclosed in square brackets, just like array indexes, but indexer parameters can be declared to be of any type, unlike array indexes, which must be integral.</span></span>  
  
 <span data-ttu-id="9f7c0-111">Par exemple, le .NET Framework définit un type `Hashtable` qui associe des clés et des valeurs de type arbitraire :</span><span class="sxs-lookup"><span data-stu-id="9f7c0-111">For example, the .NET Framework defines a `Hashtable` type that associates keys and values of arbitrary type:</span></span>  
  
 [!code-csharp[csRefOperators#45](../../../csharp/language-reference/operators/codesnippet/CSharp/index-operator_3.cs)]  
  
 <span data-ttu-id="9f7c0-112">Les crochets sont également utilisés pour spécifier des [attributs](../../../csharp/programming-guide/concepts/attributes/index.md) :</span><span class="sxs-lookup"><span data-stu-id="9f7c0-112">Square brackets are also used to specify [Attributes](../../../csharp/programming-guide/concepts/attributes/index.md):</span></span>  
  
 [!code-csharp[csRefOperators#46](../../../csharp/language-reference/operators/codesnippet/CSharp/index-operator_4.cs)]  
  
 <span data-ttu-id="9f7c0-113">Vous pouvez utiliser des crochets pour indexer un pointeur :</span><span class="sxs-lookup"><span data-stu-id="9f7c0-113">You can use square brackets to index off a pointer:</span></span>  
  
 [!code-csharp[csRefOperators#47](../../../csharp/language-reference/operators/codesnippet/CSharp/index-operator_5.cs)]  
  
 <span data-ttu-id="9f7c0-114">Aucune vérification des limites n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="9f7c0-114">No bounds checking is performed.</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="9f7c0-115">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9f7c0-115">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9f7c0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f7c0-116">See Also</span></span>  
 [<span data-ttu-id="9f7c0-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9f7c0-117">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="9f7c0-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9f7c0-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="9f7c0-119">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="9f7c0-119">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
 [<span data-ttu-id="9f7c0-120">Tableaux</span><span class="sxs-lookup"><span data-stu-id="9f7c0-120">Arrays</span></span>](../../../csharp/programming-guide/arrays/index.md)  
 [<span data-ttu-id="9f7c0-121">Indexeurs</span><span class="sxs-lookup"><span data-stu-id="9f7c0-121">Indexers</span></span>](../../../csharp/programming-guide/indexers/index.md)  
 [<span data-ttu-id="9f7c0-122">unsafe</span><span class="sxs-lookup"><span data-stu-id="9f7c0-122">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)  
 [<span data-ttu-id="9f7c0-123">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="9f7c0-123">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
