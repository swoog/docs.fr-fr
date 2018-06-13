---
title: Opérateur IsFalse (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.isfalse
helpviewer_keywords:
- AndAlso operator [Visual Basic]
- IsFalse operator [Visual Basic]
ms.assetid: 37fc9dbf-e5cc-4570-b93f-7213447974df
ms.openlocfilehash: e84b2162eb0763725f05bc52d5c4223d7c430b81
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33600044"
---
# <a name="isfalse-operator-visual-basic"></a>Opérateur IsFalse (Visual Basic)
Détermine si une expression est `False`.  
  
 Vous ne pouvez pas appeler `IsFalse` explicitement dans votre code, mais Visual Basic compilateur peut l’utiliser pour générer le code à partir de `AndAlso` clauses. Si vous définissez une classe ou une structure et ensuite utiliser une variable de ce type dans un `AndAlso` clause, vous devez définir `IsFalse` sur cette classe ou structure.  
  
 Le compilateur considère la `IsFalse` et `IsTrue` opérateurs comme un *paire équilibrée*. Cela signifie que si vous définissez un d’eux, vous devez également définir la deuxième.  
  
> [!NOTE]
>  Le `IsFalse` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsque son opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, assurez-vous que vous comprenez son comportement redéfini. Pour plus d’informations, consultez [procédures d’opérateur](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant définit le plan d’une structure qui contient les définitions pour la `IsFalse` et `IsTrue` opérateurs.  
  
 [!code-vb[VbVbalrOperators#28](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/isfalse-operator_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [IsTrue (opérateur)](../../../visual-basic/language-reference/operators/istrue-operator.md)  
 [Guide pratique : définir un opérateur](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)  
 [AndAlso (opérateur)](../../../visual-basic/language-reference/operators/andalso-operator.md)
