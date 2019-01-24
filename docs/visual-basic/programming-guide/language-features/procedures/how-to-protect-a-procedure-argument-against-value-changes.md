---
title: 'Procédure : Protéger un Argument de procédure contre les modifications de valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], parameters
- procedure arguments
- arguments [Visual Basic], passing by reference
- Visual Basic code, procedures
- arguments [Visual Basic], ByVal
- arguments [Visual Basic], passing by value
- procedure parameters
- procedures [Visual Basic], calling
- arguments [Visual Basic], ByRef
- arguments [Visual Basic], changing value
ms.assetid: d2b7c766-ce16-4d2c-8d79-3fc0e7ba2227
ms.openlocfilehash: 42015e2a024ece75a920deb414d326c88f31249e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528886"
---
# <a name="how-to-protect-a-procedure-argument-against-value-changes-visual-basic"></a>Procédure : Protéger un Argument de procédure contre les modifications de valeur (Visual Basic)
Si une procédure déclare un paramètre comme [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md), Visual Basic fournit le code de procédure une référence directe à l’élément de programmation sous-jacent à l’argument dans le code appelant. Cela permet à la procédure pour modifier la valeur sous-jacente de l’argument dans le code appelant. Dans certains cas, le code appelant souhaiterez pour vous protéger contre une telle modification.  
  
 Vous pouvez toujours protéger un argument de modification en déclarant le paramètre correspondant [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) dans la procédure. Si vous souhaitez être en mesure de modifier un argument donné dans certains cas, mais pas pour d’autres, vous pouvez le déclarer `ByRef` et laisser le code appelant à déterminer le mécanisme de passage dans chaque appel. Pour ce faire entre parenthèses l’argument correspondant à passer par valeur ou mettant ne pas entre parenthèses à passer par référence. Pour plus d'informations, voir [Procédure : Forcer un Argument d’être passés par valeur](./how-to-force-an-argument-to-be-passed-by-value.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre deux procédures qui acceptent une variable tableau et opèrent sur ses éléments. Le `increase` procédure ajoute simplement 1 à chaque élément. Le `replace` procédure assigne un nouveau tableau au paramètre `a()` , puis ajoute 1 à chaque élément. Toutefois, la réaffectation n’affecte pas la variable tableau sous-jacente dans le code appelant.  
  
 [!code-vb[VbVbcnProcedures#35](./codesnippet/VisualBasic/how-to-protect-a-procedure-argument-against-value-changes_1.vb)]  
  
 [!code-vb[VbVbcnProcedures#38](./codesnippet/VisualBasic/how-to-protect-a-procedure-argument-against-value-changes_2.vb)]  
  
 [!code-vb[VbVbcnProcedures#37](./codesnippet/VisualBasic/how-to-protect-a-procedure-argument-against-value-changes_3.vb)]  
  
 Le premier `MsgBox` appel affiche « après Increase (n) : 11, 21, 31, 41". Étant donné que le tableau `n` est un type référence, `increase` peut modifier ses membres, même si le mécanisme de passage est `ByVal`.  
  
 La seconde `MsgBox` appel affiche « après Replace (n) : 11, 21, 31, 41". Étant donné que `n` est passée `ByVal`, `replace` ne peut pas modifier la variable `n` dans le code appelant en lui assignant un nouveau tableau. Lorsque `replace` crée la nouvelle instance de tableau `k` et l’assigne à la variable locale `a`, il perd la référence à `n` transmis par le code appelant. Lorsqu’il modifie les membres de `a`, seul le tableau local `k` est affecté. Par conséquent, `replace` n’incrémente pas les valeurs du tableau `n` dans le code appelant.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 La valeur par défaut en Visual Basic consiste à passer des arguments par valeur. Toutefois, il est conseillé en programmation pour inclure le [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) ou [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md) keyword avec chaque paramètre déclaré. Cela rend votre code plus facile à lire.  
  
## <a name="see-also"></a>Voir aussi
- [Procédures](./index.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Guide pratique pour Passer des Arguments à une procédure](./how-to-pass-arguments-to-a-procedure.md)
- [Passage d’un argument par valeur et par référence](./passing-arguments-by-value-and-by-reference.md)
- [Différences entre les arguments modifiables et non modifiables](./differences-between-modifiable-and-nonmodifiable-arguments.md)
- [Différences entre le passage d’un argument par valeur et par référence](./differences-between-passing-an-argument-by-value-and-by-reference.md)
- [Guide pratique pour Modifier la valeur d’un Argument de procédure](./how-to-change-the-value-of-a-procedure-argument.md)
- [Guide pratique pour Forcer un Argument d’être passés par valeur](./how-to-force-an-argument-to-be-passed-by-value.md)
- [Passage des arguments par position et par nom](./passing-arguments-by-position-and-by-name.md)
- [Value Types and Reference Types](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
