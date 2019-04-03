---
title: La structure '<structurename>' doit contenir au moins une variable membre d'instance ou au moins une déclaration d'événement d'instance non marquée comme 'Custom'.
ms.date: 07/20/2015
f1_keywords:
- bc30941
- vbc30941
helpviewer_keywords:
- BC30941
ms.assetid: 7054cc1e-bac3-4c3d-82f3-35772bd8dd3b
ms.openlocfilehash: 598aef3943a53ee6eb97064819c9128de1839f52
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58813936"
---
# <a name="structure-structurename-must-contain-at-least-one-instance-member-variable-or-at-least-one-instance-event-declaration-not-marked-custom"></a><span data-ttu-id="ccb01-102">Structure '\<nom_structure >' doit contenir au moins une variable membre d’instance ou une déclaration d’événement au moins une instance non marquée comme 'Custom'</span><span class="sxs-lookup"><span data-stu-id="ccb01-102">Structure '\<structurename>' must contain at least one instance member variable or at least one instance event declaration not marked 'Custom'</span></span>
<span data-ttu-id="ccb01-103">Une définition de structure n’inclut pas les variables non partagées ou des événements non personnalisés non partagées.</span><span class="sxs-lookup"><span data-stu-id="ccb01-103">A structure definition does not include any nonshared variables or nonshared noncustom events.</span></span>  
  
 <span data-ttu-id="ccb01-104">Chaque structure doit avoir une variable ou un événement qui s’applique à chaque instance spécifique (non partagée) et non à toutes les instances collectivement ([partagé](../../../visual-basic/language-reference/modifiers/shared.md)).</span><span class="sxs-lookup"><span data-stu-id="ccb01-104">Every structure must have either a variable or an event that applies to each specific instance (nonshared) instead of to all instances collectively ([Shared](../../../visual-basic/language-reference/modifiers/shared.md)).</span></span> <span data-ttu-id="ccb01-105">Les procédures, les propriétés et les constantes non partagées ne répondent pas à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="ccb01-105">Nonshared constants, properties, and procedures do not satisfy this requirement.</span></span> <span data-ttu-id="ccb01-106">En outre, s’il y a aucune variable non partagée et qu’un seul événement non partagé, cet événement ne peut pas être un `Custom` événement.</span><span class="sxs-lookup"><span data-stu-id="ccb01-106">In addition, if there are no nonshared variables and only one nonshared event, that event cannot be a `Custom` event.</span></span>  
  
 <span data-ttu-id="ccb01-107">**ID d’erreur :** BC30941</span><span class="sxs-lookup"><span data-stu-id="ccb01-107">**Error ID:** BC30941</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ccb01-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="ccb01-108">To correct this error</span></span>  
  
-   <span data-ttu-id="ccb01-109">Définissez au moins une variable ou un événement qui n’est pas `Shared`.</span><span class="sxs-lookup"><span data-stu-id="ccb01-109">Define at least one variable or event that is not `Shared`.</span></span> <span data-ttu-id="ccb01-110">Si vous définissez un seul événement, il doit être non personnalisés, ainsi que non partagée.</span><span class="sxs-lookup"><span data-stu-id="ccb01-110">If you define only one event, it must be noncustom as well as nonshared.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccb01-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccb01-111">See also</span></span>

- [<span data-ttu-id="ccb01-112">Structures</span><span class="sxs-lookup"><span data-stu-id="ccb01-112">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="ccb01-113">Guide pratique pour déclarer une structure</span><span class="sxs-lookup"><span data-stu-id="ccb01-113">How to: Declare a Structure</span></span>](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="ccb01-114">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="ccb01-114">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)
