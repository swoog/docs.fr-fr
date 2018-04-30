---
title: '* , opérateur (Informations de référence sur C#)'
ms.date: 04/04/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '*_CSharpKeyword'
helpviewer_keywords:
- multiplication operator (*) [C#]
- '* operator [C#]'
ms.assetid: abd9a5f0-9b24-431e-971a-09ee1c45c50e
caps.latest.revision: 14
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 07d06d668ba43ebc3f4fae394d7b6641b122f4a6
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="-operator-c-reference"></a><span data-ttu-id="b740c-102">\*, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b740c-102">\* Operator (C# Reference)</span></span>
<span data-ttu-id="b740c-103">L’opérateur de multiplication (`*`) calcule le produit de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="b740c-103">The multiplication operator (`*`) computes the product of its operands.</span></span> <span data-ttu-id="b740c-104">Tous les types numériques ont des opérateurs de multiplication prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="b740c-104">All numeric types have predefined multiplication operators.</span></span>  

<span data-ttu-id="b740c-105">Par ailleurs, `*` sert d’opérateur de déréférencement qui permet de lire un pointeur et d’écrire sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b740c-105">`*` also serves as the dereference operator, which allows reading and writing to a pointer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b740c-106">Notes</span><span class="sxs-lookup"><span data-stu-id="b740c-106">Remarks</span></span>  
 <span data-ttu-id="b740c-107">L’opérateur `*` est aussi utilisé pour déclarer des types pointeur et déréférencer des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="b740c-107">The `*` operator is also used to declare pointer types and to dereference pointers.</span></span> <span data-ttu-id="b740c-108">Cet opérateur ne peut être utilisé que dans des contextes unsafe signalés par l’utilisation du mot clé [unsafe](../../../csharp/language-reference/keywords/unsafe.md). Il nécessite l’option de compilateur [/unsafe](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="b740c-108">This operator can only be used in unsafe contexts, denoted by the use of the [unsafe](../../../csharp/language-reference/keywords/unsafe.md) keyword, and requiring the [/unsafe](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md) compiler option.</span></span>  <span data-ttu-id="b740c-109">L’opérateur de déréférencement est également appelé opérateur d’indirection.</span><span class="sxs-lookup"><span data-stu-id="b740c-109">The dereference operator is also known as the indirection operator.</span></span>  
  
 <span data-ttu-id="b740c-110">Les types définis par l’utilisateur peuvent surcharger l’opérateur `*` binaire (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="b740c-110">User-defined types can overload the binary `*` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="b740c-111">Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="b740c-111">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b740c-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="b740c-112">Example</span></span>  
 [!code-csharp[csRefOperators#50](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-operator_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="b740c-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="b740c-113">Example</span></span>  
 [!code-csharp[csRefOperators#51](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-operator_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="b740c-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b740c-114">See Also</span></span>  
 [<span data-ttu-id="b740c-115">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b740c-115">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="b740c-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b740c-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="b740c-117">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="b740c-117">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)  
 [<span data-ttu-id="b740c-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="b740c-118">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
