---
title: Extending Tracing
ms.date: 03/30/2017
ms.assetid: 2b971a99-16ec-4949-ad2e-b0c8731a873f
ms.openlocfilehash: 59291b6a57ba602e5fea84dcd571a8d767b7cc04
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2018
ms.locfileid: "33806807"
---
# <a name="extending-tracing"></a>Extending Tracing
Cet exemple montre comment étendre la fonctionnalité de traçage de Windows Communication Foundation (WCF) en écrivant les suivis d’activité définis par l’utilisateur dans le code client et le service. Cela permet à l'utilisateur de créer des activités de suivi et de regrouper les suivis dans des unités de travail logiques. Il est également possible de mettre en corrélation des activités à travers des transferts (au sein du même point de terminaison) et la propagation (sur plusieurs points de terminaison). Dans cet exemple, le suivi est activé à la fois pour le client et pour le service. Pour plus d’informations sur la façon d’activer le suivi dans les fichiers de configuration client et le service, consultez [Tracing and Message Logging](../../../../docs/framework/wcf/samples/tracing-and-message-logging.md).  
  
 Cet exemple est basé sur le [mise en route](../../../../docs/framework/wcf/samples/getting-started-sample.md).  
  
> [!NOTE]
>  La procédure d'installation ainsi que les instructions de génération correspondant à cet exemple figurent en fin de rubrique.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Management\ExtendingTracing`  
  
## <a name="tracing-and-activity-propagation"></a>Suivi et propagation d'activité  
 Le suivi d’activité définis par l’utilisateur permet à l’utilisateur créer leurs propres activités de suivi pour grouper des suivis dans des unités logiques de travail, de mettre en corrélation les activités par transfert et propagation et de réduire le coût de performances de suivi WCF (par exemple, l’espace disque de coût d’un fichier journal).  
  
### <a name="adding-custom-sources"></a>Ajout de sources personnalisées  
 Les suivis définis par l'utilisateur peuvent être ajoutés à la fois au code du client et du service. Ajout de sources de suivi pour les fichiers de configuration client ou un service permettant à ces traces personnalisées à être enregistré et affiché dans le [outil Service Trace Viewer (SvcTraceViewer.exe)](../../../../docs/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe.md). Le code suivant montre comment ajouter une source de suivi définie par l'utilisateur nommée `ServerCalculatorTraceSource` au fichier de configuration.  
  
```xml  
<system.diagnostics>  
    <sources>  
        <source name="System.ServiceModel" switchValue="Warning" propagateActivity="true">  
            <listeners>  
                <add type="System.Diagnostics.DefaultTraceListener" name="Default">  
                    <filter type="" />  
                </add>  
                <add name="xml">  
                    <filter type="" />  
                </add>  
            </listeners>  
        </source>  
        <source name="ServerCalculatorTraceSource" switchValue="Information,ActivityTracing">  
            <listeners>  
                <add type="System.Diagnostics.DefaultTraceListener" name="Default">  
                    <filter type="" />  
                </add>  
                <add name="xml">  
                    <filter type="" />  
                </add>  
            </listeners>  
        </source>  
    </sources>  
    <sharedListeners>  
       <add initializeData="C:\logs\ServerTraces.svclog" type="System.Diagnostics.XmlWriterTraceListener"  
        name="xml" traceOutputOptions="Callstack">  
            <filter type="" />  
        </add>  
    </sharedListeners>  
    <trace autoflush="true" />  
</system.diagnostics>....  
....  
```  
  
### <a name="correlating-activities"></a>Mise en corrélation des activités  
 Pour mettre directement en corrélation des activités sur plusieurs points de terminaison, l'attribut `propagateActivity` doit avoir la valeur `true` dans la source du suivi `System.ServiceModel`. En outre, pour propager des suivis sans traverser des activités de WCF, suivi d’activité ServiceModel doit être désactivé. C'est ce qu'illustre l'exemple de code suivant.  
  
> [!NOTE]
>  La désactivation du suivi d'activité ServiceModel n'équivaut pas à désactiver le niveau de suivi, dénoté par la propriété `switchValue`.  
  
```xml  
<system.diagnostics>  
    <sources>  
      <source name="System.ServiceModel" switchValue="Warning" propagateActivity="true">  
  
    ...  
  
       </source>  
    </sources>  
</system.diagnostics>  
```  
  
### <a name="lessening-performance-cost"></a>Réduction des coûts de performance  
 Le fait de désactiver `ActivityTracing` dans la source de suivi `System.ServiceModel` génère un fichier de suivi qui contient uniquement les suivis d'activité définis par l'utilisateur, sans inclure les suivis d'activité ServiceModel. Ainsi, le fichier journal est beaucoup moins volumineux. Toutefois, la possibilité de mettre en corrélation les suivis de traitement de WCF est perdue.  
  
##### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Assurez-vous d’avoir effectué la [procédure d’installation d’à usage unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2.  Pour générer l’édition C# ou Visual Basic .NET de la solution, conformez-vous aux instructions figurant dans [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
3.  Pour exécuter l’exemple dans une configuration à un ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Exemples d’analyse AppFabric](http://go.microsoft.com/fwlink/?LinkId=193959)
