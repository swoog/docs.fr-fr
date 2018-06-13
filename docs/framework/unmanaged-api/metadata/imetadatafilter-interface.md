---
title: IMetaDataFilter, interface
ms.date: 03/30/2017
api_name:
- IMetaDataFilter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataFilter
helpviewer_keywords:
- IMetaDataFilter interface [.NET Framework metadata]
ms.assetid: ec0856ef-8c56-40ba-bf60-86e0ce8b337f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ad77aba02c819749794534ca2ecd478661bc363f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444979"
---
# <a name="imetadatafilter-interface"></a>IMetaDataFilter, interface
Fournit des méthodes pour marquer et filtrer des jetons de métadonnées pour éviter de répéter des actions qui ont déjà été prises.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[IsTokenMarked, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-istokenmarked-method.md)|Obtient une valeur qui indique si le jeton de métadonnées spécifié a été traité.|  
|[MarkToken, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-marktoken-method.md)|Définit une valeur qui indique que le jeton de métadonnées spécifié a été traité.|  
|[UnmarkAll, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-unmarkall-method.md)|Supprime les marques de traitement de tous les jetons dans la portée de métadonnées actuelle.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
