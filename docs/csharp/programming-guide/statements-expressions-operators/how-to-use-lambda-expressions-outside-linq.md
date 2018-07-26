---
title: Guide pratique pour utiliser des expressions lambda en dehors de LINQ (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [C#], outside LINQ
ms.assetid: 2b519274-6ee4-4455-ab2e-aed67dbfd07c
ms.openlocfilehash: a7b7d25adab7ce1fc777b3bdbe581666ab952413
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2018
ms.locfileid: "37959719"
---
# <a name="how-to-use-lambda-expressions-outside-linq-c-programming-guide"></a><span data-ttu-id="c75c4-102">Guide pratique pour utiliser des expressions lambda en dehors de LINQ (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="c75c4-102">How to: Use Lambda Expressions Outside LINQ (C# Programming Guide)</span></span>
<span data-ttu-id="c75c4-103">Les expressions lambda ne sont pas limitées aux requêtes [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="c75c4-103">Lambda expressions are not limited to [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] queries.</span></span> <span data-ttu-id="c75c4-104">Vous pouvez les utiliser partout où une valeur de délégué est attendue, c’est-à-dire, partout où une méthode anonyme peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c75c4-104">You can use them anywhere a delegate value is expected, that is, wherever an anonymous method can be used.</span></span> <span data-ttu-id="c75c4-105">L’exemple suivant montre comment utiliser une expression lambda dans un gestionnaire d’événements Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="c75c4-105">The following example shows how to use a lambda expression in a Windows Forms event handler.</span></span> <span data-ttu-id="c75c4-106">Notez que les types des entrées (<xref:System.Object> et <xref:System.Windows.Forms.MouseEventArgs>) sont déduits par le compilateur et n’ont pas à être fournis explicitement dans les paramètres d’entrée lambda.</span><span class="sxs-lookup"><span data-stu-id="c75c4-106">Notice that the types of the inputs (<xref:System.Object> and <xref:System.Windows.Forms.MouseEventArgs>) are inferred by the compiler and do not have to be explicitly given in the lambda input parameters.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c75c4-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="c75c4-107">Example</span></span>  
  
```  
public partial class Form1 : Form  
{  
    public Form1()  
    {  
        InitializeComponent();  
        // Use a lambda expression to define an event handler.  
       this.Click += (s, e) => { MessageBox.Show(((MouseEventArgs)e).Location.ToString());};  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="c75c4-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c75c4-108">See Also</span></span>  
 [<span data-ttu-id="c75c4-109">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="c75c4-109">Lambda Expressions</span></span>](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)  
 [<span data-ttu-id="c75c4-110">Méthodes anonymes</span><span class="sxs-lookup"><span data-stu-id="c75c4-110">Anonymous Methods</span></span>](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)  
 [<span data-ttu-id="c75c4-111">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="c75c4-111">LINQ (Language-Integrated Query)</span></span>](http://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)
