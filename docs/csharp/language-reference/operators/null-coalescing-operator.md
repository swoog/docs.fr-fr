---
title: ?? , opérateur (Informations de référence sur C#)
ms.date: 07/20/2015
f1_keywords:
- ??_CSharpKeyword
helpviewer_keywords:
- coalesce operator [C#]
- ?? operator [C#]
- conditional-AND operator (&&) [C#]
ms.assetid: 088b1f0d-c1af-4fe1-b4b8-196fd5ea9132
ms.openlocfilehash: fbcfda07cc55628aeed82eb7561516f7012bc4fe
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "50980672"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="785fd-103">??</span><span class="sxs-lookup"><span data-stu-id="785fd-103">??</span></span> <span data-ttu-id="785fd-104">, opérateur (Informations de référence sur C#)</span><span class="sxs-lookup"><span data-stu-id="785fd-104">Operator (C# Reference)</span></span>
<span data-ttu-id="785fd-105">L'opérateur `??` est appelé l'l'opérateur de fusion Null.</span><span class="sxs-lookup"><span data-stu-id="785fd-105">The `??` operator is called the null-coalescing operator.</span></span>  <span data-ttu-id="785fd-106">Il retourne l’opérande de partie gauche si ce dernier n’est pas Null ; dans le cas contraire, il retourne l’opérande de partie droite.</span><span class="sxs-lookup"><span data-stu-id="785fd-106">It returns the left-hand operand if the operand is not null; otherwise it returns the right hand operand.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="785fd-107">Notes</span><span class="sxs-lookup"><span data-stu-id="785fd-107">Remarks</span></span>  
 <span data-ttu-id="785fd-108">Un type Nullable peut représenter une valeur à partir du domaine du type, ou la valeur peut être non définie (auquel cas la valeur est Null).</span><span class="sxs-lookup"><span data-stu-id="785fd-108">A nullable type can represent a value from the type’s domain, or the value can be undefined (in which case the value is null).</span></span> <span data-ttu-id="785fd-109">Utilisez la simplicité de syntaxe de l’opérateur `??` pour retourner une valeur appropriée (l’opérande de partie droite) si l’opérande de partie gauche a un type Nullable dont la valeur est Null.</span><span class="sxs-lookup"><span data-stu-id="785fd-109">You can use the `??` operator’s syntactic expressiveness to return an appropriate value (the right hand operand) when the left operand has a nullable type whose value is null.</span></span> <span data-ttu-id="785fd-110">Si vous essayez d'assigner un type valeur Nullable à un type valeur non Nullable sans utiliser l'opérateur `??`, vous générez une erreur au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="785fd-110">If you try to assign a nullable value type to a non-nullable value type without using the `??` operator, you will generate a compile-time error.</span></span> <span data-ttu-id="785fd-111">Si vous utilisez un cast et si le type valeur Nullable est actuellement non défini, une exception `InvalidOperationException` est levée.</span><span class="sxs-lookup"><span data-stu-id="785fd-111">If you use a cast, and the nullable value type is currently undefined, an `InvalidOperationException` exception will be thrown.</span></span>  
  
 <span data-ttu-id="785fd-112">Pour plus d’informations, consultez [Types Nullable](../../../csharp/programming-guide/nullable-types/index.md).</span><span class="sxs-lookup"><span data-stu-id="785fd-112">For more information, see [Nullable Types](../../../csharp/programming-guide/nullable-types/index.md).</span></span>  
  
 <span data-ttu-id="785fd-113">Le résultat d’un opérateur</span><span class="sxs-lookup"><span data-stu-id="785fd-113">The result of a ??</span></span> <span data-ttu-id="785fd-114">?? n’est pas considéré comme une constante même si ses deux arguments sont des constantes.</span><span class="sxs-lookup"><span data-stu-id="785fd-114">operator is not considered to be a constant even if both its arguments are constants.</span></span>  
  
## <a name="example"></a><span data-ttu-id="785fd-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="785fd-115">Example</span></span>  
 [!code-csharp[csRefOperators#53](../../../csharp/language-reference/operators/codesnippet/CSharp/null-conditional-operator_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="785fd-116">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="785fd-116">C# Language Specification</span></span>  

<span data-ttu-id="785fd-117">Pour plus d’informations, consultez [Opérateur de fusion de Null](~/_csharplang/spec/expressions.md#the-null-coalescing-operator) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="785fd-117">For more information, see [The null coalescing operator](~/_csharplang/spec/expressions.md#the-null-coalescing-operator) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="785fd-118">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="785fd-118">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="785fd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="785fd-119">See Also</span></span>

- [<span data-ttu-id="785fd-120">Référence C#</span><span class="sxs-lookup"><span data-stu-id="785fd-120">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="785fd-121">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="785fd-121">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="785fd-122">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="785fd-122">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="785fd-123">Types Nullable</span><span class="sxs-lookup"><span data-stu-id="785fd-123">Nullable Types</span></span>](../../../csharp/programming-guide/nullable-types/index.md)  
- [<span data-ttu-id="785fd-124">Que signifie réellement « Lifted » ?</span><span class="sxs-lookup"><span data-stu-id="785fd-124">What Exactly Does 'Lifted' mean?</span></span>](https://blogs.msdn.microsoft.com/ericlippert/2007/06/27/what-exactly-does-lifted-mean/)
