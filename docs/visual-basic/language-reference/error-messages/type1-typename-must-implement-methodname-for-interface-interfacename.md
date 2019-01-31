---
title: <type1> '<typename>' doit implémenter '<methodname>' pour l'interface '<interfacename>'
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: c5dd7c6889a3fb5344142ee9914f98e8922d748b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264430"
---
# <a name="type1typename-must-implement-methodname-for-interface-interfacename"></a><span data-ttu-id="6d24e-102">\<type1 >'\<nom_type >' doit implémenter '\<nom_méthode >' pour l’interface '\<nom_interface >'</span><span class="sxs-lookup"><span data-stu-id="6d24e-102">\<type1>'\<typename>' must implement '\<methodname>' for interface '\<interfacename>'</span></span>
<span data-ttu-id="6d24e-103">Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure définie par l’interface.</span><span class="sxs-lookup"><span data-stu-id="6d24e-103">A class or structure claims to implement an interface but does not implement a procedure defined by the interface.</span></span> <span data-ttu-id="6d24e-104">Chaque membre de l’interface doit être implémentée.</span><span class="sxs-lookup"><span data-stu-id="6d24e-104">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="6d24e-105">**ID d’erreur :** BC30149</span><span class="sxs-lookup"><span data-stu-id="6d24e-105">**Error ID:** BC30149</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="6d24e-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="6d24e-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="6d24e-107">Déclarez une procédure avec le même nom et signature tel que défini dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="6d24e-107">Declare a procedure with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="6d24e-108">Veillez à inclure au moins le `End Function` ou `End Sub` instruction.</span><span class="sxs-lookup"><span data-stu-id="6d24e-108">Be sure to include at least the `End Function` or `End Sub` statement.</span></span>  
  
2.  <span data-ttu-id="6d24e-109">Ajouter un `Implements` clause à la fin de la `Function` ou `Sub` instruction.</span><span class="sxs-lookup"><span data-stu-id="6d24e-109">Add an `Implements` clause to the end of the `Function` or `Sub` statement.</span></span> <span data-ttu-id="6d24e-110">Exemple :</span><span class="sxs-lookup"><span data-stu-id="6d24e-110">For example:</span></span>  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="6d24e-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d24e-111">See also</span></span>
- [<span data-ttu-id="6d24e-112">Implements (instruction)</span><span class="sxs-lookup"><span data-stu-id="6d24e-112">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
- [<span data-ttu-id="6d24e-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="6d24e-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
