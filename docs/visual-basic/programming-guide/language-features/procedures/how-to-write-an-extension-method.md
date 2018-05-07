---
title: 'Comment : écrire une méthode d’extension (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- extending data types [Visual Basic]
- writing extension methods [Visual Basic]
- extension methods [Visual Basic]
ms.assetid: fb2739cc-958d-4ef4-a38b-214a74c93413
ms.openlocfilehash: e220a025c39757b492be033caeb8924523515804
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-write-an-extension-method-visual-basic"></a>Comment : écrire une méthode d’extension (Visual Basic)
Méthodes d’extension permettent d’ajouter des méthodes à une classe existante. La méthode d’extension peut être appelée comme s’il s’agissait d’une instance de cette classe.  
  
### <a name="to-define-an-extension-method"></a>Pour définir une méthode d’extension  
  
1.  Dans Visual Studio, ouvrez une application Visual Basic nouvelle ou existante.  
  
2.  En haut du fichier dans lequel vous souhaitez définir une méthode d’extension, incluez l’instruction import suivante :  
  
    ```  
    Imports System.Runtime.CompilerServices  
    ```  
  
3.  Dans un module de votre application nouvelle ou existante, commencez la définition de méthode avec l’attribut d’extension :  
  
    ```  
    <Extension()>  
    ```  
  
4.  Déclarez votre méthode de la façon habituelle, à ceci près que le type du premier paramètre doit être le type de données que vous souhaitez étendre.  
  
    ```  
    <Extension()>   
    Public Sub subName (ByVal para1 As ExtendedType, <other parameters>)  
         ' < Body of the method >  
    End Sub  
    ```  
  
## <a name="example"></a>Exemple  
 L’exemple suivant déclare une méthode d’extension dans le module `StringExtensions`. Un deuxième module `Module1`, importe `StringExtensions` et appelle la méthode. La méthode d’extension doit être dans la portée lorsqu’elle est appelée. Méthode d’extension `PrintAndPunctuate` étend la <xref:System.String> classe avec une méthode qui affiche l’instance de chaîne suivie d’une chaîne de symboles de ponctuation envoyée en tant que paramètre.  
  
```vb  
' Declarations will typically be in a separate module.  
Imports System.Runtime.CompilerServices  
  
Module StringExtensions  
    <Extension()>   
    Public Sub PrintAndPunctuate(ByVal aString As String,   
                                 ByVal punc As String)  
        Console.WriteLine(aString & punc)  
    End Sub  
  
End Module  
```  
  
```vb  
' Import the module that holds the extension method you want to use,   
' and call it.  
  
Imports ConsoleApplication2.StringExtensions  
  
Module Module1  
  
    Sub Main()  
        Dim example = "Hello"  
        example.PrintAndPunctuate("?")  
        example.PrintAndPunctuate("!!!!")  
    End Sub  
  
End Module  
```  
  
 Notez que la méthode est définie avec deux paramètres et est appelée avec une seule. Le premier paramètre, `aString`, de la méthode de définition est liée à `example`, l’instance de `String` qui appelle la méthode. La sortie de l’exemple est la suivante :  
  
 `Hello?`  
  
 `Hello!!!!`  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Runtime.CompilerServices.ExtensionAttribute>  
 [Méthodes d’extension](./extension-methods.md)  
 [Module (instruction)](../../../../visual-basic/language-reference/statements/module-statement.md)  
 [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)  
 [Portée dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
