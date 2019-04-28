---
title: 'Procédure : Appeler une méthode d’Extension (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- calling extension methods [Visual Basic]
- extension methods [Visual Basic]
ms.assetid: df07750f-40f4-4c07-a79e-1113a27cfbea
ms.openlocfilehash: 5cb0684637a716dfec947740ba345c62eaabddd7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61863673"
---
# <a name="how-to-call-an-extension-method-visual-basic"></a>Procédure : Appeler une méthode d’Extension (Visual Basic)
Méthodes d’extension permettent d’ajouter des méthodes à une classe existante. Une fois une méthode d’extension est déclarée et mises dans la portée, vous pouvez l’appeler comme une méthode d’instance du type qu’il étend. Pour plus d’informations sur la façon d’écrire une méthode d’extension, consultez [Comment : Écrire une méthode d’Extension](./how-to-write-an-extension-method.md).  
  
 Les instructions suivantes font référence à la méthode d’extension `PrintAndPunctuate`, qui affiche l’instance de chaîne qui l’appelle, suivie de n’importe quelle valeur envoyée pour le deuxième paramètre, `punc`.  
  
```vb  
Imports System.Runtime.CompilerServices  
  
Module StringExtensions  
    <Extension()>   
    Public Sub PrintAndPunctuate(ByVal aString As String,   
                                 ByVal punc As String)  
        Console.WriteLine(aString & punc)  
    End Sub  
  
End Module  
```  
  
 La méthode doit être dans la portée lorsqu’elle est appelée.  
  
### <a name="to-call-an-extension-method"></a>Pour appeler une méthode d’extension  
  
1. Déclarez une variable qui a le type de données du premier paramètre de la méthode d’extension. Pour `PrintAndPunctuate`, vous devez un <xref:System.String> variable :  
  
    ```  
    Dim example = "Ready"  
    ```  
  
2. Que la variable appellera la méthode d’extension, et sa valeur est liée au premier paramètre, `aString`. L’instruction d’appel suivante affichera `Ready?`.  
  
    ```  
    example.PrintAndPunctuate("?")  
    ```  
  
     Notez que l’appel à cette méthode d’extension ressemble à un appel à l’un de le <xref:System.String> les méthodes qui nécessitent un paramètre d’instance :  
  
    ```  
    example.EndsWith("dy")  
    example.IndexOf("R")  
    ```  
  
3. Déclarer une autre variable de chaîne et appelez la méthode pour vérifier qu’elle fonctionne avec n’importe quelle chaîne.  
  
    ```  
    Dim example2 = " or not"  
    example2.PrintAndPunctuate("!!!")  
    ```  
  
     Cette fois-ci il en résulte : `or not!!!`.  
  
## <a name="example"></a>Exemple  
 Le code suivant est un exemple complet de la création et utilisation d’une méthode d’extension simple.  
  
```vb  
Imports System.Runtime.CompilerServices  
Imports ConsoleApplication1.StringExtensions  
  
Module Module1  
  
    Sub Main()  
  
        Dim example = "Hello"  
        example.PrintAndPunctuate(".")  
        example.PrintAndPunctuate("!!!!")  
  
        Dim example2 = "Goodbye"  
        example2.PrintAndPunctuate("?")  
    End Sub  
  
    <Extension()>   
    Public Sub PrintAndPunctuate(ByVal aString As String,   
                                 ByVal punc As String)  
        Console.WriteLine(aString & punc)  
    End Sub  
End Module  
  
' Output:  
' Hello.  
' Hello!!!!  
' Goodbye?  
```  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Écrire une méthode d’Extension](./how-to-write-an-extension-method.md)
- [Méthodes d’extension](./extension-methods.md)
- [Portée dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
