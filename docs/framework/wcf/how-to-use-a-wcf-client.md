---
title: 'Comment : utiliser un client Windows Communication Foundation'
ms.date: 09/14/2018
helpviewer_keywords:
- WCF clients [WCF], using
dev_langs:
- CSharp
- VB
ms.assetid: 190349fc-0573-49c7-bb85-8e316df7f31f
ms.openlocfilehash: 12e911fb899cb85121c129b762828cdda01e64f1
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47193081"
---
# <a name="how-to-use-a-windows-communication-foundation-client"></a>Comment : utiliser un client Windows Communication Foundation

Il s’agit de la dernière des six tâches requises pour créer une application Windows Communication Foundation (WCF) de base. Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).

Une fois qu’un proxy de Windows Communication Foundation (WCF) a été créé et configuré, une instance du client peut être créée et l’application cliente peut être compilée et utilisée pour communiquer avec le service WCF. Cette rubrique décrit les procédures pour l’instanciation et à l’aide d’un client WCF. Cette procédure accomplit trois tâches :

1.  Instancie un client WCF.

2.  Appelle les opérations de service à partir du proxy généré.

3.  Ferme le client une fois que l'appel de l'opération est terminé.

## <a name="use-a-windows-communication-foundation-client"></a>Utilisez un client Windows Communication Foundation

Ouvrez le fichier Program.cs ou Program.vb du projet GettingStartedClient et remplacez le code existant par le code suivant :

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

            //Step 3: Closing the client gracefully closes the connection and cleans up resources.
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
Imports GettingStartedClientVB2.ServiceReference1

Module Module1

    Sub Main()
        ' Step 1: Create an instance of the WCF proxy
        Dim Client As New CalculatorClient()

        'Step 2: Call the service operations.
        'Call the Add service operation.
        Dim value1 As Double = 100D
        Dim value2 As Double = 15.99D
        Dim result As Double = Client.Add(value1, value2)
        Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result)

        'Call the Subtract service operation.
        value1 = 145D
        value2 = 76.54D
        result = Client.Subtract(value1, value2)
        Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result)

        'Call the Multiply service operation.
        value1 = 9D
        value2 = 81.25D
        result = Client.Multiply(value1, value2)
        Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result)

        'Call the Divide service operation.
        value1 = 22D
        value2 = 7D
        result = Client.Divide(value1, value2)
        Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result)

        ' Step 3: Closing the client gracefully closes the connection and cleans up resources.
        Client.Close()

        Console.WriteLine()
        Console.WriteLine("Press <ENTER> to terminate client.")
        Console.ReadLine()

    End Sub

End Module
```

Notez que le `using` ou `Imports` instruction qui importe le `GettingStartedClient.ServiceReference1`. Cette opération importe le code généré par **ajouter une référence de Service** dans Visual Studio. Le code instancie le proxy WCF et appelle chacune des opérations de service exposées par le service de calculatrice, ferme le proxy, puis se termine.

Vous avez maintenant terminé le didacticiel. Vous avez défini un contrat de service, implémenté le contrat de service, généré un proxy WCF, configuré une application cliente WCF, puis utilisé le proxy pour appeler des opérations de service. Pour tester l’application, exécutez d’abord GettingStartedHost pour démarrer le service, puis exécutez GettingStartedClient.

La sortie de GettingStartedHost doit ressembler à ceci :

```text
The service is ready.Press <ENTER> to terminate service.Received Add(100,15.99)Return: 115.99Received Subtract(145,76.54)Return: 68.46Received Multiply(9,81.25)Return: 731.25Received Divide(22,7)Return: 3.14285714285714
```

La sortie de GettingStartedClient doit ressembler à ceci :

```text
Add(100,15.99) = 115.99Subtract(145,76.54) = 68.46Multiply(9,81.25) = 731.25Divide(22,7) = 3.14285714285714Press <ENTER> to terminate client.
```

## <a name="see-also"></a>Voir aussi

- [Génération de clients](../../../docs/framework/wcf/building-clients.md)
- [Guide pratique pour créer un client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [Didacticiel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md)
- [Programmation WCF de base](../../../docs/framework/wcf/basic-wcf-programming.md)
- [Guide pratique pour créer un contrat duplex](../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md)
- [Guide pratique pour accéder aux services ayant un contrat duplex](../../../docs/framework/wcf/feature-details/how-to-access-services-with-a-duplex-contract.md)
- [Prise en main](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [Auto-hébergement](../../../docs/framework/wcf/samples/self-host.md)