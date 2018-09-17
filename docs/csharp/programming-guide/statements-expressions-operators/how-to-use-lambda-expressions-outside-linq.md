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
# <a name="how-to-use-lambda-expressions-outside-linq-c-programming-guide"></a>Guide pratique pour utiliser des expressions lambda en dehors de LINQ (Guide de programmation C#)
Les expressions lambda ne sont pas limitées aux requêtes [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)]. Vous pouvez les utiliser partout où une valeur de délégué est attendue, c’est-à-dire, partout où une méthode anonyme peut être utilisée. L’exemple suivant montre comment utiliser une expression lambda dans un gestionnaire d’événements Windows Forms. Notez que les types des entrées (<xref:System.Object> et <xref:System.Windows.Forms.MouseEventArgs>) sont déduits par le compilateur et n’ont pas à être fournis explicitement dans les paramètres d’entrée lambda.  
  
## <a name="example"></a>Exemple  
  
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
  
## <a name="see-also"></a>Voir aussi

- [Expressions lambda](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)  
- [Méthodes anonymes](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)  
- [LINQ (Language Integrated Query)](../../../csharp/programming-guide/concepts/linq/index.md)
