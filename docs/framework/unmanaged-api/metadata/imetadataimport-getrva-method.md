---
title: IMetaDataImport::GetRVA, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetRVA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetRVA
helpviewer_keywords:
- GetRVA method [.NET Framework metadata]
- IMetaDataImport::GetRVA method [.NET Framework metadata]
ms.assetid: ea422217-988b-4acd-b2db-c55357938275
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 126cc9d407e2653fdb3f4ea7b03fa05c24a572d0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629115"
---
# <a name="imetadataimportgetrva-method"></a>IMetaDataImport::GetRVA, méthode
Obtient l’adresse virtuelle relative (RVA) et les indicateurs d’implémentation de la méthode ou le champ représenté par le jeton spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRVA (  
   [in]  mdToken     tk,   
   [out] ULONG       *pulCodeRVA,   
   [out]  DWORD      *pdwImplFlags  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `tk`  
 [in] Un jeton de métadonnées MethodDef ou FieldDef qui représente l’objet de code pour retourner l’adresse RVA. Si le jeton est FieldDef, le champ doit être une variable globale.  
  
 `pulCodeRVA`  
 [out] Pointeur vers l’adresse virtuelle relative de l’objet de code représenté par le jeton.  
  
 `pdwImplFlags`  
 [out] Pointeur vers les indicateurs d’implémentation pour la méthode. Cette valeur est un masque de bits à partir de la [CorMethodImpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) énumération. La valeur de `pdwImplFlags` est valide uniquement si `tk` est un jeton MethodDef.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
