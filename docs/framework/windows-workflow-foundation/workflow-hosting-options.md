---
title: Options d'hébergement de workflow
ms.date: 03/30/2017
ms.assetid: 37bcd668-9c5c-4e7c-81da-a1f1b3a16514
ms.openlocfilehash: 2a03c7b5e15b76eabc714f44624f04d3385720d4
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57713317"
---
# <a name="workflow-hosting-options"></a>Options d'hébergement de workflow
La plupart des exemples Windows Workflow Foundation (WF) utilisent des workflows hébergés dans une application console, mais ce n’est pas un scénario réaliste pour les workflows réels. Les workflows dans les applications d'entreprise réelles sont hébergés dans des processus persistants, un service Windows créé par le développeur ou une application serveur telle que [!INCLUDE[iisver](../../../includes/iisver-md.md)] ou AppFabric. Les différences entre ces approches sont les suivantes.  
  
## <a name="hosting-workflows-in-iis-with-windows-appfabric"></a>Hébergement de workflows dans IIS avec Windows AppFabric  
 IIS avec AppFabric est l'hôte par défaut pour les workflows. L'application hôte de workflows utilisant AppFabric est WAS (Windows Activation Services), qui supprime la dépendance de HTTP sur IIS uniquement.  
  
## <a name="hosting-workflows-in-iis-alone"></a>Hébergement de workflows dans IIS uniquement  
 Il n'est pas recommandé d'utiliser uniquement [!INCLUDE[iisver](../../../includes/iisver-md.md)], car il existe des outils de gestion et d'analyse disponibles avec AppFabric qui facilitent la maintenance des applications en cours d'exécution. Les workflows doivent être hébergés dans [!INCLUDE[iisver](../../../includes/iisver-md.md)] uniquement si vous rencontrez des problèmes d'infrastructure lors de la migration vers AppFabric.  
  
> [!WARNING]
>  [!INCLUDE[iisver](../../../includes/iisver-md.md)] recycle les pools d'applications régulièrement pour différentes raisons. Lorsqu'un pool d'applications est recyclé, IIS cesse de recevoir des messages de l'ancien pool, et instancie un pool d'applications pour recevoir de nouvelles demandes. Si un workflow continue de fonctionner après avoir envoyé une réponse, [!INCLUDE[iisver](../../../includes/iisver-md.md)] ne se rendra pas compte du travail effectué, et peut recycler le pool d'applications d'hébergement. Si cela se produit, le workflow s’interrompra, et des services de suivi enregistreront un [1004 - WorkflowInstanceAborted](1004-workflowinstanceaborted.md) message avec un champ de raison vide.  
>   
>  Si la persistance est utilisée, l'hôte doit explicitement redémarrer les instances interrompues à partir du dernier point de persistance.  
>   
>  Si AppFabric est utilisé, le service de gestion de workflow reprend en fin de compte le workflow à partir du dernier point correct de persistance si la persistance est utilisée. Si aucune persistance n'est utilisée, et le workflow exécute des opérations en dehors d'un modèle de requête/réponse, des données seront perdues lors de l'interruption du workflow.  
  
## <a name="hosting-a-workflow-in-a-custom-windows-service"></a>Hébergement d'un workflow dans un service Windows personnalisé  
 Créer un service de workflow personnalisé pour héberger le workflow nécessite que le développeur duplique nombre des fonctionnalités prêtes à l'emploi fournies par AppFabric, mais offre plus de souplesse avec des fonctionnalités personnalisées. Cette option ne doit être prise en compte que si AppFabric s'avère ne pas être une option.
