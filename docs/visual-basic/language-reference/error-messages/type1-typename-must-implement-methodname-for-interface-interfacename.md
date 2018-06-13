---
title: '&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;methodname&gt; &#39; pour l’interface &#39; &lt;nom_interface&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: daeeab853f6a7f582542fa15ffc09ce749731d6f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33594381"
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmethodnamegt39-for-interface-39ltinterfacenamegt39"></a><span data-ttu-id="985c2-102">&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;methodname&gt; &#39; pour l’interface &#39; &lt;nom_interface&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="985c2-102">&lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;methodname&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39;</span></span>
<span data-ttu-id="985c2-103">Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure définie par l’interface.</span><span class="sxs-lookup"><span data-stu-id="985c2-103">A class or structure claims to implement an interface but does not implement a procedure defined by the interface.</span></span> <span data-ttu-id="985c2-104">Chaque membre de l’interface doit être implémentée.</span><span class="sxs-lookup"><span data-stu-id="985c2-104">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="985c2-105">**ID d’erreur :** BC30149</span><span class="sxs-lookup"><span data-stu-id="985c2-105">**Error ID:** BC30149</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="985c2-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="985c2-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="985c2-107">Déclarez une procédure avec le même nom et la même signature que ceux définis dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="985c2-107">Declare a procedure with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="985c2-108">Veillez à inclure au moins les `End Function` ou `End Sub` instruction.</span><span class="sxs-lookup"><span data-stu-id="985c2-108">Be sure to include at least the `End Function` or `End Sub` statement.</span></span>  
  
2.  <span data-ttu-id="985c2-109">Ajouter un `Implements` clause à la fin de la `Function` ou `Sub` instruction.</span><span class="sxs-lookup"><span data-stu-id="985c2-109">Add an `Implements` clause to the end of the `Function` or `Sub` statement.</span></span> <span data-ttu-id="985c2-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="985c2-110">For example:</span></span>  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="985c2-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="985c2-111">See Also</span></span>  
 [<span data-ttu-id="985c2-112">Implements (instruction)</span><span class="sxs-lookup"><span data-stu-id="985c2-112">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)  
 [<span data-ttu-id="985c2-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="985c2-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
