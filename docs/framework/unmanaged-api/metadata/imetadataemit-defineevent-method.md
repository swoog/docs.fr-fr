---
title: IMetaDataEmit::DefineEvent, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineEvent
helpviewer_keywords:
- IMetaDataEmit::DefineEvent method [.NET Framework metadata]
- DefineEvent method [.NET Framework metadata]
ms.assetid: cf064bac-9a9f-41c5-9e1d-108ff7af3afe
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 48055103b49b4c61bb7561f2d4aa6c8daae07ae2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59128906"
---
# <a name="imetadataemitdefineevent-method"></a>IMetaDataEmit::DefineEvent, méthode
Crée une définition pour un événement avec la signature de métadonnées spécifiée et obtient un jeton pour cette définition de l’événement.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineEvent (   
    [in]  mdTypeDef    td,   
    [in]  LPCWSTR      szEvent,   
    [in]  DWORD        dwEventFlags,   
    [in]  mdToken      tkEventType,   
    [in]  mdMethodDef  mdAddOn,   
    [in]  mdMethodDef  mdRemoveOn,   
    [in]  mdMethodDef  mdFire,   
    [in]  mdMethodDef  rmdOtherMethods[],   
    [out] mdEvent      *pmdEvent   
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `td`  
 [in] Le jeton pour la classe cible ou l’interface. Il s’agit soit un `mdTypeDef` ou `mdTypeDefNil` jeton.  
  
 `szEvent`  
 [in] Le nom de l’événement.  
  
 `dwEventFlags`  
 [in] Indicateurs d’événement.  
  
 `tkEventType`  
 [in] Le jeton pour la classe d’événements. Il s’agit d’un `mdTypeDef`, un `mdTypeRef`, ou un `mdTokenNil` jeton.  
  
 `mdAddOn`  
 [in] La méthode utilisée pour s’abonner à l’événement, ou null.  
  
 `mdRemoveOn`  
 [in] La méthode utilisée pour annuler l’abonnement à l’événement, ou null.  
  
 `mdFire`  
 [in] La méthode utilisée (par une classe dérivée) pour déclencher l’événement.  
  
 `rmdOtherMethods[]`  
 [in] Un tableau de jetons pour les autres méthodes associées à l’événement. Le tableau se termine par un `mdMethodDefNil` jeton.  
  
 `pmdEvent`  
 [out] Le jeton de métadonnées assigné à l’événement.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
