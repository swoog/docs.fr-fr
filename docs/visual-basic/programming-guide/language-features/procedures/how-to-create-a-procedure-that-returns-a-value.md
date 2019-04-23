---
title: 'Procédure : Créer une procédure qui retourne une valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- procedures [Visual Basic], returning a value
ms.assetid: 8ee19f95-a9ef-4033-963b-d224dca207c4
ms.openlocfilehash: 115c1df4bd49d5848d72c4cbd0242a49a12740c7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59335496"
---
# <a name="how-to-create-a-procedure-that-returns-a-value-visual-basic"></a>Procédure : Créer une procédure qui retourne une valeur (Visual Basic)
Vous utilisez un `Function` procédure pour retourner une valeur au code appelant.  
  
### <a name="to-create-a-procedure-that-returns-a-value"></a>Pour créer une procédure qui retourne une valeur  
  
1. En dehors de toute autre procédure, utilisez un `Function` instruction, suivie d’un `End Function` instruction.  
  
2. Dans le `Function` instruction, suivez le `Function` mot clé par le nom de la procédure, puis la liste de paramètres entre parenthèses.  
  
3. Suivez les parenthèses d’une `As` clause pour spécifier le type de données de la valeur retournée.  
  
4. Placez les instructions de procédure code entre la `Function` et `End Function` instructions.  
  
5. Utilisez un `Return` instruction pour retourner la valeur au code appelant.  
  
     Ce qui suit `Function` procédure calcule le côté le plus long, ou hypoténuse, d’un triangle rectangle, d’après les valeurs pour les deux côtés.  
  
     [!code-vb[VbVbcnProcedures#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#1)]  
  
     L’exemple suivant montre un appel typique à `hypotenuse`.  
  
     [!code-vb[VbVbcnProcedures#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Procédures de propriété](./property-procedures.md)
- [Procédures d’opérateur](./operator-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Function (instruction)](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Guide pratique pour Retourner une valeur à partir d’une procédure](./how-to-return-a-value-from-a-procedure.md)
- [Guide pratique pour Appeler une procédure qui retourne une valeur](./how-to-call-a-procedure-that-returns-a-value.md)
