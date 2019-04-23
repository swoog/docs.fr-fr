---
title: IMetaDataDispenserEx::GetOption, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.GetOption
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::GetOption
helpviewer_keywords:
- GetOption method [.NET Framework metadata]
- IMetaDataDispenserEx::GetOption method [.NET Framework metadata]
ms.assetid: d7f794e5-8e25-4d65-850a-7c34fbfce87d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fe9bc9aea4ceb0f5b5c03416f43894b482c3294e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59136628"
---
# <a name="imetadatadispenserexgetoption-method"></a>IMetaDataDispenserEx::GetOption, méthode
Obtient la valeur de l’option spécifiée pour la portée de métadonnées actuelle. L’option contrôle la gestion des appels à la portée de métadonnées actuelle.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetOption (  
    [in]  REFGUID         optionId,   
    [out] const VARIANT   *pValue  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `optionId`  
 [in] Pointeur vers un GUID qui spécifie l’option à récupérer. Consultez la section Notes pour obtenir la liste de GUID pris en charge.  
  
 `pValue`  
 [out] La valeur de l’option retournée. Le type de cette valeur sera une variante du type de l’option spécifiée.  
  
## <a name="remarks"></a>Notes  
 La liste suivante répertorie les GUID qui sont prises en charge pour cette méthode. Pour obtenir une description, consultez le [IMetaDataDispenserEx::SetOption](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-setoption-method.md) (méthode). Si `optionId` est pas dans cette liste, cette méthode retourne les HRESULT `E_INVALIDARG`, indiquant un paramètre incorrect.  
  
-   MetaDataCheckDuplicatesFor  
  
-   MetaDataRefToDefCheck  
  
-   MetaDataNotificationForTokenMovement  
  
-   MetaDataSetENC  
  
-   MetaDataErrorIfEmitOutOfOrder  
  
-   MetaDataGenerateTCEAdapters  
  
-   MetaDataLinkerOptions  
  
## <a name="requirements"></a>Configuration requise  
 **Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataDispenserEx, interface](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [IMetaDataDispenser, interface](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
