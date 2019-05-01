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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62055145"
---
# <a name="set-accessor-of-property-propertyname-is-not-accessible"></a>Accesseur de propriété ' set' '\<nom_propriété >' n’est pas accessible
Une instruction essaie de stocker la valeur d’une propriété lorsqu’elle n’a pas accès à la propriété `Set` procédure.  
  
 Si le [instruction Set](../../../visual-basic/language-reference/statements/set-statement.md) est marquée avec un accès plus restrictif niveau que ses [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md), tentative d’affecter la valeur de propriété peut échouer dans les cas suivants :  
  
- Le `Set` instruction est marquée [privé](../../../visual-basic/language-reference/modifiers/private.md) et le code appelant est en dehors de la classe ou structure dans laquelle la propriété est définie.  
  
- Le `Set` instruction est marquée [protégé](../../../visual-basic/language-reference/modifiers/protected.md) et le code appelant n’est pas dans la classe ou structure dans laquelle la propriété est définie, ni dans une classe dérivée.  
  
- Le `Set` instruction est marquée [Friend](../../../visual-basic/language-reference/modifiers/friend.md) et le code appelant n’est pas dans le même assembly dans lequel la propriété est définie.  
  
 **ID d’erreur :** BC31102  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Si vous avez le contrôle de code source qui définit la propriété, vous devez déclarer le `Set` procédure avec le même niveau d’accès en tant que la propriété proprement dite.  
  
- Si vous n’avez pas de contrôle de code source qui définit la propriété, ou vous devez limiter la `Set` procédure niveau d’accès plus que la propriété proprement dite, essayez de déplacer l’instruction qui définit la valeur de propriété à une région de code qui offre un meilleur accès à la propriété.  
  
## <a name="see-also"></a>Voir aussi

- [Procédures de propriété](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
- [Guide pratique pour Déclarer une propriété avec des niveaux d’accès mixtes](../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-a-property-with-mixed-access-levels.md)
