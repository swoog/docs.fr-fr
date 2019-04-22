---
title: Autres structures de contrôle (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- statements [Visual Basic], control flow
- control structures [Visual Basic]
ms.assetid: 24b811f7-98ba-40ec-8dd3-4d528cfa4574
ms.openlocfilehash: c42070ce2ea866e59e1b2e190f7c05e1ee7cc922
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58819318"
---
# <a name="other-control-structures-visual-basic"></a>Autres structures de contrôle (Visual Basic)
Visual Basic fournit des structures de contrôle qui vous aident à supprimer une ressource ou réduisent le nombre de fois où que vous devez répéter une référence d’objet.  
  
## <a name="usingend-using-construction"></a>À l’aide de... À l’aide de la Construction de fin  
 Le `Using...End Using` construction établit un bloc d’instruction dans lequel vous utilisez une ressource telle qu’une connexion SQL. Vous pouvez éventuellement acquérir la ressource avec le `Using` instruction. Lorsque vous quittez le `Using` bloc, Visual Basic supprime automatiquement la ressource afin qu’il soit disponible pour tout autre code à utiliser. La ressource doit être locale et supprimable. Pour plus d’informations, consultez [using, instruction](../../../../visual-basic/language-reference/statements/using-statement.md).  
  
## <a name="withend-with-construction"></a>Avec... Se terminer par Construction  
 Le `With...End With` vous permet de spécifier une référence d’objet une seule fois, puis exécutez une série d’instructions qui accèdent à ses membres. Cela peut simplifier votre code et améliorer les performances, car Visual Basic n’est pas obligé de rétablir la référence pour chaque instruction qui y accède. Pour plus d’informations, consultez [avec... End With, instruction](../../../../visual-basic/language-reference/statements/with-end-with-statement.md).  
  
## <a name="see-also"></a>Voir aussi

- [Flux de contrôle](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)
- [Structures de décision](../../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)
- [Structures de boucle](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
- [Structures de contrôle imbriquées](../../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [Using (instruction)](../../../../visual-basic/language-reference/statements/using-statement.md)
- [With...End With (instruction)](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)
