---
title: Sécurisation des services de workflow
ms.date: 03/30/2017
ms.assetid: 53f84ad5-1ed1-4114-8d0d-b12e8a021c6e
ms.openlocfilehash: 28c34ecf7d6d781bfa461b2737cb9325a657f47e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43524333"
---
# <a name="securing-workflow-services"></a>Sécurisation des services de workflow
L'exemple de service de workflow sécurisé présente les procédures suivantes :  
  
-   Création d'un service de workflow de base à l'aide des activités <xref:System.ServiceModel.Activities.Receive> et <xref:System.ServiceModel.Activities.SendReply>.  
  
-   À l’aide de configuration de Windows Communication Foundation (WCF) pour définir des points de terminaison sécurisés pour une utilisation par le service de workflow.  
  
-   Création de revendications à l'intérieure d'une stratégie personnalisée et utilisation de <xref:System.ServiceModel.ServiceAuthorizationManager> pour valider les revendications.  
  
## <a name="demonstrates"></a>Démonstrations  
 Utilisation de la sécurité WCF pour sécuriser la communication entre le client et service de workflow. Autorisation basée sur des revendications  
  
## <a name="discussion"></a>Discussion  
 Cet exemple illustre l’utilisation de l’infrastructure de sécurité WCF pour sécuriser un service de flux de travail comme vous le feriez avec un service WCF normal. Plus particulièrement, il utilise une revendication personnalisée pour spécifier l'autorisation. Dans ce cas, il utilise <xref:System.ServiceModel.WSHttpBinding> et la sécurité en mode de message avec les informations d'identification Windows.  
  
 L'<xref:System.IdentityModel.Policy.IAuthorizationPolicy> personnalisé (`CustomNameCheckerPolicy`) vérifie le nom d'utilisateur Windows du client et recherche un caractère spécifique. Si ce caractère est présent, il crée et ajoute la revendication à <xref:System.IdentityModel.Policy.EvaluationContext>. Ainsi, la stratégie personnalisée établit le constat selon lequel le nom d'utilisateur du client contient ce caractère. Cette revendication peut être faire l'objet d'une requête pendant toute la durée de vie de l'appel. Vous trouverez ce caractère dans `Constants.cs`.  
  
 La stratégie d'autorisation recherche la revendication à l'intérieur de `SecureWorkFlowAuthZManager`. Si elle le trouve, elle retourne `true` et autorise le workflow à continuer. Sinon, elle retourne `false`, ce qui entraîne le retour d'un message 'Accès refusé' au client. D'autres revendications sont présentes dans le contexte et peuvent également être examinées à l'intérieur de `SecureWorkFlowAuthZManager`.  
  
#### <a name="to-run-this-sample"></a>Pour exécuter cet exemple  
  
1.  Exécutez [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] avec des privilèges d'administrateur.  
  
2.  Chargez SecuringWorkflowServices.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
3.  Pour compiler la solution, appuyez sur Ctrl+Maj+B.  
  
4.  Définissez le projet Service comme projet de démarrage pour la solution.  
  
5.  Appuyez sur CTRL+F5 pour démarrer le service sans débogage.  
  
6.  Définissez le projet Client comme projet de démarrage pour la solution.  
  
7.  Appuyez sur CTRL+F5 pour démarrer le client sans débogage.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\Services\SecuringWorkflowServices`
