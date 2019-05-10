---
title: Action d'achèvement de l'instance
ms.date: 03/30/2017
ms.assetid: 90cc99d2-9fef-42fd-bcbf-a56917993721
ms.openlocfilehash: d68f41a586e44f96c9ca26cf8a142a2782adaa36
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64662975"
---
# <a name="instance-completion-action"></a>Action d'achèvement de l'instance
Le **Instance Completion Action** propriété du Store d’Instance de Workflow SQL vous permet de spécifier si les données et métadonnées d’instances de workflow sont supprimées à partir de la base de données de persistance une fois que les instances ont abouti. Les valeurs autorisées pour cette propriété sont **DeleteAll** et **DeleteNothing**. La liste suivante décrit ces trois options :  
  
- **DeleteAll (valeur par défaut).** Si la valeur de la propriété est définie sur DeleteAll, les données et métadonnées d'instances de workflow sont supprimées de la base de données de persistance après que les instances ont abouti.  
  
- **DeleteNothing.** Si la valeur de la propriété est définie sur DeleteNothing, les données et métadonnées d'instances de workflow sont conservées dans la base de données de persistance même après que les instances ont abouti.  
  
    > [!CAUTION]
    >  Garder les informations d'état de l'instance après que les instances ont abouti entraîne l'augmentation de la taille de la base de données de persistance. À mesure que la taille de la base de données augmente, les opérations de base de données que le sous-système de persistance effectue prennent plus de temps pour s'exécuter, donc vous devez régulièrement vider les informations d'état de l'instance de la base de données de persistance pour optimiser l'exécution de ces services.
