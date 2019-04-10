---
title: 'Procédure : Retourner une valeur à partir d’une procédure (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], returning from
- procedures [Visual Basic], returning a value
ms.assetid: 4bcc4724-2b4e-4df8-9b4b-16054607f87d
ms.openlocfilehash: 8b53df1634d2b9971bc44c968a17db81cac3924f
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59307884"
---
# <a name="how-to-return-a-value-from-a-procedure-visual-basic"></a>Procédure : Retourner une valeur à partir d’une procédure (Visual Basic)
Un `Function` procédure retourne une valeur au code appelant soit en exécutant un `Return` instruction ou en rencontrant une `Exit Function` ou `End Function` instruction.  
  
### <a name="to-return-a-value-using-the-return-statement"></a>Pour retourner une valeur à l’aide de l’instruction Return  
  
1. Placer un `Return` instruction au point où la tâche de la procédure est terminée.  
  
2. Suivez le `Return` mot clé avec une expression qui donne la valeur que vous souhaitez retourner au code appelant.  
  
3. Vous pouvez utiliser plusieurs instructions `Return` dans la même procédure.  
  
     Ce qui suit `Function` procédure calcule le côté le plus long, ou hypoténuse, d’un triangle rectangle et le retourne au code appelant.  
  
     [!code-vb[VbVbcnProcedures#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#1)]  
  
     L’exemple suivant montre un appel typique à `hypotenuse`, qui stocke la valeur retournée.  
  
     [!code-vb[VbVbcnProcedures#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#6)]  
  
### <a name="to-return-a-value-using-exit-function-or-end-function"></a>Pour retourner une valeur à l’aide de la fonction Exit ou End Function  
  
1. Au moins un endroit dans le `Function` procédure, assignez une valeur au nom de la procédure.  
  
2. Lorsque vous exécutez un `Exit Function` ou `End Function` instruction, Visual Basic retourne la valeur la plus récemment assignée au nom de la procédure.  
  
3. Vous pouvez utiliser plusieurs instructions `Exit Function` dans la même procédure et combiner des instructions `Return` et `Exit Function` dans la même procédure.  
  
4. Vous pouvez avoir un seul `End Function` instruction dans un `Function` procédure.  
  
     Pour plus d’informations et un exemple, consultez « Valeur de retour » dans [Function, instruction](../../../../visual-basic/language-reference/statements/function-statement.md).  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Procédures Property](./property-procedures.md)
- [Procédures d'opérateur](./operator-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Function, instruction](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Return, instruction](../../../../visual-basic/language-reference/statements/return-statement.md)
- [Procédure : créer une procédure qui retourne une valeur](./how-to-create-a-procedure-that-returns-a-value.md)
- [Procédure : appeler une procédure qui retourne une valeur](./how-to-call-a-procedure-that-returns-a-value.md)
