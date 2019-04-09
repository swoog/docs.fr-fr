---
title: 'Tutoriel : Utilisez un client Windows Communication Foundation'
ms.date: 03/19/2019
helpviewer_keywords:
- WCF clients [WCF], using
dev_langs:
- CSharp
- VB
ms.assetid: 190349fc-0573-49c7-bb85-8e316df7f31f
ms.openlocfilehash: fa9aa3612a8dc72623fc4ea4b1ea337ac773fa26
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59169966"
---
# <a name="tutorial-use-a-windows-communication-foundation-client"></a><span data-ttu-id="99516-102">Tutoriel : Utilisez un client Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="99516-102">Tutorial: Use a Windows Communication Foundation client</span></span>

<span data-ttu-id="99516-103">Ce didacticiel décrit la dernière des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base.</span><span class="sxs-lookup"><span data-stu-id="99516-103">This tutorial describes the last of five tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="99516-104">Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="99516-104">For an overview of the tutorials, see [Tutorial: Get started with Windows Communication Foundation applications](getting-started-tutorial.md).</span></span>

<span data-ttu-id="99516-105">Une fois que vous avez créé et configuré un proxy de Windows Communication Foundation (WCF), vous créez une instance du client et compilez l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="99516-105">After you've created and configured a Windows Communication Foundation (WCF) proxy, you create a client instance and compile the client application.</span></span> <span data-ttu-id="99516-106">Vous l’utilisez ensuite pour communiquer avec le service WCF.</span><span class="sxs-lookup"><span data-stu-id="99516-106">You then use it to communicate with the WCF service.</span></span> 

<span data-ttu-id="99516-107">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="99516-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="99516-108">Ajoutez du code pour utiliser le client WCF.</span><span class="sxs-lookup"><span data-stu-id="99516-108">Add code to use the WCF client.</span></span>
> - <span data-ttu-id="99516-109">Tester le client WCF.</span><span class="sxs-lookup"><span data-stu-id="99516-109">Test the WCF client.</span></span>

## <a name="add-code-to-use-the-wcf-client"></a><span data-ttu-id="99516-110">Ajoutez du code pour utiliser le client WCF</span><span class="sxs-lookup"><span data-stu-id="99516-110">Add code to use the WCF client</span></span>

<span data-ttu-id="99516-111">Le code client effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="99516-111">The client code does the following steps:</span></span>
- <span data-ttu-id="99516-112">Instancie le client WCF.</span><span class="sxs-lookup"><span data-stu-id="99516-112">Instantiates the WCF client.</span></span>
- <span data-ttu-id="99516-113">Appelle les opérations de service à partir du proxy généré.</span><span class="sxs-lookup"><span data-stu-id="99516-113">Calls the service operations from the generated proxy.</span></span>
- <span data-ttu-id="99516-114">Ferme le client après que l’appel d’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="99516-114">Closes the client after the operation call is completed.</span></span>

<span data-ttu-id="99516-115">Ouvrir le **Program.cs** ou **Module1.vb** de fichiers à partir de la **GettingStartedClient** de projet et remplacez son code par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="99516-115">Open the **Program.cs** or **Module1.vb** file from the **GettingStartedClient** project and replace its code with the following code:</span></span>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using GettingStartedClient.ServiceReference1;

namespace GettingStartedClient
{
    class Program
    {
        static void Main(string[] args)
        {
            //Step 1: Create an instance of the WCF proxy.
            CalculatorClient client = new CalculatorClient();

            // Step 2: Call the service operations.
            // Call the Add service operation.
            double value1 = 100.00D;
            double value2 = 15.99D;
            double result = client.Add(value1, value2);
            Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result);

            // Call the Subtract service operation.
            value1 = 145.00D;
            value2 = 76.54D;
            result = client.Subtract(value1, value2);
            Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result);

