---
title: '&lt;namespaceTable&gt;'
ms.date: 03/30/2017
ms.assetid: 64801766-01b7-4c65-9ce6-70ad5af67689
ms.openlocfilehash: 55b5565ffe9d3e9e7ea41d2a2e2f380490be1781
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151421"
---
# <a name="ltnamespacetablegt"></a>&lt;namespaceTable&gt;

Représente une section de configuration qui permet de définir un ensemble d’éléments contenant des mappages espace de noms-préfixe qui peuvent ensuite être utilisés dans des filtres XPath pour le routage.

**\<system.serviceModel >**   
&nbsp;&nbsp;**\<routage >**   
&nbsp;&nbsp;&nbsp;&nbsp;**\<namespaceTable >**
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.serviceModel>
  <routing>
    <namespaceTable>
      <add namespace="String"
           prefix="String" />
    </namespaceTable>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments

Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.

### <a name="attributes"></a>Attributs

Aucun.

### <a name="child-elements"></a>Éléments enfants

|     | Description |
| --- | ----------- |
| [**\<Filtre >**](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md) | Définit un mappage préfixe-espace de noms utilisé pour les expressions XPath. |

### <a name="parent-elements"></a>Éléments parents

|     | Description |
| --- | ----------- |
| [**\<routage >**](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | Représente une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, ainsi que le routage des tables qui définissent les points de terminaison cible à envoyer des messages lorsqu’un filtre correspond. |

## <a name="see-also"></a>Voir aussi

<xref:System.ServiceModel.Routing.Configuration.NamespaceElementCollection?displayProperty=nameWithType>
