---
title: Itérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Iterator
helpviewer_keywords:
- Iterator keyword [Visual Basic]
ms.assetid: 69cb0b04-ac87-49d0-bcfe-810c0d60daff
ms.openlocfilehash: 499949d1f4c20e1f465355bd076ba39f1496779b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58822698"
---
# <a name="iterator-visual-basic"></a>Itérateur (Visual Basic)
Spécifie qu’une fonction ou `Get` accesseur est un itérateur.  
  
## <a name="remarks"></a>Notes  
 Un *itérateur* effectue une itération personnalisée sur une collection. Un itérateur utilise le [Yield](../../../visual-basic/language-reference/statements/yield-statement.md) instruction pour retourner chaque élément dans la collection un à la fois. Quand un `Yield` instruction est atteinte, l’emplacement actuel dans le code est conservé. L'exécution redémarrera à partir de cet emplacement la prochaine fois que la fonction d'itérateur sera appelée.  
  
 Un itérateur peut être implémenté sous la forme d’une fonction ou un `Get` accesseur d’une définition de propriété. Le `Iterator` modificateur apparaît dans la déclaration de la fonction d’itérateur ou `Get` accesseur.  
  
 Vous appelez un itérateur depuis le code client en utilisant un [For Each... L’instruction suivante](../../../visual-basic/language-reference/statements/for-each-next-statement.md).  
  
 Le type de retour d’une fonction d’itérateur ou `Get` accesseur peut être <xref:System.Collections.IEnumerable>, <xref:System.Collections.Generic.IEnumerable%601>, <xref:System.Collections.IEnumerator>, ou <xref:System.Collections.Generic.IEnumerator%601>.  
  
 Un itérateur ne peut avoir aucun `ByRef` paramètres.  
  
 Un itérateur ne peut pas être présent dans un événement, un constructeur d’instance, un constructeur statique ou un destructeur statique.  
  
 Un itérateur peut être une fonction anonyme. Pour plus d'informations, consultez [Itérateurs](../../programming-guide/concepts/iterators.md).  
  
## <a name="usage"></a>Utilisation  
 Le modificateur `Iterator` peut être utilisé dans les contextes suivants :  
  
-   [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)  
  
-   [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre une fonction d’itérateur. La fonction d’itérateur a un `Yield` instruction qui se trouve dans un [pour... Suivant](../../../visual-basic/language-reference/statements/for-next-statement.md) boucle. Chaque itération de la [pour chaque](../../../visual-basic/language-reference/statements/for-each-next-statement.md) corps d’instruction dans `Main` crée un appel à la `Power` fonction d’itérateur. Chaque appel à la fonction d'itérateur continue vers l'exécution suivante de l'instruction `Yield`, qui se produit pendant l'itération suivante de la boucle `For…Next`.  
  
 [!code-vb[VbVbalrStatements#98](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class2.vb#98)]  
  
## <a name="example"></a>Exemple  
 L'exemple suivant illustre un accesseur `Get` qui est un itérateur. Le `Iterator` modificateur est dans la déclaration de propriété.  
  
 [!code-vb[VbVbalrStatements#99](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class2.vb#99)]  
  
 Pour obtenir des exemples supplémentaires, consultez [itérateurs](../../programming-guide/concepts/iterators.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.CompilerServices.IteratorStateMachineAttribute>
- [Itérateurs](../../programming-guide/concepts/iterators.md)
- [Yield (instruction)](../../../visual-basic/language-reference/statements/yield-statement.md)
