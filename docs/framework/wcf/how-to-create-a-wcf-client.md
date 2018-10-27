---
title: 'Comment : créer un client Windows Communication Foundation'
ms.date: 09/14/2018
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: 9572f3e2c0cddf75daf343f250b16e94bc2b0dbf
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50181668"
---
# <a name="how-to-create-a-windows-communication-foundation-client"></a>Comment : créer un client Windows Communication Foundation

Il s’agit de la quatrième des six tâches requises pour créer une application Windows Communication Foundation (WCF). Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).

Cette rubrique décrit comment récupérer les métadonnées d’un service WCF et l’utiliser pour créer un proxy WCF qui peut accéder au service. Cette tâche est effectuée à l’aide de la **ajouter une référence de Service** fonctionnalités fournies par Visual Studio. Cet outil obtient les métadonnées du point de terminaison MEX du service et génère un fichier de code source managé pour un proxy client dans le langage que vous avez choisi (C# par défaut). L'outil crée non seulement le proxy client, mais également le fichier de configuration (ou le met à jour) pour le client qui permet à l'application cliente de se connecter au service au niveau de l'un de ses points de terminaison.

> [!NOTE]
> Vous pouvez également utiliser le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) outil pour générer la classe proxy et la configuration au lieu d’utiliser **ajouter une référence de Service** dans Visual Studio.

> [!NOTE]
> Lorsque vous appelez un service WCF à partir d’un projet de bibliothèque de classes dans Visual Studio, vous pouvez utiliser la **ajouter une référence de Service** fonctionnalité pour générer automatiquement un proxy et un fichier de configuration associé. Le fichier de configuration ne sera pas utilisé par le projet de bibliothèque de classes. Vous devez ajouter les paramètres dans le fichier de configuration généré dans le fichier app.config pour le fichier exécutable qui appelle la bibliothèque de classes.

L'application cliente utilise la classe proxy générée pour communiquer avec le service. Cette procédure est décrite dans [Comment : utiliser un Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).

## <a name="to-create-a-windows-communication-foundation-client"></a>Pour créer un client Windows Communication Foundation

1. Créer un nouveau projet d’application console dans Visual Studio. Avec le bouton droit sur la solution de mise en route dans **l’Explorateur de solutions** et sélectionnez **ajouter** > **nouveau projet**. Dans le **ajouter un nouveau projet** boîte de dialogue, sur le côté gauche, sélectionnez le **Windows Desktop** catégorie sous **Visual C#** ou **Visual Basic**. Sélectionnez le **application Console (.NET Framework)** modèle, puis nommez le projet **GettingStartedClient**.

2. Ajoutez une référence à System.ServiceModel dans le projet GettingStartedClient. Avec le bouton droit sur le **références** dossier sous le projet GettingStartedClient dans **l’Explorateur de solutions**, puis sélectionnez **ajouter une référence**. Dans le **ajouter une référence** boîte de dialogue, sélectionnez **Framework** sur le côté gauche de la boîte de dialogue **assemblys**. Recherchez et sélectionnez **System.ServiceModel**, puis choisissez **OK**. Enregistrez la solution en sélectionnant **fichier** > **Enregistrer tout**.

3. Ajouter une référence de service pour le Service de calculatrice.

   1. Tout d’abord, démarrez l’application de console GettingStartedHost.

   2. Une fois que l’hôte est en cours d’exécution, cliquez sur le **références** dossier sous le projet GettingStartedClient dans **l’Explorateur de solutions** et sélectionnez **ajouter**  >   **Référence de service**.

   3. Entrez l’URL suivante dans la zone Adresse de la **ajouter une référence de Service** boîte de dialogue : [http://localhost:8000/GettingStarted/CalculatorService](http://localhost:8000/GettingStarted/CalculatorService)

   4. Choisissez **accédez**.

   Le CalculatorService s’affiche dans le **Services** zone de liste. Double-cliquez sur CalculatorService pour développer et afficher les contrats de service implémentés par le service. Laissez l’espace de noms par défaut en tant que-est et choisissez **OK**.

    Lorsque vous ajoutez une référence à un service à l’aide de Visual Studio, un nouvel élément apparaît dans **l’Explorateur de solutions** sous le **références de Service** dossier sous le projet GettingStartedClient. Si vous utilisez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) outil, un fichier de code source et le fichier app.config sont générés.

    Vous pouvez également utiliser l’outil de ligne de commande [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) avec les commutateurs appropriés pour créer le code client. L'exemple suivant génère un fichier de code et un fichier de configuration pour le service. Le premier exemple montre comment générer le proxy en VB, et le second montre comment générer le proxy en c# :

    ```shell
    svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/GettingStarted/CalculatorService
    ```

    ```shell
    svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/GettingStarted/CalculatorService
    ```

## <a name="next-steps"></a>Étapes suivantes

Vous avez créé le proxy utilisera l’application cliente pour appeler le service de calculatrice. Passez à la rubrique suivante de la série.

> [!div class="nextstepaction"]
> [Guide pratique pour configurer un client](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

## <a name="see-also"></a>Voir aussi

- [Outil ServiceModel Metadata Utility (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [Prise en main](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [Auto-hébergement](../../../docs/framework/wcf/samples/self-host.md)
- [Guide pratique pour publier les métadonnées d’un service à l’aide d’un fichier de configuration](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [Guide pratique pour utiliser Svcutil.exe pour télécharger des documents de métadonnées](../../../docs/framework/wcf/feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
