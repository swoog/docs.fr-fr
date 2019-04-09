---
title: Vue d'ensemble de l'intégration à des applications COM
ms.date: 03/30/2017
helpviewer_keywords:
- COM [WCF], integration overview
ms.assetid: 02c5697f-6e2e-47d6-b715-f3a28aebfbd5
ms.openlocfilehash: 182e5f41498d8f5e3fcbc4b84aa7e86b67ce3ccc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59087623"
---
# <a name="integrating-with-com-applications-overview"></a>Vue d'ensemble de l'intégration à des applications COM
Windows Communication Foundation (WCF) fournit au développeur de code managé avec un environnement riche pour la création d’applications connectées. Toutefois, si vous avez beaucoup investi dans le code COM non managé et que vous ne souhaitez pas migrer, vous pouvez toujours intégrer les services Web WCF directement dans votre code existant à l’aide du moniker de service WCF. Le moniker de service peut être utilisé à partir d'une large gamme d'environnements de développement COM, tels qu'Office VBA, Visual Basic 6.0 ou Visual C++ 6.0.  
  
> [!NOTE]
>  Le moniker de service utilise un canal de communication WCF pour toutes les communications. Les mécanismes de sécurité et d'identification de ce canal diffèrent de ceux utilisés sur les proxys standard COM et DCOM. En outre, étant donné que le moniker de service utilise un canal de communication WCF le délai par défaut est une minute pour tous les appels.  
  
 Le moniker de service est utilisé avec le `GetObject` afin de fournir aux développeurs non managé une approche fortement typée, spécifique au COM pour appeler des services Web WCF. Cela nécessite un local, la définition visible par COM de contrat de service Web de WCF et la liaison qui doit être utilisé. Comme les autres clients WCF, le moniker de service doit construire un canal typé pour le service, bien que cette construction devienne visible par le programmeur COM lors du premier appel de méthode.  
  
 En commun avec d’autres clients WCF, lors de l’utilisation du moniker, les applications spécifier l’adresse, la liaison et le contrat pour communiquer avec un service. Le contrat peut être spécifié (au choix) comme suit :  
  
-   Contrat typé : le contrat est enregistré sur l'ordinateur client sous la forme d'un type visible par COM.  
  
-   Contrat WSDL : le contrat est fourni sous forme de document WSDL.  
  
-   Contrat MEX : le contrat est récupéré pendant l'exécution depuis un point de terminaison d'échange de métadonnées (Metadata Exchange, MEX).  
  
## <a name="parameters-supported-by-the-service-moniker"></a>Paramètres pris en charge par le moniker de service  
 Le tableau suivant contient les paramètres pris en charge par le moniker de service.  
  
|Paramètre|Description|  
|---------------|-----------------|  
|`address`|Adresse URL du service.|  
|`binding`|Nom de la section de liaison à partir de la configuration d'application.|  
|`bindingConfiguration`|Instance de liaison nommée à partir de la section de liaison nommée.|  
|`contract`|Identificateur d'interface (IID) qui représente le contrat de service ou le nom de contrat (obtenu à partir de l'échange MEX).|  
|`wsdl`|Document WSDL qui offre une autre définition pour le contrat.|  
|`spnIdentity`|Identité de nom principal de serveur (Server Principal Name, SPN) à utiliser pour communiquer avec le service.|  
|`upnIdentity`|Identité de nom principal d'utilisateur (User Principal Name, UPN) à utiliser pour communiquer avec le service.|  
|`dnsIdentity`|Identité DNS à utiliser pour communiquer avec le service.|  
|`mexAddress`|Adresse URL du point de terminaison MEX du service.|  
|`mexBinding`|Nom de section de liaison depuis la configuration d'application avec laquelle se connecter au point de terminaison MEX.|  
|`mexBindingConfiguration`|Instance de liaison nommée à partir de la section de liaison nommée avec laquelle se connecter au point de terminaison MEX.|  
|`bindingNamespace`|Espace de noms du nom de section de liaison obtenu à partir de l’échange MEX récupéré.|  
|`contractNamespace`|Espace de noms du contrat obtenu à partir de l'échange MEX récupéré.|  
|`mexSpnIdentity`|Identité SPN à utiliser pour communiquer avec le point de terminaison MEX.|  
|`mexUpnIdentity`|Identité UPN à utiliser pour communiquer avec le point de terminaison MEX.|  
|`mexDnsIdentity`|Identité DNS à utiliser pour communiquer avec le point de terminaison MEX.|  
|`serializer`|Indiquez le type de sérialiseur utilisé : « xml » ou « contrat de données ».|  
  
> [!NOTE]
>  Même lorsque utilisé avec les clients entièrement basés sur COM, le moniker de service nécessite WCF et la prise en charge de .NET Framework 2.0 doit être installé sur l’ordinateur client. Il est également essentiel que les applications clientes qui utilisent le moniker de service chargent la version appropriée de l'exécution .NET Framework. Lorsque le moniker de service est utilisé dans le cadre d'applications Office, un fichier de configuration peut s'avérer nécessaire afin d'assurer la chargement de la version d'infrastructure adéquate. Par exemple, pour Excel, vous devez insérer le texte suivant dans un fichier Excel.exe.config, puis enregistrer ce fichier dans le même répertoire que le fichier Excel.exe :  
>   
>  `<?xml version="1.0" encoding="utf-8"?>`  
>   
>  `<configuration xmlns=` `http://schemas.microsoft.com/.NetConfiguration/v2.0` `>`  
>   
>  `<startup>`  
>   
>  `<requiredRuntime version="v2.0.50727" />`  
>   
>  `</startup>`  
>   
>  `</configuration>`  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : inscrire et configurer un moniker de service](../../../../docs/framework/wcf/feature-details/how-to-register-and-configure-a-service-moniker.md)
