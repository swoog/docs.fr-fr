---
title: Activation basée sur la configuration
ms.date: 03/30/2017
ms.assetid: 21bb762e-c43e-4b0c-887b-5e434d665838
ms.openlocfilehash: e016dffdaf93b222c1fd2380bfa175256b009068
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44188304"
---
# <a name="configuration-based-activation"></a>Activation basée sur la configuration
Cet exemple montre comment activer les services Windows Communication Foundation (WCF) sans avoir besoin d’un fichier .svc.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\Hosting\ConfigBasedActivation`  
  
## <a name="sample-details"></a>Détails de l'exemple  
 Dans cet exemple, le client est le client test WCF, et le service est hébergé dans IIS.  
  
> [!NOTE]
>  Les instructions d'installation et de génération correspondant à cet exemple figurent en fin de rubrique.  
  
### <a name="activation-of-services-without-requiring-a-svc-file"></a>Activation de services sans avoir à utiliser de fichier .svc  
 Dans [!INCLUDE[netfx35_short](../../../../includes/netfx35-short-md.md)], un fichier .svc était requis pour activer un service. Cela générait une charge de gestion supplémentaire, en raison du déploiement et de la maintenance nécessaires d'un fichier supplémentaire avec l'application. Avec le lancement de [!INCLUDE[netfx40_long](../../../../includes/netfx40-long-md.md)], les composants d'activation peuvent être configurés à l'aide du fichier de configuration de l'application.  
  
 [!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)] introduit un nouvel élément de configuration (<xref:System.ServiceModel.Configuration.ServiceActivationElement>), dans le <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection> du fichier de configuration de l'application. La collection <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection> accepte une collection de services à activer, comme le montre l'exemple de code suivant.  
  
```xml  
<serviceActivations>  
   <add relativeAddress="Calculator.svc" service="Microsoft.ServiceModel.Samples.CalculatorService" />  
  
<serviceActivations>  
```  
  
 L'observation à formuler est que la configuration semble très similaire à celle de fichiers .svc. Un attribut supplémentaire, `relativeAddress`, qui fournit l'adresse du service, a été introduit. L’adresse relative constitue également le chemin d’accès virtuel du service. L'hôte récupère le fichier Web.config du fichier à partir de l'emplacement `virtualPath`, s'il existe ; sinon, l'hôte effectue une recherche récursive dans son dossier parent.  
  
> [!NOTE]
>  Pour fonctionner, cet exemple requiert un hébergement dans IIS.  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  À l'aide de [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], ouvrez le fichier Service.csproj.  
  
2.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
3.  Testez le service en exécutant WCFTestClient.exe.  
  
4.  À l'aide de l'[!INCLUDE[fileExplorer](../../../../includes/fileexplorer-md.md)], naviguez jusqu'au dossier %SystemDrive%\Program Files\Microsoft Visual Studio 10.0\Common7\IDE.  
  
5.  Exécutez WcfTestClient.exe.  
  
6.  Définissez l'adresse MEX du service.  
  
7.  Appuyez sur CTRL+MAJ+A pour définir l'adresse du service.  
  
8.  La valeur est l’adresse http://localhost/ServiceModelSamples/Calculator.svc.  
  
9. Effectuez l'opération `Add`. Affectez au paramètre `n1` la valeur 10 et au paramètre `n2` la valeur 15.  
  
10. Appuyez sur **appeler**.  
  
     Le résultat attendu est 25.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2.  Pour générer l’édition C# ou Visual Basic .NET de la solution, conformez-vous aux instructions figurant dans [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
3.  Une fois la solution générée, exécutez Setup.bat pour installer l'application ServiceModelSamples dans IIS. Le répertoire ServiceModelSamples doit maintenant apparaître en tant qu'application IIS.  
  
4.  Pour exécuter l’exemple dans une configuration unique ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Hébergement AppFabric et exemples de persistance](https://go.microsoft.com/fwlink/?LinkId=193961)
