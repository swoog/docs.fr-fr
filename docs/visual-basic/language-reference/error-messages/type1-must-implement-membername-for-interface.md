---
title: <type1>«<typename>'doit implémenter'<membername>'pour l’interface'<interfacename>»
ms.date: 07/20/2015
f1_keywords:
- vbc30154
- bc30154
helpviewer_keywords:
- BC30154
ms.assetid: 259afdfa-3608-4760-adcb-88ec0da5020d
ms.openlocfilehash: 86b0d46e0e27b2fd8d1fccb37f4a3c45e95f5f63
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59295326"
---
# <a name="type1typename-must-implement-membername-for-interface-interfacename"></a><span data-ttu-id="86318-102">\<type1 >'\<nom_type >' doit implémenter '\<nom_membre >' pour l’interface '\<nom_interface >'</span><span class="sxs-lookup"><span data-stu-id="86318-102">\<type1>'\<typename>' must implement '\<membername>' for interface '\<interfacename>'</span></span>
<span data-ttu-id="86318-103">'\<nom_type >' doit implémenter '\<nom_membre >' pour l’interface '\<nom_interface >'.</span><span class="sxs-lookup"><span data-stu-id="86318-103">'\<typename>' must implement '\<membername>' for interface '\<interfacename>'.</span></span> <span data-ttu-id="86318-104">Propriété d’implémentation doit avoir correspondant à 'ReadOnly' / 'WriteOnly' spécificateurs.</span><span class="sxs-lookup"><span data-stu-id="86318-104">Implementing property must have matching 'ReadOnly'/'WriteOnly' specifiers.</span></span>  
  
 <span data-ttu-id="86318-105">Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure, une propriété ou un événement défini par l’interface.</span><span class="sxs-lookup"><span data-stu-id="86318-105">A class or structure claims to implement an interface but does not implement a procedure, property, or event defined by the interface.</span></span> <span data-ttu-id="86318-106">Chaque membre de l’interface doit être implémentée.</span><span class="sxs-lookup"><span data-stu-id="86318-106">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="86318-107">**ID d’erreur :** BC30154</span><span class="sxs-lookup"><span data-stu-id="86318-107">**Error ID:** BC30154</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="86318-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="86318-108">To correct this error</span></span>  
  
1. <span data-ttu-id="86318-109">Déclarez un membre avec le même nom et signature tel que défini dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="86318-109">Declare a member with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="86318-110">Veillez à inclure au moins le `End Function`, `End Sub`, ou `End Property` instruction.</span><span class="sxs-lookup"><span data-stu-id="86318-110">Be sure to include at least the `End Function`, `End Sub`, or `End Property` statement.</span></span>  
  
2. <span data-ttu-id="86318-111">Ajouter un `Implements` clause à la fin de la `Function`, `Sub`, `Property`, ou `Event` instruction.</span><span class="sxs-lookup"><span data-stu-id="86318-111">Add an `Implements` clause to the end of the `Function`, `Sub`, `Property`, or `Event` statement.</span></span> <span data-ttu-id="86318-112">Exemple :</span><span class="sxs-lookup"><span data-stu-id="86318-112">For example:</span></span>  
  
    ```  
    Public Event ItHappened() Implements IBaseInterface.ItHappened  
    ```  
  
3. <span data-ttu-id="86318-113">Lorsque vous implémentez une propriété, assurez-vous que `ReadOnly` ou `WriteOnly` est utilisé dans la même façon que dans la définition d’interface.</span><span class="sxs-lookup"><span data-stu-id="86318-113">When implementing a property, make sure that `ReadOnly` or `WriteOnly` is used in the same way as in the interface definition.</span></span>  
  
4. <span data-ttu-id="86318-114">Lorsque vous implémentez une propriété, déclarez `Get` et `Set` procédures, comme il convient.</span><span class="sxs-lookup"><span data-stu-id="86318-114">When implementing a property, declare `Get` and `Set` procedures, as appropriate.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86318-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86318-115">See also</span></span>

- [<span data-ttu-id="86318-116">Implements, instruction</span><span class="sxs-lookup"><span data-stu-id="86318-116">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
- [<span data-ttu-id="86318-117">Interfaces</span><span class="sxs-lookup"><span data-stu-id="86318-117">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
