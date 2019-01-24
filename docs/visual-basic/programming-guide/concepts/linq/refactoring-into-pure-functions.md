---
title: Refactorisation dans des fonctions pures (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 99e7d27b-a3ff-4577-bdb2-5a8278d6d7af
ms.openlocfilehash: 9c4be0c3574f2bd3171b8f5a86359d3181fe8731
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644461"
---
# <a name="refactoring-into-pure-functions-visual-basic"></a>Refactorisation dans des fonctions pures (Visual Basic)
L'un des aspects importants des transformations fonctionnelles pures consiste à apprendre à refactoriser le code à l'aide de fonctions pures.  
  
 Comme mentionné précédemment dans cette section, une fonction pure présente deux caractéristiques utiles :  
  
-   Elle n'a aucun effet secondaire. La fonction ne change aucune variable et aucune donnée de tout type en dehors de la fonction.  
  
-   Elle est cohérente. Étant donné le même ensemble de données d'entrée, elle retournera toujours la même valeur de sortie.  
  
 L'une des manières de basculer vers la programmation fonctionnelle consiste à refactoriser le code existant afin d'éliminer les effets secondaires indésirables et les dépendances externes. De cette manière, vous pouvez créer des versions avec fonctions pures du code existant.  
  
 Cette rubrique explique ce qu'est et ce que n'est pas une fonction pure. Le [didacticiel : Manipulation de contenu dans un WordprocessingML Document (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/tutorial-manipulating-content-in-a-wordprocessingml-document.md) didacticiel montre comment manipuler un document WordprocessingML et inclut deux exemples illustrant comment refactoriser à l’aide d’une fonction pure.  
  
## <a name="eliminating-side-effects-and-external-dependencies"></a>Suppression des effets secondaires et des dépendances externes  
 Les exemples suivants comparent deux fonctions non pures et une fonction pure.  
  
### <a name="non-pure-function-that-changes-a-class-member"></a>Fonction non pure qui modifie un membre de classe  
 Dans le code suivant, la fonction `HypenatedConcat` n'est pas pure car elle modifie le membre de données `aMember` dans la classe :  
  
```vb  
Module Module1  
    Dim aMember As String = "StringOne"  
  
    Public Sub HypenatedConcat(ByVal appendStr As String)  
        aMember = aMember & "-" & appendStr  
    End Sub  
  
    Sub Main()  
        HypenatedConcat("StringTwo")  
        Console.WriteLine(aMember)  
    End Sub  
End Module  
```  
  
 Ce code génère la sortie suivante :  
  
```  
StringOne-StringTwo  
```  
  
 Notez qu’il est sans intérêt si les données modifiées aient `public` ou `private` accéder, ou est un `shared` membre ou un membre d’instance. Une fonction pure ne change aucune donnée en dehors de la fonction.  
  
### <a name="non-pure-function-that-changes-an-argument"></a>Fonction non pure qui modifie un argument  
 En outre, la version suivante de cette même fonction n'est pas pure car elle modifie le contenu de son paramètre, `sb`.  
  
```vb  
Module Module1  
    Public Sub HypenatedConcat(ByVal sb As StringBuilder, ByVal appendStr As String)  
        sb.Append("-" & appendStr)  
    End Sub  
  
    Sub Main()  
        Dim sb1 As StringBuilder = New StringBuilder("StringOne")  
        HypenatedConcat(sb1, "StringTwo")  
        Console.WriteLine(sb1)  
    End Sub  
End Module  
```  
  
 Cette version du programme génère la même sortie que la première version, car la fonction `HypenatedConcat` a modifié la valeur (l'état) de son premier paramètre en appelant la fonction membre <xref:System.Text.StringBuilder.Append%2A>. Notez que cette altération a lieu en dépit du fait que `HypenatedConcat` utilise le passage de paramètre avec appel par valeur.  
  
> [!IMPORTANT]
>  Pour les types de référence, si vous passez un paramètre par valeur, une copie de la référence à un objet est passée. Cette copie est toujours associée aux mêmes données d'instance que la référence d'origine (jusqu'à ce que la variable de référence soit assignée à un nouvel objet). L'appel par référence n'est pas forcément nécessaire pour qu'une fonction modifie un paramètre.  
  
### <a name="pure-function"></a>Fonction pure  
 Cette autre version du programme montre comment implémenter la fonction `HypenatedConcat` en tant que fonction pure.  
  
```vb  
Module Module1  
    Public Function HyphenatedConcat(ByVal s As String, ByVal appendStr As String) As String  
        Return (s & "-" & appendStr)  
    End Function  
  
    Sub Main()  
        Dim s1 As String = "StringOne"  
        Dim s2 As String = HyphenatedConcat(s1, "StringTwo")  
        Console.WriteLine(s2)  
    End Sub  
End Module  
```  
  
 Là encore, cette version génère la même ligne de sortie : `StringOne-StringTwo`. Notez que pour conserver la valeur concaténée, elle est stockée dans la variable intermédiaire `s2`.  
  
 L'une des approches qui peuvent se révéler très utiles consiste à écrire des fonctions localement impures (à savoir, qui déclarent et modifient des variables locales) mais globalement pures. Ces fonctions possèdent une grande partie des caractéristiques de composabilité requises, mais elles évitent certaines des tâches de programmation fonctionnelle plus compliquées, telles que l'utilisation de la récursivité lorsqu'une simple boucle génèrerait le même résultat.  
  
## <a name="standard-query-operators"></a>Opérateurs de requête standard  
 L'une des caractéristiques importantes des opérateurs de requête standard est qu'ils sont implémentés en tant que fonctions pures.  
  
 Pour plus d’informations, consultez [présentation des opérateurs de requête Standard (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md).  
  
## <a name="see-also"></a>Voir aussi
- [Introduction aux Transformations fonctionnelles pures (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/introduction-to-pure-functional-transformations.md)
- [Comparaison de la programmation fonctionnelle et de la Programmation impérative (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/functional-programming-vs-imperative-programming.md)
