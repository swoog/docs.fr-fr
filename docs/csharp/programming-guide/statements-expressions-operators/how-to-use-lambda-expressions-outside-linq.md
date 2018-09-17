---
title: Guide pratique pour utiliser des expressions lambda en dehors de LINQ (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [C#], outside LINQ
ms.assetid: 2b519274-6ee4-4455-ab2e-aed67dbfd07c
ms.openlocfilehash: eb9fea64b8aeb96a880b7e177673c1316b7aa4c1
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44261529"
---
# <a name="how-to-use-lambda-expressions-outside-linq-c-programming-guide"></a><span data-ttu-id="03d1a-102">Guide pratique pour utiliser des expressions lambda en dehors de LINQ (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="03d1a-102">How to: Use Lambda Expressions Outside LINQ (C# Programming Guide)</span></span>
<span data-ttu-id="03d1a-103">Les expressions lambda ne sont pas limitées aux requêtes [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="03d1a-103">Lambda expressions are not limited to [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] queries.</span></span> <span data-ttu-id="03d1a-104">Vous pouvez les utiliser partout où une valeur de délégué est attendue, c’est-à-dire, partout où une méthode anonyme peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="03d1a-104">You can use them anywhere a delegate value is expected, that is, wherever an anonymous method can be used.</span></span> <span data-ttu-id="03d1a-105">L’exemple suivant montre comment utiliser une expression lambda dans un gestionnaire d’événements Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="03d1a-105">The following example shows how to use a lambda expression in a Windows Forms event handler.</span></span> <span data-ttu-id="03d1a-106">Notez que les types des entrées (<xref:System.Object> et <xref:System.Windows.Forms.MouseEventArgs>) sont déduits par le compilateur et n’ont pas à être fournis explicitement dans les paramètres d’entrée lambda.</span><span class="sxs-lookup"><span data-stu-id="03d1a-106">Notice that the types of the inputs (<xref:System.Object> and <xref:System.Windows.Forms.MouseEventArgs>) are inferred by the compiler and do not have to be explicitly given in the lambda input parameters.</span></span>  
  
## <a name="example"></a><span data-ttu-id="03d1a-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="03d1a-107">Example</span></span>  
  
```csharp  
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
  
## <a name="see-also"></a><span data-ttu-id="03d1a-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03d1a-108">See Also</span></span>

- [<span data-ttu-id="03d1a-109">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="03d1a-109">Lambda Expressions</span></span>](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)  
- [<span data-ttu-id="03d1a-110">Méthodes anonymes</span><span class="sxs-lookup"><span data-stu-id="03d1a-110">Anonymous Methods</span></span>](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)  
- [<span data-ttu-id="03d1a-111">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="03d1a-111">Language Integrated Query (LINQ))</span></span>](../../../csharp/programming-guide/concepts/linq/index.md)
