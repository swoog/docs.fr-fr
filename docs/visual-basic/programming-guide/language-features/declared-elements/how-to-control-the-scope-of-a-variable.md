---
title: 'Procédure : Contrôler la portée d’une Variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], scope
- declared elements [Visual Basic], scope
- visibility [Visual Basic], declared elements
- variables [Visual Basic], visibility
- scope [Visual Basic], declared elements
- scope [Visual Basic], variables
- scope [Visual Basic], Visual Basic
- declared elements [Visual Basic], visibility
- visibility [Visual Basic], variables
ms.assetid: 44b7f62a-cb5c-4d50-bce9-60ae68f87072
ms.openlocfilehash: 656bfa6fa9b3445d91cd8ac39b83bccf3e44758e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521411"
---
# <a name="how-to-control-the-scope-of-a-variable-visual-basic"></a>Procédure : Contrôler la portée d’une Variable (Visual Basic)
Normalement, une variable est dans *étendue*, ou est visible par référence, tout au long de la région dans laquelle vous la déclarez. Dans de certains cas, la variable *niveau d’accès* peut influencer sa portée.  
  
 Pour plus d'informations, consultez [Scope in Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md).  
  
## <a name="scope-at-block-or-procedure-level"></a>Portée au niveau de la procédure ou de bloc  
  
#### <a name="to-make-a-variable-visible-only-within-a-block"></a>Pour rendre une variable visible uniquement dans un bloc  
  
-   Place le [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) pour la variable entre le début et de fin des instructions de déclaration de ce bloc, par exemple entre les `For` et `Next` instructions d’un `For` boucle.  
  
     Vous pouvez faire référence à la variable uniquement à partir du bloc.  
  
#### <a name="to-make-a-variable-visible-only-within-a-procedure"></a>Pour rendre une variable visible uniquement dans une procédure  
  
-   Place le `Dim` instruction pour la variable à l’intérieur de la procédure mais en dehors de tout bloc (comme un `With`... `End With` bloc).  
  
     Vous pouvez faire référence à la variable uniquement à partir de la procédure, y compris à l’intérieur de n’importe quel bloc contenue dans la procédure.  
  
## <a name="scope-at-module-or-namespace-level"></a>Portée au niveau du Module ou Namespace  
 Pour plus de commodité, le terme unique *au niveau du module* s’appliquent également aux modules, les classes et structures. Le niveau d’accès d’une variable de niveau module détermine sa portée. L’espace de noms qui contient le module, une classe ou une structure influence également la portée.  
  
#### <a name="to-make-a-variable-visible-throughout-a-module-class-or-structure"></a>Pour rendre une variable visible dans l’ensemble d’un module, une classe ou une structure  
  
1.  Place le `Dim` instruction pour la variable à l’intérieur du module, une classe ou une structure, mais en dehors de toute procédure.  
  
2.  Inclure le [privé](../../../../visual-basic/language-reference/modifiers/private.md) mot clé dans la `Dim` instruction.  
  
3.  Vous pouvez faire référence à la variable à partir de n’importe où dans le module, une classe ou une structure, mais pas d’à l’extérieur.  
  
#### <a name="to-make-a-variable-visible-throughout-a-namespace"></a>Pour rendre une variable visible dans l’ensemble d’un espace de noms  
  
1.  Place le `Dim` instruction pour la variable à l’intérieur du module, une classe ou une structure, mais en dehors de toute procédure.  
  
2.  Inclure le [Friend](../../../../visual-basic/language-reference/modifiers/friend.md) ou [Public](../../../../visual-basic/language-reference/modifiers/public.md) mot clé dans la `Dim` instruction.  
  
3.  Vous pouvez faire référence à la variable à partir de n’importe où dans l’espace de noms contenant le module, une classe ou une structure.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant déclare une variable au niveau du module et limite sa visibilité au code dans le module.  
  
```  
Module demonstrateScope  
    Private strMsg As String  
    Sub initializePrivateVariable()  
        strMsg = "This variable cannot be used outside this module."  
    End Sub  
    Sub usePrivateVariable()  
        MsgBox(strMsg)  
    End Sub  
End Module  
```  
  
 Dans l’exemple précédent, toutes les procédures définies dans le module `demonstrateScope` peuvent faire référence à la `String` variable `strMsg`. Lorsque le `usePrivateVariable` procédure est appelée, elle affiche le contenu de la variable chaîne `strMsg` dans une boîte de dialogue.  
  
 Avec la modification suivante apportée à l’exemple précédent, la variable de chaîne `strMsg` peuvent être référencés par le code n’importe où dans l’espace de noms de sa déclaration.  
  
```  
Public strMsg As String  
```  
  
## <a name="robust-programming"></a>Programmation fiable  
 La portée est limitée d’une variable, les opportunités de moins que vous disposez pour accidentellement qui fait référence à la place d’une autre variable portant le même nom. Vous pouvez également réduire les problèmes de correspondance de référence.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 La portée est limitée d’une variable, plus le risque qu’un code malveillant peut rendre incorrect l’utiliser.  
  
## <a name="see-also"></a>Voir aussi
- [Portée dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
- [Durée de vie en Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)
- [Niveaux d’accès dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [Variables](../../../../visual-basic/programming-guide/language-features/variables/index.md)
- [Déclaration de variable](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [Dim (instruction)](../../../../visual-basic/language-reference/statements/dim-statement.md)
