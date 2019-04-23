---
title: <type1>«<typename>'doit implémenter'<methodname>'pour l’interface'<interfacename>»
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: 432f089bc77928308820d7456d930fba8dc513f7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59304907"
---
# <a name="type1typename-must-implement-methodname-for-interface-interfacename"></a><span data-ttu-id="04552-102">\<type1 >'\<nom_type >' doit implémenter '\<nom_méthode >' pour l’interface '\<nom_interface >'</span><span class="sxs-lookup"><span data-stu-id="04552-102">\<type1>'\<typename>' must implement '\<methodname>' for interface '\<interfacename>'</span></span>
<span data-ttu-id="04552-103">Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure définie par l’interface.</span><span class="sxs-lookup"><span data-stu-id="04552-103">A class or structure claims to implement an interface but does not implement a procedure defined by the interface.</span></span> <span data-ttu-id="04552-104">Chaque membre de l’interface doit être implémentée.</span><span class="sxs-lookup"><span data-stu-id="04552-104">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="04552-105">**ID d’erreur :** BC30149</span><span class="sxs-lookup"><span data-stu-id="04552-105">**Error ID:** BC30149</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="04552-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="04552-106">To correct this error</span></span>  
  
1. <span data-ttu-id="04552-107">Déclarez une procédure avec le même nom et signature tel que défini dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="04552-107">Declare a procedure with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="04552-108">Veillez à inclure au moins le `End Function` ou `End Sub` instruction.</span><span class="sxs-lookup"><span data-stu-id="04552-108">Be sure to include at least the `End Function` or `End Sub` statement.</span></span>  
  
2. <span data-ttu-id="04552-109">Ajouter un `Implements` clause à la fin de la `Function` ou `Sub` instruction.</span><span class="sxs-lookup"><span data-stu-id="04552-109">Add an `Implements` clause to the end of the `Function` or `Sub` statement.</span></span> <span data-ttu-id="04552-110">Exemple :</span><span class="sxs-lookup"><span data-stu-id="04552-110">For example:</span></span>  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="04552-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04552-111">See also</span></span>

- [<span data-ttu-id="04552-112">Implements (instruction)</span><span class="sxs-lookup"><span data-stu-id="04552-112">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
- [<span data-ttu-id="04552-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="04552-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
