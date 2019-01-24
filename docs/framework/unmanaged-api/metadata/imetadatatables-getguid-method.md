---
title: IMetaDataTables::GetGuid, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetGuid
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetGuid
helpviewer_keywords:
- GetGuid method [.NET Framework metadata]
- IMetaDataTables::GetGuid method [.NET Framework metadata]
ms.assetid: a3546316-e24d-417f-9909-e45d42c9d471
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bb1e9b2dc76653e544ec5e97bf0bbc996bbc8826
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54547190"
---
# <a name="imetadatatablesgetguid-method"></a>IMetaDataTables::GetGuid, méthode
Obtient un GUID à partir de la ligne à l’index spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetGuid (   
    [in]  ULONG       ixGuid,  
    [out] const GUID  **ppGUID  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ixGuid`  
 [in] L’index de la ligne à partir duquel obtenir le GUID.  
  
 `ppGuid`  
 [out] Pointeur vers un pointeur vers le GUID.  
  
## <a name="remarks"></a>Notes  
 Nous déconseillons l’utilisation de cette méthode, car elle ne retourne pas de résultats cohérents. Pour plus d’informations sur le tableau GUID, consultez la documentation de Common Language Infrastructure (CLI), en particulier « Partition II : Metadata Definition and Semantics ». La documentation est disponible en ligne. Consultez [ECMA C# and Common Language Infrastructure Standards](https://go.microsoft.com/fwlink/?LinkID=99212) sur MSDN et [Standard ECMA-335 - Common Language Infrastructure (CLI)](https://go.microsoft.com/fwlink/?LinkID=65552) sur le site web d’Ecma International.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataTables, interface](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [IMetaDataTables2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