            // Call the Multiply service operation.
            value1 = 9.00D;
            value2 = 81.25D;
            result = client.Multiply(value1, value2);
            Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result);

            // Call the Divide service operation.
            value1 = 22.00D;
            value2 = 7.00D;
            result = client.Divide(value1, value2);
            Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result);

            // Step 3: Close the client to gracefully close the connection and clean up resources.
            Console.WriteLine("\nPress <Enter> to terminate the client.");
            Console.ReadLine();
            client.Close();
        }
    }
}
```

```vb
Imports System
Imports System.Collections.Generic
Imports System.Text
Imports System.ServiceModel
Imports GettingStartedClient.ServiceReference1

Module Module1

    Sub Main()
        ' Step 1: Create an instance of the WCF proxy.
        Dim Client As New CalculatorClient()

        ' Step 2: Call the service operations.
        ' Call the Add service operation.
        Dim value1 As Double = 100D
        Dim value2 As Double = 15.99D
        Dim result As Double = Client.Add(value1, value2)
        Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result)

        ' Call the Subtract service operation.
        value1 = 145D
        value2 = 76.54D
        result = Client.Subtract(value1, value2)
        Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result)

        ' Call the Multiply service operation.
        value1 = 9D
        value2 = 81.25D
        result = Client.Multiply(value1, value2)
        Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result)

        ' Call the Divide service operation.
        value1 = 22D
        value2 = 7D
        result = Client.Divide(value1, value2)
        Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result)

        ' Step 3: Close the client to gracefully close the connection and clean up resources.
        Console.WriteLine()
        Console.WriteLine("Press <Enter> to terminate the client.")
        Console.ReadLine()
        Client.Close()

    End Sub

