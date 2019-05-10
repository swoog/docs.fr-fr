---
title: La structure '<structurename>' doit contenir au moins une variable membre d'instance ou au moins une déclaration d'événement d'instance non marquée comme 'Custom'.
ms.date: 07/20/2015
f1_keywords:
- bc30941
- vbc30941
helpviewer_keywords:
- BC30941
ms.assetid: 7054cc1e-bac3-4c3d-82f3-35772bd8dd3b
ms.openlocfilehash: 4ce24073896326bb5a68e563e2d34aafa09ef1c1
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64593214"
---
# <a name="structure-structurename-must-contain-at-least-one-instance-member-variable-or-at-least-one-instance-event-declaration-not-marked-custom"></a><span data-ttu-id="9c5cb-102">Structure '\<nom_structure >' doit contenir au moins une variable membre d’instance ou une déclaration d’événement au moins une instance non marquée comme 'Custom'</span><span class="sxs-lookup"><span data-stu-id="9c5cb-102">Structure '\<structurename>' must contain at least one instance member variable or at least one instance event declaration not marked 'Custom'</span></span>
<span data-ttu-id="9c5cb-103">Une définition de structure n’inclut pas les variables non partagées ou des événements non personnalisés non partagées.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-103">A structure definition does not include any nonshared variables or nonshared noncustom events.</span></span>  
  
 <span data-ttu-id="9c5cb-104">Chaque structure doit avoir une variable ou un événement qui s’applique à chaque instance spécifique (non partagée) et non à toutes les instances collectivement ([partagé](../../../visual-basic/language-reference/modifiers/shared.md)).</span><span class="sxs-lookup"><span data-stu-id="9c5cb-104">Every structure must have either a variable or an event that applies to each specific instance (nonshared) instead of to all instances collectively ([Shared](../../../visual-basic/language-reference/modifiers/shared.md)).</span></span> <span data-ttu-id="9c5cb-105">Les procédures, les propriétés et les constantes non partagées ne répondent pas à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-105">Nonshared constants, properties, and procedures do not satisfy this requirement.</span></span> <span data-ttu-id="9c5cb-106">En outre, s’il y a aucune variable non partagée et qu’un seul événement non partagé, cet événement ne peut pas être un `Custom` événement.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-106">In addition, if there are no nonshared variables and only one nonshared event, that event cannot be a `Custom` event.</span></span>  
  
 <span data-ttu-id="9c5cb-107">**ID d’erreur :** BC30941</span><span class="sxs-lookup"><span data-stu-id="9c5cb-107">**Error ID:** BC30941</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9c5cb-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="9c5cb-108">To correct this error</span></span>  
  
- <span data-ttu-id="9c5cb-109">Définissez au moins une variable ou un événement qui n’est pas `Shared`.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-109">Define at least one variable or event that is not `Shared`.</span></span> <span data-ttu-id="9c5cb-110">Si vous définissez un seul événement, il doit être non personnalisés, ainsi que non partagée.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-110">If you define only one event, it must be noncustom as well as nonshared.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c5cb-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c5cb-111">See also</span></span>

- [<span data-ttu-id="9c5cb-112">Structures</span><span class="sxs-lookup"><span data-stu-id="9c5cb-112">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="9c5cb-113">Guide pratique pour déclarer une structure</span><span class="sxs-lookup"><span data-stu-id="9c5cb-113">How to: Declare a Structure</span></span>](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="9c5cb-114">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="9c5cb-114">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)
