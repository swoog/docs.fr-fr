---
title: 'Comment : implémenter un contrat de service Windows Communication Foundation'
ms.date: 09/14/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- service contracts [WCF], implementing
ms.assetid: d5ab51ba-61ae-403e-b3c8-e2669e326806
ms.openlocfilehash: 569de6f49b56b46ccfeb22e9f0bd25bcf339b7e0
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47088137"
---
# <a name="how-to-implement-a-windows-communication-foundation-service-contract"></a><span data-ttu-id="41a88-102">Comment : implémenter un contrat de service Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="41a88-102">How to: Implement a Windows Communication Foundation Service Contract</span></span>

<span data-ttu-id="41a88-103">Il s’agit de la deuxième des six tâches requises pour créer un service Windows Communication Foundation (WCF) de base et un client pouvant appeler le service.</span><span class="sxs-lookup"><span data-stu-id="41a88-103">This is the second of six tasks required to create a basic Windows Communication Foundation (WCF) service and a client that can call the service.</span></span> <span data-ttu-id="41a88-104">Pour une vue d’ensemble de tous les six tâches, consultez le [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) rubrique.</span><span class="sxs-lookup"><span data-stu-id="41a88-104">For an overview of all six tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="41a88-105">L'étape suivante pour créer une application WCF consiste à implémenter l'interface de service.</span><span class="sxs-lookup"><span data-stu-id="41a88-105">The next step in creating a WCF application is to implement the service interface.</span></span> <span data-ttu-id="41a88-106">Cela implique la création d'une classe appelée `CalculatorService` qui implémente l'interface `ICalculator` définie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="41a88-106">This involves creating a class called `CalculatorService` that implements the user-defined `ICalculator` interface..</span></span>

## <a name="to-implement-a-wcf-service-contract"></a><span data-ttu-id="41a88-107">Pour implémenter un contrat de service WCF</span><span class="sxs-lookup"><span data-stu-id="41a88-107">To implement a WCF service contract</span></span>

<span data-ttu-id="41a88-108">Ouvrez le fichier Service1.cs ou Service1.vb et ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="41a88-108">Open the Service1.cs or Service1.vb file and add the following code:</span></span>

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

<span data-ttu-id="41a88-109">Chaque méthode implémente l'opération de calculatrice et écrit du texte dans la console pour faciliter le test.</span><span class="sxs-lookup"><span data-stu-id="41a88-109">Each method implements the calculator operation and writes some text to the console to make testing easier.</span></span>

## <a name="example"></a><span data-ttu-id="41a88-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="41a88-110">Example</span></span>

<span data-ttu-id="41a88-111">Le code suivant affiche à la fois l'interface qui définit le contrat et l'implémentation de l'interface.</span><span class="sxs-lookup"><span data-stu-id="41a88-111">The following code shows both the interface that defines the contract and the implementation of the interface.</span></span>

```csharp
using System;
using System.ServiceModel;

namespace GettingStartedLib
{
    [ServiceContract(Namespace = "http://Microsoft.ServiceModel.Samples")]
    public interface ICalculator
    {
        [OperationContract]
        double Add(double n1, double n2);
        [OperationContract]
        double Subtract(double n1, double n2);
        [OperationContract]
        double Multiply(double n1, double n2);
        [OperationContract]
        double Divide(double n1, double n2);
    }
}
```

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

    <ServiceContract(Namespace:="http://Microsoft.ServiceModel.Samples")> _
    Public Interface ICalculator

        <OperationContract()> _
        Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double
        <OperationContract()> _
        Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double
    End Interface
End Namespace
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

## <a name="compile-the-code"></a><span data-ttu-id="41a88-112">Compiler le code</span><span class="sxs-lookup"><span data-stu-id="41a88-112">Compile the code</span></span>

<span data-ttu-id="41a88-113">Générez la solution pour vous assurer qu'il n’y a aucune erreur de compilation.</span><span class="sxs-lookup"><span data-stu-id="41a88-113">Build the solution to ensure there are no compilation errors.</span></span> <span data-ttu-id="41a88-114">Si vous utilisez Visual Studio, sur le **Build** menu, sélectionnez **générer la Solution** (ou appuyez sur **Ctrl**+**MAJ** + **B**).</span><span class="sxs-lookup"><span data-stu-id="41a88-114">If you're using Visual Studio, on the **Build** menu select **Build Solution** (or press **Ctrl**+**Shift**+**B**).</span></span>

## <a name="next-steps"></a><span data-ttu-id="41a88-115">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="41a88-115">Next steps</span></span>

<span data-ttu-id="41a88-116">Le contrat de service est créé et implémenté.</span><span class="sxs-lookup"><span data-stu-id="41a88-116">Now the service contract is created and implemented.</span></span> <span data-ttu-id="41a88-117">Dans l’étape suivante, vous exécutez le service.</span><span class="sxs-lookup"><span data-stu-id="41a88-117">In the next step, you run the service.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="41a88-118">Guide pratique pour héberger et exécuter un service de base</span><span class="sxs-lookup"><span data-stu-id="41a88-118">How to: Host and Run a Basic Service</span></span>](../../../docs/framework/wcf/how-to-host-and-run-a-basic-wcf-service.md)

<span data-ttu-id="41a88-119">Pour obtenir des informations sur la résolution des problèmes, consultez la section [Dépannage du tutoriel Bien démarrer](../../../docs/framework/wcf/troubleshooting-the-getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="41a88-119">For troubleshooting information, see [Troubleshooting the Getting Started Tutorial](../../../docs/framework/wcf/troubleshooting-the-getting-started-tutorial.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="41a88-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41a88-120">See also</span></span>

- [<span data-ttu-id="41a88-121">Prise en main</span><span class="sxs-lookup"><span data-stu-id="41a88-121">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="41a88-122">Auto-hébergement</span><span class="sxs-lookup"><span data-stu-id="41a88-122">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)