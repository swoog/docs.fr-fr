---
title: L'instruction ne peut pas terminer un bloc en dehors d'une instruction 'If' d'une ligne
ms.date: 07/20/2015
f1_keywords:
- vbc32005
- bc32005
helpviewer_keywords:
- BC32005
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
ms.openlocfilehash: 0e645ccf17d0aba702a576791622aa4e9b3dd5e0
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64593266"
---
# <a name="statement-cannot-end-a-block-outside-of-a-line-if-statement"></a>L'instruction ne peut pas terminer un bloc en dehors d'une instruction 'If' d'une ligne
Une seule ligne `If` instruction contient plusieurs instructions séparées par le signe deux-points ( :),) d'entre eux étant un `End` instruction pour un bloc de contrôle en dehors de la ligne unique `If`. Une ligne `If` instructions n’utilisent pas la `End If` instruction.  
  
 **ID d’erreur :** BC32005  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Déplacer la ligne unique `If` instruction en dehors du bloc de contrôle qui contient le `End If` instruction.  
  
## <a name="see-also"></a>Voir aussi

- [If...Then...Else (instruction)](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
