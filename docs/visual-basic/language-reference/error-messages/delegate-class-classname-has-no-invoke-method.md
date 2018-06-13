---
title: Classe déléguée &#39; &lt;classname&gt; &#39; n’a aucun méthode Invoke, afin de l’expression de ce type ne peut pas être la cible d’un appel de méthode
ms.date: 07/20/2015
f1_keywords:
- vbc30220
- bc30220
helpviewer_keywords:
- BC30220
ms.assetid: 6be0d61c-f2f9-4f9b-ab90-8871a0d7206d
ms.openlocfilehash: cc1abba46224772e733780800dd104dfc7ebe9ad
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588828"
---
# <a name="delegate-class-39ltclassnamegt39-has-no-invoke-method-so-an-expression-of-this-type-cannot-be-the-target-of-a-method-call"></a><span data-ttu-id="a352e-102">Classe déléguée &#39; &lt;classname&gt; &#39; n’a aucun méthode Invoke, afin de l’expression de ce type ne peut pas être la cible d’un appel de méthode</span><span class="sxs-lookup"><span data-stu-id="a352e-102">Delegate class &#39;&lt;classname&gt;&#39; has no Invoke method, so an expression of this type cannot be the target of a method call</span></span>
<span data-ttu-id="a352e-103">Un appel à `Invoke` via un délégué a échoué, car `Invoke` n’est pas implémentée sur la classe déléguée.</span><span class="sxs-lookup"><span data-stu-id="a352e-103">A call to `Invoke` through a delegate has failed because `Invoke` is not implemented on the delegate class.</span></span>  
  
 <span data-ttu-id="a352e-104">**ID d’erreur :** BC30220</span><span class="sxs-lookup"><span data-stu-id="a352e-104">**Error ID:** BC30220</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a352e-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="a352e-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="a352e-106">Assurez-vous qu’une instance de la classe déléguée a été créée avec un `Dim` instruction et qu’une procédure a été assignée à l’instance de délégué avec le `AddressOf` opérateur.</span><span class="sxs-lookup"><span data-stu-id="a352e-106">Ensure that an instance of the delegate class has been created with a `Dim` statement and that a procedure has been assigned to the delegate instance with the `AddressOf` operator.</span></span>  
  
2.  <span data-ttu-id="a352e-107">Recherchez le code qui implémente la classe déléguée et vérifiez qu’il implémente la `Invoke` procédure.</span><span class="sxs-lookup"><span data-stu-id="a352e-107">Locate the code that implements the delegate class and make sure it implements the `Invoke` procedure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a352e-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a352e-108">See Also</span></span>  
 [<span data-ttu-id="a352e-109">Délégués</span><span class="sxs-lookup"><span data-stu-id="a352e-109">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)  
 [<span data-ttu-id="a352e-110">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="a352e-110">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)  
 [<span data-ttu-id="a352e-111">AddressOf (opérateur)</span><span class="sxs-lookup"><span data-stu-id="a352e-111">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)  
 [<span data-ttu-id="a352e-112">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="a352e-112">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
