---
title: '&lt;webHttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 84179d77-825d-44b9-895a-ab08e7aa044d
ms.openlocfilehash: b75762fdef4f0c71c58542be9f674da291fcf23f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54656568"
---
# <a name="ltwebhttpbindinggt"></a>&lt;webHttpBinding&gt;
Définit un élément de liaison qui est utilisé pour configurer des points de terminaison pour les services Web de Windows Communication Foundation (WCF) qui répondent aux requêtes HTTP au lieu de messages SOAP.  
  
\<system.ServiceModel>  
\<bindings>  
\<webHttpBinding>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<webHttpBinding>
  <binding allowCookies="Boolean"
           bypassProxyOnLocal="Boolean"
           closeTimeout="TimeSpan"
           hostNameComparisonMode="StrongWildCard/Exact/WeakWildcard"
           maxBufferPoolSize="integer"
           maxBufferSize="integer"
           maxReceivedMessageSize="Integer"
           name="string"
           openTimeout="TimeSpan"
           proxyAddress="URI"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan"
           transferMode="Buffered/Streamed/StreamedRequest/StreamedResponse"
           useDefaultWebProxy="Boolean"
           writeEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding">
    <security mode="None/Transport/TransportCredentialOnly">
      <transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
                 proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
                 realm="string" />
    </security>
    <readerQuotas maxArrayLength="Integer"
                  maxBytesPerRead="Integer"
                  maxDepth="Integer"
                  maxNameTableCharCount="Integer"
                  maxStringContentLength="Integer" />
  </binding>
</webHttpBinding>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|allowCookies|Valeur booléenne qui indique si le client accepte les cookies et les propage dans de futures demandes. La valeur par défaut est false.<br /><br /> Vous pouvez utiliser cette propriété lorsque vous interagissez avec les services Web ASMX qui utilisent des cookies. De cette manière, vous avez la certitude que les cookies retournés par le serveur sont automatiquement copiés dans toutes les futures demandes du client pour ce service.|  
|bypassProxyOnLocal|Valeur booléenne qui indique s'il faut ignorer le serveur proxy pour les adresses locales. La valeur par défaut est `false`.|  
|closeTimeout|<xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de fermeture. Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>. La valeur par défaut est 00:01:00.|  
|hostnameComparisonMode|Spécifie le mode de comparaison du nom d'hôte HTTP utilisé pour analyser des URI. Cet attribut est de type <xref:System.ServiceModel.HostNameComparisonMode>, ce qui indique si le nom d'hôte est utilisé pour atteindre le service en cas de correspondance sur l'URI. La valeur par défaut est <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, qui ignore le nom d'hôte dans la correspondance.|  
|maxBufferPoolSize|Entier qui spécifie la taille maximale du pool de mémoires tampons pour cette liaison. La valeur par défaut est 524 288 octets (512 x 1024). De nombreuses parties de Windows Communication Foundation (WCF) utilisent des mémoires tampons. La création et la destruction des mémoires tampons à chaque utilisation sont chères, tout comme leur nettoyage. Avec les pools de mémoires tampons, vous pouvez prendre une mémoire tampon du pool, l'utiliser et la retourner au pool une fois que vous avez terminé. Ainsi, la surcharge de la création et de la destruction des mémoires tampons est évitée.|  
|maxBufferSize|Entier qui spécifie la quantité de mémoire maximale allouée pour une utilisation par le gestionnaire des tampons de messages qui reçoivent des messages du canal. La valeur par défaut est de 524 288 (0x80000) octets.|  
|maxReceivedMessageSize|Entier positif qui spécifie la taille maximale du message, en octets, y compris les en-têtes, pouvant être reçu sur un canal configuré avec cette liaison. L'expéditeur d'un message qui dépasse cette limite se verra notifier une erreur. Ce dernier abandonne le message et crée une entrée d'événement dans le journal de suivi. La valeur par défaut est 65536. **Remarque :**  L'augmentation de cette valeur uniquement n'est pas suffisant en mode compatible ASP.NET. Vous devez également augmenter la valeur de `httpRuntime` (consultez [httpRuntime, élément (schéma des paramètres ASP.NET)](https://msdn.microsoft.com/library/e9b81350-8aaf-47cc-9843-5f7d0c59f369)).|  
|name|Chaîne qui contient le nom de configuration de la liaison. Cette valeur doit être unique car elle permet d'identifier la liaison. Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom. Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).|  
|openTimeout|<xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'ouverture. Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>. La valeur par défaut est 00:01:00.|  
|proxyAddress|URI qui spécifie l'adresse du proxy HTTP. Si `useSystemWebProxy` est `true`, ce paramètre doit avoir la valeur `null`. La valeur par défaut est `null`.|  
|receiveTimeout|<xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération de réception. Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>. La valeur par défaut est 00:01:00.|  
|sendTimeout|<xref:System.TimeSpan> qui spécifie l'intervalle de temps prévu pour la réalisation d'une opération d'envoi. Cette valeur doit être supérieure ou égale à <xref:System.TimeSpan.Zero>. La valeur par défaut est 00:01:00.|  
|transferMode.|Valeur <xref:System.ServiceModel.TransferMode> qui indique si le service configuré avec les liaisons utilise des modes de transfert de messages en continu ou en mémoire tampon (ou les deux). La valeur par défaut est `Buffered`.|  
|useDefaultWebProxy|Valeur booléenne qui spécifie si le proxy HTTP du système configuré automatiquement est utilisé. La valeur par défaut est `true`.|  
|writeEncoding|Spécifie l'encodage de caractères utilisé pour le texte du message. Les valeurs valides sont les suivantes :<br /><br /> UnicodeFffeTextEncoding : Codage Unicode BigEndian.<br /><br /> Utf16TextEncoding : encodage 16 bits.<br /><br /> Utf8TextEncoding : encodage 8 bits.<br /><br /> La valeur par défaut est Utf8TextEncoding.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<readerQuotas>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|Définit les contraintes de la complexité des messages POX qui peuvent être traités par les points de terminaison configurés avec cette liaison. Cet élément est de type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-webhttpbinding.md)|Définit les paramètres de sécurité de la liaison. Cet élément est de type <xref:System.ServiceModel.Configuration.WebHttpSecurityElement>.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<bindings>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|Cet élément conserve une collection de liaisons standard et personnalisées.|  
  
## <a name="remarks"></a>Notes  
 Le modèle de programmation Web WCF permet aux développeurs d’exposer des services Web WCF via des requêtes HTTP qui utilisent des « plain old XML » style (POX) de messagerie au lieu de la messagerie SOAP. Pour les clients communiquent avec un service à l’aide de requêtes HTTP, un point de terminaison du service doit être configuré avec le [ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md) qui a le \<WebHttpBehavior > attaché à ce dernier.  
  
 Prend en charge dans WCF pour la syndication et ASP. Intégration d’AJAX est construit au sommet du modèle de programmation Web. Pour plus d’informations sur le modèle, consultez [modèle de programmation WCF Web HTTP](../../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.WebHttpBinding>
- <xref:System.ServiceModel.Configuration.WebHttpBindingElement>
- [Modèle de programmation HTTP web WCF](../../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Configuration des liaisons fournies par le système](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [Utilisation de liaisons pour configurer des services et des clients](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](../../../../../docs/framework/misc/binding.md)
