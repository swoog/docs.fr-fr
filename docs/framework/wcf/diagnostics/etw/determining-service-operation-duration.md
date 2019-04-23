---
title: Détermination de la durée d'une opération de service
ms.date: 03/30/2017
ms.assetid: e8a93a2c-2c20-48b3-8986-57e90e9aa908
ms.openlocfilehash: fd7dec5784f50a0613b574822a31202a859b34c6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59772769"
---
# <a name="determining-service-operation-duration"></a>Détermination de la durée d'une opération de service
Si le traçage analytique est activé dans une application Windows Communication Foundation (WCF), la durée d’exécution d’une opération de service peut facilement être déterminée en examinant le journal des événements.  Cette rubrique montre comment déterminer la durée d'exécution d'une opération de service.  
  
### <a name="determining-service-operation-execution-duration"></a>Détermination de la durée d'exécution d'une opération de service  
  
1. Ouvrez l’Observateur d’événements en cliquant sur **Démarrer**, **exécuter**et en entrant `eventvwr.exe`.  
  
2. Si vous n’avez pas activé le traçage analytique, développez **journaux des Applications et Services**, **Microsoft**, **Windows**, **serveur d’applications-Applications** . Sélectionnez **vue**, **afficher analytiques et les journaux de débogage**. Avec le bouton droit **analyse** et sélectionnez **activer le journal**. Laissez l'Observateur d'événements ouvert afin que les traces soient visibles après l'exécution de l'opération de service.  
  
3. Ensuite, ouvrez une application WCF qui inclut un projet de service et un projet de client qui interagit avec ce service.  Vous pouvez créer une telle application en suivant le [Getting Started Tutorial](../../../../../docs/framework/wcf/getting-started-tutorial.md).  Si vous avez les exemples WCF installés, vous pouvez ouvrir le [mise en route](../../../../../docs/framework/wcf/samples/getting-started-sample.md), qui contient le projet terminé créé dans le didacticiel.  
  
4. Exécutez l’application serveur en appuyant sur **F5**. Exécuter l’application cliente en cliquant sur le **Client** projet et en sélectionnant **déboguer**, **démarrer une nouvelle Instance**.  
  
5. Dans l'Observateur d'événements, actualisez le journal Analyse et triez les événements par ID d'événement.  Recherchez les événements dont l’ID d’événement [214 - OperationCompleted](../../../../../docs/framework/wcf/diagnostics/etw/214-operationcompleted.md).  Ces événements affichent les opérations terminées et leur durée.  L'événement suivant affiche la durée d'une opération d'ajout.  
  
    ```Output  
    An OperationInvoker completed the call to the 'Add' method.  The method call duration was '3' ms.  
    ```
