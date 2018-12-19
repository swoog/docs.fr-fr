---
title: 'Procédure : Utiliser des expressions lambda en dehors de LINQ - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [C#], outside LINQ
ms.assetid: 2b519274-6ee4-4455-ab2e-aed67dbfd07c
ms.openlocfilehash: d4dc0375552ef1fe00f629c22b5296399b4cc99d
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243931"
---
# <a name="how-to-use-lambda-expressions-outside-linq-c-programming-guide"></a>Procédure : Utiliser des expressions lambda en dehors de LINQ (Guide de programmation C#)
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
