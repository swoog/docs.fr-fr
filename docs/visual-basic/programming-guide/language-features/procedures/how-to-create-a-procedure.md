---
title: 'Procédure : Créer une procédure (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- Visual Basic code, reusing
- procedure declarations
- procedures [Visual Basic], about procedures
ms.assetid: 4f779247-0b50-47e8-9e5c-ab5cf39ac0d2
ms.openlocfilehash: 0f3b0a793b2751b0ec9bb2b7cd6fedc12ae19e18
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56970803"
---
# <a name="how-to-create-a-procedure-visual-basic"></a>Procédure : Créer une procédure (Visual Basic)
Vous insérez une procédure entre une instruction de déclaration initiale (`Sub` ou `Function`) et une instruction de déclaration de fin (`End Sub` ou `End Function`). Code de tous les la procédure se trouve entre ces instructions.  
  
 Une procédure ne peut pas contenir une autre procédure, ses instructions de début et de fin doit donc être en dehors de toute autre procédure.  
  
 Si vous avez le code qui effectue la même tâche dans des endroits différents, vous pouvez écrire la tâche une fois qu’une procédure et puis l’appeler à partir de différents endroits dans votre code.  
  
### <a name="to-create-a-procedure-that-does-not-return-a-value"></a>Pour créer une procédure qui ne retourne pas de valeur  
  
1.  En dehors de toute autre procédure, utilisez un `Sub` instruction, suivie d’un `End Sub` instruction.  
  
2.  Dans le `Sub` instruction, suivez le `Sub` mot clé avec le nom de la procédure, puis la liste de paramètres entre parenthèses.  
  
3.  Placez les instructions de procédure code entre la `Sub` et `End Sub` instructions.  
  
### <a name="to-create-a-procedure-that-returns-a-value"></a>Pour créer une procédure qui retourne une valeur  
  
1.  En dehors de toute autre procédure, utilisez un `Function` instruction, suivie d’un `End Function` instruction.  
  
2.  Dans le `Function` instruction, suivez le `Function` mot clé avec le nom de la procédure, puis la liste de paramètres entre parenthèses, puis un `As` clause qui spécifie le type de données de la valeur de retour.  
  
3.  Placez les instructions de procédure code entre la `Function` et `End Function` instructions.  
  
4.  Utilisez un `Return` instruction pour retourner la valeur au code appelant.  
  
### <a name="to-connect-your-new-procedure-with-the-old-repetitive-blocks-of-code"></a>Pour connecter votre nouvelle procédure avec l’ancien répétitives des blocs de code  
  
1.  Assurez-vous que vous définissez la nouvelle procédure dans un endroit où l’ancien code a accès à celui-ci.  
  
2.  Dans votre bloc de code ancien, répétitives, remplacez les instructions qui effectuent les tâches répétitives avec une seule instruction qui appelle la `Sub` ou `Function` procédure.  
  
3.  Si votre procédure est un `Function` qui retourne une valeur, assurez-vous que votre instruction appelante exécute une action avec la valeur retournée, telle que le stockage dans une variable, dans le cas contraire la valeur sera perdue.  
  
## <a name="example"></a>Exemple  
 Ce qui suit `Function` procédure calcule le côté le plus long, ou hypoténuse, d’un triangle rectangle, d’après les valeurs pour les deux côtés.  
  
 [!code-vb[VbVbcnProcedures#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Procédures Function](./function-procedures.md)
- [Procédures de propriété](./property-procedures.md)
- [Procédures d’opérateur](./operator-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Procédures récursives](./recursive-procedures.md)
- [Surcharge de procédure](./procedure-overloading.md)
- [Objets et classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
- [Programmation orientée objet (Visual Basic)](../../concepts/object-oriented-programming.md)
