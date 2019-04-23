---
title: 'Tutoriel : Créer un client Windows Communication Foundation'
ms.date: 03/19/2019
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: a16a0ccabfd0f9fbe69db1ea88d4613185f3c1da
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59174367"
---
# <a name="tutorial-create-a-windows-communication-foundation-client"></a>Tutoriel : Créer un client Windows Communication Foundation

Ce didacticiel décrit la quatrième des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base. Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).

La tâche suivante pour créer une application WCF consiste à créer un client en récupérant des métadonnées à partir d’un service WCF. Visual Studio vous permet d’ajouter une référence de service, qui obtient les métadonnées de point de terminaison MEX du service. Visual Studio génère ensuite un fichier de code source managé pour un proxy de client dans la langue que vous avez choisie. Il crée également un fichier de configuration de client (*App.config*). Ce fichier permet à l’application client pour se connecter au service à un point de terminaison. 

> [!NOTE]
> Si vous appelez un service WCF à partir d’un projet de bibliothèque de classes dans Visual Studio, utilisez le **ajouter une référence de Service** fonctionnalité pour générer automatiquement un proxy et un fichier de configuration associé. Toutefois, étant donné que les projets bibliothèque de classes n’utilisent pas ce fichier de configuration, vous devez ajouter les paramètres dans le fichier de configuration généré pour le *App.config* fichier pour le fichier exécutable qui appelle la bibliothèque de classes.

> [!NOTE]
> Comme alternative, utilisez la [outil ServiceModel Metadata Utility](#servicemodel-metadata-utility-tool) au lieu de Visual Studio pour générer le fichier de configuration et de la classe proxy.

L'application cliente utilise la classe proxy générée pour communiquer avec le service. Cette procédure est décrite dans [didacticiel : Utiliser un client](how-to-use-a-wcf-client.md).

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> - Créez et configurez un projet d’application console pour le client WCF.
> - Ajouter une référence de service au service WCF pour générer les fichiers de configuration et de la classe proxy.

## <a name="create-a-windows-communication-foundation-client"></a>Créer un client Windows Communication Foundation

1. Créer un projet d’application console dans Visual Studio : 

    1. À partir de la **fichier** menu, sélectionnez **Open** > **projet/Solution** et accédez à la **GettingStarted** solution vous créé précédemment (*GettingStarted.sln*). Sélectionnez **Ouvrir**.

    2. À partir de la **vue** menu, sélectionnez **l’Explorateur de solutions**.

    3. Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **GettingStarted** solution (nœud supérieur) et sélectionnez **ajouter** > **denouveauprojet** dans le menu contextuel. 
    
    4. Dans le **ajouter un nouveau projet** fenêtre, sur le côté gauche, sélectionnez le **Windows Desktop** catégorie sous **Visual C#**  ou **Visual Basic**. 

    5. Sélectionnez le **application Console (.NET Framework)** modèle, puis entrez *GettingStartedClient* pour le **nom**. Sélectionnez **OK**.

2. Ajouter une référence dans le **GettingStartedClient** de projet pour le <xref:System.ServiceModel> assembly : 

    1.  Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **références** dossier sous le **GettingStartedClient** de projet, puis sélectionnez **ajouter une référence** dans le menu contextuel. 

    2. Dans le **ajouter une référence** fenêtre, sous **assemblys** sur le côté gauche de la fenêtre, sélectionnez **Framework**.
    
    3. Recherchez et sélectionnez **System.ServiceModel**, puis choisissez **OK**. 

    4. Enregistrez la solution en sélectionnant **fichier** > **Enregistrer tout**.

3. Ajoutez une référence de service pour le service de calculatrice :

   1. Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **références** dossier sous le **GettingStartedClient** de projet, puis sélectionnez **ajouter une référence de Service**  dans le menu contextuel.

   2. Dans le **ajouter une référence de Service** fenêtre, sélectionnez **Discover**.

      Le CalculatorService service démarre et que Visual Studio affiche dans le **Services** boîte.

   3. Sélectionnez **CalculatorService** pour le développer et afficher les contrats de service implémentés par le service. Laissez la valeur par défaut **Namespace** et choisissez **OK**.

      Visual Studio ajoute un nouvel élément sous le **Services connectés** dossier dans le **GettingStartedClient** projet. 

### <a name="servicemodel-metadata-utility-tool"></a>Outil ServiceModel Metadata Utility

Les exemples suivants montrent comment utiliser éventuellement le [ServiceModel Metadata Utility tool (Svcutil.exe)](servicemodel-metadata-utility-tool-svcutil-exe.md) pour générer le fichier de classe proxy. Cet outil génère le fichier de classe de proxy et le *App.config* fichier. Les exemples suivants montrent comment générer le proxy dans C# et Visual Basic, respectivement :

```shell
svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/GettingStarted/CalculatorService
```

```shell
svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/GettingStarted/CalculatorService
```

### <a name="client-configuration-file"></a>Fichier de configuration client

Une fois que vous avez créé le client, Visual Studio crée le **App.config** fichier de configuration dans le **GettingStartedClient** projet, qui doit être similaire à l’exemple suivant :

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
        <startup>
            <!-- specifies the version of WCF to use-->
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.6.1" />
        </startup>
        <system.serviceModel>
            <bindings>
                <!-- Uses wsHttpBinding-->
                <wsHttpBinding>
                    <binding name="WSHttpBinding_ICalculator" />
                </wsHttpBinding>
            </bindings>
            <client>
                <!-- specifies the endpoint to use when calling the service -->
                <endpoint address="http://localhost:8000/GettingStarted/CalculatorService"
                    binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_ICalculator"
                    contract="ServiceReference1.ICalculator" name="WSHttpBinding_ICalculator">
                    <identity>
                        <dns value="localhost" />
                    </identity>
                </endpoint>
            </client>
        </system.serviceModel>
    </configuration>
```

Sous le [ \<system.serviceModel >](../configure-apps/file-schema/wcf/system-servicemodel.md) section, notez le [ \<point de terminaison >](../configure-apps/file-schema/wcf/endpoint-element.md) élément. Le **&lt;point de terminaison&gt;** élément définit le point de terminaison que le client utilise pour accéder au service comme suit :
- Adresse : `http://localhost:8000/GettingStarted/CalculatorService`. Adresse du point de terminaison.
- Contrat de service : `ServiceReference1.ICalculator`. Le contrat de service gère la communication entre le client WCF et le service. Visual Studio a généré ce contrat lorsque vous avez utilisé son **ajouter une référence de Service** (fonction). Il est en fait une copie du contrat que vous avez défini dans le projet GettingStartedLib. 
- Liaison : <xref:System.ServiceModel.WSHttpBinding>. La liaison spécifie le protocole HTTP comme transport, sécurité interopérable et d’autres détails de configuration.

## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à :
> [!div class="checklist"]
> - Créez et configurez un projet d’application console pour le client WCF.
> - Ajouter une référence de service au service WCF pour générer les fichiers de configuration et de la classe proxy pour l’application cliente.

Passez au didacticiel suivant pour apprendre à utiliser le client généré.

> [!div class="nextstepaction"]
> [Tutoriel : Utiliser un client WCF](how-to-use-a-wcf-client.md)
