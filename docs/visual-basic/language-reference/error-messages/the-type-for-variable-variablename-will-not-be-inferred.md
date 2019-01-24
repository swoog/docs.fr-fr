---
title: Le type de variable &#39; &lt;variablename&gt; &#39; ne sera pas déduit, car il est lié à un champ dans une portée englobante
ms.date: 07/20/2015
f1_keywords:
- vbc42110
- bc42110
helpviewer_keywords:
- BC42110
ms.assetid: ef4442eb-08d1-434f-a03b-4aa2ed4e4414
ms.openlocfilehash: 6adcc1c2a449c9192e488a5d714e1c3271568be0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672381"
---
# <a name="the-type-for-variable-39ltvariablenamegt39-will-not-be-inferred-because-it-is-bound-to-a-field-in-an-enclosing-scope"></a>Le type de variable &#39; &lt;variablename&gt; &#39; ne sera pas déduit, car il est lié à un champ dans une portée englobante
Le type de variable '\<nom_variable >' ne sera pas déduit, car il est lié à un champ dans une portée englobante. Modifiez le nom de «\<nom_variable >', ou utilisez le nom qualifié complet (par exemple, 'Me.NomVariable' ou 'MyBase.NomVariable').  
  
 Une variable de contrôle de boucle dans votre code a le même nom en tant que champ de la classe ou d’autres portée englobante. Étant donné que la variable de contrôle est utilisée sans un `As` clause, elle est liée au champ dans la portée englobante, et le compilateur ne pas créer une variable pour lui ou déduire son type.  
  
 Dans l’exemple suivant, `Index`, la variable de contrôle dans le `For` instruction, est lié à la `Index` champ dans le `Customer` classe. Le compilateur ne crée pas de variable pour la variable de contrôle `Index` ou déduire son type.  
  
```  
Class Customer  
  
    ' The class has a field named Index.  
    Private Index As Integer  
  
    Sub Main()  
  
    ' The following line will raise this warning.  
        For Index = 1 To 10  
            ' ...  
        Next  
  
    End Sub  
End Class  
```  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC42110  
  
### <a name="to-address-this-warning"></a>Pour traiter cet avertissement  
  
-   Rendre la variable de contrôle de boucle locale en modifiant son nom à un identificateur qui n’est pas également le nom d’un champ de la classe.  
  
    ```  
    For I = 1 To 10  
    ```  
  
-   Préciser que la variable de contrôle de boucle est liée au champ de classe en ajoutant le préfixe `Me.` au nom de variable.  
  
    ```  
    For Me.Index = 1 To 10  
    ```  
  
-   Au lieu d’utiliser l’inférence de type local, utilisez un `As` clause pour spécifier un type pour la variable de contrôle de boucle.  
  
    ```  
    For Index As Integer = 1 To 10  
    ```  
  
## <a name="example"></a>Exemple  
 Le code suivant montre l’exemple précédent avec la première correction en place.  
  
```  
Class Customer  
  
    ' The class has a field named Index.  
    Private Index As Integer  
  
    Sub Main()  
  
        For I = 1 To 10  
            ' ...  
        Next  
  
    End Sub  
End Class  
```  
  
## <a name="see-also"></a>Voir aussi
- [Option Infer (instruction)](../../../visual-basic/language-reference/statements/option-infer-statement.md)
- [For Each...Next (instruction)](../../../visual-basic/language-reference/statements/for-each-next-statement.md)
- [For...Next (instruction)](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [Guide pratique pour Reportez-vous à l’Instance actuelle d’un objet](../../../visual-basic/programming-guide/language-features/variables/how-to-refer-to-the-current-instance-of-an-object.md)
- [Inférence de type local](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [Me, My, MyBase et MyClass](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
