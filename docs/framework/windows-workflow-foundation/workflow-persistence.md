---
title: Persistance du workflow
ms.date: 03/30/2017
helpviewer_keywords:
- programming [WF], persistence
ms.assetid: 39e69d1f-b771-4c16-9e18-696fa43b65b2
ms.openlocfilehash: db0e4acc76f758004948857fc0b23a9cbc62f244
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57715540"
---
# <a name="workflow-persistence"></a>Persistance du workflow
La persistance de workflow est la capture durable de l'état d'une instance de workflow, indépendamment des informations sur le processus ou l'ordinateur. Cela permet d'abord de fournir, en cas de défaillance du système, un point connu de récupération de l'instance de workflow. Ensuite, la mémoire est conservée en déchargeant les instances de workflow qui ne fonctionnent pas activement. Enfin, l'état de l'instance de workflow peut être déplacé d'un nœud vers un autre dans une batterie de serveurs.  
  
 La persistance permet l'agilité de processus, l'évolutivité, la récupération en cas de défaillance et la capacité de gérer la mémoire plus efficacement. Le processus de persistance inclut l'identification d'un point de persistance, la collecte des données à enregistrer et enfin, la délégation de la mémoire physique des données à un fournisseur de persistance.  
  
 Pour activer la persistance pour un flux de travail, vous devez associer un magasin d’instances avec le **WorkflowApplication** ou **WorkflowServiceHost** comme indiqué dans [Comment : Activer la persistance pour les Workflows et les Services de flux de travail](how-to-enable-persistence-for-workflows-and-workflow-services.md). Le **WorkflowApplication** et **WorkflowServiceHost** permet d’activer des instances de workflow persistantes dans un magasin de persistance et le chargement des instances de workflow dans le magasin d’instances qui s’y rapportent mémoire selon les données d’instance de workflow stockées dans le magasin de persistance.  
  
 Le [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] est livré avec le **SqlWorkflowInstanceStore** (classe), qui autorise la persistance des données et des métadonnées sur les instances de workflow dans une base de données SQL Server 2005 ou SQL Server 2008. Consultez [SQL Workflow Instance Store](sql-workflow-instance-store.md) pour plus d’informations.  
  
 Pour stocker et charger vos données spécifiques à l'application, ainsi que les informations sur l'instance de workflow, vous pouvez créer des participants de persistance qui étendent la classe <xref:System.Activities.Persistence.PersistenceParticipant>. Un participant de persistance participe au processus de persistance pour les fins suivantes : enregistrer des données sérialisables personnalisées dans le magasin de persistance ; charger des données, du magasin d’instances vers la mémoire ; et effectuer toute logique supplémentaire dans le cadre d’une transaction de persistance. Pour plus d’informations, consultez [Participants de persistance](persistence-participants.md).  
  
 Windows Server AppFabric simplifie le processus de configuration de la persistance. Pour plus d’informations, consultez [Concepts de persistance avec Windows Server AppFabric](https://go.microsoft.com/fwlink/?LinkId=201200)  
  
## <a name="implicit-persistence-points"></a>Points de persistance implicites  
 La liste suivante comprend des exemples de conditions selon lesquelles un workflow est rendu persistant, lors de l'association d'un magasin d'instances à un workflow.  
  
-   Quand un **TransactionScope** activité est terminée ou un **TransactedReceiveScope** activité est terminée.  
  
-   Lorsqu’une instance de workflow devienne inactive et **WorkflowIdleBehavior** est défini sur l’hôte de flux de travail. Cela se produit, par exemple, lorsque vous utilisez des activités de messagerie ou un **délai** activité.  
  
-   Lorsqu’un WorkflowApplication devient inactif et le **PersistableIdle** propriété de l’application est définie sur **PersistableIdleAction.Persist**.  
  
-   Lorsqu'une application hôte a pour instruction de rendre persistante ou de décharger une instance de workflow.  
  
-   Lorsqu'une instance de workflow est arrêtée ou prend fin.  
  
-   Quand un **Persist** activité s’exécute.  
  
-   Lorsqu'une instance d'un workflow développé à l'aide d'une version précédente de Windows Workflow Foundation rencontre un point de persistance lors de l'exécution interopérable.  
  
## <a name="in-this-section"></a>Dans cette section  
  
-   [Magasin d’instances de workflow SQL](sql-workflow-instance-store.md)  
  
-   [Magasins d’instances](instance-stores.md)  
  
-   [Participants de persistance](persistence-participants.md)  
  
-   [Bonnes pratiques sur la persistance](persistence-best-practices.md)  
  
-   [Instances de workflow non persistantes](non-persisted-workflow-instances.md)  
  
-   [Suspension et reprise d’un workflow](pausing-and-resuming-a-workflow.md)
