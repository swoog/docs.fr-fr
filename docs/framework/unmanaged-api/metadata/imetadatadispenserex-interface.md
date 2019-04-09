---
title: IMetaDataDispenserEx, interface
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx
helpviewer_keywords:
- IMetaDataDispenserEx interface [.NET Framework metadata]
ms.assetid: 78b3629e-77a2-4406-89c3-56b5cc2c4594
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 96475086b1244ae75ed692dd10cb693af0be9af7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59186951"
---
# <a name="imetadatadispenserex-interface"></a>IMetaDataDispenserEx, interface
Étend la [IMetaDataDispenser, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md) interface pour fournir la possibilité de contrôler le fonctionnement de l’API de métadonnées sur la portée de métadonnées actuelle.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[FindAssembly, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-findassembly-method.md)|Cette méthode n’est pas implémentée. Si elle est appelée, elle retourne E_NOTIMPL.|  
|[FindAssemblyModule, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-findassemblymodule-method.md)|Cette méthode n’est pas implémentée. Si elle est appelée, elle retourne E_NOTIMPL.|  
|[GetCORSystemDirectory, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-getcorsystemdirectory-method.md)|Obtient le répertoire qui contient le common language runtime (CLR) actuel. Cette méthode est prise en charge uniquement pour une utilisation par les débogueurs out-of-process. Si elle est appelée à partir d’un autre composant, elle retournera E_NOTIMPL.|  
|[GetOption, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-getoption-method.md)|Obtient la valeur de l’option spécifiée pour la portée de métadonnées actuelle. L’option contrôle la gestion des appels à la portée de métadonnées actuelle.|  
|[OpenScopeOnITypeInfo, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-openscopeonitypeinfo-method.md)|Cette méthode n’est pas implémentée. Si elle est appelée, elle retourne E_NOTIMPL.|  
|[SetOption, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-setoption-method.md)|Définit l’option spécifiée à une valeur donnée pour la portée de métadonnées actuelle. L’option contrôle la gestion des appels à la portée de métadonnées actuelle.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [IMetaDataDispenser, interface](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
- [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
