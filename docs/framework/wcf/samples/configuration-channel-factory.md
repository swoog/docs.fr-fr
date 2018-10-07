---
title: Configuration Channel Factory
ms.date: 03/30/2017
ms.assetid: 3b749493-bd8a-4ccb-893e-5948901a1486
ms.openlocfilehash: b5dbabf8cdc28cc2beaf343b0377528c6ced1c66
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2018
ms.locfileid: "48846290"
---
# <a name="configuration-channel-factory"></a>Configuration Channel Factory
Cet exemple couvre l'utilisation du <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601>. Le <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> permet une gestion centralisée de la configuration de client WCF. Celle-ci peut également être utile dans les scénarios où la configuration est sélectionnée ou modifiée après le chargement du domaine d'application.

## <a name="demonstrates"></a>Démonstrations
 <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601>

## <a name="discussion"></a>Discussion
 Cet exemple montre comment utiliser <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> pour ajouter un fichier de configuration particulier à une application cliente, sans avoir à utiliser le fichier de configuration de l'application par défaut.

 Cet exemple est composé de deux projets. Le premier projet est un service simple qui s'exécute pour répondre aux messages provenant des clients. Le deuxième projet est une application cliente qui génère deux objets <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> à l'aide d'un <xref:System.Configuration.ExeConfigurationFileMap> pour le fichier de configuration Test.config et les utilise pour communiquer avec le service. Les deux clients communiquent avec le service à l'aide de la configuration spécifiée dans Test.config.

 Le code suivant ajoute un fichier de configuration personnalisé à une application cliente.

```
ExeConfigurationFileMap fileMap = new ExeConfigurationFileMap();
fileMap.ExeConfigFilename = "Test.config";
Configuration newConfiguration = ConfigurationManager.OpenMappedExeConfiguration(fileMap, ConfigurationUserLevel.None);

ConfigurationChannelFactory<ICalculatorChannel> factory1 = new ConfigurationChannelFactory<ICalculatorChannel>("endpoint1", newConfiguration, new EndpointAddress("http://localhost:8000/servicemodelsamples/service"));
ICalculatorChannel client1 = factory1.CreateChannel();
```

#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple

1.  Ouvrez Visual Studio 2012 avec des privilèges d’administrateur.

2.  Avec le bouton droit de la solution ConfigurationChannelFactory (2 projets), puis sélectionnez **propriétés**.

3.  Dans **propriétés communes**, sélectionnez **projet de démarrage**, puis cliquez sur **plusieurs projets de démarrage**.

4.  Déplacer le **Service** de projet vers le début de la liste, avec la **Action 'Start'**, puis déplacez le **Client** projet après la **Service**projet, également avec la **Action 'Start'**, la **Client** projet est exécuté après la **Service** projet.

5.  Cliquez sur **OK**, puis appuyez sur F5 (ou CTRL + F5) pour exécuter l’exemple.

> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\ConfigurationChannelFactory`
