---
title: 'Tutoriel : Implémenter un contrat de service Windows Communication Foundation'
ms.date: 03/19/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- service contracts [WCF], implementing
ms.assetid: d5ab51ba-61ae-403e-b3c8-e2669e326806
ms.openlocfilehash: fa8c5457c636d7f37215f0d4b4fdbb1c96c9481e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61929051"
---
# <a name="tutorial-implement-a-windows-communication-foundation-service-contract"></a><span data-ttu-id="6066c-102">Tutoriel : Implémenter un contrat de service Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="6066c-102">Tutorial: Implement a Windows Communication Foundation service contract</span></span>

<span data-ttu-id="6066c-103">Ce didacticiel décrit la deuxième des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base.</span><span class="sxs-lookup"><span data-stu-id="6066c-103">This tutorial describes the second of five tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="6066c-104">Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="6066c-104">For an overview of the tutorials, see [Tutorial: Get started with Windows Communication Foundation applications](getting-started-tutorial.md).</span></span>

<span data-ttu-id="6066c-105">L’étape suivante pour créer une application WCF consiste à ajouter du code pour implémenter l’interface de service WCF que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="6066c-105">The next step for creating a WCF application is to add code to implement the WCF service interface that you created in the previous step.</span></span> <span data-ttu-id="6066c-106">Dans cette étape, vous créez une classe nommée `CalculatorService` qui implémente le défini par l’utilisateur `ICalculator` interface.</span><span class="sxs-lookup"><span data-stu-id="6066c-106">In this step, you create a class named `CalculatorService` that implements the user-defined `ICalculator` interface.</span></span> <span data-ttu-id="6066c-107">Chaque méthode dans le code suivant appelle une opération de calculatrice et écrit du texte dans la console pour le tester.</span><span class="sxs-lookup"><span data-stu-id="6066c-107">Each method in the following code calls a calculator operation and writes text to the console to test it.</span></span> 

<span data-ttu-id="6066c-108">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="6066c-108">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="6066c-109">Ajoutez du code pour implémenter le contrat de service WCF.</span><span class="sxs-lookup"><span data-stu-id="6066c-109">Add code to implement the WCF service contract.</span></span>
> - <span data-ttu-id="6066c-110">Générez la solution.</span><span class="sxs-lookup"><span data-stu-id="6066c-110">Build the solution.</span></span>

## <a name="add-code-to-implement-the-wcf-service-contract"></a><span data-ttu-id="6066c-111">Ajoutez du code pour implémenter le contrat de service WCF</span><span class="sxs-lookup"><span data-stu-id="6066c-111">Add code to implement the WCF service contract</span></span>

<span data-ttu-id="6066c-112">Dans **GettingStartedLib**, ouvrez le **Service1.cs** ou **Service1.vb** fichier et remplacez son code par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="6066c-112">In **GettingStartedLib**, open the **Service1.cs** or **Service1.vb** file and replace its code with the following code:</span></span>

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

## <a name="edit-appconfig"></a><span data-ttu-id="6066c-113">Modifiez le fichier App.config</span><span class="sxs-lookup"><span data-stu-id="6066c-113">Edit App.config</span></span>

<span data-ttu-id="6066c-114">Modifier **App.config** dans **GettingStartedLib** pour refléter les modifications apportées au code.</span><span class="sxs-lookup"><span data-stu-id="6066c-114">Edit **App.config** in **GettingStartedLib** to reflect the changes you made to the code.</span></span>
- <span data-ttu-id="6066c-115">Pour Visual C# projets :</span><span class="sxs-lookup"><span data-stu-id="6066c-115">For Visual C# projects:</span></span>
  - <span data-ttu-id="6066c-116">Modifiez la ligne 14 pour `<service name="GettingStartedLib.CalculatorService">`</span><span class="sxs-lookup"><span data-stu-id="6066c-116">Change line 14 to `<service name="GettingStartedLib.CalculatorService">`</span></span>
  - <span data-ttu-id="6066c-117">Modifiez la ligne 17 en `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span><span class="sxs-lookup"><span data-stu-id="6066c-117">Change line 17 to `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span></span>
  - <span data-ttu-id="6066c-118">Remplacez la ligne 22 à `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`</span><span class="sxs-lookup"><span data-stu-id="6066c-118">Change line 22 to `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.ICalculator">`</span></span>

- <span data-ttu-id="6066c-119">Pour les projets Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="6066c-119">For Visual Basic projects:</span></span>
  - <span data-ttu-id="6066c-120">Modifiez la ligne 14 pour `<service name="GettingStartedLib.GettingStartedLib.CalculatorService">`</span><span class="sxs-lookup"><span data-stu-id="6066c-120">Change line 14 to `<service name="GettingStartedLib.GettingStartedLib.CalculatorService">`</span></span>
  - <span data-ttu-id="6066c-121">Modifiez la ligne 17 en `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span><span class="sxs-lookup"><span data-stu-id="6066c-121">Change line 17 to `<add baseAddress = "http://localhost:8000/GettingStarted/CalculatorService" />`</span></span>
  - <span data-ttu-id="6066c-122">Remplacez la ligne 22 à `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.GettingStartedLib.ICalculator">`</span><span class="sxs-lookup"><span data-stu-id="6066c-122">Change line 22 to `<endpoint address="" binding="wsHttpBinding" contract="GettingStartedLib.GettingStartedLib.ICalculator">`</span></span>

## <a name="compile-the-code"></a><span data-ttu-id="6066c-123">Compiler le code</span><span class="sxs-lookup"><span data-stu-id="6066c-123">Compile the code</span></span>

<span data-ttu-id="6066c-124">Générez la solution pour vérifier que ne contient pas les erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="6066c-124">Build the solution to verify there aren't any compilation errors.</span></span> <span data-ttu-id="6066c-125">Si vous utilisez Visual Studio, sur le **Build** menu, sélectionnez **générer la Solution** (ou appuyez sur **Ctrl**+**MAJ** + **B**).</span><span class="sxs-lookup"><span data-stu-id="6066c-125">If you're using Visual Studio, on the **Build** menu select **Build Solution** (or press **Ctrl**+**Shift**+**B**).</span></span>

## <a name="next-steps"></a><span data-ttu-id="6066c-126">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6066c-126">Next steps</span></span>

<span data-ttu-id="6066c-127">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="6066c-127">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="6066c-128">Ajoutez du code pour implémenter le contrat de service WCF.</span><span class="sxs-lookup"><span data-stu-id="6066c-128">Add code to implement the WCF service contract.</span></span>
> - <span data-ttu-id="6066c-129">Générez la solution.</span><span class="sxs-lookup"><span data-stu-id="6066c-129">Build the solution.</span></span>

<span data-ttu-id="6066c-130">Passez au didacticiel suivant pour apprendre à exécuter le service WCF.</span><span class="sxs-lookup"><span data-stu-id="6066c-130">Advance to the next tutorial to learn how to run the WCF service.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="6066c-131">Tutoriel : Héberger et exécuter un service WCF de base</span><span class="sxs-lookup"><span data-stu-id="6066c-131">Tutorial: Host and run a basic WCF service</span></span>](how-to-host-and-run-a-basic-wcf-service.md)
