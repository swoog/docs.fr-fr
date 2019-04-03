---
title: 'Procédure : Masquer une Variable portant le même nom que votre Variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- qualification [Visual Basic], of element names
- declarations [Visual Basic], elements
- element names [Visual Basic], qualification
- references [Visual Basic], declared elements
- declaration statements [Visual Basic], declared elements
- declaring elements [Visual Basic]
- referencing declared elements [Visual Basic]
- declared elements [Visual Basic], referencing
- declared elements [Visual Basic], about declared elements
ms.assetid: e39c0752-f19f-4d2e-a453-00df1b5fc7ee
ms.openlocfilehash: a8a7eda2a636d7f89131d140c82ad4f3c4743211
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58826676"
---
# <a name="how-to-hide-a-variable-with-the-same-name-as-your-variable-visual-basic"></a>Procédure : Masquer une Variable portant le même nom que votre Variable (Visual Basic)
Vous pouvez masquer une variable par *occultation* il, autrement dit, en le redéfinissant avec une variable du même nom. Vous pouvez occulter la variable que vous souhaitez masquer de deux manières :  
  
-   **Occultation par portée.** Vous pouvez occulter via étendue en redéclarant dans une sous-région de la région contenant la variable que vous souhaitez masquer.  
  
-   **Occultation par héritage.** Si la variable que vous souhaitez masquer est définie au niveau de classe, vous pouvez le masquer via l’héritage en redéclarant avec le [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md) mot clé dans une classe dérivée.  
  
## <a name="two-ways-to-hide-a-variable"></a>Deux méthodes pour masquer une Variable  
  
#### <a name="to-hide-a-variable-by-shadowing-it-through-scope"></a>Pour masquer une variable par elle occultation par portée  
  
1.  Déterminer la région de définition de la variable que vous souhaitez masquer et déterminez une sous-région dans laquelle la redéfinir avec votre variable.  
  
    |Région de variable|Sous-région autorisée pour la redéfinir|  
    |-----------------------|-------------------------------------------|  
    |Module|Une classe dans le module|  
    |Classe|Une sous-classe de la classe<br /><br /> Une procédure au sein de la classe|  
  
     Vous ne pouvez pas redéfinir une variable de procédure dans un bloc au sein de cette procédure, par exemple dans un `If`... `End If` construction ou une `For` boucle.  
  
2.  Créez la sous-région si elle n’existe pas déjà.  
  
3.  Dans la sous-région, écrivez un [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) déclare la variable occultante.  
  
     En cas de code à l’intérieur de la sous-région fait référence au nom de variable, le compilateur résout la référence à la variable occultante.  
  
     L’exemple suivant illustre l’occultation par portée, ainsi qu’une référence qui outrepasse l’occultation.  
  
    ```  
    Module shadowByScope  
        ' The following statement declares num as a module-level variable.  
        Public num As Integer  
        Sub show()  
            ' The following statement declares num as a local variable.  
            Dim num As Integer  
            ' The following statement sets the value of the local variable.  
            num = 2  
            ' The following statement displays the module-level variable.  
            MsgBox(CStr(shadowByScope.num))  
        End Sub  
        Sub useModuleLevelNum()  
            ' The following statement sets the value of the module-level variable.  
            num = 1  
            show()  
        End Sub  
    End Module  
    ```  
  
     L’exemple précédent déclare la variable `num` à la fois au niveau du module et au niveau de la procédure (dans la procédure `show`). La variable locale `num` occulte la variable de niveau module `num` dans `show`, de sorte que la variable locale est définie sur 2. Toutefois, il n’existe aucune variable locale pour les clichés instantanés `num` dans le `useModuleLevelNum` procédure. Par conséquent, `useModuleLevelNum` définit la valeur de la variable au niveau du module à 1.  
  
     Le `MsgBox` appeler `show` ignore le mécanisme d’occultation en qualifiant `num` avec le nom du module. Par conséquent, il affiche la variable au niveau du module au lieu de la variable locale.  
  
#### <a name="to-hide-a-variable-by-shadowing-it-through-inheritance"></a>Pour masquer une variable par l’occultation par héritage  
  
1.  Assurez-vous que la variable que vous souhaitez masquer est déclarée dans une classe et au niveau de la classe (en dehors de toute procédure). Sinon, vous ne peut pas la masquer par héritage.  
  
2.  Définissez une classe dérivée à partir de la classe de la variable si celle-ci n’existe pas.  
  
3.  À l’intérieur de la classe dérivée, écrivez une `Dim` instruction déclare votre variable. Inclure le [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md) mot clé dans la déclaration.  
  
     En cas de code dans la classe dérivée fait référence au nom de variable, le compilateur résout la référence à votre variable.  
  
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
 L’occultation introduit plusieurs versions d’une variable portant le même nom. Lorsqu’une instruction de code fait référence au nom de variable, la version à laquelle le compilateur résout la référence dépend de facteurs tels que l’emplacement de l’instruction de code et la présence d’une chaîne qualifiante. Cela peut augmenter le risque de faire référence à une version non souhaitée d’une variable occultée. Vous pouvez réduire ce risque en qualifiant complètement toutes les références à une variable occultée.  
  
## <a name="see-also"></a>Voir aussi

- [Références aux éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Occultation dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
- [Différences entre l'occultation et la substitution](../../../../visual-basic/programming-guide/language-features/declared-elements/differences-between-shadowing-and-overriding.md)
- [Guide pratique pour Masquer une Variable héritée](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-an-inherited-variable.md)
- [Guide pratique pour Accéder à une Variable masquée par une classe dérivée](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-access-a-variable-hidden-by-a-derived-class.md)
- [Overrides](../../../../visual-basic/language-reference/modifiers/overrides.md)
- [Me, My, MyBase et MyClass](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [Éléments fondamentaux de l’héritage](../../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
