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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59169966"
---
# <a name="tutorial-use-a-windows-communication-foundation-client"></a>Tutoriel : Utilisez un client Windows Communication Foundation

Ce didacticiel décrit la dernière des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base. Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).

Une fois que vous avez créé et configuré un proxy de Windows Communication Foundation (WCF), vous créez une instance du client et compilez l’application cliente. Vous l’utilisez ensuite pour communiquer avec le service WCF. 

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> - Ajoutez du code pour utiliser le client WCF.
> - Tester le client WCF.

## <a name="add-code-to-use-the-wcf-client"></a>Ajoutez du code pour utiliser le client WCF

Le code client effectue les étapes suivantes :
- Instancie le client WCF.
- Appelle les opérations de service à partir du proxy généré.
- Ferme le client après que l’appel d’opération est terminée.

Ouvrir le **Program.cs** ou **Module1.vb** de fichiers à partir de la **GettingStartedClient** de projet et remplacez son code par le code suivant :

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

Notez que le `using` (pour Visual C#) ou `Imports` (pour Visual Basic) instruction qui importe `GettingStartedClient.ServiceReference1`. Cette instruction importe le code généré par Visual Studio avec le **ajouter une référence de Service** (fonction). Le code instancie le proxy WCF et appelle chacune des opérations de service qui expose le service de calculatrice. Ensuite, il ferme le proxy et termine le programme.

## <a name="test-the-wcf-client"></a>Tester le client WCF

### <a name="test-the-application-from-visual-studio"></a>Tester l’application à partir de Visual Studio

1. Enregistrez et générez la solution.

2. Sélectionnez le **GettingStartedLib** dossier, puis sélectionnez **définir comme projet de démarrage** dans le menu contextuel.

3. À partir de **les projets de démarrage**, sélectionnez **GettingStartedLib** dans la liste déroulante, puis sélectionnez **exécuter** ou appuyez sur **F5**.

### <a name="test-the-application-from-a-command-prompt"></a>Tester l’application à partir d’une invite de commandes

1. Ouvrez une invite de commandes en tant qu’administrateur, puis accédez à votre répertoire de solution Visual Studio. 

2. Pour démarrer le service : Entrez *GettingStartedHost\bin\Debug\GettingStartedHost.exe*.

3. Pour démarrer le client : Ouvrez une autre invite de commandes, accédez à votre répertoire de solution Visual Studio, puis entrez *GettingStartedClient\bin\Debug\GettingStartedClient.exe*.

   *GettingStartedHost.exe* génère la sortie suivante :

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

   *GettingStartedClient.exe* génère la sortie suivante :

   ```text
   Add(100,15.99) = 115.99
   Subtract(145,76.54) = 68.46
   Multiply(9,81.25) = 731.25
   Divide(22,7) = 3.14285714285714

   Press <Enter> to terminate the client.
   ```

## <a name="next-steps"></a>Étapes suivantes

Vous avez maintenant terminé toutes les tâches dans le didacticiel de prise en main de get WCF. Dans ce didacticiel, vous avez appris à :

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> - Ajoutez du code pour utiliser le client WCF.
> - Tester le client WCF.

Si vous avez des problèmes ou des erreurs dans une des étapes, suivez les étapes décrites dans l’article de dépannage pour les corriger.

> [!div class="nextstepaction"]
> [Résoudre les problèmes de la méthode Get en main des didacticiels WCF](troubleshooting-the-getting-started-tutorial.md)
