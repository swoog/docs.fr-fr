---
title: Le modificateur 'Custom' n'est pas valide pour les événements déclarés sans types délégués explicites
ms.date: 07/20/2015
f1_keywords:
- vbc31122
- bc31122
helpviewer_keywords:
- BC31122
ms.assetid: 6911f0d1-641a-473b-906d-8ee5681194be
ms.openlocfilehash: c1b57ccdaa9e04c837ecf7572bc164683a934b2d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273515"
---
# <a name="custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types"></a><span data-ttu-id="dfe55-102">Le modificateur 'Custom' n'est pas valide pour les événements déclarés sans types délégués explicites</span><span class="sxs-lookup"><span data-stu-id="dfe55-102">'Custom' modifier is not valid on events declared without explicit delegate types</span></span>
<span data-ttu-id="dfe55-103">Contrairement à un événement non personnalisé, un `Custom Event` déclaration nécessite un `As` clause après le nom de l’événement qui spécifie explicitement le type de délégué pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="dfe55-103">Unlike a non-custom event, a `Custom Event` declaration requires an `As` clause following the event name that explicitly specifies the delegate type for the event.</span></span>  
  
 <span data-ttu-id="dfe55-104">Les événements non personnalisés peuvent être défini avec un `As` clause et explicite type délégué, ou avec un paramètre de liste immédiatement après le nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="dfe55-104">Non-custom events can be defined either with an `As` clause and an explicit delegate type, or with a parameter list immediately following the event name.</span></span>  
  
 <span data-ttu-id="dfe55-105">**ID d’erreur :** BC31122</span><span class="sxs-lookup"><span data-stu-id="dfe55-105">**Error ID:** BC31122</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="dfe55-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="dfe55-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="dfe55-107">Définissez un délégué avec la même liste de paramètres que l’événement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="dfe55-107">Define a delegate with the same parameter list as the custom event.</span></span>  
  
     <span data-ttu-id="dfe55-108">Par exemple, si le `Custom Event` a été défini par `Custom Event Test(ByVal sender As Object, ByVal i As Integer)`, puis le délégué correspondant est la suivante.</span><span class="sxs-lookup"><span data-stu-id="dfe55-108">For example, if the `Custom Event` was defined by `Custom Event Test(ByVal sender As Object, ByVal i As Integer)`, then the corresponding delegate would be the following.</span></span>  
  
     [!code-vb[VbVbalrEventError#18](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_1.vb)]  
  
2.  <span data-ttu-id="dfe55-109">Remplacez la liste des paramètres de l’événement personnalisé avec un `As` clause qui spécifie le type de délégué.</span><span class="sxs-lookup"><span data-stu-id="dfe55-109">Replace the parameter list of the custom event with an `As` clause specifying the delegate type.</span></span>  
  
     <span data-ttu-id="dfe55-110">Poursuivre avec l’exemple, `Custom Event` déclaration réécrite comme suit.</span><span class="sxs-lookup"><span data-stu-id="dfe55-110">Continuing with the example, `Custom Event` declaration would be rewritten as follows.</span></span>  
  
     [!code-vb[VbVbalrEventError#19](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_2.vb)]  
  
## <a name="example"></a><span data-ttu-id="dfe55-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="dfe55-111">Example</span></span>  
 <span data-ttu-id="dfe55-112">Cet exemple déclare un `Custom Event` et spécifie le texte requis `As` clause avec un type délégué.</span><span class="sxs-lookup"><span data-stu-id="dfe55-112">This example declares a `Custom Event` and specifies the required `As` clause with a delegate type.</span></span>  
  
 [!code-vb[VbVbalrEventError#2](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_3.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="dfe55-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfe55-113">See also</span></span>
- [<span data-ttu-id="dfe55-114">Event (instruction)</span><span class="sxs-lookup"><span data-stu-id="dfe55-114">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)
- [<span data-ttu-id="dfe55-115">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="dfe55-115">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="dfe55-116">Événements</span><span class="sxs-lookup"><span data-stu-id="dfe55-116">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
