---
title: IMetaDataImport2::GetMethodSpecProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetMethodSpecProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetMethodSpecProps
helpviewer_keywords:
- GetMethodSpecProps method [.NET Framework metadata]
- IMetaDataImport2::GetMethodSpecProps method [.NET Framework metadata]
ms.assetid: 9544b711-e669-4eaf-8630-ee862e5e4489
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3249ad76c428752c91540e135bc978d3fe835de1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="imetadataimport2getmethodspecprops-method"></a>IMetaDataImport2::GetMethodSpecProps, méthode
Obtient le jeton de la signature de métadonnées de la méthode référencée par le MethodSpec spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetMethodSpecProps (  
   [in]  mdMethodSpec     mi,  
   [out] mdToken          *tkParent,  
   [out] PCCOR_SIGNATURE  *ppvSigBlob,   
   [out] ULONG            *pcbSigBlob  
);   
```  
  
#### <a name="parameters"></a>Paramètres  
 `mi`  
 [in] Jeton MethodSpec qui représente l’instanciation de la méthode.  
  
 `tkParent`  
 [out] Pointeur vers le jeton MethodDef ou MethodRef qui représente la définition de méthode.  
  
 `ppvSigBlob`  
 [out] Pointeur vers la signature de métadonnées binaires de la méthode.  
  
 `pcbSigBlob`  
 [out] La taille, en octets, de `ppvSigBlob`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)  
 [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
