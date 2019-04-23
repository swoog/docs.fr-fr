---
title: L’opérande 'IsNot' du type 'NomType' ne peut être comparé qu’à 'Nothing', car 'NomType' est un type nullable
ms.date: 07/20/2015
f1_keywords:
- bc32128
- vbc32128
helpviewer_keywords:
- BC32128
ms.assetid: 1155b23a-ad75-4bab-b9da-73f35c767a36
ms.openlocfilehash: f19b8cd5f80ba9fd6d1f5a9162b04ee409e24e28
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59311888"
---
# <a name="isnot-operand-of-type-typename-can-only-be-compared-to-nothing-because-typename-is-a-nullable-type"></a><span data-ttu-id="b5f88-102">L’opérande 'IsNot' du type 'NomType' ne peut être comparé qu’à 'Nothing', car 'NomType' est un type nullable</span><span class="sxs-lookup"><span data-stu-id="b5f88-102">'IsNot' operand of type 'typename' can only be compared to 'Nothing', because 'typename' is a nullable type</span></span>
<span data-ttu-id="b5f88-103">Une variable déclarée comme nullable a été comparée à une expression autre que `Nothing` à l’aide de la `IsNot` opérateur.</span><span class="sxs-lookup"><span data-stu-id="b5f88-103">A variable declared as nullable has been compared to an expression other than `Nothing` using the `IsNot` operator.</span></span>  
  
 <span data-ttu-id="b5f88-104">**ID d’erreur :** BC32128</span><span class="sxs-lookup"><span data-stu-id="b5f88-104">**Error ID:** BC32128</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b5f88-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="b5f88-105">To correct this error</span></span>  
  
1. <span data-ttu-id="b5f88-106">Pour comparer un type nullable à une expression autre que `Nothing` à l’aide de l’opérateur `IsNot` , appelez la méthode `GetType` sur le type nullable et comparez le résultat à l’expression, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="b5f88-106">To compare a nullable type to an expression other than `Nothing` by using the `IsNot` operator, call the `GetType` method on the nullable type and compare the result to the expression, as shown in the following example.</span></span>  
  
```vb  
Dim number? As Integer = 5  
  
If number IsNot Nothing Then  
  If number.GetType() IsNot Type.GetType("System.Int32") Then   
  
  End If  
End If  
```  
  
## <a name="see-also"></a><span data-ttu-id="b5f88-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5f88-107">See also</span></span>

- [<span data-ttu-id="b5f88-108">Types valeur Nullable</span><span class="sxs-lookup"><span data-stu-id="b5f88-108">Nullable Value Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [<span data-ttu-id="b5f88-109">IsNot (opérateur)</span><span class="sxs-lookup"><span data-stu-id="b5f88-109">IsNot Operator</span></span>](../../../visual-basic/language-reference/operators/isnot-operator.md)
