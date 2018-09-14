---
title: Délai durable en XAMLX
ms.date: 03/30/2017
ms.assetid: efc38df4-2d34-453c-8e59-2c21d1307354
ms.openlocfilehash: 1eef9211c67d190ecb5f329c481fa2e3d1763353
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45594094"
---
# <a name="durable-delay-in-xamlx"></a>Délai durable en XAMLX
Cet exemple montre comment utiliser un délai durable, qui est un délai rendant le workflow persistant sur un périphérique durable pendant le délai.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\DurableDelayXamlx`  
  
## <a name="discussion"></a>Discussion  
 L'exemple de workflow contient deux messages sur un fichier local qui sont séparés par un délai. Lorsque le délai est déclenché, le workflow est déchargé, et attend 5 secondes dans le magasin d'instances de workflow avant d'être rechargé en mémoire.  
  
 Le fichier .xamlx est un service de workflow est hébergé dans Visual Studio. Visual Studio utilise Cassini qui utilise un service de workflow hôte pour héberger le flux de travail.  
  
 En plus d'héberger le workflow, l'hôte de service de workflow gère les instances de workflow en les chargeant et en les déchargeant. Pour démarrer une instance de la définition de Windows Workflow Foundation (WF) (sur l’hôte de service de flux de travail), définissez un client qui envoie un message à la <xref:System.ServiceModel.Activities.Receive> activité dans le flux de travail. Ce <xref:System.ServiceModel.Activities.Receive> a sa propriété <xref:System.ServiceModel.Activities.Receive.CanCreateInstance%2A> qui a la valeur `true`, ce qui lui permet de créer une instance du workflow une fois qu'il reçoit un message.  
  
 Pendant l'initialisation, un comportement de déchargement d'instance est ajouté au fichier de configuration qui spécifie l'hôte de service de workflow sous lequel il doit décharger une instance dans le magasin de persistance (base de données). Pour cet exemple, il décharge l'instance immédiatement après le passage du workflow à l'état inactif (lorsque le délai est déclenché).  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Ouvrez une invite de commandes [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Naviguez jusqu'au dossier DurableDelayXamlx\CS.  
  
3.  Exécutez Setup.cmd.  
  
4.  Exécutez [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] en tant qu'administrateur.  
  
5.  Ouvrez le fichier solution DurableDelayXamlx.sln.  
  
6.  Dans **l’Explorateur de solutions**, avec le bouton droit de la solution et sélectionnez **propriétés**.  
  
7.  Sélectionnez **plusieurs projets de démarrage** et définissez les deux projets sur **Démarrer**.  
  
8.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
9. Pour exécuter la solution, appuyez sur Ctrl+F5.  
  
#### <a name="to-uninstall-this-sample"></a>Pour désinstaller cet exemple  
  
1.  Ouvrez une invite de commandes [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Naviguez jusqu'au dossier DurableDelayXamlx\CS.  
  
3.  Exécutez Cleanup.cmd.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\DurableDelayXamlX`
