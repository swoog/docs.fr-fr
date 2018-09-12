---
title: 'Comment : créer un client Windows Communication Foundation'
ms.date: 03/30/2017
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: 9e6d75bf8911a3c36e63b3bc108faae823434d1d
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44509997"
---
# <a name="how-to-create-a-windows-communication-foundation-client"></a>Comment : créer un client Windows Communication Foundation

Il s’agit de la quatrième des six tâches requises pour créer une application Windows Communication Foundation (WCF). Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).

Cette rubrique décrit comment récupérer les métadonnées d’un service WCF et l’utiliser pour créer un proxy WCF qui peut accéder au service. Cette tâche prend fin en utilisant la fonctionnalité Ajouter une référence de service fournie par Visual Studio. Cet outil obtient les métadonnées du point de terminaison MEX du service et génère un fichier de code source managé pour un proxy client dans le langage que vous avez choisi (C# par défaut). L'outil crée non seulement le proxy client, mais également le fichier de configuration (ou le met à jour) pour le client qui permet à l'application cliente de se connecter au service au niveau de l'un de ses points de terminaison.

> [!NOTE]
> Vous pouvez également utiliser le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) outil pour générer la classe proxy et la configuration au lieu d’utiliser Ajouter une référence de Service à l’intérieur de Visual Studio.

> [!WARNING]
> Lors de l’appel d’un service WCF à partir d’un projet de bibliothèque de classes dans [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] vous pouvez utiliser la fonctionnalité Ajouter une référence de Service pour générer automatiquement un proxy et un fichier de configuration associé.  Le fichier de configuration ne sera pas utilisé par le projet de bibliothèque de classes. Vous devez ajouter les paramètres dans le fichier de configuration généré dans le fichier app.config pour le fichier exécutable qui appelle la bibliothèque de classes.

 L'application cliente utilise la classe proxy générée pour communiquer avec le service. Cette procédure est décrite dans [Comment : utiliser un Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).

## <a name="to-create-a-windows-communication-foundation-client"></a>Pour créer un client Windows Communication Foundation

1.  Créer un nouveau projet d’application console en cliquant sur la solution de mise en route, sélectionnez **ajouter**, **nouveau projet**. Dans la boîte de dialogue **Ajouter un nouveau projet**, dans la partie gauche de la boîte de dialogue, sélectionnez **Windows** sous **C#** ou **VB**. Dans la section centrale de la boîte de dialogue, sélectionnez **Application console**. Attribuez un nom au projet `GettingStartedClient`.

2.  Définir le framework cible du projet GettingStartedClient à .NET Framework 4.5 en cliquant avec le bouton droit sur **GettingStartedClient** dans l’Explorateur de solutions et en sélectionnant **propriétés**. Dans la zone de liste déroulante **Framework cible**, sélectionnez **.NET Framework 4.5**. Définition du framework cible pour un projet VB est un peu différent, dans la boîte de dialogue Propriétés du projet GettingStartedClient, cliquez sur le **compiler** onglet sur le côté gauche de l’écran, puis cliquez sur le **avancé Options de compilation** bouton dans le coin inférieur gauche de la boîte de dialogue. Sélectionnez ensuite **.NET Framework 4.5** dans la liste déroulante **Framework cible**.

     Définition du framework cible entraîne Visual Studio 2011 recharger la solution, appuyez sur **OK** lorsque vous y êtes invité.

3.  Ajouter une référence à System.ServiceModel dans le projet GettingStartedClient en cliquant sur le **référence** dossier sous le projet GettingStartedClient dans l’Explorateur de solutions, puis sélectionnez **ajouter** Référence. Dans la boîte de dialogue **Ajouter une référence**, sélectionnez **Framework** dans la partie gauche de la boîte de dialogue. Dans la zone de texte Rechercher des assemblys, tapez `System.ServiceModel`. Dans la section centrale de la boîte de dialogue, sélectionnez **System.ServiceModel**, cliquez sur le bouton **Ajouter**, puis sur le bouton **Fermer**. Enregistrez la solution en cliquant sur le **Enregistrer tout** situé sous le menu principal.

4.  Ensuite, vous ajoutez une référence de service pour le Service de calculatrice. Pour ce faire, vous devez d'abord démarrer l'application console GettingStartedHost. Une fois que l’hôte est en cours d’exécution, cliquez sur le **références** dossier sous le projet GettingStartedClient dans **l’Explorateur de solutions** et sélectionnez **ajouter**  >   **Référence de service**. Tapez l’URL suivante dans la zone Adresse de la **ajouter une référence de Service** boîte de dialogue : [ http://localhost:8000/ServiceModelSamples/Service ](http://localhost:8000/ServiceModelSamples/Service) et cliquez sur le **accédez** bouton. Le CalculatorService doit ensuite être affiché dans la zone de liste de Services. Double-cliquez sur CalculatorService et il développer et afficher les contrats de service implémentés par le service. Laissez l’espace de noms par défaut et cliquez sur le **OK** bouton.

     Lorsque vous ajoutez une référence à un service à l’aide de Visual Studio, un nouvel élément s’affiche dans l’Explorateur de solutions sous le dossier Références de service sous le projet GettingStartedClient.  Si vous utilisez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) outil un fichier de code source et le fichier app.config sont générés.

     Vous pouvez également utiliser l’outil de ligne de commande [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) avec les commutateurs appropriés pour créer le code client. L'exemple suivant génère un fichier de code et un fichier de configuration pour le service. Le premier exemple montre comment générer le proxy en VB et le deuxième montre comment générer le proxy en C# :

    ```
    svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/ServiceModelSamples/service
    ```

    ```csharp
    svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/ServiceModelSamples/service
    ```

 Vous avez créé le proxy que l'application cliente utilisera pour appeler le service de calculatrice. Passez à la rubrique suivante de la série : [Comment : configurer un Client](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

## <a name="see-also"></a>Voir aussi

- [Outil ServiceModel Metadata Utility (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [Prise en main](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [Auto-hébergement](../../../docs/framework/wcf/samples/self-host.md)
- [Guide pratique pour publier les métadonnées d’un service à l’aide d’un fichier de configuration](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [Guide pratique pour utiliser Svcutil.exe pour télécharger des documents de métadonnées](../../../docs/framework/wcf/feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
