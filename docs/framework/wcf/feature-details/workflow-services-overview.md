---
title: Vue d’ensemble des services de flux de travail - WCF
ms.date: 03/30/2017
ms.assetid: e536dda3-e286-441e-99a7-49ddc004b646
ms.openlocfilehash: 5d5f8636bec57cee1cb72c2796fc4bafc6b9c044
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65590074"
---
# <a name="workflow-services-overview"></a>Vue d’ensemble des services de workflow

Services de workflow sont des services WCF qui sont implémentées à l’aide de flux de travail. Services de workflow sont des workflows qui utilisent les activités de messagerie pour envoyer et recevoir des messages Windows Communication Foundation (WCF). .NET Framework 4.5 introduit plusieurs activités de messagerie qui vous permettent d'envoyer et de recevoir des messages à partir d'un workflow. Pour plus d’informations sur la messagerie des activités et comment ils peuvent être utilisés pour implémenter des modèles d’échange de messages différents, consultez [activités de messagerie](messaging-activities.md).

## <a name="benefits-of-using-workflow-services"></a>Avantages de l’utilisation des services de workflow

Les applications étant de plus en plus distribuées, les services individuels sont désormais chargés d'appeler d'autres services pour alléger en partie la tâche. Implémenter ces appels en tant qu'opérations asynchrones rend le code plus complexe. La gestion des erreurs ajoute une complexité supplémentaire, sous la forme d'une gestion des exceptions et de la fourniture d'informations de suivi détaillées. Certains services ont souvent une durée d'exécution longue et peuvent consommer de précieuses ressources système à attendre une entrée. En raison de ces problèmes, les applications distribuées sont souvent très complexes, difficiles à écrire et à maintenir. Les workflows constituent une méthode naturelle pour exprimer la coordination de travail asynchrone, notamment les appels aux services externes. Les workflows sont également efficaces pour représenter des processus d'entreprise de longue durée. Ces qualités font du workflow une ressource importante pour la construction de services dans un environnement distribué.

## <a name="implementing-a-workflow-service"></a>Implémentation d’un service de flux de travail

Lorsque vous implémentez un service WCF, vous définissez plusieurs contrats qui décrivent le service et les données qu’il envoie et reçoit. Les données sont représentées en tant que contrats de données et contrats de message. Les services WCF et les services de workflow utilisent tous des définitions de contrat de données et de contrat de message dans le cadre des descriptions du service. Le service lui-même expose des métadonnées (au format WSDL) pour décrire les opérations du service. Dans WCF, les contrats de service et les contrats d'opération définissent le service et les opérations qu'il prend en charge. Toutefois dans un service de workflow, ces contrats font partie du processus d'entreprise lui-même. Ils sont exposés dans les métadonnées par un processus appelé l'inférence de contrat. Lorsqu'un service de workflow est hébergé à l'aide d'un objet <xref:System.ServiceModel.Activities.WorkflowServiceHost>, la définition du workflow est examinée et un contrat est généré en fonction du jeu d'activités de messagerie qui se trouvent dans le workflow. Plus particulièrement, les activités et les propriétés suivantes sont utilisées pour générer le contrat :

Activité <xref:System.ServiceModel.Activities.Receive>

- <xref:System.ServiceModel.Activities.Receive.ServiceContractName%2A>

- <xref:System.ServiceModel.Activities.Receive.OperationName%2A>

- <xref:System.ServiceModel.Activities.Receive.Action%2A>

Activité <xref:System.ServiceModel.Activities.SendReply>

- <xref:System.ServiceModel.Activities.SendReply.Action%2A>

Activité <xref:System.ServiceModel.Activities.TransactedReceiveScope>

Le résultat final de l’inférence de contrat est une description du service à l’aide des mêmes structures de données en tant que services WCF et les contrats d’opération. Puis ces informations sont utilisées pour exposer WSDL pour le service de workflow.

> [!NOTE]
> [!INCLUDE[netfx_current_short](../../../../includes/netfx-current-short-md.md)] ne vous permet pas d'écrire des services de workflow à l'aide d'une définition de contrat existante, sans une prise en charge d'outils supplémentaires. Les contrats du service de workflow sont créés par le processus d'inférence de contrat présenté précédemment. Les contrats de message et les contrats de données sont toutefois entièrement pris en charge.

## <a name="workflow-services-and-msmq-based-bindings"></a>Services de workflow et liaisons basées sur MSMQ

WCF définit deux liaisons <xref:System.ServiceModel.NetMsmqBinding> et <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding> basées sur MSMQ.  Les liaisons basées sur MSMQ sont souvent utilisées avec les services de workflow en raison de la longue durée d’exécution de ces services. Les liaisons basées sur MSMQ ont une propriété `ValidityDuration` qui spécifie comment de temps les messages MSMQ peuvent supposer être valides. En raison de la longue durée d'exécution des services de workflow, il est possible que la durée de validité d'un message MSMQ expire avant que le service de workflow puisse le traiter. Il est donc très important d’affecter une valeur appropriée à la durée de validité d’une liaison MSMQ. Cette valeur doit être choisie en fonction du workflow et de sa manière de traiter les messages. Par exemple si vous avez un workflow avec une activité <xref:System.ServiceModel.Activities.Receive> suivie d'une activité personnalisée qui s'exécute pendant 10 minutes, elle-même suivie d'une autre activité <xref:System.ServiceModel.Activities.Receive>, la valeur correcte pour `ValidityDuration` doit être supérieure à 10 minutes.

## <a name="hosting-a-workflow-service"></a>Hébergement d’un service de flux de travail

Comme les services WCF, les services de workflow doivent être hébergés. Services WCF utilisent le <xref:System.ServiceModel.ServiceHost> classe pour héberger des services et de flux de travail services utilisent <xref:System.ServiceModel.Activities.WorkflowServiceHost> pour héberger les services. Tels que les services WCF, services de workflow peuvent être hébergés dans un de différentes façons, par exemple :

- Dans une application .NET Framework managée.

- Dans les Services IIS (Internet Information Services).

- dans le service d'activation des processus Windows (WAS, Windows Process Activation Service) ;

- dans un service Windows managé.

Services de workflow hébergés dans une application .NET Framework managée ou un service Windows managé créer une instance de la <xref:System.ServiceModel.Activities.WorkflowServiceHost> classe et lui transmettent une instance de la <xref:System.ServiceModel.Activities.WorkflowService> qui contient la définition de flux de travail dans le <xref:System.ServiceModel.Activities.WorkflowService.Body%2A> propriété. Une définition de workflow contenant des activités de messagerie est exposée en tant que service de workflow.

Pour héberger un service de workflow dans les services IIS ou WAS, placez dans un répertoire virtuel le fichier .xamlx qui contient la définition du service de workflow. Un point de terminaison par défaut (à l’aide de <xref:System.ServiceModel.BasicHttpBinding>) est créé automatiquement pour plus d’informations, consultez [Simplified Configuration](../../../../docs/framework/wcf/simplified-configuration.md). Vous pouvez également placer un fichier Web.config dans le répertoire virtuel pour spécifier vos propres points de terminaison. Si votre définition de workflow se trouve dans un assembly, vous pouvez placer un fichier .svc dans le répertoire virtuel et l'assembly de workflow dans le répertoire App_Code. Le fichier .svc doit spécifier la fabrique hôte de service et la classe qui implémente le service de workflow. L'exemple suivant montre comment spécifier la fabrique hôte de service et la classe qui implémente le service de workflow.

```
<%@ServiceHost Factory=" System.ServiceModel.Activities.Activation.WorkflowServiceHostFactory
Service="EchoService"%>
```
