---
title: 'Procédure : créer un service de workflow qui appelle un autre service de workflow'
ms.date: 03/30/2017
ms.assetid: 99b3ee3e-aeb7-4e6f-8321-60fe6140eb67
ms.openlocfilehash: 1b30da34f7c85cccd98b18cd32b81c83630989b2
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43452727"
---
# <a name="how-to-create-a-workflow-service-that-calls-another-workflow-service"></a>Procédure : créer un service de workflow qui appelle un autre service de workflow

Il est parfois nécessaire pour un service de workflow d'obtenir des informations d'un autre service de workflow. Cette rubrique montre comment appeler un service de workflow à partir d'un autre service. Dans cette rubrique, vous créerez deux services de workflow ; un qui a une méthode qui inverse la chaîne d'entrée et un autre qui convertit la chaîne d'entrée en majuscules après avoir inversé la chaîne qui utilise le premier service.

### <a name="to-create-the-reverser-workflow-service"></a>Pour créer le service de workflow Reverser

1.  Ouvrez Visual Studio.

2.  Sélectionnez **fichier** > **nouveau projet**. Sous le **Workflow** nœud dans le **modèles installés** volet, sélectionnez **Application de Service de Workflow WCF**. Nommez la solution `NestedServices` puis cliquez sur **OK**.

3.  Sous **serveurs**, assurez-vous que l’option **utiliser le serveur Web IIS Local** est sélectionné. Cliquez sur **créer le répertoire virtuel**. Cliquez sur **OK** dans la boîte de dialogue indiquant que le répertoire virtuel a été créé.

4.  Dans l’Explorateur de solutions, renommez Service1.xamlx `StringReverserService.xamlx`.

5.  Sur le **propriétés du projet** pour le nouveau projet, cliquez sur le **Web** onglet. Définir le **Action de démarrage** à **Page spécifique**et sélectionnez StringReverserService.xamlx en tant que la page pour démarrer.

6.  Ouvrez le fichier StringReverserService.xamlx dans le concepteur et supprimez les activités `ReceiveRequest` et `SendReply` existantes, puis faites glisser une activité `ReceiveAndSendReply` dans l'activité de la séquence existante.

    1.  Définir le **NomOpération** sur ReverseString.

    2.  Définir le **ServiceContractName** sur IReverseString.

    3.  Sélectionnez le **CanCreateInstance** case à cocher.

7.  Sélectionnez le **SequentialService** activité, puis cliquez sur le **Variables** onglet en bas du concepteur. Créez deux nouvelles variables nommées StringToReverse et ReversedStringToReturn de type String.

8.  Cliquez sur le **définir** lien dans le **réception** activité. Cliquez sur le **paramètres**et créez un paramètre nommé InputString de type String qui assigne à StringToReverse.

9. Cliquez sur le **définir** lien dans le **SendReplyToReceive** activité. Cliquez sur le **paramètres**et créez un paramètre nommé ReversedString de type String, assigné à ReversedStringToReturn.

10. Pour implémenter la logique pour le service, créez une nouvelle classe nommée StringLibrary dans le projet.  Remplacez la définition de la classe par le code suivant.

    ```
    public class StringLibrary
        {
            public static String ReverseString(string StringToReverse)
            {
                char[] charArray = StringToReverse.ToCharArray();
                Array.Reverse(charArray);
                return new String(charArray);
            }
        }
    ```

11. Pour appeler la méthode ReverseString sur l’entrée, faites glisser un **InvokeMethod** activité à partir de la boîte à outils vers l’espace entre le **réception** et **SendReply** activités. Définissez les propriétés de l'activité comme ci-dessous.

    1.  **MethodName**: ReverseString

    2.  **Résultat**: ReversedStringToReturn

    3.  **Paramètres**: créer un nouveau paramètre avec un **Direction** in, un **Type** de chaîne et un **valeur** stringtoreverse.

    4.  **TargetType**: NestedServices.StringLibrary

12. Testez le service en appuyant sur F5. Dans le Client test WCF qui s'affiche, double-cliquez sur la méthode ReverseString(). Dans le volet de requête, entrez `Sample` pour la valeur du paramètre InputString. Cliquez sur **appeler**. Le service doit retourner « elpmaS ».

