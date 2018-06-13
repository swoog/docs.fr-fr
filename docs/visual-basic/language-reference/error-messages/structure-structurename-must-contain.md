---
title: Structure &#39; &lt;nom_structure&gt; &#39; doit contenir au moins une variable membre d’instance ou une déclaration d’événement au moins une instance non marquée comme &#39;personnalisé&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30941
- vbc30941
helpviewer_keywords:
- BC30941
ms.assetid: 7054cc1e-bac3-4c3d-82f3-35772bd8dd3b
ms.openlocfilehash: 85a4babc808e274a99f2c9faf08a02abf8aa4e93
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33594496"
---
# <a name="structure-39ltstructurenamegt39-must-contain-at-least-one-instance-member-variable-or-at-least-one-instance-event-declaration-not-marked-39custom39"></a><span data-ttu-id="499cd-102">Structure &#39; &lt;nom_structure&gt; &#39; doit contenir au moins une variable membre d’instance ou une déclaration d’événement au moins une instance non marquée comme &#39;personnalisé&#39;</span><span class="sxs-lookup"><span data-stu-id="499cd-102">Structure &#39;&lt;structurename&gt;&#39; must contain at least one instance member variable or at least one instance event declaration not marked &#39;Custom&#39;</span></span>
<span data-ttu-id="499cd-103">Une définition de structure n’inclut pas toutes les variables non partagées ou des événements non personnalisés non partagées.</span><span class="sxs-lookup"><span data-stu-id="499cd-103">A structure definition does not include any nonshared variables or nonshared noncustom events.</span></span>  
  
 <span data-ttu-id="499cd-104">Chaque structure doit avoir une variable ou un événement qui s’applique à chaque instance spécifique (non partagée) et non à toutes les instances collectivement ([Shared](../../../visual-basic/language-reference/modifiers/shared.md)).</span><span class="sxs-lookup"><span data-stu-id="499cd-104">Every structure must have either a variable or an event that applies to each specific instance (nonshared) instead of to all instances collectively ([Shared](../../../visual-basic/language-reference/modifiers/shared.md)).</span></span> <span data-ttu-id="499cd-105">Les procédures, les propriétés et les constantes non partagées ne répondent pas à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="499cd-105">Nonshared constants, properties, and procedures do not satisfy this requirement.</span></span> <span data-ttu-id="499cd-106">En outre, s’il y a aucune variable non partagée et qu’un seul événement non partagé, cet événement ne peut pas être un `Custom` événement.</span><span class="sxs-lookup"><span data-stu-id="499cd-106">In addition, if there are no nonshared variables and only one nonshared event, that event cannot be a `Custom` event.</span></span>  
  
 <span data-ttu-id="499cd-107">**ID d’erreur :** BC30941</span><span class="sxs-lookup"><span data-stu-id="499cd-107">**Error ID:** BC30941</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="499cd-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="499cd-108">To correct this error</span></span>  
  
-   <span data-ttu-id="499cd-109">Définissez au moins une variable ou un événement qui n’est pas `Shared`.</span><span class="sxs-lookup"><span data-stu-id="499cd-109">Define at least one variable or event that is not `Shared`.</span></span> <span data-ttu-id="499cd-110">Si vous définissez un seul événement, il doit être non personnalisés ainsi que non partagée.</span><span class="sxs-lookup"><span data-stu-id="499cd-110">If you define only one event, it must be noncustom as well as nonshared.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="499cd-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="499cd-111">See Also</span></span>  
 [<span data-ttu-id="499cd-112">Structures</span><span class="sxs-lookup"><span data-stu-id="499cd-112">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)  
 [<span data-ttu-id="499cd-113">Guide pratique : déclarer une structure</span><span class="sxs-lookup"><span data-stu-id="499cd-113">How to: Declare a Structure</span></span>](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)  
 [<span data-ttu-id="499cd-114">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="499cd-114">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)
