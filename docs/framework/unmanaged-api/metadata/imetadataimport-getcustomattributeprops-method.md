---
title: IMetaDataImport::GetCustomAttributeProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetCustomAttributeProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetCustomAttributeProps
helpviewer_keywords:
- GetCustomAttributeProps method [.NET Framework metadata]
- IMetaDataImport::GetCustomAttributeProps method [.NET Framework metadata]
ms.assetid: 6eefb243-a281-41c1-bcdc-7e17513bc446
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c27a55166ebc055f324ec45ba6dfd835c8b8bbf6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59075741"
---
# <a name="imetadataimportgetcustomattributeprops-method"></a>IMetaDataImport::GetCustomAttributeProps, méthode
Obtient la valeur de l'attribut personnalisé, en fonction de son jeton de métadonnées.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetCustomAttributeProps (  
   [in]            mdCustomAttribute   cv,  
   [out, optional] mdToken             *ptkObj,  
   [out, optional] mdToken             *ptkType,  
   [out, optional] void const          **ppBlob,  
   [out, optional] ULONG               *pcbSize  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `cv`  
 [in] Jeton de métadonnées représentant l'attribut personnalisé à récupérer.  
  
 `ptkObj`  
 [out, optional] Jeton de métadonnées représentant l'objet que l'attribut personnalisé modifie. Cette valeur peut correspondre à tout type de jeton de métadonnées, à l'exception de `mdCustomAttribute`.  
  
 `ptkType`  
 [out, optional] Jeton de métadonnées `mdMethodDef` ou `mdMemberRef` représentant le <xref:System.Type> de l'attribut personnalisé retourné.  
  
 `ppBlob`  
 [out, optional] Pointeur vers un tableau de données correspondant à la valeur de l'attribut personnalisé.  
  
 `pcbSize`  
 [out, optional] Taille en octets des données retournées dans *`ppBlob`.  
  
## <a name="remarks"></a>Notes  
 Un attribut personnalisé est stocké sous forme d'un tableau de données, le format qui est compris par le moteur de métadonnées.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
