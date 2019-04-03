---
title: Reprendre sans gestion d'erreur
ms.date: 07/20/2015
f1_keywords:
- vbrID20
ms.assetid: f9631804-fd36-4443-b36c-30db827e6176
ms.openlocfilehash: 8cb58064e7249273051ead87cbc6841d13cdf5ad
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58840443"
---
# <a name="resume-without-error"></a>Reprendre sans gestion d'erreur
Un `Resume` instruction est apparue en dehors du code de gestion des erreurs ou le code est passé dans un gestionnaire d’erreurs, même si aucune erreur s’est produite.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déplacer le `Resume` instruction dans un gestionnaire d’erreurs, ou supprimez-le.  
  
2.  Passages à des étiquettes ne peut pas se produire entre procédures, recherchez dans la procédure pour l’étiquette qui identifie le Gestionnaire d’erreurs. Si vous trouvez une étiquette dupliquée spécifiée comme cible d’un `GoTo` instruction qui n’est pas un `On Error GoTo` instruction, modifiez l’étiquette de ligne pour correspondre à la cible attendue.  
  
## <a name="see-also"></a>Voir aussi

- [Resume (instruction)](../../../visual-basic/language-reference/statements/resume-statement.md)
- [On Error (instruction)](../../../visual-basic/language-reference/statements/on-error-statement.md)
