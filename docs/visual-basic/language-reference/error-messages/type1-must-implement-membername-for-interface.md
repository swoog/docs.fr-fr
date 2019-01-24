---
title: '&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;membername&gt; &#39; pour interface &#39; &lt;nom_interface&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30154
- bc30154
helpviewer_keywords:
- BC30154
ms.assetid: 259afdfa-3608-4760-adcb-88ec0da5020d
ms.openlocfilehash: 14e7bd199215764676a4b563eafc68bd6dabadc7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574740"
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmembernamegt39-for-interface-39ltinterfacenamegt39"></a><span data-ttu-id="c5d2d-102">&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;membername&gt; &#39; pour interface &#39; &lt;nom_interface&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="c5d2d-102">&lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;membername&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39;</span></span>
<span data-ttu-id="c5d2d-103">'\<nom_type >' doit implémenter '\<nom_membre >' pour l’interface '\<nom_interface >'.</span><span class="sxs-lookup"><span data-stu-id="c5d2d-103">'\<typename>' must implement '\<membername>' for interface '\<interfacename>'.</span></span> <span data-ttu-id="c5d2d-104">Propriété d’implémentation doit avoir correspondant à 'ReadOnly' / 'WriteOnly' spécificateurs.</span><span class="sxs-lookup"><span data-stu-id="c5d2d-104">Implementing property must have matching 'ReadOnly'/'WriteOnly' specifiers.</span></span>  
  
 <span data-ttu-id="c5d2d-105">Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure, une propriété ou un événement défini par l’interface.</span><span class="sxs-lookup"><span data-stu-id="c5d2d-105">A class or structure claims to implement an interface but does not implement a procedure, property, or event defined by the interface.</span></span> <span data-ttu-id="c5d2d-106">Chaque membre de l’interface doit être implémentée.</span><span class="sxs-lookup"><span data-stu-id="c5d2d-106">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="c5d2d-107">**ID d’erreur :** BC30154</span><span class="sxs-lookup"><span data-stu-id="c5d2d-107">**Error ID:** BC30154</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c5d2d-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="c5d2d-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="c5d2d-109">Déclarez un membre avec le même nom et signature tel que défini dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="c5d2d-109">Declare a member with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="c5d2d-110">Veillez à inclure au moins le `End Function`, `End Sub`, ou `End Property` instruction.</span><span class="sxs-lookup"><span data-stu-id="c5d2d-110">Be sure to include at least the `End Function`, `End Sub`, or `End Property` statement.</span></span>  
  
2.  <span data-ttu-id="c5d2d-111">Ajouter un `Implements` clause à la fin de la `Function`, `Sub`, `Property`, ou `Event` instruction.</span><span class="sxs-lookup"><span data-stu-id="c5d2d-111">Add an `Implements` clause to the end of the `Function`, `Sub`, `Property`, or `Event` statement.</span></span> <span data-ttu-id="c5d2d-112">Exemple :</span><span class="sxs-lookup"><span data-stu-id="c5d2d-112">For example:</span></span>  
  
    ```  
    Public Event ItHappened() Implements IBaseInterface.ItHappened  
    ```  
  
3.  <span data-ttu-id="c5d2d-113">Lorsque vous implémentez une propriété, assurez-vous que `ReadOnly` ou `WriteOnly` est utilisé dans la même façon que dans la définition d’interface.</span><span class="sxs-lookup"><span data-stu-id="c5d2d-113">When implementing a property, make sure that `ReadOnly` or `WriteOnly` is used in the same way as in the interface definition.</span></span>  
  
4.  <span data-ttu-id="c5d2d-114">Lorsque vous implémentez une propriété, déclarez `Get` et `Set` procédures, comme il convient.</span><span class="sxs-lookup"><span data-stu-id="c5d2d-114">When implementing a property, declare `Get` and `Set` procedures, as appropriate.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5d2d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5d2d-115">See also</span></span>
- [<span data-ttu-id="c5d2d-116">Implements (instruction)</span><span class="sxs-lookup"><span data-stu-id="c5d2d-116">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
- [<span data-ttu-id="c5d2d-117">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c5d2d-117">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
