---
title: IAppDomainSetup, interface
ms.date: 03/30/2017
api_name:
- IAppDomainSetup
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IAppDomainSetup
helpviewer_keywords:
- IAppDomainSetup interface [.NET Framework hosting]
ms.assetid: 1844da85-c031-40bf-bea4-1a3d12a36c8c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bbde873481aea9de94862117a99079301965f33c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59220069"
---
# <a name="iappdomainsetup-interface"></a>IAppDomainSetup, interface
Fournit des propriétés qui permettent à l’hôte configurer un <xref:System.AppDomain?displayProperty=nameWithType> type avant d’appeler le [ICorRuntimeHost::CreateDomainEx](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-createdomainex-method.md) méthode pour le créer.  
  
## <a name="properties"></a>Properties  
  
|Propriété|Description|  
|--------------|-----------------|  
|<xref:System.AppDomainSetup.ApplicationBase%2A>|Obtient ou définit le nom du répertoire qui contient l’application.|  
|<xref:System.AppDomainSetup.ApplicationName%2A>|Obtient ou définit le nom de l'application.|  
|<xref:System.AppDomainSetup.CachePath%2A>|Obtient ou définit le nom d’une zone spécifique à l’application où les fichiers sont copiés de clichés instantanés.|  
|<xref:System.AppDomainSetup.ConfigurationFile%2A>|Obtient ou définit le nom du fichier de configuration pour une application.|  
|<xref:System.AppDomainSetup.DynamicBase%2A>|Obtient ou définit le nom du répertoire où les fichiers générés dynamiquement sont stockées et accessibles.|  
|<xref:System.AppDomainSetup.LicenseFile%2A>|Obtient ou définit le chemin d’accès du fichier de licence qui est associé à ce domaine.|  
|<xref:System.AppDomainSetup.PrivateBinPath%2A>|Obtient ou définit la liste des répertoires associés le <xref:System.AppDomainSetup.ApplicationBase%2A> directory pour détecter les assemblys privés.|  
|<xref:System.AppDomainSetup.PrivateBinPathProbe%2A>|Obtient ou définit une valeur de chaîne qui inclut ou exclut <xref:System.AppDomainSetup.ApplicationBase%2A> du chemin de recherche pour l’application.|  
|<xref:System.AppDomainSetup.ShadowCopyDirectories%2A>|Obtient ou définit les noms des répertoires qui contiennent des assemblys pour être une copie fantôme.|  
|<xref:System.AppDomainSetup.ShadowCopyFiles%2A>|Obtient ou définit une chaîne qui indique si la copie de clichés instantanés est activée ou désactivée. Les valeurs valides sont « true » ou « false ».|  
  
## <a name="remarks"></a>Notes  
 Le `IAppDomainSetup` interface correspond à managé <xref:System.IAppDomainSetup> d’interface, ce qui le <xref:System.AppDomainSetup> type implémente. Consultez <xref:System.IAppDomainSetup?displayProperty=nameWithType> pour une description détaillée de ses propriétés.  
  
 `IAppDomainSetup` représente les informations de liaison d’assembly qui peuvent être ajoutées à un <xref:System.AppDomain> instance avant sa création. Par exemple, un hôte peut définir le <xref:System.AppDomainSetup.ApplicationBase%2A> propriété pour établir un répertoire racine dans lequel le common language runtime (CLR) tente de détecter les assemblys managés.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.AppDomain>
- <xref:System.AppDomainSetup>
- <xref:System.IAppDomainSetup>
- [Interfaces d'hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