End Module
```

<span data-ttu-id="99516-116">Notez que le `using` (pour Visual C#) ou `Imports` (pour Visual Basic) instruction qui importe `GettingStartedClient.ServiceReference1`.</span><span class="sxs-lookup"><span data-stu-id="99516-116">Notice the `using` (for Visual C#) or `Imports` (for Visual Basic) statement that imports `GettingStartedClient.ServiceReference1`.</span></span> <span data-ttu-id="99516-117">Cette instruction importe le code généré par Visual Studio avec le **ajouter une référence de Service** (fonction).</span><span class="sxs-lookup"><span data-stu-id="99516-117">This statement imports the code that Visual Studio generated with the **Add Service Reference** function.</span></span> <span data-ttu-id="99516-118">Le code instancie le proxy WCF et appelle chacune des opérations de service qui expose le service de calculatrice.</span><span class="sxs-lookup"><span data-stu-id="99516-118">The code instantiates the WCF proxy and calls each of the service operations that the calculator service exposes.</span></span> <span data-ttu-id="99516-119">Ensuite, il ferme le proxy et termine le programme.</span><span class="sxs-lookup"><span data-stu-id="99516-119">It then closes the proxy and ends the program.</span></span>

## <a name="test-the-wcf-client"></a><span data-ttu-id="99516-120">Tester le client WCF</span><span class="sxs-lookup"><span data-stu-id="99516-120">Test the WCF client</span></span>

### <a name="test-the-application-from-visual-studio"></a><span data-ttu-id="99516-121">Tester l’application à partir de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="99516-121">Test the application from Visual Studio</span></span>

1. <span data-ttu-id="99516-122">Enregistrez et générez la solution.</span><span class="sxs-lookup"><span data-stu-id="99516-122">Save and build the solution.</span></span>

2. <span data-ttu-id="99516-123">Sélectionnez le **GettingStartedLib** dossier, puis sélectionnez **définir comme projet de démarrage** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="99516-123">Select the **GettingStartedLib** folder, and then select **Set as Startup Project** from the shortcut menu.</span></span>

3. <span data-ttu-id="99516-124">À partir de **les projets de démarrage**, sélectionnez **GettingStartedLib** dans la liste déroulante, puis sélectionnez **exécuter** ou appuyez sur **F5**.</span><span class="sxs-lookup"><span data-stu-id="99516-124">From **Startup Projects**, select **GettingStartedLib** from the drop-down list, then select **Run** or press **F5**.</span></span>

### <a name="test-the-application-from-a-command-prompt"></a><span data-ttu-id="99516-125">Tester l’application à partir d’une invite de commandes</span><span class="sxs-lookup"><span data-stu-id="99516-125">Test the application from a command prompt</span></span>

1. <span data-ttu-id="99516-126">Ouvrez une invite de commandes en tant qu’administrateur, puis accédez à votre répertoire de solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="99516-126">Open a command prompt as an administrator, and then navigate to your Visual Studio solution directory.</span></span> 

2. <span data-ttu-id="99516-127">Pour démarrer le service : Entrez *GettingStartedHost\bin\Debug\GettingStartedHost.exe*.</span><span class="sxs-lookup"><span data-stu-id="99516-127">To start the service: Enter *GettingStartedHost\bin\Debug\GettingStartedHost.exe*.</span></span>

3. <span data-ttu-id="99516-128">Pour démarrer le client : Ouvrez une autre invite de commandes, accédez à votre répertoire de solution Visual Studio, puis entrez *GettingStartedClient\bin\Debug\GettingStartedClient.exe*.</span><span class="sxs-lookup"><span data-stu-id="99516-128">To start the client: Open another command prompt, navigate to your Visual Studio solution directory, then enter *GettingStartedClient\bin\Debug\GettingStartedClient.exe*.</span></span>

   <span data-ttu-id="99516-129">*GettingStartedHost.exe* génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="99516-129">*GettingStartedHost.exe* produces the following output:</span></span>

   ```text
   The service is ready.
   Press <Enter> to terminate the service.

   Received Add(100,15.99)
   Return: 115.99
   Received Subtract(145,76.54)
   Return: 68.46
   Received Multiply(9,81.25)
   Return: 731.25
   Received Divide(22,7)
   Return: 3.14285714285714
   ```

   <span data-ttu-id="99516-130">*GettingStartedClient.exe* génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="99516-130">*GettingStartedClient.exe* produces the following output:</span></span>

   ```text
   Add(100,15.99) = 115.99
   Subtract(145,76.54) = 68.46
   Multiply(9,81.25) = 731.25
   Divide(22,7) = 3.14285714285714

   Press <Enter> to terminate the client.
   ```

## <a name="next-steps"></a><span data-ttu-id="99516-131">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="99516-131">Next steps</span></span>

<span data-ttu-id="99516-132">Vous avez maintenant terminé toutes les tâches dans le didacticiel de prise en main de get WCF.</span><span class="sxs-lookup"><span data-stu-id="99516-132">You've now completed all the tasks in the WCF get started tutorial.</span></span> <span data-ttu-id="99516-133">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="99516-133">In this tutorial, you learned how to:</span></span>

<span data-ttu-id="99516-134">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="99516-134">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="99516-135">Ajoutez du code pour utiliser le client WCF.</span><span class="sxs-lookup"><span data-stu-id="99516-135">Add code to use the WCF client.</span></span>
> - <span data-ttu-id="99516-136">Tester le client WCF.</span><span class="sxs-lookup"><span data-stu-id="99516-136">Test the WCF client.</span></span>

<span data-ttu-id="99516-137">Si vous avez des problèmes ou des erreurs dans une des étapes, suivez les étapes décrites dans l’article de dépannage pour les corriger.</span><span class="sxs-lookup"><span data-stu-id="99516-137">If you have problems or errors in any of the steps, follow the steps in the troubleshooting article to fix them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="99516-138">Résoudre les problèmes de la méthode Get en main des didacticiels WCF</span><span class="sxs-lookup"><span data-stu-id="99516-138">Troubleshoot the Get started with WCF tutorials</span></span>](troubleshooting-the-getting-started-tutorial.md)
