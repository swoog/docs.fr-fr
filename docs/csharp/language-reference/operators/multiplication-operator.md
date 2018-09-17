---
title: '* , opérateur (Informations de référence sur C#)'
ms.date: 04/04/2018
f1_keywords:
- '*_CSharpKeyword'
helpviewer_keywords:
- multiplication operator (*) [C#]
- '* operator [C#]'
ms.assetid: abd9a5f0-9b24-431e-971a-09ee1c45c50e
ms.openlocfilehash: 873cc1dc0d81425117f1784353acf08b35158133
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45596973"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="907cf-102">\*, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="907cf-102">\* Operator (C# Reference)</span></span>
<span data-ttu-id="907cf-103">L’opérateur de multiplication (`*`) calcule le produit de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="907cf-103">The multiplication operator (`*`) computes the product of its operands.</span></span> <span data-ttu-id="907cf-104">Tous les types numériques ont des opérateurs de multiplication prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="907cf-104">All numeric types have predefined multiplication operators.</span></span>  

<span data-ttu-id="907cf-105">Par ailleurs, `*` sert d’opérateur de déréférencement qui permet de lire un pointeur et d’écrire sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="907cf-105">`*` also serves as the dereference operator, which allows reading and writing to a pointer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="907cf-106">Notes</span><span class="sxs-lookup"><span data-stu-id="907cf-106">Remarks</span></span>  
 <span data-ttu-id="907cf-107">L’opérateur `*` est aussi utilisé pour déclarer des types pointeur et déréférencer des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="907cf-107">The `*` operator is also used to declare pointer types and to dereference pointers.</span></span> <span data-ttu-id="907cf-108">Cet opérateur ne peut être utilisé que dans des contextes unsafe signalés par l’utilisation du mot clé [unsafe](../../../csharp/language-reference/keywords/unsafe.md). Il nécessite l’option de compilateur [/unsafe](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="907cf-108">This operator can only be used in unsafe contexts, denoted by the use of the [unsafe](../../../csharp/language-reference/keywords/unsafe.md) keyword, and requiring the [/unsafe](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md) compiler option.</span></span>  <span data-ttu-id="907cf-109">L’opérateur de déréférencement est également appelé opérateur d’indirection.</span><span class="sxs-lookup"><span data-stu-id="907cf-109">The dereference operator is also known as the indirection operator.</span></span>  
  
 <span data-ttu-id="907cf-110">Les types définis par l’utilisateur peuvent surcharger l’opérateur `*` binaire (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="907cf-110">User-defined types can overload the binary `*` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="907cf-111">Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="907cf-111">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="907cf-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="907cf-112">Example</span></span>  
 [!code-csharp-interactive[csRefOperators#50](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-operator_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="907cf-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="907cf-113">Example</span></span>  
 [!code-csharp[csRefOperators#51](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-operator_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="907cf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="907cf-114">See Also</span></span>

- [<span data-ttu-id="907cf-115">Référence C#</span><span class="sxs-lookup"><span data-stu-id="907cf-115">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="907cf-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="907cf-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="907cf-117">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="907cf-117">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)  
- [<span data-ttu-id="907cf-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="907cf-118">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
