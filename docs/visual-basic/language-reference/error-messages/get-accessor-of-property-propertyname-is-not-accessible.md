---
title: '&#39;Obtenir&#39; accesseur de propriété &#39; &lt;propertyname&gt; &#39; n’est pas accessible'
ms.date: 07/20/2015
f1_keywords:
- vbc31103
- bc31103
helpviewer_keywords:
- BC31103
ms.assetid: 3c346c32-7669-4b04-841d-7a9df9cb703e
ms.openlocfilehash: 10b7168ac40ca7c7d696cd63cd823454f404bb94
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582212"
---
# <a name="39get39-accessor-of-property-39ltpropertynamegt39-is-not-accessible"></a>&#39;Obtenir&#39; accesseur de propriété &#39; &lt;propertyname&gt; &#39; n’est pas accessible
Une instruction essaie de récupérer la valeur d’une propriété lorsqu’elle n’a pas accès à la propriété `Get` procédure.  
  
 Si le [une instruction Get](../../../visual-basic/language-reference/statements/get-statement.md) est marquée avec un accès plus restrictif niveau que ses [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md), une tentative de lecture de la valeur de propriété peut échouer dans les cas suivants :  
  
-   Le `Get` instruction est marquée [privé](../../../visual-basic/language-reference/modifiers/private.md) et le code appelant est en dehors de la classe ou structure dans laquelle la propriété est définie.  
  
-   Le `Get` instruction est marquée [protégé](../../../visual-basic/language-reference/modifiers/protected.md) et le code appelant n’est pas dans la classe ou structure dans laquelle la propriété est définie, ni dans une classe dérivée.  
  
-   Le `Get` instruction est marquée [Friend](../../../visual-basic/language-reference/modifiers/friend.md) et le code appelant n’est pas dans le même assembly dans lequel la propriété est définie.  
  
 **ID d’erreur :** BC31103  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Si vous avez le contrôle de code source qui définit la propriété, vous devez déclarer le `Get` procédure avec le même niveau d’accès en tant que la propriété proprement dite.  
  
-   Si vous n’avez pas de contrôle de code source qui définit la propriété, ou vous devez limiter la `Get` procédure niveau d’accès plus que la propriété proprement dite, essayez de déplacer l’instruction qui lit la valeur de propriété à une région de code qui offre un meilleur accès à la propriété.  
  
## <a name="see-also"></a>Voir aussi
- [Procédures de propriété](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
- [Guide pratique pour Déclarer une propriété avec des niveaux d’accès mixtes](../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-a-property-with-mixed-access-levels.md)
