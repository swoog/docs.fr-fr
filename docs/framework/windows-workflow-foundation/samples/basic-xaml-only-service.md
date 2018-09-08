---
title: Service uniquement en XAML de base
ms.date: 03/30/2017
ms.assetid: c106feb0-0245-43b5-aefe-93ce0e4d38eb
ms.openlocfilehash: f4f296a97b9c3093874c5ec8e05023e84b0af44a
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44196970"
---
# <a name="basic-xaml-only-service"></a>Service uniquement en XAML de base
Cet exemple montre comment créer un service uniquement en XAML. Le scénario est un service de diagnostic pour les problèmes liés à la voiture. Le service est implémenté comme un workflow qui pose une série de questions au client afin de diagnostiquer le problème. Il existe deux types de problèmes que le service peut diagnostiquer (la voiture ne démarre pas ou l'air conditionné ne fonctionne pas). Le workflow utilise le modèle Demande/réponse du concepteur pour exposer trois opérations de service simples. Le service est hébergé dans IIS en créant un répertoire virtuel dans IIS et en copiant le service1.xamlx et les fichiers Web.config dans le répertoire virtuel ; aucun code compilé n'est requis. Par défaut cet exemple copie automatiquement les fichiers nécessaires dans le répertoire virtuel créé lorsque vous suivez les instructions d’installation pour les exemples WCF et WF : [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md) lors de la génération dans Visual Studio 2010.  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Chargez la solution du projet dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] et générez le projet.  
  
2.  Exécutez l'application cliente générée dans [répertoire de base de la solution]\Client\bin\debug.  
  
3.  L'application imprime les options, sélectionne une option. L'application pose ensuite des questions, répondez-y par oui ou non (à l'aide des touches O/N). Lorsque le service a terminé le diagnostic des problèmes, l'application imprime un diagnostic.  
  
4.  L'application revient aux options. Vous pouvez diagnostiquer un autre problème ou quitter l'application.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\XAMLService`