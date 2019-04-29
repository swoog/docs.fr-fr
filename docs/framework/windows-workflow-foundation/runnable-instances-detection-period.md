---
title: Période de détection des instances activables
ms.date: 03/30/2017
ms.assetid: 4ea5c787-b638-47fd-bfc8-ede8c2898ce6
ms.openlocfilehash: 9652dd811f64e5324219b8aa0700ab8219edeeb0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61937954"
---
# <a name="runnable-instances-detection-period"></a>Période de détection des instances activables
Le magasin d’instances de workflow SQL exécute une tâche interne qui se réveille régulièrement et détecte les instances exécutables ou activables dans la base de données de persistance. Le **période de détection des Instances exécutables** propriété du Store d’Instance de Workflow SQL spécifie la période de temps après lequel le Store d’Instance de Workflow SQL exécute une tâche de détection pour détecter tout workflow exécutable ou activable instances dans la base de données de persistance issue du cycle de détection précédent.  
  
 La définition d'un intervalle plus court pour cette propriété réduit le délai entre l'expiration d'un minuteur associé à une instance de workflow et la signalisation de l'événement, ainsi que le chargement subséquent de l'instance. Toutefois, cela augmente également la charge de traitement sur un hôte et peut ne pas être souhaitable dans les scénarios où les minuteurs durables et/ou les échecs d'hôte sont rares. La propriété possède le type TimeSpan et sa valeur suit le format : hh:mm:ss. La valeur minimale de cette propriété est 00:00:01 et sa valeur par défaut 00:00:05.  
  
 Pour plus d’informations, détection et activation d’instances de workflow exécutables et activables, consultez [activation d’Instance](instance-activation.md).
