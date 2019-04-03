---
title: L'accesseur 'Set' de la propriété '<propertyname>' n'est pas accessible
ms.date: 07/20/2015
f1_keywords:
- vbc31102
- bc31102
helpviewer_keywords:
- BC31102
ms.assetid: 6f7b31b7-3656-4ae1-8851-90f5f4c6950a
ms.openlocfilehash: 3bc50d6762998ca5d8f445d84c8b698c9f46436f
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58834463"
---
# <a name="set-accessor-of-property-propertyname-is-not-accessible"></a><span data-ttu-id="f17dd-102">Accesseur de propriété ' set' '\<nom_propriété >' n’est pas accessible</span><span class="sxs-lookup"><span data-stu-id="f17dd-102">'Set' accessor of property '\<propertyname>' is not accessible</span></span>
<span data-ttu-id="f17dd-103">Une instruction essaie de stocker la valeur d’une propriété lorsqu’elle n’a pas accès à la propriété `Set` procédure.</span><span class="sxs-lookup"><span data-stu-id="f17dd-103">A statement attempts to store the value of a property when it does not have access to the property's `Set` procedure.</span></span>  
  
 <span data-ttu-id="f17dd-104">Si le [instruction Set](../../../visual-basic/language-reference/statements/set-statement.md) est marquée avec un accès plus restrictif niveau que ses [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md), tentative d’affecter la valeur de propriété peut échouer dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="f17dd-104">If the [Set Statement](../../../visual-basic/language-reference/statements/set-statement.md) is marked with a more restrictive access level than its [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md), an attempt to set the property value could fail in the following cases:</span></span>  
  
-   <span data-ttu-id="f17dd-105">Le `Set` instruction est marquée [privé](../../../visual-basic/language-reference/modifiers/private.md) et le code appelant est en dehors de la classe ou structure dans laquelle la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="f17dd-105">The `Set` statement is marked [Private](../../../visual-basic/language-reference/modifiers/private.md) and the calling code is outside the class or structure in which the property is defined.</span></span>  
  
-   <span data-ttu-id="f17dd-106">Le `Set` instruction est marquée [protégé](../../../visual-basic/language-reference/modifiers/protected.md) et le code appelant n’est pas dans la classe ou structure dans laquelle la propriété est définie, ni dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="f17dd-106">The `Set` statement is marked [Protected](../../../visual-basic/language-reference/modifiers/protected.md) and the calling code is not in the class or structure in which the property is defined, nor in a derived class.</span></span>  
  
-   <span data-ttu-id="f17dd-107">Le `Set` instruction est marquée [Friend](../../../visual-basic/language-reference/modifiers/friend.md) et le code appelant n’est pas dans le même assembly dans lequel la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="f17dd-107">The `Set` statement is marked [Friend](../../../visual-basic/language-reference/modifiers/friend.md) and the calling code is not in the same assembly in which the property is defined.</span></span>  
  
 <span data-ttu-id="f17dd-108">**ID d’erreur :** BC31102</span><span class="sxs-lookup"><span data-stu-id="f17dd-108">**Error ID:** BC31102</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f17dd-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f17dd-109">To correct this error</span></span>  
  
-   <span data-ttu-id="f17dd-110">Si vous avez le contrôle de code source qui définit la propriété, vous devez déclarer le `Set` procédure avec le même niveau d’accès en tant que la propriété proprement dite.</span><span class="sxs-lookup"><span data-stu-id="f17dd-110">If you have control of the source code defining the property, consider declaring the `Set` procedure with the same access level as the property itself.</span></span>  
  
-   <span data-ttu-id="f17dd-111">Si vous n’avez pas de contrôle de code source qui définit la propriété, ou vous devez limiter la `Set` procédure niveau d’accès plus que la propriété proprement dite, essayez de déplacer l’instruction qui définit la valeur de propriété à une région de code qui offre un meilleur accès à la propriété.</span><span class="sxs-lookup"><span data-stu-id="f17dd-111">If you do not have control of the source code defining the property, or you must restrict the `Set` procedure access level more than the property itself, try to move the statement that sets the property value to a region of code that has better access to the property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f17dd-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f17dd-112">See also</span></span>

- [<span data-ttu-id="f17dd-113">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="f17dd-113">Property Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
- [<span data-ttu-id="f17dd-114">Guide pratique pour Déclarer une propriété avec des niveaux d’accès mixtes</span><span class="sxs-lookup"><span data-stu-id="f17dd-114">How to: Declare a Property with Mixed Access Levels</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-a-property-with-mixed-access-levels.md)
