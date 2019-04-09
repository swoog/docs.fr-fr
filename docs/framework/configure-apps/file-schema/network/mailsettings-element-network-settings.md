---
title: <mailSettings> Élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#mailSettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings
helpviewer_keywords:
- mailSettings element
- <mailSettings> element
ms.assetid: 54f0f153-17e5-4f49-afdc-deadb940c9c1
ms.openlocfilehash: 54fb68ab0bf8aa2665d70391350c626131ccb4bc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59180621"
---
# <a name="mailsettings-element-network-settings"></a>\<mailSettings >, élément (paramètres réseau)
Configure les options d’envoi du courrier.  

\<configuration>  
\<system.net>  
\<mailSettings>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<mailSettings>
  <smtp>...</smtp>  
</mailSettings>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Attribut|Description|  
|---------------|-----------------|  
|[\<SMTP >, élément (paramètres réseau)](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|Configure les options de Simple Mail Transport Protocol.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[\<system.Net >, élément (paramètres réseau)](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.|  
  
## <a name="example"></a>Exemple  
 L’exemple suivant spécifie les paramètres SMTP appropriés pour envoyer un e-mail à l’aide des informations d’identification du réseau par défaut.  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="Network">  
        <network  
          host="localhost"  
          port="25"  
          defaultCredentials="true"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Net.Mail.SmtpClient>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
