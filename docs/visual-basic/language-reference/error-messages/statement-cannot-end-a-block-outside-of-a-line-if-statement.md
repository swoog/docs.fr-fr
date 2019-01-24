---
title: L’instruction ne peut pas se terminer un bloc en dehors d’une ligne &#39;si&#39; instruction
ms.date: 07/20/2015
f1_keywords:
- vbc32005
- bc32005
helpviewer_keywords:
- BC32005
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
ms.openlocfilehash: 78fe136acbd09e202b1daeb16dd540cf42ada390
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574714"
---
# <a name="statement-cannot-end-a-block-outside-of-a-line-39if39-statement"></a>L’instruction ne peut pas se terminer un bloc en dehors d’une ligne &#39;si&#39; instruction
Une seule ligne `If` instruction contient plusieurs instructions séparées par le signe deux-points ( :),) d'entre eux étant un `End` instruction pour un bloc de contrôle en dehors de la ligne unique `If`. Une ligne `If` instructions n’utilisent pas la `End If` instruction.  
  
 **ID d’erreur :** BC32005  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Déplacer la ligne unique `If` instruction en dehors du bloc de contrôle qui contient le `End If` instruction.  
  
## <a name="see-also"></a>Voir aussi
- [If...Then...Else (instruction)](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
