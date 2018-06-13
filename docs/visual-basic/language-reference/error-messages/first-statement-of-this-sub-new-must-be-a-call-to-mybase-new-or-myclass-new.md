---
title: La première instruction de ce &#39;Sub New&#39; doit être un appel à &#39;MyBase.New&#39; ou &#39;MyClass.New&#39; (aucun constructeur Accessible sans paramètres)
ms.date: 07/20/2015
f1_keywords:
- bc30148
- vbc30148
helpviewer_keywords:
- BC30148
ms.assetid: 4426e8fc-cb39-4eb8-ba95-503cd32fcc89
ms.openlocfilehash: 3b24385932700a4843ae295bc82ef9529cc86b9b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33589458"
---
# <a name="first-statement-of-this-39sub-new39-must-be-a-call-to-39mybasenew39-or-39myclassnew39-no-accessible-constructor-without-parameters"></a><span data-ttu-id="b3260-102">La première instruction de ce &#39;Sub New&#39; doit être un appel à &#39;MyBase.New&#39; ou &#39;MyClass.New&#39; (aucun constructeur Accessible sans paramètres)</span><span class="sxs-lookup"><span data-stu-id="b3260-102">First statement of this &#39;Sub New&#39; must be a call to &#39;MyBase.New&#39; or &#39;MyClass.New&#39; (No Accessible Constructor Without Parameters)</span></span>
<span data-ttu-id="b3260-103">La première instruction de ce 'Sub New' doit être un appel à 'MyBase.New' ou 'MyClass.New', car la classe de base\<basename >' de '\<derivedname >' n’a pas de 'Sub New' accessible qui peut être appelé sans argument.</span><span class="sxs-lookup"><span data-stu-id="b3260-103">First statement of this 'Sub New' must be a call to 'MyBase.New' or 'MyClass.New' because base class '\<basename>' of '\<derivedname>' does not have an accessible 'Sub New' that can be called with no arguments.</span></span>  
  
 <span data-ttu-id="b3260-104">Dans une classe dérivée, chaque constructeur doit appeler un constructeur de classe de base (`MyBase.New`).</span><span class="sxs-lookup"><span data-stu-id="b3260-104">In a derived class, every constructor must call a base class constructor (`MyBase.New`).</span></span> <span data-ttu-id="b3260-105">Si la classe de base a un constructeur sans paramètre accessible aux classes dérivées, `MyBase.New` peut être appelé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b3260-105">If the base class has a constructor with no parameters that is accessible to derived classes, `MyBase.New` can be called automatically.</span></span> <span data-ttu-id="b3260-106">Si ce n’est pas le cas, un constructeur de classe de base doit être appelé avec des paramètres, et il ne peut pas être effectuée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b3260-106">If not, a base class constructor must be called with parameters, and this cannot be done automatically.</span></span> <span data-ttu-id="b3260-107">Dans ce cas, la première instruction de chaque constructeur de classe dérivée doit appeler un constructeur paramétrable sur la classe de base, ou appeler un autre constructeur dans la classe dérivée qui appelle un constructeur de classe de base.</span><span class="sxs-lookup"><span data-stu-id="b3260-107">In this case, the first statement of every derived class constructor must call a parameterized constructor on the base class, or call another constructor in the derived class that makes a base class constructor call.</span></span>  
  
 <span data-ttu-id="b3260-108">**ID d’erreur :** BC30148</span><span class="sxs-lookup"><span data-stu-id="b3260-108">**Error ID:** BC30148</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b3260-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="b3260-109">To correct this error</span></span>  
  
-   <span data-ttu-id="b3260-110">Appeler `MyBase.New` en fournissant les paramètres requis ou appelez un constructeur homologue qui effectue un appel de ce type.</span><span class="sxs-lookup"><span data-stu-id="b3260-110">Either call `MyBase.New` supplying the required parameters, or call a peer constructor that makes such a call.</span></span>  
  
     <span data-ttu-id="b3260-111">Par exemple, si la classe de base a un constructeur qui est déclaré comme `Public Sub New(ByVal index as Integer)`, la première instruction dans la liste dérivée constructeur de classe peut être `MyBase.New(100)`.</span><span class="sxs-lookup"><span data-stu-id="b3260-111">For example, if the base class has a constructor that’s declared as `Public Sub New(ByVal index as Integer)`, the first statement in the derived class constructor might be `MyBase.New(100)`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3260-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3260-112">See Also</span></span>  
 [<span data-ttu-id="b3260-113">Éléments fondamentaux de l’héritage</span><span class="sxs-lookup"><span data-stu-id="b3260-113">Inheritance Basics</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
