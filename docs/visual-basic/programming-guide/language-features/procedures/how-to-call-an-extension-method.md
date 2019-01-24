---
title: 'Procédure : Appeler une méthode d’Extension (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- calling extension methods [Visual Basic]
- extension methods [Visual Basic]
ms.assetid: df07750f-40f4-4c07-a79e-1113a27cfbea
ms.openlocfilehash: 4e9391a4c4a159cd5e198689bf7af7cd64c3a872
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54620446"
---
# <a name="how-to-call-an-extension-method-visual-basic"></a><span data-ttu-id="48270-102">Procédure : Appeler une méthode d’Extension (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="48270-102">How to: Call an Extension Method (Visual Basic)</span></span>
<span data-ttu-id="48270-103">Méthodes d’extension permettent d’ajouter des méthodes à une classe existante.</span><span class="sxs-lookup"><span data-stu-id="48270-103">Extension methods enable you to add methods to an existing class.</span></span> <span data-ttu-id="48270-104">Une fois une méthode d’extension est déclarée et mises dans la portée, vous pouvez l’appeler comme une méthode d’instance du type qu’il étend.</span><span class="sxs-lookup"><span data-stu-id="48270-104">After an extension method is declared and brought into scope, you can call it like an instance method of the type that it extends.</span></span> <span data-ttu-id="48270-105">Pour plus d’informations sur la façon d’écrire une méthode d’extension, consultez [Comment : Écrire une méthode d’Extension](./how-to-write-an-extension-method.md).</span><span class="sxs-lookup"><span data-stu-id="48270-105">For more information about how to write an extension method, see [How to: Write an Extension Method](./how-to-write-an-extension-method.md).</span></span>  
  
 <span data-ttu-id="48270-106">Les instructions suivantes font référence à la méthode d’extension `PrintAndPunctuate`, qui affiche l’instance de chaîne qui l’appelle, suivie de n’importe quelle valeur envoyée pour le deuxième paramètre, `punc`.</span><span class="sxs-lookup"><span data-stu-id="48270-106">The following instructions refer to extension method `PrintAndPunctuate`, which will display the string instance that invokes it, followed by whatever value is sent in for the second parameter, `punc`.</span></span>  
  
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
  
 <span data-ttu-id="48270-107">La méthode doit être dans la portée lorsqu’elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="48270-107">The method must be in scope when it is called.</span></span>  
  
### <a name="to-call-an-extension-method"></a><span data-ttu-id="48270-108">Pour appeler une méthode d’extension</span><span class="sxs-lookup"><span data-stu-id="48270-108">To call an extension method</span></span>  
  
1.  <span data-ttu-id="48270-109">Déclarez une variable qui a le type de données du premier paramètre de la méthode d’extension.</span><span class="sxs-lookup"><span data-stu-id="48270-109">Declare a variable that has the data type of the first parameter of the extension method.</span></span> <span data-ttu-id="48270-110">Pour `PrintAndPunctuate`, vous devez un <xref:System.String> variable :</span><span class="sxs-lookup"><span data-stu-id="48270-110">For `PrintAndPunctuate`, you need a <xref:System.String> variable:</span></span>  
  
    ```  
    Dim example = "Ready"  
    ```  
  
2.  <span data-ttu-id="48270-111">Que la variable appellera la méthode d’extension, et sa valeur est liée au premier paramètre, `aString`.</span><span class="sxs-lookup"><span data-stu-id="48270-111">That variable will invoke the extension method, and its value is bound to the first parameter, `aString`.</span></span> <span data-ttu-id="48270-112">L’instruction d’appel suivante affichera `Ready?`.</span><span class="sxs-lookup"><span data-stu-id="48270-112">The following calling statement will display `Ready?`.</span></span>  
  
    ```  
    example.PrintAndPunctuate("?")  
    ```  
  
     <span data-ttu-id="48270-113">Notez que l’appel à cette méthode d’extension ressemble à un appel à l’un de le <xref:System.String> les méthodes qui nécessitent un paramètre d’instance :</span><span class="sxs-lookup"><span data-stu-id="48270-113">Notice that the call to this extension method looks just like a call to any one of the <xref:System.String> instance methods that require one parameter:</span></span>  
  
    ```  
    example.EndsWith("dy")  
    example.IndexOf("R")  
    ```  
  
3.  <span data-ttu-id="48270-114">Déclarer une autre variable de chaîne et appelez la méthode pour vérifier qu’elle fonctionne avec n’importe quelle chaîne.</span><span class="sxs-lookup"><span data-stu-id="48270-114">Declare another string variable and call the method again to see that it works with any string.</span></span>  
  
    ```  
    Dim example2 = " or not"  
    example2.PrintAndPunctuate("!!!")  
    ```  
  
     <span data-ttu-id="48270-115">Cette fois-ci il en résulte : `or not!!!`.</span><span class="sxs-lookup"><span data-stu-id="48270-115">The result this time is: `or not!!!`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="48270-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="48270-116">Example</span></span>  
 <span data-ttu-id="48270-117">Le code suivant est un exemple complet de la création et utilisation d’une méthode d’extension simple.</span><span class="sxs-lookup"><span data-stu-id="48270-117">The following code is a complete example of the creation and use of a simple extension method.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="48270-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48270-118">See also</span></span>
- [<span data-ttu-id="48270-119">Guide pratique pour Écrire une méthode d’Extension</span><span class="sxs-lookup"><span data-stu-id="48270-119">How to: Write an Extension Method</span></span>](./how-to-write-an-extension-method.md)
- [<span data-ttu-id="48270-120">Méthodes d’extension</span><span class="sxs-lookup"><span data-stu-id="48270-120">Extension Methods</span></span>](./extension-methods.md)
- [<span data-ttu-id="48270-121">Portée dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="48270-121">Scope in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
