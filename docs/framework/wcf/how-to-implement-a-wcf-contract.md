---
title: 'Tutoriel : Implémenter un contrat de service Windows Communication Foundation'
ms.date: 03/19/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- service contracts [WCF], implementing
ms.assetid: d5ab51ba-61ae-403e-b3c8-e2669e326806
ms.openlocfilehash: fcf96af11bae701585acd92001c8000125858449
ms.sourcegitcommit: 3630c2515809e6f4b7dbb697a3354efec105a5cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58410080"
---
# <a name="tutorial-implement-a-windows-communication-foundation-service-contract"></a>Tutoriel : Implémenter un contrat de service Windows Communication Foundation

Ce didacticiel décrit la deuxième des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base. Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).

L’étape suivante pour créer une application WCF consiste à ajouter du code pour implémenter l’interface de service WCF que vous avez créé à l’étape précédente. Dans cette étape, vous créez une classe nommée `CalculatorService` qui implémente le défini par l’utilisateur `ICalculator` interface. Chaque méthode dans le code suivant appelle une opération de calculatrice et écrit du texte dans la console pour le tester. 

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> - Ajoutez du code pour implémenter le contrat de service WCF.
> - Générez la solution.

## <a name="add-code-to-implement-the-wcf-service-contract"></a>Ajoutez du code pour implémenter le contrat de service WCF

Dans **GettingStartedLib**, ouvrez le **Service1.cs** ou **Service1.vb** fichier et remplacez son code par le code suivant :

```csharp
using System;
using System.ServiceModel;

namespace GettingStartedLib
{
    public class CalculatorService : ICalculator
    {
        public double Add(double n1, double n2)
        {
            double result = n1 + n2;
            Console.WriteLine("Received Add({0},{1})", n1, n2);
            // Code added to write output to the console window.
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Subtract(double n1, double n2)
        {
            double result = n1 - n2;
            Console.WriteLine("Received Subtract({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Multiply(double n1, double n2)
        {
            double result = n1 * n2;
            Console.WriteLine("Received Multiply({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }

        public double Divide(double n1, double n2)
        {
            double result = n1 / n2;
            Console.WriteLine("Received Divide({0},{1})", n1, n2);
            Console.WriteLine("Return: {0}", result);
            return result;
        }
    }
}
```

```vb
Imports System.ServiceModel

Namespace GettingStartedLib

    Public Class CalculatorService
        Implements ICalculator

        Public Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Add
            Dim result As Double = n1 + n2
            ' Code added to write output to the console window.
            Console.WriteLine("Received Add({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result
        End Function

        Public Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Subtract
            Dim result As Double = n1 - n2
            Console.WriteLine("Received Subtract({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function

        Public Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Multiply
            Dim result As Double = n1 * n2
            Console.WriteLine("Received Multiply({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function

        Public Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double Implements ICalculator.Divide
            Dim result As Double = n1 / n2
            Console.WriteLine("Received Divide({0},{1})", n1, n2)
            Console.WriteLine("Return: {0}", result)
            Return result

        End Function
    End Class
End Namespace
```

## <a name="edit-appconfig"></a>Modifiez le fichier App.config

Modifier **App.config** dans **GettingStartedLib** pour refléter les modifications apportées au code.
   - Pour Visual C# projets :
       - Modifiez la ligne 14 pour `<service name="GettingStartedLib.CalculatorService">`
       - Modifiez la ligne 17 en `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`
       - Remplacez la ligne 22 à `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`

   - Pour les projets Visual Basic :
       - Modifiez la ligne 14 pour `<service name="GettingStartedLib.GettingStartedLib.CalculatorService">`
       - Modifiez la ligne 17 en `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`
       - Remplacez la ligne 22 à `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.GettingStartedLib.ICalculator">`


## <a name="compile-the-code"></a>Compiler le code

Générez la solution pour vérifier que ne contient pas les erreurs de compilation. Si vous utilisez Visual Studio, sur le **Build** menu, sélectionnez **générer la Solution** (ou appuyez sur **Ctrl**+**MAJ** + **B**).

## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à :
> [!div class="checklist"]
> - Ajoutez du code pour implémenter le contrat de service WCF.
> - Générez la solution.

Passez au didacticiel suivant pour apprendre à exécuter le service WCF.

> [!div class="nextstepaction"]
> [Tutoriel : Héberger et exécuter un service WCF de base](how-to-host-and-run-a-basic-wcf-service.md)
