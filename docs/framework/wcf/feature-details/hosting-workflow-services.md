---
title: Hébergement de services de workflow
ms.date: 03/30/2017
ms.assetid: 2d55217e-8697-4113-94ce-10b60863342e
ms.openlocfilehash: 02d77b851dcd35108668ee6a42022e9721b84bd8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33491324"
---
# <a name="hosting-workflow-services"></a>Hébergement de services de workflow
Un service de workflow doit être hébergé pour pouvoir répondre aux messages entrants. Les services de workflow utilisent l'infrastructure de messagerie WCF et sont donc hébergés de manière similaire. Tels que les services WCF, les services de flux de travail peuvent être hébergés dans toute application managée, sous Internet Information Services (IIS), ou sous les services Internet (WAS, Windows Process Activation Services). De plus, les services de workflow peuvent être hébergés sous Windows Server App Fabric. Pour plus d’informations sur Windows Server AppFabric, consultez [documentation de Windows Server AppFabric](http://go.microsoft.com/fwlink/?LinkId=193037), [fonctionnalités d’hébergement AppFabric](http://go.microsoft.com/fwlink/?LinkId=196494), et [Concepts d’hébergement AppFabric](http://go.microsoft.com/fwlink/?LinkId=196495). Pour plus d’informations sur les différentes façons pour héberger WCF services voir [Services d’hébergement](../../../../docs/framework/wcf/hosting-services.md).  
  
## <a name="hosting-in-a-managed-application"></a>Hébergement dans une application managée  
 Pour héberger un service de workflow dans une application managée, utilisez la classe <xref:System.ServiceModel.Activities.WorkflowServiceHost>. Le constructeur <xref:System.ServiceModel.Activities.WorkflowServiceHost> vous permet de spécifier une instance singleton du service de workflow, une définition du service de workflow ou une activité qui utilise les activités de messagerie du workflow. Appel de <<!--zz xref:System.ServiceModel.Activities.WorkflowServiceHost.Open%2A--> `System.ServiceModel.Activities.WorkflowServiceHost.Open`>, le service commence à écouter les messages entrants.  
  
## <a name="hosting-under-iis-or-was"></a>Hébergement dans les services IIS ou WAS  
 Héberger un service de workflow dans les services IIS ou WAS implique de créer un répertoire virtuel et d'y placer les fichiers qui définissent le service et son comportement. Lors de l'hébergement d'un service de workflow dans les services IIS ou WAS, il existe plusieurs possibilités :  
  
-   Placez un fichier .xamlx définissant le service de workflow dans un répertoire virtuel IIS/WAS, ainsi qu'un fichier Web.config qui spécifie les comportements, les points de terminaison et d'autres éléments de configuration du service.  
  
-   Placez un fichier .xamlx définissant le service de workflow dans un répertoire virtuel IIS/WAS. Le fichier .xamlx spécifie les points de terminaison à exposer. Les points de terminaison sont spécifiés dans un élément `WorkflowService.Endpoints`, comme le montre l'exemple suivant.  
  
    ```xml  
    <WorkflowService xmlns="http://schemas.microsoft.com/netfx/2009/xaml/servicemodel"  xmlns:p1="http://schemas.microsoft.com/netfx/2009/xaml/activities" xmlns:sad="clr-namespace:System.Activities.Debugger;assembly=System.Activities" xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">  
      <WorkflowService.Endpoints>  
        <Endpoint ServiceContractName="IWorkFlowEchoService" AddressUri="">  
          <Endpoint.Binding>  
            <BasicHttpBinding />  
          </Endpoint.Binding>  
        </Endpoint>  
      </WorkflowService.Endpoints>  
    <!-- ... -->  
    </WorkflowService>  
    ```  
  
    > [!NOTE]
    >  Les comportements ne peuvent pas être spécifiés dans un fichier .xamlx ; vous devez donc utiliser un fichier Web.config si vous devez spécifier des paramètres de comportement.  
  
-   Placez un fichier .xamlx définissant le service de workflow dans un répertoire virtuel IIS/WAS. Placez également un fichier .svc dans le répertoire virtuel. Ce fichier .svc vous permet de spécifier une fabrique hôte de service Web personnalisée, d'appliquer le comportement personnalisé ou de charger la configuration à partir d'un emplacement personnalisé.  
  
-   Placez un assembly dans le répertoire virtuel IIS/WAS qui contient une activité utilisant les activités de messagerie WCF.  
  
 Un fichier .xamlx qui définit un service de workflow doit contenir un <`Service`> élément racine ou un élément racine contenant n’importe quel type dérivé de <xref:System.Workflow.ComponentModel.Activity>. Lors de l'utilisation du modèle Activité de [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], un fichier .xamlx est créé. Lors de l'utilisation du modèle Service de workflow WCF, un fichier .xamlx est créé.  
  
## <a name="hosting-workflow-services-under-windows-server-app-fabric"></a>Hébergement des services de workflow sous Windows Server App Fabric  
 L'hébergement d'un service de workflow sous Windows Server App Fabric est similaire à l'hébergement sous IIS/WAS. La seule différence est que Windows Server App Fabric est installé. Windows Server App Fabric fournit des outils qui sont ajoutés au Gestionnaire des services IIS, ainsi que des applets de commande powershell. Ces outils simplifient le déploiement, la gestion et le suivi des services de workflow et des services WCF. . Pour plus d’informations sur Windows Server AppFabric, consultez [Windows Server AppFabric](http://go.microsoft.com/fwlink/?LinkId=193037)  
  
## <a name="referencing-custom-activities"></a>Référencement d'activités personnalisées  
 Références à des activités personnalisées doivent être ajoutées à la <`Assemblies`> sous <`System.Web.Compilation`> afin qu’ils sont chargés dans le domaine d’Application et le désérialiseur XAML est en mesure de localiser les types. Ces paramètres peuvent être effectués au niveau de l'application ou dans le Web.config racine si les paramètres doivent s'appliquer à toutes les applications sur l'ordinateur.  
  
## <a name="deployment"></a>Déploiement  
 L'outil de déploiement Web a été créé pour simplifier le travail de déploiement. Cet outil vous permet de migrer des applications entre IIS 6.0 et IIS 7.0, de synchroniser des batteries de serveurs et d’empaqueter, d’archiver et de déployer des applications Web. Pour plus d’informations, consultez [outil de déploiement MS](http://go.microsoft.com/fwlink/?LinkId=178690)  
  
## <a name="see-also"></a>Voir aussi  
 [Éléments internes de l’hôte du service de workflow](../../../../docs/framework/wcf/feature-details/workflow-service-host-internals.md)  
 [Configuration de WorkflowServiceHost](../../../../docs/framework/wcf/feature-details/configuring-workflowservicehost.md)
