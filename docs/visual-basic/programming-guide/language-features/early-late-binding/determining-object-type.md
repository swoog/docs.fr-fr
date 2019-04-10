---
title: Détermination du type Object (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- classes [Visual Basic], discovering which an object belongs to
- types [Visual Basic], determining Visual Basic object types
- object variables [Visual Basic], testing values
- TypeOf...Is expression, object type at run time
- TypeName function
- objects [Visual Basic], type determining
ms.assetid: d95e7ad1-cd63-41d6-9a28-d7a1380d49c1
ms.openlocfilehash: 4014bef2e0c27a0f6a684bc1ed95019f392062a5
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59302710"
---
# <a name="determining-object-type-visual-basic"></a>Détermination du type Object (Visual Basic)
Variables de l’objet générique (autrement dit, les variables que vous déclarez comme `Object`) peut contenir des objets à partir de n’importe quelle classe. Lors de l’utilisation de variables de type `Object`, vous devrez peut-être prendre des mesures différentes selon la classe de l’objet ; par exemple, certains objets ne peuvent pas en charge une propriété ou méthode particulière. Visual Basic fournit deux moyens de déterminer quel type d’objet est stocké dans une variable objet : le `TypeName` (fonction) et le `TypeOf...Is` opérateur.  
  
## <a name="typename-and-typeofis"></a>TypeName et TypeOf... Est  
 Le `TypeName` fonction retourne une chaîne et est le meilleur choix lorsque vous devez stocker ou afficher le nom de classe d’un objet, comme illustré dans le fragment de code suivant :  
  
 [!code-vb[VbVbalrOOP#92](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#92)]  
  
 Le `TypeOf...Is` opérateur est le meilleur choix pour le test d’un type d’objet, car il est beaucoup plus rapide qu’une comparaison de chaîne équivalente à l’aide de `TypeName`. Le fragment de code suivant utilise `TypeOf...Is` au sein d’un `If...Then...Else` instruction :  
  
 [!code-vb[VbVbalrOOP#93](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#93)]  
  
 Un mot de prudence est due ici. Le `TypeOf...Is` opérateur retourne `True` si un objet est d’un type spécifique, ou est dérivé d’un type spécifique. Presque tout ce que vous faites avec Visual Basic implique des objets, qui incluent certains éléments pas normalement considérés comme des objets, tels que des chaînes et les entiers. Ces objets sont dérivés et héritent des méthodes de <xref:System.Object>. Quand il est passé un `Integer` et évaluée avec `Object`, le `TypeOf...Is` opérateur retourne `True`. L’exemple suivant indique que le paramètre `InParam` est à la fois un `Object` et un `Integer`:  
  
 [!code-vb[VbVbalrOOP#94](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#94)]  
  
 L’exemple suivant utilise à la fois `TypeOf...Is` et `TypeName` pour déterminer le type d’objet passé dans le `Ctrl` argument. Le `TestObject` les appels de procédure `ShowType` avec trois différents types de contrôles.  
  
#### <a name="to-run-the-example"></a>Pour exécuter l'exemple  
  
1. Créez un nouveau projet d’Application de Windows et ajoutez un <xref:System.Windows.Forms.Button> contrôle, un <xref:System.Windows.Forms.CheckBox> contrôle et un <xref:System.Windows.Forms.RadioButton> contrôle au formulaire.  
  
2. À partir du bouton sur votre formulaire, appelez le `TestObject` procédure.  
  
3. Ajoutez le code suivant à votre formulaire :  
  
     [!code-vb[VbVbalrOOP#95](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#95)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Information.TypeName%2A>
- [Appel d'une propriété ou méthode à l'aide d'un nom de chaîne](../../../../visual-basic/programming-guide/language-features/early-late-binding/calling-a-property-or-method-using-a-string-name.md)
- [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md)
- [If...Then...Else, instruction](../../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [String, type de données](../../../../visual-basic/language-reference/data-types/string-data-type.md)
- [Integer, type de données](../../../../visual-basic/language-reference/data-types/integer-data-type.md)
