---
title: Reprendre sans gestion d'erreur
ms.date: 07/20/2015
f1_keywords:
- vbrID20
ms.assetid: f9631804-fd36-4443-b36c-30db827e6176
ms.openlocfilehash: 5e45f713a433365b4bbc8286154a3b877b08ec59
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33597873"
---
# <a name="resume-without-error"></a>Reprendre sans gestion d'erreur
A `Resume` instruction apparaît en dehors du code de gestion des erreurs ou le code est passé dans un gestionnaire d’erreurs, même si aucune erreur s’est produite.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déplacer la `Resume` instruction dans un gestionnaire d’erreurs ou de le supprimer.  
  
2.  Passages à des étiquettes ne peuvent pas se produire entre procédures, recherchez dans la procédure pour l’étiquette qui identifie le Gestionnaire d’erreurs. Si vous trouvez une étiquette dupliquée spécifiée comme cible d’un `GoTo` instruction qui n’est pas un `On Error GoTo` instruction, modifiez l’étiquette de ligne pour s’accorder avec sa cible prévue.  
  
## <a name="see-also"></a>Voir aussi  
 [Resume (instruction)](../../../visual-basic/language-reference/statements/resume-statement.md)  
 [On Error (instruction)](../../../visual-basic/language-reference/statements/on-error-statement.md)
