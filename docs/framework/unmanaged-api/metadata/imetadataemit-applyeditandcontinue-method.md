---
title: IMetaDataEmit::ApplyEditAndContinue, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.ApplyEditAndContinue
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::ApplyEditAndContinue
helpviewer_keywords:
- ApplyEditAndContinue method [.NET Framework metadata]
- IMetaDataEmit::ApplyEditAndContinue method [.NET Framework metadata]
ms.assetid: 35991289-f389-495d-8caa-a6384fb1d557
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d0558154dc64ca95a691f36fb67586d570caa888
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57484990"
---
# <a name="imetadataemitapplyeditandcontinue-method"></a>IMetaDataEmit::ApplyEditAndContinue, méthode
Met à jour la portée d’assembly actuelle avec les modifications apportées dans les métadonnées spécifiées.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ApplyEditAndContinue (   
    [in]  IUnknown    *pImport  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pImport`  
 \[dans\] pointeur vers un [IUnknown](/cpp/atl/iunknown) objet qui représente les métadonnées delta à partir du fichier exécutable portable (PE).
  
 Les métadonnées delta sont le bloc de métadonnées qui inclut les modifications qui ont été apportées à la copie des métadonnées réelles du module.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
