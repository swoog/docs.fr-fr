---
title: IMetaDataImport::GetMemberRefProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMemberRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMemberRefProps
helpviewer_keywords:
- GetMemberRefProps method [.NET Framework metadata]
- IMetaDataImport::GetMemberRefProps method [.NET Framework metadata]
ms.assetid: 0ea73055-ece0-4151-a094-414c88ef8941
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a2c431abb7a4a872454b9c2689ee195ed36ef236
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59177007"
---
# <a name="imetadataimportgetmemberrefprops-method"></a>IMetaDataImport::GetMemberRefProps, méthode
Obtient les métadonnées associées au membre référencé par le jeton spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetMemberRefProps (  
   [in]  mdMemberRef       mr,   
   [out] mdToken           *ptk,   
   [out] LPWSTR            szMember,   
   [in]  ULONG             cchMember,   
   [out] ULONG             *pchMember,   
   [out] PCCOR_SIGNATURE   *ppvSigBlob,   
   [out] ULONG             *pbSig   
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `mr`  
 [in] Le jeton MemberRef pour retourner les métadonnées associées.  
  
 `ptk`  
 [out] Jeton TypeDef ou TypeRef ou TypeSpec qui représente la classe qui déclare le membre, ou un jeton ModuleRef qui représente la classe de module qui déclare le membre, ou MethodDef qui représente le membre.  
  
 `szMember`  
 [out] Un mémoire tampon de chaîne pour le nom du membre.  
  
 `cchMember`  
 [in] La taille demandée en caractères larges de `szMember`.  
  
 `pchMember`  
 [out] La taille retournée en caractères larges de `szMember`.  
  
 `ppvSibBlob`  
 [out] Pointeur vers la signature de métadonnées binaires pour le membre.  
  
 `pbSig`  
 [out] La taille en octets de `ppvSigBlob`.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
