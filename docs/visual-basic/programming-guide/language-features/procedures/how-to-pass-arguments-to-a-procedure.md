---
title: 'Procédure : Passer des Arguments à une procédure (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- arguments [Visual Basic], passing to procedures
- procedures [Visual Basic], arguments
- procedures [Visual Basic], parameters
- procedure arguments
- Visual Basic code, procedures
- procedure parameters
- procedures [Visual Basic], calling
- argument passing [Visual Basic], procedures
ms.assetid: 08723588-3890-4ddc-8249-79e049e0f241
ms.openlocfilehash: 0bc7c9d09922b7fbef534e6b58389ca343cc1e13
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56974391"
---
# <a name="how-to-pass-arguments-to-a-procedure-visual-basic"></a>Procédure : Passer des Arguments à une procédure (Visual Basic)
Lorsque vous appelez une procédure, vous suivez le nom de la procédure avec une liste d’arguments entre parenthèses. Vous fournissez un argument correspondant à chaque paramètre requis de la procédure définit et vous pouvez éventuellement fournir des arguments à la `Optional` paramètres. Si vous ne fournissez pas un `Optional` paramètre dans l’appel, vous devez inclure une virgule pour marquer sa place dans la liste d’arguments si vous fournissez des arguments suivants.  
  
 Si vous avez l’intention de passer un argument d’un type de données différent de celui de son paramètre correspondant, tel que `Byte` à `String`, vous pouvez définir le commutateur de vérification de type ([Option Strict, instruction](../../../../visual-basic/language-reference/statements/option-strict-statement.md)) à `Off`. Si `Option Strict` est `On`, vous devez utiliser soit conversions étendues ou mots clés de conversion explicite. Pour plus d’informations, consultez [Widening and Narrowing Conversions](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md) et [les fonctions de Conversion de Type](../../../../visual-basic/language-reference/functions/type-conversion-functions.md).  
  
 Pour plus d’informations, consultez [les paramètres de procédure et les Arguments](./procedure-parameters-and-arguments.md).  
  
### <a name="to-pass-one-or-more-arguments-to-a-procedure"></a>Pour passer un ou plusieurs arguments à une procédure  
  
1.  Dans l’instruction appelante, faites suivre le nom de procédure avec des parenthèses.  
  
2.  Dans les parenthèses, placez une liste d’arguments. Inclure un argument pour chaque paramètre obligatoire, que la procédure définit et séparez les arguments par des virgules.  
  
3.  Assurez-vous que chaque argument est une expression valide qui correspond à un type de données convertible au type de la procédure définit pour le paramètre correspondant.  
  
4.  Si un paramètre est défini en tant que [facultatif](../../../../visual-basic/language-reference/modifiers/optional.md), vous pouvez inclure dans la liste d’arguments ou l’omettre. Si vous l’omettez, la procédure utilise la valeur par défaut définie pour ce paramètre.  
  
5.  Si vous omettez un argument pour un `Optional` paramètre et qu’un autre paramètre après lui dans la liste de paramètres, vous pouvez marquer la place de l’argument omis par une virgule supplémentaire dans la liste d’arguments.  
  
     L’exemple suivant appelle le Visual Basic <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> (fonction).  
  
     [!code-vb[VbVbcnProcedures#34](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#34)]  
  
     L’exemple précédent fournit le premier argument obligatoire, qui est la chaîne de message à afficher. Elle omet un argument pour le deuxième paramètre facultatif qui spécifie les boutons à afficher sur la boîte de message. Étant donné que l’appel ne fournit pas de valeur, `MsgBox` utilise la valeur par défaut, `MsgBoxStyle.OKOnly`, qui affiche uniquement un **OK** bouton.  
  
     La deuxième virgule dans la liste d’arguments marque la place du deuxième argument omis et la dernière chaîne est passée au troisième paramètre facultatif de `MsgBox`, qui est le texte à afficher dans la barre de titre.  
  
## <a name="see-also"></a>Voir aussi

- [Procédures Sub](./sub-procedures.md)
- [Procédures Function](./function-procedures.md)
- [Procédures de propriété](./property-procedures.md)
- [Procédures d’opérateur](./operator-procedures.md)
- [Guide pratique pour Définir un paramètre pour une procédure](./how-to-define-a-parameter-for-a-procedure.md)
- [Passage d’un argument par valeur et par référence](./passing-arguments-by-value-and-by-reference.md)
- [Procédures récursives](./recursive-procedures.md)
- [Surcharge de procédure](./procedure-overloading.md)
- [Objets et classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
- [Programmation orientée objet (Visual Basic)](../../concepts/object-oriented-programming.md)
