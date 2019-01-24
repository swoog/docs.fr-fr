---
title: Fonction imbriquée n’a pas une signature qui est compatible avec le délégué &#39; &lt;nom_délégué&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc36532
- bc36532
helpviewer_keywords:
- BC36532
ms.assetid: 493f292c-d81e-40ef-8b47-61f020571829
ms.openlocfilehash: abfda4ee6064ec9ea54b8a3c383d10f8263a1458
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506405"
---
# <a name="nested-function-does-not-have-a-signature-that-is-compatible-with-delegate-39ltdelegatenamegt39"></a><span data-ttu-id="5ae2d-102">Fonction imbriquée n’a pas une signature qui est compatible avec le délégué &#39; &lt;nom_délégué&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="5ae2d-102">Nested function does not have a signature that is compatible with delegate &#39;&lt;delegatename&gt;&#39;</span></span>
<span data-ttu-id="5ae2d-103">Une expression lambda a été assignée à un délégué qui a une signature incompatible.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-103">A lambda expression has been assigned to a delegate that has an incompatible signature.</span></span> <span data-ttu-id="5ae2d-104">Par exemple, dans le code suivant, le délégué `Del` a deux paramètres entiers.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-104">For example, in the following code, delegate `Del` has two integer parameters.</span></span>  
  
```vb  
Delegate Function Del(ByVal p As Integer, ByVal q As Integer) As Integer  
```  
  
 <span data-ttu-id="5ae2d-105">L’erreur est générée si une expression lambda avec un argument est déclarée comme type `Del`:</span><span class="sxs-lookup"><span data-stu-id="5ae2d-105">The error is raised if a lambda expression with one argument is declared as type `Del`:</span></span>  
  
```vb  
' Neither of these is valid.   
' Dim lambda1 As Del = Function(n As Integer) n + 1  
' Dim lambda2 As Del = Function(n) n + 1  
```  
  
 <span data-ttu-id="5ae2d-106">**ID d’erreur :** BC36532</span><span class="sxs-lookup"><span data-stu-id="5ae2d-106">**Error ID:** BC36532</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="5ae2d-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="5ae2d-107">To correct this error</span></span>  
  
-   <span data-ttu-id="5ae2d-108">Ajustez la définition du délégué ou l’expression lambda assignée afin que les signatures sont compatibles.</span><span class="sxs-lookup"><span data-stu-id="5ae2d-108">Adjust either the delegate definition or the assigned lambda expression so that the signatures are compatible.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ae2d-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ae2d-109">See also</span></span>
- [<span data-ttu-id="5ae2d-110">Conversion simplifiée des délégués</span><span class="sxs-lookup"><span data-stu-id="5ae2d-110">Relaxed Delegate Conversion</span></span>](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
- [<span data-ttu-id="5ae2d-111">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="5ae2d-111">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
