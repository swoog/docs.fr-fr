---
title: L'expression a le type '<typename>', qui est un type restreint et qui ne peut pas être utilisé pour accéder aux membres hérités de 'Object' ou 'ValueType'
ms.date: 07/20/2015
f1_keywords:
- bc31393
- vbc31393
helpviewer_keywords:
- BC31393
ms.assetid: 2963cf3f-c527-4aa7-b67c-ee80b6d23186
ms.openlocfilehash: 6d2edadc323994f7f25394321fb1aff18f7154c5
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58824271"
---
# <a name="expression-has-the-type-typename-which-is-a-restricted-type-and-cannot-be-used-to-access-members-inherited-from-object-or-valuetype"></a><span data-ttu-id="ae380-102">Expression a le type '\<nom_type >' qui est un type restreint et ne peut pas être utilisé pour accéder aux membres hérités de 'Object' ou 'ValueType'</span><span class="sxs-lookup"><span data-stu-id="ae380-102">Expression has the type '\<typename>' which is a restricted type and cannot be used to access members inherited from 'Object' or 'ValueType'</span></span>
<span data-ttu-id="ae380-103">Une expression correspond à un type qui ne peut pas être converti (boxed) par le common language runtime (CLR) mais accède à un membre qui requiert un boxing.</span><span class="sxs-lookup"><span data-stu-id="ae380-103">An expression evaluates to a type that cannot be boxed by the common language runtime (CLR) but accesses a member that requires boxing.</span></span>  
  
 <span data-ttu-id="ae380-104">Le*boxing* est le traitement nécessaire à la conversion d’un type en `Object` ou, à l’occasion, en <xref:System.ValueType>.</span><span class="sxs-lookup"><span data-stu-id="ae380-104">*Boxing* refers to the processing necessary to convert a type to `Object` or, on occasion, to <xref:System.ValueType>.</span></span> <span data-ttu-id="ae380-105">Le common language runtime ne peut pas convertir certains types de structure, par exemple <xref:System.ArgIterator>, <xref:System.RuntimeArgumentHandle>, et <xref:System.TypedReference>.</span><span class="sxs-lookup"><span data-stu-id="ae380-105">The common language runtime cannot box certain structure types, for example <xref:System.ArgIterator>, <xref:System.RuntimeArgumentHandle>, and <xref:System.TypedReference>.</span></span>  
  
 <span data-ttu-id="ae380-106">Cette expression tente d’utiliser le type restreint pour appeler une méthode héritée <xref:System.Object> ou <xref:System.ValueType>, tel que <xref:System.Object.GetHashCode%2A> ou <xref:System.Object.ToString%2A>.</span><span class="sxs-lookup"><span data-stu-id="ae380-106">This expression attempts to use the restricted type to call a method inherited from <xref:System.Object> or <xref:System.ValueType>, such as <xref:System.Object.GetHashCode%2A> or <xref:System.Object.ToString%2A>.</span></span> <span data-ttu-id="ae380-107">Pour accéder à cette méthode, Visual Basic a tenté une conversion boxing implicite qui provoque cette erreur.</span><span class="sxs-lookup"><span data-stu-id="ae380-107">To access this method, Visual Basic has attempted an implicit boxing conversion that causes this error.</span></span>  
  
 <span data-ttu-id="ae380-108">**ID d’erreur :** BC31393</span><span class="sxs-lookup"><span data-stu-id="ae380-108">**Error ID:** BC31393</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ae380-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="ae380-109">To correct this error</span></span>  
  
1.  <span data-ttu-id="ae380-110">Recherchez l’expression évaluée comme étant le type cité.</span><span class="sxs-lookup"><span data-stu-id="ae380-110">Locate the expression that evaluates to the cited type.</span></span>  
  
2.  <span data-ttu-id="ae380-111">Recherchez la partie de votre instruction qui essaie d’appeler la méthode héritée <xref:System.Object> ou <xref:System.ValueType>.</span><span class="sxs-lookup"><span data-stu-id="ae380-111">Locate the part of your statement that attempts to call the method inherited from <xref:System.Object> or <xref:System.ValueType>.</span></span>  
  
3.  <span data-ttu-id="ae380-112">Réécrivez l’instruction pour éviter l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="ae380-112">Rewrite the statement to avoid the method call.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae380-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae380-113">See also</span></span>

- [<span data-ttu-id="ae380-114">Conversions implicites et explicites</span><span class="sxs-lookup"><span data-stu-id="ae380-114">Implicit and Explicit Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
