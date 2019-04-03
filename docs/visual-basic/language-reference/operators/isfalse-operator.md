---
title: Opérateur IsFalse (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.isfalse
helpviewer_keywords:
- AndAlso operator [Visual Basic]
- IsFalse operator [Visual Basic]
ms.assetid: 37fc9dbf-e5cc-4570-b93f-7213447974df
ms.openlocfilehash: 9f25c406038486224c2c4708c86ef86889c44c15
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58818486"
---
# <a name="isfalse-operator-visual-basic"></a>Opérateur IsFalse (Visual Basic)
Détermine si une expression est `False`.  
  
 Vous ne pouvez pas appeler `IsFalse` explicitement dans votre code, mais le Visual Basic compilateur peut l’utiliser pour générer le code à partir de `AndAlso` clauses. Si vous définissez une classe ou une structure et ensuite utiliser une variable de ce type dans un `AndAlso` clause, vous devez définir `IsFalse` sur cette classe ou structure.  
  
 Le compilateur considère les `IsFalse` et `IsTrue` opérateurs comme un *mis en correspondance de paire*. Cela signifie que si vous définissez un d’eux, vous devez également définir le.  
  
> [!NOTE]
>  Le `IsFalse` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsque son opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant définit le contour d’une structure qui contient les définitions pour le `IsFalse` et `IsTrue` opérateurs.  
  
 [!code-vb[VbVbalrOperators#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#28)]  
  
## <a name="see-also"></a>Voir aussi

- [IsTrue (opérateur)](../../../visual-basic/language-reference/operators/istrue-operator.md)
- [Guide pratique pour Définir un opérateur](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [AndAlso (opérateur)](../../../visual-basic/language-reference/operators/andalso-operator.md)
