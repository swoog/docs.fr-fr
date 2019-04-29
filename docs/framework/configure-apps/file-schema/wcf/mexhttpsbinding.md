---
title: <mexHttpsBinding>
ms.date: 03/30/2017
ms.assetid: f2ed3774-78b9-4a15-b79b-655f1ad68b86
ms.openlocfilehash: 4e96c28ac9b372092d06538d24d165dde6c5fe48
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772539"
---
# <a name="mexhttpsbinding"></a>\<mexHttpsBinding>
Spécifie les paramètres pour une liaison utilisée dans le cadre de l’échange de messages WS-MetadataExchange (WS-MEX) sur HTTPS.  
  
 \<system.ServiceModel>  
\<bindings>  
\<mexHttpsBinding>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<mexHttpsBinding>
  <binding closeTimeout="TimeSpan"
            name="string"
            openTimeout="TimeSpan"
            receiveTimeout="TimeSpan"
            sendTimeout="TimeSpan">
  </binding>
</mexHttpsBinding>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`closeTimeout`|<xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de fermeture. Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>. La valeur par défaut est 00:01:00.|  
|`name`|Chaîne qui contient le nom de configuration de la liaison. Cette valeur doit être unique car elle permet d'identifier la liaison. Chaque liaison porte un `name` et a un attribut `namespace` qui l’identifient de façon unique dans les métadonnées du service. De plus, ce nom est unique parmi les liaisons du même type. Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom. Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).|  
|`openTimeout`|<xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'ouverture. Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>. La valeur par défaut est 00:01:00.|  
|`receiveTimeout`|<xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de réception. Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>. La valeur par défaut est 00:10:00.|  
|`sendTimeout`|<xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'envoi. Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>. La valeur par défaut est 00:01:00.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<bindings>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|Cet élément conserve une collection de liaisons standard et personnalisées.|  
  
## <a name="remarks"></a>Notes  
 Cette liaison est essentiellement une liaison `WSHttpBinding` qui prend en charge la sécurité au niveau du transport à l’aide de certificats. Pour plus d’informations sur la configuration et à l’aide de tel un point de terminaison, consultez [Comment : Configurer un personnalisé WS-Metadata Exchange liaison](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md), [Comment : Récupérer des métadonnées sur une liaison non - MEX](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md)et l’exemple [personnalisé sécuriser les métadonnées de point de terminaison](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexHttpsBinding%2A>
- <xref:System.ServiceModel.Configuration.MexHttpsBindingElement>
- [Guide pratique pour Publier les métadonnées d’un Service à l’aide d’un fichier de Configuration](../../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [Publication et récupération de métadonnées sur une liaison personnalisée](../../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)
- [Guide pratique pour Configurer un personnalisé WS-Metadata Exchange de liaison](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md)
- [Guide pratique pour Récupérer des métadonnées sur une liaison non - MEX](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md)
- [Point de terminaison de métadonnées sécurisé personnalisé](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md)
- [Métadonnées](../../../../../docs/framework/wcf/feature-details/metadata.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Configuration des liaisons fournies par le système](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [Utilisation de liaisons pour configurer des services et des clients](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](../../../../../docs/framework/misc/binding.md)
