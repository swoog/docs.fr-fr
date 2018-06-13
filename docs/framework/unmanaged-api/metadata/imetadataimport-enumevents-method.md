---
title: IMetaDataImport::EnumEvents, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumEvents
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumEvents
helpviewer_keywords:
- IMetaDataImport::EnumEvents method [.NET Framework metadata]
- EnumEvents method [.NET Framework metadata]
ms.assetid: e1efedcb-3dd7-42ae-a399-21c24728aec5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 608b4a7d147124ede60e9d81f91600dfdaad0a65
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446494"
---
# <a name="imetadataimportenumevents-method"></a>IMetaDataImport::EnumEvents, méthode
Énumère les jetons de définition d'événements pour le jeton TypeDef spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumEvents (   
   [in, out] HCORENUM    *phEnum,   
   [in]      mdTypeDef   td,   
   [out]     mdEvent     rEvents[],   
   [in]      ULONG       cMax,  
   [out]    ULONG        *pcEvents  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `phEnum`  
 [dans, out] Pointeur vers l’énumérateur.  
  
 `td`  
 [in] Le jeton TypeDef dont les définitions d’événement doivent être énumérés.  
  
 `rEvents`  
 [out] Tableau d’événements retournés.  
  
 `cMax`  
 [in] Taille maximale du tableau `rEvents`.  
  
 `pcEvents`  
 [out] Le nombre réel d’événements retournés dans `rEvents`.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|`EnumEvents` retourné avec succès.|  
|`S_FALSE`|Il n’existe pas d’événements à énumérer. Dans ce cas, `pcEvents` est égal à zéro.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
