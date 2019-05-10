---
title: 'Procédure : Accéder à une Variable masquée par une classe dérivée (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- qualification [Visual Basic], of element names
- base classes [Visual Basic], accessing elements
- element names [Visual Basic], qualification
- references [Visual Basic], declared elements
- declared elements [Visual Basic], referencing
- variables [Visual Basic], accessing hidden
ms.assetid: ae21a8ac-9cd4-4fba-a3ec-ecc4321ef93c
ms.openlocfilehash: 43f7af1a1b540dd630cc2f228f1e5a6018d7c5d7
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64610458"
---
# <a name="how-to-access-a-variable-hidden-by-a-derived-class-visual-basic"></a>Procédure : Accéder à une Variable masquée par une classe dérivée (Visual Basic)
Lorsque le code dans une classe dérivée accède à une variable, le compilateur résout normalement la référence vers la version accessible le plus proche, autrement dit, la version accessible le moins qui d’étapes vers l’arrière de la classe. Si la variable est définie dans la classe dérivée, le code accède normalement à cette définition.  
  
 Si la variable de classe dérivée masque une variable dans la classe de base, elle masque la version de la classe de base. Toutefois, vous pouvez accéder à la variable de classe de base en qualifiant avec le `MyBase` mot clé.  
  
### <a name="to-access-a-base-class-variable-hidden-by-a-derived-class"></a>Pour accéder à une variable de classe de base masquée par une classe dérivée  
  
- Dans une expression ou une instruction d’assignation, faites précéder le nom de variable avec le `MyBase` mot clé et une période (`.`).  
  
     Le compilateur résout la référence à la version de la classe de base de la variable.  
  
     L’exemple suivant illustre l’occultation par héritage. Il effectue deux références, qui accède à la variable occultation et une qui outrepasse l’occultation.  
  
    ```  
    Public Class shadowBaseClass  
        Public shadowString As String = "This is the base class string."  
    End Class  
    Public Class shadowDerivedClass  
        Inherits shadowBaseClass  
        Public Shadows shadowString As String = "This is the derived class string."  
        Public Sub showStrings()  
            Dim s As String = "Unqualified shadowString: " & shadowString &  
                vbCrLf & "MyBase.shadowString: " & MyBase.shadowString  
            MsgBox(s)  
        End Sub  
    End Class  
    ```  
  
     L’exemple précédent déclare la variable `shadowString` dans la classe de base et la masque dans la classe dérivée. La procédure `showStrings` dans la classe dérivée, affiche la version de masquage de la chaîne lorsque le nom `shadowString` n’est pas qualifié. Il affiche ensuite la version ombrée lorsque `shadowString` est qualifié avec le `MyBase` mot clé.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Pour réduire le risque de faire référence à une version non souhaitée d’une variable occultée, vous pouvez qualifier complètement toutes les références à une variable occultée. L’occultation introduit plusieurs versions d’une variable portant le même nom. Lorsqu’une instruction de code fait référence au nom de variable, la version à laquelle le compilateur résout la référence dépend de facteurs tels que l’emplacement de l’instruction de code et la présence d’une chaîne qualifiante. Cela peut augmenter le risque de faire référence à une version incorrecte de la variable.  
  
## <a name="see-also"></a>Voir aussi

- [Références aux éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Occultation dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
- [Différences entre l'occultation et la substitution](../../../../visual-basic/programming-guide/language-features/declared-elements/differences-between-shadowing-and-overriding.md)
- [Guide pratique pour Masquer une Variable portant le même nom que votre Variable](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-a-variable-with-the-same-name-as-your-variable.md)
- [Guide pratique pour Masquer une Variable héritée](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-an-inherited-variable.md)
- [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md)
- [Overrides](../../../../visual-basic/language-reference/modifiers/overrides.md)
- [Me, My, MyBase et MyClass](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [Éléments fondamentaux de l’héritage](../../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
