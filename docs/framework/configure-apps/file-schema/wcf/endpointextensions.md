---
title: <endpointExtensions>
ms.date: 03/30/2017
ms.assetid: 33396e0a-1fae-4616-b822-923584eebfd1
ms.openlocfilehash: 12ac8d9a7b0ed584fb1308e56d197a03b1c53e51
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61700876"
---
# <a name="endpointextensions"></a>\<endpointExtensions>
Cette section inscrit un nouveau point de terminaison standard dans la section des extensions du fichier de configuration machine ou d'application. Vous pouvez ajouter un point de terminaison standard à cette collection à l’aide du mot clé `add` et affecter à l’attribut `type` de l’élément le type du point de terminaison et à l’attribut `name` le nom du point de terminaison standard.  
  
 L'exemple suivant utilise l'élément `add`, ainsi que l'attribut `name`, pour ajouter un point de terminaison standard à la section `<endpointExtensions>` du fichier de configuration.  
  
```xml  
<system.serviceModel>
  <extensions>
    <endpointExtensions>
      <add name="udpDiscoveryEndpoint"
           type="System.Discovery.UdpEndpointCollectionElement, System.Discovery.dll, Version=1.0.0.0, Culture=neutral, PublicKeyToken=ffffffffffffffff"/>
    </endpointExtensions>
  </extensions>
</system.serviceModel>
```  
  
 Après avoir inscrit le point de terminaison standard, vous pouvez l'utiliser comme indiqué dans l'exemple suivant. Dans le [ \<point de terminaison >](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-element.md) élément, le `kind` attribut spécifie le type de point de terminaison standard qui a été enregistré dans le `<endpointExtensions>` section. Le `endpointConfiguration` attribut sera identique à la `name` attribut de l’élément de configuration du point de terminaison standard dans la `<standardEndpoints>` section.  
  
```xml  
<system.serviceModel>
  <services>
    <service name="Service1">
      <endpoint kind="udpDiscoveryEndpoint"
                endpointConfiguration="udpConfig" />
    </service>
  </services>
  <standardEndpoints>
    <udpDiscoveryEndpoint>
      <standardEndpoint name="udpConfig"
                        multicastAddress="soap.udp://239.255.255.250:3703"
                        ... />
    </udpDiscoveryEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
