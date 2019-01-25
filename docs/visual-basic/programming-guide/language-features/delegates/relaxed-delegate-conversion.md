---
title: Conversion simplifiée des délégués (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- relaxed delegate conversion [Visual Basic]
- delegates [Visual Basic], relaxed conversion
- conversions [Visual Basic], relaxed delegate
ms.assetid: 64f371d0-5416-4f65-b23b-adcbf556e81c
ms.openlocfilehash: e2838b6473b8c00927073a530b4b49870fcfa9c6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54600377"
---
# <a name="relaxed-delegate-conversion-visual-basic"></a>Conversion simplifiée des délégués (Visual Basic)
Conversion simplifiée des délégués vous permet de vous permettent d’affecter des sous-routines et des fonctions aux délégués ou aux gestionnaires même lorsque leurs signatures ne sont pas identiques. Par conséquent, la liaison aux délégués devient cohérente avec la liaison déjà autorisée pour les appels de méthode.  
  
## <a name="parameters-and-return-type"></a>Paramètres et Type de retour  
 À la place de correspondance exacte de signature, la conversion simplifiée requiert que les conditions suivantes est remplie lorsque `Option Strict` est défini sur `On`:  
  
-   Une conversion étendue doit avoir le type de données de chaque paramètre de délégué au type de données du paramètre correspondant de la fonction attribué ou `Sub`. Dans l’exemple suivant, le délégué `Del1` a un paramètre, un `Integer`. Paramètre `m` dans l’expression lambda assigné expressions doivent avoir un type de données pour laquelle il existe une conversion étendue de `Integer`, tel que `Long` ou `Double`.  
  
     [!code-vb[VbVbalrRelaxedDelegates#1](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_1.vb)]  
  
     [!code-vb[VbVbalrRelaxedDelegates#2](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_2.vb)]  
  
     Les conversions restrictives sont autorisées uniquement lorsque `Option Strict` est défini sur `Off`.  
  
     [!code-vb[VbVbalrRelaxedDelegates#8](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_3.vb)]  
  
-   Une conversion étendue doit exister dans la direction opposée du type de retour de la fonction assignée ou `Sub` pour le type de retour du délégué. Dans les exemples suivants, le corps de chaque expression lambda assignée doit correspondre à un type de données qui s’étend à `Integer` , car le type de retour de `del1` est `Integer`.  
  
     [!code-vb[VbVbalrRelaxedDelegates#3](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_4.vb)]  
  
 Si `Option Strict` est défini sur `Off`, la restriction étendue est supprimée dans les deux sens.  
  
 [!code-vb[VbVbalrRelaxedDelegates#4](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_5.vb)]  
  
## <a name="omitting-parameter-specifications"></a>L’omission des spécifications de paramètre  
 Délégués souples permettent d’omettre complètement les spécifications de paramètre dans la méthode assignée :  
  
 [!code-vb[VbVbalrRelaxedDelegates#5](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_6.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#6](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_7.vb)]  
  
 Notez que vous ne pouvez pas spécifier certains paramètres et omettre d’autres.  
  
 [!code-vb[VbVbalrRelaxedDelegates#15](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_8.vb)]  
  
 La possibilité d’omettre des paramètres est utile dans une situation telles que la définition d’un gestionnaire d’événements, où plusieurs paramètres complexes sont impliqués. Les arguments de certains gestionnaires d’événements ne sont pas utilisés. Au lieu de cela, le gestionnaire accède directement à l’état du contrôle sur lequel l’événement est enregistré et ignore les arguments. Délégués souples permettent d’omettre les arguments dans les déclarations qui ne comprennent aucune ambiguïté. Dans l’exemple suivant, la méthode entièrement spécifiée `OnClick` peut être réécrite en tant que `RelaxedOnClick`.  
  
```vb  
Sub OnClick(ByVal sender As Object, ByVal e As EventArgs) Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
  
Sub RelaxedOnClick() Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
```  
  
## <a name="addressof-examples"></a>Exemples d’AddressOf  
 Pour faciliter les relations de type voir, les expressions lambda sont utilisées dans les exemples précédents. Toutefois, les mêmes simplifications sont autorisées pour les assignations de délégués qui utilisent `AddressOf`, `Handles`, ou `AddHandler`.  
  
 Dans l’exemple suivant, les fonctions `f1`, `f2`, `f3`, et `f4` peuvent être affectés à `Del1`.  
  
 [!code-vb[VbVbalrRelaxedDelegates#1](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_1.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#7](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_9.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#9](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_10.vb)]  
  
 L’exemple suivant est valide uniquement lorsque `Option Strict` est défini sur `Off`.  
  
 [!code-vb[VbVbalrRelaxedDelegates#14](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_11.vb)]  
  
## <a name="dropping-function-returns"></a>Suppression des retours de fonction  
 Conversion simplifiée des délégués vous permet d’assigner une fonction à un `Sub` délégué, en ignorant la valeur de retournée de la fonction. Toutefois, vous ne pouvez pas assigner un `Sub` à un délégué de fonction. Dans l’exemple suivant, l’adresse de fonction `doubler` est affectée à `Sub` déléguer `Del3`.  
  
 [!code-vb[VbVbalrRelaxedDelegates#10](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_12.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#11](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_13.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Expressions lambda](../../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [Conversions étendues et restrictives](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Délégués](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [Guide pratique pour Passer des procédures à une autre procédure en Visual Basic](../../../../visual-basic/programming-guide/language-features/delegates/how-to-pass-procedures-to-another-procedure.md)
- [Inférence de type local](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [Option Strict (instruction)](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
