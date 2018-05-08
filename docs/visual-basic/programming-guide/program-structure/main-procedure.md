---
title: Procédure Main dans Visual Basic
ms.date: 07/20/2015
f1_keywords:
- vb.Main
helpviewer_keywords:
- Main procedure
- Main method [Visual Basic]
- main function
ms.assetid: f0db283e-f283-4464-b521-b90858cc1b44
ms.openlocfilehash: 109bf94eb91292cfca700a9e456c8ab53e83d68f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="main-procedure-in-visual-basic"></a>Procédure Main dans Visual Basic
Toutes les applications Visual Basic doivent contenir une procédure appelée `Main`. Cette procédure sert de point de départ et contrôle général pour votre application. Le .NET Framework appelle votre `Main` procédure lorsqu’il a chargé votre application et est prêt à passer le contrôle. Sauf si vous créez une application Windows Forms, vous devez écrire le `Main` procédure pour les applications qui s’exécutent sur leurs propres.  
  
 `Main` contient le code qui s’exécute en premier. Dans `Main`, vous pouvez déterminer quel formulaire doit d’abord être chargé au démarrage du programme, savoir si une copie de votre application est déjà en cours d’exécution sur le système, définir un ensemble de variables pour votre application ou ouvrir une base de données requise par l’application.  
  
## <a name="requirements-for-the-main-procedure"></a>Configuration requise pour la procédure principale  
 Un fichier qui s’exécute sur sa propre (généralement avec l’extension .exe) doit contenir un `Main` procédure. Une bibliothèque (par exemple avec l’extension .dll) ne s’exécute pas son propre et ne requiert pas un `Main` procédure. La configuration requise pour les différents types de projets que vous pouvez créer est les suivantes :  
  
-   Applications console s’exécutent leurs propres, et vous devez fournir au moins un `Main` procédure. .  
  
-   Applications Windows Forms s’exécutent sur leurs propres. Toutefois, le compilateur Visual Basic génère automatiquement un `Main` procédure telle une application et que vous n’avez pas besoin d’écrire un.  
  
-   Bibliothèques de classes ne nécessitent pas une `Main` procédure. Il s’agit notamment des bibliothèques de contrôles Windows et les bibliothèques de contrôles Web. Les applications Web sont déployées en tant que bibliothèques de classes.  
  
## <a name="declaring-the-main-procedure"></a>Déclaration de la procédure principale  
 Il existe quatre méthodes pour déclarer le `Main` procédure. Il peut accepter des arguments ou non, et elle peut retourner une valeur ou non.  
  
> [!NOTE]
>  Si vous déclarez `Main` dans une classe, vous devez utiliser le `Shared` (mot clé). Dans un module, `Main` n’est pas nécessaire de `Shared`.  
  
-   La façon la plus simple consiste à déclarer un `Sub` procédure qui n’a pas été acceptent des arguments ou une valeur de retour.  
  
    ```  
    Module mainModule  
        Sub Main()  
            MsgBox("The Main procedure is starting the application.")  
            ' Insert call to appropriate starting place in your code.  
            MsgBox("The application is terminating.")  
        End Sub  
    End Module  
    ```  
  
-   `Main` peut également retourner un `Integer` valeur, que le système d’exploitation utilise comme code de sortie de votre programme. Autres programmes peuvent tester ce code en examinant la valeur ERRORLEVEL Windows. Pour retourner un code de sortie, vous devez déclarer `Main` comme un `Function` procédure au lieu d’un `Sub` procédure.  
  
    ```  
    Module mainModule  
        Function Main() As Integer  
            MsgBox("The Main procedure is starting the application.")  
            Dim returnValue As Integer = 0  
            ' Insert call to appropriate starting place in your code.  
            ' On return, assign appropriate value to returnValue.  
            ' 0 usually means successful completion.  
            MsgBox("The application is terminating with error level " &  
                 CStr(returnValue) & ".")  
            Return returnValue  
        End Function  
    End Module  
    ```  
  
-   `Main` peut également prendre une `String` tableau en tant qu’argument. Chaque chaîne dans le tableau contient un des arguments de ligne de commande utilisés pour appeler votre programme. Vous pouvez effectuer des actions différentes en fonction de leurs valeurs.  
  
    ```  
    Module mainModule  
        Function Main(ByVal cmdArgs() As String) As Integer  
            MsgBox("The Main procedure is starting the application.")  
            Dim returnValue As Integer = 0  
            ' See if there are any arguments.  
            If cmdArgs.Length > 0 Then  
                For argNum As Integer = 0 To UBound(cmdArgs, 1)  
                    ' Insert code to examine cmdArgs(argNum) and take  
                    ' appropriate action based on its value.  
                Next argNum  
            End If  
            ' Insert call to appropriate starting place in your code.  
            ' On return, assign appropriate value to returnValue.  
            ' 0 usually means successful completion.  
            MsgBox("The application is terminating with error level " &  
                 CStr(returnValue) & ".")  
            Return returnValue  
        End Function  
    End Module  
    ```  
  
-   Vous pouvez déclarer `Main` à examiner les arguments de ligne de commande, mais pas retourner un code de sortie, comme suit.  
  
    ```  
    Module mainModule  
        Sub Main(ByVal cmdArgs() As String)  
            MsgBox("The Main procedure is starting the application.")  
            Dim returnValue As Integer = 0  
            ' See if there are any arguments.  
            If cmdArgs.Length > 0 Then  
                For argNum As Integer = 0 To UBound(cmdArgs, 1)  
                    ' Insert code to examine cmdArgs(argNum) and take  
                    ' appropriate action based on its value.  
                Next argNum  
            End If  
            ' Insert call to appropriate starting place in your code.  
            MsgBox("The application is terminating.")  
        End Sub  
    End Module  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A>  
 <xref:System.Array.Length%2A>  
 <xref:Microsoft.VisualBasic.Information.UBound%2A>  
 [Structure d’un programme Visual Basic](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)  
 [/main](../../../visual-basic/reference/command-line-compiler/main.md)  
 [Shared](../../../visual-basic/language-reference/modifiers/shared.md)  
 [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)  
 [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)  
 [Integer (type de données)](../../../visual-basic/language-reference/data-types/integer-data-type.md)  
 [String (type de données)](../../../visual-basic/language-reference/data-types/string-data-type.md)