### <a name="to-create-the-uppercaser-workflow-service"></a>Pour créer le service de workflow UpperCaser

1.  Cliquez sur le projet NestedServices et sélectionnez **ajouter** > **un nouvel élément**. Dans le **Workflow** nœud, sélectionnez **Service de Workflow WCF**et nommez le nouveau service `UpperCaserService`. Cliquez sur **Ajouter**. Un nouveau service de workflow nommé UpperCaserService.xamlx doit être ajouté au projet.

2.  Ouvrez le fichier Uppercaserservices.xamlx dans le concepteur et supprimez les **ReceiveRequest** et `SendReply` activités, puis faites glisser un `ReceiveAndSendReply` activité dans l’activité de séquence existante.

    1.  Définir le **NomOpération** sur UpperCaseString.

    2.  Définir le **ServiceContractName** sur IUpperCaseString.

    3.  Sélectionnez le **CanCreateInstance** case à cocher.

3.  Sélectionnez l’activité SequentialService, puis cliquez sur le **Variables** onglet en bas du concepteur. Créez trois nouvelles variables nommées StringToUpper, StringToReverse et StringToReturn de type String.

4.  Cliquez sur le **définir** lien dans le **réception** activité. Cliquez sur le **paramètres**et créez un paramètre nommé InputString de type String qui assigne à StringToUpper.

5.  Cliquez sur le **définir** lien dans le **SendReplyToReceive** activité. Cliquez sur le **paramètres**et créez un paramètre nommé ModifiedString de type String, assigné à StringToReturn.

6.  Pour implémenter la logique pour le service, créez une nouvelle méthode dans la classe StringLibrary à l'aide du code suivant.

    ```
    public static String UpperCaseString(string StringToUpperCase)
    {
         return StringToUpperCase.ToUpper();

    }
    ```

7.  Pour appeler la méthode UpperCaseString sur l’entrée, faites glisser un **InvokeMethod** activité à partir de la boîte à outils vers l’espace entre le **réception** et **SendReply** activités. Définissez les propriétés de l'activité comme ci-dessous.

    1.  **MethodName**: UpperCaseString

    2.  **Résultat**: StringToReverse

    3.  **Paramètres**: créer un nouveau paramètre avec un **Direction** in, un **Type** de chaîne et un **valeur** stringtoupper.

    4.  **TargetType**: NestedServices.StringLibrary

8.  Vous allez maintenant appeler le premier service sur la chaîne modifiée. Cliquez sur le projet et sélectionnez **ajouter** > **une référence de Service**. Ajouter une référence de service au service à http://localhost/NestedServices/StringReverserService.xamlx et générez le projet pour créer une activité personnalisée pour accéder au premier service Web.

9. Faire glisser une instance de la nouvelle activité du workflow, entre le **InvokeMethod** activité et le **SendReplyToReceive** activités. Assignez la variable StringToReverse à la propriété InputString de la nouvelle activité, et la variable StringToReturn à la propriété StringToReturn.

10. Ouvrez la page de propriétés pour le projet NestedServices et modifier le **Page spécifique** dans le **Web** onglet par uppercaserservice.xamlx.

11. Testez le service en appuyant sur F5. Dans le Client test WCF qui s'affiche, double-cliquez sur la méthode ReverseString(). Dans le volet de requête, entrez `Sample` pour la valeur du paramètre InputString. Cliquez sur **appeler**. Le service doit retourner « ELPMAS ».

### <a name="to-create-a-client-to-call-the-services"></a>Pour créer un client qui appelle les services

1.  Ajoutez à la solution un nouveau projet d'application console nommé Client.

2.  Cliquez sur le projet Client et sélectionnez **ajouter** > **une référence de Service**. Dans la fenêtre qui s’affiche, cliquez sur **Discover**. Sélectionnez StringReverserService.xamlx et entrez ReverseService comme espace de noms.  Cliquez sur **OK**.

3.  Remplacez le code de la méthode Main dans Program.cs par le code suivant.

    ```
    static void Main(string[] args)
    {
        Console.Write("Input string to process:");
        String input = Console.ReadLine();
        var service = new ReverseService.ReverseStringClient();
        Console.WriteLine("Output from service: {0}", service.ReverseString(input));
        Console.ReadKey();
    }
    ```