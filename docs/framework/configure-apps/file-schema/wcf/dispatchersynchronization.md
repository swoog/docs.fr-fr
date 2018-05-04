---
title: '&lt;dispatcherSynchronization&gt;'
ms.date: 03/30/2017
ms.assetid: cc030f9c-4e38-4b14-94dc-9a0e41ec8e2d
ms.openlocfilehash: 34c12a05ee363df6b6cfc9ff3809bab50ee8d522
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltdispatchersynchronizationgt"></a>&lt;dispatcherSynchronization&gt;

Spécifie un comportement de point de terminaison qui permet à un service d'envoyer des réponses de manière asynchrone.

\<system.serviceModel > \<comportements > \<endpointBehaviors > \<comportement >

## <a name="syntax"></a>Syntaxe

```xml
<dispatcherSynchronizationBehavior asynchronousSendEnabled="Boolean" 
                                   maxPendingReceives="Integer" />
```

## <a name="type"></a>Type

`Type`

## <a name="attributes-and-elements"></a>Attributs et éléments

Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.

### <a name="attributes"></a>Attributs

| Attribut               | Description       |
| ----------------------- | ----------------- |
| asynchronousSendEnabled | Valeur booléenne qui indique si un comportement d'envoi asynchrone est activé. |
| `maxPendingReceives`    | Entier qui spécifie le nombre de réceptions simultanées qui peuvent être émises sur le canal.<br /><br /> Cette valeur doit être configurée uniquement après avoir correctement configuré le comportement de limitation de service. |

### <a name="child-elements"></a>Éléments enfants

Aucun.

### <a name="parent-elements"></a>Éléments parents

| Élément | Description |  
| ------- | ----------- |  
| [\<behavior>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|Spécifie un comportement de point de terminaison. |

## <a name="see-also"></a>Voir aussi

 <xref:System.ServiceModel.Configuration.DispatcherSynchronizationElement> <xref:System.ServiceModel.Description.DispatcherSynchronizationBehavior>
