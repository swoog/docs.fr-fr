---
title: 'Procédure : Créer une procédure qui retourne une valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- procedures [Visual Basic], returning a value
ms.assetid: 8ee19f95-a9ef-4033-963b-d224dca207c4
ms.openlocfilehash: 18becfe05da27e538c5c294b26e0bb7aa19cad2b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506418"
---
# <a name="how-to-create-a-procedure-that-returns-a-value-visual-basic"></a>Procédure : Créer une procédure qui retourne une valeur (Visual Basic)
Vous utilisez un `Function` procédure pour retourner une valeur au code appelant.  
  
### <a name="to-create-a-procedure-that-returns-a-value"></a>Pour créer une procédure qui retourne une valeur  
  
1.  En dehors de toute autre procédure, utilisez un `Function` instruction, suivie d’un `End Function` instruction.  
  
2.  Dans le `Function` instruction, suivez le `Function` mot clé par le nom de la procédure, puis la liste de paramètres entre parenthèses.  
  
3.  Suivez les parenthèses d’une `As` clause pour spécifier le type de données de la valeur retournée.  
  
4.  Placez les instructions de procédure code entre la `Function` et `End Function` instructions.  
  
5.  Utilisez un `Return` instruction pour retourner la valeur au code appelant.  
  
     Ce qui suit `Function` procédure calcule le côté le plus long, ou hypoténuse, d’un triangle rectangle, d’après les valeurs pour les deux côtés.  
  
     [!code-vb[VbVbcnProcedures#1](./codesnippet/VisualBasic/how-to-create-a-procedure-that-returns-a-value_1.vb)]  
  
     L’exemple suivant montre un appel typique à `hypotenuse`.  
  
     [!code-vb[VbVbcnProcedures#6](./codesnippet/VisualBasic/how-to-create-a-procedure-that-returns-a-value_2.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Procédures de propriété](./property-procedures.md)
- [Procédures d’opérateur](./operator-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Function (instruction)](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Guide pratique pour Retourner une valeur à partir d’une procédure](./how-to-return-a-value-from-a-procedure.md)
- [Guide pratique pour Appeler une procédure qui retourne une valeur](./how-to-call-a-procedure-that-returns-a-value.md)
