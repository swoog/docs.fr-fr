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
ms.openlocfilehash: ce94765467899ac7c906b0dfcdf0ceb78c659b5f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448202"
---
# <a name="imetadataemitdefineevent-method"></a>IMetaDataEmit::DefineEvent, méthode
Crée une définition pour un événement avec la signature de métadonnées spécifiée et obtient un jeton pour cette définition d’événement.  
  
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
  
#### <a name="parameters"></a>Paramètres  
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
 [in] Tableau de jetons pour les autres méthodes associées à l’événement. Le tableau se termine par un `mdMethodDefNil` jeton.  
  
 `pmdEvent`  
 [out] Le jeton de métadonnées assigné à l’événement.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
