---
title: Structures de décision (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- statements [Visual Basic], control flow
- If statement [Visual Basic], decision structures
- If statement [Visual Basic], If...Then...Else
- control flow [Visual Basic], decision structures
- decision structures [Visual Basic]
- conditional statements [Visual Basic], decision structures
ms.assetid: 2e2e0895-4483-442a-b17c-26aead751ec2
ms.openlocfilehash: 4a76b2565c343e69ac3c11441035a7682a8f08ec
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59318934"
---
# <a name="decision-structures-visual-basic"></a>Structures de décision (Visual Basic)
Visual Basic vous permet de tester des conditions et d’effectuer des opérations différentes en fonction des résultats de ce test. Vous pouvez tester une condition vraie ou fausse, pour différentes valeurs d’une expression ou plusieurs exceptions générées lorsque vous exécutez une série d’instructions.  
  
 L’illustration suivante montre une structure de décision qui teste une condition est true et effectue des actions différentes selon qu’il est true ou false.  
  
 ![Un diagramme de flux d’une instruction If... Then... Construction de l’autre.](./media/decision-structures/if-then-else-construction.gif)  
  
## <a name="ifthenelse-construction"></a>If... Then... Construction Else  
 `If...Then...Else` constructions vous permettent de tester pour une ou plusieurs conditions et d’exécuter une ou plusieurs instructions selon chaque condition. Vous pouvez tester des conditions et prendre des mesures de plusieurs manières :  
  
-   Exécuter une ou plusieurs instructions si une condition est `True`  
  
-   Exécuter une ou plusieurs instructions si une condition est `False`  
  
-   Exécutez des instructions si une condition est `True` et d’autres s’il s’agit `False`  
  
-   Tester une condition supplémentaire si une condition préalable est `False`  
  
 La structure de contrôle qui offre toutes ces possibilités est le [si... Then... Else, instruction](../../../../visual-basic/language-reference/statements/if-then-else-statement.md). Vous pouvez utiliser une version de ligne si vous avez qu’un test et une instruction à exécuter. Si vous avez un ensemble de conditions et actions plus complexe, vous pouvez utiliser la version de plusieurs lignes.  
  
## <a name="selectcase-construction"></a>Sélectionnez... Construction de cas  
 Le `Select...Case` construction vous permet d’évaluer une expression une seule fois et d’exécuter différents jeux d’instructions selon différentes valeurs possibles. Pour plus d’informations, consultez [sélectionnez... Instruction case](../../../../visual-basic/language-reference/statements/select-case-statement.md).  
  
## <a name="trycatchfinally-construction"></a>Try... Catch... Pour finir de Construction  
 `Try...Catch...Finally` constructions vous permettent d’exécuter un ensemble d’instructions sous un environnement qui conserve le contrôle si l’un de vos instructions provoque une exception. Vous pouvez prendre des mesures différentes pour différentes exceptions. Vous pouvez éventuellement spécifier un bloc de code qui s’exécute avant de quitter la totalité `Try...Catch...Finally` construction, quel que soit ce qui se produit. Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
> [!NOTE]
>  Pour de nombreuses structures de contrôle, lorsque vous cliquez sur un mot clé, tous les mots clés dans la structure sont mis en surbrillance. Par exemple, lorsque vous cliquez sur `If` dans un `If...Then...Else` construction, toutes les instances de `If`, `Then`, `ElseIf`, `Else`, et `End If` dans la construction sont mises en surbrillance. Pour déplacer vers le mot clé en surbrillance suivant ou précédent, appuyez sur CTRL + MAJ + flèche bas ou CTRL + MAJ + flèche haut.  
  
## <a name="see-also"></a>Voir aussi

- [Flux de contrôle](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)
- [Structures de boucle](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
- [Autres structures de contrôle](../../../../visual-basic/programming-guide/language-features/control-flow/other-control-structures.md)
- [Structures de contrôle imbriquées](../../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [If, opérateur](../../../../visual-basic/language-reference/operators/if-operator.md)
